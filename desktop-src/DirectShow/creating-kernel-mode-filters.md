---
description: 建立 Kernel-Mode 篩選
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: 建立 Kernel-Mode 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109777"
---
# <a name="creating-kernel-mode-filters"></a><span data-ttu-id="ff86a-103">建立 Kernel-Mode 篩選</span><span class="sxs-lookup"><span data-stu-id="ff86a-103">Creating Kernel-Mode Filters</span></span>

<span data-ttu-id="ff86a-104">某些核心模式篩選器無法透過 **CoCreateInstance** 建立，因此沒有 clsid。</span><span class="sxs-lookup"><span data-stu-id="ff86a-104">Certain kernel-mode filters cannot be created through **CoCreateInstance**, and thus do not have CLSIDs.</span></span> <span data-ttu-id="ff86a-105">這些篩選準則包括 [t/接收到接收轉換器](tee-sink-to-sink-converter.md)、副本 [編碼器](cc-decoder-filter.md) 篩選器，以及 [WST 編解碼器](wst-codec-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="ff86a-105">These filters include the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md), the [CC Decoder](cc-decoder-filter.md) filter, and the [WST Codec](wst-codec-filter.md) filter.</span></span> <span data-ttu-id="ff86a-106">若要建立這些篩選準則的其中之一，請使用 [系統裝置列舉](system-device-enumerator.md) 值物件，並依篩選器的名稱進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="ff86a-106">To create one of these filters, use the [System Device Enumerator](system-device-enumerator.md) object and search by the filter's name.</span></span>

1.  <span data-ttu-id="ff86a-107">建立系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="ff86a-107">Create the System Device Enumerator.</span></span>
2.  <span data-ttu-id="ff86a-108">使用篩選準則分類的 CLSID 來呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff86a-108">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method with the CLSID of the filter category for that filter.</span></span> <span data-ttu-id="ff86a-109">這個方法會建立篩選準則分類的列舉值。</span><span class="sxs-lookup"><span data-stu-id="ff86a-109">This method creates an enumerator for the filter category.</span></span> <span data-ttu-id="ff86a-110"> (*列舉* 值只是一個物件，該物件會使用已定義的 COM 介面傳回其他物件的清單。 ) 列舉值會傳回 **IMoniker** 指標，代表該類別中的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ff86a-110">(An *enumerator* is simply an object that returns a list of other objects, using a defined COM interface.) The enumerator returns **IMoniker** pointers, which represent the filters in that category.</span></span>
3.  <span data-ttu-id="ff86a-111">針對每個標記，呼叫 **IMoniker：： BindToStorage** 來取得 **IPropertyBag** 介面。</span><span class="sxs-lookup"><span data-stu-id="ff86a-111">For each moniker, call **IMoniker::BindToStorage** to get an **IPropertyBag** interface.</span></span>
4.  <span data-ttu-id="ff86a-112">呼叫 **IPropertyBag：： Read** 以取得篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff86a-112">Call **IPropertyBag::Read** to get the name of the filter.</span></span>
5.  <span data-ttu-id="ff86a-113">如果名稱相符，請呼叫 **IMoniker：： BindToObject** 來建立篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ff86a-113">If the name matches, call **IMoniker::BindToObject** to create the filter.</span></span>

<span data-ttu-id="ff86a-114">下列程式碼顯示執行這些步驟的函式：</span><span class="sxs-lookup"><span data-stu-id="ff86a-114">The following code shows a function that performs these steps:</span></span>


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



<span data-ttu-id="ff86a-115">下列程式碼範例會使用此函式來建立 CC 解碼篩選器，並將它新增至篩選圖形：</span><span class="sxs-lookup"><span data-stu-id="ff86a-115">The following code example uses this function to create the CC Decoder filter and add it to the filter graph:</span></span>


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="ff86a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff86a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff86a-117">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="ff86a-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="ff86a-118">使用系統裝置列舉值</span><span class="sxs-lookup"><span data-stu-id="ff86a-118">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




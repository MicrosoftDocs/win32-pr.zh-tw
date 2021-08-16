---
description: 建立 Kernel-Mode 篩選
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: 建立 Kernel-Mode 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473565046c462e8992350c3662360e4c22b3b5b75e10f0e79e1399885355056e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953937"
---
# <a name="creating-kernel-mode-filters"></a>建立 Kernel-Mode 篩選

某些核心模式篩選器無法透過 **CoCreateInstance** 建立，因此沒有 clsid。 這些篩選準則包括 [t/接收到接收轉換器](tee-sink-to-sink-converter.md)、副本 [編碼器](cc-decoder-filter.md) 篩選器，以及 [WST 編解碼器](wst-codec-filter.md) 篩選器。 若要建立這些篩選準則的其中之一，請使用 [系統裝置列舉](system-device-enumerator.md) 值物件，並依篩選器的名稱進行搜尋。

1.  建立系統裝置枚舉器。
2.  使用篩選準則分類的 CLSID 來呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 方法。 這個方法會建立篩選準則分類的列舉值。  (*列舉* 值只是一個物件，該物件會使用已定義的 COM 介面傳回其他物件的清單。 ) 列舉值會傳回 **IMoniker** 指標，代表該類別中的篩選準則。
3.  針對每個標記，呼叫 **IMoniker：： BindToStorage** 來取得 **IPropertyBag** 介面。
4.  呼叫 **IPropertyBag：： Read** 以取得篩選的名稱。
5.  如果名稱相符，請呼叫 **IMoniker：： BindToObject** 來建立篩選準則。

下列程式碼顯示執行這些步驟的函式：


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



下列程式碼範例會使用此函式來建立 CC 解碼篩選器，並將它新增至篩選圖形：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[使用系統裝置列舉值](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




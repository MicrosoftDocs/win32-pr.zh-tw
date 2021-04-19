---
description: 列舉效果和轉換
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: 列舉效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971929"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="c1ef0-103">列舉效果和轉換</span><span class="sxs-lookup"><span data-stu-id="c1ef0-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="c1ef0-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c1ef0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c1ef0-105">DirectShow 提供用來列舉裝置的 [系統裝置列舉](system-device-enumerator.md) 值物件。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="c1ef0-106">您可以使用它來抓取在使用者系統上安裝之效果或轉換的名字標記。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="c1ef0-107">系統裝置列舉值會公開 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="c1ef0-108">它會傳回指定裝置類別的類別列舉值。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="c1ef0-109">類別列舉值接著會公開 [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) 介面，並傳回類別中每個裝置的名字。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="c1ef0-110">如需使用 **ICreateDevEnum** 的詳細討論，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="c1ef0-111">以下是有關 DirectShow 編輯服務的簡短摘要。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="c1ef0-112">若要列舉效果或轉換，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="c1ef0-113">建立系統裝置列舉值的實例。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="c1ef0-114">呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 方法以取出類別列舉值。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="c1ef0-115">類別目錄是由)  (Clsid 的類別識別碼所定義。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="c1ef0-116">使用 CLSID \_ VideoEffects1Category 進行轉換的效果或 clsid \_ VideoEffects2Category。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="c1ef0-117">呼叫 **IEnumMoniker：： Next** 以取得列舉中的每個標記。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="c1ef0-118">針對每個標記，呼叫 **IMoniker：： BindToStorage** 來取出其相關聯的屬性包。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="c1ef0-119">屬性包包含效果或轉換 (GUID) 的易記名稱和全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="c1ef0-120">應用程式可以顯示易記名稱清單，然後取得對應的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="c1ef0-121">下列程式碼範例說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="c1ef0-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="c1ef0-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1ef0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ef0-123">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="c1ef0-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 

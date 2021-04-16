---
description: 使用系統裝置列舉值
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: 使用系統裝置列舉值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550762"
---
# <a name="using-the-system-device-enumerator"></a><span data-ttu-id="d3799-103">使用系統裝置列舉值</span><span class="sxs-lookup"><span data-stu-id="d3799-103">Using the System Device Enumerator</span></span>

<span data-ttu-id="d3799-104">系統裝置列舉值提供統一的方式來列舉使用者系統上註冊的篩選準則（依類別目錄）。</span><span class="sxs-lookup"><span data-stu-id="d3799-104">The System Device Enumerator provides a uniform way to enumerate, by category, the filters registered on a user's system.</span></span> <span data-ttu-id="d3799-105">此外，它也會區分個別硬體裝置，即使相同的篩選器支援它們也是一樣。</span><span class="sxs-lookup"><span data-stu-id="d3799-105">Moreover, it differentiates between individual hardware devices, even if the same filter supports them.</span></span> <span data-ttu-id="d3799-106">這特別適用于使用 Windows Driver Model (WDM) 和 KSProxy 篩選器的裝置。</span><span class="sxs-lookup"><span data-stu-id="d3799-106">This is particularly useful for devices that use the Windows Driver Model (WDM) and the KSProxy filter.</span></span> <span data-ttu-id="d3799-107">例如，使用者可能會有數個 WDM 影片捕獲裝置，而且全部都受到相同的篩選準則支援。</span><span class="sxs-lookup"><span data-stu-id="d3799-107">For example, the user might have several WDM video capture devices, all supported by the same filter.</span></span> <span data-ttu-id="d3799-108">系統裝置列舉值會將它們視為個別的裝置實例。</span><span class="sxs-lookup"><span data-stu-id="d3799-108">The System Device Enumerator treats them as separate device instances.</span></span>

<span data-ttu-id="d3799-109">系統裝置列舉值的運作方式是建立特定類別的列舉值，例如音訊捕獲或影片壓縮。</span><span class="sxs-lookup"><span data-stu-id="d3799-109">The System Device Enumerator works by creating an enumerator for a specific category, such as audio capture or video compression.</span></span> <span data-ttu-id="d3799-110">類別列舉值會針對類別中的每個裝置傳回唯一的標記。</span><span class="sxs-lookup"><span data-stu-id="d3799-110">The category enumerator returns a unique moniker for each device in the category.</span></span> <span data-ttu-id="d3799-111">類別列舉值會自動在類別中包含任何相關的隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="d3799-111">The category enumerator automatically includes any relevant Plug and Play devices in the category.</span></span> <span data-ttu-id="d3799-112">如需分類清單，請參閱 [篩選分類](filter-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="d3799-112">For a list of categories, see [Filter Categories](filter-categories.md).</span></span>

<span data-ttu-id="d3799-113">若要使用系統裝置列舉值，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="d3799-113">To use the System Device Enumerator, do the following:</span></span>

1.  <span data-ttu-id="d3799-114">藉由呼叫 **CoCreateInstance** 來建立系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="d3799-114">Create the system device enumerator by calling **CoCreateInstance**.</span></span> <span data-ttu-id="d3799-115">CLSID)  (的類別識別碼是 CLSID \_ SystemDeviceEnum。</span><span class="sxs-lookup"><span data-stu-id="d3799-115">The class identifier (CLSID) is CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="d3799-116">藉由呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 與所需分類的 CLSID 來取得類別列舉值。</span><span class="sxs-lookup"><span data-stu-id="d3799-116">Obtain a category enumerator by calling [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the CLSID of the desired category.</span></span> <span data-ttu-id="d3799-117">這個方法會傳回 **IEnumMoniker** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d3799-117">This method returns an **IEnumMoniker** interface pointer.</span></span> <span data-ttu-id="d3799-118">如果類別目錄是空的 (或不存在) 中，此方法會傳回 \_ FALSE，而不是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d3799-118">If the category is empty (or does not exist), the method returns S\_FALSE rather than an error code.</span></span> <span data-ttu-id="d3799-119">如果是，則傳回的 **IEnumMoniker** 指標為 **Null** ，而取值會造成例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d3799-119">If so, the returned **IEnumMoniker** pointer is **NULL** and dereferencing it will cause an exception.</span></span> <span data-ttu-id="d3799-120">因此， \_ 當您呼叫 **CreateClassEnumerator** 時，請明確地測試是否沒問題，而不是呼叫一般的 **SUCCEEDED** 宏。</span><span class="sxs-lookup"><span data-stu-id="d3799-120">Therefore, explicitly test for S\_OK when you call **CreateClassEnumerator**, instead of calling the usual **SUCCEEDED** macro.</span></span>
3.  <span data-ttu-id="d3799-121">使用 **IEnumMoniker：： Next** 方法來列舉每個標記。</span><span class="sxs-lookup"><span data-stu-id="d3799-121">Use the **IEnumMoniker::Next** method to enumerate each moniker.</span></span> <span data-ttu-id="d3799-122">這個方法會傳回 **IMoniker** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d3799-122">This method returns an **IMoniker** interface pointer.</span></span> <span data-ttu-id="d3799-123">當 **下一個** 方法到達列舉的結尾時，它也會傳回 \_ FALSE，因此再次檢查是否 \_ 正常。</span><span class="sxs-lookup"><span data-stu-id="d3799-123">When the **Next** method reaches the end of the enumeration, it also returns S\_FALSE, so again check for S\_OK.</span></span>
4.  <span data-ttu-id="d3799-124">若要取得裝置的易記名稱 (例如，要顯示在使用者介面) 中，請呼叫 **IMoniker：： BindToStorage** 方法。</span><span class="sxs-lookup"><span data-stu-id="d3799-124">To retrieve the friendly name of the device (for example, to display in the user interface), call the **IMoniker::BindToStorage** method.</span></span>
5.  <span data-ttu-id="d3799-125">若要建立及初始化管理裝置的 DirectShow 篩選器，請在標記上呼叫 **IMoniker：： BindToObject** 。</span><span class="sxs-lookup"><span data-stu-id="d3799-125">To create and initialize the DirectShow filter that manages the device, call **IMoniker::BindToObject** on the moniker.</span></span> <span data-ttu-id="d3799-126">呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選準則新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="d3799-126">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the graph.</span></span>

<span data-ttu-id="d3799-127">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="d3799-127">The following diagram illustrates this process.</span></span>

![列舉裝置](images/sysdevenum.png)

<span data-ttu-id="d3799-129">下列範例示範如何列舉在使用者系統上安裝的影片壓縮機。</span><span class="sxs-lookup"><span data-stu-id="d3799-129">The following example shows how to enumerate the video compressors installed on the user's system.</span></span> <span data-ttu-id="d3799-130">為了簡潔起見，此範例會執行最少量的錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="d3799-130">For brevity, the example performs minimal error checking.</span></span>


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



<span data-ttu-id="d3799-131">**裝置的名字**</span><span class="sxs-lookup"><span data-stu-id="d3799-131">**Device Monikers**</span></span>

<span data-ttu-id="d3799-132">針對裝置的名字標記，您可以傳遞 [**IFilterGraph2：： AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) 方法來建立裝置的捕獲篩選器。</span><span class="sxs-lookup"><span data-stu-id="d3799-132">For device monikers, you can pass the moniker to the [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) method to create a capture filter for the device.</span></span> <span data-ttu-id="d3799-133">如需範例程式碼，請參閱該方法的檔。</span><span class="sxs-lookup"><span data-stu-id="d3799-133">For example code, see the documentation for that method.</span></span>

<span data-ttu-id="d3799-134">**IMoniker：： GetDisplayName** 方法會傳回標記的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d3799-134">The **IMoniker::GetDisplayName** method returns the display name of the moniker.</span></span> <span data-ttu-id="d3799-135">雖然顯示名稱是可讀取的，但通常不會將它顯示給終端使用者。</span><span class="sxs-lookup"><span data-stu-id="d3799-135">Although the display name is readable, you would not typically display it to an end-user.</span></span> <span data-ttu-id="d3799-136">改為取得屬性包中的易記名稱，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="d3799-136">Get the friendly name from the property bag instead, as described previously.</span></span>

<span data-ttu-id="d3799-137">**IMoniker：:P arsedisplayname** 方法或 **MkParseDisplayName** 函數可以用來建立指定篩選類別目錄的預設裝置標記。</span><span class="sxs-lookup"><span data-stu-id="d3799-137">The **IMoniker::ParseDisplayName** method or the **MkParseDisplayName** function can be used to create a default device moniker for a given filter category.</span></span> <span data-ttu-id="d3799-138">使用顯示名稱搭配表單 `@device:*:{category-clsid}` ，其中 `category-clsid` 是分類 GUID 的字串表示。</span><span class="sxs-lookup"><span data-stu-id="d3799-138">Use a display name with the form `@device:*:{category-clsid}`, where `category-clsid` is the string representation of the category GUID.</span></span> <span data-ttu-id="d3799-139">預設的名字標記是該類別的裝置列舉值所傳回的第一個標記。</span><span class="sxs-lookup"><span data-stu-id="d3799-139">The default moniker is the first moniker returned by the device enumerator for that category.</span></span>

 

 




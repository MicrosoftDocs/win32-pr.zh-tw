---
description: 選擇壓縮篩選
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: 選擇壓縮篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109841"
---
# <a name="choosing-a-compression-filter"></a><span data-ttu-id="9713b-103">選擇壓縮篩選</span><span class="sxs-lookup"><span data-stu-id="9713b-103">Choosing a Compression Filter</span></span>

<span data-ttu-id="9713b-104">有數種類型的軟體元件可以執行影片或音訊壓縮，例如：</span><span class="sxs-lookup"><span data-stu-id="9713b-104">Several types of software components can perform video or audio compression, such as:</span></span>

-   <span data-ttu-id="9713b-105">原生 DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="9713b-105">Native DirectShow filters</span></span>
-   <span data-ttu-id="9713b-106">影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器</span><span class="sxs-lookup"><span data-stu-id="9713b-106">Video Compression Manager (VCM) codecs</span></span>
-   <span data-ttu-id="9713b-107">音訊壓縮管理員 (的) 編解碼器</span><span class="sxs-lookup"><span data-stu-id="9713b-107">Audio Compression Manager (ACM) codecs</span></span>
-   <span data-ttu-id="9713b-108">DirectX 媒體物件 (DMOs) </span><span class="sxs-lookup"><span data-stu-id="9713b-108">DirectX Media Objects (DMOs)</span></span>

<span data-ttu-id="9713b-109">在 DirectShow 中，BC-VCM-LVM-HYPERV 編解碼器是由 [AVI 壓縮程式篩選器](avi-compressor-filter.md)包裝，而使用的編解碼器會由「通過」包裝函式 [篩選器](acm-wrapper-filter.md)包裝。</span><span class="sxs-lookup"><span data-stu-id="9713b-109">In DirectShow, VCM codecs are wrapped by the [AVI Compressor Filter](avi-compressor-filter.md), and ACM codecs are wrapped by the [ACM Wrapper Filter](acm-wrapper-filter.md).</span></span> <span data-ttu-id="9713b-110">DMOs 是以 [Sql-dmo 包裝函式篩選器](dmo-wrapper-filter.md)包裝。</span><span class="sxs-lookup"><span data-stu-id="9713b-110">DMOs are wrapped by the [DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="9713b-111">系統裝置列舉值可提供一致的方式來列舉和建立任何這些壓縮程式類型，而不需擔心基礎模型。</span><span class="sxs-lookup"><span data-stu-id="9713b-111">The system device enumerator provides a consistent way to enumerate and create any of these compressor types, without worrying about the underlying model.</span></span>

<span data-ttu-id="9713b-112">如需系統裝置列舉值的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="9713b-112">For details about the system device enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span> <span data-ttu-id="9713b-113">簡單地說，所有的 DirectShow 篩選準則都會依類別分類，而且每個類別都是由 GUID 來識別。</span><span class="sxs-lookup"><span data-stu-id="9713b-113">Briefly, all DirectShow filters are classified by category, and each category is identified by a GUID.</span></span> <span data-ttu-id="9713b-114">針對影片壓縮機，類別目錄 GUID 是 CLSID \_ VideoCompressorCategory。</span><span class="sxs-lookup"><span data-stu-id="9713b-114">For video compressors, the category GUID is CLSID\_VideoCompressorCategory.</span></span> <span data-ttu-id="9713b-115">針對音訊壓縮機，它是 CLSID \_ AudioCompressorCategory。</span><span class="sxs-lookup"><span data-stu-id="9713b-115">For audio compressors, it is CLSID\_AudioCompressorCategory.</span></span> <span data-ttu-id="9713b-116">為了列舉特定的類別，系統裝置列舉值會建立支援 [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker)介面的 *列舉* 值物件。</span><span class="sxs-lookup"><span data-stu-id="9713b-116">To enumerate a particular category, the system device enumerator creates an *enumerator* object that supports the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface.</span></span> <span data-ttu-id="9713b-117">應用程式會使用此介面來抓取裝置的名字標記，其中每個裝置的標記都代表一個 DirectShow 篩選器的實例。</span><span class="sxs-lookup"><span data-stu-id="9713b-117">The application uses this interface to retrieve device monikers, where each device moniker represents an instance of a DirectShow filter.</span></span> <span data-ttu-id="9713b-118">您可以使用「標記」來建立篩選，或在不建立篩選的情況下取得裝置的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9713b-118">You can use the moniker to create the filter, or to get the device's friendly name without creating the filter.</span></span>

<span data-ttu-id="9713b-119">若要列舉使用者系統上的可用影片或音訊壓縮機，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9713b-119">To enumerate the video or audio compressors available on the user's system, do the following:</span></span>

1.  <span data-ttu-id="9713b-120">呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立具有 CLSID SYSTEMDEVICEENUM 類別識別碼的系統裝置枚舉器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9713b-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the system device enumerator, which has a class ID of CLSID\_SystemDeviceEnum.</span></span>
2.  <span data-ttu-id="9713b-121">使用篩選準則分類 GUID 呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 。</span><span class="sxs-lookup"><span data-stu-id="9713b-121">Call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the filter category GUID.</span></span> <span data-ttu-id="9713b-122">方法會傳回 **IEnumMoniker** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="9713b-122">The method returns an **IEnumMoniker** interface pointer.</span></span>
3.  <span data-ttu-id="9713b-123">使用 IEnumMoniker：： Next 方法來列舉裝置的名字標記。</span><span class="sxs-lookup"><span data-stu-id="9713b-123">Use the IEnumMoniker::Next method to enumerate the device monikers.</span></span> <span data-ttu-id="9713b-124">這個方法會傳回代表標記的 [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) 介面。</span><span class="sxs-lookup"><span data-stu-id="9713b-124">This method returns an [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) interface, which represents the moniker.</span></span>

<span data-ttu-id="9713b-125">若要從標記取得易記名稱，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9713b-125">To get the friendly name from a moniker, do the following:</span></span>

1.  <span data-ttu-id="9713b-126">呼叫 **IMoniker：： BindToStorage** 方法。</span><span class="sxs-lookup"><span data-stu-id="9713b-126">Call the **IMoniker::BindToStorage** method.</span></span> <span data-ttu-id="9713b-127">這個方法會傳回 **IPropertyBag** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="9713b-127">This method returns an **IPropertyBag** interface pointer.</span></span>
2.  <span data-ttu-id="9713b-128">使用 **IPropertyBag：： read** 方法讀取 **FriendlyName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9713b-128">Use the **IPropertyBag::Read** method to read the **FriendlyName** property.</span></span>

<span data-ttu-id="9713b-129">一般而言，應用程式會顯示壓縮機清單，讓使用者可以選擇一個。</span><span class="sxs-lookup"><span data-stu-id="9713b-129">Typically, an application would display a list of compressors, so that the user could choose one.</span></span> <span data-ttu-id="9713b-130">例如，下列程式碼會在清單方塊中填入可用影片壓縮機的名稱。</span><span class="sxs-lookup"><span data-stu-id="9713b-130">For example, the following code populates a list box with the names of the available video compressors.</span></span>


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



<span data-ttu-id="9713b-131">若要從標記建立篩選準則實例，請呼叫 **IMoniker：： BindToObject** 方法。</span><span class="sxs-lookup"><span data-stu-id="9713b-131">To create a filter instance from the moniker, call the **IMoniker::BindToObject** method.</span></span> <span data-ttu-id="9713b-132">方法會傳回 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。</span><span class="sxs-lookup"><span data-stu-id="9713b-132">The method returns an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span>


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



<span data-ttu-id="9713b-133">針對 BC-VCM-LVM-HYPERV 編解碼器，每個標記都代表一個特定的編解碼器，即使所有編解碼器都是由相同的 AVI 壓縮篩選器所包裝也一樣。</span><span class="sxs-lookup"><span data-stu-id="9713b-133">For VCM codecs, each moniker represents one particular codec, even though all of the codecs are wrapped by the same AVI Compression filter.</span></span> <span data-ttu-id="9713b-134">呼叫 **BindToObject** 會建立此篩選準則的實例，並針對該編解碼器進行初始化。</span><span class="sxs-lookup"><span data-stu-id="9713b-134">Calling **BindToObject** creates an instance of this filter, initialized for that codec.</span></span> <span data-ttu-id="9713b-135">基於這個理由，您無法直接在 AVI 壓縮篩選器上呼叫 **CoCreateInstance** 。</span><span class="sxs-lookup"><span data-stu-id="9713b-135">For this reason, you cannot call **CoCreateInstance** directly on the AVI Compression filter.</span></span> <span data-ttu-id="9713b-136">您必須經過系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="9713b-136">You must go through the system device enumerator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9713b-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="9713b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9713b-138">Recompressing AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="9713b-138">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 

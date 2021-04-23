---
description: 在 DirectShow 中使用 DMOs
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: 在 DirectShow 中使用 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908686"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="173a9-103">在 DirectShow 中使用 DMOs</span><span class="sxs-lookup"><span data-stu-id="173a9-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="173a9-104">以 DirectShow 為基礎的應用程式可以使用篩選圖形中的 DMOs，[透過 []](dmo-wrapper-filter.md)</span><span class="sxs-lookup"><span data-stu-id="173a9-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="173a9-105">此篩選準則會匯總一，並處理所有使用 SQL-DMO 的詳細資料，例如，將資料傳入和傳出、配置 [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) 物件等等。</span><span class="sxs-lookup"><span data-stu-id="173a9-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="173a9-106">因為是由篩選準則來匯總，所以應用程式可以查詢此篩選器中的任何 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="173a9-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="173a9-107">但是，應用程式應該讓篩選器處理該的所有串流作業。</span><span class="sxs-lookup"><span data-stu-id="173a9-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="173a9-108">例如，請勿設定媒體類型、處理任何緩衝區、排清、鎖定，以及啟用或停用品質控制，或設定影片優化。</span><span class="sxs-lookup"><span data-stu-id="173a9-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="173a9-109">如果您知道您想要使用之特定的) 的類別識別碼 (CLSID，您可以使用該的</span><span class="sxs-lookup"><span data-stu-id="173a9-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="173a9-110">呼叫 **CoCreateInstance** 以建立 [的] 包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="173a9-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="173a9-111">查詢 [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) 介面的 sql-dmo 包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="173a9-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="173a9-112">呼叫 [**IDMOWrapperFilter：： Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) 方法。</span><span class="sxs-lookup"><span data-stu-id="173a9-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="173a9-113">指定 SQL-DMO 的 CLSID 和此的類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="173a9-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="173a9-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="173a9-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="173a9-115">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="173a9-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="173a9-116">[**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)函式會列舉登錄中的 DMOs。</span><span class="sxs-lookup"><span data-stu-id="173a9-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="173a9-117">此函式會使用用於 DirectShow 篩選器的不同分類 Guid 集合。</span><span class="sxs-lookup"><span data-stu-id="173a9-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="173a9-118">**使用系統裝置列舉值搭配 DMOs**</span><span class="sxs-lookup"><span data-stu-id="173a9-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="173a9-119">您可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉 **DMOEnum** 方法所支援的任何 sql-dmo 類別，而不是直接建立一個。</span><span class="sxs-lookup"><span data-stu-id="173a9-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="173a9-120">當系統裝置枚舉器列舉特定的 DirectShow 篩選類別時，也會包含 DMOs。</span><span class="sxs-lookup"><span data-stu-id="173a9-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="173a9-121">下表顯示的是 SQL-DMO 類別和 DirectShow 類別之間的對應。</span><span class="sxs-lookup"><span data-stu-id="173a9-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



| <span data-ttu-id="173a9-122">標籤</span><span class="sxs-lookup"><span data-stu-id="173a9-122">Label</span></span> | <span data-ttu-id="173a9-123">值</span><span class="sxs-lookup"><span data-stu-id="173a9-123">Value</span></span> |
|-----------------------------|--------------------------------|
| <span data-ttu-id="173a9-124">SQL-DMO 類別</span><span class="sxs-lookup"><span data-stu-id="173a9-124">DMO Category</span></span>                | <span data-ttu-id="173a9-125">DirectShow 對等</span><span class="sxs-lookup"><span data-stu-id="173a9-125">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="173a9-126">DMOCATEGORY \_ 音訊 \_ 編碼器</span><span class="sxs-lookup"><span data-stu-id="173a9-126">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="173a9-127">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="173a9-127">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="173a9-128">DMOCATEGORY \_ 音訊 \_ 解碼器</span><span class="sxs-lookup"><span data-stu-id="173a9-128">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="173a9-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="173a9-129">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="173a9-130">DMOCATEGORY \_ 影片 \_ 編碼器</span><span class="sxs-lookup"><span data-stu-id="173a9-130">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="173a9-131">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="173a9-131">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="173a9-132">DMOCATEGORY \_ 影片 \_ 解碼器</span><span class="sxs-lookup"><span data-stu-id="173a9-132">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="173a9-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="173a9-133">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="173a9-134">系統裝置列舉值會傳回一份標記物件清單。</span><span class="sxs-lookup"><span data-stu-id="173a9-134">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="173a9-135">如果標記法代表的是，則 **IMoniker：： BindToObject** 方法會自動建立 sql-dmo 包裝函式篩選器，並將它初始化為該。</span><span class="sxs-lookup"><span data-stu-id="173a9-135">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="173a9-136">這樣一來，就會對應用程式透明說出一種。</span><span class="sxs-lookup"><span data-stu-id="173a9-136">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="173a9-137">如需使用系統裝置列舉值的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="173a9-137">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="173a9-138">**限制**</span><span class="sxs-lookup"><span data-stu-id="173a9-138">**Limitations**</span></span>

<span data-ttu-id="173a9-139">在 DirectShow 中使用 DMOs 時，有一些限制：</span><span class="sxs-lookup"><span data-stu-id="173a9-139">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="173a9-140">SQL-DMO 包裝函式篩選不支援具有零個輸入的 DMOs、多個輸入或零個輸出。</span><span class="sxs-lookup"><span data-stu-id="173a9-140">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="173a9-141">SQL-DMO 包裝函式篩選器上的所有 pin 連接都會使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。</span><span class="sxs-lookup"><span data-stu-id="173a9-141">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="173a9-142">DirectShow 編輯服務不支援以 SQL-DMO 為基礎的效果或轉換。</span><span class="sxs-lookup"><span data-stu-id="173a9-142">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="173a9-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="173a9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173a9-144">使用 DMOs</span><span class="sxs-lookup"><span data-stu-id="173a9-144">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 




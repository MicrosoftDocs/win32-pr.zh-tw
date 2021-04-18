---
description: 在 DirectShow 編輯服務中選取解碼器
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: 在 DirectShow 編輯服務中選取解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467639"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="69cdf-103">在 DirectShow 編輯服務中選取解碼器</span><span class="sxs-lookup"><span data-stu-id="69cdf-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="69cdf-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="69cdf-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="69cdf-105">當 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 轉譯影片編輯專案時，轉譯引擎會自動選取必要的解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="69cdf-106">這可能會發生在 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法內，或在轉譯期間以動態方式發生。</span><span class="sxs-lookup"><span data-stu-id="69cdf-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="69cdf-107">使用者可能會安裝數個可以解碼特定檔案的解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="69cdf-108">當有多個可用的解碼器時，DES 會使用 [智慧型連接](intelligent-connect.md) 演算法來選取解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="69cdf-109">沒有任何方法可讓應用程式直接指定要使用哪個解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="69cdf-110">不過，您可以透過 [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) 回呼介面間接選擇此解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="69cdf-111">藉由在您的應用程式中執行此介面，您可以在圖形建立程式期間收到通知，並從圖形拒絕某些篩選。</span><span class="sxs-lookup"><span data-stu-id="69cdf-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="69cdf-112">首先，執行公開 [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) 介面的類別：</span><span class="sxs-lookup"><span data-stu-id="69cdf-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="69cdf-113">然後，建立篩選圖形管理員的實例，並註冊您的類別以接收回呼通知：</span><span class="sxs-lookup"><span data-stu-id="69cdf-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="69cdf-114">接下來，請建立轉譯引擎，並呼叫 [**IRenderEngine：： SetFilterGraph**](irenderengine-setfiltergraph.md) 方法，並加上篩選圖形管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="69cdf-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="69cdf-115">這可確保轉譯引擎不會建立自己的篩選圖形管理員，而是會使用您為回呼設定的實例。</span><span class="sxs-lookup"><span data-stu-id="69cdf-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="69cdf-116">轉譯專案時，會立即呼叫應用程式的 [**IAMGraphBuilderCallback：： SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) 方法，然後篩選圖形管理員才會建立新的篩選。</span><span class="sxs-lookup"><span data-stu-id="69cdf-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="69cdf-117">**SelectedFilter** 方法會接收 **IMoniker** 介面的指標，該介面表示篩選的標記。</span><span class="sxs-lookup"><span data-stu-id="69cdf-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="69cdf-118">檢查標記，如果您決定拒絕篩選，請從 **SelectedFilter** 方法傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="69cdf-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="69cdf-119">困難的部分是找出哪些名字代表了它們，尤其是哪一個名字代表您要拒絕的解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="69cdf-120">其中一個解決方案如下：</span><span class="sxs-lookup"><span data-stu-id="69cdf-120">One solution is the following:</span></span>

-   <span data-ttu-id="69cdf-121">轉譯專案之前，請使用 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) 方法來建立已註冊為接受所需輸入類型的篩選器清單。</span><span class="sxs-lookup"><span data-stu-id="69cdf-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="69cdf-122">針對影片或音訊壓縮類型，此清單應對應至一組解碼器。</span><span class="sxs-lookup"><span data-stu-id="69cdf-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="69cdf-123">**EnumMatchingFilters** 方法會傳回一個名字組的集合。</span><span class="sxs-lookup"><span data-stu-id="69cdf-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="69cdf-124">針對集合中的每個標記，取得 **DisplayName** 屬性，如 [使用篩選器](using-the-filter-mapper.md)對應程式中所述。</span><span class="sxs-lookup"><span data-stu-id="69cdf-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="69cdf-125">儲存顯示名稱清單，但省略符合您要用於解碼之篩選的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="69cdf-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="69cdf-126">軟體篩選器的顯示名稱具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="69cdf-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="69cdf-127">其中</span><span class="sxs-lookup"><span data-stu-id="69cdf-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="69cdf-128">這是篩選準則分類的 GUID，而</span><span class="sxs-lookup"><span data-stu-id="69cdf-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="69cdf-129">這是篩選的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="69cdf-129">is the filter's CLSID.</span></span> <span data-ttu-id="69cdf-130">若為 DMOs，格式會相同，但會變更 `sw` 為 `dmo` 。</span><span class="sxs-lookup"><span data-stu-id="69cdf-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="69cdf-131">清單現在包含輸出所需媒體類型，但不是您慣用篩選的每個篩選器的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="69cdf-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="69cdf-132">在 **SelectedFilter** 方法中，取得建議的標記上的 **DisplayName** 屬性，並針對儲存的清單進行檢查。</span><span class="sxs-lookup"><span data-stu-id="69cdf-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="69cdf-133">如果顯示名稱符合清單中的專案，則拒絕該篩選。</span><span class="sxs-lookup"><span data-stu-id="69cdf-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="69cdf-134">否則，請返回 \_ [確定] 以接受它。</span><span class="sxs-lookup"><span data-stu-id="69cdf-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69cdf-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="69cdf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69cdf-136">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="69cdf-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 




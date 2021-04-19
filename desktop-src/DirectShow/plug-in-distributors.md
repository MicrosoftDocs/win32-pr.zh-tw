---
description: 外掛程式散發者
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: 外掛程式散發者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107000040"
---
# <a name="plug-in-distributors"></a><span data-ttu-id="e00c5-103">外掛程式散發者</span><span class="sxs-lookup"><span data-stu-id="e00c5-103">Plug-in Distributors</span></span>

<span data-ttu-id="e00c5-104">外掛程式散發者 (Pid) 是擴充篩選圖形管理員功能的一種方式。</span><span class="sxs-lookup"><span data-stu-id="e00c5-104">Plug-in distributors (PIDs) are a way to extend the functionality of the filter graph manager.</span></span> <span data-ttu-id="e00c5-105">外掛程式散發者是篩選圖形管理員在執行時間匯總的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e00c5-105">A plug-in distributor is a COM object that the filter graph manager aggregates at run time.</span></span> <span data-ttu-id="e00c5-106">應用程式會透過篩選圖形管理員取得 PID 的存取權。</span><span class="sxs-lookup"><span data-stu-id="e00c5-106">Applications obtain access to the PID through the filter graph manager.</span></span>

<span data-ttu-id="e00c5-107">當篩選圖形管理員針對不支援的介面進行查詢時，它會在登錄中搜尋下列格式的索引鍵：</span><span class="sxs-lookup"><span data-stu-id="e00c5-107">When the filter graph manager is queried for an interface that it does not support, it searches the registry for a key with the following form:</span></span>


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



<span data-ttu-id="e00c5-108">`IID` 這是包含介面識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="e00c5-108">`IID` is a string containing the interface identifier.</span></span> <span data-ttu-id="e00c5-109">如果登錄專案存在，專案的值會定義支援介面之 PID (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="e00c5-109">If the registry entry exists, the value of the entry defines the class identifier (CLSID) of a PID that supports the interface.</span></span> <span data-ttu-id="e00c5-110">篩選圖形管理員會匯總 PID 並傳回介面指標，進而作為 PID 的外部 **IUnknown** 。</span><span class="sxs-lookup"><span data-stu-id="e00c5-110">The filter graph manager aggregates the PID and returns an interface pointer, thereby acting as the outer **IUnknown** for the PID.</span></span> <span data-ttu-id="e00c5-111">當應用程式呼叫介面上的方法時，實際上是在 PID 上呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="e00c5-111">When the application calls methods on the interface, it is actually calling them on the PID.</span></span> <span data-ttu-id="e00c5-112">不過，PID 的存在對應用程式而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="e00c5-112">However, the existence of the PID is transparent to the application.</span></span>

<span data-ttu-id="e00c5-113">「散發者」 *一詞是指 PID* 可以查詢其外部 **IUnknown** 指標，以取得篩選圖形管理員上的介面。</span><span class="sxs-lookup"><span data-stu-id="e00c5-113">The term *distributor* stems from the fact that a PID can query its outer **IUnknown** pointer for interfaces on the filter graph manager.</span></span> <span data-ttu-id="e00c5-114">藉由呼叫 [**IFilterGraph：： EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) 方法，PID 可以列舉圖形中的篩選，並將方法呼叫散發至這些篩選器。</span><span class="sxs-lookup"><span data-stu-id="e00c5-114">By calling the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method, the PID can enumerate the filters in the graph and distribute method calls to those filters.</span></span> <span data-ttu-id="e00c5-115">以這種方式，PID 可以作為應用程式在篩選準則上呼叫方法的單一控制點。</span><span class="sxs-lookup"><span data-stu-id="e00c5-115">In this way, a PID can serve as a single control point for the application to call methods on filters.</span></span>

<span data-ttu-id="e00c5-116">當篩選圖形管理員匯總 PID 時，它會查詢 [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) 介面的 pid。</span><span class="sxs-lookup"><span data-stu-id="e00c5-116">When the filter graph manager aggregates a PID, it queries the PID for the [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) interface.</span></span> <span data-ttu-id="e00c5-117">如果 PID 支援這個介面，則篩選圖形管理員會使用它來通知 PID 有關圖形中的變更：</span><span class="sxs-lookup"><span data-stu-id="e00c5-117">If the PID supports this interface, the filter graph manager uses it to notify the PID about changes in the graph:</span></span>

-   <span data-ttu-id="e00c5-118">當篩選圖形在執行、暫停和停止狀態之間切換時，它會呼叫 [**IDistributorNotify：： run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run)、 [**IDistributorNotify：:P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)或 [**IDistributorNotify：： Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop)。</span><span class="sxs-lookup"><span data-stu-id="e00c5-118">When the filter graph switches between run, paused, and stopped states, it calls [**IDistributorNotify::Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::Pause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause), or [**IDistributorNotify::Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).</span></span>
-   <span data-ttu-id="e00c5-119">設定參考時鐘時，篩選圖形管理員會呼叫 [**IDistributorNotify：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource)。</span><span class="sxs-lookup"><span data-stu-id="e00c5-119">When a reference clock is set, the filter graph manager calls [**IDistributorNotify::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).</span></span>
-   <span data-ttu-id="e00c5-120">當加入或移除篩選，或變更 pin 連接時，篩選圖形管理員會呼叫 [**IDistributorNotify：： NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange)。</span><span class="sxs-lookup"><span data-stu-id="e00c5-120">When filters are added or removed, or pin connections are changed, the filter graph manager calls [**IDistributorNotify::NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).</span></span>

<span data-ttu-id="e00c5-121">若要執行自訂 PID，請建立支援匯總的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e00c5-121">To implement a custom PID, create a COM object that supports aggregation.</span></span> <span data-ttu-id="e00c5-122">它必須支援篩選圖形管理員還不支援的介面。</span><span class="sxs-lookup"><span data-stu-id="e00c5-122">It must support an interface that the filter graph manager does not already support.</span></span> <span data-ttu-id="e00c5-123">（選擇性）它可以支援 **IDistributorNotify** 介面。</span><span class="sxs-lookup"><span data-stu-id="e00c5-123">Optionally, it can support the **IDistributorNotify** interface.</span></span>

<span data-ttu-id="e00c5-124">如果 PID 從篩選圖形管理員取得任何介面指標，則應該立即釋出。</span><span class="sxs-lookup"><span data-stu-id="e00c5-124">If the PID obtains any interface pointers from the filter graph manager, it should release them immediately.</span></span> <span data-ttu-id="e00c5-125">否則，它可能會建立迴圈參考計數，這可能會導致無法終結篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="e00c5-125">Otherwise, it might create a circular reference count, which could prevent the filter graph manager from being destroyed.</span></span> <span data-ttu-id="e00c5-126">在任何情況下都不需要在篩選圖形管理員上保存參考計數，因為篩選圖形管理員會控制 PID 的存留期。</span><span class="sxs-lookup"><span data-stu-id="e00c5-126">Holding a reference count on the filter graph manager is unnecessary in any case, because the filter graph manager controls the PID's lifetime.</span></span>

<span data-ttu-id="e00c5-127">因為 PID 是特別針對篩選圖形管理員所設計，所以您可能想要在 PID 的函式方法中強制執行此程式。</span><span class="sxs-lookup"><span data-stu-id="e00c5-127">Because a PID is designed specifically for aggregation by the filter graph manager, you might want to enforce this in the PID's constructor method.</span></span> <span data-ttu-id="e00c5-128">檢查外部 **IUnknown** 指標是否為 **Null**，如果是，則傳回錯誤碼 VFW \_ E \_ 需要擁有者 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e00c5-128">Check whether the outer **IUnknown** pointer is **NULL**, and if so, return the error code VFW\_E\_NEED\_OWNER.</span></span> <span data-ttu-id="e00c5-129"> (查看 [錯誤和成功碼](error-and-success-codes.md)。也 ) 為了防止其他物件匯總 PID，您可以查詢 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)介面的外部 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="e00c5-129">(See [Error and Success Codes](error-and-success-codes.md).) Also, to prevent other objects from aggregating the PID, you can query the outer **IUnknown** pointer for the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="e00c5-130">如果物件未公開 **IGraphBuilder**，則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e00c5-130">Return an error code if the object does not expose **IGraphBuilder**.</span></span>

 

 




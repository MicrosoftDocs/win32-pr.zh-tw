---
description: 建立群組組合和追蹤
ms.assetid: c3bef3cd-5e3c-42c5-850f-b4cb00c414bd
title: 建立群組組合和追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2808c2d096b52ad73da7d518d703bc25103751d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846796"
---
# <a name="creating-groups-compositions-and-tracks"></a><span data-ttu-id="55ba1-103">建立群組組合和追蹤</span><span class="sxs-lookup"><span data-stu-id="55ba1-103">Creating Groups Compositions and Tracks</span></span>

<span data-ttu-id="55ba1-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="55ba1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="55ba1-105">群組、組合和軌跡是時間軸和來源剪輯之間的中繼層。</span><span class="sxs-lookup"><span data-stu-id="55ba1-105">Groups, compositions, and tracks are the intermediate layers between the timeline and the source clips.</span></span> <span data-ttu-id="55ba1-106">它們是由其可包含的物件類型所區分。</span><span class="sxs-lookup"><span data-stu-id="55ba1-106">They are distinguished by the type of object they can contain.</span></span>

-   <span data-ttu-id="55ba1-107">追蹤包含來源物件。</span><span class="sxs-lookup"><span data-stu-id="55ba1-107">Tracks contain source objects.</span></span>
-   <span data-ttu-id="55ba1-108">組合包含曲目和其他組合，但不包含來源物件。</span><span class="sxs-lookup"><span data-stu-id="55ba1-108">Compositions contain tracks and other compositions, but not source objects.</span></span>
-   <span data-ttu-id="55ba1-109">群組是最上層的組合。</span><span class="sxs-lookup"><span data-stu-id="55ba1-109">Groups are top-level compositions.</span></span> <span data-ttu-id="55ba1-110">群組包含組合和追蹤，但組合不能包含群組。</span><span class="sxs-lookup"><span data-stu-id="55ba1-110">Groups contain compositions and tracks, but compositions cannot contain groups.</span></span>
-   <span data-ttu-id="55ba1-111">*虛擬追蹤* 是可以位於組合或群組內的任何物件。</span><span class="sxs-lookup"><span data-stu-id="55ba1-111">A *virtual track* is any object that can reside inside a composition or a group.</span></span> <span data-ttu-id="55ba1-112">這包括追蹤和組合。</span><span class="sxs-lookup"><span data-stu-id="55ba1-112">This includes tracks and compositions.</span></span>

<span data-ttu-id="55ba1-113">這些物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="55ba1-113">These objects expose the following interfaces:</span></span>



| <span data-ttu-id="55ba1-114">介面</span><span class="sxs-lookup"><span data-stu-id="55ba1-114">Interface</span></span>                                                  | <span data-ttu-id="55ba1-115">公開者</span><span class="sxs-lookup"><span data-stu-id="55ba1-115">Exposed By</span></span>           |
|------------------------------------------------------------|----------------------|
| [<span data-ttu-id="55ba1-116">**IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="55ba1-116">**IAMTimelineTrack**</span></span>](iamtimelinetrack.md)               | <span data-ttu-id="55ba1-117">資料軌</span><span class="sxs-lookup"><span data-stu-id="55ba1-117">Tracks</span></span>               |
| [<span data-ttu-id="55ba1-118">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="55ba1-118">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="55ba1-119">追蹤，組合</span><span class="sxs-lookup"><span data-stu-id="55ba1-119">Tracks, Compositions</span></span> |
| [<span data-ttu-id="55ba1-120">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="55ba1-120">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)                 | <span data-ttu-id="55ba1-121">組合，群組</span><span class="sxs-lookup"><span data-stu-id="55ba1-121">Compositions, Groups</span></span> |
| [<span data-ttu-id="55ba1-122">**IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="55ba1-122">**IAMTimelineGroup**</span></span>](iamtimelinegroup.md)               | <span data-ttu-id="55ba1-123">群組</span><span class="sxs-lookup"><span data-stu-id="55ba1-123">Groups</span></span>               |



 

<span data-ttu-id="55ba1-124">這些介面包含將物件加入至時間軸的方法。</span><span class="sxs-lookup"><span data-stu-id="55ba1-124">These interfaces contain the methods for adding objects to the timeline.</span></span>

-   <span data-ttu-id="55ba1-125">[**IAMTimeline：： AddGroup**](iamtimeline-addgroup.md)：將群組插入到時間軸。</span><span class="sxs-lookup"><span data-stu-id="55ba1-125">[**IAMTimeline::AddGroup**](iamtimeline-addgroup.md): Inserts a group into the timeline.</span></span>
-   <span data-ttu-id="55ba1-126">[**IAMTimelineComp：： VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)：將虛擬追蹤插入組合或群組中。</span><span class="sxs-lookup"><span data-stu-id="55ba1-126">[**IAMTimelineComp::VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md): Inserts a virtual track into a composition or group.</span></span>
-   <span data-ttu-id="55ba1-127">[**IAMTimelineTrack：： SrcAdd**](iamtimelinetrack-srcadd.md)：將來源插入至追蹤。</span><span class="sxs-lookup"><span data-stu-id="55ba1-127">[**IAMTimelineTrack::SrcAdd**](iamtimelinetrack-srcadd.md): Inserts a source into a track.</span></span>

<span data-ttu-id="55ba1-128">例如，下列程式碼會將新的曲目插入群組中。</span><span class="sxs-lookup"><span data-stu-id="55ba1-128">For example, the following code inserts a new track into a group.</span></span> <span data-ttu-id="55ba1-129">如上表所示，群組被視為一種組合，而曲目是一種虛擬追蹤。因此，若要將追蹤插入到群組中，您必須查詢其 **IAMTimelineComp** 介面的群組，並呼叫 **IAMTimelineComp：： VTrackInsBefore** 方法。</span><span class="sxs-lookup"><span data-stu-id="55ba1-129">As shown in the previous table, a group is considered a kind of composition, and a track is a kind of virtual track. Therefore, to insert the track into the group, you must query the group for its **IAMTimelineComp** interface and call the **IAMTimelineComp::VTrackInsBefore** method.</span></span>


```C++
IAMTimelineGroup    *pGroup;
// Create a new group (not shown). 

IAMTimelineComp     *pComp = NULL;
IAMTimelineObj      *pTrackObj = NULL;

pTL->CreateEmptyNode(&pTrackObj, TIMELINE_MAJOR_TYPE_TRACK);
pGroup->QueryInterface(IID_IAMTimelineComp, (void **)&pComp);
pComp->VTrackInsBefore(pTrackObj, 0);
```



<span data-ttu-id="55ba1-130">**VTrackInsBefore** 的第二個參數會指定虛擬追蹤的優先順序。優先權層級從零開始。</span><span class="sxs-lookup"><span data-stu-id="55ba1-130">The second parameter to **VTrackInsBefore** specifies the priority of the virtual track. Priority levels start at zero.</span></span> <span data-ttu-id="55ba1-131">如果您指定的值是-1，則會在優先順序清單的結尾插入虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="55ba1-131">If you specify the value –1, the virtual track is inserted at the end of the priority list.</span></span> <span data-ttu-id="55ba1-132">如果您指定的值已有虛擬追蹤，則從該點開始的所有專案都會依一個優先權層級向下移動。</span><span class="sxs-lookup"><span data-stu-id="55ba1-132">If you specify a value where there is already a virtual track, everything from that point on moves down the list by one priority level.</span></span> <span data-ttu-id="55ba1-133">請勿以大於虛擬追蹤數目的優先順序插入虛擬追蹤，因為它會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="55ba1-133">Do not insert a virtual track at a priority greater than the number of virtual tracks, because it will cause undefined behavior.</span></span>

<span data-ttu-id="55ba1-134">若要從時間軸永久刪除物件，請呼叫物件上的 [**IAMTimelineObj：： RemoveAll**](iamtimelineobj-removeall.md) 。</span><span class="sxs-lookup"><span data-stu-id="55ba1-134">To delete an object permanently from the timeline, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md) on the object.</span></span> <span data-ttu-id="55ba1-135">這個方法會移除物件及其所有子系。</span><span class="sxs-lookup"><span data-stu-id="55ba1-135">This method removes the object and all its children.</span></span> <span data-ttu-id="55ba1-136">若要移除物件以在時間軸中的其他位置重新插入物件，請改為呼叫 [**IAMTimelineObj：： remove**](iamtimelineobj-remove.md) 。</span><span class="sxs-lookup"><span data-stu-id="55ba1-136">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md) instead.</span></span> <span data-ttu-id="55ba1-137">不同于 **RemoveAll**，這個方法不會刪除物件的子系。</span><span class="sxs-lookup"><span data-stu-id="55ba1-137">Unlike **RemoveAll**, this method does not delete the object's children.</span></span> <span data-ttu-id="55ba1-138">若要從時程表中移除所有專案，請呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md)。</span><span class="sxs-lookup"><span data-stu-id="55ba1-138">To remove everything from the timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55ba1-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="55ba1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55ba1-140">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="55ba1-140">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




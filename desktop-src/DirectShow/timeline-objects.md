---
description: 時間軸物件
ms.assetid: da426964-d5bd-45ca-a914-c19062f3564b
title: 時間軸物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580286b31afd77f064411dd29d60a62b80bfb51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998002"
---
# <a name="timeline-objects"></a><span data-ttu-id="f1369-103">時間軸物件</span><span class="sxs-lookup"><span data-stu-id="f1369-103">Timeline Objects</span></span>

<span data-ttu-id="f1369-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f1369-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f1369-105">時間軸中的每種物件類型（來源、追蹤、效果等等）都是不同的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="f1369-105">Each type of object in the timeline—source, track, effect, and so forth—is a distinct COM object.</span></span> <span data-ttu-id="f1369-106">不過，應用程式不會使用 **CoCreateInstance** 函數來建立它們。</span><span class="sxs-lookup"><span data-stu-id="f1369-106">However, an application does not create them using the **CoCreateInstance** function.</span></span> <span data-ttu-id="f1369-107">相反地，它會呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f1369-107">Instead, it calls the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="f1369-108">這個方法會建立所要求型別的物件、將它初始化，然後將指標傳回物件。</span><span class="sxs-lookup"><span data-stu-id="f1369-108">This method creates an object of the requested type, initializes it, and returns a pointer to the object.</span></span> <span data-ttu-id="f1369-109">如需詳細資訊，請參閱 [建立時間軸](constructing-a-timeline.md)。</span><span class="sxs-lookup"><span data-stu-id="f1369-109">For details, see [Constructing a Timeline](constructing-a-timeline.md).</span></span>

<span data-ttu-id="f1369-110">每個時間軸物件都會公開 [**IAMTimelineObj**](iamtimelineobj.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="f1369-110">Every timeline object exposes the [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="f1369-111">此外，各種物件類型都支援其專屬的特殊介面：</span><span class="sxs-lookup"><span data-stu-id="f1369-111">In addition, the various object types support their own specialized interfaces:</span></span>

-   <span data-ttu-id="f1369-112">來源： [ **IAMTimelineSrc**](iamtimelinesrc.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-112">Source: [**IAMTimelineSrc**](iamtimelinesrc.md)</span></span>
-   <span data-ttu-id="f1369-113">追蹤： [ **IAMTimelineTrack**](iamtimelinetrack.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-113">Track: [**IAMTimelineTrack**](iamtimelinetrack.md)</span></span>
-   <span data-ttu-id="f1369-114">組合： [ **IAMTimelineComp**](iamtimelinecomp.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-114">Composition: [**IAMTimelineComp**](iamtimelinecomp.md)</span></span>
-   <span data-ttu-id="f1369-115">群組： [**IAMTimelineComp**](iamtimelinecomp.md)、 [**IAMTimelineGroup**](iamtimelinegroup.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-115">Group: [**IAMTimelineComp**](iamtimelinecomp.md), [**IAMTimelineGroup**](iamtimelinegroup.md)</span></span>
-   <span data-ttu-id="f1369-116">效果： [ **IAMTimelineEffect**](iamtimelineeffect.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-116">Effect: [**IAMTimelineEffect**](iamtimelineeffect.md)</span></span>
-   <span data-ttu-id="f1369-117">轉換： [ **IAMTimelineTrans**](iamtimelinetrans.md)</span><span class="sxs-lookup"><span data-stu-id="f1369-117">Transition: [**IAMTimelineTrans**](iamtimelinetrans.md)</span></span>

<span data-ttu-id="f1369-118">請注意，群組是一種組合，因此支援 [**IAMTimelineComp**](iamtimelinecomp.md)，以及自己的 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="f1369-118">Note that groups are a type of composition, so they support [**IAMTimelineComp**](iamtimelinecomp.md), as well as their own [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="f1369-119">除了先前所列的介面之外，時程表物件也會公開其他的次要介面。</span><span class="sxs-lookup"><span data-stu-id="f1369-119">In addition to the interfaces listed previously, timeline objects expose other, secondary interfaces.</span></span> <span data-ttu-id="f1369-120">這些介面會決定物件類型之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="f1369-120">These interfaces determine the relationships between the object types.</span></span>



| <span data-ttu-id="f1369-121">介面</span><span class="sxs-lookup"><span data-stu-id="f1369-121">Interface</span></span>                                                  | <span data-ttu-id="f1369-122">意義</span><span class="sxs-lookup"><span data-stu-id="f1369-122">Meaning</span></span>                                                                                                       | <span data-ttu-id="f1369-123">公開者</span><span class="sxs-lookup"><span data-stu-id="f1369-123">Exposed By</span></span>                        |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="f1369-124">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="f1369-124">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md) | <span data-ttu-id="f1369-125">此物件是虛擬追蹤。虛擬追蹤可以位於組合內，並保留其他時程表物件。</span><span class="sxs-lookup"><span data-stu-id="f1369-125">The object is a virtual track. Virtual tracks can reside inside compositions and hold other timeline objects.</span></span> | <span data-ttu-id="f1369-126">撰寫、追蹤</span><span class="sxs-lookup"><span data-stu-id="f1369-126">Composition, Track</span></span>                |
| [<span data-ttu-id="f1369-127">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="f1369-127">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)     | <span data-ttu-id="f1369-128">物件可能會有效果。</span><span class="sxs-lookup"><span data-stu-id="f1369-128">The object can have effects.</span></span>                                                                                  | <span data-ttu-id="f1369-129">撰寫、追蹤、來源</span><span class="sxs-lookup"><span data-stu-id="f1369-129">Composition, Track, Source</span></span>        |
| [<span data-ttu-id="f1369-130">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="f1369-130">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)       | <span data-ttu-id="f1369-131">物件可以有轉換。</span><span class="sxs-lookup"><span data-stu-id="f1369-131">The object can have transitions.</span></span>                                                                              | <span data-ttu-id="f1369-132">撰寫、追蹤</span><span class="sxs-lookup"><span data-stu-id="f1369-132">Composition, Track</span></span>                |
| [<span data-ttu-id="f1369-133">**IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="f1369-133">**IAMTimelineSplittable**</span></span>](iamtimelinesplittable.md)     | <span data-ttu-id="f1369-134">物件可以分割成兩個物件。</span><span class="sxs-lookup"><span data-stu-id="f1369-134">The object can be split into two objects.</span></span>                                                                     | <span data-ttu-id="f1369-135">追蹤、來源、效果、轉換</span><span class="sxs-lookup"><span data-stu-id="f1369-135">Track, Source, Effect, Transition</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f1369-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1369-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1369-137">時間軸元件的總覽</span><span class="sxs-lookup"><span data-stu-id="f1369-137">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 




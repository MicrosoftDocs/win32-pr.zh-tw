---
description: 參考時鐘
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: 參考時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973539"
---
# <a name="reference-clocks"></a><span data-ttu-id="48c5b-103">參考時鐘</span><span class="sxs-lookup"><span data-stu-id="48c5b-103">Reference Clocks</span></span>

<span data-ttu-id="48c5b-104">篩選圖形管理員的其中一個函式，是將圖形中的所有篩選器同步處理至相同的時鐘，稱為 *參考時鐘*。</span><span class="sxs-lookup"><span data-stu-id="48c5b-104">One function of the Filter Graph Manager is to synchronize all of the filters in the graph to the same clock, called the *reference clock*.</span></span>

<span data-ttu-id="48c5b-105">公開 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面的任何物件都可以作為參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="48c5b-105">Any object that exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface can act as the reference clock.</span></span> <span data-ttu-id="48c5b-106">您可以透過 DirectShow 篩選（通常是音訊轉譯器）提供參考時鐘來存取硬體計時器。</span><span class="sxs-lookup"><span data-stu-id="48c5b-106">The reference clock might be provided by a DirectShow filter—typically the audio renderer, which has access to a hardware timer.</span></span> <span data-ttu-id="48c5b-107">做為回復，篩選圖形管理員可以使用系統時間。</span><span class="sxs-lookup"><span data-stu-id="48c5b-107">As a fallback, the Filter Graph Manager can use the system time.</span></span>

<span data-ttu-id="48c5b-108">名義上，參考時鐘會以 100-毫微秒間隔來測量時間，雖然時鐘的實際精確度可能較少。</span><span class="sxs-lookup"><span data-stu-id="48c5b-108">Nominally, a reference clock measures time in 100-nanosecond intervals, although the actual accuracy of the clock might be less.</span></span> <span data-ttu-id="48c5b-109">若要取出時鐘的目前時間，請呼叫 [**IReferenceClock：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法。</span><span class="sxs-lookup"><span data-stu-id="48c5b-109">To retrieve the clock's current time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span> <span data-ttu-id="48c5b-110">時鐘的基準（從開始計算算起的時間）取決於執行，因此 **GetTime** 傳回的值不會有任何意義。</span><span class="sxs-lookup"><span data-stu-id="48c5b-110">The clock's baseline—the time from which it starts counting—depends on the implementation, so the value returned by **GetTime** is not inherently meaningful.</span></span> <span data-ttu-id="48c5b-111">重要的是當圖形開始執行時的差異。</span><span class="sxs-lookup"><span data-stu-id="48c5b-111">What matters is the delta from when the graph started running.</span></span>

<span data-ttu-id="48c5b-112">雖然參考時鐘的精確度可能不同，但 [**GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) 方法所傳回的時間保證會以單純方式增加。</span><span class="sxs-lookup"><span data-stu-id="48c5b-112">Although the accuracy of a reference clock can vary, the times returned by the [**GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method are guaranteed to increase monotonically.</span></span> <span data-ttu-id="48c5b-113">換句話說，時鐘時間永遠不會反向。</span><span class="sxs-lookup"><span data-stu-id="48c5b-113">In other words, clock times will never go backward.</span></span> <span data-ttu-id="48c5b-114">如果參考時鐘產生的是硬體來源的時鐘時間，而硬體時鐘會向後跳躍 (例如，如果有對時鐘) 的調整， **GetTime** 方法應該會繼續傳回上次回報的時間，直到硬體時鐘趕上為止。</span><span class="sxs-lookup"><span data-stu-id="48c5b-114">If a reference clock is generating clock times from a hardware source and the hardware clock jumps backward (for example, if there is an adjustment to the clock), the **GetTime** method should continue to return the last reported time until the hardware clock catches up.</span></span> <span data-ttu-id="48c5b-115">如需詳細資訊，請參閱 [**CBaseReferenceClock 類別**](cbasereferenceclock.md)。</span><span class="sxs-lookup"><span data-stu-id="48c5b-115">For more information, see [**CBaseReferenceClock Class**](cbasereferenceclock.md).</span></span>

<span data-ttu-id="48c5b-116">**預設參考時鐘**</span><span class="sxs-lookup"><span data-stu-id="48c5b-116">**Default Reference Clock**</span></span>

<span data-ttu-id="48c5b-117">篩選圖形管理員會在圖形執行時自動選取參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="48c5b-117">The Filter Graph Manager automatically selects a reference clock when the graph runs.</span></span> <span data-ttu-id="48c5b-118">它會使用下列演算法來選取時鐘：</span><span class="sxs-lookup"><span data-stu-id="48c5b-118">It uses the following algorithm to select the clock:</span></span>

-   <span data-ttu-id="48c5b-119">如果應用程式已選取時鐘 (請參閱下面的) ，請使用該時鐘。</span><span class="sxs-lookup"><span data-stu-id="48c5b-119">If the application has selected a clock (see below), use that clock.</span></span>
-   <span data-ttu-id="48c5b-120">如果圖形包含支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)的即時來源篩選器，請使用該篩選準則。</span><span class="sxs-lookup"><span data-stu-id="48c5b-120">If the graph contains a live source filter that supports [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), use that filter.</span></span> <span data-ttu-id="48c5b-121">如需即時來源的定義，請參閱 [即時來源](live-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="48c5b-121">For the definition of a live source, see [Live Sources](live-sources.md).</span></span>
-   <span data-ttu-id="48c5b-122">如果圖表不包含任何即時來源篩選，請使用圖形中支援 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)的任何篩選，從轉譯器開始，然後工作上游。</span><span class="sxs-lookup"><span data-stu-id="48c5b-122">If the graph does NOT contain any live source filters, use any filter in the graph that supports [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), starting from the renderers and working upstream.</span></span> <span data-ttu-id="48c5b-123">偏好未連接的篩選準則的連接篩選。</span><span class="sxs-lookup"><span data-stu-id="48c5b-123">Prefer connected filters over unconnected filters.</span></span> <span data-ttu-id="48c5b-124"> (如果圖形正在轉譯音訊串流，則演算法中的這個步驟通常會選取音訊轉譯器篩選器。 ) </span><span class="sxs-lookup"><span data-stu-id="48c5b-124">(If the graph is rendering an audio stream, this step in the algorithm will normally select the audio renderer filter.)</span></span>
-   <span data-ttu-id="48c5b-125">如果沒有任何篩選準則提供適當的時鐘，請使用 [系統參考時鐘](system-reference-clock.md)（以系統時間為基礎）。</span><span class="sxs-lookup"><span data-stu-id="48c5b-125">If no filter provides a suitable clock, use the [System Reference Clock](system-reference-clock.md), which is based on the system time.</span></span>

<span data-ttu-id="48c5b-126">**設定參考時鐘**</span><span class="sxs-lookup"><span data-stu-id="48c5b-126">**Setting the Reference Clock**</span></span>

<span data-ttu-id="48c5b-127">應用程式可以在篩選圖形管理員上呼叫 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法，以選取時鐘。</span><span class="sxs-lookup"><span data-stu-id="48c5b-127">An application can select a clock by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="48c5b-128">只有當您有特殊原因想要使用另一個時鐘時，才應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="48c5b-128">You should do this only if you have a particular reason to prefer another clock.</span></span>

<span data-ttu-id="48c5b-129">您可以藉由呼叫值 **為 Null** 的 [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) ，指示篩選圖形管理員不要使用參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="48c5b-129">You can instruct the Filter Graph Manager not to use a reference clock by calling [**SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) with the value **NULL**.</span></span> <span data-ttu-id="48c5b-130">例如，您可能會盡可能快速地處理範例。</span><span class="sxs-lookup"><span data-stu-id="48c5b-130">For example, you might do this to process samples as quickly as possible.</span></span> <span data-ttu-id="48c5b-131">若要還原預設的參考時鐘，請在篩選圖形管理員上呼叫 [**IFilterGraph：： SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) 方法。</span><span class="sxs-lookup"><span data-stu-id="48c5b-131">To restore the default reference clock, call the [**IFilterGraph::SetDefaultSyncSource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) method on the Filter Graph Manager.</span></span>

<span data-ttu-id="48c5b-132">每當參考時鐘變更時，篩選圖形管理員就會呼叫其 [**IMediaFilter：： SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) 方法來通知每個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="48c5b-132">Whenever the reference clock changes, the Filter Graph Manager notifies each filter by calling its [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="48c5b-133">應用程式永遠不應該在篩選器上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="48c5b-133">Applications should never call this method on filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48c5b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="48c5b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48c5b-135">設定圖形時鐘</span><span class="sxs-lookup"><span data-stu-id="48c5b-135">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="48c5b-136">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="48c5b-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 




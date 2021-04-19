---
description: 媒體會話事件
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: 媒體會話事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982146"
---
# <a name="media-session-events"></a><span data-ttu-id="b5686-103">媒體會話事件</span><span class="sxs-lookup"><span data-stu-id="b5686-103">Media Session Events</span></span>

<span data-ttu-id="b5686-104">大部分媒體會話的作業都會以非同步方式執行，因此應用程式必須使用媒體會話的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面來接聽事件。</span><span class="sxs-lookup"><span data-stu-id="b5686-104">Most of the Media Session's operations are performed asynchronously, so the application must listen for events by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="b5686-105"> ([**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面會繼承 **IMFMediaEventGenerator**。 ) 確切的事件順序將取決於您的應用程式，但是媒體會話幾乎會在任何情況下引發下列事件。</span><span class="sxs-lookup"><span data-stu-id="b5686-105">(The [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface inherits **IMFMediaEventGenerator**.) The exact sequence of events will depend on your application, but the following events are raised by the Media Session in almost any situation.</span></span>



| <span data-ttu-id="b5686-106">事件</span><span class="sxs-lookup"><span data-stu-id="b5686-106">Event</span></span>                                                                  | <span data-ttu-id="b5686-107">描述</span><span class="sxs-lookup"><span data-stu-id="b5686-107">Description</span></span>                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5686-108">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="b5686-108">MEEndOfPresentation</span></span>](meendofpresentation.md)                         | <span data-ttu-id="b5686-109">當媒體來源完成簡報時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-109">Raised when the media source has completed the presentation.</span></span> <span data-ttu-id="b5686-110">現在資料可能仍在管線中移動。</span><span class="sxs-lookup"><span data-stu-id="b5686-110">Data might still be moving through the pipeline at this time.</span></span>                                                                                                     |
| [<span data-ttu-id="b5686-111">MEError</span><span class="sxs-lookup"><span data-stu-id="b5686-111">MEError</span></span>](meerror.md)                                                 | <span data-ttu-id="b5686-112">在串流期間發生錯誤時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-112">Raised if an error occurs during streaming.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="b5686-113">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="b5686-113">MESessionClosed</span></span>](mesessionclosed.md)                                 | <span data-ttu-id="b5686-114">當 [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 方法完成時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-114">Raised when the [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="b5686-115">此事件是媒體會話佇列的最後一個事件。</span><span class="sxs-lookup"><span data-stu-id="b5686-115">This event is the last event that the Media Session queues.</span></span> <span data-ttu-id="b5686-116">當您收到此事件之後，就可以安全地關閉您所建立的任何媒體來源。</span><span class="sxs-lookup"><span data-stu-id="b5686-116">After you receive this event, it is safe to shut down any media sources that you created.</span></span> |
| [<span data-ttu-id="b5686-117">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="b5686-117">MESessionEnded</span></span>](mesessionended.md)                                   | <span data-ttu-id="b5686-118">當最後一個簡報完成媒體會話時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-118">Raised when the Media Session is done with the last presentation.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="b5686-119">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="b5686-119">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md) | <span data-ttu-id="b5686-120">當新的簡報開始時，會通知應用程式呈現時間。</span><span class="sxs-lookup"><span data-stu-id="b5686-120">Notifies the application of the presentation time when the new presentation will start.</span></span>                                                                                                                                        |
| [<span data-ttu-id="b5686-121">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="b5686-121">MESessionStarted</span></span>](mesessionstarted.md)                               | <span data-ttu-id="b5686-122">[**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法完成時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-122">Raised when the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes.</span></span> <span data-ttu-id="b5686-123">除非發生錯誤，否則資料會在此時間點透過管線移動。</span><span class="sxs-lookup"><span data-stu-id="b5686-123">Unless an error occurred, data is moving through the pipeline at this point.</span></span>                                                                          |
| [<span data-ttu-id="b5686-124">MESessionTopologySet</span><span class="sxs-lookup"><span data-stu-id="b5686-124">MESessionTopologySet</span></span>](mesessiontopologyset.md)                       | <span data-ttu-id="b5686-125">[**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)方法完成時引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-125">Raised when the [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes.</span></span> <span data-ttu-id="b5686-126">除非發生錯誤，否則應用程式不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="b5686-126">Unless an error occurs, the application does not need to take any action.</span></span>                                                                 |
| [<span data-ttu-id="b5686-127">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="b5686-127">MESessionTopologyStatus</span></span>](mesessiontopologystatus.md)                 | <span data-ttu-id="b5686-128">在拓撲的狀態變更時，于不同的時間引發。</span><span class="sxs-lookup"><span data-stu-id="b5686-128">Raised at various times when the status of a topology changes.</span></span>                                                                                                                                                                 |



 

<span data-ttu-id="b5686-129">[**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)方法不會引發事件。</span><span class="sxs-lookup"><span data-stu-id="b5686-129">The [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) method does not raise an event.</span></span> <span data-ttu-id="b5686-130">**Shutdown** 方法是同步的。</span><span class="sxs-lookup"><span data-stu-id="b5686-130">The **Shutdown** method is synchronous.</span></span> <span data-ttu-id="b5686-131">在這個方法傳回之後，就可以安全地釋放您的事件回呼指標。</span><span class="sxs-lookup"><span data-stu-id="b5686-131">After this method returns, it is safe to release your event callback pointer.</span></span>

<span data-ttu-id="b5686-132">除了來自媒體會話的事件之外，應用程式可能會從拓撲中的媒體接收器接收事件。</span><span class="sxs-lookup"><span data-stu-id="b5686-132">In addition to events from the Media Session, the application might receive events from the media sinks in the topology.</span></span> <span data-ttu-id="b5686-133">這些可以是媒體接收所定義的自訂事件，可能包含任意資料。</span><span class="sxs-lookup"><span data-stu-id="b5686-133">These can be custom events defined by the media sink, which might contain arbitrary data.</span></span> <span data-ttu-id="b5686-134">例如，接收可能會從來源資料衍生事件資料，而該資料可能來自不受信任的外部來源。</span><span class="sxs-lookup"><span data-stu-id="b5686-134">For example, the sink might derive the event data from the source data, which can be from an untrusted external source.</span></span> <span data-ttu-id="b5686-135">應用程式應該忽略無法辨識的任何事件，並在剖析事件資料時特別小心。</span><span class="sxs-lookup"><span data-stu-id="b5686-135">An application should ignore any events that it does not recognize, and exercise caution when parsing event data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5686-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5686-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5686-137">媒體會話</span><span class="sxs-lookup"><span data-stu-id="b5686-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




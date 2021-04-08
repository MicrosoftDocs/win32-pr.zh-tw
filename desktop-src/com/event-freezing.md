---
title: 事件凍結
description: 事件凍結
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839928"
---
# <a name="event-freezing"></a><span data-ttu-id="fded8-103">事件凍結</span><span class="sxs-lookup"><span data-stu-id="fded8-103">Event Freezing</span></span>

<span data-ttu-id="fded8-104">容器可透過呼叫 [**IOleControl：： FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) 和 **TRUE**，通知控制項尚未準備好回應事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-104">A container can notify a control that it is not ready to respond to events by calling [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE**.</span></span> <span data-ttu-id="fded8-105">它可以藉由呼叫 **FreezeEvents** 和 **FALSE** 來解除凍結事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-105">It can unfreeze the events by calling **FreezeEvents** with **FALSE**.</span></span> <span data-ttu-id="fded8-106">當容器凍結事件時，它會凍結事件處理，而不是事件接收;也就是說，當事件凍結時，容器仍然可以接收事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-106">When a container freezes events, it is freezing event processing, not event receiving; that is, a container can still receive events while events are frozen.</span></span> <span data-ttu-id="fded8-107">如果容器在事件被凍結時收到事件通知，容器應忽略該事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-107">If a container receives an event notification while its events are frozen, the container should ignore the event.</span></span> <span data-ttu-id="fded8-108">沒有其他適用的動作。</span><span class="sxs-lookup"><span data-stu-id="fded8-108">No other action is appropriate.</span></span>

<span data-ttu-id="fded8-109">如果控制項對 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)的呼叫很重要，則控制項應該要記下容器的呼叫，如果沒有遺漏 **事件的話。**</span><span class="sxs-lookup"><span data-stu-id="fded8-109">A control should take note of a container's call to [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **TRUE** if it is important to the control that an event is not missed.</span></span> <span data-ttu-id="fded8-110">當容器的事件處理被凍結時，控制項應該執行下列其中一項技術：</span><span class="sxs-lookup"><span data-stu-id="fded8-110">While a container's event processing is frozen, a control should implement one of the following techniques:</span></span>

-   <span data-ttu-id="fded8-111">引發事件，瞭解容器不會採取任何動作的完整知識。</span><span class="sxs-lookup"><span data-stu-id="fded8-111">Fire the events in the full knowledge that the container will take no action.</span></span>
-   <span data-ttu-id="fded8-112">捨棄控制項將引發的所有事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-112">Discard all events that the control would have fired.</span></span>
-   <span data-ttu-id="fded8-113">將所有暫止的事件排入佇列，並在容器以 **FALSE** 呼叫 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)之後引發這些事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-113">Queue up all pending events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>
-   <span data-ttu-id="fded8-114">只將相關或重要的事件排入佇列，並在容器以 **FALSE** 呼叫 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)之後引發這些事件。</span><span class="sxs-lookup"><span data-stu-id="fded8-114">Queue up only relevant or important events and fire them after the container has called [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) with **FALSE**.</span></span>

<span data-ttu-id="fded8-115">在不同的情況下，每個技巧都是可接受的。</span><span class="sxs-lookup"><span data-stu-id="fded8-115">Each technique is acceptable and appropriate in different circumstances.</span></span> <span data-ttu-id="fded8-116">控制項開發人員負責決定和執行控制項功能的適當技術。</span><span class="sxs-lookup"><span data-stu-id="fded8-116">The control developer is responsible for determining and implementing the appropriate technique for the control's functionality.</span></span>

 

 





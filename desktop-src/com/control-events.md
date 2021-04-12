---
title: 控制 COM) 的事件 (
description: 除了提供屬性和方法之外，控制項也提供輸出介面來通知其用戶端事件。
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024447"
---
# <a name="control-events-com"></a><span data-ttu-id="bddb0-103">控制 COM) 的事件 (</span><span class="sxs-lookup"><span data-stu-id="bddb0-103">Control Events (COM)</span></span>

<span data-ttu-id="bddb0-104">除了提供屬性和方法之外，控制項也提供輸出介面來通知其用戶端事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-104">In addition to providing properties and methods, a control also provides outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="bddb0-105">用戶端必須支援這些事件的處理。</span><span class="sxs-lookup"><span data-stu-id="bddb0-105">The client must support handling of these events.</span></span> <span data-ttu-id="bddb0-106">如需可連線物件如何運作的詳細資訊，請參閱 [COM 中的事件和](events-in-com-and-connectable-objects.md) 可連接的物件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-106">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

<span data-ttu-id="bddb0-107">控制項可以針對不同目的支援不同的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="bddb0-107">A control can support different outgoing interfaces for different purposes.</span></span> <span data-ttu-id="bddb0-108">所有輸出介面都會標示為控制項類型資訊中的來源介面，但只有一個會標示為預設值，表示它是主要的輸出介面。</span><span class="sxs-lookup"><span data-stu-id="bddb0-108">All outgoing interfaces are marked as source interfaces in the control's type information, but only one is marked default to indicate that it is the primary outgoing interface.</span></span>

<span data-ttu-id="bddb0-109">容器可支援一個或多個由控制項定義的連出介面。</span><span class="sxs-lookup"><span data-stu-id="bddb0-109">A container can support one or more of the outgoing interfaces defined by a control.</span></span> <span data-ttu-id="bddb0-110">控制項應該準備好處理只提供某些輸出介面支援的容器。</span><span class="sxs-lookup"><span data-stu-id="bddb0-110">The control should be prepared to deal with containers that only provide support for some of their outgoing interfaces.</span></span>

<span data-ttu-id="bddb0-111">控制項支援四種類型的事件：</span><span class="sxs-lookup"><span data-stu-id="bddb0-111">Controls support four kinds of events:</span></span>

-   <span data-ttu-id="bddb0-112">要求事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-112">Request events.</span></span> <span data-ttu-id="bddb0-113">控制項會要求其用戶端的許可權，藉由呼叫輸出介面中的方法來進行某個動作，進而觸發要求事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-113">A control requests permission from its client to do something by calling a method in the outgoing interface, thus triggering a request event.</span></span> <span data-ttu-id="bddb0-114">用戶端會在控制項呼叫的方法中，透過布林值 out 參數來對控制項發出信號。</span><span class="sxs-lookup"><span data-stu-id="bddb0-114">The client signals the control through a boolean, out-parameter in the method that the control called.</span></span> <span data-ttu-id="bddb0-115">因此，用戶端可以防止控制項執行動作。</span><span class="sxs-lookup"><span data-stu-id="bddb0-115">The client can thus prevent the control from performing the action.</span></span>
-   <span data-ttu-id="bddb0-116">之前的事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-116">Before events.</span></span> <span data-ttu-id="bddb0-117">控制項會通知其用戶端，它會藉由呼叫輸出介面中的方法來進行某個動作，進而觸發 before 事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-117">A control notifies its client hat it is going to do something by calling a method in the outgoing interface, thus triggering a before event.</span></span> <span data-ttu-id="bddb0-118">用戶端沒有機會可以防止該動作，但它可以採取任何必要的步驟，並指定即將發生的動作。</span><span class="sxs-lookup"><span data-stu-id="bddb0-118">The client does not have the opportunity to prevent the action, but it can take any necessary steps given the action that is about to occur.</span></span>
-   <span data-ttu-id="bddb0-119">After 事件之後。</span><span class="sxs-lookup"><span data-stu-id="bddb0-119">After events.</span></span> <span data-ttu-id="bddb0-120">控制項會通知其用戶端，它只會在輸出介面中呼叫方法來完成某項工作，進而觸發 after 事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-120">A control notifies its client that it has just done something by calling a method in the outgoing interface, thus triggering an after event.</span></span> <span data-ttu-id="bddb0-121">同樣地，用戶端無法取消此動作，但它可以採取必要的步驟，並提供所發生的動作。</span><span class="sxs-lookup"><span data-stu-id="bddb0-121">Again, the client cannot cancel this action, but it can take necessary steps given the action that has occurred.</span></span>
-   <span data-ttu-id="bddb0-122">進行事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-122">Do events.</span></span> <span data-ttu-id="bddb0-123">控制項會觸發 do 事件，以允許其用戶端覆寫控制項的動作，並提供一些替代或補充動作。</span><span class="sxs-lookup"><span data-stu-id="bddb0-123">A control triggers a do event to allow its client to override the control's action and provide some alternative or supplementary actions.</span></span> <span data-ttu-id="bddb0-124">通常，控制項針對 do 事件所呼叫的方法，有許多參數可與用戶端協商將會發生的動作。</span><span class="sxs-lookup"><span data-stu-id="bddb0-124">Usually, the method that a control calls for a do event has a number of parameters for negotiating with the client about the actions that will occur.</span></span>

<span data-ttu-id="bddb0-125">下列 dispid 是針對控制項可支援的標準事件所定義： Click、DblClick、KeyDown、KeyPress、KeyUp、MouseMove、MouseUp 和 Error。</span><span class="sxs-lookup"><span data-stu-id="bddb0-125">The following dispids are defined for standard events that controls can support: Click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp, and Error.</span></span> <span data-ttu-id="bddb0-126">所有這些標準事件都有負的 DISPID 值，表示其標準狀態。</span><span class="sxs-lookup"><span data-stu-id="bddb0-126">All of these standard events have negative DISPID values, indicating their standard status.</span></span>

<span data-ttu-id="bddb0-127">以 **TRUE** 呼叫 [**IOleControl：： FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)方法時，會告知控制項容器是否會從控制項中處理事件，直到再次以 **FALSE** 呼叫 **FreezeEvents** 為止。</span><span class="sxs-lookup"><span data-stu-id="bddb0-127">The [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) method, when called with **TRUE**, tells a control whether the container will bother handling events from the control until **FreezeEvents** is again called with **FALSE**.</span></span> <span data-ttu-id="bddb0-128">在這段時間內，控制權無法相依于實際處理任何事件的容器。</span><span class="sxs-lookup"><span data-stu-id="bddb0-128">During this time control cannot depend on the container actually handling any events.</span></span> <span data-ttu-id="bddb0-129">如果必須處理事件，控制項應該將事件排入佇列，以便在以 **FALSE** 呼叫 **FreezeEvents** 時引發事件。</span><span class="sxs-lookup"><span data-stu-id="bddb0-129">If an event must be handled, the control should queue the event in order to fire it when **FreezeEvents** is called with **FALSE**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bddb0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="bddb0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bddb0-131">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="bddb0-131">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 





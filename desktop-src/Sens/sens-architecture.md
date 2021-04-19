---
description: 系統事件通知服務適用于 COM + 事件系統。
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: SENS 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981198"
---
# <a name="sens-architecture"></a><span data-ttu-id="0a05b-103">SENS 架構</span><span class="sxs-lookup"><span data-stu-id="0a05b-103">SENS Architecture</span></span>

<span data-ttu-id="0a05b-104">系統事件通知服務適用于 COM + 事件系統。</span><span class="sxs-lookup"><span data-stu-id="0a05b-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="0a05b-105">SENS 是它所監視的事件類別的事件發行者：網路、登入和電源/電池事件。</span><span class="sxs-lookup"><span data-stu-id="0a05b-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="0a05b-106">接收通知的應用程式稱為「事件訂閱者」。</span><span class="sxs-lookup"><span data-stu-id="0a05b-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="0a05b-107">當應用程式訂閱接收通知時，也可以指定與訂閱的事件相關聯的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="0a05b-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="0a05b-108">SENS 和 COM + 事件會使用篩選器，進一步判斷應用程式應該收到通知的時機。</span><span class="sxs-lookup"><span data-stu-id="0a05b-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="0a05b-109">通知是非同步，因此在傳送通知時，接收通知的應用程式不一定要處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="0a05b-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="0a05b-110">當應用程式訂閱接收通知時，它可以指定事件發生時是否應該啟動，或稍後在活動啟用時通知。</span><span class="sxs-lookup"><span data-stu-id="0a05b-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="0a05b-111">只有在應用程式停止執行之前，訂用帳戶可以是暫時性且有效的，否則它可能會一直有效，直到從系統移除應用程式為止。</span><span class="sxs-lookup"><span data-stu-id="0a05b-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="0a05b-112">COM + 事件資料存放區包含事件發行者 (SENS) 、事件訂閱者和篩選器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0a05b-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="0a05b-113">SENS 也會針對類型程式庫中的每個事件類別預先定義輸出介面。</span><span class="sxs-lookup"><span data-stu-id="0a05b-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="0a05b-114">事件類別</span><span class="sxs-lookup"><span data-stu-id="0a05b-114">Event class</span></span>    | <span data-ttu-id="0a05b-115">GUID</span><span class="sxs-lookup"><span data-stu-id="0a05b-115">GUID</span></span>                          | <span data-ttu-id="0a05b-116">介面</span><span class="sxs-lookup"><span data-stu-id="0a05b-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="0a05b-117">網路事件</span><span class="sxs-lookup"><span data-stu-id="0a05b-117">Network events</span></span> | <span data-ttu-id="0a05b-118">SENSGUID \_ EVENTCLASS \_ 網路</span><span class="sxs-lookup"><span data-stu-id="0a05b-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="0a05b-119">ISensNetwork</span><span class="sxs-lookup"><span data-stu-id="0a05b-119">ISensNetwork</span></span> |
| <span data-ttu-id="0a05b-120">登入事件</span><span class="sxs-lookup"><span data-stu-id="0a05b-120">Logon events</span></span>   | <span data-ttu-id="0a05b-121">SENSGUID \_ EVENTCLASS \_ 登入</span><span class="sxs-lookup"><span data-stu-id="0a05b-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="0a05b-122">ISensLogon</span><span class="sxs-lookup"><span data-stu-id="0a05b-122">ISensLogon</span></span>   |
| <span data-ttu-id="0a05b-123">電源活動</span><span class="sxs-lookup"><span data-stu-id="0a05b-123">Power events</span></span>   | <span data-ttu-id="0a05b-124">SENSGUID \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="0a05b-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="0a05b-125">ISensOnNow</span><span class="sxs-lookup"><span data-stu-id="0a05b-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="0a05b-126">若要接收任何這些事件的通知，您的應用程式必須執行下列兩項作業：</span><span class="sxs-lookup"><span data-stu-id="0a05b-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="0a05b-127">訂閱您感興趣的 SENS 事件。</span><span class="sxs-lookup"><span data-stu-id="0a05b-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="0a05b-128">若要訂閱事件，請在 COM + 事件中使用 **IEventSubscription** 和 **IEventSystem** 介面。</span><span class="sxs-lookup"><span data-stu-id="0a05b-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="0a05b-129">您必須提供事件類別的識別碼和 SENS 發行者識別碼 SENSGUID \_ 發行者。</span><span class="sxs-lookup"><span data-stu-id="0a05b-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="0a05b-130">訂用帳戶在每個事件層級上，因此訂閱應用程式也必須指定類別中的哪些事件有興趣。</span><span class="sxs-lookup"><span data-stu-id="0a05b-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="0a05b-131">每個事件都會對應至介面中對應至其事件類別的方法。</span><span class="sxs-lookup"><span data-stu-id="0a05b-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="0a05b-132">針對您處理的每個介面，建立具有執行的接收物件。</span><span class="sxs-lookup"><span data-stu-id="0a05b-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="0a05b-133">如需這些介面和各介面所支援之事件的詳細資訊，請參閱 [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)、 [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)和 [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) 。</span><span class="sxs-lookup"><span data-stu-id="0a05b-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="0a05b-134">當其中一個受監視的事件發生時，SENS 會使用任何相關聯的篩選來處理每個訂閱，並透過 COM + 事件系統通知訂閱者。</span><span class="sxs-lookup"><span data-stu-id="0a05b-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 




---
title: 接收變更的通知
description: 許多用戶端可以同時更新路由表，而且用戶端必須在路由資訊發生變更時收到通知。
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacd8d1d0329cf29be82a890be30b602b9330249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372076"
---
# <a name="receiving-notification-of-changes"></a><span data-ttu-id="b107c-103">接收變更的通知</span><span class="sxs-lookup"><span data-stu-id="b107c-103">Receiving Notification of Changes</span></span>

<span data-ttu-id="b107c-104">許多用戶端可以同時更新路由表，而且用戶端必須在路由資訊發生變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="b107c-104">Many clients can simultaneously update the routing table, and clients must be notified when changes to routing information occur.</span></span> <span data-ttu-id="b107c-105">例如，未收到其他用戶端對路由表之變更通知的用戶端，可能會公告過期的路由資訊。</span><span class="sxs-lookup"><span data-stu-id="b107c-105">For example, a client that is not notified of another client's changes to the routing table could advertise outdated route information.</span></span> <span data-ttu-id="b107c-106">藉由程式設計用戶端註冊路由表管理員來註冊路由表中的變更，就可以防止這種情況。</span><span class="sxs-lookup"><span data-stu-id="b107c-106">This can be prevented by programming clients to register with the routing table manager to be notified of changes in the routing table.</span></span> <span data-ttu-id="b107c-107">路由表管理員會將變更的通知傳送給所有註冊用來接收這些用戶端的用戶端。</span><span class="sxs-lookup"><span data-stu-id="b107c-107">The routing table manager sends notifications of changes to all clients that register to receive them.</span></span>

<span data-ttu-id="b107c-108">變更通知只適用于目的地。</span><span class="sxs-lookup"><span data-stu-id="b107c-108">Change notification applies only to destinations.</span></span> <span data-ttu-id="b107c-109">沒有任何方法可以查詢路由表管理員是否有特定路由的變更。</span><span class="sxs-lookup"><span data-stu-id="b107c-109">There is no way to query the routing table manager for changes to a particular route.</span></span>

<span data-ttu-id="b107c-110">對目的地的其中一個路由進行變更時，路由表管理員會送出已發生變更的通知。</span><span class="sxs-lookup"><span data-stu-id="b107c-110">When a change is made to one of the routes to a destination, the routing table manager sends out a notification that a change has occurred.</span></span> <span data-ttu-id="b107c-111">這項通知只會傳送到已向路由表管理員註冊的用戶端，以瞭解所發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="b107c-111">This notification goes only to those clients that have registered with the routing table manager for the type of change that has occurred.</span></span> <span data-ttu-id="b107c-112">路由表管理員中路由資訊的所有變更都會出現在一或多個視圖中，而且可以在任何支援的視圖子集中要求變更通知訊息。</span><span class="sxs-lookup"><span data-stu-id="b107c-112">All changes to routing information in the routing table manager occur in one or more views, and change notification messages can be requested in any subset of supported views.</span></span>

<span data-ttu-id="b107c-113">目前有三種類型的變更通知可供用戶端註冊：</span><span class="sxs-lookup"><span data-stu-id="b107c-113">There are currently three types of change notifications for which a client can register:</span></span>

-   <span data-ttu-id="b107c-114">對目的地的路由進行任何變更的通知。</span><span class="sxs-lookup"><span data-stu-id="b107c-114">Notification of any change to the routes for the destination.</span></span> <span data-ttu-id="b107c-115">此要求是使用 RTM 「 \_ 變更 \_ 類型全部」旗標進行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b107c-115">This request is made using the RTM\_CHANGE\_TYPE\_ALL flag.</span></span>
-   <span data-ttu-id="b107c-116">如果目的地的最佳路由變更，或目前最佳路由變更的下列任何資訊，則會發出通知：</span><span class="sxs-lookup"><span data-stu-id="b107c-116">Notification if the best route to the destination changes, or any of the following information for the current best route changes:</span></span>

    -   <span data-ttu-id="b107c-117">喜好設定</span><span class="sxs-lookup"><span data-stu-id="b107c-117">Preference</span></span>
    -   <span data-ttu-id="b107c-118">下一個躍點</span><span class="sxs-lookup"><span data-stu-id="b107c-118">Next hops</span></span>
    -   <span data-ttu-id="b107c-119">路由旗標</span><span class="sxs-lookup"><span data-stu-id="b107c-119">Route flags</span></span>

    <span data-ttu-id="b107c-120">此要求是使用 RTM \_ 變更類型的 \_ \_ 最佳旗標進行。</span><span class="sxs-lookup"><span data-stu-id="b107c-120">This request is made using the RTM\_CHANGE\_TYPE\_BEST flag.</span></span>

-   <span data-ttu-id="b107c-121">類型 RTM 變更類型的所有變更的 \_ 通知 \_ \_ ，最適合最大路由中非轉送旗標的變更。</span><span class="sxs-lookup"><span data-stu-id="b107c-121">Notification of all changes of the type RTM\_CHANGE\_TYPE\_BEST, except changes in non-forwarding flags in the best route.</span></span> <span data-ttu-id="b107c-122">例如，路由器管理員會在單點傳送視圖中等待此類型的變更，並更新單播轉寄站中的資訊。</span><span class="sxs-lookup"><span data-stu-id="b107c-122">For example, the router manager waits for changes of this type in the unicast view, and updates information in the unicast forwarder.</span></span> <span data-ttu-id="b107c-123">此要求是使用 RTM \_ 變更 \_ 類型 \_ 轉送旗標進行。</span><span class="sxs-lookup"><span data-stu-id="b107c-123">This request is made using the RTM\_CHANGE\_TYPE\_FORWARDING flag.</span></span>

<span data-ttu-id="b107c-124">變更通知的要求也可以藉由將變更通知註冊為「標示」的目的地，限制為目的地的子集。</span><span class="sxs-lookup"><span data-stu-id="b107c-124">Requests for notifications of changes can also be restricted to a subset of destinations by registering for notifications of changes only to "marked" destinations.</span></span> <span data-ttu-id="b107c-125">用戶端可以藉由呼叫 [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification)來標示變更通知的目的地。</span><span class="sxs-lookup"><span data-stu-id="b107c-125">The client can mark a destination for change notification by calling [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).</span></span>

<span data-ttu-id="b107c-126">發生變更時，路由表管理員會檢查是否有任何用戶端必須收到這項變更的通知。</span><span class="sxs-lookup"><span data-stu-id="b107c-126">When a change occurs, the routing table manager checks to see if there are any clients that must be notified of this change.</span></span> <span data-ttu-id="b107c-127">如果符合下列所有條件，用戶端必須收到變更通知：</span><span class="sxs-lookup"><span data-stu-id="b107c-127">A client must be notified of a change if all of the following conditions are met:</span></span>

-   <span data-ttu-id="b107c-128">發生的變更類型是用戶端已註冊通知的類型</span><span class="sxs-lookup"><span data-stu-id="b107c-128">The type of change that occurred is a type for which the client has registered for notification</span></span>
-   <span data-ttu-id="b107c-129">如果用戶端已要求所有目的地的變更，則會變更用戶端已標示的目的地，或任何目的地</span><span class="sxs-lookup"><span data-stu-id="b107c-129">Changes to a destination that the client has marked have occurred or any destination, if the client has requested changes for all destinations</span></span>
-   <span data-ttu-id="b107c-130">用戶端已要求發生此變更之視圖的變更通知</span><span class="sxs-lookup"><span data-stu-id="b107c-130">The client requested change notification for the view in which this change occurred</span></span>

<span data-ttu-id="b107c-131">如果變更符合上述所有條件，則會快取此變更，並通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="b107c-131">If the change meets all of the above criteria, the change is cached and the client is notified.</span></span>

<span data-ttu-id="b107c-132">通知不會指定實際變更的內容，只會指出已發生的變更。</span><span class="sxs-lookup"><span data-stu-id="b107c-132">The notification does not specify what the actual changes are, only that they have occurred.</span></span> <span data-ttu-id="b107c-133">用戶端必須使用從先前呼叫 [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)取得的通知控制碼來呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) ，以取出變更。</span><span class="sxs-lookup"><span data-stu-id="b107c-133">The client must retrieve the changes by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) using the notification handle that was obtained from a previous call to [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).</span></span>

 

 





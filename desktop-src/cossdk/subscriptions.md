---
description: 訂用帳戶資料位於訂用帳戶 COM + 目錄中。 您可以使用 [元件服務] 系統管理工具或使用 ICOMAdminCatalog：： InstallComponent 介面以程式設計方式建立訂用帳戶。
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: 訂用帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187707"
---
# <a name="subscriptions"></a><span data-ttu-id="9b839-104">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="9b839-104">Subscriptions</span></span>

<span data-ttu-id="9b839-105">訂用帳戶資料位於訂用帳戶 COM + 目錄中。</span><span class="sxs-lookup"><span data-stu-id="9b839-105">Subscription data resides in the subscription COM+ catalog.</span></span> <span data-ttu-id="9b839-106">您可以使用 [元件服務] 系統管理工具或使用 [**ICOMAdminCatalog：： InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) 介面以程式設計方式建立訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="9b839-106">A subscription can be created either by using the Component Services administrative tool or programmatically by using the [**ICOMAdminCatalog::InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) interface.</span></span>

<span data-ttu-id="9b839-107">[**SubscriptionsForComponent**](subscriptionsforcomponent.md)集合是用來新增、刪除或變更訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b839-107">The [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection is used to add, delete, or change information pertaining to subscriptions.</span></span> <span data-ttu-id="9b839-108">**SubscriptionsForComponent** 集合是元件的子集合。</span><span class="sxs-lookup"><span data-stu-id="9b839-108">The **SubscriptionsForComponent** collection is a child collection to a component.</span></span> <span data-ttu-id="9b839-109">若要加入訂用帳戶，請取得元件的 **SubscriptionsForComponent** 集合，並使用 [**add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) 方法將專案加入至集合。</span><span class="sxs-lookup"><span data-stu-id="9b839-109">To add a subscription, get the component's **SubscriptionsForComponent** collection and use the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method to add an entry to the collection.</span></span> <span data-ttu-id="9b839-110">若要設定訂用帳戶物件的各種屬性，請使用 [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b839-110">To set up the various properties of the subscription object, use the [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) property.</span></span> <span data-ttu-id="9b839-111">若要儲存變更，請使用 **SubscriptionsForComponent** 集合物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 。</span><span class="sxs-lookup"><span data-stu-id="9b839-111">To save the changes, use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the **SubscriptionsForComponent** collection object.</span></span>

<span data-ttu-id="9b839-112">您也可以使用「元件服務」系統管理工具來修改部分（但不是全部）的訂用帳戶屬性。</span><span class="sxs-lookup"><span data-stu-id="9b839-112">You can also use the Component Services administration tool to modify some, but not all, of the subscription properties.</span></span> <span data-ttu-id="9b839-113">訂閱會指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="9b839-113">Subscriptions specify the following information:</span></span>

-   <span data-ttu-id="9b839-114">訂閱者的身分識別和位置</span><span class="sxs-lookup"><span data-stu-id="9b839-114">Identity and location of the subscriber</span></span>
-   <span data-ttu-id="9b839-115">傳遞方法</span><span class="sxs-lookup"><span data-stu-id="9b839-115">Delivery method</span></span>
-   <span data-ttu-id="9b839-116">要傳遞的事件方法</span><span class="sxs-lookup"><span data-stu-id="9b839-116">Event methods to deliver</span></span>
-   <span data-ttu-id="9b839-117">訂閱者想要從中接收事件之事件類別元件的事件類別物件和 PublisherID 屬性</span><span class="sxs-lookup"><span data-stu-id="9b839-117">Event class object and PublisherID property of an event class component from which the subscriber wants to receive events</span></span>

<span data-ttu-id="9b839-118">訂閱與事件類別物件分開存在。</span><span class="sxs-lookup"><span data-stu-id="9b839-118">Subscriptions exist independently from event class objects.</span></span> <span data-ttu-id="9b839-119">您可以將 [已啟用] 屬性設定為 [False]，以停用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="9b839-119">You can disable a subscription by setting the Enabled property to False.</span></span> <span data-ttu-id="9b839-120">COM + 事件不會呼叫已停用的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="9b839-120">A disabled subscription is not called by COM+ Events.</span></span>

<span data-ttu-id="9b839-121">這三種訂用帳戶類型如下：</span><span class="sxs-lookup"><span data-stu-id="9b839-121">The three types of subscriptions are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="9b839-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>持續</span><span class="sxs-lookup"><span data-stu-id="9b839-122"><span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>Persistent</span></span>
</dt> <dd>

<span data-ttu-id="9b839-123">持續性訂用帳戶位於 COM + 目錄中，而且與訂閱者的存留期無關。</span><span class="sxs-lookup"><span data-stu-id="9b839-123">Persistent subscriptions reside in the COM+ catalog and are independent from the subscriber's lifetime.</span></span> <span data-ttu-id="9b839-124">持續性訂閱會在系統重新開機後存活。</span><span class="sxs-lookup"><span data-stu-id="9b839-124">Persistent subscriptions survive a system restart.</span></span> <span data-ttu-id="9b839-125">一般而言，當應用程式安裝在訂閱者的電腦上，並在移除應用程式時移除時，就會建立持續性訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b839-125">Generally, a persistent subscription is created when an application is installed on a subscriber's computer and removed when the application is removed.</span></span> <span data-ttu-id="9b839-126">建立持續性訂閱之後，COM + 事件會在每次傳遞事件時啟動訂閱者。</span><span class="sxs-lookup"><span data-stu-id="9b839-126">After a persistent subscription is created, COM+ Events activates the subscriber each time an event should be delivered to it.</span></span>

<span data-ttu-id="9b839-127">當發行者具現化並在 [事件類別](the-com--event-class-object.md) 物件上進行呼叫時，物件會在 com + 目錄中尋找所有持續性的訂閱，並為每個物件建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="9b839-127">When a publisher instantiates and makes a call on an [event class](the-com--event-class-object.md) object, the object looks for all the persistent subscriptions in the COM+ catalog and creates a new instance of each object.</span></span> <span data-ttu-id="9b839-128">建立程式可以是直接或透過已排入佇列之元件的標記。</span><span class="sxs-lookup"><span data-stu-id="9b839-128">The creation process can be either direct or through a moniker for queued components.</span></span> <span data-ttu-id="9b839-129">依訂用帳戶的 [**SubscriberMoniker**](subscriptionsforcomponent.md) 屬性來指定訂閱者物件。</span><span class="sxs-lookup"><span data-stu-id="9b839-129">Specify the subscriber object by the [**SubscriberMoniker**](subscriptionsforcomponent.md) property of the subscription.</span></span> <span data-ttu-id="9b839-130">持續性訂用帳戶所建立的訂閱者物件一律會在每次事件呼叫之後釋放。</span><span class="sxs-lookup"><span data-stu-id="9b839-130">Subscriber objects created by a persistent subscription are always released after each event call.</span></span>

</dd> <dt>

<span data-ttu-id="9b839-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>瞬 態</span><span class="sxs-lookup"><span data-stu-id="9b839-131"><span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>Transient</span></span>
</dt> <dd>

<span data-ttu-id="9b839-132">對於暫時性訂閱，您可以使用 [**TransientSubscriptions**](transientsubscriptions.md) 集合，其父物件是根目錄物件。</span><span class="sxs-lookup"><span data-stu-id="9b839-132">For transient subscriptions, you can use the [**TransientSubscriptions**](transientsubscriptions.md) collection, whose parent object is the root catalog object.</span></span> <span data-ttu-id="9b839-133">暫時性訂閱會要求已存在之特定訂閱者物件的事件。</span><span class="sxs-lookup"><span data-stu-id="9b839-133">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="9b839-134">暫時性訂閱會儲存在 COM + 目錄中，但如果事件系統或作業系統停止，就會刪除訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b839-134">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="9b839-135">與持續性訂閱不同的是，暫時性訂閱會系結至特定的物件，而且只會儲存在事件系統中。</span><span class="sxs-lookup"><span data-stu-id="9b839-135">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="9b839-136">暫時性訂用帳戶可比持續性訂閱更有效率，但您必須管理其物件生命週期。</span><span class="sxs-lookup"><span data-stu-id="9b839-136">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span> <span data-ttu-id="9b839-137">如需註冊暫時性訂閱的詳細資訊，請參閱 [註冊暫時性訂用](registering-a-transient-subscription.md)帳戶。</span><span class="sxs-lookup"><span data-stu-id="9b839-137">For information about registering a transient subscription, see [Registering a Transient Subscription](registering-a-transient-subscription.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b839-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>每位使用者</span><span class="sxs-lookup"><span data-stu-id="9b839-138"><span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>Per user</span></span>
</dt> <dd>

<span data-ttu-id="9b839-139">只有當訂閱者登入事件系統的電腦時，每個使用者訂閱才可以提供事件。</span><span class="sxs-lookup"><span data-stu-id="9b839-139">Per User subscriptions can deliver events only when the subscriber is logged on to the event system's computer.</span></span> <span data-ttu-id="9b839-140">當訂閱者登入時，事件系統會啟用 *PerUser* 旗標設為 **TRUE** 的所有訂用帳戶，並將 *UserName* 設定為登入之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b839-140">When the subscriber logs on, the event system enables all subscriptions on which the *PerUser* flag is set to **TRUE** and *UserName* is set to the name of the user who is logged on.</span></span> <span data-ttu-id="9b839-141">當訂閱者登出時，就會停用訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b839-141">When the subscriber logs off, the subscriptions are disabled.</span></span>

<span data-ttu-id="9b839-142">只有當「發行者」和「訂閱者」位於同一部電腦時，每個使用者訂閱才會生效。</span><span class="sxs-lookup"><span data-stu-id="9b839-142">Per User subscriptions are effective only when the publisher and subscriber are on the same computer.</span></span> <span data-ttu-id="9b839-143">只有在發行者電腦上才會偵測到登入和登出，而不是在訂閱者物件所在的電腦上偵測到。</span><span class="sxs-lookup"><span data-stu-id="9b839-143">Logon and logoff are detected only at the publisher's computer—not the computer on which the subscriber object resides.</span></span>

</dd> </dl>

<span data-ttu-id="9b839-144">事件系統會在建立、修改或移除事件類別物件或訂用帳戶時，使用中繼事件來通知有興趣的訂閱者。</span><span class="sxs-lookup"><span data-stu-id="9b839-144">The event system uses meta-events to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span> <span data-ttu-id="9b839-145">若要從事件系統接收中繼事件，應用程式必須建立位於事件系統電腦上的訂用帳戶，並指定引發介面識別碼 (IID \_ IEventObjectChange) 。</span><span class="sxs-lookup"><span data-stu-id="9b839-145">To receive meta-events from the event system, applications must create a subscription that resides on the event system's computer and that specifies the firing interface ID (IID\_IEventObjectChange).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b839-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b839-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b839-147">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="9b839-147">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="9b839-148">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="9b839-148">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="9b839-149">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="9b839-149">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="9b839-150">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="9b839-150">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 




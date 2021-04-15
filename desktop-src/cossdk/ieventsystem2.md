---
description: 由 Microsoft Internet Explorer 系統事件通知服務使用 (SENS) 來存取事件資料存放區。 這個介面會擴充 IEventSystem 介面。
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: IEventSystem2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468385"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="9ca55-104">IEventSystem2 介面</span><span class="sxs-lookup"><span data-stu-id="9ca55-104">IEventSystem2 interface</span></span>

<span data-ttu-id="9ca55-105">由 Microsoft Internet Explorer 系統事件通知服務使用 (SENS) 來存取事件資料存放區。</span><span class="sxs-lookup"><span data-stu-id="9ca55-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="9ca55-106">這個介面會擴充 [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) 介面。</span><span class="sxs-lookup"><span data-stu-id="9ca55-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9ca55-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="9ca55-107">When to implement</span></span>

<span data-ttu-id="9ca55-108">您不需要執行 **IEventSystem2** 介面。</span><span class="sxs-lookup"><span data-stu-id="9ca55-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="9ca55-109">系統提供的事件系統物件 (CLSID \_ CEventSystem) 實行 **IEventSystem2**。</span><span class="sxs-lookup"><span data-stu-id="9ca55-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="9ca55-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="9ca55-110">When to use</span></span>

<span data-ttu-id="9ca55-111">如果您使用 SENS，您可以呼叫 **IEventSystem2** 的方法，在事件存放區中新增和移除物件，以及從事件存放區取得物件。</span><span class="sxs-lookup"><span data-stu-id="9ca55-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="9ca55-112">因為不再支援 [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher)和發行者物件，所以不會在 [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher)方法上呼叫 [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) 。</span><span class="sxs-lookup"><span data-stu-id="9ca55-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="9ca55-113">成員</span><span class="sxs-lookup"><span data-stu-id="9ca55-113">Members</span></span>

<span data-ttu-id="9ca55-114">**IEventSystem2** 介面繼承自 **IEventSystem**。</span><span class="sxs-lookup"><span data-stu-id="9ca55-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="9ca55-115">**IEventSystem2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9ca55-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="9ca55-116">方法</span><span class="sxs-lookup"><span data-stu-id="9ca55-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ca55-117">方法</span><span class="sxs-lookup"><span data-stu-id="9ca55-117">Methods</span></span>

<span data-ttu-id="9ca55-118">**IEventSystem2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9ca55-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="9ca55-119">方法</span><span class="sxs-lookup"><span data-stu-id="9ca55-119">Method</span></span>                                                                         | <span data-ttu-id="9ca55-120">描述</span><span class="sxs-lookup"><span data-stu-id="9ca55-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="9ca55-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="9ca55-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="9ca55-122">捕獲事件系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9ca55-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="9ca55-123">**VerifyTransientSubscribers**</span><span class="sxs-lookup"><span data-stu-id="9ca55-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="9ca55-124">確認資料存放區中的所有暫時性訂閱者是否存在。</span><span class="sxs-lookup"><span data-stu-id="9ca55-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ca55-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ca55-125">Requirements</span></span>



| <span data-ttu-id="9ca55-126">需求</span><span class="sxs-lookup"><span data-stu-id="9ca55-126">Requirement</span></span> | <span data-ttu-id="9ca55-127">值</span><span class="sxs-lookup"><span data-stu-id="9ca55-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9ca55-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ca55-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca55-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ca55-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9ca55-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ca55-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca55-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ca55-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9ca55-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ca55-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca55-133">**IEventSystem**</span><span class="sxs-lookup"><span data-stu-id="9ca55-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 


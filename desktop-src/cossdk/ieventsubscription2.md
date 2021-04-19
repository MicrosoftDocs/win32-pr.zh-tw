---
description: 儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 IEventSubscription 介面。
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: IEventSubscription2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973980"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="fbe6f-104">IEventSubscription2 介面</span><span class="sxs-lookup"><span data-stu-id="fbe6f-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="fbe6f-105">儲存和捕獲事件訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="fbe6f-106">這個介面會擴充 [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) 介面。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="fbe6f-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="fbe6f-107">When to implement</span></span>

<span data-ttu-id="fbe6f-108">您不需要執行 **IEventSubscription2** 介面。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="fbe6f-109">系統提供的事件物件類別 (CLSID \_ CEventSubscription) 實行 **IEventSubscription2**。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fbe6f-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="fbe6f-110">When to use</span></span>

<span data-ttu-id="fbe6f-111">[Com + 事件](com--events.md)系統會使用此介面來取得個別訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="fbe6f-112">成員</span><span class="sxs-lookup"><span data-stu-id="fbe6f-112">Members</span></span>

<span data-ttu-id="fbe6f-113">**IEventSubscription2** 介面繼承自 **IEventSubscription**。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="fbe6f-114">**IEventSubscription2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fbe6f-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="fbe6f-115">屬性</span><span class="sxs-lookup"><span data-stu-id="fbe6f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbe6f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="fbe6f-116">Properties</span></span>

<span data-ttu-id="fbe6f-117">**IEventSubscription2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="fbe6f-118">屬性</span><span class="sxs-lookup"><span data-stu-id="fbe6f-118">Property</span></span>                                                                      | <span data-ttu-id="fbe6f-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="fbe6f-119">Access type</span></span>           | <span data-ttu-id="fbe6f-120">Description</span><span class="sxs-lookup"><span data-stu-id="fbe6f-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="fbe6f-121">**>filtercriteria**</span><span class="sxs-lookup"><span data-stu-id="fbe6f-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="fbe6f-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fbe6f-122">Read/write</span></span><br/> | <span data-ttu-id="fbe6f-123">管理訂用帳戶的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="fbe6f-124">**SubscriberMoniker**</span><span class="sxs-lookup"><span data-stu-id="fbe6f-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="fbe6f-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fbe6f-125">Read/write</span></span><br/> | <span data-ttu-id="fbe6f-126">訂閱者的名字。</span><span class="sxs-lookup"><span data-stu-id="fbe6f-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="fbe6f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbe6f-127">Requirements</span></span>



| <span data-ttu-id="fbe6f-128">需求</span><span class="sxs-lookup"><span data-stu-id="fbe6f-128">Requirement</span></span> | <span data-ttu-id="fbe6f-129">值</span><span class="sxs-lookup"><span data-stu-id="fbe6f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fbe6f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbe6f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe6f-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbe6f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fbe6f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbe6f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe6f-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbe6f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fbe6f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbe6f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe6f-135">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="fbe6f-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 





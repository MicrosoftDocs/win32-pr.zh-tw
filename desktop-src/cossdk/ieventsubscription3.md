---
description: 儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 IEventSubscription2 介面。
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: IEventSubscription3 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973978"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="ab765-104">IEventSubscription3 介面</span><span class="sxs-lookup"><span data-stu-id="ab765-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="ab765-105">儲存和捕獲事件訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ab765-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="ab765-106">這個介面會擴充 [**IEventSubscription2**](ieventsubscription2.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="ab765-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ab765-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="ab765-107">When to implement</span></span>

<span data-ttu-id="ab765-108">您不需要執行 **IEventSubscription3** 介面。</span><span class="sxs-lookup"><span data-stu-id="ab765-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="ab765-109">系統提供的事件物件類別 (CLSID \_ CEventSubscription) 實行 **IEventSubscription3**。</span><span class="sxs-lookup"><span data-stu-id="ab765-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ab765-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="ab765-110">When to use</span></span>

<span data-ttu-id="ab765-111">[Com + 事件](com--events.md)系統會使用此介面來取得個別訂閱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ab765-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="ab765-112">成員</span><span class="sxs-lookup"><span data-stu-id="ab765-112">Members</span></span>

<span data-ttu-id="ab765-113">**IEventSubscription3** 介面繼承自 **IEventSubscription2**。</span><span class="sxs-lookup"><span data-stu-id="ab765-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="ab765-114">**IEventSubscription3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ab765-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="ab765-115">屬性</span><span class="sxs-lookup"><span data-stu-id="ab765-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab765-116">屬性</span><span class="sxs-lookup"><span data-stu-id="ab765-116">Properties</span></span>

<span data-ttu-id="ab765-117">**IEventSubscription3** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ab765-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="ab765-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ab765-118">Property</span></span>                                                                                  | <span data-ttu-id="ab765-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="ab765-119">Access type</span></span>           | <span data-ttu-id="ab765-120">Description</span><span class="sxs-lookup"><span data-stu-id="ab765-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="ab765-121">**EventClassApplicationID**</span><span class="sxs-lookup"><span data-stu-id="ab765-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="ab765-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ab765-122">Read/write</span></span><br/> | <span data-ttu-id="ab765-123">事件類別物件的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="ab765-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="ab765-124">**EventClassPartitionID**</span><span class="sxs-lookup"><span data-stu-id="ab765-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="ab765-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ab765-125">Read/write</span></span><br/> | <span data-ttu-id="ab765-126">事件類別物件的資料分割 GUID。</span><span class="sxs-lookup"><span data-stu-id="ab765-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="ab765-127">**SubscriberApplicationID**</span><span class="sxs-lookup"><span data-stu-id="ab765-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="ab765-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ab765-128">Read/write</span></span><br/> | <span data-ttu-id="ab765-129">訂閱者的應用程式 GUID。</span><span class="sxs-lookup"><span data-stu-id="ab765-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="ab765-130">**SubscriberPartitionID**</span><span class="sxs-lookup"><span data-stu-id="ab765-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="ab765-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ab765-131">Read/write</span></span><br/> | <span data-ttu-id="ab765-132">訂閱者的資料分割 GUID。</span><span class="sxs-lookup"><span data-stu-id="ab765-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ab765-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab765-133">Requirements</span></span>



| <span data-ttu-id="ab765-134">需求</span><span class="sxs-lookup"><span data-stu-id="ab765-134">Requirement</span></span> | <span data-ttu-id="ab765-135">值</span><span class="sxs-lookup"><span data-stu-id="ab765-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ab765-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab765-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ab765-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab765-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ab765-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab765-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ab765-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab765-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ab765-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab765-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab765-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="ab765-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 





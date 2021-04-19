---
description: 表示已卸載之事件的發生次數。 卸載的事件是未傳遞給事件取用者的事件。
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998524"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="626ed-104">\_\_EventDroppedEvent 類別</span><span class="sxs-lookup"><span data-stu-id="626ed-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="626ed-105">**\_ \_ EventDroppedEvent** 系統類別代表已卸載之事件的發生次數。</span><span class="sxs-lookup"><span data-stu-id="626ed-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="626ed-106">卸載的事件是未傳遞給事件取用者的事件。</span><span class="sxs-lookup"><span data-stu-id="626ed-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="626ed-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="626ed-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="626ed-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="626ed-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="626ed-109">語法</span><span class="sxs-lookup"><span data-stu-id="626ed-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="626ed-110">成員</span><span class="sxs-lookup"><span data-stu-id="626ed-110">Members</span></span>

<span data-ttu-id="626ed-111">**\_ \_ EventDroppedEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="626ed-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="626ed-112">屬性</span><span class="sxs-lookup"><span data-stu-id="626ed-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="626ed-113">屬性</span><span class="sxs-lookup"><span data-stu-id="626ed-113">Properties</span></span>

<span data-ttu-id="626ed-114">**\_ \_ EventDroppedEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="626ed-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="626ed-115">**事件**</span><span class="sxs-lookup"><span data-stu-id="626ed-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ed-116">資料類型： **\_ \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="626ed-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="626ed-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="626ed-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626ed-118">丟棄的事件。</span><span class="sxs-lookup"><span data-stu-id="626ed-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="626ed-119">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="626ed-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ed-120">資料類型： **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="626ed-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="626ed-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="626ed-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626ed-122">[**\_ \_ EventConsumer**](--eventconsumer.md)實例的參考，代表您識別用來接收事件的永久取用者。</span><span class="sxs-lookup"><span data-stu-id="626ed-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="626ed-123">訂閱事件的不同永久取用者可以繼續接收事件。</span><span class="sxs-lookup"><span data-stu-id="626ed-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="626ed-124">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="626ed-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ed-125">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="626ed-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="626ed-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="626ed-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626ed-127">事件提供者用來判斷可以接收事件之使用者的描述項。</span><span class="sxs-lookup"><span data-stu-id="626ed-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="626ed-128">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="626ed-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="626ed-129">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="626ed-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ed-130">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="626ed-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="626ed-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="626ed-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="626ed-132">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="626ed-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="626ed-133">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="626ed-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="626ed-134">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="626ed-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="626ed-135">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="626ed-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="626ed-136">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="626ed-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="626ed-137">備註</span><span class="sxs-lookup"><span data-stu-id="626ed-137">Remarks</span></span>

<span data-ttu-id="626ed-138">**\_ \_ EventDroppedEvent** 類別衍生自 [**\_ \_ SystemEvent**](--systemevent.md)。</span><span class="sxs-lookup"><span data-stu-id="626ed-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="626ed-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="626ed-139">Requirements</span></span>



| <span data-ttu-id="626ed-140">需求</span><span class="sxs-lookup"><span data-stu-id="626ed-140">Requirement</span></span> | <span data-ttu-id="626ed-141">值</span><span class="sxs-lookup"><span data-stu-id="626ed-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="626ed-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="626ed-142">Minimum supported client</span></span><br/> | <span data-ttu-id="626ed-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="626ed-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="626ed-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="626ed-144">Minimum supported server</span></span><br/> | <span data-ttu-id="626ed-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="626ed-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="626ed-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="626ed-146">Namespace</span></span><br/>                | <span data-ttu-id="626ed-147">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="626ed-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="626ed-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="626ed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626ed-149">**\_\_SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="626ed-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="626ed-150">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="626ed-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


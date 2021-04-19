---
description: 報告因為傳遞佇列溢位而捨棄事件。
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994504"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="2fcf0-103">\_\_EventQueueOverflowEvent 類別</span><span class="sxs-lookup"><span data-stu-id="2fcf0-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="2fcf0-104">**\_ \_ EventQueueOverflowEvent** 系統類別會報告因為傳遞佇列溢位而卸載事件的時機。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="2fcf0-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2fcf0-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcf0-107">語法</span><span class="sxs-lookup"><span data-stu-id="2fcf0-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2fcf0-108">成員</span><span class="sxs-lookup"><span data-stu-id="2fcf0-108">Members</span></span>

<span data-ttu-id="2fcf0-109">**\_ \_ EventQueueOverflowEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2fcf0-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2fcf0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2fcf0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fcf0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2fcf0-111">Properties</span></span>

<span data-ttu-id="2fcf0-112">**\_ \_ EventQueueOverflowEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fcf0-113">**CurrentQueueSize**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcf0-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcf0-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2fcf0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fcf0-116">目前的佇列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-116">Current queue size, in bytes.</span></span> <span data-ttu-id="2fcf0-117">所有結合的佇列，這個屬性的預設值為 10 MB。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="2fcf0-118">**事件**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcf0-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2fcf0-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2fcf0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fcf0-121">感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-121">Event of interest.</span></span> <span data-ttu-id="2fcf0-122">這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcf0-123">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcf0-124">資料類型： **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="2fcf0-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2fcf0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fcf0-126">預定取用者的參考。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-126">Reference to the intended consumer.</span></span> <span data-ttu-id="2fcf0-127">這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcf0-128">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcf0-129">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="2fcf0-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2fcf0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2fcf0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fcf0-131">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2fcf0-132">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fcf0-133">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcf0-134">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2fcf0-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2fcf0-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fcf0-136">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2fcf0-137">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2fcf0-138">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="2fcf0-139">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2fcf0-140">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fcf0-141">備註</span><span class="sxs-lookup"><span data-stu-id="2fcf0-141">Remarks</span></span>

<span data-ttu-id="2fcf0-142">只有具備系統管理員許可權的使用者能夠收到此事件。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="2fcf0-143">**\_ \_ EventQueueOverflowEvent** 類別衍生自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="2fcf0-144">如需詳細資訊，請參閱 [**\_ \_ EventConsumer**](--eventconsumer.md)類別中的 [**MaximumQueueSize**](--eventconsumer.md)屬性和 **Win32 \_ WMISetting** 類別中的 [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcf0-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fcf0-145">Requirements</span></span>



| <span data-ttu-id="2fcf0-146">需求</span><span class="sxs-lookup"><span data-stu-id="2fcf0-146">Requirement</span></span> | <span data-ttu-id="2fcf0-147">值</span><span class="sxs-lookup"><span data-stu-id="2fcf0-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2fcf0-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fcf0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcf0-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fcf0-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2fcf0-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fcf0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcf0-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fcf0-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2fcf0-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="2fcf0-152">Namespace</span></span><br/>                | <span data-ttu-id="2fcf0-153">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="2fcf0-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2fcf0-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fcf0-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcf0-155">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="2fcf0-156">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="2fcf0-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


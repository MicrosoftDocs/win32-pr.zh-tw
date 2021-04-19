---
description: 代表由於事件取用者失敗而卸載的某個其他事件的發生次數。
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: __ConsumerFailureEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982756"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="cf8bb-103">\_\_ConsumerFailureEvent 類別</span><span class="sxs-lookup"><span data-stu-id="cf8bb-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="cf8bb-104">**\_ \_ ConsumerFailureEvent** 系統類別代表因為事件取用者失敗而卸載的某個其他事件。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="cf8bb-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cf8bb-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8bb-107">語法</span><span class="sxs-lookup"><span data-stu-id="cf8bb-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="cf8bb-108">成員</span><span class="sxs-lookup"><span data-stu-id="cf8bb-108">Members</span></span>

<span data-ttu-id="cf8bb-109">**\_ \_ ConsumerFailureEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf8bb-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="cf8bb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="cf8bb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf8bb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cf8bb-111">Properties</span></span>

<span data-ttu-id="cf8bb-112">**\_ \_ ConsumerFailureEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf8bb-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-116">取用者傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-120">擴充的錯誤碼描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-121">**ErrorObject**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-122">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-124">發生錯誤的物件。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-125">**事件**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-126">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-128">發生錯誤的事件。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-128">Event in error.</span></span> <span data-ttu-id="cf8bb-129">這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-130">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-131">資料類型： **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-133">預定取用者的參考。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-133">Reference to the intended consumer.</span></span> <span data-ttu-id="cf8bb-134">這個屬性繼承自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-135">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-136">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="cf8bb-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-138">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="cf8bb-139">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf8bb-140">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8bb-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8bb-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8bb-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8bb-143">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="cf8bb-144">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="cf8bb-145">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="cf8bb-146">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="cf8bb-147">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8bb-148">備註</span><span class="sxs-lookup"><span data-stu-id="cf8bb-148">Remarks</span></span>

<span data-ttu-id="cf8bb-149">**\_ \_ ConsumerFailureEvent** 類別衍生自 [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8bb-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8bb-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf8bb-150">Requirements</span></span>



| <span data-ttu-id="cf8bb-151">需求</span><span class="sxs-lookup"><span data-stu-id="cf8bb-151">Requirement</span></span> | <span data-ttu-id="cf8bb-152">值</span><span class="sxs-lookup"><span data-stu-id="cf8bb-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cf8bb-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf8bb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8bb-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf8bb-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cf8bb-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf8bb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8bb-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf8bb-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cf8bb-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf8bb-157">Namespace</span></span><br/>                | <span data-ttu-id="cf8bb-158">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="cf8bb-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cf8bb-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf8bb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8bb-160">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="cf8bb-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="cf8bb-161">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="cf8bb-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


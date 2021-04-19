---
description: 表示類別修改事件，這是在命名空間中的類別變更時所產生的內建事件種類。
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977956"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="8414d-103">\_\_ClassModificationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="8414d-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="8414d-104">**\_ \_ ClassModificationEvent** 系統類別代表類別修改事件，這是在命名空間中的類別變更時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="8414d-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="8414d-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8414d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8414d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8414d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8414d-107">語法</span><span class="sxs-lookup"><span data-stu-id="8414d-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8414d-108">成員</span><span class="sxs-lookup"><span data-stu-id="8414d-108">Members</span></span>

<span data-ttu-id="8414d-109">**\_ \_ ClassModificationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8414d-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8414d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8414d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8414d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8414d-111">Properties</span></span>

<span data-ttu-id="8414d-112">**\_ \_ ClassModificationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8414d-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8414d-113">**PreviousClass**</span><span class="sxs-lookup"><span data-stu-id="8414d-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8414d-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="8414d-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8414d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8414d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8414d-116">類別原始版本的複本。</span><span class="sxs-lookup"><span data-stu-id="8414d-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="8414d-117">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="8414d-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8414d-118">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="8414d-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8414d-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8414d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8414d-120">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="8414d-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8414d-121">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="8414d-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="8414d-122">**>targetclass**</span><span class="sxs-lookup"><span data-stu-id="8414d-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8414d-123">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="8414d-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8414d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8414d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8414d-125">類別修改事件所報告之新修改類別的複本。</span><span class="sxs-lookup"><span data-stu-id="8414d-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="8414d-126">這個屬性繼承自 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="8414d-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8414d-127">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="8414d-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8414d-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8414d-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8414d-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8414d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8414d-130">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="8414d-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8414d-131">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="8414d-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8414d-132">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="8414d-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="8414d-133">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="8414d-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8414d-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="8414d-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8414d-135">備註</span><span class="sxs-lookup"><span data-stu-id="8414d-135">Remarks</span></span>

<span data-ttu-id="8414d-136">**\_ \_ ClassModificationEvent** 類別衍生自 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="8414d-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="8414d-137">此事件會報告類別定義的新舊版本。</span><span class="sxs-lookup"><span data-stu-id="8414d-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8414d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="8414d-138">Requirements</span></span>



| <span data-ttu-id="8414d-139">需求</span><span class="sxs-lookup"><span data-stu-id="8414d-139">Requirement</span></span> | <span data-ttu-id="8414d-140">值</span><span class="sxs-lookup"><span data-stu-id="8414d-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8414d-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8414d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8414d-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8414d-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8414d-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8414d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8414d-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8414d-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8414d-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="8414d-145">Namespace</span></span><br/>                | <span data-ttu-id="8414d-146">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="8414d-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8414d-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8414d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8414d-148">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="8414d-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="8414d-149">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="8414d-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


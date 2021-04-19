---
description: 是與類別相關之所有內建事件的基類。
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: __ClassOperationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981229"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="80fee-103">\_\_ClassOperationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="80fee-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="80fee-104">**\_ \_ ClassOperationEvent** 系統類別是所有與類別相關之內建事件的基類。</span><span class="sxs-lookup"><span data-stu-id="80fee-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="80fee-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="80fee-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="80fee-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="80fee-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fee-107">語法</span><span class="sxs-lookup"><span data-stu-id="80fee-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="80fee-108">成員</span><span class="sxs-lookup"><span data-stu-id="80fee-108">Members</span></span>

<span data-ttu-id="80fee-109">**\_ \_ ClassOperationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="80fee-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="80fee-110">屬性</span><span class="sxs-lookup"><span data-stu-id="80fee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80fee-111">屬性</span><span class="sxs-lookup"><span data-stu-id="80fee-111">Properties</span></span>

<span data-ttu-id="80fee-112">**\_ \_ ClassOperationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="80fee-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80fee-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="80fee-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fee-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="80fee-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="80fee-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80fee-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80fee-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="80fee-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="80fee-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="80fee-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fee-118">**>targetclass**</span><span class="sxs-lookup"><span data-stu-id="80fee-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fee-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="80fee-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="80fee-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80fee-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80fee-121">受事件影響的類別。</span><span class="sxs-lookup"><span data-stu-id="80fee-121">Class affected by the event.</span></span> <span data-ttu-id="80fee-122">針對建立事件，這是新建立的類別。</span><span class="sxs-lookup"><span data-stu-id="80fee-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="80fee-123">針對修改事件，這是已變更類別的新版本。</span><span class="sxs-lookup"><span data-stu-id="80fee-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="80fee-124">如果是刪除事件，這就是已刪除的類別。</span><span class="sxs-lookup"><span data-stu-id="80fee-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="80fee-125">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="80fee-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fee-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="80fee-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="80fee-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80fee-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80fee-128">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="80fee-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="80fee-129">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="80fee-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="80fee-130">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="80fee-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="80fee-131">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="80fee-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="80fee-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="80fee-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80fee-133">備註</span><span class="sxs-lookup"><span data-stu-id="80fee-133">Remarks</span></span>

<span data-ttu-id="80fee-134">**\_ \_ ClassOperationEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="80fee-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="80fee-135">不會建立 **\_ \_ ClassOperationEvent** 的實例，只會建立其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="80fee-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="80fee-136">下列類別衍生自 **\_ \_ ClassOperationEvent**：</span><span class="sxs-lookup"><span data-stu-id="80fee-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="80fee-137">**\_\_ClassCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="80fee-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="80fee-138">**\_\_ClassModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="80fee-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="80fee-139">**\_\_ClassDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="80fee-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="80fee-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="80fee-140">Requirements</span></span>



| <span data-ttu-id="80fee-141">需求</span><span class="sxs-lookup"><span data-stu-id="80fee-141">Requirement</span></span> | <span data-ttu-id="80fee-142">值</span><span class="sxs-lookup"><span data-stu-id="80fee-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="80fee-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80fee-143">Minimum supported client</span></span><br/> | <span data-ttu-id="80fee-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80fee-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="80fee-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80fee-145">Minimum supported server</span></span><br/> | <span data-ttu-id="80fee-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80fee-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="80fee-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="80fee-147">Namespace</span></span><br/>                | <span data-ttu-id="80fee-148">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="80fee-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="80fee-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80fee-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fee-150">**\_\_事件**</span><span class="sxs-lookup"><span data-stu-id="80fee-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="80fee-151">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="80fee-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="80fee-152">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="80fee-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 


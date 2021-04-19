---
description: 所有與命名空間相關之內建事件的基類。
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000321"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="657b4-103">\_\_NamespaceOperationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="657b4-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="657b4-104">**\_ \_ NamespaceOperationEvent** 系統類別是所有與命名空間相關之內建事件的基類。</span><span class="sxs-lookup"><span data-stu-id="657b4-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="657b4-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="657b4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="657b4-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="657b4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="657b4-107">語法</span><span class="sxs-lookup"><span data-stu-id="657b4-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="657b4-108">成員</span><span class="sxs-lookup"><span data-stu-id="657b4-108">Members</span></span>

<span data-ttu-id="657b4-109">**\_ \_ NamespaceOperationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="657b4-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="657b4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="657b4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="657b4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="657b4-111">Properties</span></span>

<span data-ttu-id="657b4-112">**\_ \_ NamespaceOperationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="657b4-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="657b4-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="657b4-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="657b4-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="657b4-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="657b4-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="657b4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="657b4-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="657b4-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="657b4-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="657b4-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="657b4-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="657b4-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="657b4-119">資料類型： **\_ \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="657b4-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="657b4-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="657b4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="657b4-121">受事件影響的命名空間。</span><span class="sxs-lookup"><span data-stu-id="657b4-121">Namespace affected by the event.</span></span> <span data-ttu-id="657b4-122">針對建立事件，這是新建立的命名空間。</span><span class="sxs-lookup"><span data-stu-id="657b4-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="657b4-123">針對修改事件，這是已變更的命名空間。</span><span class="sxs-lookup"><span data-stu-id="657b4-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="657b4-124">如果是刪除事件，這就是已刪除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="657b4-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="657b4-125">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="657b4-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="657b4-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="657b4-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="657b4-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="657b4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="657b4-128">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="657b4-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="657b4-129">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="657b4-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="657b4-130">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="657b4-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="657b4-131">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="657b4-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="657b4-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="657b4-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="657b4-133">備註</span><span class="sxs-lookup"><span data-stu-id="657b4-133">Remarks</span></span>

<span data-ttu-id="657b4-134">**\_ \_ NamespaceOperationEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="657b4-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="657b4-135">不會建立這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="657b4-135">Instances of this class are not created.</span></span> <span data-ttu-id="657b4-136">WMI 會建立下列其中一個衍生自這個類別的類別實例：</span><span class="sxs-lookup"><span data-stu-id="657b4-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="657b4-137">**\_\_NamespaceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="657b4-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="657b4-138">**\_\_NamespaceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="657b4-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="657b4-139">**\_\_NamespaceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="657b4-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="657b4-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="657b4-140">Requirements</span></span>



| <span data-ttu-id="657b4-141">需求</span><span class="sxs-lookup"><span data-stu-id="657b4-141">Requirement</span></span> | <span data-ttu-id="657b4-142">值</span><span class="sxs-lookup"><span data-stu-id="657b4-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="657b4-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="657b4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="657b4-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="657b4-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="657b4-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="657b4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="657b4-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="657b4-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="657b4-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="657b4-147">Namespace</span></span><br/>                | <span data-ttu-id="657b4-148">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="657b4-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="657b4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="657b4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657b4-150">**\_\_事件**</span><span class="sxs-lookup"><span data-stu-id="657b4-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="657b4-151">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="657b4-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="657b4-152">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="657b4-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 


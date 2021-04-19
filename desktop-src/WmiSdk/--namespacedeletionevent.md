---
description: 報告命名空間刪除事件，這是從目前命名空間移除子命名空間時所產生的內建事件種類。
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: __NamespaceDeletionEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994503"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="57053-103">\_\_NamespaceDeletionEvent 類別</span><span class="sxs-lookup"><span data-stu-id="57053-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="57053-104">**\_ \_ NamespaceDeletionEvent** 系統類別會報告命名空間刪除事件，這是從目前的命名空間移除子命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="57053-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="57053-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="57053-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="57053-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="57053-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57053-107">語法</span><span class="sxs-lookup"><span data-stu-id="57053-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="57053-108">成員</span><span class="sxs-lookup"><span data-stu-id="57053-108">Members</span></span>

<span data-ttu-id="57053-109">**\_ \_ NamespaceDeletionEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="57053-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="57053-110">屬性</span><span class="sxs-lookup"><span data-stu-id="57053-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57053-111">屬性</span><span class="sxs-lookup"><span data-stu-id="57053-111">Properties</span></span>

<span data-ttu-id="57053-112">**\_ \_ NamespaceDeletionEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="57053-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57053-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="57053-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57053-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="57053-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="57053-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="57053-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57053-116">事件提供者用來判斷可接收事件之使用者的描述項。</span><span class="sxs-lookup"><span data-stu-id="57053-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="57053-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="57053-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="57053-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="57053-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57053-119">資料類型： **\_ \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="57053-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="57053-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="57053-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57053-121">已刪除之 [**\_ \_ 命名空間**](--namespace.md)實例的複本。</span><span class="sxs-lookup"><span data-stu-id="57053-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="57053-122">**\_ \_ 命名空間** 實例的 **Name** 屬性會識別已刪除的命名空間。</span><span class="sxs-lookup"><span data-stu-id="57053-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="57053-123">這個屬性繼承自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="57053-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="57053-124">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="57053-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57053-125">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="57053-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57053-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="57053-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57053-127">指出事件產生時間的唯一值。</span><span class="sxs-lookup"><span data-stu-id="57053-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="57053-128">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="57053-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="57053-129">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="57053-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="57053-130">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="57053-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="57053-131">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="57053-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57053-132">備註</span><span class="sxs-lookup"><span data-stu-id="57053-132">Remarks</span></span>

<span data-ttu-id="57053-133">**\_ \_ NamespaceDeletionEvent** 類別衍生自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="57053-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57053-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="57053-134">Requirements</span></span>



| <span data-ttu-id="57053-135">需求</span><span class="sxs-lookup"><span data-stu-id="57053-135">Requirement</span></span> | <span data-ttu-id="57053-136">值</span><span class="sxs-lookup"><span data-stu-id="57053-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="57053-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57053-137">Minimum supported client</span></span><br/> | <span data-ttu-id="57053-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57053-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="57053-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57053-139">Minimum supported server</span></span><br/> | <span data-ttu-id="57053-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57053-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="57053-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="57053-141">Namespace</span></span><br/>                | <span data-ttu-id="57053-142">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="57053-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="57053-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57053-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57053-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="57053-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="57053-145">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="57053-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


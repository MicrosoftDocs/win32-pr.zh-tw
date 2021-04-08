---
description: 報告命名空間修改事件，這是在修改命名空間時所產生的內建事件種類。
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694936"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="b8b80-103">\_\_NamespaceModificationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="b8b80-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="b8b80-104">**\_ \_ NamespaceModificationEvent** 系統類別會報告命名空間修改事件，這是在修改命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="b8b80-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="b8b80-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8b80-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b8b80-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b8b80-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b80-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8b80-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b8b80-108">成員</span><span class="sxs-lookup"><span data-stu-id="b8b80-108">Members</span></span>

<span data-ttu-id="b8b80-109">**\_ \_ NamespaceModificationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8b80-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b8b80-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b8b80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8b80-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b8b80-111">Properties</span></span>

<span data-ttu-id="b8b80-112">**\_ \_ NamespaceModificationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8b80-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8b80-113">**PreviousNamespace**</span><span class="sxs-lookup"><span data-stu-id="b8b80-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b80-114">資料類型： **\_ \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="b8b80-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="b8b80-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b80-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b80-116">[**\_ \_ 命名空間**](--namespace.md)實例的原始版本複本。</span><span class="sxs-lookup"><span data-stu-id="b8b80-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="b8b80-117">這個實例的 **Name** 屬性會識別修改過的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b8b80-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="b8b80-118">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="b8b80-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b80-119">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8b80-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b8b80-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b80-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b80-121">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="b8b80-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b8b80-122">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b80-123">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="b8b80-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b80-124">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8b80-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b8b80-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b80-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b80-126">事件提供者用來判斷可接收事件之使用者的描述項。</span><span class="sxs-lookup"><span data-stu-id="b8b80-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="b8b80-127">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="b8b80-128">在 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)中 (ACL) 的 **Null** 存取控制清單會將無限存取權授與所有人。</span><span class="sxs-lookup"><span data-stu-id="b8b80-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="b8b80-129">如需詳細資訊，請參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="b8b80-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="b8b80-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b80-131">資料類型： **\_ \_ 命名空間**</span><span class="sxs-lookup"><span data-stu-id="b8b80-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="b8b80-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b80-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b80-133">已修改之 [**\_ \_ 命名空間**](--namespace.md)實例的複本。</span><span class="sxs-lookup"><span data-stu-id="b8b80-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="b8b80-134">**\_ \_ 命名空間** 實例的 **Name** 屬性，表示修改過的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b8b80-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="b8b80-135">這個屬性繼承自類別 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b80-136">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="b8b80-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b80-137">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b8b80-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8b80-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b80-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b80-139">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="b8b80-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="b8b80-140">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="b8b80-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b8b80-141">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="b8b80-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="b8b80-142">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b8b80-143">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8b80-144">備註</span><span class="sxs-lookup"><span data-stu-id="b8b80-144">Remarks</span></span>

<span data-ttu-id="b8b80-145">**\_ \_ NamespaceModificationEvent** 類別衍生自 [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b80-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="b8b80-146">目標命名空間和先前命名空間之間的唯一差異，在於 [**名稱**](--namespace.md)以外的限定詞和屬性。</span><span class="sxs-lookup"><span data-stu-id="b8b80-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="b8b80-147">請注意， **\_ \_ 命名空間** 實例的 [**Name**](--namespace.md)屬性無法變更，因為命名空間無法重新命名。</span><span class="sxs-lookup"><span data-stu-id="b8b80-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="b8b80-148">若要修改命名空間的名稱，必須刪除 **\_ \_ 命名空間** 實例，並使用新名稱重新建立。</span><span class="sxs-lookup"><span data-stu-id="b8b80-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="b8b80-149">因此，當 **名稱** 以外的限定詞和屬性發生變更時，就會產生命名空間修改事件。</span><span class="sxs-lookup"><span data-stu-id="b8b80-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="b8b80-150">命名空間中發生任何類型的變更時，不會產生命名空間修改事件。</span><span class="sxs-lookup"><span data-stu-id="b8b80-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="b8b80-151">只有在修改命名空間實例時，才會產生命名空間修改事件。</span><span class="sxs-lookup"><span data-stu-id="b8b80-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b80-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8b80-152">Requirements</span></span>



| <span data-ttu-id="b8b80-153">需求</span><span class="sxs-lookup"><span data-stu-id="b8b80-153">Requirement</span></span> | <span data-ttu-id="b8b80-154">值</span><span class="sxs-lookup"><span data-stu-id="b8b80-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b8b80-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8b80-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b80-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8b80-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b8b80-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8b80-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b80-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8b80-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b8b80-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8b80-159">Namespace</span></span><br/>                | <span data-ttu-id="b8b80-160">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="b8b80-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b8b80-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b80-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b80-162">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="b8b80-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="b8b80-163">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="b8b80-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


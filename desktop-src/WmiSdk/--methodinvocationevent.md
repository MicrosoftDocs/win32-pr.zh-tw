---
description: '\_ \_ MethodInvocationEvent 系統類別已定義，但未執行。'
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: __MethodInvocationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
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
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193880"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="c6586-103">\_\_MethodInvocationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="c6586-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="c6586-104">**\_ \_ MethodInvocationEvent** 系統類別已定義，但未執行。</span><span class="sxs-lookup"><span data-stu-id="c6586-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="c6586-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6586-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c6586-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c6586-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6586-107">語法</span><span class="sxs-lookup"><span data-stu-id="c6586-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c6586-108">成員</span><span class="sxs-lookup"><span data-stu-id="c6586-108">Members</span></span>

<span data-ttu-id="c6586-109">**\_ \_ MethodInvocationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c6586-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c6586-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c6586-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6586-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c6586-111">Properties</span></span>

<span data-ttu-id="c6586-112">**\_ \_ MethodInvocationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c6586-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6586-113">**方法**</span><span class="sxs-lookup"><span data-stu-id="c6586-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6586-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6586-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-116">為了觸發事件而叫用的方法。</span><span class="sxs-lookup"><span data-stu-id="c6586-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="c6586-117">**參數**</span><span class="sxs-lookup"><span data-stu-id="c6586-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-118">資料類型： **\_ \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c6586-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="c6586-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-120">參考表示方法呼叫之輸入和輸出參數的實例。</span><span class="sxs-lookup"><span data-stu-id="c6586-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="c6586-121">**PreCall**</span><span class="sxs-lookup"><span data-stu-id="c6586-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c6586-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6586-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-124">若 **為 TRUE**，則會在呼叫方法之前引發事件。</span><span class="sxs-lookup"><span data-stu-id="c6586-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="c6586-125">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="c6586-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-126">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="c6586-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c6586-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-128">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="c6586-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c6586-129">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="c6586-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="c6586-130">如需詳細資訊，請參閱 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。</span><span class="sxs-lookup"><span data-stu-id="c6586-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="c6586-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="c6586-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-132">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="c6586-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c6586-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-134">實例：叫用方法。</span><span class="sxs-lookup"><span data-stu-id="c6586-134">Instance the method is invoked on.</span></span> <span data-ttu-id="c6586-135">這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="c6586-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6586-136">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="c6586-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6586-137">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c6586-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6586-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6586-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6586-139">指出事件產生時間的唯一值。</span><span class="sxs-lookup"><span data-stu-id="c6586-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="c6586-140">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="c6586-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c6586-141">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="c6586-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="c6586-142">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="c6586-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c6586-143">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c6586-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6586-144">備註</span><span class="sxs-lookup"><span data-stu-id="c6586-144">Remarks</span></span>

<span data-ttu-id="c6586-145">**\_ \_ MethodInvocationEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="c6586-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6586-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6586-146">Requirements</span></span>



| <span data-ttu-id="c6586-147">需求</span><span class="sxs-lookup"><span data-stu-id="c6586-147">Requirement</span></span> | <span data-ttu-id="c6586-148">值</span><span class="sxs-lookup"><span data-stu-id="c6586-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c6586-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6586-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c6586-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6586-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c6586-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6586-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c6586-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6586-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c6586-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="c6586-153">Namespace</span></span><br/>                | <span data-ttu-id="c6586-154">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="c6586-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c6586-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6586-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6586-156">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="c6586-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="c6586-157">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="c6586-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


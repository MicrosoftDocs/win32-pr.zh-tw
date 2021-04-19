---
description: 表示作業與受管理元素之間的關聯，可能會受到其執行影響。
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001412"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="0c046-103">Msvm \_ AffectedJobElement 類別</span><span class="sxs-lookup"><span data-stu-id="0c046-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="0c046-104">表示作業與受管理元素之間的關聯，可能會受到其執行影響。</span><span class="sxs-lookup"><span data-stu-id="0c046-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="0c046-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c046-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c046-106">語法</span><span class="sxs-lookup"><span data-stu-id="0c046-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="0c046-107">成員</span><span class="sxs-lookup"><span data-stu-id="0c046-107">Members</span></span>

<span data-ttu-id="0c046-108">**Msvm \_ AffectedJobElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0c046-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0c046-109">屬性</span><span class="sxs-lookup"><span data-stu-id="0c046-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c046-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0c046-110">Properties</span></span>

<span data-ttu-id="0c046-111">**Msvm \_ AffectedJobElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0c046-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c046-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="0c046-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c046-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0c046-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0c046-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c046-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c046-115">受管理的元素受工作的執行影響。</span><span class="sxs-lookup"><span data-stu-id="0c046-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="0c046-116">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0c046-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="0c046-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c046-118">資料類型： **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="0c046-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0c046-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c046-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c046-120">影響受管理元素的作業。</span><span class="sxs-lookup"><span data-stu-id="0c046-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="0c046-121">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0c046-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="0c046-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c046-123">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c046-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c046-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c046-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c046-125">描述 managed 元素效果的列舉。</span><span class="sxs-lookup"><span data-stu-id="0c046-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="0c046-126">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0c046-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c046-127">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0c046-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c046-128">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0c046-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c046-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0c046-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c046-130">提供 **ElementEffects** 中對應陣列位置的效果詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0c046-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="0c046-131">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0c046-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c046-132">備註</span><span class="sxs-lookup"><span data-stu-id="0c046-132">Remarks</span></span>

<span data-ttu-id="0c046-133">存取 **Msvm \_ AffectedJobElement** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0c046-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0c046-134">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0c046-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c046-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c046-135">Requirements</span></span>



| <span data-ttu-id="0c046-136">需求</span><span class="sxs-lookup"><span data-stu-id="0c046-136">Requirement</span></span> | <span data-ttu-id="0c046-137">值</span><span class="sxs-lookup"><span data-stu-id="0c046-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c046-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c046-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0c046-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c046-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c046-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c046-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0c046-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c046-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c046-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c046-142">Namespace</span></span><br/>                | <span data-ttu-id="0c046-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c046-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c046-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0c046-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c046-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0c046-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c046-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0c046-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c046-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c046-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c046-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c046-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c046-149">**CIM \_ AffectedJobElement**</span><span class="sxs-lookup"><span data-stu-id="0c046-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="0c046-150">[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c046-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c046-151">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="0c046-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


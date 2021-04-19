---
description: 表示作業與受管理元素之間的關聯，這些專案可能會受其執行影響。
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Msvm_AffectedStorageJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970948"
---
# <a name="msvm_affectedstoragejobelement-class"></a><span data-ttu-id="45610-103">Msvm \_ AffectedStorageJobElement 類別</span><span class="sxs-lookup"><span data-stu-id="45610-103">Msvm\_AffectedStorageJobElement class</span></span>

<span data-ttu-id="45610-104">表示作業與受管理元素之間的關聯，這些專案可能會受其執行影響。</span><span class="sxs-lookup"><span data-stu-id="45610-104">Represents the association between a job and the managed elements that may be affected by its execution.</span></span>

<span data-ttu-id="45610-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="45610-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45610-106">語法</span><span class="sxs-lookup"><span data-stu-id="45610-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="45610-107">成員</span><span class="sxs-lookup"><span data-stu-id="45610-107">Members</span></span>

<span data-ttu-id="45610-108">**Msvm \_ AffectedStorageJobElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="45610-108">The **Msvm\_AffectedStorageJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="45610-109">屬性</span><span class="sxs-lookup"><span data-stu-id="45610-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45610-110">屬性</span><span class="sxs-lookup"><span data-stu-id="45610-110">Properties</span></span>

<span data-ttu-id="45610-111">**Msvm \_ AffectedStorageJobElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="45610-111">The **Msvm\_AffectedStorageJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45610-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="45610-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45610-113">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="45610-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="45610-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45610-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45610-115">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="45610-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="45610-116">受管理的元素受工作的執行影響。</span><span class="sxs-lookup"><span data-stu-id="45610-116">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="45610-117">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="45610-117">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45610-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="45610-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45610-119">資料類型： **[ **Msvm \_ get-storagejob**](msvm-storagejob.md)**</span><span class="sxs-lookup"><span data-stu-id="45610-119">Data type: **[**Msvm\_StorageJob**](msvm-storagejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="45610-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45610-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45610-121">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**OVERRIDE**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ AffectedJobElement. AffectingElement" ) </span><span class="sxs-lookup"><span data-stu-id="45610-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_AffectedJobElement.AffectingElement")</span></span>
</dt> </dl>

<span data-ttu-id="45610-122">影響受影響元素的作業。</span><span class="sxs-lookup"><span data-stu-id="45610-122">The job that is affecting the affected element.</span></span> <span data-ttu-id="45610-123">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="45610-123">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45610-124">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="45610-124">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45610-125">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="45610-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45610-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45610-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45610-127">描述 managed 元素效果的列舉。</span><span class="sxs-lookup"><span data-stu-id="45610-127">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="45610-128">這個陣列對應于 **OtherElementEffectsDescriptions** 屬性陣列，後者會提供與這個屬性所列舉之高階效果相關的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="45610-128">This array corresponds to the **OtherElementEffectsDescriptions** property array, where the latter provides details related to the high-level effects enumerated by this property.</span></span> <span data-ttu-id="45610-129">如果 **ElementEffects** 屬性陣列包含值1， (其他) ，則需要額外的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="45610-129">Additional detail is required if the **ElementEffects** property array contains the value 1, (Other).</span></span> <span data-ttu-id="45610-130">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="45610-130">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="45610-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="45610-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45610-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="45610-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45610-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**專屬用途** (2) </span><span class="sxs-lookup"><span data-stu-id="45610-133"><span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Exclusive Use** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45610-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**效能影響** (3) </span><span class="sxs-lookup"><span data-stu-id="45610-134"><span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Performance Impact** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45610-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**元素完整性** (4 ) </span><span class="sxs-lookup"><span data-stu-id="45610-135"><span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Element Integrity** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45610-136">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45610-136">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45610-137">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="45610-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45610-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="45610-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45610-139">在 **ElementEffects** 屬性陣列中的對應陣列位置提供效果的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="45610-139">Provides details for the effect at the corresponding array position in the **ElementEffects** property array.</span></span> <span data-ttu-id="45610-140">只要 **ElementEffects** 屬性陣列中的對應元素包含值 1 (其他) ，就需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="45610-140">This information is required whenever the corresponding element in the **ElementEffects** property array contains the value 1 (Other).</span></span> <span data-ttu-id="45610-141">這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="45610-141">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45610-142">備註</span><span class="sxs-lookup"><span data-stu-id="45610-142">Remarks</span></span>

<span data-ttu-id="45610-143">存取 **Msvm \_ AffectedStorageJobElement** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="45610-143">Access to the **Msvm\_AffectedStorageJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="45610-144">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="45610-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="45610-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="45610-145">Requirements</span></span>



| <span data-ttu-id="45610-146">需求</span><span class="sxs-lookup"><span data-stu-id="45610-146">Requirement</span></span> | <span data-ttu-id="45610-147">值</span><span class="sxs-lookup"><span data-stu-id="45610-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45610-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45610-148">Minimum supported client</span></span><br/> | <span data-ttu-id="45610-149">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45610-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45610-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45610-150">Minimum supported server</span></span><br/> | <span data-ttu-id="45610-151">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45610-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45610-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="45610-152">Namespace</span></span><br/>                | <span data-ttu-id="45610-153">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="45610-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45610-154">MOF</span><span class="sxs-lookup"><span data-stu-id="45610-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45610-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="45610-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45610-156">DLL</span><span class="sxs-lookup"><span data-stu-id="45610-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45610-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45610-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45610-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45610-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45610-159">**CIM \_ AffectedJobElement**</span><span class="sxs-lookup"><span data-stu-id="45610-159">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="45610-160">[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="45610-160">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="45610-161">儲存類別</span><span class="sxs-lookup"><span data-stu-id="45610-161">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


---
description: 表示作業與 CIM ManagedElement 物件之間的關聯 \_ ，這些物件可能會受到其執行影響。
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: CIM_AffectedJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115100"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="c5714-103">CIM \_ AffectedJobElement 類別</span><span class="sxs-lookup"><span data-stu-id="c5714-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="c5714-104">表示作業與 **CIM \_ ManagedElement** 物件之間的關聯，這些物件可能會受到其執行影響。</span><span class="sxs-lookup"><span data-stu-id="c5714-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="c5714-105">作業可能無法描述所有受影響的元素。</span><span class="sxs-lookup"><span data-stu-id="c5714-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="c5714-106">此關聯的主要用途是在作業需要獨佔使用受影響的 managed 專案時提供資訊，或描述可能產生的副作用。</span><span class="sxs-lookup"><span data-stu-id="c5714-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5714-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5714-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="c5714-108">成員</span><span class="sxs-lookup"><span data-stu-id="c5714-108">Members</span></span>

<span data-ttu-id="c5714-109">**CIM \_ AffectedJobElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c5714-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="c5714-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c5714-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5714-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c5714-111">Properties</span></span>

<span data-ttu-id="c5714-112">**CIM \_ AffectedJobElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c5714-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5714-113">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="c5714-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5714-114">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="c5714-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="c5714-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5714-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5714-116">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5714-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5714-117">受管理的元素受工作的執行影響。</span><span class="sxs-lookup"><span data-stu-id="c5714-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="c5714-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="c5714-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5714-119">資料類型： **CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="c5714-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="c5714-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5714-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5714-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c5714-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c5714-122">影響受管理元素的作業。</span><span class="sxs-lookup"><span data-stu-id="c5714-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="c5714-123">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="c5714-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5714-124">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c5714-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5714-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5714-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5714-126">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AffectedJobElement**。**OtherElementEffectsDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="c5714-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c5714-127">作業對 managed 元素的影響。</span><span class="sxs-lookup"><span data-stu-id="c5714-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5714-128">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c5714-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c5714-129">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c5714-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="c5714-130">**專屬用途** (2) </span><span class="sxs-lookup"><span data-stu-id="c5714-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="c5714-131">**效能影響** (3) </span><span class="sxs-lookup"><span data-stu-id="c5714-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="c5714-132">**元素完整性** (4) </span><span class="sxs-lookup"><span data-stu-id="c5714-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="c5714-133">**建立** (5) </span><span class="sxs-lookup"><span data-stu-id="c5714-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5714-134">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c5714-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5714-135">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c5714-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c5714-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c5714-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5714-137">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AffectedJobElement**。**ElementEffects**") </span><span class="sxs-lookup"><span data-stu-id="c5714-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="c5714-138">對應 "1" (**ElementEffects** 陣列中其他) 值的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c5714-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5714-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5714-139">Requirements</span></span>



| <span data-ttu-id="c5714-140">需求</span><span class="sxs-lookup"><span data-stu-id="c5714-140">Requirement</span></span> | <span data-ttu-id="c5714-141">值</span><span class="sxs-lookup"><span data-stu-id="c5714-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5714-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5714-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c5714-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5714-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c5714-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5714-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c5714-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5714-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c5714-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5714-146">Namespace</span></span><br/>                | <span data-ttu-id="c5714-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5714-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5714-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c5714-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5714-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c5714-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5714-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c5714-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5714-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5714-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


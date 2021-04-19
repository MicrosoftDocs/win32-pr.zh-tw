---
description: 代表服務與受管理元素之間的關聯，可能會受到其執行影響。
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991755"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="d608e-103">CIM \_ ServiceAffectsElement 類別</span><span class="sxs-lookup"><span data-stu-id="d608e-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="d608e-104">代表服務與受管理元素之間的關聯，可能會受到其執行影響。</span><span class="sxs-lookup"><span data-stu-id="d608e-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="d608e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d608e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="d608e-106">成員</span><span class="sxs-lookup"><span data-stu-id="d608e-106">Members</span></span>

<span data-ttu-id="d608e-107">**CIM \_ ServiceAffectsElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d608e-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="d608e-108">屬性</span><span class="sxs-lookup"><span data-stu-id="d608e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d608e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d608e-109">Properties</span></span>

<span data-ttu-id="d608e-110">**CIM \_ ServiceAffectsElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d608e-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d608e-111">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="d608e-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d608e-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d608e-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d608e-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d608e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d608e-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d608e-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d608e-115">受服務影響的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="d608e-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="d608e-116">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="d608e-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d608e-117">資料類型： **CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="d608e-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d608e-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d608e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d608e-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d608e-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d608e-120">影響受管理元素的服務。</span><span class="sxs-lookup"><span data-stu-id="d608e-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="d608e-121">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="d608e-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d608e-122">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d608e-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d608e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d608e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d608e-124">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ServiceAffectsElement**。**OtherElementEffectsDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="d608e-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="d608e-125">Managed 元素的效果。</span><span class="sxs-lookup"><span data-stu-id="d608e-125">The effect on the managed element.</span></span> <span data-ttu-id="d608e-126">這個陣列對應于 **OtherElementEffectsDescriptions** 陣列。</span><span class="sxs-lookup"><span data-stu-id="d608e-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="d608e-127">\- 獨佔使用 (2) ：沒有其他服務可能會與元素有此關聯。</span><span class="sxs-lookup"><span data-stu-id="d608e-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="d608e-128">\- 效能影響 (3) ：已淘汰以使用「取用」、「增強效能」或「降低效能」。</span><span class="sxs-lookup"><span data-stu-id="d608e-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="d608e-129">執行服務可能會增強或降低元素的效能。</span><span class="sxs-lookup"><span data-stu-id="d608e-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="d608e-130">這可能是執行的副作用，也可能是服務所提供之方法的預期結果。</span><span class="sxs-lookup"><span data-stu-id="d608e-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="d608e-131">\- 專案完整性 (4) ：已淘汰以使用「取用」、「增強完整性」或「降低完整性」。</span><span class="sxs-lookup"><span data-stu-id="d608e-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="d608e-132">執行服務可能會增強或降低元素的完整性。</span><span class="sxs-lookup"><span data-stu-id="d608e-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="d608e-133">這可能是執行的副作用，也可能是服務所提供之方法的預期結果。</span><span class="sxs-lookup"><span data-stu-id="d608e-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="d608e-134">\- 管理 (5) ：服務會管理元素。</span><span class="sxs-lookup"><span data-stu-id="d608e-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="d608e-135">\- 取用 (6) ：服務執行會取用部分或所有相關聯的專案，作為執行服務的結果。</span><span class="sxs-lookup"><span data-stu-id="d608e-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="d608e-136">例如，服務可能會耗用 CPU 迴圈，這可能會影響效能，或可能影響效能和完整性的儲存體。</span><span class="sxs-lookup"><span data-stu-id="d608e-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="d608e-137"> (比方說，缺乏可用的儲存體可能會降低儲存狀態的能力，而降低完整性。</span><span class="sxs-lookup"><span data-stu-id="d608e-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="d608e-138">「取用」 ) 可單獨使用或與其他值搭配使用，尤其是「降低效能」和「降級完整性」。</span><span class="sxs-lookup"><span data-stu-id="d608e-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="d608e-139">「管理」但不應該使用「取用」來反映服務可能提供的佈建服務。</span><span class="sxs-lookup"><span data-stu-id="d608e-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="d608e-140">\- 增強完整性 (7) ：此服務可能會增強相關元素的完整性。</span><span class="sxs-lookup"><span data-stu-id="d608e-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="d608e-141">\- 降低 (8) 的完整性：服務可能會降低相關元素的完整性。</span><span class="sxs-lookup"><span data-stu-id="d608e-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="d608e-142">\- 增強效能 (9) ：此服務可能會增強相關元素的效能。</span><span class="sxs-lookup"><span data-stu-id="d608e-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="d608e-143">\- 降低效能 (10) ：服務可能會降低相關元素的效能。</span><span class="sxs-lookup"><span data-stu-id="d608e-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d608e-144">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d608e-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d608e-145">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d608e-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="d608e-146">**專屬用途** (2) </span><span class="sxs-lookup"><span data-stu-id="d608e-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="d608e-147">**效能影響** (3) </span><span class="sxs-lookup"><span data-stu-id="d608e-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="d608e-148">**元素完整性** (4) </span><span class="sxs-lookup"><span data-stu-id="d608e-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="d608e-149">**管理** (5) </span><span class="sxs-lookup"><span data-stu-id="d608e-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="d608e-150">**耗用** (6) </span><span class="sxs-lookup"><span data-stu-id="d608e-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="d608e-151">**增強完整性** (7) </span><span class="sxs-lookup"><span data-stu-id="d608e-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="d608e-152">**降低完整性** (8) </span><span class="sxs-lookup"><span data-stu-id="d608e-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="d608e-153"> (9) **增強效能**</span><span class="sxs-lookup"><span data-stu-id="d608e-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="d608e-154">**降低效能** (10) </span><span class="sxs-lookup"><span data-stu-id="d608e-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d608e-155">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d608e-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d608e-156">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="d608e-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d608e-157">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d608e-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d608e-158">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d608e-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d608e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d608e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d608e-160">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ServiceAffectsElement**。**ElementEffects**") </span><span class="sxs-lookup"><span data-stu-id="d608e-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="d608e-161">陣列中的每個專案都會針對 **ElementEffects** 陣列中的對應專案提供額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="d608e-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="d608e-162">**ElementEffects** 陣列中設定為 **其他** ( "1" ) 的任何專案都需要描述。</span><span class="sxs-lookup"><span data-stu-id="d608e-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d608e-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="d608e-163">Requirements</span></span>



| <span data-ttu-id="d608e-164">需求</span><span class="sxs-lookup"><span data-stu-id="d608e-164">Requirement</span></span> | <span data-ttu-id="d608e-165">值</span><span class="sxs-lookup"><span data-stu-id="d608e-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d608e-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d608e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="d608e-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d608e-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d608e-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d608e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="d608e-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d608e-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d608e-170">命名空間</span><span class="sxs-lookup"><span data-stu-id="d608e-170">Namespace</span></span><br/>                | <span data-ttu-id="d608e-171">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d608e-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d608e-172">MOF</span><span class="sxs-lookup"><span data-stu-id="d608e-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d608e-173"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d608e-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d608e-174">DLL</span><span class="sxs-lookup"><span data-stu-id="d608e-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d608e-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d608e-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


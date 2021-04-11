---
description: 將電源供應器與監視其輸入電壓的電壓感應器產生關聯。
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyVoltageSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111089"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="e640d-103">CIM \_ AssociatedSupplyVoltageSensor 類別</span><span class="sxs-lookup"><span data-stu-id="e640d-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="e640d-104">**CIM \_ AssociatedSupplyVoltageSensor** 類別會將電源供應器與監視其輸入電壓的電壓感應器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e640d-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e640d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e640d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e640d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e640d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e640d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e640d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e640d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e640d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e640d-109">語法</span><span class="sxs-lookup"><span data-stu-id="e640d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="e640d-110">成員</span><span class="sxs-lookup"><span data-stu-id="e640d-110">Members</span></span>

<span data-ttu-id="e640d-111">**CIM \_ AssociatedSupplyVoltageSensor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e640d-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="e640d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e640d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e640d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e640d-113">Properties</span></span>

<span data-ttu-id="e640d-114">**CIM \_ AssociatedSupplyVoltageSensor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e640d-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e640d-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="e640d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e640d-116">資料類型： **CIM \_ 電壓感應器**</span><span class="sxs-lookup"><span data-stu-id="e640d-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="e640d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e640d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e640d-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="e640d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e640d-119">描述電壓感應器的 [**CIM \_ 電壓感應器**](cim-voltagesensor.md) 。</span><span class="sxs-lookup"><span data-stu-id="e640d-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e640d-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="e640d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e640d-121">資料類型： **CIM \_ 電源電源**</span><span class="sxs-lookup"><span data-stu-id="e640d-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="e640d-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e640d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e640d-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="e640d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e640d-124">[**CIM 電源 \_ 供應器**](cim-powersupply.md)，描述與電壓感應器相關聯的電源供應器。</span><span class="sxs-lookup"><span data-stu-id="e640d-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e640d-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="e640d-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e640d-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e640d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e640d-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e640d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e640d-128">指出由相關聯感應器測量的電源供應器輸入電壓範圍。</span><span class="sxs-lookup"><span data-stu-id="e640d-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e640d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e640d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e640d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e640d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="e640d-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**範圍 1** (2) </span><span class="sxs-lookup"><span data-stu-id="e640d-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="e640d-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**範圍 2** (3) </span><span class="sxs-lookup"><span data-stu-id="e640d-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="e640d-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**範圍1和 2** (4) </span><span class="sxs-lookup"><span data-stu-id="e640d-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e640d-134">範圍1和2</span><span class="sxs-lookup"><span data-stu-id="e640d-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e640d-135">備註</span><span class="sxs-lookup"><span data-stu-id="e640d-135">Remarks</span></span>

<span data-ttu-id="e640d-136">**Cim \_ AssociatedSupplyVoltageSensor** 類別衍生自 [**cim \_ AssociatedSensor**](cim-associatedsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="e640d-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="e640d-137">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e640d-137">WMI does not implement this class.</span></span>

<span data-ttu-id="e640d-138">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e640d-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e640d-139">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e640d-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e640d-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="e640d-140">Requirements</span></span>



| <span data-ttu-id="e640d-141">需求</span><span class="sxs-lookup"><span data-stu-id="e640d-141">Requirement</span></span> | <span data-ttu-id="e640d-142">值</span><span class="sxs-lookup"><span data-stu-id="e640d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e640d-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e640d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e640d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e640d-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e640d-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e640d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e640d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e640d-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e640d-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="e640d-147">Namespace</span></span><br/>                | <span data-ttu-id="e640d-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e640d-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e640d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e640d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e640d-150"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e640d-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e640d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e640d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e640d-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e640d-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e640d-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e640d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e640d-154">**CIM \_ AssociatedSensor**</span><span class="sxs-lookup"><span data-stu-id="e640d-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 


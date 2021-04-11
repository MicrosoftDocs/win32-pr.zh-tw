---
description: CIM \_ AssociatedSupplyCurrentSensor 類別會將電源供應器與目前的 (amperage) 感應器建立關聯，以監視其輸入頻率。
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyCurrentSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190975"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a><span data-ttu-id="8488b-103">CIM \_ AssociatedSupplyCurrentSensor 類別</span><span class="sxs-lookup"><span data-stu-id="8488b-103">CIM\_AssociatedSupplyCurrentSensor class</span></span>

<span data-ttu-id="8488b-104">**CIM \_ AssociatedSupplyCurrentSensor** 類別會將電源供應器與目前的 (amperage) 感應器建立關聯，以監視其輸入頻率。</span><span class="sxs-lookup"><span data-stu-id="8488b-104">The **CIM\_AssociatedSupplyCurrentSensor** class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8488b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8488b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8488b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8488b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8488b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8488b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8488b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8488b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8488b-109">語法</span><span class="sxs-lookup"><span data-stu-id="8488b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="8488b-110">成員</span><span class="sxs-lookup"><span data-stu-id="8488b-110">Members</span></span>

<span data-ttu-id="8488b-111">**CIM \_ AssociatedSupplyCurrentSensor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8488b-111">The **CIM\_AssociatedSupplyCurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="8488b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8488b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8488b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8488b-113">Properties</span></span>

<span data-ttu-id="8488b-114">**CIM \_ AssociatedSupplyCurrentSensor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8488b-114">The **CIM\_AssociatedSupplyCurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8488b-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="8488b-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8488b-116">資料類型： **CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="8488b-116">Data type: **CIM\_CurrentSensor**</span></span>
</dt> <dt>

<span data-ttu-id="8488b-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8488b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8488b-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="8488b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8488b-119">描述目前感應器的 [**CIM \_ CurrentSensor**](cim-currentsensor.md) 。</span><span class="sxs-lookup"><span data-stu-id="8488b-119">A [**CIM\_CurrentSensor**](cim-currentsensor.md) that describes the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="8488b-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="8488b-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8488b-121">資料類型： **CIM \_ 電源電源**</span><span class="sxs-lookup"><span data-stu-id="8488b-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="8488b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8488b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8488b-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="8488b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8488b-124">[**CIM 電源 \_ 供應器**](cim-powersupply.md)，描述與目前感應器相關聯的電源供應器。</span><span class="sxs-lookup"><span data-stu-id="8488b-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="8488b-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="8488b-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8488b-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8488b-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8488b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8488b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8488b-128">指出由相關聯感應器測量的電源供應器輸入頻率範圍。</span><span class="sxs-lookup"><span data-stu-id="8488b-128">Indicates the power supply input frequency range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8488b-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8488b-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8488b-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8488b-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="8488b-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**範圍 1** (2) </span><span class="sxs-lookup"><span data-stu-id="8488b-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="8488b-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**範圍 2** (3) </span><span class="sxs-lookup"><span data-stu-id="8488b-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="8488b-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**範圍1和 2** (4) </span><span class="sxs-lookup"><span data-stu-id="8488b-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8488b-134">範圍1和2</span><span class="sxs-lookup"><span data-stu-id="8488b-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8488b-135">備註</span><span class="sxs-lookup"><span data-stu-id="8488b-135">Remarks</span></span>

<span data-ttu-id="8488b-136">**Cim \_ AssociatedSupplyCurrentSensor** 類別衍生自 [**cim \_ AssociatedSensor**](cim-associatedsensor.md)。</span><span class="sxs-lookup"><span data-stu-id="8488b-136">The **CIM\_AssociatedSupplyCurrentSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="8488b-137">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="8488b-137">WMI does not implement this class.</span></span>

<span data-ttu-id="8488b-138">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8488b-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8488b-139">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8488b-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8488b-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="8488b-140">Requirements</span></span>



| <span data-ttu-id="8488b-141">需求</span><span class="sxs-lookup"><span data-stu-id="8488b-141">Requirement</span></span> | <span data-ttu-id="8488b-142">值</span><span class="sxs-lookup"><span data-stu-id="8488b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8488b-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8488b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8488b-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8488b-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8488b-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8488b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8488b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8488b-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8488b-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="8488b-147">Namespace</span></span><br/>                | <span data-ttu-id="8488b-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8488b-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8488b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8488b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8488b-150"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8488b-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8488b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8488b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8488b-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8488b-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8488b-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8488b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8488b-154">**CIM \_ AssociatedSensor**</span><span class="sxs-lookup"><span data-stu-id="8488b-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 


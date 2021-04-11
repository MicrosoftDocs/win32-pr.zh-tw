---
description: CIM \_ PackageTempSensor 關聯表示通常會在套件中安裝溫度感應器的關聯性，例如底座或機架，以監視封裝的環境。
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: CIM_PackageTempSensor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110817"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="3305f-103">CIM \_ PackageTempSensor 類別</span><span class="sxs-lookup"><span data-stu-id="3305f-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="3305f-104">**CIM \_ PackageTempSensor** 關聯表示通常會在套件中安裝溫度感應器的關聯性，例如底座或機架，以監視封裝的環境。</span><span class="sxs-lookup"><span data-stu-id="3305f-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3305f-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3305f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3305f-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3305f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3305f-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3305f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3305f-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3305f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3305f-109">語法</span><span class="sxs-lookup"><span data-stu-id="3305f-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3305f-110">成員</span><span class="sxs-lookup"><span data-stu-id="3305f-110">Members</span></span>

<span data-ttu-id="3305f-111">**CIM \_ PackageTempSensor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3305f-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="3305f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3305f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3305f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3305f-113">Properties</span></span>

<span data-ttu-id="3305f-114">**CIM \_ PackageTempSensor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3305f-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3305f-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="3305f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3305f-116">資料類型： **CIM \_ 溫度感應器**</span><span class="sxs-lookup"><span data-stu-id="3305f-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="3305f-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3305f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3305f-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="3305f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3305f-119">[**CIM \_ 溫度感應器**](cim-temperaturesensor.md)，描述套件的溫度感應器。</span><span class="sxs-lookup"><span data-stu-id="3305f-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="3305f-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="3305f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3305f-121">資料類型： **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="3305f-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="3305f-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3305f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3305f-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="3305f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3305f-124">[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述其環境受監視的實體套件。</span><span class="sxs-lookup"><span data-stu-id="3305f-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3305f-125">備註</span><span class="sxs-lookup"><span data-stu-id="3305f-125">Remarks</span></span>

<span data-ttu-id="3305f-126">**CIM \_PackageTempSensor** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="3305f-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3305f-127">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3305f-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3305f-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3305f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3305f-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3305f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3305f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3305f-130">Requirements</span></span>



| <span data-ttu-id="3305f-131">需求</span><span class="sxs-lookup"><span data-stu-id="3305f-131">Requirement</span></span> | <span data-ttu-id="3305f-132">值</span><span class="sxs-lookup"><span data-stu-id="3305f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3305f-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3305f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3305f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3305f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3305f-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3305f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3305f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3305f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3305f-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="3305f-137">Namespace</span></span><br/>                | <span data-ttu-id="3305f-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3305f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3305f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3305f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3305f-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3305f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3305f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3305f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3305f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3305f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3305f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3305f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3305f-144">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="3305f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


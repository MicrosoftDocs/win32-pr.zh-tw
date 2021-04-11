---
description: 表示 CIM \_ BaseMetricDefinition 物件用來定義 managed 專案計量的關聯。
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: CIM_MetricDefForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850303"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="16cee-103">CIM \_ MetricDefForME 類別</span><span class="sxs-lookup"><span data-stu-id="16cee-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="16cee-104">表示 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 物件用來定義 managed 專案計量的關聯。</span><span class="sxs-lookup"><span data-stu-id="16cee-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cee-105">語法</span><span class="sxs-lookup"><span data-stu-id="16cee-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="16cee-106">成員</span><span class="sxs-lookup"><span data-stu-id="16cee-106">Members</span></span>

<span data-ttu-id="16cee-107">**CIM \_ MetricDefForME** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16cee-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="16cee-108">屬性</span><span class="sxs-lookup"><span data-stu-id="16cee-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16cee-109">屬性</span><span class="sxs-lookup"><span data-stu-id="16cee-109">Properties</span></span>

<span data-ttu-id="16cee-110">**CIM \_ MetricDefForME** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16cee-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16cee-111">**先行**</span><span class="sxs-lookup"><span data-stu-id="16cee-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16cee-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16cee-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="16cee-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16cee-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16cee-114">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="16cee-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="16cee-115">與度量定義相關聯的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="16cee-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="16cee-116">**依賴**</span><span class="sxs-lookup"><span data-stu-id="16cee-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16cee-117">資料類型： **CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="16cee-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="16cee-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16cee-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16cee-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="16cee-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="16cee-120">與 managed 元素相關聯的度量定義。</span><span class="sxs-lookup"><span data-stu-id="16cee-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="16cee-121">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="16cee-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16cee-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="16cee-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16cee-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16cee-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16cee-124">指出是否要針對 managed 元素收集度量。</span><span class="sxs-lookup"><span data-stu-id="16cee-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="16cee-125">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="16cee-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16cee-126">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="16cee-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="16cee-127">**保留** (4) </span><span class="sxs-lookup"><span data-stu-id="16cee-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="16cee-128">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="16cee-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="16cee-129">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="16cee-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="16cee-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="16cee-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="16cee-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="16cee-131">Requirements</span></span>



| <span data-ttu-id="16cee-132">需求</span><span class="sxs-lookup"><span data-stu-id="16cee-132">Requirement</span></span> | <span data-ttu-id="16cee-133">值</span><span class="sxs-lookup"><span data-stu-id="16cee-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16cee-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16cee-134">Minimum supported client</span></span><br/> | <span data-ttu-id="16cee-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="16cee-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="16cee-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16cee-136">Minimum supported server</span></span><br/> | <span data-ttu-id="16cee-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16cee-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="16cee-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="16cee-138">Namespace</span></span><br/>                | <span data-ttu-id="16cee-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="16cee-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16cee-140">MOF</span><span class="sxs-lookup"><span data-stu-id="16cee-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16cee-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16cee-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16cee-142">DLL</span><span class="sxs-lookup"><span data-stu-id="16cee-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16cee-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16cee-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16cee-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16cee-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16cee-145">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="16cee-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


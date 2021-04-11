---
description: 表示從另一個計量值衍生的度量定義。 CIM \_ AggregationMetricDefinition 物件應該與它所套用的 cim \_ ManagedElement 物件相關聯。
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: CIM_AggregationMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692400"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="e590f-104">CIM \_ AggregationMetricDefinition 類別</span><span class="sxs-lookup"><span data-stu-id="e590f-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="e590f-105">表示從另一個計量值衍生的度量定義。</span><span class="sxs-lookup"><span data-stu-id="e590f-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="e590f-106">**Cim \_ AggregationMetricDefinition** 物件應該與它所套用的 **cim \_ ManagedElement** 物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="e590f-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="e590f-107">語法</span><span class="sxs-lookup"><span data-stu-id="e590f-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="e590f-108">成員</span><span class="sxs-lookup"><span data-stu-id="e590f-108">Members</span></span>

<span data-ttu-id="e590f-109">**CIM \_ AggregationMetricDefinition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e590f-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="e590f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e590f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e590f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e590f-111">Properties</span></span>

<span data-ttu-id="e590f-112">**CIM \_ AggregationMetricDefinition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e590f-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e590f-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e590f-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e590f-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e590f-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e590f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e590f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e590f-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ChangeType" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AggregationMetricDefinition**。**IsContinuous**") </span><span class="sxs-lookup"><span data-stu-id="e590f-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="e590f-117">使用一般屬性（例如方向變更、最小值和最大值和包裝語義）來表示計量值的變更方式。</span><span class="sxs-lookup"><span data-stu-id="e590f-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="e590f-118">**Simple Function** (5) </span><span class="sxs-lookup"><span data-stu-id="e590f-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e590f-119">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e590f-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e590f-120">**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="e590f-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e590f-121">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="e590f-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e590f-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e590f-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e590f-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e590f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e590f-124">在基礎度量上執行的基本計算，會到達此衍生計量的值。</span><span class="sxs-lookup"><span data-stu-id="e590f-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="e590f-125">當 **ChangeType** 屬性的值不是 "5" 時，這個屬性會是 **Null** (簡單函數) 。</span><span class="sxs-lookup"><span data-stu-id="e590f-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e590f-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e590f-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="e590f-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**最小** (2) </span><span class="sxs-lookup"><span data-stu-id="e590f-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e590f-128">計量會回報針對相關受監視實體偵測到的最小值。</span><span class="sxs-lookup"><span data-stu-id="e590f-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="e590f-129">這也稱為低水位線。</span><span class="sxs-lookup"><span data-stu-id="e590f-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="e590f-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (3) </span><span class="sxs-lookup"><span data-stu-id="e590f-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e590f-131">計量會回報針對相關受監視實體偵測到的最大值。</span><span class="sxs-lookup"><span data-stu-id="e590f-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="e590f-132">這也稱為高水位線。</span><span class="sxs-lookup"><span data-stu-id="e590f-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="e590f-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**平均** (4) </span><span class="sxs-lookup"><span data-stu-id="e590f-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e590f-134">度量會報告基礎度量值的平均值。</span><span class="sxs-lookup"><span data-stu-id="e590f-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="e590f-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>中 **位數** (5) </span><span class="sxs-lookup"><span data-stu-id="e590f-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e590f-136">計量會報告基礎度量值的中位數值。</span><span class="sxs-lookup"><span data-stu-id="e590f-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="e590f-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**模式** (6) </span><span class="sxs-lookup"><span data-stu-id="e590f-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e590f-138">度量會報告基礎度量值的強制回應值。</span><span class="sxs-lookup"><span data-stu-id="e590f-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e590f-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="e590f-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="e590f-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e590f-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e590f-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="e590f-141">Requirements</span></span>



| <span data-ttu-id="e590f-142">需求</span><span class="sxs-lookup"><span data-stu-id="e590f-142">Requirement</span></span> | <span data-ttu-id="e590f-143">值</span><span class="sxs-lookup"><span data-stu-id="e590f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e590f-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e590f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e590f-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e590f-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e590f-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e590f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e590f-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e590f-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e590f-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="e590f-148">Namespace</span></span><br/>                | <span data-ttu-id="e590f-149">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e590f-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e590f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e590f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e590f-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e590f-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e590f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e590f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e590f-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e590f-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e590f-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e590f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e590f-155">**CIM \_ BaseMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="e590f-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 


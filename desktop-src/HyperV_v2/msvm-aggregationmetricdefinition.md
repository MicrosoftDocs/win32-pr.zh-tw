---
description: 代表衍生自另一個計量值之度量的定義方面。
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Msvm_AggregationMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193927"
---
# <a name="msvm_aggregationmetricdefinition-class"></a><span data-ttu-id="1aa12-103">Msvm \_ AggregationMetricDefinition 類別</span><span class="sxs-lookup"><span data-stu-id="1aa12-103">Msvm\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="1aa12-104">代表衍生自另一個計量值之度量的定義方面。</span><span class="sxs-lookup"><span data-stu-id="1aa12-104">Represents the definition aspects of a metric that is derived from another metric value.</span></span> <span data-ttu-id="1aa12-105">**Msvm \_ AggregationMetricDefinition** 物件應該與它所套用的 managed 元素相關聯。</span><span class="sxs-lookup"><span data-stu-id="1aa12-105">The **Msvm\_AggregationMetricDefinition** object should be associated with the managed elements to which it applies.</span></span>

<span data-ttu-id="1aa12-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1aa12-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa12-107">語法</span><span class="sxs-lookup"><span data-stu-id="1aa12-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="1aa12-108">成員</span><span class="sxs-lookup"><span data-stu-id="1aa12-108">Members</span></span>

<span data-ttu-id="1aa12-109">**Msvm \_ AggregationMetricDefinition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1aa12-109">The **Msvm\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="1aa12-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1aa12-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1aa12-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1aa12-111">Properties</span></span>

<span data-ttu-id="1aa12-112">**Msvm \_ AggregationMetricDefinition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1aa12-112">The **Msvm\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1aa12-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="1aa12-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1aa12-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-116">定義一個或多個字串，可用來針對特定維度上的度量值， (細分) 查詢。</span><span class="sxs-lookup"><span data-stu-id="1aa12-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="1aa12-117">其中一個範例是交易名稱，允許將所有交易的總值細分為一組值，每個交易名稱各一個值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="1aa12-118">其他範例可能是應用程式系統或使用者組名。</span><span class="sxs-lookup"><span data-stu-id="1aa12-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="1aa12-119">這些字串是免費格式，對計量資料的使用者而言應該有意義。</span><span class="sxs-lookup"><span data-stu-id="1aa12-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="1aa12-120">這些字串表示基礎檢測針對此計量定義支援哪些細分維度。</span><span class="sxs-lookup"><span data-stu-id="1aa12-120">The strings indicate which break down dimensions are supported for this metric definition by the underlying instrumentation.</span></span> <span data-ttu-id="1aa12-121">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-122">**計算**</span><span class="sxs-lookup"><span data-stu-id="1aa12-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-125">描述用於執行計算之度量的特性。</span><span class="sxs-lookup"><span data-stu-id="1aa12-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="1aa12-126">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="1aa12-127">這可能是 **Null** 或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="1aa12-128">值</span><span class="sxs-lookup"><span data-stu-id="1aa12-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="1aa12-129">意義</span><span class="sxs-lookup"><span data-stu-id="1aa12-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="1aa12-130"><dt>**非可計算**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="1aa12-131">無法計算此值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-131">The value cannot be calculated.</span></span> <span data-ttu-id="1aa12-132">例如，字串。</span><span class="sxs-lookup"><span data-stu-id="1aa12-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="1aa12-133"><dt>**Summable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="1aa12-134">此值可以加總許多實例。</span><span class="sxs-lookup"><span data-stu-id="1aa12-134">The value can be summed over many instances.</span></span> <span data-ttu-id="1aa12-135">例如，如果每個備份作業都是工作單位，而且每個作業平均備份27000檔案，則100備份作業會處理2700000檔案。</span><span class="sxs-lookup"><span data-stu-id="1aa12-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="1aa12-136"><dt>**非 summable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="1aa12-137">此值不能加總在許多實例上。</span><span class="sxs-lookup"><span data-stu-id="1aa12-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="1aa12-138">其中一個範例是在作業抵達伺服器時測量佇列長度的度量。</span><span class="sxs-lookup"><span data-stu-id="1aa12-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="1aa12-139">如果每個作業都是工作單位，而且每個作業抵達時的平均佇列長度為33，則表示100作業的佇列長度為3300並不合理。</span><span class="sxs-lookup"><span data-stu-id="1aa12-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="1aa12-140">假設 mean 為33，是合理的。</span><span class="sxs-lookup"><span data-stu-id="1aa12-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1aa12-141">**標題**</span><span class="sxs-lookup"><span data-stu-id="1aa12-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-144">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1aa12-144">A short description of the object.</span></span> <span data-ttu-id="1aa12-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1aa12-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="1aa12-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-149">表示計量值如何變更，以典型的細部屬性組合（例如方向變更、最小和最大值和最大值），以及換行語義的形式呈現。</span><span class="sxs-lookup"><span data-stu-id="1aa12-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="1aa12-150">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="1aa12-151">值</span><span class="sxs-lookup"><span data-stu-id="1aa12-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1aa12-152">意義</span><span class="sxs-lookup"><span data-stu-id="1aa12-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1aa12-153"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="1aa12-154">度量設計師未限定 **ChangeType**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-154">The metric designer did not qualify the **ChangeType**.</span></span><br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="1aa12-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="1aa12-156">如果 **IsContinuous** 屬性為 "false"， **ChangeType** 就沒有意義，且必須設定為 "N/A"。</span><span class="sxs-lookup"><span data-stu-id="1aa12-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="1aa12-157"><dt>**計數器**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="1aa12-158">度量是計數器度量。</span><span class="sxs-lookup"><span data-stu-id="1aa12-158">The metric is a counter metric.</span></span> <span data-ttu-id="1aa12-159">這些都有非負整數值，在達到可表示的最大值，然後換行並開始從0增加時，才會增加。</span><span class="sxs-lookup"><span data-stu-id="1aa12-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="1aa12-160"><dt></dt>量測計<dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="1aa12-161">計量是量測計度量。</span><span class="sxs-lookup"><span data-stu-id="1aa12-161">The metric is a gauge metric.</span></span> <span data-ttu-id="1aa12-162">這些值具有可任意增加和減少的整數或浮點值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="1aa12-163"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="1aa12-164"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="1aa12-165">廠商可以擴充廠商保留範圍中的 **ChangeType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1aa12-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="1aa12-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="1aa12-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-169">度量的資料類型。</span><span class="sxs-lookup"><span data-stu-id="1aa12-169">The data type of the metric.</span></span> <span data-ttu-id="1aa12-170">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="1aa12-171"><span id="boolean"></span><span id="BOOLEAN"></span>**布林值** (1) </span><span class="sxs-lookup"><span data-stu-id="1aa12-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2) </span><span class="sxs-lookup"><span data-stu-id="1aa12-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3) </span><span class="sxs-lookup"><span data-stu-id="1aa12-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4) </span><span class="sxs-lookup"><span data-stu-id="1aa12-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5) </span><span class="sxs-lookup"><span data-stu-id="1aa12-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6) </span><span class="sxs-lookup"><span data-stu-id="1aa12-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7) </span><span class="sxs-lookup"><span data-stu-id="1aa12-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8) </span><span class="sxs-lookup"><span data-stu-id="1aa12-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9) </span><span class="sxs-lookup"><span data-stu-id="1aa12-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-180"><span id="string"></span><span id="STRING"></span>**字串** (10) </span><span class="sxs-lookup"><span data-stu-id="1aa12-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11) </span><span class="sxs-lookup"><span data-stu-id="1aa12-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12) </span><span class="sxs-lookup"><span data-stu-id="1aa12-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13) </span><span class="sxs-lookup"><span data-stu-id="1aa12-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 ) </span><span class="sxs-lookup"><span data-stu-id="1aa12-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1aa12-185">**說明**</span><span class="sxs-lookup"><span data-stu-id="1aa12-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-188">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1aa12-188">A description of the object.</span></span> <span data-ttu-id="1aa12-189">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1aa12-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1aa12-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-193">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa12-193">A display name for the object.</span></span> <span data-ttu-id="1aa12-194">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1aa12-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="1aa12-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-198">指出基礎檢測如何收集度量值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="1aa12-199">這可讓用戶端應用程式選擇正確的度量以供用途。</span><span class="sxs-lookup"><span data-stu-id="1aa12-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="1aa12-200">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="1aa12-201">這可能是 **Null** 或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="1aa12-202">值</span><span class="sxs-lookup"><span data-stu-id="1aa12-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1aa12-203">意義</span><span class="sxs-lookup"><span data-stu-id="1aa12-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1aa12-204"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="1aa12-205">收集類型未知。</span><span class="sxs-lookup"><span data-stu-id="1aa12-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="1aa12-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="1aa12-207">當測量的資源內的值變更時，就會立即更新度量值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="1aa12-208"><dt>**週期**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="1aa12-209">度量值會定期更新。</span><span class="sxs-lookup"><span data-stu-id="1aa12-209">The metric values get updated periodically.</span></span> <span data-ttu-id="1aa12-210">比方說，在用戶端應用程式中，套用至目前時間的度量值在每個收集間隔期間都會出現常數，然後在每個收集間隔結束時跳到新值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="1aa12-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="1aa12-212">每次用戶端應用程式讀取時，就會決定度量值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="1aa12-213"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="1aa12-214"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="1aa12-215">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="1aa12-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-218">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1aa12-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-219">可唯一識別度量定義的字串。</span><span class="sxs-lookup"><span data-stu-id="1aa12-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="1aa12-220">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1aa12-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-224">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1aa12-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-225">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="1aa12-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1aa12-226">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1aa12-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="1aa12-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-228">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1aa12-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-230">指出度量值為連續或純量。</span><span class="sxs-lookup"><span data-stu-id="1aa12-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="1aa12-231">效能計量是連續度量的範例。</span><span class="sxs-lookup"><span data-stu-id="1aa12-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="1aa12-232">純量計量的範例包括錯誤碼或操作狀態。</span><span class="sxs-lookup"><span data-stu-id="1aa12-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="1aa12-233">您可以使用「大於」關聯來比較連續計量。</span><span class="sxs-lookup"><span data-stu-id="1aa12-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="1aa12-234">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-235">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1aa12-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-238">計量的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa12-238">The name of the metric.</span></span> <span data-ttu-id="1aa12-239">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="1aa12-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-243">識別值的特定單位。</span><span class="sxs-lookup"><span data-stu-id="1aa12-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="1aa12-244">這個屬性的值將會是程式設計單位辨識符號的合法值，如 [DSP0004 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="1aa12-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="1aa12-245">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa12-246">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="1aa12-246">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-248">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1aa12-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-249">識別在基礎度量上執行的基本計算，以到達此衍生度量的值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-249">Identifies the basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="1aa12-250">這個屬性會繼承自 **CIM \_ AggregationMetricDefinition** ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1aa12-250">This property is inherited from **CIM\_AggregationMetricDefinition** and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1aa12-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**最小** (2) </span><span class="sxs-lookup"><span data-stu-id="1aa12-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (3) </span><span class="sxs-lookup"><span data-stu-id="1aa12-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**平均** (4) </span><span class="sxs-lookup"><span data-stu-id="1aa12-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>中 **位數** (5) </span><span class="sxs-lookup"><span data-stu-id="1aa12-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**模式** (6) </span><span class="sxs-lookup"><span data-stu-id="1aa12-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1aa12-256">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="1aa12-256">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aa12-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-259">表示套用度量值的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="1aa12-259">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="1aa12-260">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-260">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="1aa12-261">值</span><span class="sxs-lookup"><span data-stu-id="1aa12-261">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1aa12-262">意義</span><span class="sxs-lookup"><span data-stu-id="1aa12-262">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1aa12-263"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-263"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="1aa12-264">計量設計師未限定時間範圍，或對提供者而言是未知的。</span><span class="sxs-lookup"><span data-stu-id="1aa12-264">The time scope was not qualified by the metric designer, or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="1aa12-265"><dt>**點**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-265"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="1aa12-266">度量會套用至某個時間點。</span><span class="sxs-lookup"><span data-stu-id="1aa12-266">The metric applies to a point in time.</span></span> <span data-ttu-id="1aa12-267">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間點，而 **Duration** 屬性一律為0。</span><span class="sxs-lookup"><span data-stu-id="1aa12-267">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="1aa12-268"><dt>**間隔**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-268"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="1aa12-269">度量會套用至時間間隔。</span><span class="sxs-lookup"><span data-stu-id="1aa12-269">The metric applies to a time interval.</span></span> <span data-ttu-id="1aa12-270">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾，而 **duration** 屬性則會指定其持續時間。</span><span class="sxs-lookup"><span data-stu-id="1aa12-270">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="1aa12-271"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-271"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="1aa12-272">計量適用于啟動測量資源 (的時間間隔，也就是 MetricDefForMe) 相關聯的 ManagedElement。</span><span class="sxs-lookup"><span data-stu-id="1aa12-272">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="1aa12-273">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾。</span><span class="sxs-lookup"><span data-stu-id="1aa12-273">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="1aa12-274">如果 **Duration** 屬性是0，這表示測量的資源的啟動時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="1aa12-274">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="1aa12-275">否則， **duration** 會指定資源和 **時間戳記** 啟動之間的持續時間。</span><span class="sxs-lookup"><span data-stu-id="1aa12-275">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="1aa12-276"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-276"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="1aa12-277"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-277"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="1aa12-278">**單位**</span><span class="sxs-lookup"><span data-stu-id="1aa12-278">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aa12-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aa12-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aa12-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aa12-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aa12-281">識別值的單位，例如「mb」。</span><span class="sxs-lookup"><span data-stu-id="1aa12-281">Identifies the units of a value, for example, "megabytes".</span></span> <span data-ttu-id="1aa12-282">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="1aa12-282">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1aa12-283">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aa12-283">Requirements</span></span>



| <span data-ttu-id="1aa12-284">需求</span><span class="sxs-lookup"><span data-stu-id="1aa12-284">Requirement</span></span> | <span data-ttu-id="1aa12-285">值</span><span class="sxs-lookup"><span data-stu-id="1aa12-285">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa12-286">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aa12-286">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa12-287">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aa12-287">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1aa12-288">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aa12-288">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa12-289">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aa12-289">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1aa12-290">命名空間</span><span class="sxs-lookup"><span data-stu-id="1aa12-290">Namespace</span></span><br/>                | <span data-ttu-id="1aa12-291">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1aa12-291">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1aa12-292">MOF</span><span class="sxs-lookup"><span data-stu-id="1aa12-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aa12-293"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-293"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aa12-294">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa12-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa12-295"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1aa12-295"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


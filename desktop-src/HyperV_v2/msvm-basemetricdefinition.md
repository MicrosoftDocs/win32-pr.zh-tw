---
description: 表示度量的定義方面。
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986402"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="3c9f6-103">Msvm \_ BaseMetricDefinition 類別</span><span class="sxs-lookup"><span data-stu-id="3c9f6-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="3c9f6-104">表示度量的定義方面。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="3c9f6-105">**Msvm \_ BaseMetricDefinition** 類別應該與它所套用的 [**CIM \_ ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)相關聯。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="3c9f6-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c9f6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
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
};
```

## <a name="members"></a><span data-ttu-id="3c9f6-108">成員</span><span class="sxs-lookup"><span data-stu-id="3c9f6-108">Members</span></span>

<span data-ttu-id="3c9f6-109">**Msvm \_ BaseMetricDefinition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c9f6-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="3c9f6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3c9f6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c9f6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3c9f6-111">Properties</span></span>

<span data-ttu-id="3c9f6-112">**Msvm \_ BaseMetricDefinition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c9f6-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3c9f6-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-116">定義一個或多個字串，可用來針對特定維度上的度量值， (細分) 查詢。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="3c9f6-117">其中一個範例是交易名稱，允許將所有交易的總值細分為一組值，每個交易名稱各一個值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="3c9f6-118">其他範例可能是應用程式系統或使用者組名。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="3c9f6-119">這些字串是免費格式，對計量資料的使用者而言應該有意義。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="3c9f6-120">這些字串表示基礎檢測針對此計量定義支援哪些細分維度。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="3c9f6-121">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-122">**計算**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-125">描述用於執行計算之度量的特性。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="3c9f6-126">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="3c9f6-127">這可能是 **Null** 或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="3c9f6-128">值</span><span class="sxs-lookup"><span data-stu-id="3c9f6-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="3c9f6-129">意義</span><span class="sxs-lookup"><span data-stu-id="3c9f6-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="3c9f6-130"><dt>**非可計算**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3c9f6-131">無法計算此值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-131">The value cannot be calculated.</span></span> <span data-ttu-id="3c9f6-132">例如，字串。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="3c9f6-133"><dt>**Summable**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="3c9f6-134">此值可以加總許多實例。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-134">The value can be summed over many instances.</span></span> <span data-ttu-id="3c9f6-135">例如，如果每個備份作業都是工作單位，而且每個作業平均備份27000檔案，則100備份作業會處理2700000檔案。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="3c9f6-136"><dt>**非 summable**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="3c9f6-137">此值不能加總在許多實例上。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="3c9f6-138">其中一個範例是在作業抵達伺服器時測量佇列長度的度量。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="3c9f6-139">如果每個作業都是工作單位，而且每個作業抵達時的平均佇列長度為33，則表示100作業的佇列長度為3300並不合理。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="3c9f6-140">假設 mean 為33，是合理的。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c9f6-141">**標題**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-144">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-144">A short description of the object.</span></span> <span data-ttu-id="3c9f6-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-149">表示計量值如何變更，以典型的細部屬性組合（例如方向變更、最小和最大值和最大值），以及換行語義的形式呈現。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="3c9f6-150">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="3c9f6-151">值</span><span class="sxs-lookup"><span data-stu-id="3c9f6-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3c9f6-152">意義</span><span class="sxs-lookup"><span data-stu-id="3c9f6-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c9f6-153"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="3c9f6-154">度量設計師未限定 **ChangeType。**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="3c9f6-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="3c9f6-156">如果 **IsContinuous** 屬性為 "false"， **ChangeType** 就沒有意義，且必須設定為 "N/A"。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="3c9f6-157"><dt>**計數器**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="3c9f6-158">度量是計數器度量。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-158">The metric is a counter metric.</span></span> <span data-ttu-id="3c9f6-159">這些都有非負整數值，在達到可表示的最大值，然後換行並開始從0增加時，才會增加。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="3c9f6-160"><dt></dt>量測計<dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="3c9f6-161">計量是量測計度量。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-161">The metric is a gauge metric.</span></span> <span data-ttu-id="3c9f6-162">這些值具有可任意增加和減少的整數或浮點值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3c9f6-163"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="3c9f6-164"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="3c9f6-165">廠商可以擴充廠商保留範圍中的 **ChangeType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="3c9f6-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-169">度量的資料類型。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-169">The data type of the metric.</span></span> <span data-ttu-id="3c9f6-170">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="3c9f6-171"><span id="boolean"></span><span id="BOOLEAN"></span>**布林值** (1) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-180"><span id="string"></span><span id="STRING"></span>**字串** (10) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 ) </span><span class="sxs-lookup"><span data-stu-id="3c9f6-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c9f6-185">**說明**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-188">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-188">A description of the object.</span></span> <span data-ttu-id="3c9f6-189">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-193">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-193">A display name for the object.</span></span> <span data-ttu-id="3c9f6-194">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-198">指出基礎檢測如何收集度量值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="3c9f6-199">這可讓用戶端應用程式選擇正確的度量以供用途。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="3c9f6-200">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="3c9f6-201">這可能是 **Null** 或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="3c9f6-202">值</span><span class="sxs-lookup"><span data-stu-id="3c9f6-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3c9f6-203">意義</span><span class="sxs-lookup"><span data-stu-id="3c9f6-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c9f6-204"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="3c9f6-205">收集類型未知。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="3c9f6-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="3c9f6-207">當測量的資源內的值變更時，就會立即更新度量值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="3c9f6-208"><dt>**週期**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="3c9f6-209">度量值會定期更新。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-209">The metric values get updated periodically.</span></span> <span data-ttu-id="3c9f6-210">比方說，在用戶端應用程式中，套用至目前時間的度量值在每個收集間隔期間都會出現常數，然後在每個收集間隔結束時跳到新值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="3c9f6-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="3c9f6-212">每次用戶端應用程式讀取時，就會決定度量值。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3c9f6-213"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="3c9f6-214"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3c9f6-215">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-218">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-219">可唯一識別度量定義的字串。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="3c9f6-220">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-224">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-225">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3c9f6-226">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-228">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-230">指出度量值為連續或純量。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="3c9f6-231">效能計量是連續度量的範例。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="3c9f6-232">純量計量的範例包括錯誤碼或操作狀態。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="3c9f6-233">您可以使用「大於」關聯來比較連續計量。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="3c9f6-234">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-235">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-238">計量的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-238">The name of the metric.</span></span> <span data-ttu-id="3c9f6-239">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-243">識別值的特定單位。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="3c9f6-244">這個屬性的值將會是程式設計單位辨識符號的合法值，如 [DSP0004 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="3c9f6-245">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="3c9f6-246">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-249">表示套用度量值的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="3c9f6-250">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="3c9f6-251">值</span><span class="sxs-lookup"><span data-stu-id="3c9f6-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3c9f6-252">意義</span><span class="sxs-lookup"><span data-stu-id="3c9f6-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c9f6-253"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="3c9f6-254">時間範圍未由計量設計師限定，或對提供者而言是未知的。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="3c9f6-255"><dt>**點**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="3c9f6-256">度量會套用至某個時間點。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-256">The metric applies to a point in time.</span></span> <span data-ttu-id="3c9f6-257">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間點，而 **Duration** 屬性一律為0。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="3c9f6-258"><dt>**間隔**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="3c9f6-259">度量會套用至時間間隔。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-259">The metric applies to a time interval.</span></span> <span data-ttu-id="3c9f6-260">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾，而 **duration** 屬性則會指定其持續時間。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="3c9f6-261"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="3c9f6-262">計量適用于啟動測量資源 (的時間間隔，也就是 MetricDefForMe) 相關聯的 ManagedElement。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="3c9f6-263">在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="3c9f6-264">如果 **Duration** 屬性是0，這表示測量的資源的啟動時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="3c9f6-265">否則， **duration** 會指定資源和 **時間戳記** 啟動之間的持續時間。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3c9f6-266"><dt>**DMTF 保留**</dt> <dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="3c9f6-267"><dt>**廠商保留**</dt> <dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="3c9f6-268">**單位**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c9f6-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c9f6-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c9f6-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c9f6-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c9f6-271">識別值的特定單位，例如「mb」。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="3c9f6-272">這個屬性繼承自 **CIM \_ BaseMetricDefinition**。</span><span class="sxs-lookup"><span data-stu-id="3c9f6-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c9f6-273">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c9f6-273">Requirements</span></span>



| <span data-ttu-id="3c9f6-274">需求</span><span class="sxs-lookup"><span data-stu-id="3c9f6-274">Requirement</span></span> | <span data-ttu-id="3c9f6-275">值</span><span class="sxs-lookup"><span data-stu-id="3c9f6-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9f6-276">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c9f6-276">Minimum supported client</span></span><br/> | <span data-ttu-id="3c9f6-277">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c9f6-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c9f6-278">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c9f6-278">Minimum supported server</span></span><br/> | <span data-ttu-id="3c9f6-279">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c9f6-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c9f6-280">命名空間</span><span class="sxs-lookup"><span data-stu-id="3c9f6-280">Namespace</span></span><br/>                | <span data-ttu-id="3c9f6-281">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3c9f6-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c9f6-282">MOF</span><span class="sxs-lookup"><span data-stu-id="3c9f6-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c9f6-283"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c9f6-284">DLL</span><span class="sxs-lookup"><span data-stu-id="3c9f6-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c9f6-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f6-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


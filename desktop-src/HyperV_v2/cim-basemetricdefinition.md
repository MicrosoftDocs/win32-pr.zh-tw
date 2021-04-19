---
description: 表示包含 CIM MetricInstance 物件中繼資料的度量定義 \_ 。
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001455"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="503e8-103">CIM \_ BaseMetricDefinition 類別</span><span class="sxs-lookup"><span data-stu-id="503e8-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="503e8-104">表示包含 **CIM \_ MetricInstance** 物件中繼資料的度量定義。</span><span class="sxs-lookup"><span data-stu-id="503e8-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="503e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="503e8-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="503e8-106">成員</span><span class="sxs-lookup"><span data-stu-id="503e8-106">Members</span></span>

<span data-ttu-id="503e8-107">**CIM \_ BaseMetricDefinition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="503e8-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="503e8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="503e8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="503e8-109">屬性</span><span class="sxs-lookup"><span data-stu-id="503e8-109">Properties</span></span>

<span data-ttu-id="503e8-110">**CIM \_ BaseMetricDefinition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="503e8-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="503e8-111">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="503e8-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-112">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="503e8-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="503e8-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-114">陣列，其中包含可用來將 [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) 物件的查詢沿著特定維度細分的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="503e8-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="503e8-115">這些字串對計量資料的終端使用者應該有意義。</span><span class="sxs-lookup"><span data-stu-id="503e8-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="503e8-116">此外，這些字串應該會指出基礎檢測針對計量定義支援哪些細分維度。</span><span class="sxs-lookup"><span data-stu-id="503e8-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="503e8-117">例如，允許將所有交易的總值細分為一組值的交易名稱，每個交易名稱各有一個值。</span><span class="sxs-lookup"><span data-stu-id="503e8-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="503e8-118">其他範例包括應用程式系統或使用者組名。</span><span class="sxs-lookup"><span data-stu-id="503e8-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="503e8-119">**計算**</span><span class="sxs-lookup"><span data-stu-id="503e8-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-120">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="503e8-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-122">用來執行計算的度量特性。</span><span class="sxs-lookup"><span data-stu-id="503e8-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="503e8-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**非可計算** (1) </span><span class="sxs-lookup"><span data-stu-id="503e8-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-124">字串。</span><span class="sxs-lookup"><span data-stu-id="503e8-124">A string.</span></span> <span data-ttu-id="503e8-125">算術沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="503e8-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="503e8-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2) </span><span class="sxs-lookup"><span data-stu-id="503e8-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-127">將此值與許多實例（例如 UnitOfWork）加總，例如在備份作業中處理的檔案數目，是合理的。</span><span class="sxs-lookup"><span data-stu-id="503e8-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="503e8-128">例如，如果每個備份作業都是 UnitOfWork，而且每個作業都會平均備份27000檔案，則應該假設100備份作業已處理2700000檔案。</span><span class="sxs-lookup"><span data-stu-id="503e8-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="503e8-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**非 summable** (3) </span><span class="sxs-lookup"><span data-stu-id="503e8-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-130">在 UnitOfWork 的許多實例加總此值並不合理。</span><span class="sxs-lookup"><span data-stu-id="503e8-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="503e8-131">其中一個範例是在作業抵達伺服器時測量佇列長度的度量。</span><span class="sxs-lookup"><span data-stu-id="503e8-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="503e8-132">如果每個作業都是 UnitOfWork，而且每個作業抵達時的平均佇列長度為33，則表示100作業的佇列長度為3300並不合理。</span><span class="sxs-lookup"><span data-stu-id="503e8-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="503e8-133">假設 mean 為33，是合理的。</span><span class="sxs-lookup"><span data-stu-id="503e8-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="503e8-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="503e8-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="503e8-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="503e8-137">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ BaseMetricDefinition**.**IsContinuous**") </span><span class="sxs-lookup"><span data-stu-id="503e8-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="503e8-138">使用一般屬性（例如方向變更、最小值和最大值和包裝語義）來表示計量值的變更方式。</span><span class="sxs-lookup"><span data-stu-id="503e8-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="503e8-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="503e8-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-140">度量設計師未限定 ChangeType。</span><span class="sxs-lookup"><span data-stu-id="503e8-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="503e8-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2) </span><span class="sxs-lookup"><span data-stu-id="503e8-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-142">如果 "IsContinuous" 屬性為 "false"，ChangeType 就沒有意義，且必須設定為 "N/A"。</span><span class="sxs-lookup"><span data-stu-id="503e8-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="503e8-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**計數器** (3) </span><span class="sxs-lookup"><span data-stu-id="503e8-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-144">度量是計數器度量。</span><span class="sxs-lookup"><span data-stu-id="503e8-144">The metric is a counter metric.</span></span> <span data-ttu-id="503e8-145">這些都有非負整數值，會在到達可表示的最大值時單純增加，然後換行並開始從0增加。</span><span class="sxs-lookup"><span data-stu-id="503e8-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="503e8-146">這類計數器（也稱為變換計數器）可以用來計算網路錯誤的數目或處理的交易數目。</span><span class="sxs-lookup"><span data-stu-id="503e8-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="503e8-147">用戶端應用程式追蹤換行程式的唯一方法，是以適當的短間隔取出計數器的值。</span><span class="sxs-lookup"><span data-stu-id="503e8-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="503e8-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>量測 **計 (4**) </span><span class="sxs-lookup"><span data-stu-id="503e8-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-149">計量是量測計度量。</span><span class="sxs-lookup"><span data-stu-id="503e8-149">The metric is a gauge metric.</span></span> <span data-ttu-id="503e8-150">這些值具有可任意增加和減少的整數或浮點值。</span><span class="sxs-lookup"><span data-stu-id="503e8-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="503e8-151">量測計在達到可表示的最小值或最大值時不能換行，而是在該數位的值 "棒"。</span><span class="sxs-lookup"><span data-stu-id="503e8-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="503e8-152">可代表值範圍內的最小值或最大值，而不一定會定義度量值 "棒"。</span><span class="sxs-lookup"><span data-stu-id="503e8-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="503e8-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) </span><span class="sxs-lookup"><span data-stu-id="503e8-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="503e8-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="503e8-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="503e8-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="503e8-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-156">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="503e8-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-158">度量的資料類型。</span><span class="sxs-lookup"><span data-stu-id="503e8-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="503e8-159">**布林值** (1) </span><span class="sxs-lookup"><span data-stu-id="503e8-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="503e8-160">**char16** (2) </span><span class="sxs-lookup"><span data-stu-id="503e8-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="503e8-161">**datetime** (3) </span><span class="sxs-lookup"><span data-stu-id="503e8-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="503e8-162">**real32** (4) </span><span class="sxs-lookup"><span data-stu-id="503e8-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="503e8-163">**real64** (5) </span><span class="sxs-lookup"><span data-stu-id="503e8-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="503e8-164">**sint16** (6) </span><span class="sxs-lookup"><span data-stu-id="503e8-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="503e8-165">**sint32** (7) </span><span class="sxs-lookup"><span data-stu-id="503e8-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="503e8-166">**sint64** (8) </span><span class="sxs-lookup"><span data-stu-id="503e8-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="503e8-167">**sint8** (9) </span><span class="sxs-lookup"><span data-stu-id="503e8-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="503e8-168">**字串** (10) </span><span class="sxs-lookup"><span data-stu-id="503e8-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="503e8-169">**uint16** (11) </span><span class="sxs-lookup"><span data-stu-id="503e8-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="503e8-170">**uint32** (12) </span><span class="sxs-lookup"><span data-stu-id="503e8-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="503e8-171">**uint64** (13) </span><span class="sxs-lookup"><span data-stu-id="503e8-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="503e8-172">**uint8** (14) </span><span class="sxs-lookup"><span data-stu-id="503e8-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="503e8-173">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="503e8-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-174">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="503e8-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-176">指出基礎檢測如何收集度量值。</span><span class="sxs-lookup"><span data-stu-id="503e8-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="503e8-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="503e8-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-178">指出 GatheringType 是未知的。</span><span class="sxs-lookup"><span data-stu-id="503e8-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="503e8-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2) </span><span class="sxs-lookup"><span data-stu-id="503e8-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-180">指出當測量的資源內的值變更時，會立即更新 CIM 度量值。</span><span class="sxs-lookup"><span data-stu-id="503e8-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="503e8-181">OnChange 計量的值會確實反映資源在任何時間內的目前情況。</span><span class="sxs-lookup"><span data-stu-id="503e8-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="503e8-182">例如，當使用者登入和關閉時，會立即更新的已登入使用者數目。</span><span class="sxs-lookup"><span data-stu-id="503e8-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="503e8-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**定期** (3) </span><span class="sxs-lookup"><span data-stu-id="503e8-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-184">"：表示會定期更新 CIM 度量值。</span><span class="sxs-lookup"><span data-stu-id="503e8-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="503e8-185">比方說，在用戶端應用程式中，套用至目前時間的度量值在每個收集間隔中都會顯示為常數，然後在每個收集間隔結束時跳到新值。</span><span class="sxs-lookup"><span data-stu-id="503e8-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="503e8-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4) </span><span class="sxs-lookup"><span data-stu-id="503e8-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-187">指出每次用戶端應用程式讀取時，都會決定 CIM 度量值。</span><span class="sxs-lookup"><span data-stu-id="503e8-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="503e8-188">如果有人要求，OnRequest 計量的值真的會傳回資源內目前的狀況。</span><span class="sxs-lookup"><span data-stu-id="503e8-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="503e8-189">不過，它們不會變更 "未觀察到"，因此不建議訂閱 OnRequest 計量的值變更。</span><span class="sxs-lookup"><span data-stu-id="503e8-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="503e8-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) </span><span class="sxs-lookup"><span data-stu-id="503e8-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="503e8-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="503e8-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="503e8-192">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="503e8-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="503e8-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="503e8-195">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="503e8-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="503e8-196">度量定義的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="503e8-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="503e8-197">建議您開啟 Software Foundation (憑證) UUID/Guid。</span><span class="sxs-lookup"><span data-stu-id="503e8-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="503e8-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="503e8-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-199">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="503e8-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-201">如果度量值是連續的，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="503e8-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="503e8-202">**名稱**</span><span class="sxs-lookup"><span data-stu-id="503e8-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="503e8-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-205">計量的名稱。</span><span class="sxs-lookup"><span data-stu-id="503e8-205">The name of the metric.</span></span> <span data-ttu-id="503e8-206">此名稱不一定要是唯一的，但應該是描述性的，而且可能包含空格。</span><span class="sxs-lookup"><span data-stu-id="503e8-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="503e8-207">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="503e8-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="503e8-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-210">值的特定單位。</span><span class="sxs-lookup"><span data-stu-id="503e8-210">The specific units of a value.</span></span> <span data-ttu-id="503e8-211">這個屬性的值應該是程式設計單位辨識符號的合法值，如 DSP0004 2.4 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="503e8-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="503e8-212">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="503e8-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="503e8-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="503e8-215">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**"、"**CIM \_ BaseMetricValue**。**Duration**") </span><span class="sxs-lookup"><span data-stu-id="503e8-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="503e8-216">適用于度量設計師的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="503e8-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="503e8-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="503e8-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-218">指出時間範圍未由計量設計師限定，或對提供者而言是未知的。</span><span class="sxs-lookup"><span data-stu-id="503e8-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="503e8-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**點** (2) </span><span class="sxs-lookup"><span data-stu-id="503e8-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-220">指出度量會套用至某個時間點。</span><span class="sxs-lookup"><span data-stu-id="503e8-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="503e8-221">在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間點，而持續時間一律為0。</span><span class="sxs-lookup"><span data-stu-id="503e8-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="503e8-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**間隔** (3) </span><span class="sxs-lookup"><span data-stu-id="503e8-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-223">指出度量會套用至時間間隔。</span><span class="sxs-lookup"><span data-stu-id="503e8-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="503e8-224">在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間間隔的結束時間，並指定其持續時間。</span><span class="sxs-lookup"><span data-stu-id="503e8-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="503e8-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4) </span><span class="sxs-lookup"><span data-stu-id="503e8-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="503e8-226">表示計量會套用至開始測量資源 (（也就是 MetricDefForMe) 相關聯的 ManagedElement）啟動的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="503e8-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="503e8-227">在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間間隔的結束時間。</span><span class="sxs-lookup"><span data-stu-id="503e8-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="503e8-228">如果持續時間為0，這表示測量的資源的啟動時間是未知的。</span><span class="sxs-lookup"><span data-stu-id="503e8-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="503e8-229">否則，Duration 會指定資源和時間戳記啟動之間的持續時間。</span><span class="sxs-lookup"><span data-stu-id="503e8-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="503e8-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) </span><span class="sxs-lookup"><span data-stu-id="503e8-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="503e8-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="503e8-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="503e8-232">**單位**</span><span class="sxs-lookup"><span data-stu-id="503e8-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="503e8-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="503e8-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="503e8-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="503e8-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="503e8-235">度量的單位。</span><span class="sxs-lookup"><span data-stu-id="503e8-235">The units of the metric.</span></span> <span data-ttu-id="503e8-236">範例包括位元組、封包、作業、檔案、毫秒和安培。</span><span class="sxs-lookup"><span data-stu-id="503e8-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="503e8-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="503e8-237">Requirements</span></span>



| <span data-ttu-id="503e8-238">需求</span><span class="sxs-lookup"><span data-stu-id="503e8-238">Requirement</span></span> | <span data-ttu-id="503e8-239">值</span><span class="sxs-lookup"><span data-stu-id="503e8-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503e8-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="503e8-240">Minimum supported client</span></span><br/> | <span data-ttu-id="503e8-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="503e8-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="503e8-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="503e8-242">Minimum supported server</span></span><br/> | <span data-ttu-id="503e8-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="503e8-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="503e8-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="503e8-244">Namespace</span></span><br/>                | <span data-ttu-id="503e8-245">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="503e8-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="503e8-246">MOF</span><span class="sxs-lookup"><span data-stu-id="503e8-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="503e8-247"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="503e8-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="503e8-248">DLL</span><span class="sxs-lookup"><span data-stu-id="503e8-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="503e8-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="503e8-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="503e8-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="503e8-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503e8-251">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="503e8-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 


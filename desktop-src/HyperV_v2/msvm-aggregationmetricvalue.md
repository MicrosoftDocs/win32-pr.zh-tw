---
description: 表示 Msvm AggregationMetricDefinition 類別的實例所定義之度量的實例值 \_ 。
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027197"
---
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="58278-103">Msvm \_ AggregationMetricValue 類別</span><span class="sxs-lookup"><span data-stu-id="58278-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="58278-104">表示 [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) 類別的實例所定義之度量的實例值。</span><span class="sxs-lookup"><span data-stu-id="58278-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="58278-105">繼承自 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 的屬性會提供實際的度量值。</span><span class="sxs-lookup"><span data-stu-id="58278-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="58278-106">這個類別所定義的屬性會提供套用彙總函式的間隔相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58278-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="58278-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="58278-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58278-108">語法</span><span class="sxs-lookup"><span data-stu-id="58278-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="58278-109">成員</span><span class="sxs-lookup"><span data-stu-id="58278-109">Members</span></span>

<span data-ttu-id="58278-110">**Msvm \_ AggregationMetricValue** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58278-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="58278-111">屬性</span><span class="sxs-lookup"><span data-stu-id="58278-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58278-112">屬性</span><span class="sxs-lookup"><span data-stu-id="58278-112">Properties</span></span>

<span data-ttu-id="58278-113">**Msvm \_ AggregationMetricValue** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="58278-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58278-114">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="58278-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-115">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="58278-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58278-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-117">代表計算匯總的持續時間。</span><span class="sxs-lookup"><span data-stu-id="58278-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="58278-118">套用彙總函式的監視間隔開始時間，是藉由從 **AggregationTimeStamp** 減去 **AggregationDuration** 來決定。</span><span class="sxs-lookup"><span data-stu-id="58278-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="58278-119">這個屬性繼承自 **CIM \_ AggregationMetricValue**。</span><span class="sxs-lookup"><span data-stu-id="58278-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="58278-120">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="58278-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-121">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="58278-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58278-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-123">識別套用彙總函式以判斷度量實例值的時間。</span><span class="sxs-lookup"><span data-stu-id="58278-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="58278-124">這與建立實例的時間不同。</span><span class="sxs-lookup"><span data-stu-id="58278-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="58278-125">針對指定的 **CIM \_ AggregationMetricValue** 實例，每當套用彙總函式來計算值時， **AggregationTimeStamp** 就會變更。</span><span class="sxs-lookup"><span data-stu-id="58278-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="58278-126">這個屬性繼承自 **CIM \_ AggregationMetricValue**。</span><span class="sxs-lookup"><span data-stu-id="58278-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="58278-127">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="58278-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-130">從關聯的 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)中定義的 **BreakdownDimensions** 陣列指定一個細目維度。</span><span class="sxs-lookup"><span data-stu-id="58278-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="58278-131">這是用來細分這組度量值的維度。</span><span class="sxs-lookup"><span data-stu-id="58278-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="58278-132">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-133">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="58278-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-136">定義為此度量值實例定義之 **BreakdownDimension** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="58278-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="58278-137">例如，如果 **BreakdownDimension** 是 "TransactionName"，則此屬性可以命名套用此特定度量值的實際交易。</span><span class="sxs-lookup"><span data-stu-id="58278-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="58278-138">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="58278-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="58278-142">A short description of the object.</span></span> <span data-ttu-id="58278-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-144">**說明**</span><span class="sxs-lookup"><span data-stu-id="58278-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-147">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="58278-147">A description of the object.</span></span> <span data-ttu-id="58278-148">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-149">**有效期間**</span><span class="sxs-lookup"><span data-stu-id="58278-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-150">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="58278-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58278-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-152">指定此度量值有效的持續時間。</span><span class="sxs-lookup"><span data-stu-id="58278-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="58278-153">這個屬性不應該存在於只套用至某個時間點的時間戳記，但應針對在特定 (期間內視為有效的值指定（例如，取樣) ）。</span><span class="sxs-lookup"><span data-stu-id="58278-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="58278-154">如果 **Duration** 屬性存在，而且不是 **Null**， **TimeStamp** 屬性會指定間隔的結尾。</span><span class="sxs-lookup"><span data-stu-id="58278-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="58278-155">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="58278-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-159">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="58278-159">A display name for the object.</span></span> <span data-ttu-id="58278-160">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58278-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58278-164">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="58278-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="58278-165">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="58278-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="58278-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-167">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="58278-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-170">度量值所屬專案的描述性名稱， (已測量的元素) 。</span><span class="sxs-lookup"><span data-stu-id="58278-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="58278-171">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="58278-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-175">此值之 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="58278-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="58278-176">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-177">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="58278-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="58278-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58278-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-180">以字串表示的度量值。</span><span class="sxs-lookup"><span data-stu-id="58278-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="58278-181">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-182">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="58278-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-183">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="58278-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58278-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-185">指定捕獲或計算度量值的時間。</span><span class="sxs-lookup"><span data-stu-id="58278-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="58278-186">請注意，這與建立實例的時間不同。</span><span class="sxs-lookup"><span data-stu-id="58278-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="58278-187">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58278-188">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="58278-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58278-189">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="58278-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58278-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="58278-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58278-191">如果下一個時間點的值將使用相同的類別實例，而且只是變更屬性值 (例如 **值** 或 **時間戳記**) ，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="58278-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="58278-192">若 **為 True**，則會重複使用此實例。</span><span class="sxs-lookup"><span data-stu-id="58278-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="58278-193">如果 **為 False**，則現有的實例會維持不變，並為新的時間點建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="58278-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="58278-194">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="58278-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58278-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="58278-195">Requirements</span></span>



| <span data-ttu-id="58278-196">需求</span><span class="sxs-lookup"><span data-stu-id="58278-196">Requirement</span></span> | <span data-ttu-id="58278-197">值</span><span class="sxs-lookup"><span data-stu-id="58278-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58278-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58278-198">Minimum supported client</span></span><br/> | <span data-ttu-id="58278-199">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58278-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58278-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58278-200">Minimum supported server</span></span><br/> | <span data-ttu-id="58278-201">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58278-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58278-202">命名空間</span><span class="sxs-lookup"><span data-stu-id="58278-202">Namespace</span></span><br/>                | <span data-ttu-id="58278-203">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="58278-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58278-204">MOF</span><span class="sxs-lookup"><span data-stu-id="58278-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58278-205"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="58278-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58278-206">DLL</span><span class="sxs-lookup"><span data-stu-id="58278-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58278-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58278-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


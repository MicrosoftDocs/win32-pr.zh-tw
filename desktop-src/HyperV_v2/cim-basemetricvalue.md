---
description: 表示度量的實例值。
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944853"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="ce2fd-103">CIM \_ BaseMetricValue 類別</span><span class="sxs-lookup"><span data-stu-id="ce2fd-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="ce2fd-104">表示度量的實例值。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce2fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce2fd-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="ce2fd-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce2fd-106">Members</span></span>

<span data-ttu-id="ce2fd-107">**CIM \_ BaseMetricValue** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ce2fd-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="ce2fd-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ce2fd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce2fd-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ce2fd-109">Properties</span></span>

<span data-ttu-id="ce2fd-110">**CIM \_ BaseMetricValue** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce2fd-111">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-114">根據相關聯之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)物件的 **BreakdownDimensions** 屬性，將這組度量值細分為的維度。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-115">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-118">針對這個實例值所定義之 **BreakdownDimension** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="ce2fd-119">例如，如果 **BreakdownDimension** 包含 "TransactionName"，則此屬性可以命名套用此特定度量值的實際交易。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-120">**有效期間**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-121">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-123">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**"，"**CIM \_ BaseMetricValue**.**TimeStamp**") </span><span class="sxs-lookup"><span data-stu-id="ce2fd-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-124">此度量值有效的持續時間。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="ce2fd-125">這個屬性不應該存在於只適用于某個時間點的時間戳記，但應針對在特定時間週期內視為有效的值來定義 (例如，</span><span class="sxs-lookup"><span data-stu-id="ce2fd-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="ce2fd-126">取樣) 。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-126">sampling).</span></span> <span data-ttu-id="ce2fd-127">如果 **Duration** 屬性存在且為非 Null，則 **時間戳記** 值應為間隔的結尾。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-131">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="ce2fd-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-132">在包含的命名空間範圍內唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ce2fd-133">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="ce2fd-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="ce2fd-134">*OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="ce2fd-135">此模式類似于架構類別名稱的結構。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="ce2fd-136">此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="ce2fd-137">因此， *OrgID* 不能包含冒號 ( '： ' ) 。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="ce2fd-138">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="ce2fd-139">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="ce2fd-140">若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce2fd-141">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-144">度量測量之元素的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="ce2fd-145">如果計量定義未與 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件相關聯，而且可在其他情況下用來提供補充資訊，則需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="ce2fd-146">這可讓您獨立于任何 **CIM \_ ManagedElement** 物件之外捕獲計量。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="ce2fd-147">如果有多個 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件與計量值相關聯，您可以選擇其中一個受控元素來建立度量的補充資訊。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="ce2fd-148">屬性並非用來做為用來查詢測量元素的外鍵。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="ce2fd-149">相反地，應該使用與 **CIM \_ ManagedElement** 的關聯。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-153">限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**識別碼**") </span><span class="sxs-lookup"><span data-stu-id="ce2fd-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-154">與這個實例值相關聯之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-155">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-158">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce2fd-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-159">度量值的字串表示。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-159">A string representation of the metric value.</span></span> <span data-ttu-id="ce2fd-160">度量值的原始資料類型會在相關聯的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 物件中指定。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-161">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-164">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**"，"**CIM \_ BaseMetricValue**.**Duration**") </span><span class="sxs-lookup"><span data-stu-id="ce2fd-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-165">計算度量實例值的時間。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="ce2fd-166">這與建立實例的時間不同。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="ce2fd-167">如果 **Volatile** 屬性為 true，則會在每次建立新的度量快照時變更此值。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="ce2fd-168">管理應用程式可以藉由抓取 **CIM \_ BaseMetricValue** 的實例，並根據其 **時間戳記** 值進行排序，來建立計量資料的時間序列。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="ce2fd-169">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2fd-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce2fd-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ce2fd-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce2fd-172">如果每次計量實例的值變更時， **時間戳記** 值變更，則為 True。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="ce2fd-173">如果這個物件必須保持不變，並為新的 **時間戳記** 值建立新的物件，則為 False。</span><span class="sxs-lookup"><span data-stu-id="ce2fd-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce2fd-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce2fd-174">Requirements</span></span>



| <span data-ttu-id="ce2fd-175">需求</span><span class="sxs-lookup"><span data-stu-id="ce2fd-175">Requirement</span></span> | <span data-ttu-id="ce2fd-176">值</span><span class="sxs-lookup"><span data-stu-id="ce2fd-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2fd-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce2fd-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2fd-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ce2fd-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ce2fd-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce2fd-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2fd-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce2fd-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ce2fd-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce2fd-181">Namespace</span></span><br/>                | <span data-ttu-id="ce2fd-182">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ce2fd-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ce2fd-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ce2fd-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce2fd-184"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ce2fd-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce2fd-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ce2fd-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce2fd-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ce2fd-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ce2fd-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce2fd-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2fd-188">**CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="ce2fd-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 


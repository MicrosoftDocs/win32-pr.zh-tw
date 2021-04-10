---
description: 表示 Msvm BaseMetricDefinition 類別的實例所定義的度量值 \_ 。
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851859"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="36ba2-103">Msvm \_ BaseMetricValue 類別</span><span class="sxs-lookup"><span data-stu-id="36ba2-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="36ba2-104">表示 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 類別的實例所定義的度量值。</span><span class="sxs-lookup"><span data-stu-id="36ba2-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="36ba2-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="36ba2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ba2-106">語法</span><span class="sxs-lookup"><span data-stu-id="36ba2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a><span data-ttu-id="36ba2-107">成員</span><span class="sxs-lookup"><span data-stu-id="36ba2-107">Members</span></span>

<span data-ttu-id="36ba2-108">**Msvm \_ BaseMetricValue** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36ba2-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="36ba2-109">屬性</span><span class="sxs-lookup"><span data-stu-id="36ba2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36ba2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="36ba2-110">Properties</span></span>

<span data-ttu-id="36ba2-111">**Msvm \_ BaseMetricValue** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="36ba2-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36ba2-112">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="36ba2-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-115">從關聯的 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)中定義的 **BreakdownDimensions** 陣列指定一個細目維度。</span><span class="sxs-lookup"><span data-stu-id="36ba2-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="36ba2-116">這是用來細分這組度量值的維度。</span><span class="sxs-lookup"><span data-stu-id="36ba2-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="36ba2-117">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-118">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="36ba2-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-121">定義為此度量值實例定義之 **BreakdownDimension** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="36ba2-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="36ba2-122">例如，如果 **BreakdownDimension** 是 "TransactionName"，則此屬性可以命名套用此特定度量值的實際交易。</span><span class="sxs-lookup"><span data-stu-id="36ba2-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="36ba2-123">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="36ba2-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-127">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="36ba2-127">A short description of the object.</span></span> <span data-ttu-id="36ba2-128">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-129">**說明**</span><span class="sxs-lookup"><span data-stu-id="36ba2-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-132">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="36ba2-132">A description of the object.</span></span> <span data-ttu-id="36ba2-133">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-134">**有效期間**</span><span class="sxs-lookup"><span data-stu-id="36ba2-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="36ba2-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-137">指定此度量值有效的持續時間。</span><span class="sxs-lookup"><span data-stu-id="36ba2-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="36ba2-138">這個屬性不應該存在於只套用至某個時間點的時間戳記，但應針對在特定 (期間內視為有效的值指定（例如，取樣) ）。</span><span class="sxs-lookup"><span data-stu-id="36ba2-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="36ba2-139">如果 **Duration** 屬性存在，而且不是 **Null**， **TimeStamp** 屬性會指定間隔的結尾。</span><span class="sxs-lookup"><span data-stu-id="36ba2-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="36ba2-140">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="36ba2-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-144">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="36ba2-144">A display name for the object.</span></span> <span data-ttu-id="36ba2-145">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="36ba2-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-149">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="36ba2-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-150">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="36ba2-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="36ba2-151">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-152">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="36ba2-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-155">度量值所屬專案的描述性名稱， (已測量的元素) 。</span><span class="sxs-lookup"><span data-stu-id="36ba2-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="36ba2-156">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="36ba2-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-160">此值之 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="36ba2-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="36ba2-161">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-162">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="36ba2-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="36ba2-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-165">以字串表示的度量值。</span><span class="sxs-lookup"><span data-stu-id="36ba2-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="36ba2-166">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-167">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="36ba2-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-168">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="36ba2-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-170">指定捕獲或計算度量值的時間。</span><span class="sxs-lookup"><span data-stu-id="36ba2-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="36ba2-171">請注意，這與建立實例的時間不同。</span><span class="sxs-lookup"><span data-stu-id="36ba2-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="36ba2-172">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="36ba2-173">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="36ba2-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36ba2-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="36ba2-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36ba2-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="36ba2-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36ba2-176">如果下一個時間點的值將使用相同的類別實例，而且只是變更屬性值 (例如 **值** 或 **時間戳記**) ，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="36ba2-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="36ba2-177">若 **為 True**，則會重複使用此實例。</span><span class="sxs-lookup"><span data-stu-id="36ba2-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="36ba2-178">如果 **為 False**，則現有的實例會維持不變，並為新的時間點建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="36ba2-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="36ba2-179">這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="36ba2-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36ba2-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="36ba2-180">Requirements</span></span>



| <span data-ttu-id="36ba2-181">需求</span><span class="sxs-lookup"><span data-stu-id="36ba2-181">Requirement</span></span> | <span data-ttu-id="36ba2-182">值</span><span class="sxs-lookup"><span data-stu-id="36ba2-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ba2-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36ba2-183">Minimum supported client</span></span><br/> | <span data-ttu-id="36ba2-184">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36ba2-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="36ba2-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36ba2-185">Minimum supported server</span></span><br/> | <span data-ttu-id="36ba2-186">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36ba2-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36ba2-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="36ba2-187">Namespace</span></span><br/>                | <span data-ttu-id="36ba2-188">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="36ba2-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="36ba2-189">MOF</span><span class="sxs-lookup"><span data-stu-id="36ba2-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36ba2-190"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="36ba2-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36ba2-191">DLL</span><span class="sxs-lookup"><span data-stu-id="36ba2-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36ba2-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36ba2-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


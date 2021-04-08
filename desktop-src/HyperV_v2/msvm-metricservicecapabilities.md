---
description: 描述相關聯 Msvm \_ MetricService 實例的功能。
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852384"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="ddb52-103">Msvm \_ MetricServiceCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="ddb52-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="ddb52-104">描述相關聯 [**Msvm \_ MetricService**](msvm-metricservice.md) 實例的功能。</span><span class="sxs-lookup"><span data-stu-id="ddb52-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="ddb52-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ddb52-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb52-106">語法</span><span class="sxs-lookup"><span data-stu-id="ddb52-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="ddb52-107">成員</span><span class="sxs-lookup"><span data-stu-id="ddb52-107">Members</span></span>

<span data-ttu-id="ddb52-108">**Msvm \_ MetricServiceCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ddb52-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ddb52-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ddb52-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddb52-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ddb52-110">Properties</span></span>

<span data-ttu-id="ddb52-111">**Msvm \_ MetricServiceCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ddb52-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddb52-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="ddb52-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ddb52-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ddb52-115">A short description of the object.</span></span> <span data-ttu-id="ddb52-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="ddb52-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="ddb52-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-120">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="ddb52-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-121">識別可由相關聯的 **cim \_ MetricService** 實例控制的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)實例。</span><span class="sxs-lookup"><span data-stu-id="ddb52-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="ddb52-122">如果此屬性為 **Null**，則可以控制所有元素。</span><span class="sxs-lookup"><span data-stu-id="ddb52-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="ddb52-123">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="ddb52-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-125">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-127">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="ddb52-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-128">識別可由相關聯的 **cim \_ MetricService** 實例控制的 **cim \_ BaseMetricDefinition** 實例。</span><span class="sxs-lookup"><span data-stu-id="ddb52-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="ddb52-129">如果此屬性為 **Null**，則可以控制所有計量。</span><span class="sxs-lookup"><span data-stu-id="ddb52-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="ddb52-130">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="ddb52-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ddb52-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-134">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ddb52-134">A description of the object.</span></span> <span data-ttu-id="ddb52-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「定義 Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="ddb52-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ddb52-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ddb52-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-139">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ddb52-139">A display name for the object.</span></span> <span data-ttu-id="ddb52-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="ddb52-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="ddb52-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ddb52-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-144">指出是否可以修改 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ddb52-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="ddb52-145">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="ddb52-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ddb52-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-149">指定 **ElementName** 的限制，以正則運算式表示。</span><span class="sxs-lookup"><span data-stu-id="ddb52-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="ddb52-150">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ddb52-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ddb52-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-154">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ddb52-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-155">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ddb52-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ddb52-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ddb52-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="ddb52-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-158">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-160">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="ddb52-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-161">針對 **ControllableManagedElements** 屬性中位於相同陣列索引的值所識別的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)物件，識別相關聯的 **cim \_ MetricService** 實例所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="ddb52-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="ddb52-162">如果此屬性為 **Null**，則支援所有控制項類型。</span><span class="sxs-lookup"><span data-stu-id="ddb52-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="ddb52-163">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ddb52-164">值</span><span class="sxs-lookup"><span data-stu-id="ddb52-164">Value</span></span>                                                                                   | <span data-ttu-id="ddb52-165">意義</span><span class="sxs-lookup"><span data-stu-id="ddb52-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="ddb52-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="ddb52-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="ddb52-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="ddb52-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ddb52-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="ddb52-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="ddb52-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ddb52-171">大量</span><span class="sxs-lookup"><span data-stu-id="ddb52-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="ddb52-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ddb52-173">兩者</span><span class="sxs-lookup"><span data-stu-id="ddb52-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="ddb52-174"><dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="ddb52-175">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="ddb52-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="ddb52-176"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ddb52-177">特定廠商</span><span class="sxs-lookup"><span data-stu-id="ddb52-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddb52-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="ddb52-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-179">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="ddb52-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-181">限定詞： **int32.maxvalue** (256) </span><span class="sxs-lookup"><span data-stu-id="ddb52-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-182">指定 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="ddb52-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="ddb52-183">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ddb52-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="ddb52-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-185">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-187">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="ddb52-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-188">識別 **ControllableMetrics** 屬性中相同陣列索引的值所識別之 **cim \_ BaseMetricDefinition** 的相關 **cim \_ MetricService** 實例所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="ddb52-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="ddb52-189">如果此屬性為 **Null**，則支援所有控制項類型。</span><span class="sxs-lookup"><span data-stu-id="ddb52-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="ddb52-190">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ddb52-191">值</span><span class="sxs-lookup"><span data-stu-id="ddb52-191">Value</span></span>                                                                                   | <span data-ttu-id="ddb52-192">意義</span><span class="sxs-lookup"><span data-stu-id="ddb52-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="ddb52-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="ddb52-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="ddb52-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="ddb52-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ddb52-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="ddb52-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="ddb52-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ddb52-198">大量</span><span class="sxs-lookup"><span data-stu-id="ddb52-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="ddb52-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ddb52-200">兩者</span><span class="sxs-lookup"><span data-stu-id="ddb52-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="ddb52-201"><dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="ddb52-202">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="ddb52-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="ddb52-203"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ddb52-204">特定廠商</span><span class="sxs-lookup"><span data-stu-id="ddb52-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddb52-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="ddb52-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-206">資料類型： **unit16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-208">指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="ddb52-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="ddb52-209">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="ddb52-210">值</span><span class="sxs-lookup"><span data-stu-id="ddb52-210">Value</span></span>                                                                         | <span data-ttu-id="ddb52-211">意義</span><span class="sxs-lookup"><span data-stu-id="ddb52-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="ddb52-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="ddb52-213">已啟用</span><span class="sxs-lookup"><span data-stu-id="ddb52-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="ddb52-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="ddb52-215">禁用</span><span class="sxs-lookup"><span data-stu-id="ddb52-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="ddb52-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="ddb52-217">關閉</span><span class="sxs-lookup"><span data-stu-id="ddb52-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="ddb52-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="ddb52-219">離線</span><span class="sxs-lookup"><span data-stu-id="ddb52-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="ddb52-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="ddb52-221">測試</span><span class="sxs-lookup"><span data-stu-id="ddb52-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="ddb52-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="ddb52-223">推遲</span><span class="sxs-lookup"><span data-stu-id="ddb52-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="ddb52-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="ddb52-225">靜止</span><span class="sxs-lookup"><span data-stu-id="ddb52-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="ddb52-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="ddb52-227">重新啟動</span><span class="sxs-lookup"><span data-stu-id="ddb52-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="ddb52-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="ddb52-229">重設</span><span class="sxs-lookup"><span data-stu-id="ddb52-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ddb52-230">**>supportedmethods**</span><span class="sxs-lookup"><span data-stu-id="ddb52-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddb52-231">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ddb52-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddb52-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ddb52-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddb52-233">指定度量服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="ddb52-234">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="ddb52-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="ddb52-235">值</span><span class="sxs-lookup"><span data-stu-id="ddb52-235">Value</span></span>                                                                                   | <span data-ttu-id="ddb52-236">意義</span><span class="sxs-lookup"><span data-stu-id="ddb52-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ddb52-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="ddb52-238">支援 [**ControlMetrics**](controlmetrics-msvm-metricservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="ddb52-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="ddb52-240">支援 **ControlMetricsByClass** 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ddb52-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="ddb52-242">支援 **ShowMetrics** 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="ddb52-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="ddb52-244">支援 **ShowMetricsByClass** 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ddb52-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="ddb52-246">支援 **GetMetricValues** 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ddb52-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="ddb52-248">支援 **ControlSampleTimes** 方法。</span><span class="sxs-lookup"><span data-stu-id="ddb52-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ddb52-249"><dt>8. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="ddb52-250">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="ddb52-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="ddb52-251"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="ddb52-252">特定廠商</span><span class="sxs-lookup"><span data-stu-id="ddb52-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddb52-253">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddb52-253">Requirements</span></span>



| <span data-ttu-id="ddb52-254">需求</span><span class="sxs-lookup"><span data-stu-id="ddb52-254">Requirement</span></span> | <span data-ttu-id="ddb52-255">值</span><span class="sxs-lookup"><span data-stu-id="ddb52-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb52-256">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ddb52-256">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb52-257">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddb52-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ddb52-258">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ddb52-258">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb52-259">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddb52-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ddb52-260">命名空間</span><span class="sxs-lookup"><span data-stu-id="ddb52-260">Namespace</span></span><br/>                | <span data-ttu-id="ddb52-261">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ddb52-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ddb52-262">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb52-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb52-263"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb52-264">DLL</span><span class="sxs-lookup"><span data-stu-id="ddb52-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb52-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ddb52-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ddb52-266">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddb52-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb52-267">**CIM \_ MetricServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ddb52-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="ddb52-268">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="ddb52-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 


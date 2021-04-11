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
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="bd5dd-103">Msvm \_ MetricServiceCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="bd5dd-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="bd5dd-104">描述相關聯 [**Msvm \_ MetricService**](msvm-metricservice.md) 實例的功能。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="bd5dd-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5dd-106">語法</span><span class="sxs-lookup"><span data-stu-id="bd5dd-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bd5dd-107">成員</span><span class="sxs-lookup"><span data-stu-id="bd5dd-107">Members</span></span>

<span data-ttu-id="bd5dd-108">**Msvm \_ MetricServiceCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bd5dd-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="bd5dd-109">屬性</span><span class="sxs-lookup"><span data-stu-id="bd5dd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd5dd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bd5dd-110">Properties</span></span>

<span data-ttu-id="bd5dd-111">**Msvm \_ MetricServiceCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd5dd-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-115">A short description of the object.</span></span> <span data-ttu-id="bd5dd-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-118">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-120">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="bd5dd-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-121">識別可由相關聯的 **cim \_ MetricService** 實例控制的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)實例。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="bd5dd-122">如果此屬性為 **Null**，則可以控制所有元素。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="bd5dd-123">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-125">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-127">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="bd5dd-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-128">識別可由相關聯的 **cim \_ MetricService** 實例控制的 **cim \_ BaseMetricDefinition** 實例。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="bd5dd-129">如果此屬性為 **Null**，則可以控制所有計量。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="bd5dd-130">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-134">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-134">A description of the object.</span></span> <span data-ttu-id="bd5dd-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「定義 Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-139">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-139">A display name for the object.</span></span> <span data-ttu-id="bd5dd-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-144">指出是否可以修改 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="bd5dd-145">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-149">指定 **ElementName** 的限制，以正則運算式表示。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="bd5dd-150">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-154">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-155">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bd5dd-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-158">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-160">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="bd5dd-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-161">針對 **ControllableManagedElements** 屬性中位於相同陣列索引的值所識別的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)物件，識別相關聯的 **cim \_ MetricService** 實例所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="bd5dd-162">如果此屬性為 **Null**，則支援所有控制項類型。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="bd5dd-163">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="bd5dd-164">值</span><span class="sxs-lookup"><span data-stu-id="bd5dd-164">Value</span></span>                                                                                   | <span data-ttu-id="bd5dd-165">意義</span><span class="sxs-lookup"><span data-stu-id="bd5dd-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="bd5dd-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="bd5dd-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="bd5dd-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="bd5dd-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="bd5dd-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-171">大量</span><span class="sxs-lookup"><span data-stu-id="bd5dd-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="bd5dd-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-173">兩者</span><span class="sxs-lookup"><span data-stu-id="bd5dd-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="bd5dd-174"><dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="bd5dd-175">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="bd5dd-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="bd5dd-176"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="bd5dd-177">特定廠商</span><span class="sxs-lookup"><span data-stu-id="bd5dd-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd5dd-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-179">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-181">限定詞： **int32.maxvalue** (256) </span><span class="sxs-lookup"><span data-stu-id="bd5dd-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-182">指定 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="bd5dd-183">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bd5dd-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-185">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-187">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="bd5dd-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-188">識別 **ControllableMetrics** 屬性中相同陣列索引的值所識別之 **cim \_ BaseMetricDefinition** 的相關 **cim \_ MetricService** 實例所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="bd5dd-189">如果此屬性為 **Null**，則支援所有控制項類型。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="bd5dd-190">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="bd5dd-191">值</span><span class="sxs-lookup"><span data-stu-id="bd5dd-191">Value</span></span>                                                                                   | <span data-ttu-id="bd5dd-192">意義</span><span class="sxs-lookup"><span data-stu-id="bd5dd-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="bd5dd-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="bd5dd-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="bd5dd-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="bd5dd-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="bd5dd-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-198">大量</span><span class="sxs-lookup"><span data-stu-id="bd5dd-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="bd5dd-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-200">兩者</span><span class="sxs-lookup"><span data-stu-id="bd5dd-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="bd5dd-201"><dt>5. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="bd5dd-202">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="bd5dd-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="bd5dd-203"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="bd5dd-204">特定廠商</span><span class="sxs-lookup"><span data-stu-id="bd5dd-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd5dd-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-206">資料類型： **unit16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-208">指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="bd5dd-209">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="bd5dd-210">值</span><span class="sxs-lookup"><span data-stu-id="bd5dd-210">Value</span></span>                                                                         | <span data-ttu-id="bd5dd-211">意義</span><span class="sxs-lookup"><span data-stu-id="bd5dd-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="bd5dd-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-213">已啟用</span><span class="sxs-lookup"><span data-stu-id="bd5dd-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="bd5dd-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-215">禁用</span><span class="sxs-lookup"><span data-stu-id="bd5dd-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="bd5dd-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-217">關閉</span><span class="sxs-lookup"><span data-stu-id="bd5dd-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="bd5dd-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-219">離線</span><span class="sxs-lookup"><span data-stu-id="bd5dd-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="bd5dd-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-221">測試</span><span class="sxs-lookup"><span data-stu-id="bd5dd-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="bd5dd-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-223">推遲</span><span class="sxs-lookup"><span data-stu-id="bd5dd-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="bd5dd-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="bd5dd-225">靜止</span><span class="sxs-lookup"><span data-stu-id="bd5dd-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="bd5dd-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="bd5dd-227">重新啟動</span><span class="sxs-lookup"><span data-stu-id="bd5dd-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="bd5dd-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="bd5dd-229">重設</span><span class="sxs-lookup"><span data-stu-id="bd5dd-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="bd5dd-230">**>supportedmethods**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5dd-231">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bd5dd-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd5dd-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd5dd-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd5dd-233">指定度量服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="bd5dd-234">這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="bd5dd-235">值</span><span class="sxs-lookup"><span data-stu-id="bd5dd-235">Value</span></span>                                                                                   | <span data-ttu-id="bd5dd-236">意義</span><span class="sxs-lookup"><span data-stu-id="bd5dd-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd5dd-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-238">支援 [**ControlMetrics**](controlmetrics-msvm-metricservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="bd5dd-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-240">支援 **ControlMetricsByClass** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bd5dd-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-242">支援 **ShowMetrics** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="bd5dd-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-244">支援 **ShowMetricsByClass** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="bd5dd-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-246">支援 **GetMetricValues** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="bd5dd-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="bd5dd-248">支援 **ControlSampleTimes** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd5dd-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="bd5dd-249"><dt>8. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="bd5dd-250">已保留 DMTF</span><span class="sxs-lookup"><span data-stu-id="bd5dd-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="bd5dd-251"><dt>32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="bd5dd-252">特定廠商</span><span class="sxs-lookup"><span data-stu-id="bd5dd-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd5dd-253">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd5dd-253">Requirements</span></span>



| <span data-ttu-id="bd5dd-254">需求</span><span class="sxs-lookup"><span data-stu-id="bd5dd-254">Requirement</span></span> | <span data-ttu-id="bd5dd-255">值</span><span class="sxs-lookup"><span data-stu-id="bd5dd-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5dd-256">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd5dd-256">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5dd-257">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5dd-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd5dd-258">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd5dd-258">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5dd-259">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5dd-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd5dd-260">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd5dd-260">Namespace</span></span><br/>                | <span data-ttu-id="bd5dd-261">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bd5dd-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bd5dd-262">MOF</span><span class="sxs-lookup"><span data-stu-id="bd5dd-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd5dd-263"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd5dd-264">DLL</span><span class="sxs-lookup"><span data-stu-id="bd5dd-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd5dd-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd5dd-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd5dd-266">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd5dd-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5dd-267">**CIM \_ MetricServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="bd5dd-268">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="bd5dd-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 


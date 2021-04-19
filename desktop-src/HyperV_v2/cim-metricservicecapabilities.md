---
description: 描述 CIM MetricService 物件的功能 \_ 。
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997147"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="55800-103">CIM \_ MetricServiceCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="55800-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="55800-104">描述 [**CIM \_ MetricService**](cim-metricservice.md) 物件的功能。</span><span class="sxs-lookup"><span data-stu-id="55800-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="55800-105">語法</span><span class="sxs-lookup"><span data-stu-id="55800-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="55800-106">成員</span><span class="sxs-lookup"><span data-stu-id="55800-106">Members</span></span>

<span data-ttu-id="55800-107">**CIM \_ MetricServiceCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="55800-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="55800-108">屬性</span><span class="sxs-lookup"><span data-stu-id="55800-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55800-109">屬性</span><span class="sxs-lookup"><span data-stu-id="55800-109">Properties</span></span>

<span data-ttu-id="55800-110">**CIM \_ MetricServiceCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="55800-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55800-111">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="55800-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55800-112">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="55800-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55800-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55800-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55800-114">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MetricServiceCapabilities**。**ManagedElementControlTypes**") </span><span class="sxs-lookup"><span data-stu-id="55800-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="55800-115">陣列，其中包含由計量服務控制之 [**CIM \_ ManagedElement**](cim-managedelement.md) 實例的識別碼。</span><span class="sxs-lookup"><span data-stu-id="55800-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="55800-116">識別碼必須格式化為 Web-Based Enterprise Management (WBEM) Uri。</span><span class="sxs-lookup"><span data-stu-id="55800-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="55800-117">若要使用此屬性，計量服務必須支援啟用或停用至少一個針對 **CIM \_ ManagedElement** 實例定義的計量。</span><span class="sxs-lookup"><span data-stu-id="55800-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="55800-118">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="55800-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55800-119">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="55800-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55800-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55800-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55800-121">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MetricServiceCapabilities**。**MetricControlTypes**") </span><span class="sxs-lookup"><span data-stu-id="55800-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="55800-122">陣列，其中包含定義度量服務所管理之計量的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="55800-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="55800-123">識別碼必須格式化為 Web-Based Enterprise Management (WBEM) Uri。</span><span class="sxs-lookup"><span data-stu-id="55800-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="55800-124">若要使用這個屬性， [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例必須透過 [**Cim \_ ServiceAffectsElement**](cim-serviceaffectselement.md)類別與 [**cim \_ MetricService**](cim-metricservice.md)實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="55800-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="55800-125">此外，計量服務必須支援啟用或停用 **CIM \_ BaseMetricDefinition** 實例所定義的至少一個度量。</span><span class="sxs-lookup"><span data-stu-id="55800-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="55800-126">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="55800-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55800-127">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="55800-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55800-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55800-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55800-129">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MetricServiceCapabilities**。**ControllableManagedElements**") </span><span class="sxs-lookup"><span data-stu-id="55800-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="55800-130">陣列，指出 **ControllableManagedElements** 陣列中 managed 元素的度量服務所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="55800-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="55800-131">這個陣列對應于 **ControllableManagedElements** 陣列。</span><span class="sxs-lookup"><span data-stu-id="55800-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="55800-132">此陣列中的控制項類型會透過 **ControllableManagedElements** 陣列與計量相關聯。</span><span class="sxs-lookup"><span data-stu-id="55800-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55800-133">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="55800-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="55800-134">**離散** (2) </span><span class="sxs-lookup"><span data-stu-id="55800-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="55800-135">**大量** (3) </span><span class="sxs-lookup"><span data-stu-id="55800-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="55800-136">**(4**) </span><span class="sxs-lookup"><span data-stu-id="55800-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55800-137">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="55800-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="55800-138">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="55800-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55800-139">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="55800-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55800-140">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="55800-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55800-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55800-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55800-142">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ MetricServiceCapabilities**。**ControllableMetrics**") </span><span class="sxs-lookup"><span data-stu-id="55800-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="55800-143">陣列，表示度量服務所支援的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="55800-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="55800-144">這個陣列對應于 **ControllableMetrics** 陣列。</span><span class="sxs-lookup"><span data-stu-id="55800-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="55800-145">此陣列中的控制項類型會透過 **ControllableMetrics** 陣列與計量相關聯。</span><span class="sxs-lookup"><span data-stu-id="55800-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55800-146">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="55800-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="55800-147">**離散** (2) </span><span class="sxs-lookup"><span data-stu-id="55800-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="55800-148">**大量** (3) </span><span class="sxs-lookup"><span data-stu-id="55800-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="55800-149">**(4**) </span><span class="sxs-lookup"><span data-stu-id="55800-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55800-150">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="55800-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="55800-151">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="55800-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55800-152">**>supportedmethods**</span><span class="sxs-lookup"><span data-stu-id="55800-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55800-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="55800-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55800-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="55800-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55800-155">陣列，其中包含計量服務所支援之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="55800-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="55800-156">**ControlMetrics** (2) </span><span class="sxs-lookup"><span data-stu-id="55800-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="55800-157">**ControlMetricsByClass** (3) </span><span class="sxs-lookup"><span data-stu-id="55800-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="55800-158">**ShowMetrics** (4) </span><span class="sxs-lookup"><span data-stu-id="55800-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="55800-159">**ShowMetricsByClass** (5) </span><span class="sxs-lookup"><span data-stu-id="55800-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="55800-160">**GetMetricValues** (6) </span><span class="sxs-lookup"><span data-stu-id="55800-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="55800-161">**ControlSampleTimes** (7) </span><span class="sxs-lookup"><span data-stu-id="55800-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="55800-162">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="55800-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="55800-163">**特定供應商** (0x8000) </span><span class="sxs-lookup"><span data-stu-id="55800-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="55800-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="55800-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="55800-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="55800-165">Requirements</span></span>



| <span data-ttu-id="55800-166">需求</span><span class="sxs-lookup"><span data-stu-id="55800-166">Requirement</span></span> | <span data-ttu-id="55800-167">值</span><span class="sxs-lookup"><span data-stu-id="55800-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55800-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55800-168">Minimum supported client</span></span><br/> | <span data-ttu-id="55800-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="55800-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="55800-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55800-170">Minimum supported server</span></span><br/> | <span data-ttu-id="55800-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55800-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="55800-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="55800-172">Namespace</span></span><br/>                | <span data-ttu-id="55800-173">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="55800-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="55800-174">MOF</span><span class="sxs-lookup"><span data-stu-id="55800-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55800-175"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="55800-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55800-176">DLL</span><span class="sxs-lookup"><span data-stu-id="55800-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55800-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55800-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55800-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55800-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55800-179">**CIM \_ EnabledLogicalElementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55800-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 


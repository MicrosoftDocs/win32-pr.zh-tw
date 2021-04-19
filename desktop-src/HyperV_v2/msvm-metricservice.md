---
description: 提供管理計量的能力。
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Msvm_MetricService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982718"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="18042-103">Msvm \_ MetricService 類別</span><span class="sxs-lookup"><span data-stu-id="18042-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="18042-104">提供管理計量的能力。</span><span class="sxs-lookup"><span data-stu-id="18042-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="18042-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18042-106">語法</span><span class="sxs-lookup"><span data-stu-id="18042-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="18042-107">成員</span><span class="sxs-lookup"><span data-stu-id="18042-107">Members</span></span>

<span data-ttu-id="18042-108">**Msvm \_ MetricService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18042-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="18042-109">方法</span><span class="sxs-lookup"><span data-stu-id="18042-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="18042-110">屬性</span><span class="sxs-lookup"><span data-stu-id="18042-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18042-111">方法</span><span class="sxs-lookup"><span data-stu-id="18042-111">Methods</span></span>

<span data-ttu-id="18042-112">**Msvm \_ MetricService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="18042-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="18042-113">方法</span><span class="sxs-lookup"><span data-stu-id="18042-113">Method</span></span>                                                                    | <span data-ttu-id="18042-114">描述</span><span class="sxs-lookup"><span data-stu-id="18042-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="18042-115">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="18042-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="18042-116">用來控制 managed 元素或元素的計量集合。</span><span class="sxs-lookup"><span data-stu-id="18042-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="18042-117">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="18042-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="18042-118">依類別控制度量。</span><span class="sxs-lookup"><span data-stu-id="18042-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="18042-119">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="18042-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="18042-120">設定控制項取樣時間。</span><span class="sxs-lookup"><span data-stu-id="18042-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="18042-121">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="18042-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="18042-122">抓取度量值。</span><span class="sxs-lookup"><span data-stu-id="18042-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="18042-123">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="18042-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="18042-124">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="18042-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="18042-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="18042-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="18042-126">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="18042-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="18042-127">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="18042-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="18042-128">顯示指定的計量。</span><span class="sxs-lookup"><span data-stu-id="18042-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="18042-129">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="18042-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="18042-130">依類別顯示度量。</span><span class="sxs-lookup"><span data-stu-id="18042-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="18042-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="18042-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="18042-132">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="18042-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="18042-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="18042-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="18042-134">停止服務。</span><span class="sxs-lookup"><span data-stu-id="18042-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="18042-135">屬性</span><span class="sxs-lookup"><span data-stu-id="18042-135">Properties</span></span>

<span data-ttu-id="18042-136">**Msvm \_ MetricService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18042-137">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="18042-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-138">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18042-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18042-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-140">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="18042-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="18042-141">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18042-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18042-142">**標題**</span><span class="sxs-lookup"><span data-stu-id="18042-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-145">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="18042-145">A short description of the object.</span></span> <span data-ttu-id="18042-146">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「hyper-v 計量服務」。</span><span class="sxs-lookup"><span data-stu-id="18042-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="18042-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="18042-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-150">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="18042-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="18042-151">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18042-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18042-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18042-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18042-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18042-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18042-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18042-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="18042-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18042-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="18042-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18042-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="18042-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18042-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18042-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18042-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18042-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18042-160">)</span><span class="sxs-lookup"><span data-stu-id="18042-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18042-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18042-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-164">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="18042-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="18042-165">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ MetricService"。</span><span class="sxs-lookup"><span data-stu-id="18042-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="18042-166">**說明**</span><span class="sxs-lookup"><span data-stu-id="18042-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-169">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="18042-169">A description of the object.</span></span> <span data-ttu-id="18042-170">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「提供 hyper-v 計量 WMI 管理」。</span><span class="sxs-lookup"><span data-stu-id="18042-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="18042-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="18042-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-174">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18042-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="18042-175">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18042-176">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18042-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18042-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18042-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18042-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="18042-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18042-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="18042-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18042-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="18042-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18042-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="18042-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18042-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="18042-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18042-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18042-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18042-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18042-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18042-185">)</span><span class="sxs-lookup"><span data-stu-id="18042-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18042-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18042-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-189">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="18042-189">A display name for the object.</span></span> <span data-ttu-id="18042-190">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「hyper-v 計量服務」。</span><span class="sxs-lookup"><span data-stu-id="18042-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="18042-191">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="18042-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-194">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="18042-195">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="18042-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="18042-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="18042-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-199">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="18042-200">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="18042-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="18042-201">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="18042-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="18042-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="18042-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-205">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="18042-205">The current health of the element.</span></span> <span data-ttu-id="18042-206">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="18042-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="18042-207">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="18042-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="18042-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="18042-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="18042-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18042-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-210">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18042-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18042-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-212">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="18042-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="18042-213">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18042-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18042-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18042-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18042-217">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="18042-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18042-218">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="18042-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18042-219">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18042-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18042-220">**名稱**</span><span class="sxs-lookup"><span data-stu-id="18042-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-223">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="18042-223">The label by which the object is known.</span></span> <span data-ttu-id="18042-224">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "metricsvc"。</span><span class="sxs-lookup"><span data-stu-id="18042-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="18042-225">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="18042-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-226">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-228">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18042-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="18042-229">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18042-230">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18042-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18042-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18042-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18042-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18042-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18042-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="18042-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18042-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="18042-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18042-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="18042-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18042-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="18042-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18042-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="18042-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="18042-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="18042-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="18042-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="18042-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="18042-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="18042-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="18042-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="18042-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="18042-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="18042-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="18042-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="18042-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="18042-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="18042-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="18042-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="18042-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="18042-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="18042-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="18042-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="18042-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="18042-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18042-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18042-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18042-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18042-250">)</span><span class="sxs-lookup"><span data-stu-id="18042-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18042-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="18042-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-252">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18042-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18042-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-254">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-254">The current statuses of the object.</span></span> <span data-ttu-id="18042-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="18042-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="18042-256">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="18042-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-259">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="18042-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="18042-260">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="18042-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="18042-261">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18042-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18042-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="18042-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-265">值，提供有關如何聯繫服務主要擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="18042-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="18042-266">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18042-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18042-267">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="18042-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-270">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="18042-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="18042-271">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="18042-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="18042-272">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18042-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18042-273">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="18042-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-274">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-276">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="18042-276">Provides high level status information.</span></span> <span data-ttu-id="18042-277">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="18042-278">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18042-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18042-279">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18042-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18042-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18042-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18042-281"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="18042-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18042-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="18042-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18042-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="18042-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18042-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18042-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18042-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18042-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18042-286">)</span><span class="sxs-lookup"><span data-stu-id="18042-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18042-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="18042-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-288">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-290">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="18042-291">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="18042-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="18042-292">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="18042-293">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="18042-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="18042-294">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="18042-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="18042-295">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="18042-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="18042-296">**已開始**</span><span class="sxs-lookup"><span data-stu-id="18042-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18042-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18042-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-299">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="18042-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="18042-300">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="18042-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="18042-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="18042-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-304">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="18042-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="18042-305">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18042-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18042-306">**狀態**</span><span class="sxs-lookup"><span data-stu-id="18042-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-309">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="18042-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="18042-310">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18042-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-311">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="18042-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18042-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-313">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="18042-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="18042-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，字串一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="18042-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="18042-315">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18042-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-318">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="18042-318">The scoping system's creation class name.</span></span> <span data-ttu-id="18042-319">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="18042-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="18042-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18042-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18042-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18042-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-323">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="18042-323">The name of the hosting computer system.</span></span> <span data-ttu-id="18042-324">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="18042-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="18042-325">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="18042-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-326">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18042-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18042-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-328">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="18042-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="18042-329">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18042-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18042-330">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="18042-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18042-331">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18042-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18042-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18042-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18042-333">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="18042-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="18042-334">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18042-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18042-335">規格需求</span><span class="sxs-lookup"><span data-stu-id="18042-335">Requirements</span></span>



| <span data-ttu-id="18042-336">需求</span><span class="sxs-lookup"><span data-stu-id="18042-336">Requirement</span></span> | <span data-ttu-id="18042-337">值</span><span class="sxs-lookup"><span data-stu-id="18042-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18042-338">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18042-338">Minimum supported client</span></span><br/> | <span data-ttu-id="18042-339">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18042-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18042-340">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18042-340">Minimum supported server</span></span><br/> | <span data-ttu-id="18042-341">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18042-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18042-342">命名空間</span><span class="sxs-lookup"><span data-stu-id="18042-342">Namespace</span></span><br/>                | <span data-ttu-id="18042-343">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="18042-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18042-344">MOF</span><span class="sxs-lookup"><span data-stu-id="18042-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18042-345"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18042-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18042-346">DLL</span><span class="sxs-lookup"><span data-stu-id="18042-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18042-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18042-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


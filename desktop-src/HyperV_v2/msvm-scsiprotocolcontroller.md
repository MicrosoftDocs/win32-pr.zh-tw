---
description: 代表綜合 SCSI 控制器。
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Msvm_SCSIProtocolController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514252"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="4ad8b-103">Msvm \_ SCSIProtocolController 類別</span><span class="sxs-lookup"><span data-stu-id="4ad8b-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="4ad8b-104">代表綜合 SCSI 控制器。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="4ad8b-105">綜合 SCSI 控制器最多可支援256個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="4ad8b-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad8b-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ad8b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SCSIProtocolController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="4ad8b-108">成員</span><span class="sxs-lookup"><span data-stu-id="4ad8b-108">Members</span></span>

<span data-ttu-id="4ad8b-109">**Msvm \_ SCSIProtocolController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4ad8b-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="4ad8b-110">方法</span><span class="sxs-lookup"><span data-stu-id="4ad8b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4ad8b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad8b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4ad8b-112">方法</span><span class="sxs-lookup"><span data-stu-id="4ad8b-112">Methods</span></span>

<span data-ttu-id="4ad8b-113">**Msvm \_ SCSIProtocolController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="4ad8b-114">方法</span><span class="sxs-lookup"><span data-stu-id="4ad8b-114">Method</span></span>                                                                       | <span data-ttu-id="4ad8b-115">描述</span><span class="sxs-lookup"><span data-stu-id="4ad8b-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="4ad8b-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="4ad8b-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ad8b-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="4ad8b-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ad8b-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="4ad8b-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="4ad8b-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="4ad8b-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="4ad8b-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="4ad8b-125">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="4ad8b-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="4ad8b-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ad8b-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="4ad8b-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4ad8b-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="4ad8b-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4ad8b-132">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad8b-132">Properties</span></span>

<span data-ttu-id="4ad8b-133">**Msvm \_ SCSIProtocolController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ad8b-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-135">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-137">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="4ad8b-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="4ad8b-139">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-139">Value</span></span>                                                                            | <span data-ttu-id="4ad8b-140">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4ad8b-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="4ad8b-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="4ad8b-143">不適用</span><span class="sxs-lookup"><span data-stu-id="4ad8b-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-144">**可用性**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-147">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-147">The primary availability and status of the device.</span></span> <span data-ttu-id="4ad8b-148">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="4ad8b-149">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-149">Value</span></span>                                                                        | <span data-ttu-id="4ad8b-150">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4ad8b-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="4ad8b-152">不適用</span><span class="sxs-lookup"><span data-stu-id="4ad8b-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-153">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-154">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-156">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4ad8b-157">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-158">**標題**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-161">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-161">A short description of the object.</span></span> <span data-ttu-id="4ad8b-162">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-166">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4ad8b-167">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ad8b-168">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ad8b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ad8b-176">)</span><span class="sxs-lookup"><span data-stu-id="4ad8b-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ad8b-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-180">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4ad8b-181">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-182">**說明**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-185">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-185">A description of the object.</span></span> <span data-ttu-id="4ad8b-186">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-190">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4ad8b-191">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ad8b-192">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ad8b-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ad8b-201">)</span><span class="sxs-lookup"><span data-stu-id="4ad8b-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ad8b-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-205">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-209">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-209">A display name for the object.</span></span> <span data-ttu-id="4ad8b-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-214">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4ad8b-215">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4ad8b-216">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-216">Value</span></span>                                                                        | <span data-ttu-id="4ad8b-217">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4ad8b-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4ad8b-219">已啟用</span><span class="sxs-lookup"><span data-stu-id="4ad8b-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-223">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4ad8b-224">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4ad8b-225">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4ad8b-226">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-226">Value</span></span>                                                                        | <span data-ttu-id="4ad8b-227">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4ad8b-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="4ad8b-229">不適用</span><span class="sxs-lookup"><span data-stu-id="4ad8b-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-233">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="4ad8b-234">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-238">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="4ad8b-239">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-243">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-243">The current health of the element.</span></span> <span data-ttu-id="4ad8b-244">這表示此元素的健全狀況，但不一定是其子元件的健康情況。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4ad8b-245">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4ad8b-246">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-248">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-250">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="4ad8b-251">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-253">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-255">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4ad8b-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-260">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-261">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4ad8b-262">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-266">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="4ad8b-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-271">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-271">This property has been deprecated.</span></span> <span data-ttu-id="4ad8b-272">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-273">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-274">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-276">可透過此通訊協定控制器控制或存取的單位數目上限。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="4ad8b-277">這個屬性繼承自 [**CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-278">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-281">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-281">The label by which the object is known.</span></span> <span data-ttu-id="4ad8b-282">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-284">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-286">識別如何選取 SCSI 通訊協定控制器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="4ad8b-287">這個屬性繼承自 [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="4ad8b-288">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-288">Value</span></span>                                                                        | <span data-ttu-id="4ad8b-289">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4ad8b-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="4ad8b-291">Unknown</span><span class="sxs-lookup"><span data-stu-id="4ad8b-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-292">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-293">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-295">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4ad8b-296">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ad8b-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ad8b-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ad8b-317">)</span><span class="sxs-lookup"><span data-stu-id="4ad8b-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ad8b-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-319">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-321">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-321">The current status of the object.</span></span> <span data-ttu-id="4ad8b-322">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="4ad8b-323">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-323">Value</span></span>                                                                            | <span data-ttu-id="4ad8b-324">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="4ad8b-325"><dt>二級</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="4ad8b-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="4ad8b-327">確定</span><span class="sxs-lookup"><span data-stu-id="4ad8b-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-328">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-331">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4ad8b-332">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4ad8b-333">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-335">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-337">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4ad8b-338">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-339">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-342">描述當 **NameFormat** 為 1 (其他) 時，如何識別通訊協定控制器的字串。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="4ad8b-343">這個屬性繼承自 [**CIM \_ SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-345">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-347">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-347">The power management capabilities of the device.</span></span> <span data-ttu-id="4ad8b-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-350">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-352">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4ad8b-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-355">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-357">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4ad8b-358">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-360">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-362">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-362">Provides high level status information.</span></span> <span data-ttu-id="4ad8b-363">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4ad8b-364">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4ad8b-365">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4ad8b-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-367"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4ad8b-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4ad8b-372">)</span><span class="sxs-lookup"><span data-stu-id="4ad8b-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ad8b-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-374">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-376">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="4ad8b-377">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4ad8b-378">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="4ad8b-379">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4ad8b-380">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-380">Value</span></span>                                                                         | <span data-ttu-id="4ad8b-381">意義</span><span class="sxs-lookup"><span data-stu-id="4ad8b-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4ad8b-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4ad8b-383">不適用</span><span class="sxs-lookup"><span data-stu-id="4ad8b-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ad8b-384">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-387">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-387">The current status of the object.</span></span> <span data-ttu-id="4ad8b-388">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-389">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-390">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4ad8b-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-392">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4ad8b-393">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-395">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-397">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-397">The current state of the logical device.</span></span> <span data-ttu-id="4ad8b-398">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-402">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-402">The scoping system's creation class name.</span></span> <span data-ttu-id="4ad8b-403">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-405">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-407">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="4ad8b-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-409">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-410">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-412">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4ad8b-413">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-414">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-415">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-417">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4ad8b-418">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4ad8b-419">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad8b-420">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad8b-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad8b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad8b-422">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4ad8b-423">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ad8b-424">備註</span><span class="sxs-lookup"><span data-stu-id="4ad8b-424">Remarks</span></span>

<span data-ttu-id="4ad8b-425">存取 **Msvm \_ SCSIProtocolController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4ad8b-426">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4ad8b-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad8b-427">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ad8b-427">Requirements</span></span>



| <span data-ttu-id="4ad8b-428">需求</span><span class="sxs-lookup"><span data-stu-id="4ad8b-428">Requirement</span></span> | <span data-ttu-id="4ad8b-429">值</span><span class="sxs-lookup"><span data-stu-id="4ad8b-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad8b-430">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ad8b-430">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad8b-431">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ad8b-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ad8b-432">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ad8b-432">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad8b-433">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ad8b-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ad8b-434">命名空間</span><span class="sxs-lookup"><span data-stu-id="4ad8b-434">Namespace</span></span><br/>                | <span data-ttu-id="4ad8b-435">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4ad8b-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ad8b-436">MOF</span><span class="sxs-lookup"><span data-stu-id="4ad8b-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ad8b-437"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ad8b-438">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad8b-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad8b-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ad8b-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ad8b-440">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ad8b-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad8b-441">**CIM \_ SCSIProtocolController**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="4ad8b-442">**CIM \_ SCSIProtocolController**</span><span class="sxs-lookup"><span data-stu-id="4ad8b-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="4ad8b-443">儲存類別</span><span class="sxs-lookup"><span data-stu-id="4ad8b-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


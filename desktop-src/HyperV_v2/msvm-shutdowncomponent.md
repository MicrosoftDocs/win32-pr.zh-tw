---
description: 代表關機服務的狀態，此服務提供從主機系統的管理介面關閉虛擬機器作業系統的機制。
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Msvm_ShutdownComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026438"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="20dcc-103">Msvm \_ ShutdownComponent 類別</span><span class="sxs-lookup"><span data-stu-id="20dcc-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="20dcc-104">代表關機服務的狀態，此服務提供從主機系統的管理介面關閉虛擬機器作業系統的機制。</span><span class="sxs-lookup"><span data-stu-id="20dcc-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="20dcc-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20dcc-106">語法</span><span class="sxs-lookup"><span data-stu-id="20dcc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ShutdownComponent";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="20dcc-107">成員</span><span class="sxs-lookup"><span data-stu-id="20dcc-107">Members</span></span>

<span data-ttu-id="20dcc-108">**Msvm \_ ShutdownComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="20dcc-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="20dcc-109">方法</span><span class="sxs-lookup"><span data-stu-id="20dcc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="20dcc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="20dcc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20dcc-111">方法</span><span class="sxs-lookup"><span data-stu-id="20dcc-111">Methods</span></span>

<span data-ttu-id="20dcc-112">**Msvm \_ ShutdownComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="20dcc-113">方法</span><span class="sxs-lookup"><span data-stu-id="20dcc-113">Method</span></span>                                                                  | <span data-ttu-id="20dcc-114">描述</span><span class="sxs-lookup"><span data-stu-id="20dcc-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20dcc-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="20dcc-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="20dcc-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="20dcc-117">**InitiateReboot**</span><span class="sxs-lookup"><span data-stu-id="20dcc-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="20dcc-118">在相關聯的子虛擬機器上起始作業系統重新開機操作。</span><span class="sxs-lookup"><span data-stu-id="20dcc-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="20dcc-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="20dcc-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="20dcc-120">在相關聯的子虛擬機器上起始作業系統關閉操作。</span><span class="sxs-lookup"><span data-stu-id="20dcc-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="20dcc-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="20dcc-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="20dcc-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="20dcc-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="20dcc-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="20dcc-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="20dcc-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="20dcc-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="20dcc-126">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="20dcc-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="20dcc-127">**重設**</span><span class="sxs-lookup"><span data-stu-id="20dcc-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="20dcc-128">重設元件。</span><span class="sxs-lookup"><span data-stu-id="20dcc-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="20dcc-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="20dcc-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="20dcc-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="20dcc-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="20dcc-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="20dcc-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="20dcc-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="20dcc-134">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="20dcc-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="20dcc-135">屬性</span><span class="sxs-lookup"><span data-stu-id="20dcc-135">Properties</span></span>

<span data-ttu-id="20dcc-136">**Msvm \_ ShutdownComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20dcc-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="20dcc-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-138">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-140">裝置的其他可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-140">Additional availability and status of the device.</span></span> <span data-ttu-id="20dcc-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="20dcc-142">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-142">Value</span></span>                                                                        | <span data-ttu-id="20dcc-143">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="20dcc-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="20dcc-145">不適用</span><span class="sxs-lookup"><span data-stu-id="20dcc-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20dcc-146">**可用性**</span><span class="sxs-lookup"><span data-stu-id="20dcc-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-149">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-149">The primary availability and status of the device.</span></span> <span data-ttu-id="20dcc-150">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="20dcc-151">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-151">Value</span></span>                                                                        | <span data-ttu-id="20dcc-152">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="20dcc-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="20dcc-154">不適用</span><span class="sxs-lookup"><span data-stu-id="20dcc-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20dcc-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="20dcc-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-158">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="20dcc-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="20dcc-159">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-160">**標題**</span><span class="sxs-lookup"><span data-stu-id="20dcc-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-163">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="20dcc-163">A short description of the object.</span></span> <span data-ttu-id="20dcc-164">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="20dcc-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-168">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="20dcc-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="20dcc-169">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="20dcc-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="20dcc-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="20dcc-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="20dcc-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="20dcc-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="20dcc-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="20dcc-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="20dcc-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="20dcc-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="20dcc-178">)</span><span class="sxs-lookup"><span data-stu-id="20dcc-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20dcc-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20dcc-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-182">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="20dcc-182">The scoping system's creation class name.</span></span> <span data-ttu-id="20dcc-183">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-184">**說明**</span><span class="sxs-lookup"><span data-stu-id="20dcc-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-187">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="20dcc-187">A description of the object.</span></span> <span data-ttu-id="20dcc-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="20dcc-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-192">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="20dcc-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="20dcc-193">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="20dcc-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="20dcc-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="20dcc-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="20dcc-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="20dcc-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="20dcc-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="20dcc-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="20dcc-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="20dcc-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="20dcc-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="20dcc-203">)</span><span class="sxs-lookup"><span data-stu-id="20dcc-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20dcc-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="20dcc-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-207">用來唯一命名 LogicalDevice 的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="20dcc-208">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*VMGUID* \\ *GUID*"，其中 *VMGUID* 是與此裝置相關聯之 [**Msvm 實例 \_**](msvm-computersystem.md) **名稱的名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="20dcc-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-212">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="20dcc-212">A display name for the object.</span></span> <span data-ttu-id="20dcc-213">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-214">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="20dcc-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-215">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-217">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="20dcc-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="20dcc-218">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-218">Value</span></span>                                                                        | <span data-ttu-id="20dcc-219">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="20dcc-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="20dcc-221">沒有預設值</span><span class="sxs-lookup"><span data-stu-id="20dcc-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20dcc-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-225">元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-225">The enabled state of the element.</span></span> <span data-ttu-id="20dcc-226">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會設定為 2 (啟用) 或 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="20dcc-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="20dcc-227">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-227">Value</span></span>                                                                        | <span data-ttu-id="20dcc-228">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="20dcc-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="20dcc-230">已啟用</span><span class="sxs-lookup"><span data-stu-id="20dcc-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="20dcc-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="20dcc-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="20dcc-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20dcc-233">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="20dcc-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-234">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="20dcc-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-236">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="20dcc-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="20dcc-237">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20dcc-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-241">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="20dcc-242">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-246">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="20dcc-246">The current health of the element.</span></span> <span data-ttu-id="20dcc-247">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="20dcc-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="20dcc-248">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="20dcc-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-250">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-252">自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="20dcc-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="20dcc-253">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20dcc-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-255">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="20dcc-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-257">整合服務安裝到虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="20dcc-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="20dcc-258">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="20dcc-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-262">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="20dcc-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-263">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="20dcc-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="20dcc-264">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20dcc-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-266">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20dcc-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-268">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="20dcc-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="20dcc-269">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-270">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="20dcc-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-271">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="20dcc-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-273">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="20dcc-273">This property has been deprecated.</span></span> <span data-ttu-id="20dcc-274">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-275">**名稱**</span><span class="sxs-lookup"><span data-stu-id="20dcc-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-278">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="20dcc-278">The label by which the object is known.</span></span> <span data-ttu-id="20dcc-279">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-280">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="20dcc-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-281">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-283">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="20dcc-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="20dcc-284">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="20dcc-285">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="20dcc-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="20dcc-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="20dcc-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="20dcc-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="20dcc-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="20dcc-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="20dcc-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="20dcc-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="20dcc-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="20dcc-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="20dcc-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="20dcc-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="20dcc-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="20dcc-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="20dcc-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="20dcc-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="20dcc-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="20dcc-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="20dcc-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="20dcc-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="20dcc-305">)</span><span class="sxs-lookup"><span data-stu-id="20dcc-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20dcc-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="20dcc-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-307">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-309">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-309">The current status of the element.</span></span> <span data-ttu-id="20dcc-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="20dcc-311">以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。</span><span class="sxs-lookup"><span data-stu-id="20dcc-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="20dcc-312">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="20dcc-313">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="20dcc-314"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="20dcc-315">服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="20dcc-315">The service is operating normally.</span></span> <span data-ttu-id="20dcc-316">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="20dcc-317"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="20dcc-318">服務正常運作，但來賓服務已協商相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="20dcc-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="20dcc-319">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="20dcc-320"><dt>**無法復原的錯誤**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="20dcc-321">來賓不支援相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="20dcc-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="20dcc-322">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="20dcc-323"><dt>**無連絡人**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="20dcc-324">尚未安裝或尚未連線到來賓服務。</span><span class="sxs-lookup"><span data-stu-id="20dcc-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="20dcc-325"><dt>**遺失的通訊**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="20dcc-326">來賓服務已不會再回應正常。</span><span class="sxs-lookup"><span data-stu-id="20dcc-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="20dcc-327">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-330">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="20dcc-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="20dcc-331">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="20dcc-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="20dcc-332">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="20dcc-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="20dcc-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-334">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-336">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="20dcc-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="20dcc-337">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="20dcc-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="20dcc-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-339">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-341">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="20dcc-341">The power management capabilities of the device.</span></span> <span data-ttu-id="20dcc-342">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="20dcc-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-344">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="20dcc-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-346">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="20dcc-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="20dcc-347">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-348">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="20dcc-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-349">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="20dcc-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-351">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="20dcc-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="20dcc-352">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="20dcc-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="20dcc-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-354">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-356">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="20dcc-356">Provides high level status information.</span></span> <span data-ttu-id="20dcc-357">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="20dcc-358">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="20dcc-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="20dcc-359">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="20dcc-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="20dcc-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-361"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="20dcc-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="20dcc-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="20dcc-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="20dcc-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="20dcc-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="20dcc-366">)</span><span class="sxs-lookup"><span data-stu-id="20dcc-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20dcc-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-368">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-370">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="20dcc-371">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="20dcc-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="20dcc-372">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="20dcc-373">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="20dcc-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="20dcc-374">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-374">Value</span></span>                                                                         | <span data-ttu-id="20dcc-375">意義</span><span class="sxs-lookup"><span data-stu-id="20dcc-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="20dcc-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="20dcc-377">不適用</span><span class="sxs-lookup"><span data-stu-id="20dcc-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="20dcc-378">**狀態**</span><span class="sxs-lookup"><span data-stu-id="20dcc-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-381">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-381">The current status of the object.</span></span> <span data-ttu-id="20dcc-382">這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="20dcc-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="20dcc-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-384">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="20dcc-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-386">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="20dcc-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="20dcc-387">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="20dcc-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-389">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-391">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-391">The current state of the logical device.</span></span> <span data-ttu-id="20dcc-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20dcc-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-396">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="20dcc-396">The scoping system's creation class name.</span></span> <span data-ttu-id="20dcc-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="20dcc-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20dcc-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-401">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="20dcc-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="20dcc-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="20dcc-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-404">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="20dcc-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-406">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="20dcc-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="20dcc-407">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="20dcc-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="20dcc-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-409">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="20dcc-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-411">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="20dcc-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="20dcc-412">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20dcc-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="20dcc-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20dcc-414">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20dcc-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20dcc-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20dcc-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20dcc-416">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="20dcc-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="20dcc-417">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="20dcc-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20dcc-418">備註</span><span class="sxs-lookup"><span data-stu-id="20dcc-418">Remarks</span></span>

<span data-ttu-id="20dcc-419">存取 **Msvm \_ ShutdownComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="20dcc-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="20dcc-420">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="20dcc-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="20dcc-421">規格需求</span><span class="sxs-lookup"><span data-stu-id="20dcc-421">Requirements</span></span>



| <span data-ttu-id="20dcc-422">需求</span><span class="sxs-lookup"><span data-stu-id="20dcc-422">Requirement</span></span> | <span data-ttu-id="20dcc-423">值</span><span class="sxs-lookup"><span data-stu-id="20dcc-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20dcc-424">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20dcc-424">Minimum supported client</span></span><br/> | <span data-ttu-id="20dcc-425">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20dcc-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20dcc-426">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20dcc-426">Minimum supported server</span></span><br/> | <span data-ttu-id="20dcc-427">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20dcc-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20dcc-428">命名空間</span><span class="sxs-lookup"><span data-stu-id="20dcc-428">Namespace</span></span><br/>                | <span data-ttu-id="20dcc-429">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="20dcc-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20dcc-430">MOF</span><span class="sxs-lookup"><span data-stu-id="20dcc-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20dcc-431"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20dcc-432">DLL</span><span class="sxs-lookup"><span data-stu-id="20dcc-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20dcc-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20dcc-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20dcc-434">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20dcc-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20dcc-435">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="20dcc-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="20dcc-436">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="20dcc-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


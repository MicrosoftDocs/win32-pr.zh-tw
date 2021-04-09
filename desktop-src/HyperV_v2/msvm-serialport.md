---
description: 代表與序列控制器相關聯的序列埠。
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Msvm_SerialPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849489"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="875f7-103">Msvm \_ SerialPort 類別</span><span class="sxs-lookup"><span data-stu-id="875f7-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="875f7-104">代表與序列控制器相關聯的序列埠。</span><span class="sxs-lookup"><span data-stu-id="875f7-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="875f7-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="875f7-106">語法</span><span class="sxs-lookup"><span data-stu-id="875f7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="875f7-107">成員</span><span class="sxs-lookup"><span data-stu-id="875f7-107">Members</span></span>

<span data-ttu-id="875f7-108">**Msvm \_ SerialPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="875f7-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="875f7-109">方法</span><span class="sxs-lookup"><span data-stu-id="875f7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="875f7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="875f7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="875f7-111">方法</span><span class="sxs-lookup"><span data-stu-id="875f7-111">Methods</span></span>

<span data-ttu-id="875f7-112">**Msvm \_ SerialPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="875f7-113">方法</span><span class="sxs-lookup"><span data-stu-id="875f7-113">Method</span></span>                                                           | <span data-ttu-id="875f7-114">描述</span><span class="sxs-lookup"><span data-stu-id="875f7-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="875f7-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="875f7-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="875f7-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="875f7-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="875f7-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="875f7-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="875f7-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="875f7-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="875f7-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="875f7-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="875f7-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="875f7-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="875f7-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="875f7-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="875f7-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="875f7-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="875f7-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="875f7-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="875f7-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="875f7-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="875f7-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="875f7-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="875f7-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="875f7-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="875f7-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="875f7-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="875f7-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="875f7-131">屬性</span><span class="sxs-lookup"><span data-stu-id="875f7-131">Properties</span></span>

<span data-ttu-id="875f7-132">**Msvm \_ SerialPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="875f7-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="875f7-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="875f7-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="875f7-138">值</span><span class="sxs-lookup"><span data-stu-id="875f7-138">Value</span></span>                                                                            | <span data-ttu-id="875f7-139">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="875f7-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="875f7-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="875f7-142">不適用</span><span class="sxs-lookup"><span data-stu-id="875f7-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="875f7-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-146">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-146">The primary availability and status of the device.</span></span> <span data-ttu-id="875f7-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="875f7-148">值</span><span class="sxs-lookup"><span data-stu-id="875f7-148">Value</span></span>                                                                        | <span data-ttu-id="875f7-149">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="875f7-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="875f7-151">不適用</span><span class="sxs-lookup"><span data-stu-id="875f7-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="875f7-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-155">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="875f7-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="875f7-156">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-157">**標題**</span><span class="sxs-lookup"><span data-stu-id="875f7-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-160">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="875f7-160">A short description of the object.</span></span> <span data-ttu-id="875f7-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="875f7-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-165">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="875f7-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="875f7-166">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="875f7-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="875f7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="875f7-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="875f7-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="875f7-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="875f7-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="875f7-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="875f7-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="875f7-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="875f7-175">)</span><span class="sxs-lookup"><span data-stu-id="875f7-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="875f7-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="875f7-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-179">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="875f7-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="875f7-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-181">**說明**</span><span class="sxs-lookup"><span data-stu-id="875f7-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-184">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="875f7-184">A description of the object.</span></span> <span data-ttu-id="875f7-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="875f7-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-189">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="875f7-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="875f7-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="875f7-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="875f7-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="875f7-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="875f7-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="875f7-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="875f7-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="875f7-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="875f7-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="875f7-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="875f7-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="875f7-200">)</span><span class="sxs-lookup"><span data-stu-id="875f7-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="875f7-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="875f7-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-204">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為「Microsoft：*GUID* \\ *裝置特定資料*」，其中 *裝置特定資料* 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="875f7-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="875f7-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-208">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="875f7-208">A display name for the object.</span></span> <span data-ttu-id="875f7-209">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="875f7-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-213">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="875f7-214">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="875f7-215">值</span><span class="sxs-lookup"><span data-stu-id="875f7-215">Value</span></span>                                                                        | <span data-ttu-id="875f7-216">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="875f7-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="875f7-218">已啟用</span><span class="sxs-lookup"><span data-stu-id="875f7-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="875f7-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-222">元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-222">The enabled state of the element.</span></span> <span data-ttu-id="875f7-223">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="875f7-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="875f7-224">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="875f7-225">值</span><span class="sxs-lookup"><span data-stu-id="875f7-225">Value</span></span>                                                                        | <span data-ttu-id="875f7-226">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="875f7-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="875f7-228">不適用</span><span class="sxs-lookup"><span data-stu-id="875f7-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="875f7-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-230">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="875f7-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-232">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="875f7-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="875f7-233">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="875f7-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-237">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="875f7-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="875f7-238">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="875f7-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-240">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-242">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="875f7-242">The current health of the element.</span></span> <span data-ttu-id="875f7-243">這表示此元素的健全狀況，但不一定是其子元件的健康情況。</span><span class="sxs-lookup"><span data-stu-id="875f7-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="875f7-244">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="875f7-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="875f7-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="875f7-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-247">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-249">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="875f7-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="875f7-250">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="875f7-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="875f7-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-252">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="875f7-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-254">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="875f7-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="875f7-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="875f7-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="875f7-259">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="875f7-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="875f7-260">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="875f7-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="875f7-261">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="875f7-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-263">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="875f7-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-265">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="875f7-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="875f7-266">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="875f7-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-268">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="875f7-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-270">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="875f7-270">This property has been deprecated.</span></span> <span data-ttu-id="875f7-271">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="875f7-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="875f7-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-275">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="875f7-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="875f7-276">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-277">**名稱**</span><span class="sxs-lookup"><span data-stu-id="875f7-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-280">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="875f7-280">The label by which the object is known.</span></span> <span data-ttu-id="875f7-281">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="875f7-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="875f7-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-285">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="875f7-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="875f7-286">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="875f7-287">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="875f7-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="875f7-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="875f7-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="875f7-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="875f7-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="875f7-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="875f7-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="875f7-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="875f7-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="875f7-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="875f7-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="875f7-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="875f7-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="875f7-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="875f7-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="875f7-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="875f7-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="875f7-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="875f7-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="875f7-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="875f7-307">)</span><span class="sxs-lookup"><span data-stu-id="875f7-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="875f7-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="875f7-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-309">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-311">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-311">The current statuses of the object.</span></span> <span data-ttu-id="875f7-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="875f7-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-316">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="875f7-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="875f7-317">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="875f7-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="875f7-318">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="875f7-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-320">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-322">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="875f7-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="875f7-323">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="875f7-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="875f7-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-327">當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="875f7-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="875f7-328">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="875f7-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-330">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-332">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="875f7-333">值</span><span class="sxs-lookup"><span data-stu-id="875f7-333">Value</span></span>                                                                        | <span data-ttu-id="875f7-334">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="875f7-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="875f7-336">其他</span><span class="sxs-lookup"><span data-stu-id="875f7-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="875f7-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-338">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-340">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="875f7-340">The power management capabilities of the device.</span></span> <span data-ttu-id="875f7-341">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="875f7-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="875f7-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-345">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="875f7-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="875f7-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="875f7-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-348">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="875f7-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-350">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="875f7-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="875f7-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="875f7-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-353">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-355">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="875f7-355">Provides high level status information.</span></span> <span data-ttu-id="875f7-356">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="875f7-357">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="875f7-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="875f7-358">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="875f7-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="875f7-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-360"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="875f7-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="875f7-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="875f7-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="875f7-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="875f7-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="875f7-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="875f7-365">)</span><span class="sxs-lookup"><span data-stu-id="875f7-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="875f7-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="875f7-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-367">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="875f7-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-369">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="875f7-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="875f7-370">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="875f7-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-372">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-374">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="875f7-375">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="875f7-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="875f7-376">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="875f7-377">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="875f7-378">值</span><span class="sxs-lookup"><span data-stu-id="875f7-378">Value</span></span>                                                                         | <span data-ttu-id="875f7-379">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="875f7-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="875f7-381">不適用</span><span class="sxs-lookup"><span data-stu-id="875f7-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="875f7-382">**速度**</span><span class="sxs-lookup"><span data-stu-id="875f7-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-383">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="875f7-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-385">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="875f7-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="875f7-386">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-387">**狀態**</span><span class="sxs-lookup"><span data-stu-id="875f7-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-390">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-390">The current status of the object.</span></span> <span data-ttu-id="875f7-391">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="875f7-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-393">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="875f7-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="875f7-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-395">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="875f7-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="875f7-396">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="875f7-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="875f7-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-400">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-400">The current state of the logical device.</span></span> <span data-ttu-id="875f7-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="875f7-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-405">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="875f7-405">The scoping system's creation class name.</span></span> <span data-ttu-id="875f7-406">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="875f7-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="875f7-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-410">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="875f7-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="875f7-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="875f7-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="875f7-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="875f7-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-413">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="875f7-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-415">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="875f7-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="875f7-416">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="875f7-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="875f7-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-418">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="875f7-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-420">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="875f7-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="875f7-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="875f7-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-423">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-425">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="875f7-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="875f7-426">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="875f7-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="875f7-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="875f7-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="875f7-428">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="875f7-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="875f7-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="875f7-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="875f7-430">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="875f7-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="875f7-431">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="875f7-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="875f7-432">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="875f7-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="875f7-433">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="875f7-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="875f7-434">值</span><span class="sxs-lookup"><span data-stu-id="875f7-434">Value</span></span>                                                                        | <span data-ttu-id="875f7-435">意義</span><span class="sxs-lookup"><span data-stu-id="875f7-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="875f7-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="875f7-437">不受限制</span><span class="sxs-lookup"><span data-stu-id="875f7-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="875f7-438">備註</span><span class="sxs-lookup"><span data-stu-id="875f7-438">Remarks</span></span>

<span data-ttu-id="875f7-439">存取 **Msvm \_ SerialPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="875f7-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="875f7-440">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="875f7-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="875f7-441">規格需求</span><span class="sxs-lookup"><span data-stu-id="875f7-441">Requirements</span></span>



| <span data-ttu-id="875f7-442">需求</span><span class="sxs-lookup"><span data-stu-id="875f7-442">Requirement</span></span> | <span data-ttu-id="875f7-443">值</span><span class="sxs-lookup"><span data-stu-id="875f7-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875f7-444">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="875f7-444">Minimum supported client</span></span><br/> | <span data-ttu-id="875f7-445">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="875f7-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="875f7-446">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="875f7-446">Minimum supported server</span></span><br/> | <span data-ttu-id="875f7-447">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="875f7-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="875f7-448">命名空間</span><span class="sxs-lookup"><span data-stu-id="875f7-448">Namespace</span></span><br/>                | <span data-ttu-id="875f7-449">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="875f7-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="875f7-450">MOF</span><span class="sxs-lookup"><span data-stu-id="875f7-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="875f7-451"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="875f7-452">DLL</span><span class="sxs-lookup"><span data-stu-id="875f7-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875f7-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="875f7-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="875f7-454">另請參閱</span><span class="sxs-lookup"><span data-stu-id="875f7-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875f7-455">**CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="875f7-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="875f7-456">[**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="875f7-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="875f7-457">序列裝置類別</span><span class="sxs-lookup"><span data-stu-id="875f7-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 


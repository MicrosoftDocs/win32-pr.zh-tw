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
# <a name="msvm_serialport-class"></a><span data-ttu-id="f1786-103">Msvm \_ SerialPort 類別</span><span class="sxs-lookup"><span data-stu-id="f1786-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="f1786-104">代表與序列控制器相關聯的序列埠。</span><span class="sxs-lookup"><span data-stu-id="f1786-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="f1786-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1786-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1786-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f1786-107">成員</span><span class="sxs-lookup"><span data-stu-id="f1786-107">Members</span></span>

<span data-ttu-id="f1786-108">**Msvm \_ SerialPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f1786-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="f1786-109">方法</span><span class="sxs-lookup"><span data-stu-id="f1786-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1786-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f1786-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1786-111">方法</span><span class="sxs-lookup"><span data-stu-id="f1786-111">Methods</span></span>

<span data-ttu-id="f1786-112">**Msvm \_ SerialPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="f1786-113">方法</span><span class="sxs-lookup"><span data-stu-id="f1786-113">Method</span></span>                                                           | <span data-ttu-id="f1786-114">描述</span><span class="sxs-lookup"><span data-stu-id="f1786-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="f1786-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f1786-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="f1786-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f1786-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f1786-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="f1786-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f1786-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f1786-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="f1786-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="f1786-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f1786-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="f1786-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="f1786-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="f1786-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="f1786-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="f1786-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="f1786-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="f1786-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f1786-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="f1786-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f1786-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f1786-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="f1786-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f1786-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f1786-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="f1786-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f1786-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1786-131">屬性</span><span class="sxs-lookup"><span data-stu-id="f1786-131">Properties</span></span>

<span data-ttu-id="f1786-132">**Msvm \_ SerialPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1786-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f1786-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="f1786-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f1786-138">值</span><span class="sxs-lookup"><span data-stu-id="f1786-138">Value</span></span>                                                                            | <span data-ttu-id="f1786-139">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f1786-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="f1786-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="f1786-142">不適用</span><span class="sxs-lookup"><span data-stu-id="f1786-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="f1786-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-146">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-146">The primary availability and status of the device.</span></span> <span data-ttu-id="f1786-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="f1786-148">值</span><span class="sxs-lookup"><span data-stu-id="f1786-148">Value</span></span>                                                                        | <span data-ttu-id="f1786-149">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f1786-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="f1786-151">不適用</span><span class="sxs-lookup"><span data-stu-id="f1786-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f1786-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-155">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="f1786-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="f1786-156">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-157">**標題**</span><span class="sxs-lookup"><span data-stu-id="f1786-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-160">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f1786-160">A short description of the object.</span></span> <span data-ttu-id="f1786-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f1786-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-165">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="f1786-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f1786-166">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1786-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1786-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f1786-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="f1786-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="f1786-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="f1786-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="f1786-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f1786-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="f1786-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1786-175">)</span><span class="sxs-lookup"><span data-stu-id="f1786-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1786-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1786-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-179">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1786-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f1786-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-181">**說明**</span><span class="sxs-lookup"><span data-stu-id="f1786-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-184">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f1786-184">A description of the object.</span></span> <span data-ttu-id="f1786-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f1786-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-189">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f1786-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f1786-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1786-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1786-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="f1786-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="f1786-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="f1786-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="f1786-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="f1786-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="f1786-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f1786-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="f1786-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1786-200">)</span><span class="sxs-lookup"><span data-stu-id="f1786-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1786-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1786-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-204">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為「Microsoft：*GUID* \\ *裝置特定資料*」，其中 *裝置特定資料* 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f1786-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f1786-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-208">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f1786-208">A display name for the object.</span></span> <span data-ttu-id="f1786-209">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f1786-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-213">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f1786-214">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f1786-215">值</span><span class="sxs-lookup"><span data-stu-id="f1786-215">Value</span></span>                                                                        | <span data-ttu-id="f1786-216">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="f1786-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f1786-218">已啟用</span><span class="sxs-lookup"><span data-stu-id="f1786-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f1786-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-222">元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-222">The enabled state of the element.</span></span> <span data-ttu-id="f1786-223">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="f1786-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="f1786-224">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f1786-225">值</span><span class="sxs-lookup"><span data-stu-id="f1786-225">Value</span></span>                                                                        | <span data-ttu-id="f1786-226">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f1786-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="f1786-228">不適用</span><span class="sxs-lookup"><span data-stu-id="f1786-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f1786-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-230">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f1786-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-232">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1786-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="f1786-233">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f1786-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-237">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f1786-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="f1786-238">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f1786-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-240">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-242">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="f1786-242">The current health of the element.</span></span> <span data-ttu-id="f1786-243">這表示此元素的健全狀況，但不一定是其子元件的健康情況。</span><span class="sxs-lookup"><span data-stu-id="f1786-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f1786-244">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f1786-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f1786-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f1786-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-247">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-249">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f1786-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f1786-250">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f1786-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1786-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-252">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f1786-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-254">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f1786-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f1786-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1786-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1786-259">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f1786-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f1786-260">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f1786-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f1786-261">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f1786-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-263">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1786-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-265">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f1786-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="f1786-266">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f1786-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-268">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f1786-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-270">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="f1786-270">This property has been deprecated.</span></span> <span data-ttu-id="f1786-271">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="f1786-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f1786-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-275">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1786-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="f1786-276">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-277">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f1786-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-280">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="f1786-280">The label by which the object is known.</span></span> <span data-ttu-id="f1786-281">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="f1786-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f1786-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-285">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f1786-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f1786-286">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1786-287">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1786-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f1786-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="f1786-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="f1786-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="f1786-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="f1786-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="f1786-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="f1786-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="f1786-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="f1786-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="f1786-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="f1786-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="f1786-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="f1786-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="f1786-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="f1786-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="f1786-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="f1786-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f1786-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="f1786-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1786-307">)</span><span class="sxs-lookup"><span data-stu-id="f1786-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1786-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f1786-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-309">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-311">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-311">The current statuses of the object.</span></span> <span data-ttu-id="f1786-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f1786-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-316">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="f1786-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f1786-317">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f1786-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f1786-318">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f1786-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-320">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-322">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="f1786-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f1786-323">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f1786-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="f1786-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-327">當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="f1786-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="f1786-328">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="f1786-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-330">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-332">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="f1786-333">值</span><span class="sxs-lookup"><span data-stu-id="f1786-333">Value</span></span>                                                                        | <span data-ttu-id="f1786-334">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="f1786-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f1786-336">其他</span><span class="sxs-lookup"><span data-stu-id="f1786-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f1786-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-338">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-340">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="f1786-340">The power management capabilities of the device.</span></span> <span data-ttu-id="f1786-341">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f1786-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f1786-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-345">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="f1786-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f1786-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f1786-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-348">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f1786-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-350">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="f1786-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f1786-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f1786-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-353">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-355">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f1786-355">Provides high level status information.</span></span> <span data-ttu-id="f1786-356">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f1786-357">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f1786-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f1786-358">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="f1786-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f1786-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-360"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="f1786-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="f1786-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="f1786-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f1786-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1786-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="f1786-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="f1786-365">)</span><span class="sxs-lookup"><span data-stu-id="f1786-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1786-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="f1786-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-367">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f1786-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-369">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1786-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="f1786-370">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f1786-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-372">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-374">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="f1786-375">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="f1786-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="f1786-376">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="f1786-377">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="f1786-378">值</span><span class="sxs-lookup"><span data-stu-id="f1786-378">Value</span></span>                                                                         | <span data-ttu-id="f1786-379">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f1786-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="f1786-381">不適用</span><span class="sxs-lookup"><span data-stu-id="f1786-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1786-382">**速度**</span><span class="sxs-lookup"><span data-stu-id="f1786-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-383">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f1786-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-385">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1786-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="f1786-386">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-387">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f1786-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-390">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-390">The current status of the object.</span></span> <span data-ttu-id="f1786-391">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f1786-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-393">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1786-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1786-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-395">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="f1786-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f1786-396">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f1786-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f1786-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-400">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-400">The current state of the logical device.</span></span> <span data-ttu-id="f1786-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1786-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-405">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f1786-405">The scoping system's creation class name.</span></span> <span data-ttu-id="f1786-406">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1786-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1786-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-410">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1786-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="f1786-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f1786-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f1786-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f1786-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-413">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f1786-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-415">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="f1786-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f1786-416">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f1786-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f1786-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-418">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f1786-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-420">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="f1786-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="f1786-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f1786-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-423">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-425">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f1786-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f1786-426">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f1786-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1786-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="f1786-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1786-428">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1786-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1786-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1786-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1786-430">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="f1786-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="f1786-431">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="f1786-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="f1786-432">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="f1786-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="f1786-433">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f1786-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="f1786-434">值</span><span class="sxs-lookup"><span data-stu-id="f1786-434">Value</span></span>                                                                        | <span data-ttu-id="f1786-435">意義</span><span class="sxs-lookup"><span data-stu-id="f1786-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f1786-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="f1786-437">不受限制</span><span class="sxs-lookup"><span data-stu-id="f1786-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1786-438">備註</span><span class="sxs-lookup"><span data-stu-id="f1786-438">Remarks</span></span>

<span data-ttu-id="f1786-439">存取 **Msvm \_ SerialPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="f1786-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f1786-440">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="f1786-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1786-441">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1786-441">Requirements</span></span>



| <span data-ttu-id="f1786-442">需求</span><span class="sxs-lookup"><span data-stu-id="f1786-442">Requirement</span></span> | <span data-ttu-id="f1786-443">值</span><span class="sxs-lookup"><span data-stu-id="f1786-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1786-444">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1786-444">Minimum supported client</span></span><br/> | <span data-ttu-id="f1786-445">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1786-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1786-446">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1786-446">Minimum supported server</span></span><br/> | <span data-ttu-id="f1786-447">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1786-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1786-448">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1786-448">Namespace</span></span><br/>                | <span data-ttu-id="f1786-449">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f1786-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1786-450">MOF</span><span class="sxs-lookup"><span data-stu-id="f1786-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1786-451"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1786-452">DLL</span><span class="sxs-lookup"><span data-stu-id="f1786-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1786-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1786-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1786-454">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1786-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1786-455">**CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="f1786-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="f1786-456">[**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1786-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1786-457">序列裝置類別</span><span class="sxs-lookup"><span data-stu-id="f1786-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 


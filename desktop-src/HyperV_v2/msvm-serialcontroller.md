---
description: 代表序列控制器的功能和管理。
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Msvm_SerialController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973882"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="c3ff2-103">Msvm \_ SerialController 類別</span><span class="sxs-lookup"><span data-stu-id="c3ff2-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="c3ff2-104">代表序列控制器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="c3ff2-105">串列控制器是一律存在於虛擬機器中的邏輯裝置，因此不會透過資源集區配置。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="c3ff2-106">虛擬機器中一律會有一個串列控制器實例。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="c3ff2-107">串列控制器具有固定的埠實例數目。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="c3ff2-108">這種執行支援每個控制器都有兩個埠。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="c3ff2-109">[第2代虛擬機器](virtualization-glossary.md)中的序列控制器是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="c3ff2-110">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ff2-111">語法</span><span class="sxs-lookup"><span data-stu-id="c3ff2-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
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
  string   CreationClassName = "Msvm_SerialController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="c3ff2-112">成員</span><span class="sxs-lookup"><span data-stu-id="c3ff2-112">Members</span></span>

<span data-ttu-id="c3ff2-113">**Msvm \_ SerialController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c3ff2-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="c3ff2-114">方法</span><span class="sxs-lookup"><span data-stu-id="c3ff2-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3ff2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c3ff2-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3ff2-116">方法</span><span class="sxs-lookup"><span data-stu-id="c3ff2-116">Methods</span></span>

<span data-ttu-id="c3ff2-117">**Msvm \_ SerialController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="c3ff2-118">方法</span><span class="sxs-lookup"><span data-stu-id="c3ff2-118">Method</span></span>                                                                 | <span data-ttu-id="c3ff2-119">描述</span><span class="sxs-lookup"><span data-stu-id="c3ff2-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c3ff2-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="c3ff2-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3ff2-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="c3ff2-123">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3ff2-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="c3ff2-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c3ff2-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="c3ff2-127">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c3ff2-128">**重設**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="c3ff2-129">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="c3ff2-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="c3ff2-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3ff2-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="c3ff2-133">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c3ff2-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="c3ff2-135">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c3ff2-136">屬性</span><span class="sxs-lookup"><span data-stu-id="c3ff2-136">Properties</span></span>

<span data-ttu-id="c3ff2-137">**Msvm \_ SerialController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3ff2-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-141">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="c3ff2-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c3ff2-143">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-143">Value</span></span>                                                                            | <span data-ttu-id="c3ff2-144">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3ff2-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="c3ff2-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="c3ff2-147">不適用</span><span class="sxs-lookup"><span data-stu-id="c3ff2-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-148">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-151">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-151">The primary availability and status of the device.</span></span> <span data-ttu-id="c3ff2-152">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c3ff2-153">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-153">Value</span></span>                                                                        | <span data-ttu-id="c3ff2-154">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3ff2-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c3ff2-156">不適用</span><span class="sxs-lookup"><span data-stu-id="c3ff2-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-157">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-158">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-160">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c3ff2-161">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-163">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-165">在晶片硬體中可能具有固有的序列控制器的緩衝和其他功能。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="c3ff2-166">這個屬性繼承自 [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-167">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-168">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-170">自由格式字串的陣列，可針對 **功能** 陣列中所指出的任何序列控制器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="c3ff2-171">這個屬性繼承自 [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-172">**標題**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-175">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-175">A short description of the object.</span></span> <span data-ttu-id="c3ff2-176">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-180">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c3ff2-181">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3ff2-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3ff2-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3ff2-190">)</span><span class="sxs-lookup"><span data-stu-id="c3ff2-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3ff2-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-194">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c3ff2-195">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-196">**說明**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-199">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-199">A description of the object.</span></span> <span data-ttu-id="c3ff2-200">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-204">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c3ff2-205">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3ff2-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3ff2-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3ff2-215">)</span><span class="sxs-lookup"><span data-stu-id="c3ff2-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3ff2-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-219">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft： *<GUID>* "。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-223">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-223">A display name for the object.</span></span> <span data-ttu-id="c3ff2-224">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-225">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-226">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-228">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c3ff2-229">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3ff2-230">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-230">Value</span></span>                                                                        | <span data-ttu-id="c3ff2-231">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c3ff2-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c3ff2-233">已啟用</span><span class="sxs-lookup"><span data-stu-id="c3ff2-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-235">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-237">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c3ff2-238">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c3ff2-239">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3ff2-240">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-240">Value</span></span>                                                                        | <span data-ttu-id="c3ff2-241">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3ff2-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="c3ff2-243">不適用</span><span class="sxs-lookup"><span data-stu-id="c3ff2-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-244">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-247">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="c3ff2-248">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-252">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="c3ff2-253">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-255">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-257">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-257">The current health of the element.</span></span> <span data-ttu-id="c3ff2-258">這表示此元素的健全狀況，但不一定是其子元件的健康情況。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c3ff2-259">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c3ff2-260">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-262">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-264">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="c3ff2-265">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-267">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-269">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c3ff2-270">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-274">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-275">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c3ff2-276">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-278">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-280">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="c3ff2-281">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-282">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-285">序列控制器支援的最大傳輸速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="c3ff2-286">這個屬性繼承自 [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-288">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-290">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="c3ff2-291">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="c3ff2-292">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="c3ff2-293">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-294">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-295">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-297">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-297">This property has been deprecated.</span></span> <span data-ttu-id="c3ff2-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-299">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-302">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-302">The label by which the object is known.</span></span> <span data-ttu-id="c3ff2-303">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-304">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-305">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-307">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c3ff2-308">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3ff2-309">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3ff2-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3ff2-329">)</span><span class="sxs-lookup"><span data-stu-id="c3ff2-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3ff2-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-331">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-333">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-333">The current statuses of the object.</span></span> <span data-ttu-id="c3ff2-334">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-335">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-338">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c3ff2-339">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c3ff2-340">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-342">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-344">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c3ff2-345">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-347">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-349">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-349">The power management capabilities of the device.</span></span> <span data-ttu-id="c3ff2-350">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-351">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-352">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-354">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c3ff2-355">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-356">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-357">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-359">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c3ff2-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-361">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-364">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-364">Provides high level status information.</span></span> <span data-ttu-id="c3ff2-365">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c3ff2-366">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c3ff2-367">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c3ff2-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-369"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c3ff2-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c3ff2-374">)</span><span class="sxs-lookup"><span data-stu-id="c3ff2-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3ff2-375">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-378">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="c3ff2-379">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-380">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-381">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-383">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="c3ff2-384">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="c3ff2-385">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-385">Value</span></span>                                                                         | <span data-ttu-id="c3ff2-386">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c3ff2-387"><dt>個</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="c3ff2-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="c3ff2-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-390">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-392">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="c3ff2-393">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c3ff2-394">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="c3ff2-395">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c3ff2-396">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-396">Value</span></span>                                                                         | <span data-ttu-id="c3ff2-397">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c3ff2-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c3ff2-399">不適用</span><span class="sxs-lookup"><span data-stu-id="c3ff2-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-400">**安全性**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-401">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-403">控制器的操作安全性。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-403">The operational security for the controller.</span></span> <span data-ttu-id="c3ff2-404">這個屬性繼承自 [**CIM \_ SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="c3ff2-405">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-405">Value</span></span>                                                                        | <span data-ttu-id="c3ff2-406">意義</span><span class="sxs-lookup"><span data-stu-id="c3ff2-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="c3ff2-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c3ff2-408">無</span><span class="sxs-lookup"><span data-stu-id="c3ff2-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3ff2-409">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-410">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-412">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-412">The current status of the object.</span></span> <span data-ttu-id="c3ff2-413">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-414">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-415">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c3ff2-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-417">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c3ff2-418">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-420">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-422">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-422">The current state of the logical device.</span></span> <span data-ttu-id="c3ff2-423">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-424">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-427">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-427">The scoping system's creation class name.</span></span> <span data-ttu-id="c3ff2-428">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-432">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="c3ff2-433">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-435">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-437">控制器上次開機的時間。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-437">The last time the controller was powered on.</span></span> <span data-ttu-id="c3ff2-438">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-439">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-440">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-442">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c3ff2-443">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-444">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-445">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-447">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c3ff2-448">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c3ff2-449">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ff2-450">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3ff2-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c3ff2-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3ff2-452">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c3ff2-453">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3ff2-454">備註</span><span class="sxs-lookup"><span data-stu-id="c3ff2-454">Remarks</span></span>

<span data-ttu-id="c3ff2-455">存取 **Msvm \_ SerialController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c3ff2-456">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="c3ff2-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ff2-457">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3ff2-457">Requirements</span></span>



| <span data-ttu-id="c3ff2-458">需求</span><span class="sxs-lookup"><span data-stu-id="c3ff2-458">Requirement</span></span> | <span data-ttu-id="c3ff2-459">值</span><span class="sxs-lookup"><span data-stu-id="c3ff2-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ff2-460">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3ff2-460">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ff2-461">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3ff2-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3ff2-462">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3ff2-462">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ff2-463">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3ff2-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3ff2-464">命名空間</span><span class="sxs-lookup"><span data-stu-id="c3ff2-464">Namespace</span></span><br/>                | <span data-ttu-id="c3ff2-465">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c3ff2-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3ff2-466">MOF</span><span class="sxs-lookup"><span data-stu-id="c3ff2-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3ff2-467"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3ff2-468">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ff2-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3ff2-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3ff2-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3ff2-470">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3ff2-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ff2-471">**CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="c3ff2-472">**CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="c3ff2-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="c3ff2-473">序列裝置類別</span><span class="sxs-lookup"><span data-stu-id="c3ff2-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 


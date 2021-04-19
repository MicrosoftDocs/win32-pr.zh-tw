---
description: 代表模擬的乙太網路介面卡。
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Msvm_EmulatedEthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000096"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="9631d-103">Msvm \_ EmulatedEthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="9631d-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="9631d-104">代表模擬的乙太網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="9631d-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="9631d-105">當虛擬機器未在來賓中安裝任何整合線路時，會使用此介面卡來執行綜合乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="9631d-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="9631d-106">第2代虛擬機器無法使用此類別。</span><span class="sxs-lookup"><span data-stu-id="9631d-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="9631d-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9631d-108">語法</span><span class="sxs-lookup"><span data-stu-id="9631d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="9631d-109">成員</span><span class="sxs-lookup"><span data-stu-id="9631d-109">Members</span></span>

<span data-ttu-id="9631d-110">**Msvm \_ EmulatedEthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9631d-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="9631d-111">方法</span><span class="sxs-lookup"><span data-stu-id="9631d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9631d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9631d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9631d-113">方法</span><span class="sxs-lookup"><span data-stu-id="9631d-113">Methods</span></span>

<span data-ttu-id="9631d-114">**Msvm \_ EmulatedEthernetPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="9631d-115">方法</span><span class="sxs-lookup"><span data-stu-id="9631d-115">Method</span></span>                                                                     | <span data-ttu-id="9631d-116">描述</span><span class="sxs-lookup"><span data-stu-id="9631d-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9631d-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9631d-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="9631d-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9631d-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="9631d-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="9631d-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9631d-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="9631d-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="9631d-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9631d-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9631d-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="9631d-124">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9631d-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9631d-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="9631d-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="9631d-126">重設模擬裝置。</span><span class="sxs-lookup"><span data-stu-id="9631d-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="9631d-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="9631d-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="9631d-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9631d-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9631d-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="9631d-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9631d-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9631d-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="9631d-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9631d-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9631d-133">屬性</span><span class="sxs-lookup"><span data-stu-id="9631d-133">Properties</span></span>

<span data-ttu-id="9631d-134">**Msvm \_ EmulatedEthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9631d-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="9631d-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-138">可以支援的作用中或已協商的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="9631d-139">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1500。</span><span class="sxs-lookup"><span data-stu-id="9631d-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="9631d-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-143">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="9631d-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="9631d-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-145">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="9631d-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9631d-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-148">指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="9631d-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="9631d-149">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="9631d-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="9631d-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-153">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-153">The primary availability and status of the device.</span></span> <span data-ttu-id="9631d-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9631d-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9631d-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-158">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="9631d-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9631d-159">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="9631d-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="9631d-160">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="9631d-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9631d-161">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9631d-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9631d-162">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9631d-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9631d-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="9631d-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="9631d-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="9631d-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="9631d-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="9631d-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="9631d-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="9631d-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="9631d-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="9631d-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9631d-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="9631d-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="9631d-173">)</span><span class="sxs-lookup"><span data-stu-id="9631d-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9631d-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9631d-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-177">乙太網路埠的功能。</span><span class="sxs-lookup"><span data-stu-id="9631d-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="9631d-178">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-179">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9631d-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-180">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-182">自由格式字串的陣列，可針對 **功能** 陣列中所指出的任何乙太網路埠功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="9631d-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="9631d-183">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="9631d-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="9631d-184">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-185">**標題**</span><span class="sxs-lookup"><span data-stu-id="9631d-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-188">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="9631d-188">A short description of the object.</span></span> <span data-ttu-id="9631d-189">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="9631d-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-190">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9631d-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-193">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="9631d-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9631d-194">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9631d-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9631d-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-199">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9631d-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="9631d-200">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9631d-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="9631d-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ EmulatedEthernetPort"。</span><span class="sxs-lookup"><span data-stu-id="9631d-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-202">**說明**</span><span class="sxs-lookup"><span data-stu-id="9631d-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-205">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9631d-205">A description of the object.</span></span> <span data-ttu-id="9631d-206">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 模擬乙太網路埠」。</span><span class="sxs-lookup"><span data-stu-id="9631d-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9631d-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-210">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9631d-211">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9631d-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9631d-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-216">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="9631d-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="9631d-217">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且一律設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="9631d-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9631d-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-221">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9631d-221">A display name for the object.</span></span> <span data-ttu-id="9631d-222">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「傳統網路介面卡」。</span><span class="sxs-lookup"><span data-stu-id="9631d-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-223">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9631d-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-224">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-226">從所有支援的專案清單中啟用的功能，這些功能都是在 **功能** 陣列中定義。</span><span class="sxs-lookup"><span data-stu-id="9631d-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="9631d-227">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9631d-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-228">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9631d-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-229">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-231">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9631d-232">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且一律設定為 2 ( 「已啟用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9631d-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-234">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-236">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9631d-237">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9631d-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9631d-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-241">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9631d-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9631d-242">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9631d-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-246">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9631d-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="9631d-247">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-248">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="9631d-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-249">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9631d-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-251">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="9631d-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="9631d-252">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，而且一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="9631d-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9631d-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-254">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-256">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="9631d-256">The current health of the element.</span></span> <span data-ttu-id="9631d-257">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="9631d-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9631d-258">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 ( 「確定」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9631d-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-260">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-262">自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9631d-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="9631d-263">這個陣列的每個專案都與 **OtherIdentifyingInfo** 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="9631d-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="9631d-264">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9631d-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-266">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9631d-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-268">**日期時間** 值，指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="9631d-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="9631d-269">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="9631d-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="9631d-270">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9631d-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9631d-274">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9631d-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9631d-275">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9631d-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9631d-276">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9631d-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-278">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9631d-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-280">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9631d-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="9631d-281">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-282">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="9631d-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-285">連結的類型。</span><span class="sxs-lookup"><span data-stu-id="9631d-285">The types of links.</span></span> <span data-ttu-id="9631d-286">當設定為 1 ( "Other" ) 時，相關的屬性 **OtherLinkTechnology** 會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="9631d-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="9631d-287">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ，而且一律設定為 2 ( 「Ethernet」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-288">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="9631d-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-289">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9631d-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-291">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="9631d-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="9631d-292">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，一律設為1500。</span><span class="sxs-lookup"><span data-stu-id="9631d-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-293">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="9631d-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-294">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-296">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-297">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="9631d-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-298">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-300">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9631d-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9631d-301">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))，一律設為1000000000。</span><span class="sxs-lookup"><span data-stu-id="9631d-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-302">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9631d-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-305">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="9631d-305">The label by which the object is known.</span></span> <span data-ttu-id="9631d-306">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="9631d-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，且一律設定為「Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="9631d-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="9631d-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-309">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-311">Ethernet/802.3 MAC 位址（格式化為十二個十六進位數位） (例如 "010203040506" ) ，其中每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（在字串) 的第一個字元的低序位位中找到）。</span><span class="sxs-lookup"><span data-stu-id="9631d-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="9631d-312">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-313">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9631d-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-314">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-316">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9631d-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9631d-317">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9631d-318">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9631d-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-320">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-322">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-322">The current statuses of the element.</span></span> <span data-ttu-id="9631d-323">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 ( 「確定」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-324">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9631d-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-325">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-327">自由格式字串的陣列，可針對指定為「其他」的任何已啟用功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="9631d-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="9631d-328">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9631d-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-332">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="9631d-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="9631d-333">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9631d-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9631d-334">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9631d-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-336">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-338">除了可用來識別邏輯裝置的裝置識別碼資訊以外的任何資料。</span><span class="sxs-lookup"><span data-stu-id="9631d-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9631d-339">例如，您可以使用這個屬性來保存裝置的作業系統顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9631d-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="9631d-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="9631d-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-344">當 LinkTechnology 設定為 1 ( "Other" ) 時，描述的字串值。</span><span class="sxs-lookup"><span data-stu-id="9631d-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="9631d-345">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9631d-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="9631d-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-349">這個屬性會繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9631d-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-350">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="9631d-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-351">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-353">當 **PortType** 設定為 1 ( "Other" ) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="9631d-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="9631d-354">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ，一律設為「虛擬乙太網路」。</span><span class="sxs-lookup"><span data-stu-id="9631d-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-355">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="9631d-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-358">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="9631d-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="9631d-359">您可以使用固件升級或軟體設定來變更此位址。</span><span class="sxs-lookup"><span data-stu-id="9631d-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="9631d-360">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="9631d-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="9631d-361">如果網路介面卡沒有任何硬式編碼位址，則應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="9631d-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="9631d-362">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="9631d-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-363">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="9631d-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-364">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-366">網路埠的編號通常相對於邏輯模組或網路元素。</span><span class="sxs-lookup"><span data-stu-id="9631d-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="9631d-367">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="9631d-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="9631d-368">值</span><span class="sxs-lookup"><span data-stu-id="9631d-368">Value</span></span>                                                                        | <span data-ttu-id="9631d-369">意義</span><span class="sxs-lookup"><span data-stu-id="9631d-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="9631d-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9631d-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="9631d-371">未模擬 NIC。</span><span class="sxs-lookup"><span data-stu-id="9631d-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="9631d-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9631d-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="9631d-373">NIC 會模擬。</span><span class="sxs-lookup"><span data-stu-id="9631d-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="9631d-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="9631d-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-375">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-377">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="9631d-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="9631d-378">當設定為 1 ( "Other" ) 時，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="9631d-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="9631d-379">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，而且一律設定為 1 ( 「其他」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-380">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9631d-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-381">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-383">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="9631d-383">The power management capabilities of the device.</span></span> <span data-ttu-id="9631d-384">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9631d-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-386">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9631d-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-388">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="9631d-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9631d-389">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-390">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9631d-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-391">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-393">自上次電源週期起，此裝置已電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="9631d-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="9631d-394">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-395">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9631d-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-396">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-398">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9631d-398">Provides high level status information.</span></span> <span data-ttu-id="9631d-399">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9631d-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9631d-400">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9631d-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9631d-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="9631d-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-403">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-405">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9631d-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9631d-406">實際的頻寬會以 LogicalPort 報告。</span><span class="sxs-lookup"><span data-stu-id="9631d-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="9631d-407">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))，一律設為1000000000。</span><span class="sxs-lookup"><span data-stu-id="9631d-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9631d-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-409">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-411">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="9631d-412">當 **EnabledState** 設定為5時 ( 「不適用」 ) ，則此屬性不會有任何意義。</span><span class="sxs-lookup"><span data-stu-id="9631d-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="9631d-413">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="9631d-414">**速度**</span><span class="sxs-lookup"><span data-stu-id="9631d-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-415">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9631d-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-417">埠目前的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9631d-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="9631d-418">對於頻寬不同的埠，或無法精確估計的埠，這個屬性應該包含名義的頻寬。</span><span class="sxs-lookup"><span data-stu-id="9631d-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="9631d-419">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1000000000。</span><span class="sxs-lookup"><span data-stu-id="9631d-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-420">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9631d-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-423">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9631d-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-424">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9631d-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-425">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9631d-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9631d-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-427">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="9631d-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9631d-428">這個陣列中的專案與在 **OperationalStatus** 中相同陣列索引的專案相互關聯。</span><span class="sxs-lookup"><span data-stu-id="9631d-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="9631d-429">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="9631d-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9631d-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-431">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-433">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-433">The state of the logical device.</span></span> <span data-ttu-id="9631d-434">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-435">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="9631d-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9631d-438">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="9631d-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9631d-439">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9631d-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="9631d-440">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)，一律設為1500。</span><span class="sxs-lookup"><span data-stu-id="9631d-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-441">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9631d-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-444">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9631d-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="9631d-445">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律會設定為 "Msvm \_ 。</span><span class="sxs-lookup"><span data-stu-id="9631d-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="9631d-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9631d-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-447">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9631d-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-449">**GUID** 形式的虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="9631d-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="9631d-450">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9631d-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9631d-451">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9631d-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-452">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9631d-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-454">專案的 **EnabledState** 上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="9631d-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="9631d-455">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="9631d-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="9631d-456">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="9631d-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="9631d-457">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-458">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9631d-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-461">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="9631d-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9631d-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="9631d-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-463">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9631d-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-464">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-466">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="9631d-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9631d-467">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9631d-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9631d-468">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="9631d-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9631d-469">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9631d-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9631d-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9631d-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9631d-471">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="9631d-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="9631d-472">如果埠的使用沒有限制，則值應該設定為 4 ( 「不受限制」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="9631d-473">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ，而且一律設定為 4 ( 「不受限制」 ) 。</span><span class="sxs-lookup"><span data-stu-id="9631d-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9631d-474">備註</span><span class="sxs-lookup"><span data-stu-id="9631d-474">Remarks</span></span>

<span data-ttu-id="9631d-475">存取 **Msvm \_ EmulatedEthernetPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9631d-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9631d-476">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9631d-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9631d-477">範例</span><span class="sxs-lookup"><span data-stu-id="9631d-477">Examples</span></span>

<span data-ttu-id="9631d-478">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="9631d-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9631d-479">規格需求</span><span class="sxs-lookup"><span data-stu-id="9631d-479">Requirements</span></span>



| <span data-ttu-id="9631d-480">需求</span><span class="sxs-lookup"><span data-stu-id="9631d-480">Requirement</span></span> | <span data-ttu-id="9631d-481">值</span><span class="sxs-lookup"><span data-stu-id="9631d-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9631d-482">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9631d-482">Minimum supported client</span></span><br/> | <span data-ttu-id="9631d-483">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9631d-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9631d-484">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9631d-484">Minimum supported server</span></span><br/> | <span data-ttu-id="9631d-485">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9631d-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9631d-486">命名空間</span><span class="sxs-lookup"><span data-stu-id="9631d-486">Namespace</span></span><br/>                | <span data-ttu-id="9631d-487">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9631d-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9631d-488">MOF</span><span class="sxs-lookup"><span data-stu-id="9631d-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9631d-489"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9631d-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9631d-490">DLL</span><span class="sxs-lookup"><span data-stu-id="9631d-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9631d-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9631d-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9631d-492">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9631d-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9631d-493">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="9631d-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="9631d-494">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="9631d-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


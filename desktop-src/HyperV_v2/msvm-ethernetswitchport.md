---
description: 代表參數上的埠。
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Msvm_EthernetSwitchPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982778"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="1bccc-103">Msvm \_ EthernetSwitchPort 類別</span><span class="sxs-lookup"><span data-stu-id="1bccc-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="1bccc-104">代表參數上的埠。</span><span class="sxs-lookup"><span data-stu-id="1bccc-104">Represents a port on the switch.</span></span>

<span data-ttu-id="1bccc-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bccc-106">語法</span><span class="sxs-lookup"><span data-stu-id="1bccc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="1bccc-107">成員</span><span class="sxs-lookup"><span data-stu-id="1bccc-107">Members</span></span>

<span data-ttu-id="1bccc-108">**Msvm \_ EthernetSwitchPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1bccc-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="1bccc-109">方法</span><span class="sxs-lookup"><span data-stu-id="1bccc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1bccc-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1bccc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1bccc-111">方法</span><span class="sxs-lookup"><span data-stu-id="1bccc-111">Methods</span></span>

<span data-ttu-id="1bccc-112">**Msvm \_ EthernetSwitchPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="1bccc-113">方法</span><span class="sxs-lookup"><span data-stu-id="1bccc-113">Method</span></span>                                                                   | <span data-ttu-id="1bccc-114">描述</span><span class="sxs-lookup"><span data-stu-id="1bccc-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="1bccc-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1bccc-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="1bccc-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1bccc-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="1bccc-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="1bccc-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1bccc-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="1bccc-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="1bccc-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="1bccc-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1bccc-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="1bccc-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="1bccc-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="1bccc-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="1bccc-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="1bccc-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="1bccc-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="1bccc-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="1bccc-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="1bccc-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1bccc-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="1bccc-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="1bccc-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1bccc-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="1bccc-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1bccc-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1bccc-131">屬性</span><span class="sxs-lookup"><span data-stu-id="1bccc-131">Properties</span></span>

<span data-ttu-id="1bccc-132">**Msvm \_ EthernetSwitchPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="1bccc-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-134">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-136">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-137">使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="1bccc-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="1bccc-138">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="1bccc-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-140">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-142">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="1bccc-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-144">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="1bccc-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bccc-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-147">指出埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="1bccc-148">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-149">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1bccc-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-152">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-152">The primary availability and status of the device.</span></span> <span data-ttu-id="1bccc-153">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1bccc-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-155">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-157">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="1bccc-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="1bccc-158">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="1bccc-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="1bccc-159">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="1bccc-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="1bccc-160">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="1bccc-161">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="1bccc-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="1bccc-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="1bccc-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="1bccc-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="1bccc-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="1bccc-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="1bccc-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="1bccc-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="1bccc-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="1bccc-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="1bccc-172">)</span><span class="sxs-lookup"><span data-stu-id="1bccc-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1bccc-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-174">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-176">陣列，指定埠的功能。</span><span class="sxs-lookup"><span data-stu-id="1bccc-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="1bccc-177">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1bccc-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1bccc-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="1bccc-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="1bccc-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="1bccc-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**負載平衡** (5 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1bccc-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-185">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-187">自由格式字串的陣列，可針對 **功能** 陣列中包含的埠功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="1bccc-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="1bccc-188">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的對應專案相關。</span><span class="sxs-lookup"><span data-stu-id="1bccc-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="1bccc-189">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-190">**標題**</span><span class="sxs-lookup"><span data-stu-id="1bccc-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-193">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1bccc-193">A short description of the object.</span></span> <span data-ttu-id="1bccc-194">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，一律設定為「乙太網路交換器埠」。</span><span class="sxs-lookup"><span data-stu-id="1bccc-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-195">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1bccc-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-198">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="1bccc-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1bccc-199">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1bccc-200">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1bccc-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-204">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1bccc-204">The scoping system's creation class name.</span></span> <span data-ttu-id="1bccc-205">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ EthernetSwitchPort"。</span><span class="sxs-lookup"><span data-stu-id="1bccc-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-206">**說明**</span><span class="sxs-lookup"><span data-stu-id="1bccc-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-209">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1bccc-209">A description of the object.</span></span> <span data-ttu-id="1bccc-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 虛擬乙太網路交換器埠」。</span><span class="sxs-lookup"><span data-stu-id="1bccc-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1bccc-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-214">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1bccc-215">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1bccc-216">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1bccc-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-220">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1bccc-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1bccc-221">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1bccc-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-225">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1bccc-225">A display name for the object.</span></span> <span data-ttu-id="1bccc-226">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-227">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1bccc-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-228">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-230">從 **功能** 陣列中所有支援的功能清單中，指定啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="1bccc-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="1bccc-231">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1bccc-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1bccc-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="1bccc-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="1bccc-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="1bccc-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**負載平衡** (5 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1bccc-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-241">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="1bccc-242">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-246">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1bccc-247">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1bccc-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="1bccc-248">值</span><span class="sxs-lookup"><span data-stu-id="1bccc-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="1bccc-249">意義</span><span class="sxs-lookup"><span data-stu-id="1bccc-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1bccc-250"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1bccc-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="1bccc-251">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="1bccc-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1bccc-252"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1bccc-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="1bccc-253">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="1bccc-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1bccc-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1bccc-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-255">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bccc-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-257">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1bccc-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="1bccc-258">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1bccc-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-262">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1bccc-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="1bccc-263">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-264">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="1bccc-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-265">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bccc-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-267">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="1bccc-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="1bccc-268">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-270">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-272">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="1bccc-272">The current health of the element.</span></span> <span data-ttu-id="1bccc-273">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1bccc-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-275">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-277">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1bccc-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="1bccc-278">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1bccc-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-280">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1bccc-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-282">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1bccc-282">The date and time when the object was installed.</span></span> <span data-ttu-id="1bccc-283">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="1bccc-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="1bccc-284">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1bccc-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-288">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1bccc-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-289">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1bccc-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1bccc-290">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-291">**IOVOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="1bccc-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bccc-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-294">目前的 i/o 虛擬化 (的) 卸載此埠上的使用量。</span><span class="sxs-lookup"><span data-stu-id="1bccc-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="1bccc-295">使用方式是埠上使用的 SR-IOV 資源數量。</span><span class="sxs-lookup"><span data-stu-id="1bccc-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1bccc-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-297">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bccc-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-299">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1bccc-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="1bccc-300">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-301">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="1bccc-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-302">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-304">指定埠的連結技術類型。</span><span class="sxs-lookup"><span data-stu-id="1bccc-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="1bccc-305">當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="1bccc-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="1bccc-306">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1bccc-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1bccc-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="1bccc-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-310"><span id="IB"></span><span id="ib"></span>**IB** (3) </span><span class="sxs-lookup"><span data-stu-id="1bccc-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-311"><span id="FC"></span><span id="fc"></span>**FC** (4) </span><span class="sxs-lookup"><span data-stu-id="1bccc-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5) </span><span class="sxs-lookup"><span data-stu-id="1bccc-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6) </span><span class="sxs-lookup"><span data-stu-id="1bccc-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**權杖環** (7) </span><span class="sxs-lookup"><span data-stu-id="1bccc-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (8) </span><span class="sxs-lookup"><span data-stu-id="1bccc-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (9) </span><span class="sxs-lookup"><span data-stu-id="1bccc-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**藍牙** (10) </span><span class="sxs-lookup"><span data-stu-id="1bccc-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**無線區域網路** (11 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-319">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="1bccc-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-320">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bccc-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-322">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="1bccc-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="1bccc-323">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，一律設為1500。</span><span class="sxs-lookup"><span data-stu-id="1bccc-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-324">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="1bccc-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-325">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-327">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="1bccc-327">This property has been deprecated.</span></span> <span data-ttu-id="1bccc-328">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-329">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="1bccc-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-330">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-332">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-333">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1bccc-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1bccc-334">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-335">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1bccc-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-338">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1bccc-338">The label by which the object is known.</span></span> <span data-ttu-id="1bccc-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="1bccc-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-341">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-343">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-344">包含埠之 MAC 位址的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="1bccc-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="1bccc-345">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-346">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1bccc-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-347">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-349">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1bccc-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1bccc-350">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1bccc-351">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1bccc-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-353">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-355">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-355">The current statuses of the object.</span></span> <span data-ttu-id="1bccc-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-357">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1bccc-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-358">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-360">自由格式字串的陣列，可針對指定為 1 (其他) 的任何已啟用功能，提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="1bccc-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="1bccc-361">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-363">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-365">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="1bccc-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1bccc-366">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="1bccc-367">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1bccc-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1bccc-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-369">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-371">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1bccc-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="1bccc-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-373">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="1bccc-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-376">描述 **LinkTechnology** 設定為1， (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="1bccc-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="1bccc-377">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-378">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="1bccc-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-381">使用這個屬性會取代 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="1bccc-382">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-383">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="1bccc-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-384">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-386">描述當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="1bccc-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="1bccc-387">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-388">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="1bccc-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-389">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-391">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-392">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="1bccc-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="1bccc-393">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="1bccc-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="1bccc-394">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="1bccc-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="1bccc-395">如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="1bccc-396">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-397">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="1bccc-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-400">連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1bccc-400">The port number.</span></span> <span data-ttu-id="1bccc-401">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="1bccc-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-403">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-405">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="1bccc-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="1bccc-406">當設定為1時 (其他) ，相關的 **OtherPortType** 屬性會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="1bccc-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="1bccc-407">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1bccc-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1bccc-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="1bccc-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="1bccc-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="1bccc-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="1bccc-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="1bccc-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="1bccc-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="1bccc-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="1bccc-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="1bccc-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="1bccc-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="1bccc-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="1bccc-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="1bccc-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="1bccc-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="1bccc-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="1bccc-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="1bccc-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="1bccc-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="1bccc-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (16，000. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1bccc-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-431">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-433">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="1bccc-433">The power management capabilities of the device.</span></span> <span data-ttu-id="1bccc-434">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1bccc-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-436">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bccc-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-438">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="1bccc-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="1bccc-439">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-440">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1bccc-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-441">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-443">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="1bccc-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="1bccc-444">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-445">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1bccc-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-446">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-448">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1bccc-448">Provides high level status information.</span></span> <span data-ttu-id="1bccc-449">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1bccc-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="1bccc-450">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bccc-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1bccc-451">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1bccc-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-453">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-454">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="1bccc-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-455">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-456">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1bccc-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1bccc-457">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="1bccc-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="1bccc-458">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-460">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-461">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-462">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="1bccc-463">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-464">**速度**</span><span class="sxs-lookup"><span data-stu-id="1bccc-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-465">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-467">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-468">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1bccc-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1bccc-469">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-470">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1bccc-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-471">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-473">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-473">The current status of the object.</span></span> <span data-ttu-id="1bccc-474">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-475">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1bccc-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-476">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bccc-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-478">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="1bccc-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1bccc-479">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1bccc-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-481">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-483">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-483">The current state of the logical device.</span></span> <span data-ttu-id="1bccc-484">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-485">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="1bccc-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-486">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-488">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-489">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1bccc-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="1bccc-490">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1bccc-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-492">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-493">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-494">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1bccc-494">The scoping system's creation class name.</span></span> <span data-ttu-id="1bccc-495">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ VirtualEthernetSwitch"。</span><span class="sxs-lookup"><span data-stu-id="1bccc-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1bccc-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-497">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1bccc-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-498">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-499">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bccc-499">The scoping system's name.</span></span> <span data-ttu-id="1bccc-500">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1bccc-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-501">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1bccc-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-502">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1bccc-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-504">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="1bccc-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1bccc-505">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1bccc-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-506">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1bccc-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-507">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1bccc-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-508">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-509">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="1bccc-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="1bccc-510">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-511">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1bccc-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-512">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-514">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="1bccc-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1bccc-515">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1bccc-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1bccc-516">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="1bccc-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-517">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1bccc-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-518">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-519">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="1bccc-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="1bccc-520">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="1bccc-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="1bccc-521">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="1bccc-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="1bccc-522">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bccc-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1bccc-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1bccc-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="1bccc-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="1bccc-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**不受限制** (4 ) </span><span class="sxs-lookup"><span data-stu-id="1bccc-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bccc-527">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="1bccc-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bccc-528">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bccc-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bccc-529">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1bccc-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bccc-530">目前的虛擬機器佇列 (VMQ) 卸載此埠上的使用量。</span><span class="sxs-lookup"><span data-stu-id="1bccc-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="1bccc-531">使用量是埠上使用的 VMQ 資源數量。</span><span class="sxs-lookup"><span data-stu-id="1bccc-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bccc-532">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bccc-532">Requirements</span></span>



| <span data-ttu-id="1bccc-533">需求</span><span class="sxs-lookup"><span data-stu-id="1bccc-533">Requirement</span></span> | <span data-ttu-id="1bccc-534">值</span><span class="sxs-lookup"><span data-stu-id="1bccc-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bccc-535">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bccc-535">Minimum supported client</span></span><br/> | <span data-ttu-id="1bccc-536">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bccc-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1bccc-537">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bccc-537">Minimum supported server</span></span><br/> | <span data-ttu-id="1bccc-538">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bccc-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bccc-539">命名空間</span><span class="sxs-lookup"><span data-stu-id="1bccc-539">Namespace</span></span><br/>                | <span data-ttu-id="1bccc-540">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1bccc-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1bccc-541">MOF</span><span class="sxs-lookup"><span data-stu-id="1bccc-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bccc-542"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1bccc-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bccc-543">DLL</span><span class="sxs-lookup"><span data-stu-id="1bccc-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bccc-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bccc-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: 代表 (網路介面卡) 的外部乙太網路埠。
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Msvm_ExternalEthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511896"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="04938-103">Msvm \_ ExternalEthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="04938-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="04938-104">代表 (網路介面卡) 的外部乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="04938-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="04938-105">這些類型的乙太網路埠可讓虛擬機器存取外部網路。</span><span class="sxs-lookup"><span data-stu-id="04938-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="04938-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04938-107">語法</span><span class="sxs-lookup"><span data-stu-id="04938-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="04938-108">成員</span><span class="sxs-lookup"><span data-stu-id="04938-108">Members</span></span>

<span data-ttu-id="04938-109">**Msvm \_ ExternalEthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="04938-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="04938-110">方法</span><span class="sxs-lookup"><span data-stu-id="04938-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="04938-111">屬性</span><span class="sxs-lookup"><span data-stu-id="04938-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04938-112">方法</span><span class="sxs-lookup"><span data-stu-id="04938-112">Methods</span></span>

<span data-ttu-id="04938-113">**Msvm \_ ExternalEthernetPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="04938-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="04938-114">方法</span><span class="sxs-lookup"><span data-stu-id="04938-114">Method</span></span>                                                                     | <span data-ttu-id="04938-115">描述</span><span class="sxs-lookup"><span data-stu-id="04938-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="04938-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="04938-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="04938-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04938-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="04938-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="04938-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04938-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="04938-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="04938-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="04938-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="04938-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="04938-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="04938-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="04938-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="04938-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="04938-125">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="04938-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="04938-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="04938-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="04938-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04938-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="04938-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="04938-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04938-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="04938-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="04938-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="04938-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04938-132">屬性</span><span class="sxs-lookup"><span data-stu-id="04938-132">Properties</span></span>

<span data-ttu-id="04938-133">**Msvm \_ ExternalEthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04938-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="04938-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-137">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="04938-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="04938-138">使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="04938-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="04938-139">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="04938-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-141">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-143">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="04938-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="04938-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-145">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="04938-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04938-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04938-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-148">指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="04938-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="04938-149">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="04938-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-153">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-153">The primary availability and status of the device.</span></span> <span data-ttu-id="04938-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="04938-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-158">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="04938-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="04938-159">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="04938-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="04938-160">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="04938-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="04938-161">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="04938-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="04938-162">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="04938-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="04938-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04938-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="04938-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04938-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="04938-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04938-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="04938-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="04938-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="04938-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="04938-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="04938-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="04938-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="04938-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="04938-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="04938-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="04938-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="04938-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="04938-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="04938-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="04938-173">)</span><span class="sxs-lookup"><span data-stu-id="04938-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="04938-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-177">陣列，指定埠的功能。</span><span class="sxs-lookup"><span data-stu-id="04938-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="04938-178">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="04938-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="04938-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04938-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04938-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04938-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04938-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="04938-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04938-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="04938-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04938-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="04938-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04938-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="04938-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04938-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-186">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-188">自由格式字串的陣列，可針對 **功能** 陣列中包含的埠功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="04938-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="04938-189">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的對應專案相關。</span><span class="sxs-lookup"><span data-stu-id="04938-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="04938-190">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="04938-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-191">**標題**</span><span class="sxs-lookup"><span data-stu-id="04938-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-194">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="04938-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="04938-195">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="04938-195">A short description of the object.</span></span> <span data-ttu-id="04938-196">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Ethernet 埠」。</span><span class="sxs-lookup"><span data-stu-id="04938-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="04938-197">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="04938-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-200">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="04938-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="04938-201">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04938-202">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04938-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-206">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="04938-206">The scoping system's creation class name.</span></span> <span data-ttu-id="04938-207">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ ExternalEthernetPort"。</span><span class="sxs-lookup"><span data-stu-id="04938-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="04938-208">**說明**</span><span class="sxs-lookup"><span data-stu-id="04938-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-211">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="04938-211">A description of the object.</span></span> <span data-ttu-id="04938-212">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft External Ethernet Port」。</span><span class="sxs-lookup"><span data-stu-id="04938-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="04938-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="04938-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-214">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-216">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="04938-217">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04938-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="04938-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-222">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="04938-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="04938-223">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="04938-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04938-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="04938-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-227">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="04938-227">A display name for the object.</span></span> <span data-ttu-id="04938-228">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-229">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="04938-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-230">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-232">從 **功能** 陣列中所有支援的功能清單中，指定啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="04938-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="04938-233">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="04938-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="04938-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04938-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04938-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04938-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04938-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="04938-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04938-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="04938-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04938-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="04938-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04938-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="04938-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="04938-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-243">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="04938-244">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="04938-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="04938-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="04938-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-248">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="04938-249">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="04938-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="04938-250">例如，關閉 (4) 並啟動 (10) 是啟用和停用之間的暫時性狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="04938-251">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="04938-252">值</span><span class="sxs-lookup"><span data-stu-id="04938-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="04938-253">意義</span><span class="sxs-lookup"><span data-stu-id="04938-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="04938-254"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04938-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="04938-255"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04938-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="04938-256"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04938-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="04938-257">元素是或可能正在執行命令、將會處理任何已排入佇列的命令，並將新的要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="04938-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="04938-258"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04938-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="04938-259">元素將不會執行命令，而且會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="04938-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="04938-260">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="04938-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="04938-261">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="04938-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="04938-262"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="04938-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="04938-263">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="04938-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="04938-264"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="04938-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="04938-265">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="04938-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="04938-266"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="04938-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="04938-267">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="04938-268"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="04938-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="04938-269">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="04938-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="04938-270"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="04938-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="04938-271">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="04938-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="04938-272">專案的行為類似于已啟用的狀態，但它只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="04938-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="04938-273">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="04938-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="04938-274"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="04938-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="04938-275">元素正在進入已啟用的狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="04938-276">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="04938-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="04938-277"><dt>**DMTF 保留**</dt>的 <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="04938-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="04938-278">保留的。</span><span class="sxs-lookup"><span data-stu-id="04938-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="04938-279"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="04938-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="04938-280">保留的。</span><span class="sxs-lookup"><span data-stu-id="04938-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="04938-281">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="04938-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-282">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04938-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04938-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-284">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="04938-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="04938-285">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="04938-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-289">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="04938-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="04938-290">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-291">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="04938-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-292">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04938-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04938-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-294">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="04938-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="04938-295">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="04938-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-297">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-299">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="04938-299">The current health of the element.</span></span> <span data-ttu-id="04938-300">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="04938-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="04938-301">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="04938-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="04938-302">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="04938-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="04938-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04938-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-304">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-306">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="04938-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="04938-307">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="04938-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-309">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="04938-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04938-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-311">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="04938-311">The date and time when the object was installed.</span></span> <span data-ttu-id="04938-312">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="04938-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="04938-313">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="04938-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-317">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="04938-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="04938-318">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="04938-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="04938-319">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-320">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="04938-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-321">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04938-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04938-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-323">如果此屬性為 **True**，則此乙太網路埠可以連線至交換器，因此可提供虛擬機器的連線。</span><span class="sxs-lookup"><span data-stu-id="04938-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="04938-324">如果此屬性為 **False**，則虛擬機器網路架構不會使用此乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="04938-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="04938-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="04938-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-326">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="04938-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04938-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-328">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="04938-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="04938-329">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-330">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="04938-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-331">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-333">指定埠的連結技術類型。</span><span class="sxs-lookup"><span data-stu-id="04938-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="04938-334">當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="04938-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="04938-335">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="04938-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04938-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04938-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04938-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04938-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="04938-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04938-339"><span id="IB"></span><span id="ib"></span>**IB** (3) </span><span class="sxs-lookup"><span data-stu-id="04938-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04938-340"><span id="FC"></span><span id="fc"></span>**FC** (4) </span><span class="sxs-lookup"><span data-stu-id="04938-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04938-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5) </span><span class="sxs-lookup"><span data-stu-id="04938-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="04938-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6) </span><span class="sxs-lookup"><span data-stu-id="04938-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="04938-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**權杖環** (7) </span><span class="sxs-lookup"><span data-stu-id="04938-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="04938-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (8) </span><span class="sxs-lookup"><span data-stu-id="04938-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="04938-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (9) </span><span class="sxs-lookup"><span data-stu-id="04938-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="04938-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**藍牙** (10) </span><span class="sxs-lookup"><span data-stu-id="04938-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="04938-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**無線區域網路** (11) </span><span class="sxs-lookup"><span data-stu-id="04938-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-348">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="04938-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-349">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="04938-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04938-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-351">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="04938-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="04938-352">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，一律設為1500。</span><span class="sxs-lookup"><span data-stu-id="04938-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="04938-353">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="04938-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-354">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-356">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="04938-356">This property has been deprecated.</span></span> <span data-ttu-id="04938-357">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-358">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="04938-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-359">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-361">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="04938-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="04938-362">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="04938-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="04938-363">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04938-364">**名稱**</span><span class="sxs-lookup"><span data-stu-id="04938-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-367">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="04938-367">The label by which the object is known.</span></span> <span data-ttu-id="04938-368">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="04938-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-370">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-372">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="04938-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="04938-373">包含埠之 MAC 位址的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="04938-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="04938-374">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-375">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="04938-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-378">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="04938-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="04938-379">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04938-380">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="04938-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-382">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-384">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-384">The current statuses of the object.</span></span> <span data-ttu-id="04938-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="04938-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="04938-386">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="04938-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-387">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-389">自由格式字串的陣列，可針對指定為 1 (其他的任何已啟用功能提供更詳細的說明。 ) 此屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="04938-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-390">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="04938-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-393">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="04938-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="04938-394">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="04938-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="04938-395">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04938-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="04938-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-397">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-399">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="04938-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="04938-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-401">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="04938-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-402">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-404">描述 **LinkTechnology** 設定為 1 (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="04938-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="04938-405">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-406">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="04938-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-409">使用這個屬性會取代 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="04938-410">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-411">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="04938-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-414">當 **PortType** 設定為 1 ( "Other" ) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="04938-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="04938-415">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04938-416">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="04938-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-417">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-419">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="04938-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="04938-420">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="04938-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="04938-421">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="04938-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="04938-422">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="04938-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="04938-423">如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="04938-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="04938-424">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-425">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="04938-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-426">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-428">連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="04938-428">The port number.</span></span> <span data-ttu-id="04938-429">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="04938-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-431">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-433">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="04938-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="04938-434">當設定為 1 ( "Other" ) 時，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="04938-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="04938-435">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="04938-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04938-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04938-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="04938-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04938-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="04938-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="04938-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="04938-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="04938-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="04938-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="04938-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="04938-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="04938-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="04938-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="04938-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="04938-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="04938-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="04938-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="04938-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="04938-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="04938-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="04938-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="04938-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="04938-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="04938-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="04938-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="04938-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="04938-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="04938-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="04938-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="04938-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="04938-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="04938-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="04938-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="04938-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="04938-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="04938-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="04938-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="04938-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="04938-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="04938-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="04938-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="04938-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (16000 65535) </span><span class="sxs-lookup"><span data-stu-id="04938-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-458">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="04938-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-459">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-461">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="04938-461">The power management capabilities of the device.</span></span> <span data-ttu-id="04938-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-463">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="04938-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-464">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="04938-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04938-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-466">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="04938-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="04938-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-468">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="04938-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-469">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-471">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="04938-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="04938-472">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-473">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="04938-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-474">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-476">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="04938-476">Provides high level status information.</span></span> <span data-ttu-id="04938-477">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="04938-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="04938-478">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="04938-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04938-479">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04938-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="04938-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-481">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-483">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="04938-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="04938-484">要求的埠頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="04938-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="04938-485">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="04938-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="04938-486">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04938-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="04938-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-488">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-490">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="04938-491">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="04938-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="04938-492">**速度**</span><span class="sxs-lookup"><span data-stu-id="04938-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-493">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-495">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="04938-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="04938-496">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="04938-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="04938-497">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04938-498">**狀態**</span><span class="sxs-lookup"><span data-stu-id="04938-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-501">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-501">The current status of the object.</span></span> <span data-ttu-id="04938-502">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="04938-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="04938-503">正常</span><span class="sxs-lookup"><span data-stu-id="04938-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="04938-504"><span id="OK"></span><span id="ok"></span>**還行**</span><span class="sxs-lookup"><span data-stu-id="04938-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="04938-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤**</span><span class="sxs-lookup"><span data-stu-id="04938-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="04938-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**退化**</span><span class="sxs-lookup"><span data-stu-id="04938-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="04938-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**</span><span class="sxs-lookup"><span data-stu-id="04938-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="04938-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred 失敗**</span><span class="sxs-lookup"><span data-stu-id="04938-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="04938-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始**</span><span class="sxs-lookup"><span data-stu-id="04938-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="04938-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止**</span><span class="sxs-lookup"><span data-stu-id="04938-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="04938-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務**</span><span class="sxs-lookup"><span data-stu-id="04938-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="04938-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**強調**</span><span class="sxs-lookup"><span data-stu-id="04938-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="04938-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span><span class="sxs-lookup"><span data-stu-id="04938-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="04938-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**無連絡人**</span><span class="sxs-lookup"><span data-stu-id="04938-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="04938-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**遺失的通訊**</span><span class="sxs-lookup"><span data-stu-id="04938-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04938-516">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04938-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-517">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="04938-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04938-518">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-519">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="04938-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="04938-520">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="04938-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="04938-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="04938-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-522">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-523">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-524">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-524">The current state of the logical device.</span></span> <span data-ttu-id="04938-525">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-526">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="04938-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-527">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-528">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04938-529">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="04938-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="04938-530">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="04938-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="04938-531">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="04938-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="04938-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04938-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-533">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-535">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="04938-535">The scoping system's creation class name.</span></span> <span data-ttu-id="04938-536">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律會設定為 "Msvm \_ 。</span><span class="sxs-lookup"><span data-stu-id="04938-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="04938-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="04938-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="04938-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04938-539">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-540">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="04938-540">The name of the scoping system.</span></span> <span data-ttu-id="04938-541">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="04938-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04938-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="04938-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-543">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="04938-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04938-544">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-545">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="04938-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="04938-546">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="04938-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04938-547">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="04938-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-548">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="04938-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04938-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-550">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="04938-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="04938-551">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-552">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="04938-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-553">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-554">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-555">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="04938-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="04938-556">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="04938-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04938-557">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="04938-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04938-558">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="04938-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04938-559">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="04938-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04938-560">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="04938-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="04938-561">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="04938-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="04938-562">如果埠的使用沒有限制，則此值應該設定為「不受限制」。</span><span class="sxs-lookup"><span data-stu-id="04938-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="04938-563">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="04938-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="04938-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="04938-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04938-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="04938-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04938-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="04938-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04938-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**不受限制** (4) </span><span class="sxs-lookup"><span data-stu-id="04938-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04938-568">備註</span><span class="sxs-lookup"><span data-stu-id="04938-568">Remarks</span></span>

<span data-ttu-id="04938-569">存取 **Msvm \_ ExternalEthernetPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="04938-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="04938-570">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="04938-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="04938-571">範例</span><span class="sxs-lookup"><span data-stu-id="04938-571">Examples</span></span>

<span data-ttu-id="04938-572">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="04938-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04938-573">規格需求</span><span class="sxs-lookup"><span data-stu-id="04938-573">Requirements</span></span>



| <span data-ttu-id="04938-574">需求</span><span class="sxs-lookup"><span data-stu-id="04938-574">Requirement</span></span> | <span data-ttu-id="04938-575">值</span><span class="sxs-lookup"><span data-stu-id="04938-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04938-576">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04938-576">Minimum supported client</span></span><br/> | <span data-ttu-id="04938-577">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04938-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04938-578">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04938-578">Minimum supported server</span></span><br/> | <span data-ttu-id="04938-579">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04938-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04938-580">命名空間</span><span class="sxs-lookup"><span data-stu-id="04938-580">Namespace</span></span><br/>                | <span data-ttu-id="04938-581">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="04938-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04938-582">MOF</span><span class="sxs-lookup"><span data-stu-id="04938-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04938-583"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="04938-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04938-584">DLL</span><span class="sxs-lookup"><span data-stu-id="04938-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04938-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04938-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04938-586">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04938-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04938-587">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="04938-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="04938-588">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="04938-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


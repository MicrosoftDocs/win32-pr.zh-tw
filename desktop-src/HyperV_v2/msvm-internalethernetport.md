---
description: 代表 (網路介面卡) 的內部乙太網路埠。
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Msvm_InternalEthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690860"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="394f9-103">Msvm \_ InternalEthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="394f9-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="394f9-104">代表 (網路介面卡) 的內部乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="394f9-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="394f9-105">這種類型的乙太網路埠可讓虛擬機器存取執行網路軟體的虛擬化伺服器。</span><span class="sxs-lookup"><span data-stu-id="394f9-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="394f9-106">內部網路介面卡可在離開實體系統之前，先路由傳送或篩選虛擬機器的網路流量。</span><span class="sxs-lookup"><span data-stu-id="394f9-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="394f9-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="394f9-108">語法</span><span class="sxs-lookup"><span data-stu-id="394f9-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="394f9-109">成員</span><span class="sxs-lookup"><span data-stu-id="394f9-109">Members</span></span>

<span data-ttu-id="394f9-110">**Msvm \_ InternalEthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="394f9-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="394f9-111">方法</span><span class="sxs-lookup"><span data-stu-id="394f9-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="394f9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="394f9-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="394f9-113">方法</span><span class="sxs-lookup"><span data-stu-id="394f9-113">Methods</span></span>

<span data-ttu-id="394f9-114">**Msvm \_ InternalEthernetPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="394f9-115">方法</span><span class="sxs-lookup"><span data-stu-id="394f9-115">Method</span></span>                                                                     | <span data-ttu-id="394f9-116">描述</span><span class="sxs-lookup"><span data-stu-id="394f9-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="394f9-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="394f9-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="394f9-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="394f9-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="394f9-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="394f9-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="394f9-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="394f9-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="394f9-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="394f9-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="394f9-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="394f9-124">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="394f9-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="394f9-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="394f9-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="394f9-126">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="394f9-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="394f9-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="394f9-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="394f9-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="394f9-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="394f9-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="394f9-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="394f9-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="394f9-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="394f9-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="394f9-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="394f9-133">屬性</span><span class="sxs-lookup"><span data-stu-id="394f9-133">Properties</span></span>

<span data-ttu-id="394f9-134">**Msvm \_ InternalEthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="394f9-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="394f9-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-138">可以支援的作用中或已協商的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="394f9-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="394f9-139">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="394f9-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-143">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="394f9-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="394f9-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="394f9-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-145">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="394f9-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="394f9-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-148">指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="394f9-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="394f9-149">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="394f9-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-153">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-153">The primary availability and status of the device.</span></span> <span data-ttu-id="394f9-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="394f9-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-158">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="394f9-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="394f9-159">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="394f9-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="394f9-160">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="394f9-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="394f9-161">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="394f9-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="394f9-162">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="394f9-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="394f9-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-164">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-166">乙太網路埠的功能。</span><span class="sxs-lookup"><span data-stu-id="394f9-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="394f9-167">如果列出容錯移轉或負載平衡功能，則必須同時定義 [**cim \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (容錯移轉) 或 [**cim \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (負載平衡) ，才能完全描述該功能。</span><span class="sxs-lookup"><span data-stu-id="394f9-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="394f9-168">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="394f9-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="394f9-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="394f9-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="394f9-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="394f9-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="394f9-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="394f9-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="394f9-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="394f9-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-176">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-178">自由格式字串的陣列，可針對 **功能** 陣列中所指出的任何乙太網路埠功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="394f9-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="394f9-179">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="394f9-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="394f9-180">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-181">**標題**</span><span class="sxs-lookup"><span data-stu-id="394f9-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-184">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="394f9-184">A short description of the object.</span></span> <span data-ttu-id="394f9-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="394f9-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-189">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="394f9-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="394f9-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="394f9-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="394f9-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-195">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="394f9-196">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="394f9-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="394f9-197">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="394f9-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-198">**說明**</span><span class="sxs-lookup"><span data-stu-id="394f9-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-201">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="394f9-201">A description of the object.</span></span> <span data-ttu-id="394f9-202">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="394f9-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-204">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-206">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="394f9-207">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="394f9-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="394f9-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-212">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="394f9-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="394f9-213">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為「Microsoft：*GUID* \\ *裝置特定資料*」。</span><span class="sxs-lookup"><span data-stu-id="394f9-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="394f9-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="394f9-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="394f9-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="394f9-217">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-217">A display name for the object.</span></span> <span data-ttu-id="394f9-218">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="394f9-219">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ，並且是根據主機中的 NIC 所產生。</span><span class="sxs-lookup"><span data-stu-id="394f9-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="394f9-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-221">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-223">從 **功能** 陣列中定義的所有支援專案清單中，指定要啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="394f9-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="394f9-224">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="394f9-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="394f9-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="394f9-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="394f9-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="394f9-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="394f9-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="394f9-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="394f9-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="394f9-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-232">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-234">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="394f9-235">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="394f9-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-239">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="394f9-240">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="394f9-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-242">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="394f9-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-244">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="394f9-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="394f9-245">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="394f9-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-249">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="394f9-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="394f9-250">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 屬性，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="394f9-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-252">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="394f9-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-254">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="394f9-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="394f9-255">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="394f9-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-259">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="394f9-259">The current health of the element.</span></span> <span data-ttu-id="394f9-260">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="394f9-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="394f9-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="394f9-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-263">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-265">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="394f9-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="394f9-266">這個陣列的每個專案都與位於相同索引的 **OtherIdentifyingInfo** 屬性陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="394f9-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="394f9-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="394f9-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-269">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="394f9-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-271">**日期時間** 值，指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="394f9-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="394f9-272">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="394f9-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="394f9-273">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="394f9-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="394f9-277">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="394f9-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="394f9-278">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="394f9-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="394f9-279">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="394f9-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-281">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="394f9-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-283">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="394f9-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="394f9-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="394f9-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-286">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-288">連結的類型。</span><span class="sxs-lookup"><span data-stu-id="394f9-288">The types of links.</span></span> <span data-ttu-id="394f9-289">當設定為1時 (其他) ，相關的屬性 **OtherLinkTechnology** 會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="394f9-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="394f9-290">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="394f9-291">值</span><span class="sxs-lookup"><span data-stu-id="394f9-291">Value</span></span>                                                                        | <span data-ttu-id="394f9-292">意義</span><span class="sxs-lookup"><span data-stu-id="394f9-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="394f9-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="394f9-294">乙太網路</span><span class="sxs-lookup"><span data-stu-id="394f9-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="394f9-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="394f9-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-296">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="394f9-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-298">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="394f9-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="394f9-299">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="394f9-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-301">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-303">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="394f9-303">This property has been deprecated.</span></span> <span data-ttu-id="394f9-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="394f9-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-306">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-308">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="394f9-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="394f9-309">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-310">**名稱**</span><span class="sxs-lookup"><span data-stu-id="394f9-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-313">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="394f9-313">The label by which the object is known.</span></span> <span data-ttu-id="394f9-314">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="394f9-315">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="394f9-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-317">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-319">Ethernet/802.3 MAC 位址格式化為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（以字串的第一個字元的低位順序表示）。 ) 此屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="394f9-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-323">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="394f9-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="394f9-324">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="394f9-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="394f9-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-327">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-329">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-329">The current statuses of the element.</span></span> <span data-ttu-id="394f9-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="394f9-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-332">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-334">自由格式字串的陣列，可針對指定為 1 (其他) 的任何已啟用功能，提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="394f9-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="394f9-335">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="394f9-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-339">描述當 **enabledstate** 屬性設定為 1 (其他時，專案已啟用或停用狀態的字串 ) 。當 **enabledstate** 屬性是1以外的任何值時，必須將此屬性設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="394f9-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="394f9-340">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="394f9-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-342">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-344">除了可用來識別邏輯裝置的裝置識別碼資訊以外的任何資料。</span><span class="sxs-lookup"><span data-stu-id="394f9-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="394f9-345">例如，您可以使用這個屬性來保存裝置的作業系統顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="394f9-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="394f9-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-350">描述 **LinkTechnology** 屬性設定為 1 (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="394f9-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="394f9-351">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="394f9-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-355">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="394f9-355">This property is deprecated.</span></span> <span data-ttu-id="394f9-356">使用 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-356">Use the **PortType** property.</span></span> <span data-ttu-id="394f9-357">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="394f9-358">已淘汰的描述：當 **PortType** 屬性設定為 1 (其他) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="394f9-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="394f9-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-362">當 **PortType** 屬性設定為 1 (其他) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="394f9-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="394f9-363">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="394f9-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="394f9-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="394f9-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-367">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="394f9-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="394f9-368">您可以使用固件升級或軟體設定來變更此位址。</span><span class="sxs-lookup"><span data-stu-id="394f9-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="394f9-369">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="394f9-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="394f9-370">如果網路介面卡沒有任何硬式編碼位址，則應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="394f9-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="394f9-371">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-372">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="394f9-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-373">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-375">網路埠的編號通常相對於邏輯模組或網路元素。</span><span class="sxs-lookup"><span data-stu-id="394f9-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="394f9-376">模擬 Nic 的這個值是1，所有其他 Nic 的值都是0。</span><span class="sxs-lookup"><span data-stu-id="394f9-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="394f9-377">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="394f9-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-379">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-381">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="394f9-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="394f9-382">當設定為1時 (其他) ，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="394f9-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="394f9-383">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="394f9-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="394f9-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="394f9-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="394f9-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="394f9-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="394f9-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="394f9-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="394f9-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="394f9-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="394f9-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="394f9-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="394f9-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="394f9-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="394f9-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="394f9-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="394f9-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="394f9-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="394f9-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="394f9-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="394f9-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="394f9-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="394f9-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="394f9-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (16000 65535) </span><span class="sxs-lookup"><span data-stu-id="394f9-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="394f9-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="394f9-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-407">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-409">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="394f9-409">The power management capabilities of the device.</span></span> <span data-ttu-id="394f9-410">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="394f9-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-412">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="394f9-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-414">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="394f9-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="394f9-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="394f9-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-417">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-419">自上次電源週期起，此裝置已電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="394f9-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="394f9-420">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="394f9-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-422">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-424">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="394f9-424">Provides high level status information.</span></span> <span data-ttu-id="394f9-425">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="394f9-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="394f9-426">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="394f9-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="394f9-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-429">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-431">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="394f9-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="394f9-432">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="394f9-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="394f9-433">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="394f9-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-435">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-437">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="394f9-438">當 [ **EnabledState** ] 屬性設定為5時 (不適用) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="394f9-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="394f9-439">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-440">**速度**</span><span class="sxs-lookup"><span data-stu-id="394f9-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-441">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="394f9-443">限定詞：覆 **寫**、 **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="394f9-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="394f9-444">埠目前的頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="394f9-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="394f9-445">對於頻寬不同的埠，或無法精確估計的埠，這個屬性應該包含名義的頻寬。</span><span class="sxs-lookup"><span data-stu-id="394f9-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="394f9-446">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-447">**狀態**</span><span class="sxs-lookup"><span data-stu-id="394f9-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-450">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-450">The current status of the object.</span></span> <span data-ttu-id="394f9-451">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="394f9-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="394f9-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-453">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="394f9-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="394f9-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-455">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="394f9-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="394f9-456">這個陣列中的專案與在 **OperationalStatus** 中相同陣列索引的專案相互關聯。</span><span class="sxs-lookup"><span data-stu-id="394f9-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="394f9-457">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="394f9-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="394f9-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-461">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-461">The state of the logical device.</span></span> <span data-ttu-id="394f9-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="394f9-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-464">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="394f9-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-466">可支援的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="394f9-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="394f9-467">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="394f9-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="394f9-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-471">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-471">The scoping system's creation class name.</span></span> <span data-ttu-id="394f9-472">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不支援</span><span class="sxs-lookup"><span data-stu-id="394f9-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="394f9-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="394f9-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="394f9-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-476">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="394f9-476">The name of the scoping system.</span></span> <span data-ttu-id="394f9-477">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="394f9-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="394f9-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="394f9-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-479">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="394f9-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-481">上次變更元素的 **EnabledState** 屬性時的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="394f9-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="394f9-482">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="394f9-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="394f9-483">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="394f9-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="394f9-484">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="394f9-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-486">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-488">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="394f9-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="394f9-489">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="394f9-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="394f9-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-491">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-493">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="394f9-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="394f9-494">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="394f9-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="394f9-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="394f9-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="394f9-496">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="394f9-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="394f9-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="394f9-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="394f9-498">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="394f9-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="394f9-499">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="394f9-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="394f9-500">值</span><span class="sxs-lookup"><span data-stu-id="394f9-500">Value</span></span>                                                                        | <span data-ttu-id="394f9-501">意義</span><span class="sxs-lookup"><span data-stu-id="394f9-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="394f9-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="394f9-503">不受限制</span><span class="sxs-lookup"><span data-stu-id="394f9-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="394f9-504">備註</span><span class="sxs-lookup"><span data-stu-id="394f9-504">Remarks</span></span>

<span data-ttu-id="394f9-505">存取 **Msvm \_ InternalEthernetPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="394f9-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="394f9-506">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="394f9-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="394f9-507">範例</span><span class="sxs-lookup"><span data-stu-id="394f9-507">Examples</span></span>

<span data-ttu-id="394f9-508">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="394f9-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="394f9-509">規格需求</span><span class="sxs-lookup"><span data-stu-id="394f9-509">Requirements</span></span>



| <span data-ttu-id="394f9-510">需求</span><span class="sxs-lookup"><span data-stu-id="394f9-510">Requirement</span></span> | <span data-ttu-id="394f9-511">值</span><span class="sxs-lookup"><span data-stu-id="394f9-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394f9-512">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="394f9-512">Minimum supported client</span></span><br/> | <span data-ttu-id="394f9-513">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="394f9-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="394f9-514">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="394f9-514">Minimum supported server</span></span><br/> | <span data-ttu-id="394f9-515">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="394f9-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="394f9-516">命名空間</span><span class="sxs-lookup"><span data-stu-id="394f9-516">Namespace</span></span><br/>                | <span data-ttu-id="394f9-517">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="394f9-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="394f9-518">MOF</span><span class="sxs-lookup"><span data-stu-id="394f9-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="394f9-519"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="394f9-520">DLL</span><span class="sxs-lookup"><span data-stu-id="394f9-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="394f9-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="394f9-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="394f9-522">另請參閱</span><span class="sxs-lookup"><span data-stu-id="394f9-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394f9-523">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="394f9-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="394f9-524">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="394f9-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


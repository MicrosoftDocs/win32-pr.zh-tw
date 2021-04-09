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
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="671d2-103">Msvm \_ InternalEthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="671d2-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="671d2-104">代表 (網路介面卡) 的內部乙太網路埠。</span><span class="sxs-lookup"><span data-stu-id="671d2-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="671d2-105">這種類型的乙太網路埠可讓虛擬機器存取執行網路軟體的虛擬化伺服器。</span><span class="sxs-lookup"><span data-stu-id="671d2-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="671d2-106">內部網路介面卡可在離開實體系統之前，先路由傳送或篩選虛擬機器的網路流量。</span><span class="sxs-lookup"><span data-stu-id="671d2-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="671d2-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="671d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="671d2-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="671d2-109">成員</span><span class="sxs-lookup"><span data-stu-id="671d2-109">Members</span></span>

<span data-ttu-id="671d2-110">**Msvm \_ InternalEthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="671d2-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="671d2-111">方法</span><span class="sxs-lookup"><span data-stu-id="671d2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="671d2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="671d2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="671d2-113">方法</span><span class="sxs-lookup"><span data-stu-id="671d2-113">Methods</span></span>

<span data-ttu-id="671d2-114">**Msvm \_ InternalEthernetPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="671d2-115">方法</span><span class="sxs-lookup"><span data-stu-id="671d2-115">Method</span></span>                                                                     | <span data-ttu-id="671d2-116">描述</span><span class="sxs-lookup"><span data-stu-id="671d2-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="671d2-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="671d2-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="671d2-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="671d2-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="671d2-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="671d2-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="671d2-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="671d2-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="671d2-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="671d2-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="671d2-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="671d2-124">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="671d2-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="671d2-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="671d2-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="671d2-126">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="671d2-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="671d2-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="671d2-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="671d2-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="671d2-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="671d2-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="671d2-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="671d2-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="671d2-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="671d2-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="671d2-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="671d2-133">屬性</span><span class="sxs-lookup"><span data-stu-id="671d2-133">Properties</span></span>

<span data-ttu-id="671d2-134">**Msvm \_ InternalEthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="671d2-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="671d2-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-138">可以支援的作用中或已協商的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="671d2-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="671d2-139">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="671d2-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-143">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="671d2-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="671d2-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="671d2-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-145">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="671d2-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="671d2-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-148">指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="671d2-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="671d2-149">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="671d2-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-153">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-153">The primary availability and status of the device.</span></span> <span data-ttu-id="671d2-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="671d2-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-158">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="671d2-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="671d2-159">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="671d2-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="671d2-160">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="671d2-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="671d2-161">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="671d2-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="671d2-162">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="671d2-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="671d2-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-164">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-166">乙太網路埠的功能。</span><span class="sxs-lookup"><span data-stu-id="671d2-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="671d2-167">如果列出容錯移轉或負載平衡功能，則必須同時定義 [**cim \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (容錯移轉) 或 [**cim \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (負載平衡) ，才能完全描述該功能。</span><span class="sxs-lookup"><span data-stu-id="671d2-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="671d2-168">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="671d2-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="671d2-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="671d2-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="671d2-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="671d2-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="671d2-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="671d2-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="671d2-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="671d2-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-176">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-178">自由格式字串的陣列，可針對 **功能** 陣列中所指出的任何乙太網路埠功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="671d2-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="671d2-179">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="671d2-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="671d2-180">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-181">**標題**</span><span class="sxs-lookup"><span data-stu-id="671d2-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-184">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="671d2-184">A short description of the object.</span></span> <span data-ttu-id="671d2-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="671d2-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-189">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="671d2-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="671d2-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="671d2-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="671d2-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-195">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="671d2-196">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="671d2-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="671d2-197">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="671d2-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-198">**說明**</span><span class="sxs-lookup"><span data-stu-id="671d2-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-201">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="671d2-201">A description of the object.</span></span> <span data-ttu-id="671d2-202">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="671d2-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-204">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-206">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="671d2-207">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="671d2-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="671d2-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-212">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="671d2-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="671d2-213">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為「Microsoft：*GUID* \\ *裝置特定資料*」。</span><span class="sxs-lookup"><span data-stu-id="671d2-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="671d2-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="671d2-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-216">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="671d2-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="671d2-217">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-217">A display name for the object.</span></span> <span data-ttu-id="671d2-218">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="671d2-219">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ，並且是根據主機中的 NIC 所產生。</span><span class="sxs-lookup"><span data-stu-id="671d2-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="671d2-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-221">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-223">從 **功能** 陣列中定義的所有支援專案清單中，指定要啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="671d2-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="671d2-224">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="671d2-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="671d2-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="671d2-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2) </span><span class="sxs-lookup"><span data-stu-id="671d2-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3) </span><span class="sxs-lookup"><span data-stu-id="671d2-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**容錯移轉** (4) </span><span class="sxs-lookup"><span data-stu-id="671d2-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**負載平衡** (5) </span><span class="sxs-lookup"><span data-stu-id="671d2-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="671d2-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="671d2-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-232">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-234">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="671d2-235">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="671d2-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-239">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="671d2-240">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="671d2-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-242">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="671d2-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-244">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="671d2-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="671d2-245">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="671d2-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-249">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="671d2-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="671d2-250">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 屬性，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="671d2-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-252">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="671d2-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-254">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="671d2-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="671d2-255">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="671d2-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-259">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="671d2-259">The current health of the element.</span></span> <span data-ttu-id="671d2-260">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="671d2-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="671d2-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="671d2-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-263">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-265">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="671d2-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="671d2-266">這個陣列的每個專案都與位於相同索引的 **OtherIdentifyingInfo** 屬性陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="671d2-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="671d2-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="671d2-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-269">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="671d2-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-271">**日期時間** 值，指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="671d2-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="671d2-272">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="671d2-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="671d2-273">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="671d2-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="671d2-277">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="671d2-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="671d2-278">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="671d2-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="671d2-279">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="671d2-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-281">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="671d2-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-283">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="671d2-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="671d2-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="671d2-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-286">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-288">連結的類型。</span><span class="sxs-lookup"><span data-stu-id="671d2-288">The types of links.</span></span> <span data-ttu-id="671d2-289">當設定為1時 (其他) ，相關的屬性 **OtherLinkTechnology** 會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="671d2-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="671d2-290">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="671d2-291">值</span><span class="sxs-lookup"><span data-stu-id="671d2-291">Value</span></span>                                                                        | <span data-ttu-id="671d2-292">意義</span><span class="sxs-lookup"><span data-stu-id="671d2-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="671d2-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="671d2-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="671d2-294">乙太網路</span><span class="sxs-lookup"><span data-stu-id="671d2-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="671d2-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="671d2-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-296">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="671d2-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-298">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="671d2-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="671d2-299">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="671d2-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-301">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-303">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="671d2-303">This property has been deprecated.</span></span> <span data-ttu-id="671d2-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="671d2-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-306">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-308">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="671d2-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="671d2-309">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-310">**名稱**</span><span class="sxs-lookup"><span data-stu-id="671d2-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-313">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="671d2-313">The label by which the object is known.</span></span> <span data-ttu-id="671d2-314">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="671d2-315">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="671d2-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-317">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-319">Ethernet/802.3 MAC 位址格式化為十二個十六進位數位 (例如 "010203040506" ) ，其中每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（以字串的第一個字元的低位順序表示）。 ) 此屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="671d2-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-323">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="671d2-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="671d2-324">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="671d2-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="671d2-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-327">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-329">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-329">The current statuses of the element.</span></span> <span data-ttu-id="671d2-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="671d2-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-332">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-334">自由格式字串的陣列，可針對指定為 1 (其他) 的任何已啟用功能，提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="671d2-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="671d2-335">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="671d2-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-339">描述當 **enabledstate** 屬性設定為 1 (其他時，專案已啟用或停用狀態的字串 ) 。當 **enabledstate** 屬性是1以外的任何值時，必須將此屬性設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="671d2-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="671d2-340">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="671d2-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-342">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-344">除了可用來識別邏輯裝置的裝置識別碼資訊以外的任何資料。</span><span class="sxs-lookup"><span data-stu-id="671d2-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="671d2-345">例如，您可以使用這個屬性來保存裝置的作業系統顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="671d2-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="671d2-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-350">描述 **LinkTechnology** 屬性設定為 1 (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="671d2-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="671d2-351">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="671d2-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-355">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="671d2-355">This property is deprecated.</span></span> <span data-ttu-id="671d2-356">使用 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-356">Use the **PortType** property.</span></span> <span data-ttu-id="671d2-357">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="671d2-358">已淘汰的描述：當 **PortType** 屬性設定為 1 (其他) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="671d2-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="671d2-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-362">當 **PortType** 屬性設定為 1 (其他) 時，模組的類型。</span><span class="sxs-lookup"><span data-stu-id="671d2-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="671d2-363">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="671d2-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="671d2-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="671d2-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-365">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-367">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="671d2-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="671d2-368">您可以使用固件升級或軟體設定來變更此位址。</span><span class="sxs-lookup"><span data-stu-id="671d2-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="671d2-369">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="671d2-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="671d2-370">如果網路介面卡沒有任何硬式編碼位址，則應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="671d2-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="671d2-371">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-372">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="671d2-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-373">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-375">網路埠的編號通常相對於邏輯模組或網路元素。</span><span class="sxs-lookup"><span data-stu-id="671d2-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="671d2-376">模擬 Nic 的這個值是1，所有其他 Nic 的值都是0。</span><span class="sxs-lookup"><span data-stu-id="671d2-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="671d2-377">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="671d2-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-379">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-381">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="671d2-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="671d2-382">當設定為1時 (其他) ，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="671d2-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="671d2-383">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="671d2-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="671d2-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="671d2-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="671d2-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="671d2-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="671d2-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="671d2-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="671d2-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="671d2-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="671d2-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="671d2-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="671d2-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="671d2-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="671d2-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="671d2-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="671d2-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="671d2-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="671d2-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="671d2-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="671d2-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="671d2-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="671d2-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="671d2-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (16000 65535) </span><span class="sxs-lookup"><span data-stu-id="671d2-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="671d2-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="671d2-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-407">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-409">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="671d2-409">The power management capabilities of the device.</span></span> <span data-ttu-id="671d2-410">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="671d2-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-412">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="671d2-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-414">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="671d2-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="671d2-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="671d2-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-417">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-419">自上次電源週期起，此裝置已電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="671d2-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="671d2-420">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="671d2-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-422">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-424">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="671d2-424">Provides high level status information.</span></span> <span data-ttu-id="671d2-425">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="671d2-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="671d2-426">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="671d2-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="671d2-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-429">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-431">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="671d2-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="671d2-432">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="671d2-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="671d2-433">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="671d2-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-435">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-437">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="671d2-438">當 [ **EnabledState** ] 屬性設定為5時 (不適用) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="671d2-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="671d2-439">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-440">**速度**</span><span class="sxs-lookup"><span data-stu-id="671d2-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-441">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="671d2-443">限定詞：覆 **寫**、 **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="671d2-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="671d2-444">埠目前的頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="671d2-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="671d2-445">對於頻寬不同的埠，或無法精確估計的埠，這個屬性應該包含名義的頻寬。</span><span class="sxs-lookup"><span data-stu-id="671d2-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="671d2-446">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-447">**狀態**</span><span class="sxs-lookup"><span data-stu-id="671d2-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-450">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-450">The current status of the object.</span></span> <span data-ttu-id="671d2-451">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="671d2-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="671d2-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-453">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="671d2-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="671d2-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-455">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="671d2-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="671d2-456">這個陣列中的專案與在 **OperationalStatus** 中相同陣列索引的專案相互關聯。</span><span class="sxs-lookup"><span data-stu-id="671d2-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="671d2-457">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="671d2-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="671d2-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-461">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-461">The state of the logical device.</span></span> <span data-ttu-id="671d2-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="671d2-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-464">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="671d2-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-466">可支援的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="671d2-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="671d2-467">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="671d2-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="671d2-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-471">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-471">The scoping system's creation class name.</span></span> <span data-ttu-id="671d2-472">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不支援</span><span class="sxs-lookup"><span data-stu-id="671d2-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="671d2-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="671d2-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="671d2-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-476">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="671d2-476">The name of the scoping system.</span></span> <span data-ttu-id="671d2-477">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="671d2-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="671d2-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="671d2-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-479">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="671d2-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-481">上次變更元素的 **EnabledState** 屬性時的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="671d2-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="671d2-482">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="671d2-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="671d2-483">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="671d2-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="671d2-484">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="671d2-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-486">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-488">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="671d2-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="671d2-489">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="671d2-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="671d2-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-491">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-493">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="671d2-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="671d2-494">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="671d2-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="671d2-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="671d2-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671d2-496">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="671d2-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="671d2-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="671d2-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671d2-498">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="671d2-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="671d2-499">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="671d2-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="671d2-500">值</span><span class="sxs-lookup"><span data-stu-id="671d2-500">Value</span></span>                                                                        | <span data-ttu-id="671d2-501">意義</span><span class="sxs-lookup"><span data-stu-id="671d2-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="671d2-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="671d2-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="671d2-503">不受限制</span><span class="sxs-lookup"><span data-stu-id="671d2-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="671d2-504">備註</span><span class="sxs-lookup"><span data-stu-id="671d2-504">Remarks</span></span>

<span data-ttu-id="671d2-505">存取 **Msvm \_ InternalEthernetPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="671d2-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="671d2-506">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="671d2-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="671d2-507">範例</span><span class="sxs-lookup"><span data-stu-id="671d2-507">Examples</span></span>

<span data-ttu-id="671d2-508">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="671d2-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="671d2-509">規格需求</span><span class="sxs-lookup"><span data-stu-id="671d2-509">Requirements</span></span>



| <span data-ttu-id="671d2-510">需求</span><span class="sxs-lookup"><span data-stu-id="671d2-510">Requirement</span></span> | <span data-ttu-id="671d2-511">值</span><span class="sxs-lookup"><span data-stu-id="671d2-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671d2-512">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="671d2-512">Minimum supported client</span></span><br/> | <span data-ttu-id="671d2-513">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671d2-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="671d2-514">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="671d2-514">Minimum supported server</span></span><br/> | <span data-ttu-id="671d2-515">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671d2-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="671d2-516">命名空間</span><span class="sxs-lookup"><span data-stu-id="671d2-516">Namespace</span></span><br/>                | <span data-ttu-id="671d2-517">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="671d2-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="671d2-518">MOF</span><span class="sxs-lookup"><span data-stu-id="671d2-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="671d2-519"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="671d2-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="671d2-520">DLL</span><span class="sxs-lookup"><span data-stu-id="671d2-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671d2-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="671d2-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="671d2-522">另請參閱</span><span class="sxs-lookup"><span data-stu-id="671d2-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671d2-523">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="671d2-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="671d2-524">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="671d2-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


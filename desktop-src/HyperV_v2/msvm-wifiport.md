---
description: 代表可系結至虛擬交換器的實體 Wi-Fi (802.11) 網路介面卡，以提供虛擬機器的外部網路連線能力。
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Msvm_WiFiPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945428"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="f6cb1-103">Msvm \_ WiFiPort 類別</span><span class="sxs-lookup"><span data-stu-id="f6cb1-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="f6cb1-104">代表可系結至虛擬交換器的實體 Wi-Fi (802.11) 網路介面卡，以提供虛擬機器的外部網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="f6cb1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6cb1-106">語法</span><span class="sxs-lookup"><span data-stu-id="f6cb1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="f6cb1-107">成員</span><span class="sxs-lookup"><span data-stu-id="f6cb1-107">Members</span></span>

<span data-ttu-id="f6cb1-108">**Msvm \_ WiFiPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f6cb1-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="f6cb1-109">方法</span><span class="sxs-lookup"><span data-stu-id="f6cb1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6cb1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f6cb1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6cb1-111">方法</span><span class="sxs-lookup"><span data-stu-id="f6cb1-111">Methods</span></span>

<span data-ttu-id="f6cb1-112">**Msvm \_ WiFiPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="f6cb1-113">方法</span><span class="sxs-lookup"><span data-stu-id="f6cb1-113">Method</span></span>                 | <span data-ttu-id="f6cb1-114">描述</span><span class="sxs-lookup"><span data-stu-id="f6cb1-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="f6cb1-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-115">**EnableDevice**</span></span>       | <span data-ttu-id="f6cb1-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-117">**OnlineDevice**</span></span>       | <span data-ttu-id="f6cb1-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="f6cb1-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-121">**RequestStateChange**</span></span> | <span data-ttu-id="f6cb1-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-123">**Reset**</span></span>              | <span data-ttu-id="f6cb1-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-125">**RestoreProperties**</span></span>  | <span data-ttu-id="f6cb1-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-127">**SaveProperties**</span></span>     | <span data-ttu-id="f6cb1-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="f6cb1-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-129">**SetPowerState**</span></span>      | <span data-ttu-id="f6cb1-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f6cb1-131">屬性</span><span class="sxs-lookup"><span data-stu-id="f6cb1-131">Properties</span></span>

<span data-ttu-id="f6cb1-132">**Msvm \_ WiFiPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6cb1-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-134">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-136">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-137">使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="f6cb1-138">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-140">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-142">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="f6cb1-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-144">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-147">指出埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="f6cb1-148">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-149">**可用性**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-152">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-152">The primary availability and status of the device.</span></span> <span data-ttu-id="f6cb1-153">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-155">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-157">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="f6cb1-158">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="f6cb1-159">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="f6cb1-160">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="f6cb1-161">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f6cb1-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="f6cb1-172">)</span><span class="sxs-lookup"><span data-stu-id="f6cb1-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6cb1-173">**標題**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-176">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-176">A short description of the object.</span></span> <span data-ttu-id="f6cb1-177">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-178">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-181">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f6cb1-182">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6cb1-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-187">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-187">The scoping system's creation class name.</span></span> <span data-ttu-id="f6cb1-188">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-189">**說明**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-192">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-192">A description of the object.</span></span> <span data-ttu-id="f6cb1-193">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-195">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-197">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f6cb1-198">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6cb1-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-203">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="f6cb1-204">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-208">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-208">A display name for the object.</span></span> <span data-ttu-id="f6cb1-209">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-213">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="f6cb1-214">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-216">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-218">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="f6cb1-219">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="f6cb1-220">值</span><span class="sxs-lookup"><span data-stu-id="f6cb1-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="f6cb1-221">意義</span><span class="sxs-lookup"><span data-stu-id="f6cb1-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="f6cb1-222"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f6cb1-223">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f6cb1-224"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f6cb1-225">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6cb1-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-227">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-229">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="f6cb1-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-234">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="f6cb1-235">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-236">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-237">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-239">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="f6cb1-240">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-242">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-244">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-244">The current health of the element.</span></span> <span data-ttu-id="f6cb1-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-247">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-249">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="f6cb1-250">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-252">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-254">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-254">The date and time when the object was installed.</span></span> <span data-ttu-id="f6cb1-255">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="f6cb1-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-260">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-261">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6cb1-262">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-263">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-264">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-266">指定 Wi-Fi 埠是否系結至虛擬機器網路架構。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="f6cb1-267">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-267">This will be one of the following values.</span></span>



| <span data-ttu-id="f6cb1-268">值</span><span class="sxs-lookup"><span data-stu-id="f6cb1-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="f6cb1-269">意義</span><span class="sxs-lookup"><span data-stu-id="f6cb1-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="f6cb1-270"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="f6cb1-271">Wi-Fi 埠會系結至虛擬機器網路架構。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="f6cb1-272"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="f6cb1-273">Wi-Fi 埠未系結至虛擬機器網路架構。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f6cb1-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-275">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-277">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="f6cb1-278">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-279">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-280">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-282">指定埠的連結技術類型。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="f6cb1-283">當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="f6cb1-284">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="f6cb1-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-288"><span id="IB"></span><span id="ib"></span>**IB** (3) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-289"><span id="FC"></span><span id="fc"></span>**FC** (4) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**權杖環** (7) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (8) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (9) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**藍牙** (10) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**無線區域網路** (11 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6cb1-297">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-298">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-300">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-300">This property has been deprecated.</span></span> <span data-ttu-id="f6cb1-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-302">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-303">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-305">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-306">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f6cb1-307">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-308">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-311">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-311">The label by which the object is known.</span></span> <span data-ttu-id="f6cb1-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-314">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-316">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-317">包含埠之 MAC 位址的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="f6cb1-318">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-319">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-320">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-322">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f6cb1-323">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6cb1-324">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-326">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-328">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-328">The current statuses of the object.</span></span> <span data-ttu-id="f6cb1-329">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-330">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-333">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="f6cb1-334">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="f6cb1-335">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-337">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-339">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="f6cb1-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-344">描述 **LinkTechnology** 設定為1， (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="f6cb1-345">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-349">使用這個屬性會取代 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="f6cb1-350">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-351">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-354">描述當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="f6cb1-355">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-356">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-357">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-359">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-360">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="f6cb1-361">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="f6cb1-362">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="f6cb1-363">如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="f6cb1-364">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-365">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-366">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-368">連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-368">The port number.</span></span> <span data-ttu-id="f6cb1-369">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-371">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-373">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="f6cb1-374">當設定為1時 (其他) ，相關的 **OtherPortType** 屬性會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="f6cb1-375">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f6cb1-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (16，000. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6cb1-398">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-399">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-401">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-401">The power management capabilities of the device.</span></span> <span data-ttu-id="f6cb1-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-403">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-404">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-406">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="f6cb1-407">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-408">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-409">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-411">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="f6cb1-412">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-413">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-414">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-416">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-416">Provides high level status information.</span></span> <span data-ttu-id="f6cb1-417">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="f6cb1-418">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6cb1-419">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-421">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-422">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="f6cb1-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-423">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-424">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f6cb1-425">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="f6cb1-426">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-428">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-430">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="f6cb1-431">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-432">**速度**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-433">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-435">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-436">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="f6cb1-437">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-438">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-441">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-441">The current status of the object.</span></span> <span data-ttu-id="f6cb1-442">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-443">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-444">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f6cb1-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-446">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f6cb1-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-449">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-451">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-451">The current state of the logical device.</span></span> <span data-ttu-id="f6cb1-452">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-453">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-454">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-456">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-457">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="f6cb1-458">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-459">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-460">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-461">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-462">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-462">The scoping system's creation class name.</span></span> <span data-ttu-id="f6cb1-463">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-465">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-467">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-467">The scoping system's name.</span></span> <span data-ttu-id="f6cb1-468">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-469">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-470">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-471">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-472">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f6cb1-473">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-474">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-475">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-477">此裝置開機的總時數。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="f6cb1-478">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-479">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-480">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-482">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f6cb1-483">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f6cb1-484">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6cb1-485">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f6cb1-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6cb1-487">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="f6cb1-488">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="f6cb1-489">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="f6cb1-490">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f6cb1-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f6cb1-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="f6cb1-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6cb1-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**不受限制** (4 ) </span><span class="sxs-lookup"><span data-stu-id="f6cb1-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6cb1-495">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6cb1-495">Requirements</span></span>



| <span data-ttu-id="f6cb1-496">需求</span><span class="sxs-lookup"><span data-stu-id="f6cb1-496">Requirement</span></span> | <span data-ttu-id="f6cb1-497">值</span><span class="sxs-lookup"><span data-stu-id="f6cb1-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6cb1-498">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6cb1-498">Minimum supported client</span></span><br/> | <span data-ttu-id="f6cb1-499">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6cb1-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6cb1-500">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6cb1-500">Minimum supported server</span></span><br/> | <span data-ttu-id="f6cb1-501">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6cb1-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6cb1-502">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6cb1-502">Namespace</span></span><br/>                | <span data-ttu-id="f6cb1-503">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6cb1-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6cb1-504">MOF</span><span class="sxs-lookup"><span data-stu-id="f6cb1-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6cb1-505"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6cb1-506">DLL</span><span class="sxs-lookup"><span data-stu-id="f6cb1-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6cb1-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6cb1-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


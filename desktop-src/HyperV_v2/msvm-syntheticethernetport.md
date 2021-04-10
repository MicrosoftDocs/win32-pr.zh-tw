---
description: 代表綜合乙太網路介面卡。
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Msvm_SyntheticEthernetPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848669"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="d7104-103">Msvm \_ SyntheticEthernetPort 類別</span><span class="sxs-lookup"><span data-stu-id="d7104-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="d7104-104">代表綜合乙太網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="d7104-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="d7104-105">此介面卡是慣用的網路介面卡，因為它的效能很高，因為它的變更可能會立即生效，但使用 (熱可配置) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="d7104-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7104-107">語法</span><span class="sxs-lookup"><span data-stu-id="d7104-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="d7104-108">成員</span><span class="sxs-lookup"><span data-stu-id="d7104-108">Members</span></span>

<span data-ttu-id="d7104-109">**Msvm \_ SyntheticEthernetPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7104-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d7104-110">方法</span><span class="sxs-lookup"><span data-stu-id="d7104-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7104-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d7104-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7104-112">方法</span><span class="sxs-lookup"><span data-stu-id="d7104-112">Methods</span></span>

<span data-ttu-id="d7104-113">**Msvm \_ SyntheticEthernetPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="d7104-114">方法</span><span class="sxs-lookup"><span data-stu-id="d7104-114">Method</span></span>                                                                      | <span data-ttu-id="d7104-115">描述</span><span class="sxs-lookup"><span data-stu-id="d7104-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d7104-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d7104-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="d7104-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d7104-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d7104-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="d7104-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d7104-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d7104-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="d7104-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d7104-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d7104-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="d7104-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="d7104-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d7104-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="d7104-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="d7104-125">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="d7104-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="d7104-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="d7104-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="d7104-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d7104-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d7104-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="d7104-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d7104-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d7104-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="d7104-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7104-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7104-132">屬性</span><span class="sxs-lookup"><span data-stu-id="d7104-132">Properties</span></span>

<span data-ttu-id="d7104-133">**Msvm \_ SyntheticEthernetPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7104-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d7104-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-137">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="d7104-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d7104-138">可以支援的作用中或已協商的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d7104-139">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d7104-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-143">裝置的其他可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="d7104-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="d7104-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-145">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="d7104-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7104-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-148">指出網路埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="d7104-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="d7104-149">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="d7104-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-153">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-153">The primary availability and status of the device.</span></span> <span data-ttu-id="d7104-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d7104-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d7104-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-156">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-158">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="d7104-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="d7104-159">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="d7104-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="d7104-160">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="d7104-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="d7104-161">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d7104-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="d7104-162">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d7104-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="d7104-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="d7104-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="d7104-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="d7104-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="d7104-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="d7104-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="d7104-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="d7104-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="d7104-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d7104-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="d7104-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d7104-173">)</span><span class="sxs-lookup"><span data-stu-id="d7104-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d7104-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d7104-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-177">Ethernet 埠的功能。</span><span class="sxs-lookup"><span data-stu-id="d7104-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="d7104-178">例如，裝置可能支援 AlertOnLan、WakeOnLan、負載平衡或容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="d7104-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="d7104-179">如果列出容錯移轉或負載平衡功能，則應該也要定義 SpareGroup (容錯移轉) 或 ExtraCapacityGroup (負載平衡) ，以完整描述該功能。</span><span class="sxs-lookup"><span data-stu-id="d7104-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="d7104-180">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="d7104-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d7104-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-182">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-184">自由格式字串的陣列，可針對 **功能** 屬性陣列中所指出的任何 EthernetPort 功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="d7104-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="d7104-185">請注意，這個陣列的每個專案都與位於相同索引的 [ **功能** ] 屬性陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="d7104-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="d7104-186">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="d7104-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-187">**標題**</span><span class="sxs-lookup"><span data-stu-id="d7104-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-190">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d7104-190">A short description of the object.</span></span> <span data-ttu-id="d7104-191">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d7104-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-195">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="d7104-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d7104-196">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d7104-197">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d7104-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-201">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7104-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="d7104-202">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d7104-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-203">**說明**</span><span class="sxs-lookup"><span data-stu-id="d7104-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-206">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d7104-206">A description of the object.</span></span> <span data-ttu-id="d7104-207">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d7104-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-209">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-211">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d7104-212">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d7104-213">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d7104-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-217">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="d7104-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="d7104-218">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d7104-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d7104-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-222">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d7104-222">A display name for the object.</span></span> <span data-ttu-id="d7104-223">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d7104-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-225">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-227">從所有支援的專案清單中啟用的功能，這些功能是在 [ **功能** ] 屬性陣列中定義。</span><span class="sxs-lookup"><span data-stu-id="d7104-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="d7104-228">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d7104-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-230">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-232">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d7104-233">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d7104-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-235">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-237">此元素的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="d7104-238">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d7104-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-240">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7104-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-242">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d7104-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-246">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="d7104-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-248">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7104-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-250">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="d7104-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="d7104-251">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d7104-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-255">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="d7104-255">The current health of the element.</span></span> <span data-ttu-id="d7104-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d7104-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-258">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-260">自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d7104-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="d7104-261">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="d7104-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d7104-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-263">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d7104-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-265">將乙太網路埠新增到虛擬機器的日期。</span><span class="sxs-lookup"><span data-stu-id="d7104-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="d7104-266">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d7104-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-270">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d7104-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d7104-271">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d7104-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d7104-272">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d7104-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-274">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d7104-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-276">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d7104-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-278">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-280">連結類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="d7104-280">An enumeration of the types of links.</span></span> <span data-ttu-id="d7104-281">當設定為1時 (其他) ，相關的屬性 **OtherLinkTechnology** 會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="d7104-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="d7104-282">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="d7104-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="d7104-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d7104-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="d7104-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d7104-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-287">將接收或傳送的資訊 (非 MAC) 欄位的大小上限。</span><span class="sxs-lookup"><span data-stu-id="d7104-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="d7104-288">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d7104-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-290">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="d7104-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-294">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-296">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="d7104-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d7104-297">埠的最大頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7104-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="d7104-298">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-299">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d7104-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-302">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d7104-302">A display name for the object.</span></span> <span data-ttu-id="d7104-303">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="d7104-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-305">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-307">Ethernet/802.3 MAC 位址格式化為12個十六進位數位 (例如 "010203040506" ) ，每一組代表以標準位 (順序表示之 MAC 位址的六個八位八位組中的其中一個（以字串) 的第一個字元的低序位位表示）。</span><span class="sxs-lookup"><span data-stu-id="d7104-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="d7104-308">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d7104-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-310">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-312">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d7104-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d7104-313">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d7104-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d7104-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-316">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-318">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-318">The current status of the element.</span></span> <span data-ttu-id="d7104-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d7104-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-321">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-323">自由格式字串的陣列，可針對指定為「其他」的任何已啟用功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="d7104-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="d7104-324">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="d7104-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d7104-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-328">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d7104-329">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d7104-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-331">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-333">除了可用來識別邏輯裝置的裝置識別碼資訊以外的任何資料。</span><span class="sxs-lookup"><span data-stu-id="d7104-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d7104-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="d7104-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="d7104-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-338">描述 **LinkTechnology** 設定為 1 (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="d7104-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="d7104-339">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="d7104-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-341">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-343">這個屬性會繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d7104-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="d7104-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-347">當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="d7104-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="d7104-348">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="d7104-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-352">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="d7104-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="d7104-353">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="d7104-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="d7104-354">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="d7104-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="d7104-355">如果網路介面卡沒有任何硬式編碼位址存在， **PermanentAddress** 屬性應該保留空白。</span><span class="sxs-lookup"><span data-stu-id="d7104-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="d7104-356">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-357">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="d7104-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-358">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-360">網路埠的編號通常相對於邏輯模組或網路元素。</span><span class="sxs-lookup"><span data-stu-id="d7104-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="d7104-361">模擬 Nic 的這個值是1，所有其他 Nic 的值都是0。</span><span class="sxs-lookup"><span data-stu-id="d7104-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="d7104-362">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="d7104-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-364">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-366">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="d7104-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="d7104-367">當設定為1時 (其他) ，相關的屬性 **OtherPortType** 會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="d7104-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="d7104-368">這個屬性繼承自 [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d7104-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-370">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d7104-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-374">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d7104-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-376">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d7104-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-378">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-380">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d7104-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-382">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-384">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d7104-384">Provides high level status information.</span></span> <span data-ttu-id="d7104-385">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d7104-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d7104-386">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7104-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d7104-387">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d7104-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-389">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-391">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="d7104-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d7104-392">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7104-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d7104-393">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="d7104-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="d7104-394">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d7104-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-396">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-398">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="d7104-399">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-400">**速度**</span><span class="sxs-lookup"><span data-stu-id="d7104-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-401">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-403">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="d7104-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="d7104-404">埠目前的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7104-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="d7104-405">對於頻寬不同的埠，或無法精確估計的埠，這個屬性應該包含名義的頻寬。</span><span class="sxs-lookup"><span data-stu-id="d7104-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="d7104-406">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-407">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d7104-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-410">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-410">The current status of the element.</span></span> <span data-ttu-id="d7104-411">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d7104-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-413">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d7104-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d7104-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-415">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="d7104-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d7104-416">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d7104-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d7104-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-418">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-420">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="d7104-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-422">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7104-424">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="d7104-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d7104-425">可支援的最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="d7104-426">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="d7104-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d7104-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-430">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="d7104-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="d7104-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d7104-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d7104-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d7104-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-435">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="d7104-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="d7104-436">這個屬性會包含 **GUID** 形式的虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7104-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="d7104-437">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d7104-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d7104-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-439">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d7104-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-441">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="d7104-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d7104-442">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d7104-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-444">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d7104-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-446">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d7104-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7104-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d7104-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-448">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-450">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d7104-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d7104-451">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d7104-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="d7104-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7104-453">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d7104-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d7104-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d7104-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7104-455">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="d7104-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="d7104-456">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="d7104-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="d7104-457">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d7104-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7104-458">備註</span><span class="sxs-lookup"><span data-stu-id="d7104-458">Remarks</span></span>

<span data-ttu-id="d7104-459">存取 **Msvm \_ SyntheticEthernetPort** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="d7104-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d7104-460">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="d7104-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d7104-461">範例</span><span class="sxs-lookup"><span data-stu-id="d7104-461">Examples</span></span>

<span data-ttu-id="d7104-462">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="d7104-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7104-463">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7104-463">Requirements</span></span>



| <span data-ttu-id="d7104-464">需求</span><span class="sxs-lookup"><span data-stu-id="d7104-464">Requirement</span></span> | <span data-ttu-id="d7104-465">值</span><span class="sxs-lookup"><span data-stu-id="d7104-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7104-466">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7104-466">Minimum supported client</span></span><br/> | <span data-ttu-id="d7104-467">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7104-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d7104-468">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7104-468">Minimum supported server</span></span><br/> | <span data-ttu-id="d7104-469">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7104-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7104-470">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7104-470">Namespace</span></span><br/>                | <span data-ttu-id="d7104-471">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d7104-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d7104-472">MOF</span><span class="sxs-lookup"><span data-stu-id="d7104-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7104-473"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d7104-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7104-474">DLL</span><span class="sxs-lookup"><span data-stu-id="d7104-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7104-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7104-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7104-476">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7104-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7104-477">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="d7104-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="d7104-478">**CIM \_ EthernetPort**</span><span class="sxs-lookup"><span data-stu-id="d7104-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 


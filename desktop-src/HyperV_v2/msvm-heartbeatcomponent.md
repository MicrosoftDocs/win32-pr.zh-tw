---
description: 表示心跳服務的狀態，此服務會透過定期報告心跳來負責監視虛擬機器的狀態。
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Msvm_HeartbeatComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511005"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="0b5c9-103">Msvm \_ HeartbeatComponent 類別</span><span class="sxs-lookup"><span data-stu-id="0b5c9-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="0b5c9-104">表示心跳服務的狀態，此服務會透過定期報告心跳來負責監視虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="0b5c9-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b5c9-106">語法</span><span class="sxs-lookup"><span data-stu-id="0b5c9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
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
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
};
```

## <a name="members"></a><span data-ttu-id="0b5c9-107">成員</span><span class="sxs-lookup"><span data-stu-id="0b5c9-107">Members</span></span>

<span data-ttu-id="0b5c9-108">**Msvm \_ HeartbeatComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b5c9-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="0b5c9-109">方法</span><span class="sxs-lookup"><span data-stu-id="0b5c9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b5c9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0b5c9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b5c9-111">方法</span><span class="sxs-lookup"><span data-stu-id="0b5c9-111">Methods</span></span>

<span data-ttu-id="0b5c9-112">**Msvm \_ HeartbeatComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="0b5c9-113">方法</span><span class="sxs-lookup"><span data-stu-id="0b5c9-113">Method</span></span>                                                                   | <span data-ttu-id="0b5c9-114">描述</span><span class="sxs-lookup"><span data-stu-id="0b5c9-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0b5c9-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="0b5c9-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b5c9-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="0b5c9-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b5c9-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="0b5c9-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0b5c9-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="0b5c9-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0b5c9-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="0b5c9-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="0b5c9-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="0b5c9-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b5c9-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="0b5c9-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0b5c9-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="0b5c9-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0b5c9-131">屬性</span><span class="sxs-lookup"><span data-stu-id="0b5c9-131">Properties</span></span>

<span data-ttu-id="0b5c9-132">**Msvm \_ HeartbeatComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b5c9-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="0b5c9-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-141">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-141">The primary availability and status of the device.</span></span> <span data-ttu-id="0b5c9-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-144">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-146">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0b5c9-147">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="0b5c9-148">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0b5c9-149">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0b5c9-150">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0b5c9-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0b5c9-161">)</span><span class="sxs-lookup"><span data-stu-id="0b5c9-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b5c9-162">**標題**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-165">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-165">A short description of the object.</span></span> <span data-ttu-id="0b5c9-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，且一律設定為「心跳」。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-170">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0b5c9-171">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b5c9-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-176">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-176">The scoping system's creation class name.</span></span> <span data-ttu-id="0b5c9-177">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ HeartbeatComponent"。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-178">**說明**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-181">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-181">A description of the object.</span></span> <span data-ttu-id="0b5c9-182">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 心跳服務」。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-186">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0b5c9-187">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b5c9-188">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-192">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="0b5c9-193">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*VMGUID* \\ *GUID*"，其中 *VMGUID* 是與此裝置相關聯之 [**Msvm 的 \_**](msvm-computersystem.md) [**名稱**] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-197">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-197">A display name for the object.</span></span> <span data-ttu-id="0b5c9-198">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會設定為「心跳」。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-199">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-200">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-202">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 7 (沒有預設) 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-204">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-206">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0b5c9-207">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="0b5c9-208">值</span><span class="sxs-lookup"><span data-stu-id="0b5c9-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="0b5c9-209">意義</span><span class="sxs-lookup"><span data-stu-id="0b5c9-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0b5c9-210"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c9-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="0b5c9-211">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0b5c9-212"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c9-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0b5c9-213">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b5c9-214">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-215">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-217">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0b5c9-218">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-222">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0b5c9-223">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-225">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-227">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-227">The current health of the element.</span></span> <span data-ttu-id="0b5c9-228">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-230">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-232">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0b5c9-233">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-235">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-237">整合服務安裝到虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="0b5c9-238">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-242">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-243">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0b5c9-244">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-246">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-248">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="0b5c9-249">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-250">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-251">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-253">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-253">This property has been deprecated.</span></span> <span data-ttu-id="0b5c9-254">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-255">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-258">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-258">The label by which the object is known.</span></span> <span data-ttu-id="0b5c9-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-260">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-261">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-263">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0b5c9-264">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b5c9-265">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-267">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-269">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "OperationalStatus" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-270">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-270">The current status of the element.</span></span> <span data-ttu-id="0b5c9-271">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0b5c9-272">以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b5c9-273"><span id="OK"></span><span id="ok"></span>**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-274">服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-274">The service is operating normally.</span></span> <span data-ttu-id="0b5c9-275">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b5c9-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (3) **降級**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-277">服務正常運作，但來賓服務已協商相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="0b5c9-278">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0b5c9-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-280">來賓不支援相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="0b5c9-281">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0b5c9-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-283">尚未安裝或尚未連線到來賓服務。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0b5c9-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-285">來賓服務已不會再回應正常。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0b5c9-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (15) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-287">虛擬機器已暫停。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="0b5c9-288">**OperationalStatus** \[ 1 \] 屬性值表示結合的應用程式狀態值。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="0b5c9-289">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="0b5c9-290">您可以使用 [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) 方法，在虛擬機器上設定應用程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b5c9-291"><span id="OK"></span><span id="ok"></span>**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-292">在虛擬機器中執行的應用程式會正常運作。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="0b5c9-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**通訊協定不相符** (32775) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-294">來賓和主機元件正在執行不同的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="0b5c9-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**應用程式重大狀態** (32782) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-296">虛擬機器內的一或多個應用程式處於重大狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="0b5c9-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**通訊超時** (32783) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-298">等候來賓元件的回應計時。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="0b5c9-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**通訊失敗** (32784) </span><span class="sxs-lookup"><span data-stu-id="0b5c9-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="0b5c9-300">無法與來賓元件通訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0b5c9-301">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-304">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0b5c9-305">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="0b5c9-306">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-308">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-310">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0b5c9-311">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-312">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-313">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-315">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-315">The power management capabilities of the device.</span></span> <span data-ttu-id="0b5c9-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-317">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-318">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-320">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0b5c9-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-322">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-323">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-325">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0b5c9-326">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-327">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-328">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-330">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-330">Provides high level status information.</span></span> <span data-ttu-id="0b5c9-331">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0b5c9-332">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0b5c9-333">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-335">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-337">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="0b5c9-338">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-339">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-342">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-342">The current status of the object.</span></span> <span data-ttu-id="0b5c9-343">這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-344">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-345">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0b5c9-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-347">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0b5c9-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-350">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-352">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-352">The current state of the logical device.</span></span> <span data-ttu-id="0b5c9-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-357">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-357">The scoping system's creation class name.</span></span> <span data-ttu-id="0b5c9-358">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律會設定為 "Msvm \_ 。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-362">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-362">The scoping system's name.</span></span> <span data-ttu-id="0b5c9-363">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且是與此信號服務相關聯之 [**Msvm \_ 的同**](msvm-computersystem.md) 類型名稱。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-364">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-365">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-367">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0b5c9-368">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-369">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-370">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-372">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0b5c9-373">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b5c9-374">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b5c9-375">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b5c9-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b5c9-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b5c9-377">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0b5c9-378">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b5c9-379">備註</span><span class="sxs-lookup"><span data-stu-id="0b5c9-379">Remarks</span></span>

<span data-ttu-id="0b5c9-380">存取 **Msvm \_ HeartbeatComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0b5c9-381">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0b5c9-382">範例</span><span class="sxs-lookup"><span data-stu-id="0b5c9-382">Examples</span></span>

<span data-ttu-id="0b5c9-383">下列 c # 範例會取得虛擬機器的應用程式健康情況狀態。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="0b5c9-384">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b5c9-385">若要正確運作，必須使用系統管理員許可權來執行下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="0b5c9-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0b5c9-386">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b5c9-386">Requirements</span></span>



| <span data-ttu-id="0b5c9-387">需求</span><span class="sxs-lookup"><span data-stu-id="0b5c9-387">Requirement</span></span> | <span data-ttu-id="0b5c9-388">值</span><span class="sxs-lookup"><span data-stu-id="0b5c9-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5c9-389">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b5c9-389">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5c9-390">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b5c9-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b5c9-391">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b5c9-391">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5c9-392">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b5c9-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b5c9-393">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b5c9-393">Namespace</span></span><br/>                | <span data-ttu-id="0b5c9-394">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0b5c9-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b5c9-395">MOF</span><span class="sxs-lookup"><span data-stu-id="0b5c9-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b5c9-396"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c9-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b5c9-397">DLL</span><span class="sxs-lookup"><span data-stu-id="0b5c9-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b5c9-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b5c9-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b5c9-399">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b5c9-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b5c9-400">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="0b5c9-401">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="0b5c9-402">**Msvm \_ HeartbeatComponent**</span><span class="sxs-lookup"><span data-stu-id="0b5c9-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 


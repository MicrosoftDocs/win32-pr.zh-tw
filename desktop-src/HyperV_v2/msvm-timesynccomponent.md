---
description: 代表時間同步處理服務的狀態，此服務負責同步處理虛擬機器的系統時間與管理作業系統中執行之作業系統的系統時間。
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Msvm_TimeSyncComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987419"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="74400-103">Msvm \_ TimeSyncComponent 類別</span><span class="sxs-lookup"><span data-stu-id="74400-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="74400-104">代表時間同步處理服務的狀態，此服務負責同步處理虛擬機器的系統時間與管理作業系統中執行之作業系統的系統時間。</span><span class="sxs-lookup"><span data-stu-id="74400-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="74400-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74400-106">語法</span><span class="sxs-lookup"><span data-stu-id="74400-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {"OK"};
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="74400-107">成員</span><span class="sxs-lookup"><span data-stu-id="74400-107">Members</span></span>

<span data-ttu-id="74400-108">**Msvm \_ TimeSyncComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="74400-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="74400-109">方法</span><span class="sxs-lookup"><span data-stu-id="74400-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="74400-110">屬性</span><span class="sxs-lookup"><span data-stu-id="74400-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74400-111">方法</span><span class="sxs-lookup"><span data-stu-id="74400-111">Methods</span></span>

<span data-ttu-id="74400-112">**Msvm \_ TimeSyncComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="74400-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="74400-113">方法</span><span class="sxs-lookup"><span data-stu-id="74400-113">Method</span></span>                                                                  | <span data-ttu-id="74400-114">描述</span><span class="sxs-lookup"><span data-stu-id="74400-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="74400-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="74400-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="74400-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74400-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="74400-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="74400-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74400-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="74400-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="74400-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="74400-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="74400-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="74400-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="74400-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="74400-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="74400-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="74400-124">重設元件。</span><span class="sxs-lookup"><span data-stu-id="74400-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="74400-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="74400-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="74400-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74400-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="74400-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="74400-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="74400-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="74400-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="74400-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="74400-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="74400-131">屬性</span><span class="sxs-lookup"><span data-stu-id="74400-131">Properties</span></span>

<span data-ttu-id="74400-132">**Msvm \_ TimeSyncComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74400-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="74400-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="74400-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="74400-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="74400-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="74400-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-141">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-141">The primary availability and status of the device.</span></span> <span data-ttu-id="74400-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="74400-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="74400-143">值</span><span class="sxs-lookup"><span data-stu-id="74400-143">Value</span></span>                                                                        | <span data-ttu-id="74400-144">意義</span><span class="sxs-lookup"><span data-stu-id="74400-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="74400-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="74400-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="74400-146">不適用</span><span class="sxs-lookup"><span data-stu-id="74400-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74400-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="74400-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="74400-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="74400-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74400-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74400-152">**標題**</span><span class="sxs-lookup"><span data-stu-id="74400-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-155">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="74400-155">A short description of the object.</span></span> <span data-ttu-id="74400-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="74400-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-160">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="74400-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="74400-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74400-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="74400-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="74400-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74400-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="74400-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74400-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="74400-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74400-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="74400-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74400-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="74400-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="74400-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="74400-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74400-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="74400-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="74400-170">)</span><span class="sxs-lookup"><span data-stu-id="74400-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="74400-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74400-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-174">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="74400-174">The scoping system's creation class name.</span></span> <span data-ttu-id="74400-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="74400-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74400-176">**說明**</span><span class="sxs-lookup"><span data-stu-id="74400-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-179">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="74400-179">A description of the object.</span></span> <span data-ttu-id="74400-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="74400-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-184">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74400-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="74400-185">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74400-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="74400-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="74400-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74400-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="74400-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74400-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="74400-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74400-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="74400-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74400-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="74400-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="74400-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="74400-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="74400-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="74400-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74400-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="74400-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="74400-195">)</span><span class="sxs-lookup"><span data-stu-id="74400-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="74400-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="74400-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-199">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="74400-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*VMGUID* \\ *GUID*"，其中 *VMGUID* 是與此裝置相關聯之 [**Msvm 實例 \_**](msvm-computersystem.md) **名稱的名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="74400-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="74400-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-204">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="74400-204">A display name for the object.</span></span> <span data-ttu-id="74400-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="74400-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-209">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 。</span><span class="sxs-lookup"><span data-stu-id="74400-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="74400-210">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="74400-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="74400-211">值</span><span class="sxs-lookup"><span data-stu-id="74400-211">Value</span></span>                                                                        | <span data-ttu-id="74400-212">意義</span><span class="sxs-lookup"><span data-stu-id="74400-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="74400-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="74400-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="74400-214">沒有預設值</span><span class="sxs-lookup"><span data-stu-id="74400-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74400-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="74400-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-216">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-218">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="74400-219">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會設定為 2 (啟用) 或 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="74400-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="74400-220">值</span><span class="sxs-lookup"><span data-stu-id="74400-220">Value</span></span>                                                                        | <span data-ttu-id="74400-221">意義</span><span class="sxs-lookup"><span data-stu-id="74400-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="74400-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="74400-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="74400-223">已啟用</span><span class="sxs-lookup"><span data-stu-id="74400-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="74400-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="74400-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="74400-225">Disabled</span><span class="sxs-lookup"><span data-stu-id="74400-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74400-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="74400-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-227">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="74400-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74400-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-229">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="74400-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="74400-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="74400-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-234">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="74400-235">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="74400-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-239">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="74400-239">The current health of the element.</span></span> <span data-ttu-id="74400-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="74400-241">值</span><span class="sxs-lookup"><span data-stu-id="74400-241">Value</span></span>                                                                        | <span data-ttu-id="74400-242">意義</span><span class="sxs-lookup"><span data-stu-id="74400-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="74400-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="74400-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="74400-244">確定</span><span class="sxs-lookup"><span data-stu-id="74400-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74400-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74400-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-246">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-248">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74400-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="74400-249">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="74400-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-251">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="74400-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74400-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-253">整合服務安裝到虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="74400-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="74400-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74400-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74400-258">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="74400-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="74400-259">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="74400-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="74400-260">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="74400-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="74400-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74400-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-264">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="74400-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="74400-265">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-266">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="74400-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-267">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="74400-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74400-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-269">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="74400-269">This property has been deprecated.</span></span> <span data-ttu-id="74400-270">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="74400-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74400-271">**名稱**</span><span class="sxs-lookup"><span data-stu-id="74400-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-274">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="74400-274">The label by which the object is known.</span></span> <span data-ttu-id="74400-275">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-276">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="74400-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-277">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-279">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74400-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="74400-280">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74400-281">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="74400-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="74400-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74400-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="74400-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74400-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="74400-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74400-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="74400-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74400-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="74400-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="74400-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="74400-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="74400-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="74400-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="74400-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="74400-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="74400-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="74400-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="74400-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="74400-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="74400-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="74400-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="74400-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="74400-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="74400-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="74400-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="74400-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="74400-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="74400-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="74400-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="74400-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="74400-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="74400-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="74400-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="74400-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="74400-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74400-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="74400-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="74400-301">)</span><span class="sxs-lookup"><span data-stu-id="74400-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="74400-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="74400-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-303">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-305">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-305">The current status of the element.</span></span> <span data-ttu-id="74400-306">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="74400-307">以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。</span><span class="sxs-lookup"><span data-stu-id="74400-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="74400-308">值</span><span class="sxs-lookup"><span data-stu-id="74400-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="74400-309">意義</span><span class="sxs-lookup"><span data-stu-id="74400-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74400-310"><dt>二級</dt></span><span class="sxs-lookup"><span data-stu-id="74400-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="74400-311"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="74400-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="74400-312">服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="74400-312">The service is operating normally.</span></span> <span data-ttu-id="74400-313">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="74400-314"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="74400-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="74400-315">服務正常運作，但來賓服務已協商相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="74400-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="74400-316">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="74400-317"><dt>**無法復原的錯誤**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="74400-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="74400-318">來賓不支援相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="74400-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="74400-319">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="74400-320"><dt>**無連絡人**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="74400-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="74400-321">尚未安裝或尚未連線到來賓服務。</span><span class="sxs-lookup"><span data-stu-id="74400-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="74400-322"><dt>**遺失的通訊**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="74400-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="74400-323">來賓服務已不會再回應正常。</span><span class="sxs-lookup"><span data-stu-id="74400-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="74400-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="74400-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-327">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="74400-328">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="74400-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="74400-329">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74400-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74400-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="74400-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-331">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-333">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="74400-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="74400-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74400-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74400-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="74400-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-336">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-338">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="74400-338">The power management capabilities of the device.</span></span> <span data-ttu-id="74400-339">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-340">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="74400-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-341">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="74400-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74400-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-343">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="74400-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="74400-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-345">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="74400-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-346">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="74400-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74400-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-348">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="74400-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="74400-349">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="74400-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-350">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="74400-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-351">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-353">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="74400-353">Provides high level status information.</span></span> <span data-ttu-id="74400-354">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="74400-355">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="74400-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="74400-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="74400-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="74400-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74400-358"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="74400-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="74400-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="74400-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="74400-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="74400-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="74400-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="74400-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="74400-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="74400-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="74400-363">)</span><span class="sxs-lookup"><span data-stu-id="74400-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="74400-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="74400-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-365">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-367">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="74400-368">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="74400-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="74400-369">值</span><span class="sxs-lookup"><span data-stu-id="74400-369">Value</span></span>                                                                         | <span data-ttu-id="74400-370">意義</span><span class="sxs-lookup"><span data-stu-id="74400-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="74400-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="74400-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="74400-372">不適用</span><span class="sxs-lookup"><span data-stu-id="74400-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74400-373">**狀態**</span><span class="sxs-lookup"><span data-stu-id="74400-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-376">字串，指定物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="74400-377">這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="74400-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74400-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-379">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="74400-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74400-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-381">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="74400-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="74400-382">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="74400-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="74400-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="74400-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-384">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-386">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-386">The current state of the logical device.</span></span> <span data-ttu-id="74400-387">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74400-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-389">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-391">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="74400-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="74400-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="74400-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74400-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="74400-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="74400-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74400-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-396">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="74400-396">The name of the scoping system.</span></span> <span data-ttu-id="74400-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="74400-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="74400-398">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="74400-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-399">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="74400-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74400-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-401">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="74400-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="74400-402">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74400-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="74400-403">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="74400-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-404">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="74400-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74400-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-406">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="74400-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="74400-407">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="74400-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74400-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="74400-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74400-409">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="74400-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74400-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="74400-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74400-411">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="74400-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="74400-412">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="74400-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="74400-413">值</span><span class="sxs-lookup"><span data-stu-id="74400-413">Value</span></span>                                                                         | <span data-ttu-id="74400-414">意義</span><span class="sxs-lookup"><span data-stu-id="74400-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="74400-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="74400-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="74400-416">不適用</span><span class="sxs-lookup"><span data-stu-id="74400-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74400-417">備註</span><span class="sxs-lookup"><span data-stu-id="74400-417">Remarks</span></span>

<span data-ttu-id="74400-418">存取 **Msvm \_ TimeSyncComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="74400-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="74400-419">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="74400-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="74400-420">規格需求</span><span class="sxs-lookup"><span data-stu-id="74400-420">Requirements</span></span>



| <span data-ttu-id="74400-421">需求</span><span class="sxs-lookup"><span data-stu-id="74400-421">Requirement</span></span> | <span data-ttu-id="74400-422">值</span><span class="sxs-lookup"><span data-stu-id="74400-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74400-423">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74400-423">Minimum supported client</span></span><br/> | <span data-ttu-id="74400-424">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74400-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74400-425">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74400-425">Minimum supported server</span></span><br/> | <span data-ttu-id="74400-426">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74400-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74400-427">命名空間</span><span class="sxs-lookup"><span data-stu-id="74400-427">Namespace</span></span><br/>                | <span data-ttu-id="74400-428">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="74400-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74400-429">MOF</span><span class="sxs-lookup"><span data-stu-id="74400-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74400-430"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="74400-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74400-431">DLL</span><span class="sxs-lookup"><span data-stu-id="74400-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74400-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74400-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74400-433">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74400-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74400-434">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="74400-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="74400-435">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="74400-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


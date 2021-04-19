---
description: 代表磁碟區陰影複製服務 (VSS) 服務的狀態，此服務會在客體作業系統中執行 VSS 要求者。
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Msvm_VssComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991689"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="1ebd0-103">Msvm \_ VssComponent 類別</span><span class="sxs-lookup"><span data-stu-id="1ebd0-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="1ebd0-104">代表磁碟區陰影複製服務 (VSS) 服務的狀態，此服務會在客體作業系統中執行 VSS 要求者。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="1ebd0-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebd0-106">語法</span><span class="sxs-lookup"><span data-stu-id="1ebd0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_VssComponent";
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

## <a name="members"></a><span data-ttu-id="1ebd0-107">成員</span><span class="sxs-lookup"><span data-stu-id="1ebd0-107">Members</span></span>

<span data-ttu-id="1ebd0-108">**Msvm \_ VssComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ebd0-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1ebd0-109">方法</span><span class="sxs-lookup"><span data-stu-id="1ebd0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ebd0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1ebd0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ebd0-111">方法</span><span class="sxs-lookup"><span data-stu-id="1ebd0-111">Methods</span></span>

<span data-ttu-id="1ebd0-112">**Msvm \_ VssComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="1ebd0-113">方法</span><span class="sxs-lookup"><span data-stu-id="1ebd0-113">Method</span></span>                                                             | <span data-ttu-id="1ebd0-114">描述</span><span class="sxs-lookup"><span data-stu-id="1ebd0-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="1ebd0-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="1ebd0-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ebd0-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="1ebd0-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ebd0-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="1ebd0-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="1ebd0-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="1ebd0-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="1ebd0-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="1ebd0-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="1ebd0-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="1ebd0-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ebd0-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="1ebd0-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1ebd0-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="1ebd0-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1ebd0-131">屬性</span><span class="sxs-lookup"><span data-stu-id="1ebd0-131">Properties</span></span>

<span data-ttu-id="1ebd0-132">**Msvm \_ VssComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ebd0-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="1ebd0-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-141">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-141">The primary availability and status of the device.</span></span> <span data-ttu-id="1ebd0-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="1ebd0-143">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-143">Value</span></span>                                                                        | <span data-ttu-id="1ebd0-144">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1ebd0-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="1ebd0-146">不適用</span><span class="sxs-lookup"><span data-stu-id="1ebd0-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ebd0-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1ebd0-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-152">**標題**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-155">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-155">A short description of the object.</span></span> <span data-ttu-id="1ebd0-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-160">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1ebd0-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ebd0-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ebd0-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ebd0-170">)</span><span class="sxs-lookup"><span data-stu-id="1ebd0-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ebd0-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-174">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-174">The scoping system's creation class name.</span></span> <span data-ttu-id="1ebd0-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-176">**說明**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-179">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-179">A description of the object.</span></span> <span data-ttu-id="1ebd0-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-184">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1ebd0-185">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ebd0-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ebd0-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ebd0-195">)</span><span class="sxs-lookup"><span data-stu-id="1ebd0-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ebd0-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-199">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1ebd0-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*VMGUID* \\ *GUID*"，其中 *VMGUID* 是與此裝置相關聯之 [**Msvm 的 \_**](msvm-computersystem.md) [**名稱**] 屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-204">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-204">A display name for the object.</span></span> <span data-ttu-id="1ebd0-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-209">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 7 (沒有預設) 。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="1ebd0-210">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-210">Value</span></span>                                                                        | <span data-ttu-id="1ebd0-211">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="1ebd0-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1ebd0-213">已啟用</span><span class="sxs-lookup"><span data-stu-id="1ebd0-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="1ebd0-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1ebd0-215">Disabled</span><span class="sxs-lookup"><span data-stu-id="1ebd0-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="1ebd0-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="1ebd0-217">沒有預設值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ebd0-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-221">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1ebd0-222">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1ebd0-223">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-223">Value</span></span>                                                                        | <span data-ttu-id="1ebd0-224">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="1ebd0-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1ebd0-226">已啟用</span><span class="sxs-lookup"><span data-stu-id="1ebd0-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="1ebd0-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1ebd0-228">Disabled</span><span class="sxs-lookup"><span data-stu-id="1ebd0-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ebd0-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-230">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-232">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="1ebd0-233">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-237">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="1ebd0-238">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-240">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-242">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-242">The current health of the element.</span></span> <span data-ttu-id="1ebd0-243">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1ebd0-244">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1ebd0-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="1ebd0-246">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-246">Value</span></span>                                                                        | <span data-ttu-id="1ebd0-247">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="1ebd0-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="1ebd0-249">確定</span><span class="sxs-lookup"><span data-stu-id="1ebd0-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ebd0-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-251">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-253">自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="1ebd0-254">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-256">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-258">整合服務安裝到虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="1ebd0-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-263">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-264">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1ebd0-265">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-267">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-269">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="1ebd0-270">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-271">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-272">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-274">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-274">This property has been deprecated.</span></span> <span data-ttu-id="1ebd0-275">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-276">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-279">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-279">The label by which the object is known.</span></span> <span data-ttu-id="1ebd0-280">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-281">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-282">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-284">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1ebd0-285">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ebd0-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ebd0-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ebd0-306">)</span><span class="sxs-lookup"><span data-stu-id="1ebd0-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ebd0-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-308">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-310">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-310">The current status of the element.</span></span> <span data-ttu-id="1ebd0-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="1ebd0-312">以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="1ebd0-313">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="1ebd0-314">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ebd0-315"><dt>二級</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="1ebd0-316"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="1ebd0-317">服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-317">The service is operating normally.</span></span> <span data-ttu-id="1ebd0-318">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="1ebd0-319"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="1ebd0-320">服務正常運作，但來賓服務已協商相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="1ebd0-321">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="1ebd0-322"><dt>**無法復原的錯誤**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="1ebd0-323">來賓不支援相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="1ebd0-324">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="1ebd0-325"><dt>**無連絡人**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="1ebd0-326">尚未安裝或尚未連線到來賓服務。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="1ebd0-327"><dt>**遺失的通訊**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="1ebd0-328">來賓服務已不會再回應正常。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="1ebd0-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-332">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1ebd0-333">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1ebd0-334">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-336">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-338">其他資料，超過裝置識別碼資訊，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="1ebd0-339">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-341">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-343">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-343">The power management capabilities of the device.</span></span> <span data-ttu-id="1ebd0-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-346">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-348">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="1ebd0-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-350">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-351">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-353">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="1ebd0-354">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-355">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-356">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-358">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-358">Provides high level status information.</span></span> <span data-ttu-id="1ebd0-359">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1ebd0-360">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ebd0-361">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ebd0-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-363"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1ebd0-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ebd0-368">)</span><span class="sxs-lookup"><span data-stu-id="1ebd0-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ebd0-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-370">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-372">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="1ebd0-373">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1ebd0-374">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-374">Value</span></span>                                                                         | <span data-ttu-id="1ebd0-375">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1ebd0-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1ebd0-377">不適用</span><span class="sxs-lookup"><span data-stu-id="1ebd0-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ebd0-378">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-381">字串，指定物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="1ebd0-382">這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-384">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ebd0-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-386">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1ebd0-387">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-389">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-391">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-391">The current state of the logical device.</span></span> <span data-ttu-id="1ebd0-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-394">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-396">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-396">The scoping system's creation class name.</span></span> <span data-ttu-id="1ebd0-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-401">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-401">The scoping system's name.</span></span> <span data-ttu-id="1ebd0-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-404">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-406">專案的 **EnabledState** 上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="1ebd0-407">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-409">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-411">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="1ebd0-412">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ebd0-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ebd0-414">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ebd0-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ebd0-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ebd0-416">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1ebd0-417">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1ebd0-418">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-418">Value</span></span>                                                                         | <span data-ttu-id="1ebd0-419">意義</span><span class="sxs-lookup"><span data-stu-id="1ebd0-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1ebd0-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1ebd0-421">不適用</span><span class="sxs-lookup"><span data-stu-id="1ebd0-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ebd0-422">備註</span><span class="sxs-lookup"><span data-stu-id="1ebd0-422">Remarks</span></span>

<span data-ttu-id="1ebd0-423">存取 **Msvm \_ VssComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1ebd0-424">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="1ebd0-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebd0-425">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ebd0-425">Requirements</span></span>



| <span data-ttu-id="1ebd0-426">需求</span><span class="sxs-lookup"><span data-stu-id="1ebd0-426">Requirement</span></span> | <span data-ttu-id="1ebd0-427">值</span><span class="sxs-lookup"><span data-stu-id="1ebd0-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebd0-428">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ebd0-428">Minimum supported client</span></span><br/> | <span data-ttu-id="1ebd0-429">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ebd0-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ebd0-430">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ebd0-430">Minimum supported server</span></span><br/> | <span data-ttu-id="1ebd0-431">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ebd0-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ebd0-432">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ebd0-432">Namespace</span></span><br/>                | <span data-ttu-id="1ebd0-433">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1ebd0-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ebd0-434">MOF</span><span class="sxs-lookup"><span data-stu-id="1ebd0-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ebd0-435"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ebd0-436">DLL</span><span class="sxs-lookup"><span data-stu-id="1ebd0-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ebd0-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ebd0-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ebd0-438">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ebd0-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebd0-439">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="1ebd0-440">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="1ebd0-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


---
description: 代表索引鍵/值組 exchange 服務的狀態，此服務提供一種機制，可在虛擬機器與管理作業系統上執行的作業系統之間交換資料。
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Msvm_KvpExchangeComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852396"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="3913a-103">Msvm \_ KvpExchangeComponent 類別</span><span class="sxs-lookup"><span data-stu-id="3913a-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="3913a-104">代表索引鍵/值組 exchange 服務的狀態，此服務提供一種機制，可在虛擬機器與管理作業系統上執行的作業系統之間交換資料。</span><span class="sxs-lookup"><span data-stu-id="3913a-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="3913a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3913a-106">語法</span><span class="sxs-lookup"><span data-stu-id="3913a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="3913a-107">成員</span><span class="sxs-lookup"><span data-stu-id="3913a-107">Members</span></span>

<span data-ttu-id="3913a-108">**Msvm \_ KvpExchangeComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3913a-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="3913a-109">方法</span><span class="sxs-lookup"><span data-stu-id="3913a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3913a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3913a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3913a-111">方法</span><span class="sxs-lookup"><span data-stu-id="3913a-111">Methods</span></span>

<span data-ttu-id="3913a-112">**Msvm \_ KvpExchangeComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="3913a-113">方法</span><span class="sxs-lookup"><span data-stu-id="3913a-113">Method</span></span>                                                                     | <span data-ttu-id="3913a-114">描述</span><span class="sxs-lookup"><span data-stu-id="3913a-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3913a-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3913a-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="3913a-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3913a-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3913a-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="3913a-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3913a-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3913a-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="3913a-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3913a-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3913a-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="3913a-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="3913a-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="3913a-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="3913a-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="3913a-124">重設元件。</span><span class="sxs-lookup"><span data-stu-id="3913a-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="3913a-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3913a-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="3913a-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3913a-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3913a-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="3913a-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3913a-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3913a-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="3913a-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3913a-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3913a-131">屬性</span><span class="sxs-lookup"><span data-stu-id="3913a-131">Properties</span></span>

<span data-ttu-id="3913a-132">**Msvm \_ KvpExchangeComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3913a-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3913a-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="3913a-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3913a-138">值</span><span class="sxs-lookup"><span data-stu-id="3913a-138">Value</span></span>                                                                            | <span data-ttu-id="3913a-139">意義</span><span class="sxs-lookup"><span data-stu-id="3913a-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3913a-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="3913a-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="3913a-142">不適用</span><span class="sxs-lookup"><span data-stu-id="3913a-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3913a-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="3913a-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-146">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-146">The primary availability and status of the device.</span></span> <span data-ttu-id="3913a-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3913a-148">值</span><span class="sxs-lookup"><span data-stu-id="3913a-148">Value</span></span>                                                                        | <span data-ttu-id="3913a-149">意義</span><span class="sxs-lookup"><span data-stu-id="3913a-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3913a-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3913a-151">不適用</span><span class="sxs-lookup"><span data-stu-id="3913a-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3913a-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3913a-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-155">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="3913a-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3913a-156">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-157">**標題**</span><span class="sxs-lookup"><span data-stu-id="3913a-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-160">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3913a-160">A short description of the object.</span></span> <span data-ttu-id="3913a-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3913a-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-165">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="3913a-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3913a-166">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3913a-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3913a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3913a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="3913a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="3913a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="3913a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="3913a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3913a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="3913a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3913a-175">)</span><span class="sxs-lookup"><span data-stu-id="3913a-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3913a-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3913a-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-179">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3913a-179">The scoping system's creation class name.</span></span> <span data-ttu-id="3913a-180">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-181">**說明**</span><span class="sxs-lookup"><span data-stu-id="3913a-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-184">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3913a-184">A description of the object.</span></span> <span data-ttu-id="3913a-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3913a-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-189">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3913a-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3913a-190">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3913a-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3913a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="3913a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="3913a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="3913a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="3913a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="3913a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="3913a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3913a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="3913a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3913a-200">)</span><span class="sxs-lookup"><span data-stu-id="3913a-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3913a-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3913a-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-204">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="3913a-205">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3913a-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-209">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3913a-209">A display name for the object.</span></span> <span data-ttu-id="3913a-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3913a-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-214">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3913a-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3913a-215">值</span><span class="sxs-lookup"><span data-stu-id="3913a-215">Value</span></span>                                                                        | <span data-ttu-id="3913a-216">意義</span><span class="sxs-lookup"><span data-stu-id="3913a-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="3913a-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="3913a-218">沒有預設值</span><span class="sxs-lookup"><span data-stu-id="3913a-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3913a-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3913a-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-222">元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-222">The enabled state of the element.</span></span> <span data-ttu-id="3913a-223">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3913a-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3913a-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="3913a-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="3913a-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3913a-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3913a-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-227">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3913a-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-229">指出現在是否已清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3913a-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="3913a-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3913a-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-234">字串，提供 **LastErrorCode** 屬性中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="3913a-235">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="3913a-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-237">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3913a-239">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) </span><span class="sxs-lookup"><span data-stu-id="3913a-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="3913a-240">內嵌 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 實例的陣列，其中包含一組成對的索引鍵/值組，在客體作業系統內執行的服務已推入可供外部用戶端存取。</span><span class="sxs-lookup"><span data-stu-id="3913a-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="3913a-241">此陣列將不會包含任何由 integration service 直接推送的內部專案。</span><span class="sxs-lookup"><span data-stu-id="3913a-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="3913a-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-243">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3913a-245">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) </span><span class="sxs-lookup"><span data-stu-id="3913a-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="3913a-246">內嵌 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 實例的陣列，其中包含客體作業系統已推送以供外部用戶端存取的一組索引鍵/值組。</span><span class="sxs-lookup"><span data-stu-id="3913a-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="3913a-247">此陣列將不會包含在客體作業系統內執行的其他服務所推送的任何資料項目。</span><span class="sxs-lookup"><span data-stu-id="3913a-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3913a-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-249">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-251">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="3913a-251">The current health of the element.</span></span> <span data-ttu-id="3913a-252">這表示此元素的健全狀況，但不一定是其子元件的健康情況。</span><span class="sxs-lookup"><span data-stu-id="3913a-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3913a-253">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3913a-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3913a-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3913a-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-256">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-258">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3913a-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="3913a-259">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3913a-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-261">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3913a-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-263">整合服務安裝到虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3913a-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="3913a-264">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3913a-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-266">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3913a-268">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3913a-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3913a-269">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3913a-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3913a-270">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3913a-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-272">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3913a-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-274">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3913a-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="3913a-275">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3913a-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-277">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3913a-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-279">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="3913a-279">This property has been deprecated.</span></span> <span data-ttu-id="3913a-280">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-281">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3913a-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-284">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="3913a-284">The label by which the object is known.</span></span> <span data-ttu-id="3913a-285">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3913a-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-287">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-289">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3913a-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3913a-290">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3913a-291">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3913a-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3913a-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="3913a-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="3913a-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="3913a-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="3913a-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="3913a-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="3913a-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="3913a-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="3913a-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="3913a-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="3913a-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="3913a-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="3913a-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="3913a-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="3913a-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="3913a-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="3913a-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3913a-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="3913a-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3913a-311">)</span><span class="sxs-lookup"><span data-stu-id="3913a-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3913a-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3913a-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-313">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-315">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-315">The current status of the element.</span></span> <span data-ttu-id="3913a-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="3913a-317">以下是「 **OperationalStatus** \[ 0」屬性值的可能值 \] 。</span><span class="sxs-lookup"><span data-stu-id="3913a-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="3913a-318">值</span><span class="sxs-lookup"><span data-stu-id="3913a-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="3913a-319">意義</span><span class="sxs-lookup"><span data-stu-id="3913a-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="3913a-320"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="3913a-321">服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="3913a-321">The service is operating normally.</span></span> <span data-ttu-id="3913a-322">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="3913a-323"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="3913a-324">服務正常運作，但來賓服務已協商相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="3913a-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="3913a-325">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="3913a-326"><dt>**無法復原的錯誤**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="3913a-327">來賓不支援相容的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="3913a-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="3913a-328">**OperationalStatus** \[ 1 \] 和 **StatusDescriptions** \[ 1 \] 屬性值可能包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="3913a-329"><dt>**無連絡人**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="3913a-330">尚未安裝或尚未連線到來賓服務。</span><span class="sxs-lookup"><span data-stu-id="3913a-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="3913a-331"><dt>**遺失的通訊**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="3913a-332">來賓服務已不會再回應正常。</span><span class="sxs-lookup"><span data-stu-id="3913a-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="3913a-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3913a-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-336">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3913a-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3913a-337">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3913a-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="3913a-338">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3913a-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3913a-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-340">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-342">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="3913a-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3913a-343">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3913a-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3913a-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-345">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-347">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="3913a-347">The power management capabilities of the device.</span></span> <span data-ttu-id="3913a-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3913a-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-350">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3913a-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-352">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="3913a-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3913a-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3913a-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-355">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3913a-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-357">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="3913a-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3913a-358">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="3913a-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3913a-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-360">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-362">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="3913a-362">Provides high level status information.</span></span> <span data-ttu-id="3913a-363">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3913a-364">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3913a-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3913a-365">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3913a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3913a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-367"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="3913a-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="3913a-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="3913a-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3913a-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3913a-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="3913a-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3913a-372">)</span><span class="sxs-lookup"><span data-stu-id="3913a-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3913a-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3913a-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-374">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-376">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="3913a-377">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3913a-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3913a-378">值</span><span class="sxs-lookup"><span data-stu-id="3913a-378">Value</span></span>                                                                         | <span data-ttu-id="3913a-379">意義</span><span class="sxs-lookup"><span data-stu-id="3913a-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="3913a-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="3913a-381">不適用</span><span class="sxs-lookup"><span data-stu-id="3913a-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3913a-382">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3913a-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-383">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-385">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-385">The current status of the object.</span></span> <span data-ttu-id="3913a-386">這個屬性會繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="3913a-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3913a-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-388">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3913a-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3913a-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-390">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="3913a-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3913a-391">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3913a-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3913a-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-393">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-395">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-395">The current state of the logical device.</span></span> <span data-ttu-id="3913a-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3913a-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-400">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3913a-400">The scoping system's creation class name.</span></span> <span data-ttu-id="3913a-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3913a-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3913a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-405">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="3913a-405">The scoping system's name.</span></span> <span data-ttu-id="3913a-406">此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 [**名稱**](msvm-computersystem.md)屬性值。 **\_**</span><span class="sxs-lookup"><span data-stu-id="3913a-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="3913a-407">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="3913a-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3913a-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3913a-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-409">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3913a-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-411">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="3913a-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3913a-412">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3913a-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-414">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3913a-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-416">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="3913a-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3913a-417">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3913a-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3913a-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3913a-419">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3913a-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3913a-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3913a-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3913a-421">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="3913a-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3913a-422">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3913a-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3913a-423">備註</span><span class="sxs-lookup"><span data-stu-id="3913a-423">Remarks</span></span>

<span data-ttu-id="3913a-424">存取 **Msvm \_ KvpExchangeComponent** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="3913a-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3913a-425">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="3913a-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3913a-426">規格需求</span><span class="sxs-lookup"><span data-stu-id="3913a-426">Requirements</span></span>



| <span data-ttu-id="3913a-427">需求</span><span class="sxs-lookup"><span data-stu-id="3913a-427">Requirement</span></span> | <span data-ttu-id="3913a-428">值</span><span class="sxs-lookup"><span data-stu-id="3913a-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3913a-429">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3913a-429">Minimum supported client</span></span><br/> | <span data-ttu-id="3913a-430">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3913a-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3913a-431">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3913a-431">Minimum supported server</span></span><br/> | <span data-ttu-id="3913a-432">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3913a-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3913a-433">命名空間</span><span class="sxs-lookup"><span data-stu-id="3913a-433">Namespace</span></span><br/>                | <span data-ttu-id="3913a-434">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3913a-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3913a-435">MOF</span><span class="sxs-lookup"><span data-stu-id="3913a-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3913a-436"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3913a-437">DLL</span><span class="sxs-lookup"><span data-stu-id="3913a-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3913a-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3913a-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3913a-439">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3913a-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3913a-440">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3913a-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="3913a-441">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3913a-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


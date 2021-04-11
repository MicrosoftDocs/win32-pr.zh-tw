---
description: 代表虛擬機器中的虛擬處理器。
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Msvm_Processor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849496"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="0ec1b-103">Msvm \_ Processor 類別</span><span class="sxs-lookup"><span data-stu-id="0ec1b-103">Msvm\_Processor class</span></span>

<span data-ttu-id="0ec1b-104">代表虛擬機器中的虛擬處理器。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="0ec1b-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec1b-106">語法</span><span class="sxs-lookup"><span data-stu-id="0ec1b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="0ec1b-107">成員</span><span class="sxs-lookup"><span data-stu-id="0ec1b-107">Members</span></span>

<span data-ttu-id="0ec1b-108">**Msvm \_ Processor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0ec1b-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="0ec1b-109">方法</span><span class="sxs-lookup"><span data-stu-id="0ec1b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0ec1b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0ec1b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0ec1b-111">方法</span><span class="sxs-lookup"><span data-stu-id="0ec1b-111">Methods</span></span>

<span data-ttu-id="0ec1b-112">**Msvm \_ Processor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="0ec1b-113">方法</span><span class="sxs-lookup"><span data-stu-id="0ec1b-113">Method</span></span>                                                          | <span data-ttu-id="0ec1b-114">描述</span><span class="sxs-lookup"><span data-stu-id="0ec1b-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0ec1b-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="0ec1b-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ec1b-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="0ec1b-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ec1b-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="0ec1b-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0ec1b-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="0ec1b-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0ec1b-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="0ec1b-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="0ec1b-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="0ec1b-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ec1b-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="0ec1b-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ec1b-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="0ec1b-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0ec1b-131">屬性</span><span class="sxs-lookup"><span data-stu-id="0ec1b-131">Properties</span></span>

<span data-ttu-id="0ec1b-132">**Msvm \_ Processor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ec1b-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-136">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="0ec1b-137">**Availability** 屬性代表裝置的主要狀態和可用性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="0ec1b-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-139">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-142">處理器位址寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-142">The processor address width, in bits.</span></span> <span data-ttu-id="0ec1b-143">這個屬性是從 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)繼承而來，而值則是32或64，視虛擬機器的特性而定。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-144">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-147">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-147">The primary availability and status of the device.</span></span> <span data-ttu-id="0ec1b-148">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-149">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-150">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-152">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0ec1b-153">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-154">**標題**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-157">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-158">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-158">A short description of the object.</span></span> <span data-ttu-id="0ec1b-159">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-160">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-163">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0ec1b-164">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ec1b-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0ec1b-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0ec1b-173">)</span><span class="sxs-lookup"><span data-stu-id="0ec1b-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ec1b-174">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-175">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-177">處理器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-177">The current status of the processor.</span></span> <span data-ttu-id="0ec1b-178">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-182">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-183">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0ec1b-184">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="0ec1b-185">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-186">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-189">實體處理器的最大速度，將虛擬處理器的容量納入考慮。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="0ec1b-190">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-194">處理器資料寬度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-194">The processor data width, in bits.</span></span> <span data-ttu-id="0ec1b-195">這個屬性是從 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)繼承而來，而值則是32或64，視虛擬機器的特性而定。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-196">**說明**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-199">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-199">A description of the object.</span></span> <span data-ttu-id="0ec1b-200">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-204">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0ec1b-205">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ec1b-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0ec1b-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0ec1b-215">)</span><span class="sxs-lookup"><span data-stu-id="0ec1b-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ec1b-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-219">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="0ec1b-220">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且一律設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-224">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-224">A display name for the object.</span></span> <span data-ttu-id="0ec1b-225">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-226">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-227">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-229">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="0ec1b-230">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-232">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-234">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0ec1b-235">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-236">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-237">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-239">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0ec1b-240">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-244">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0ec1b-245">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-246">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-247">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-249">基礎實體處理器的外部匯流排頻率速度。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="0ec1b-250">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-251">**系列**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-252">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-254">基礎實體處理器的處理器系列。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="0ec1b-255">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-259">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-259">The current health of the element.</span></span> <span data-ttu-id="0ec1b-260">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-262">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-264">自由格式字串的陣列，提供 [**OtherIdentifyingInfo**](msvm-keyboard.md) 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="0ec1b-265">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-267">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-269">建立虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="0ec1b-270">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-272">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-274">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-275">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0ec1b-276">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-278">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-280">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="0ec1b-281">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-282">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-285">虛擬機器耗用的總處理能力的目前百分比。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="0ec1b-286">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-287">**LoadPercentageHistory**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-288">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-290">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-291">虛擬機器耗用的總處理能力百分比記錄。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="0ec1b-292">這是包含範例的陣列。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-294">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-296">虛擬處理器的最大頻率速度（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="0ec1b-297">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-298">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-299">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-301">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-301">This property has been deprecated.</span></span> <span data-ttu-id="0ec1b-302">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-303">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-306">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-307">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-307">The label by which the object is known.</span></span> <span data-ttu-id="0ec1b-308">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="0ec1b-309">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-310">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-311">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-313">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0ec1b-314">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ec1b-315">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0ec1b-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0ec1b-335">)</span><span class="sxs-lookup"><span data-stu-id="0ec1b-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ec1b-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-337">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-339">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-339">The current status of the element.</span></span> <span data-ttu-id="0ec1b-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-341">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-344">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0ec1b-345">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0ec1b-346">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-347">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-350">處理器系列類型的描述。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-350">A description of the processor family type.</span></span> <span data-ttu-id="0ec1b-351">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-353">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-355">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0ec1b-356">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-358">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-360">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-360">The power management capabilities of the device.</span></span> <span data-ttu-id="0ec1b-361">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-362">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-363">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-365">指出裝置是否支援電源管理。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="0ec1b-366">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-367">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-368">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-370">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0ec1b-371">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-372">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-373">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-375">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-375">Provides high level status information.</span></span> <span data-ttu-id="0ec1b-376">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0ec1b-377">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ec1b-378">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0ec1b-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-380"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0ec1b-385">)</span><span class="sxs-lookup"><span data-stu-id="0ec1b-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ec1b-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-389">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="0ec1b-390">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-391">**角色**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-394">描述處理器角色的字串。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="0ec1b-395">例如，「中央處理器」或「數學處理器」。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="0ec1b-396">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-397">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-400">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-400">The current status of the object.</span></span> <span data-ttu-id="0ec1b-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-402">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-403">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ec1b-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-405">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0ec1b-406">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-408">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-410">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-410">The current state of the logical device.</span></span> <span data-ttu-id="0ec1b-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-412">**逐步執行**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-413">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-415">基礎實體處理器處理器系列內處理器的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="0ec1b-416">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-418">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-420">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-421">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="0ec1b-422">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-426">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="0ec1b-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-427">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-427">The name of the scoping system.</span></span> <span data-ttu-id="0ec1b-428">此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 [**名稱**](msvm-computersystem.md)屬性值。 **\_**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="0ec1b-429">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-430">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-431">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-433">虛擬機器狀態的變更日期或時間。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="0ec1b-434">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="0ec1b-435">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="0ec1b-436">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-437">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-438">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-440">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0ec1b-441">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-442">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-443">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-445">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0ec1b-446">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-447">**唯一**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-450">處理器的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="0ec1b-451">此識別碼在處理器系列中只能是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="0ec1b-452">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0ec1b-453">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ec1b-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ec1b-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ec1b-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ec1b-456">CPU 通訊端資訊，其中包含有關如何升級處理器 (的資料) 是否支援升級。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="0ec1b-457">這個屬性繼承自 [**CIM \_ 處理器**](/windows/desktop/CIMWin32Prov/cim-processor)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ec1b-458">備註</span><span class="sxs-lookup"><span data-stu-id="0ec1b-458">Remarks</span></span>

<span data-ttu-id="0ec1b-459">**Msvm \_ Processor** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0ec1b-460">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0ec1b-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec1b-461">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ec1b-461">Requirements</span></span>



| <span data-ttu-id="0ec1b-462">需求</span><span class="sxs-lookup"><span data-stu-id="0ec1b-462">Requirement</span></span> | <span data-ttu-id="0ec1b-463">值</span><span class="sxs-lookup"><span data-stu-id="0ec1b-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec1b-464">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ec1b-464">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec1b-465">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ec1b-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ec1b-466">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ec1b-466">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec1b-467">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ec1b-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ec1b-468">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ec1b-468">Namespace</span></span><br/>                | <span data-ttu-id="0ec1b-469">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0ec1b-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ec1b-470">MOF</span><span class="sxs-lookup"><span data-stu-id="0ec1b-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ec1b-471"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0ec1b-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ec1b-472">DLL</span><span class="sxs-lookup"><span data-stu-id="0ec1b-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ec1b-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ec1b-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ec1b-474">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ec1b-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec1b-475">**CIM \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="0ec1b-476">**CIM \_ 處理器**</span><span class="sxs-lookup"><span data-stu-id="0ec1b-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="0ec1b-477">處理器類別</span><span class="sxs-lookup"><span data-stu-id="0ec1b-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 


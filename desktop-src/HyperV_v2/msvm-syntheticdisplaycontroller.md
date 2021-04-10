---
description: 代表存在於每個虛擬機器設定中的綜合顯示控制器的狀態。
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Msvm_SyntheticDisplayController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848511"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="bc890-103">Msvm \_ SyntheticDisplayController 類別</span><span class="sxs-lookup"><span data-stu-id="bc890-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="bc890-104">代表存在於每個虛擬機器設定中的綜合顯示控制器的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="bc890-105">在虛擬機器中，每次只能有一個顯示控制器可供使用，而且只有在客體作業系統已載入必要的影片加速服務時，才可啟用綜合控制器。</span><span class="sxs-lookup"><span data-stu-id="bc890-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="bc890-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc890-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc890-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="bc890-108">成員</span><span class="sxs-lookup"><span data-stu-id="bc890-108">Members</span></span>

<span data-ttu-id="bc890-109">**Msvm \_ SyntheticDisplayController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc890-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="bc890-110">方法</span><span class="sxs-lookup"><span data-stu-id="bc890-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc890-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bc890-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc890-112">方法</span><span class="sxs-lookup"><span data-stu-id="bc890-112">Methods</span></span>

<span data-ttu-id="bc890-113">**Msvm \_ SyntheticDisplayController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="bc890-114">方法</span><span class="sxs-lookup"><span data-stu-id="bc890-114">Method</span></span>                                                                           | <span data-ttu-id="bc890-115">描述</span><span class="sxs-lookup"><span data-stu-id="bc890-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="bc890-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="bc890-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="bc890-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc890-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="bc890-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="bc890-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc890-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="bc890-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="bc890-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="bc890-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="bc890-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="bc890-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="bc890-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="bc890-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="bc890-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="bc890-125">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="bc890-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="bc890-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="bc890-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="bc890-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc890-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="bc890-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="bc890-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="bc890-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bc890-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="bc890-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc890-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc890-132">屬性</span><span class="sxs-lookup"><span data-stu-id="bc890-132">Properties</span></span>

<span data-ttu-id="bc890-133">**Msvm \_ SyntheticDisplayController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc890-134">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bc890-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-135">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-137">顯示控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="bc890-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="bc890-138">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律設定為 2 (圖形加速器) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="bc890-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-140">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="bc890-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="bc890-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="bc890-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="bc890-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-152">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc890-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-153">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-155">自由格式字串的陣列，可針對 **AcceleratorCapabilities** 屬性陣列中所指定的任何影片加速器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="bc890-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="bc890-156">這個陣列的每個專案都與位於相同索引的 **AcceleratorCapabilities** 屬性陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="bc890-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="bc890-157">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律設定為「圖形加速器」。</span><span class="sxs-lookup"><span data-stu-id="bc890-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-158">**標題**</span><span class="sxs-lookup"><span data-stu-id="bc890-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-161">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="bc890-161">A short description of the object.</span></span> <span data-ttu-id="bc890-162">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「顯示控制器」。</span><span class="sxs-lookup"><span data-stu-id="bc890-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="bc890-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-166">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="bc890-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bc890-167">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc890-168">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc890-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bc890-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="bc890-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="bc890-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="bc890-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="bc890-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bc890-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="bc890-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc890-176">)</span><span class="sxs-lookup"><span data-stu-id="bc890-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc890-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc890-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-180">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc890-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bc890-181">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ SyntheticDisplayController"。</span><span class="sxs-lookup"><span data-stu-id="bc890-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-182">**說明**</span><span class="sxs-lookup"><span data-stu-id="bc890-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-185">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="bc890-185">A description of the object.</span></span> <span data-ttu-id="bc890-186">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 綜合顯示控制器」。</span><span class="sxs-lookup"><span data-stu-id="bc890-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bc890-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-190">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bc890-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bc890-191">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc890-192">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc890-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="bc890-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="bc890-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="bc890-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="bc890-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="bc890-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="bc890-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bc890-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="bc890-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc890-201">)</span><span class="sxs-lookup"><span data-stu-id="bc890-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc890-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bc890-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-205">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="bc890-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bc890-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-209">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bc890-209">A display name for the object.</span></span> <span data-ttu-id="bc890-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，預設一律設定為「顯示控制器」。</span><span class="sxs-lookup"><span data-stu-id="bc890-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="bc890-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-214">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="bc890-215">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bc890-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-219">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="bc890-220">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="bc890-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="bc890-221">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 或 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-222">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bc890-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-223">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bc890-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-225">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bc890-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-229">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bc890-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-231">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-233">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="bc890-233">The current health of the element.</span></span> <span data-ttu-id="bc890-234">這個屬性工作表示這個專案的健康情況，但不一定是它的子項目。</span><span class="sxs-lookup"><span data-stu-id="bc890-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="bc890-235">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="bc890-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="bc890-236">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc890-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-238">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-240">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bc890-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-242">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bc890-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-244">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="bc890-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="bc890-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc890-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc890-249">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="bc890-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bc890-250">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="bc890-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bc890-251">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bc890-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-253">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc890-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-255">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-256">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="bc890-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-257">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc890-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-259">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc890-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="bc890-260">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律設定為 4194304 (0x400000) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-261">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="bc890-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc890-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-264">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="bc890-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="bc890-265">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="bc890-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="bc890-266">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bc890-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="bc890-267">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="bc890-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="bc890-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bc890-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-271">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-272">**名稱**</span><span class="sxs-lookup"><span data-stu-id="bc890-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-275">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="bc890-275">The label by which the object is known.</span></span> <span data-ttu-id="bc890-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="bc890-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-277">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="bc890-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-278">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bc890-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-280">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="bc890-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="bc890-281">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，一律設為1024。</span><span class="sxs-lookup"><span data-stu-id="bc890-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="bc890-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-285">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bc890-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bc890-286">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc890-287">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc890-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bc890-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="bc890-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="bc890-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="bc890-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="bc890-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="bc890-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="bc890-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="bc890-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="bc890-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="bc890-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="bc890-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="bc890-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="bc890-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="bc890-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="bc890-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="bc890-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="bc890-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bc890-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="bc890-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc890-307">)</span><span class="sxs-lookup"><span data-stu-id="bc890-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc890-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bc890-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-309">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-311">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-311">The current statuses of the object.</span></span> <span data-ttu-id="bc890-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="bc890-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-316">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="bc890-317">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bc890-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="bc890-318">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bc890-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-320">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-323">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bc890-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-326">描述影片架構類型的字串，當 **VideoArchitecture** 屬性是 1 ( "Other" ) 時。</span><span class="sxs-lookup"><span data-stu-id="bc890-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="bc890-327">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bc890-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-328">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bc890-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-331">當實例的 **VideoMemoryType** 屬性為1時 (其他) 的視訊記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="bc890-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="bc890-332">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bc890-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-334">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-336">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-337">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bc890-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-338">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="bc890-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bc890-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bc890-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-345">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="bc890-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-346">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-348">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="bc890-348">Provides high level status information.</span></span> <span data-ttu-id="bc890-349">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="bc890-350">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="bc890-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bc890-351">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="bc890-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="bc890-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bc890-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-353"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="bc890-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="bc890-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="bc890-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bc890-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="bc890-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc890-358">)</span><span class="sxs-lookup"><span data-stu-id="bc890-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc890-359">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="bc890-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-362">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="bc890-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="bc890-363">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，而且一律設定為「影片」。</span><span class="sxs-lookup"><span data-stu-id="bc890-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-364">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="bc890-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-365">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-367">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bc890-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="bc890-368">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，而且一律設定為 1 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="bc890-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-370">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-372">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="bc890-373">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="bc890-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="bc890-374">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="bc890-375">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange**。</span><span class="sxs-lookup"><span data-stu-id="bc890-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="bc890-376">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="bc890-377">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，它設定為 2 (啟用) 、3 (停用) 或 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-378">**狀態**</span><span class="sxs-lookup"><span data-stu-id="bc890-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-381">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-382">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bc890-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-383">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="bc890-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bc890-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-385">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="bc890-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="bc890-386">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="bc890-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bc890-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-388">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-390">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bc890-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-394">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="bc890-394">The scoping system's creation class name.</span></span> <span data-ttu-id="bc890-395">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律會設定為 "Msvm \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc890-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="bc890-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bc890-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-399">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc890-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="bc890-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="bc890-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="bc890-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-402">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bc890-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-404">虛擬機器的上次開機時間。</span><span class="sxs-lookup"><span data-stu-id="bc890-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="bc890-405">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="bc890-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-406">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="bc890-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-407">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="bc890-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-409">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="bc890-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="bc890-410">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bc890-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-411">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="bc890-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-412">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="bc890-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-414">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="bc890-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-415">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="bc890-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-416">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-418">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="bc890-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="bc890-419">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc890-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bc890-420">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bc890-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-421">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-423">指定用來產生視訊訊號的顯示器控制器影片架構。</span><span class="sxs-lookup"><span data-stu-id="bc890-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="bc890-424">通常，專用的視頻處理器會根據指定的架構產生影片信號。</span><span class="sxs-lookup"><span data-stu-id="bc890-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="bc890-425">它是顯示控制器最大解析度功能的指標。</span><span class="sxs-lookup"><span data-stu-id="bc890-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="bc890-426">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bc890-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bc890-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="bc890-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="bc890-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2) </span><span class="sxs-lookup"><span data-stu-id="bc890-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3) </span><span class="sxs-lookup"><span data-stu-id="bc890-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4) </span><span class="sxs-lookup"><span data-stu-id="bc890-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5) </span><span class="sxs-lookup"><span data-stu-id="bc890-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6) </span><span class="sxs-lookup"><span data-stu-id="bc890-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7) </span><span class="sxs-lookup"><span data-stu-id="bc890-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8) </span><span class="sxs-lookup"><span data-stu-id="bc890-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9) </span><span class="sxs-lookup"><span data-stu-id="bc890-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10) </span><span class="sxs-lookup"><span data-stu-id="bc890-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**線性框架緩衝區** (11) </span><span class="sxs-lookup"><span data-stu-id="bc890-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="bc890-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bc890-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc890-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="bc890-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="bc890-442">)</span><span class="sxs-lookup"><span data-stu-id="bc890-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc890-443">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bc890-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-444">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="bc890-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-446">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="bc890-446">The type of video memory.</span></span> <span data-ttu-id="bc890-447">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律設定為 2 (VRAM) 。</span><span class="sxs-lookup"><span data-stu-id="bc890-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="bc890-448">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="bc890-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc890-449">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bc890-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc890-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bc890-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bc890-451">描述視頻處理器/控制器的字串。</span><span class="sxs-lookup"><span data-stu-id="bc890-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="bc890-452">這個屬性會繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))，而且一律會設定為「綜合視頻處理器」。</span><span class="sxs-lookup"><span data-stu-id="bc890-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc890-453">備註</span><span class="sxs-lookup"><span data-stu-id="bc890-453">Remarks</span></span>

<span data-ttu-id="bc890-454">存取 **Msvm \_ SyntheticDisplayController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="bc890-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bc890-455">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="bc890-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc890-456">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc890-456">Requirements</span></span>



| <span data-ttu-id="bc890-457">需求</span><span class="sxs-lookup"><span data-stu-id="bc890-457">Requirement</span></span> | <span data-ttu-id="bc890-458">值</span><span class="sxs-lookup"><span data-stu-id="bc890-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc890-459">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc890-459">Minimum supported client</span></span><br/> | <span data-ttu-id="bc890-460">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc890-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bc890-461">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc890-461">Minimum supported server</span></span><br/> | <span data-ttu-id="bc890-462">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc890-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc890-463">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc890-463">Namespace</span></span><br/>                | <span data-ttu-id="bc890-464">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bc890-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bc890-465">MOF</span><span class="sxs-lookup"><span data-stu-id="bc890-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc890-466"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bc890-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc890-467">DLL</span><span class="sxs-lookup"><span data-stu-id="bc890-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc890-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc890-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc890-469">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc890-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc890-470">**CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="bc890-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="bc890-471">[**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc890-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bc890-472">影片類別</span><span class="sxs-lookup"><span data-stu-id="bc890-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 


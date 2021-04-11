---
description: 代表存在於每個虛擬機器設定中的模擬 S3 控制器的狀態。
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Msvm_S3DisplayController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115981"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="b8a90-103">Msvm \_ S3DisplayController 類別</span><span class="sxs-lookup"><span data-stu-id="b8a90-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="b8a90-104">代表存在於每個虛擬機器設定中的模擬 S3 控制器的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="b8a90-105">虛擬機器中隨時只能有一個顯示控制器處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="b8a90-106">此類別僅適用于第1代虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b8a90-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="b8a90-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a90-108">語法</span><span class="sxs-lookup"><span data-stu-id="b8a90-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
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
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="b8a90-109">成員</span><span class="sxs-lookup"><span data-stu-id="b8a90-109">Members</span></span>

<span data-ttu-id="b8a90-110">**Msvm \_ S3DisplayController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8a90-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="b8a90-111">方法</span><span class="sxs-lookup"><span data-stu-id="b8a90-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8a90-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b8a90-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8a90-113">方法</span><span class="sxs-lookup"><span data-stu-id="b8a90-113">Methods</span></span>

<span data-ttu-id="b8a90-114">**Msvm \_ S3DisplayController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="b8a90-115">方法</span><span class="sxs-lookup"><span data-stu-id="b8a90-115">Method</span></span>                                                                    | <span data-ttu-id="b8a90-116">描述</span><span class="sxs-lookup"><span data-stu-id="b8a90-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b8a90-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b8a90-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="b8a90-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8a90-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b8a90-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="b8a90-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8a90-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b8a90-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="b8a90-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b8a90-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b8a90-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="b8a90-124">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="b8a90-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="b8a90-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="b8a90-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="b8a90-126">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="b8a90-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="b8a90-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="b8a90-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="b8a90-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8a90-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="b8a90-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="b8a90-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b8a90-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="b8a90-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b8a90-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8a90-133">屬性</span><span class="sxs-lookup"><span data-stu-id="b8a90-133">Properties</span></span>

<span data-ttu-id="b8a90-134">**Msvm \_ S3DisplayController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b8a90-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-136">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-138">顯示控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="b8a90-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="b8a90-139">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b8a90-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-143">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="b8a90-144">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-145">**可用性**</span><span class="sxs-lookup"><span data-stu-id="b8a90-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-148">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-148">The primary availability and status of the device.</span></span> <span data-ttu-id="b8a90-149">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="b8a90-150">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-150">Value</span></span>                                                                        | <span data-ttu-id="b8a90-151">意義</span><span class="sxs-lookup"><span data-stu-id="b8a90-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b8a90-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="b8a90-153">不適用</span><span class="sxs-lookup"><span data-stu-id="b8a90-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a90-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b8a90-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-155">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-157">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="b8a90-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b8a90-158">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8a90-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b8a90-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-160">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-162">自由格式字串的陣列，可針對 **AcceleratorCapabilities** 陣列中所指定的任何影片加速器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="b8a90-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="b8a90-163">這個陣列的每個專案都與 **AcceleratorCapabilities** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="b8a90-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="b8a90-164">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-165">**標題**</span><span class="sxs-lookup"><span data-stu-id="b8a90-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-168">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="b8a90-168">A short description of the object.</span></span> <span data-ttu-id="b8a90-169">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a90-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-171">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-173">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="b8a90-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b8a90-174">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8a90-175">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b8a90-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b8a90-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="b8a90-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="b8a90-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="b8a90-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b8a90-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b8a90-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b8a90-183">)</span><span class="sxs-lookup"><span data-stu-id="b8a90-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8a90-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8a90-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-187">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a90-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b8a90-188">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Msvm \_ S3DisplayController"。</span><span class="sxs-lookup"><span data-stu-id="b8a90-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-189">**說明**</span><span class="sxs-lookup"><span data-stu-id="b8a90-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-192">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b8a90-192">A description of the object.</span></span> <span data-ttu-id="b8a90-193">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a90-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-195">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-197">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8a90-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b8a90-198">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8a90-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b8a90-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="b8a90-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="b8a90-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="b8a90-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="b8a90-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="b8a90-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b8a90-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b8a90-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b8a90-208">)</span><span class="sxs-lookup"><span data-stu-id="b8a90-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8a90-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b8a90-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-212">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="b8a90-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="b8a90-213">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b8a90-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-217">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a90-217">A display name for the object.</span></span> <span data-ttu-id="b8a90-218">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b8a90-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-222">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="b8a90-223">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b8a90-224">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-224">Value</span></span>                                                                        | <span data-ttu-id="b8a90-225">意義</span><span class="sxs-lookup"><span data-stu-id="b8a90-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="b8a90-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b8a90-227">已啟用</span><span class="sxs-lookup"><span data-stu-id="b8a90-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="b8a90-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b8a90-229">Disabled</span><span class="sxs-lookup"><span data-stu-id="b8a90-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a90-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-233">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b8a90-234">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="b8a90-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="b8a90-235">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 或 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="b8a90-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="b8a90-236">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-236">Value</span></span>                                                                        | <span data-ttu-id="b8a90-237">意義</span><span class="sxs-lookup"><span data-stu-id="b8a90-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="b8a90-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b8a90-239">已啟用</span><span class="sxs-lookup"><span data-stu-id="b8a90-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="b8a90-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b8a90-241">Disabled</span><span class="sxs-lookup"><span data-stu-id="b8a90-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a90-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b8a90-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-243">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8a90-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-245">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8a90-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b8a90-246">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b8a90-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-250">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8a90-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="b8a90-251">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-255">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="b8a90-255">The current health of the element.</span></span> <span data-ttu-id="b8a90-256">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="b8a90-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="b8a90-257">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b8a90-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="b8a90-258">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="b8a90-259">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-259">Value</span></span>                                                                        | <span data-ttu-id="b8a90-260">意義</span><span class="sxs-lookup"><span data-stu-id="b8a90-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="b8a90-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="b8a90-262">確定</span><span class="sxs-lookup"><span data-stu-id="b8a90-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a90-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b8a90-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-264">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-266">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8a90-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="b8a90-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8a90-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8a90-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-269">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b8a90-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-271">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b8a90-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="b8a90-272">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b8a90-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-276">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="b8a90-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-277">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b8a90-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b8a90-278">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b8a90-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-280">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8a90-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-282">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b8a90-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="b8a90-283">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-284">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="b8a90-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8a90-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-287">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8a90-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="b8a90-288">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-289">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="b8a90-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-290">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8a90-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-292">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="b8a90-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="b8a90-293">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="b8a90-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="b8a90-294">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b8a90-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="b8a90-295">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-296">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b8a90-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-297">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b8a90-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-299">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="b8a90-299">This property has been deprecated.</span></span> <span data-ttu-id="b8a90-300">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-301">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b8a90-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-304">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b8a90-304">The label by which the object is known.</span></span> <span data-ttu-id="b8a90-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-306">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="b8a90-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-307">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8a90-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-309">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="b8a90-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="b8a90-310">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-311">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a90-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-312">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-314">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8a90-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b8a90-315">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8a90-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b8a90-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b8a90-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="b8a90-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="b8a90-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="b8a90-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="b8a90-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="b8a90-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="b8a90-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="b8a90-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="b8a90-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="b8a90-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="b8a90-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="b8a90-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="b8a90-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="b8a90-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="b8a90-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="b8a90-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b8a90-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b8a90-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b8a90-336">)</span><span class="sxs-lookup"><span data-stu-id="b8a90-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8a90-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a90-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-338">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-340">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-340">The current statuses of the object.</span></span> <span data-ttu-id="b8a90-341">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="b8a90-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-342">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-345">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b8a90-346">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b8a90-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="b8a90-347">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8a90-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b8a90-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-349">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-351">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b8a90-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b8a90-352">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8a90-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-353">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="b8a90-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-354">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-356">描述影片架構類型的字串，當 **VideoArchitecture** 屬性是 1 ( "Other" ) 時。</span><span class="sxs-lookup"><span data-stu-id="b8a90-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="b8a90-357">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-358">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="b8a90-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-359">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-361">當實例的 **VideoMemoryType** 屬性為1時 (其他) 的視訊記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="b8a90-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="b8a90-362">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b8a90-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-364">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-366">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="b8a90-366">The power management capabilities of the device.</span></span> <span data-ttu-id="b8a90-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-368">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b8a90-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-369">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8a90-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-371">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="b8a90-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b8a90-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-373">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b8a90-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-374">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b8a90-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-376">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="b8a90-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b8a90-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-378">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a90-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-379">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-381">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="b8a90-381">Provides high level status information.</span></span> <span data-ttu-id="b8a90-382">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b8a90-383">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b8a90-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b8a90-384">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b8a90-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-386"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="b8a90-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="b8a90-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="b8a90-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b8a90-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b8a90-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b8a90-391">)</span><span class="sxs-lookup"><span data-stu-id="b8a90-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8a90-392">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="b8a90-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-393">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-395">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="b8a90-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="b8a90-396">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-397">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="b8a90-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-400">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b8a90-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="b8a90-401">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-403">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-405">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="b8a90-406">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="b8a90-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="b8a90-407">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="b8a90-408">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="b8a90-409">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-409">Value</span></span>                                                                         | <span data-ttu-id="b8a90-410">意義</span><span class="sxs-lookup"><span data-stu-id="b8a90-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="b8a90-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="b8a90-412">不適用</span><span class="sxs-lookup"><span data-stu-id="b8a90-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a90-413">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b8a90-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-414">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-416">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-416">The current status of the object.</span></span> <span data-ttu-id="b8a90-417">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-418">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b8a90-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-419">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8a90-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-421">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="b8a90-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b8a90-422">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="b8a90-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b8a90-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-424">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-426">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-426">The current state of the logical device.</span></span> <span data-ttu-id="b8a90-427">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-428">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8a90-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-429">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-431">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a90-431">The scoping system's creation class name.</span></span> <span data-ttu-id="b8a90-432">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b8a90-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-436">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8a90-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="b8a90-437">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="b8a90-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-439">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b8a90-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-441">虛擬機器的上次開機時間。</span><span class="sxs-lookup"><span data-stu-id="b8a90-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="b8a90-442">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-443">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b8a90-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-444">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b8a90-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-446">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="b8a90-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b8a90-447">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-448">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b8a90-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-449">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b8a90-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-451">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="b8a90-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b8a90-452">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b8a90-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-453">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b8a90-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-456">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b8a90-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b8a90-457">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8a90-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-458">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="b8a90-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-461">指定用來產生視訊訊號的顯示器控制器影片架構。</span><span class="sxs-lookup"><span data-stu-id="b8a90-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="b8a90-462">通常，專用的視頻處理器會根據指定的架構產生影片信號。</span><span class="sxs-lookup"><span data-stu-id="b8a90-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="b8a90-463">它是顯示控制器最大解析度功能的指標。</span><span class="sxs-lookup"><span data-stu-id="b8a90-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="b8a90-464">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b8a90-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b8a90-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b8a90-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2) </span><span class="sxs-lookup"><span data-stu-id="b8a90-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3) </span><span class="sxs-lookup"><span data-stu-id="b8a90-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4) </span><span class="sxs-lookup"><span data-stu-id="b8a90-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5) </span><span class="sxs-lookup"><span data-stu-id="b8a90-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6) </span><span class="sxs-lookup"><span data-stu-id="b8a90-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7) </span><span class="sxs-lookup"><span data-stu-id="b8a90-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8) </span><span class="sxs-lookup"><span data-stu-id="b8a90-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9) </span><span class="sxs-lookup"><span data-stu-id="b8a90-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10) </span><span class="sxs-lookup"><span data-stu-id="b8a90-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**線性框架緩衝區** (11) </span><span class="sxs-lookup"><span data-stu-id="b8a90-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="b8a90-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b8a90-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b8a90-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b8a90-480">)</span><span class="sxs-lookup"><span data-stu-id="b8a90-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8a90-481">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="b8a90-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-482">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8a90-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-484">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="b8a90-484">The type of video memory.</span></span> <span data-ttu-id="b8a90-485">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a90-486">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="b8a90-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a90-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8a90-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a90-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8a90-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a90-489">描述視頻處理器/控制器的字串。</span><span class="sxs-lookup"><span data-stu-id="b8a90-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="b8a90-490">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b8a90-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8a90-491">備註</span><span class="sxs-lookup"><span data-stu-id="b8a90-491">Remarks</span></span>

<span data-ttu-id="b8a90-492">存取 **Msvm \_ S3DisplayController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="b8a90-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8a90-493">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="b8a90-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a90-494">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a90-494">Requirements</span></span>



| <span data-ttu-id="b8a90-495">需求</span><span class="sxs-lookup"><span data-stu-id="b8a90-495">Requirement</span></span> | <span data-ttu-id="b8a90-496">值</span><span class="sxs-lookup"><span data-stu-id="b8a90-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a90-497">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8a90-497">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a90-498">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a90-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8a90-499">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8a90-499">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a90-500">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a90-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8a90-501">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8a90-501">Namespace</span></span><br/>                | <span data-ttu-id="b8a90-502">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8a90-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8a90-503">MOF</span><span class="sxs-lookup"><span data-stu-id="b8a90-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8a90-504"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8a90-505">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a90-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a90-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8a90-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8a90-507">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8a90-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a90-508">**CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="b8a90-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="b8a90-509">[**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8a90-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b8a90-510">影片類別</span><span class="sxs-lookup"><span data-stu-id="b8a90-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 


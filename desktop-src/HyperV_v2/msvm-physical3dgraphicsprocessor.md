---
description: 描述 (GPU) 的實體3-d 圖形處理器單位。
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Msvm_Physical3dGraphicsProcessor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695071"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="461f1-103">Msvm \_ Physical3dGraphicsProcessor 類別</span><span class="sxs-lookup"><span data-stu-id="461f1-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="461f1-104">描述 (GPU) 的實體3-d 圖形處理器單位。</span><span class="sxs-lookup"><span data-stu-id="461f1-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="461f1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="461f1-106">語法</span><span class="sxs-lookup"><span data-stu-id="461f1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
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
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="461f1-107">成員</span><span class="sxs-lookup"><span data-stu-id="461f1-107">Members</span></span>

<span data-ttu-id="461f1-108">**Msvm \_ Physical3dGraphicsProcessor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="461f1-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="461f1-109">方法</span><span class="sxs-lookup"><span data-stu-id="461f1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="461f1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="461f1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="461f1-111">方法</span><span class="sxs-lookup"><span data-stu-id="461f1-111">Methods</span></span>

<span data-ttu-id="461f1-112">**Msvm \_ Physical3dGraphicsProcessor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="461f1-113">方法</span><span class="sxs-lookup"><span data-stu-id="461f1-113">Method</span></span>                 | <span data-ttu-id="461f1-114">描述</span><span class="sxs-lookup"><span data-stu-id="461f1-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="461f1-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="461f1-115">**EnableDevice**</span></span>       | <span data-ttu-id="461f1-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="461f1-117">**OnlineDevice**</span></span>       | <span data-ttu-id="461f1-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="461f1-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="461f1-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="461f1-121">**RequestStateChange**</span></span> | <span data-ttu-id="461f1-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="461f1-123">**Reset**</span></span>              | <span data-ttu-id="461f1-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="461f1-125">**RestoreProperties**</span></span>  | <span data-ttu-id="461f1-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="461f1-127">**SaveProperties**</span></span>     | <span data-ttu-id="461f1-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="461f1-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="461f1-129">**SetPowerState**</span></span>      | <span data-ttu-id="461f1-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="461f1-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="461f1-131">屬性</span><span class="sxs-lookup"><span data-stu-id="461f1-131">Properties</span></span>

<span data-ttu-id="461f1-132">**Msvm \_ Physical3dGraphicsProcessor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="461f1-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="461f1-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-134">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-136">指定配置給此裝置的介面卡索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="461f1-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="461f1-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-138">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-140">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="461f1-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-142">**可用性**</span><span class="sxs-lookup"><span data-stu-id="461f1-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-145">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-145">The primary availability and status of the device.</span></span> <span data-ttu-id="461f1-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="461f1-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="461f1-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="461f1-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="461f1-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="461f1-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-153">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-155">指定 GPU 可用的影片記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="461f1-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-156">**標題**</span><span class="sxs-lookup"><span data-stu-id="461f1-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-159">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="461f1-159">A short description of the object.</span></span> <span data-ttu-id="461f1-160">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="461f1-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-162">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-164">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="461f1-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="461f1-165">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="461f1-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="461f1-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="461f1-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="461f1-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="461f1-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="461f1-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="461f1-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="461f1-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="461f1-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="461f1-174">)</span><span class="sxs-lookup"><span data-stu-id="461f1-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="461f1-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="461f1-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-176">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="461f1-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-178">如果相容于虛擬化，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="461f1-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="461f1-179">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="461f1-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="461f1-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="461f1-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-183">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="461f1-183">The scoping system's creation class name.</span></span> <span data-ttu-id="461f1-184">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="461f1-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="461f1-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-186">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-188">指定 GPU 專用的系統記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="461f1-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="461f1-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-190">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-192">指定 GPU 專用的影片記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="461f1-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-193">**說明**</span><span class="sxs-lookup"><span data-stu-id="461f1-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-196">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="461f1-196">A description of the object.</span></span> <span data-ttu-id="461f1-197">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="461f1-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-201">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="461f1-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="461f1-202">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="461f1-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="461f1-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="461f1-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="461f1-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="461f1-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="461f1-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="461f1-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="461f1-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="461f1-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="461f1-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="461f1-212">)</span><span class="sxs-lookup"><span data-stu-id="461f1-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="461f1-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="461f1-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-216">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="461f1-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="461f1-217">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="461f1-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="461f1-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-221">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-222">指定 GPU 所支援的 DirectX 新版。</span><span class="sxs-lookup"><span data-stu-id="461f1-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="461f1-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-224">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="461f1-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-226">指定驅動程式組建日期。</span><span class="sxs-lookup"><span data-stu-id="461f1-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="461f1-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-228">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="461f1-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-230">指定安裝驅動程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="461f1-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="461f1-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-234">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-235">指定驅動程式模型版本。</span><span class="sxs-lookup"><span data-stu-id="461f1-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="461f1-236">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="461f1-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="461f1-237">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="461f1-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-240">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-241">指定驅動程式提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="461f1-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="461f1-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-245">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-246">指定驅動程式版本。</span><span class="sxs-lookup"><span data-stu-id="461f1-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="461f1-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-250">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="461f1-250">A display name for the object.</span></span> <span data-ttu-id="461f1-251">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="461f1-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-255">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="461f1-256">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="461f1-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="461f1-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-258">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="461f1-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-260">指定是否已啟用介面卡使用 RemoteFX。</span><span class="sxs-lookup"><span data-stu-id="461f1-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="461f1-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-264">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="461f1-265">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="461f1-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="461f1-266">值</span><span class="sxs-lookup"><span data-stu-id="461f1-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="461f1-267">意義</span><span class="sxs-lookup"><span data-stu-id="461f1-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="461f1-268"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="461f1-269">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="461f1-270"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="461f1-271"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="461f1-272">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="461f1-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="461f1-273"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="461f1-274">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="461f1-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="461f1-275">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="461f1-276">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="461f1-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="461f1-277"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="461f1-278">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="461f1-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="461f1-279"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="461f1-280">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="461f1-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="461f1-281"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="461f1-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="461f1-282">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="461f1-283"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="461f1-284">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="461f1-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="461f1-285"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="461f1-286">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="461f1-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="461f1-287">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="461f1-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="461f1-288">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="461f1-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="461f1-289"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="461f1-290">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="461f1-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="461f1-291">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="461f1-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="461f1-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="461f1-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-293">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="461f1-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-295">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="461f1-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="461f1-296">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="461f1-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-298">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-300">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="461f1-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="461f1-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="461f1-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-305">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-306">包含介面卡的 GPU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="461f1-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="461f1-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-308">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-310">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="461f1-310">The current health of the element.</span></span> <span data-ttu-id="461f1-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="461f1-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-313">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-315">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="461f1-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="461f1-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="461f1-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-318">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="461f1-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-320">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="461f1-320">The date and time when the object was installed.</span></span> <span data-ttu-id="461f1-321">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="461f1-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="461f1-322">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="461f1-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-326">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="461f1-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="461f1-327">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="461f1-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="461f1-328">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="461f1-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-330">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="461f1-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-332">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="461f1-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="461f1-333">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="461f1-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-335">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-337">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="461f1-337">This property has been deprecated.</span></span> <span data-ttu-id="461f1-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-339">**名稱**</span><span class="sxs-lookup"><span data-stu-id="461f1-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-342">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="461f1-342">The label by which the object is known.</span></span> <span data-ttu-id="461f1-343">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="461f1-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-345">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-347">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="461f1-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="461f1-348">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="461f1-349">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="461f1-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="461f1-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="461f1-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="461f1-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="461f1-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="461f1-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="461f1-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="461f1-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="461f1-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="461f1-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="461f1-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="461f1-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="461f1-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="461f1-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="461f1-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="461f1-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="461f1-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="461f1-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="461f1-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="461f1-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="461f1-369">)</span><span class="sxs-lookup"><span data-stu-id="461f1-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="461f1-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="461f1-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-371">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-373">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-373">The current statuses of the object.</span></span> <span data-ttu-id="461f1-374">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="461f1-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-378">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="461f1-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="461f1-379">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="461f1-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="461f1-380">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="461f1-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="461f1-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-382">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-384">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="461f1-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="461f1-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="461f1-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-389">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="461f1-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="461f1-390">指定 GPU 所支援的圖元著色器新版。</span><span class="sxs-lookup"><span data-stu-id="461f1-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="461f1-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-392">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-394">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="461f1-394">The power management capabilities of the device.</span></span> <span data-ttu-id="461f1-395">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="461f1-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-397">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="461f1-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-399">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="461f1-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="461f1-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="461f1-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-402">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-404">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="461f1-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="461f1-405">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="461f1-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-407">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-409">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="461f1-409">Provides high level status information.</span></span> <span data-ttu-id="461f1-410">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="461f1-411">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="461f1-412">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="461f1-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="461f1-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-414"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="461f1-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="461f1-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="461f1-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="461f1-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="461f1-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="461f1-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="461f1-419">)</span><span class="sxs-lookup"><span data-stu-id="461f1-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="461f1-420">**評分**</span><span class="sxs-lookup"><span data-stu-id="461f1-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-421">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="461f1-423">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="461f1-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="461f1-424">指定此裝置的 GPU RemoteFX 評等。</span><span class="sxs-lookup"><span data-stu-id="461f1-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="461f1-425">目前未使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="461f1-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="461f1-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-427">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-429">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="461f1-430">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="461f1-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="461f1-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-432">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-434">指定 GPU 可用的共用系統記憶體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="461f1-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-435">**狀態**</span><span class="sxs-lookup"><span data-stu-id="461f1-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-438">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-438">The current status of the object.</span></span> <span data-ttu-id="461f1-439">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="461f1-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-441">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="461f1-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="461f1-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-443">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="461f1-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="461f1-444">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="461f1-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="461f1-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-446">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-448">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-448">The current state of the logical device.</span></span> <span data-ttu-id="461f1-449">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="461f1-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-451">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-452">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-453">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="461f1-453">The scoping system's creation class name.</span></span> <span data-ttu-id="461f1-454">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="461f1-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="461f1-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-456">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="461f1-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-458">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="461f1-458">The scoping system's name.</span></span> <span data-ttu-id="461f1-459">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="461f1-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="461f1-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="461f1-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-461">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="461f1-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-462">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-463">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="461f1-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="461f1-464">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="461f1-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="461f1-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-466">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-468">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="461f1-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="461f1-469">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="461f1-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="461f1-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-471">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="461f1-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-473">指定 GPU 上的視訊記憶體總量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="461f1-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="461f1-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="461f1-475">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="461f1-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="461f1-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="461f1-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="461f1-477">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="461f1-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="461f1-478">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="461f1-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="461f1-479">規格需求</span><span class="sxs-lookup"><span data-stu-id="461f1-479">Requirements</span></span>



| <span data-ttu-id="461f1-480">需求</span><span class="sxs-lookup"><span data-stu-id="461f1-480">Requirement</span></span> | <span data-ttu-id="461f1-481">值</span><span class="sxs-lookup"><span data-stu-id="461f1-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="461f1-482">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="461f1-482">Minimum supported client</span></span><br/> | <span data-ttu-id="461f1-483">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="461f1-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="461f1-484">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="461f1-484">Minimum supported server</span></span><br/> | <span data-ttu-id="461f1-485">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="461f1-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="461f1-486">命名空間</span><span class="sxs-lookup"><span data-stu-id="461f1-486">Namespace</span></span><br/>                | <span data-ttu-id="461f1-487">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="461f1-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="461f1-488">MOF</span><span class="sxs-lookup"><span data-stu-id="461f1-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="461f1-489"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="461f1-490">DLL</span><span class="sxs-lookup"><span data-stu-id="461f1-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="461f1-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="461f1-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


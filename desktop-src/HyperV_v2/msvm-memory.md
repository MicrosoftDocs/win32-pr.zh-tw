---
description: 代表目前配置給虛擬機器的記憶體。
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Msvm_Memory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852395"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="2983d-103">Msvm \_ Memory 類別</span><span class="sxs-lookup"><span data-stu-id="2983d-103">Msvm\_Memory class</span></span>

<span data-ttu-id="2983d-104">代表目前配置給虛擬機器的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2983d-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="2983d-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2983d-106">語法</span><span class="sxs-lookup"><span data-stu-id="2983d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
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
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="2983d-107">成員</span><span class="sxs-lookup"><span data-stu-id="2983d-107">Members</span></span>

<span data-ttu-id="2983d-108">**Msvm \_ Memory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2983d-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="2983d-109">方法</span><span class="sxs-lookup"><span data-stu-id="2983d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2983d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2983d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2983d-111">方法</span><span class="sxs-lookup"><span data-stu-id="2983d-111">Methods</span></span>

<span data-ttu-id="2983d-112">**Msvm \_ Memory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="2983d-113">方法</span><span class="sxs-lookup"><span data-stu-id="2983d-113">Method</span></span>                                                       | <span data-ttu-id="2983d-114">描述</span><span class="sxs-lookup"><span data-stu-id="2983d-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="2983d-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2983d-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="2983d-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2983d-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2983d-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="2983d-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2983d-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2983d-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="2983d-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="2983d-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2983d-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="2983d-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="2983d-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="2983d-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="2983d-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="2983d-124">重設虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="2983d-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="2983d-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2983d-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="2983d-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2983d-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2983d-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="2983d-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2983d-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2983d-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="2983d-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2983d-131">屬性</span><span class="sxs-lookup"><span data-stu-id="2983d-131">Properties</span></span>

<span data-ttu-id="2983d-132">**Msvm \_ Memory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2983d-133">**存取**</span><span class="sxs-lookup"><span data-stu-id="2983d-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-136">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="2983d-137">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，預設會設定為 3 (讀取/寫入支援的) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2983d-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="2983d-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-143">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-145">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-146">**可用性**</span><span class="sxs-lookup"><span data-stu-id="2983d-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-149">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="2983d-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2983d-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-151">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-153">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="2983d-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2983d-154">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2983d-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2983d-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-156">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-158">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2983d-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="2983d-159">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2983d-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="2983d-160">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="2983d-161">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為1048576。</span><span class="sxs-lookup"><span data-stu-id="2983d-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-162">**標題**</span><span class="sxs-lookup"><span data-stu-id="2983d-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-165">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="2983d-165">A short description of the object.</span></span> <span data-ttu-id="2983d-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-170">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="2983d-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2983d-171">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2983d-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2983d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2983d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="2983d-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="2983d-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="2983d-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="2983d-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2983d-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="2983d-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2983d-180">)</span><span class="sxs-lookup"><span data-stu-id="2983d-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2983d-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="2983d-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-184">使用 BasedOn 關聯將儲存範圍分層時 **，可** 供取用的區塊數目上限（大小上限）。</span><span class="sxs-lookup"><span data-stu-id="2983d-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="2983d-185">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="2983d-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-187">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-189">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2983d-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-193">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="2983d-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2983d-194">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="2983d-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-195">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="2983d-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-198">使用的資料組織類型。</span><span class="sxs-lookup"><span data-stu-id="2983d-198">The type of data organization used.</span></span> <span data-ttu-id="2983d-199">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為2。</span><span class="sxs-lookup"><span data-stu-id="2983d-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-200">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="2983d-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-203">目前維護之資料的完整複本數目。</span><span class="sxs-lookup"><span data-stu-id="2983d-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="2983d-204">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="2983d-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="2983d-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-206">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="2983d-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-208">Delta 保留的目前值。</span><span class="sxs-lookup"><span data-stu-id="2983d-208">The current value for delta reservation.</span></span> <span data-ttu-id="2983d-209">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="2983d-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-210">**說明**</span><span class="sxs-lookup"><span data-stu-id="2983d-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-213">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="2983d-213">A description of the object.</span></span> <span data-ttu-id="2983d-214">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-216">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-218">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2983d-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2983d-219">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2983d-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2983d-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="2983d-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="2983d-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="2983d-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="2983d-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="2983d-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="2983d-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2983d-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="2983d-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2983d-229">)</span><span class="sxs-lookup"><span data-stu-id="2983d-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2983d-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2983d-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-233">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="2983d-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2983d-234">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="2983d-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2983d-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-238">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2983d-238">A display name for the object.</span></span> <span data-ttu-id="2983d-239">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2983d-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-243">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2983d-244">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2983d-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2983d-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-248">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2983d-249">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="2983d-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="2983d-250">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2983d-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2983d-251">值</span><span class="sxs-lookup"><span data-stu-id="2983d-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2983d-252">意義</span><span class="sxs-lookup"><span data-stu-id="2983d-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2983d-253"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2983d-254">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="2983d-255"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2983d-256"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="2983d-257">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="2983d-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2983d-258"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2983d-259">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="2983d-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="2983d-260">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="2983d-261">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="2983d-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2983d-262"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2983d-263">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="2983d-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2983d-264"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2983d-265">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="2983d-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="2983d-266"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="2983d-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="2983d-267">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="2983d-268"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="2983d-269">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="2983d-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="2983d-270"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="2983d-271">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="2983d-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="2983d-272">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="2983d-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="2983d-273">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="2983d-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="2983d-274"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="2983d-275">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="2983d-276">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="2983d-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="2983d-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="2983d-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-278">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-280">連續記憶體區塊的結束位址。</span><span class="sxs-lookup"><span data-stu-id="2983d-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="2983d-281">由於 **StartingAddress** 屬性一律為0，因此這個值一律會反映虛擬機器中的總記憶體量。</span><span class="sxs-lookup"><span data-stu-id="2983d-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="2983d-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-285">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="2983d-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-287">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-289">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2983d-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-291">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-293">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="2983d-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-295">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-297">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="2983d-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-299">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-301">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2983d-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-305">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2983d-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-307">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-309">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2983d-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-313">描述此儲存範圍所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="2983d-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="2983d-314">這個屬性會繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，而且一律會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="2983d-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-316">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-318">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="2983d-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-320">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2983d-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-322">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory) ，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="2983d-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-324">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2983d-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-326">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-328">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-330">儲存範圍的其他狀態資訊超出在 **OperationalStatus** 中捕捉到的範圍，以及繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="2983d-331">這項額外資訊 (例如，「停用保護」、值 = 9) 是在 **VolumeStatus** 屬性中捕捉。</span><span class="sxs-lookup"><span data-stu-id="2983d-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="2983d-332">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 2 (無/不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2983d-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-334">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-336">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="2983d-336">The current health of the element.</span></span> <span data-ttu-id="2983d-337">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="2983d-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2983d-338">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2983d-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2983d-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="2983d-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2983d-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-341">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-343">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2983d-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-345">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2983d-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-347">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2983d-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2983d-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2983d-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2983d-352">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="2983d-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2983d-353">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2983d-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2983d-354">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="2983d-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-356">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-358">如果基礎儲存範圍參與儲存體冗余群組，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="2983d-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="2983d-359">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="2983d-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2983d-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-361">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2983d-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2983d-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-365">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-368">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2983d-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2983d-371">限定詞： **MaxLen** (1024) ，覆 **寫** ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2983d-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2983d-372">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2983d-372">The label by which the object is known.</span></span> <span data-ttu-id="2983d-373">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="2983d-374">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 "*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="2983d-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="2983d-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2983d-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-378">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="2983d-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2983d-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-380">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-382">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="2983d-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="2983d-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-384">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-386">如果不存在單一失敗點，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="2983d-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="2983d-387">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="2983d-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2983d-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-389">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-391">計算值，表示除以 **區塊** 的總記憶體量。</span><span class="sxs-lookup"><span data-stu-id="2983d-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="2983d-392">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="2983d-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-394">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-396">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2983d-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2983d-397">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2983d-398">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2983d-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2983d-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="2983d-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="2983d-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="2983d-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="2983d-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="2983d-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="2983d-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="2983d-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="2983d-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="2983d-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="2983d-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="2983d-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="2983d-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="2983d-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="2983d-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="2983d-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="2983d-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2983d-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="2983d-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2983d-418">)</span><span class="sxs-lookup"><span data-stu-id="2983d-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2983d-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-420">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-422">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-422">The current statuses of the object.</span></span> <span data-ttu-id="2983d-423">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2983d-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-427">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2983d-428">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2983d-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2983d-429">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2983d-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-431">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-433">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2983d-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-435">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-437">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="2983d-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-441">當 **NameFormat** 屬性包含值 1 (其他 ") 時， **Name** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="2983d-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="2983d-442">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="2983d-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-444">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-446">當 **NameNamespace** 屬性包含值 1 (其他) 時， **Name** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="2983d-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="2983d-447">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2983d-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="2983d-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-449">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-451">目前無法在不遺失資料的情況下失敗的實體封裝數目。</span><span class="sxs-lookup"><span data-stu-id="2983d-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="2983d-452">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="2983d-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2983d-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-454">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-456">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2983d-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-458">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-460">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2983d-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-462">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-464">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2983d-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-466">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-468">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="2983d-468">Provides high level status information.</span></span> <span data-ttu-id="2983d-469">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2983d-470">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2983d-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2983d-471">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2983d-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2983d-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-473"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="2983d-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="2983d-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="2983d-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2983d-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2983d-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="2983d-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2983d-478">)</span><span class="sxs-lookup"><span data-stu-id="2983d-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2983d-479">**原始**</span><span class="sxs-lookup"><span data-stu-id="2983d-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-480">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-482">如果包含的系統沒有建立或刪除此操作專案的能力，則 **為 True** 。</span><span class="sxs-lookup"><span data-stu-id="2983d-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="2983d-483">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="2983d-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-484">**目的**</span><span class="sxs-lookup"><span data-stu-id="2983d-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-485">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-487">描述媒體及其用途的字串。</span><span class="sxs-lookup"><span data-stu-id="2983d-487">A string that describes the media and its use.</span></span> <span data-ttu-id="2983d-488">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為「系統記憶體」。</span><span class="sxs-lookup"><span data-stu-id="2983d-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="2983d-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2983d-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-490">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-491">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-492">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="2983d-493">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="2983d-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="2983d-494">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="2983d-495">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="2983d-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="2983d-496">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2983d-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="2983d-497">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="2983d-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="2983d-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-499">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-501">如果媒體存取裝置依序存取儲存體，則 **為 True** 。</span><span class="sxs-lookup"><span data-stu-id="2983d-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="2983d-502">磁帶磁碟分割是依序存取的儲存範圍範例。</span><span class="sxs-lookup"><span data-stu-id="2983d-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="2983d-503">儲存體磁片區、磁碟分割和邏輯磁片代表隨機存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="2983d-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="2983d-504">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="2983d-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-505">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="2983d-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-506">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-508">由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應的起始位址。</span><span class="sxs-lookup"><span data-stu-id="2983d-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="2983d-509">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設為0。</span><span class="sxs-lookup"><span data-stu-id="2983d-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-510">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2983d-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-513">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2983d-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-515">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2983d-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2983d-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-517">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="2983d-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2983d-518">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2983d-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2983d-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-520">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-522">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2983d-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-524">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-525">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-526">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="2983d-526">The scoping system's creation class name.</span></span> <span data-ttu-id="2983d-527">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="2983d-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="2983d-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-529">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-531">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="2983d-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2983d-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-533">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2983d-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-535">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2983d-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="2983d-536">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="2983d-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2983d-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-538">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2983d-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-539">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-540">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="2983d-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2983d-541">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 "Null"。</span><span class="sxs-lookup"><span data-stu-id="2983d-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="2983d-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2983d-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-543">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2983d-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-544">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-545">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2983d-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2983d-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2983d-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-547">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2983d-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-549">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="2983d-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2983d-550">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2983d-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2983d-551">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="2983d-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2983d-552">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2983d-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2983d-553">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2983d-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2983d-554">指出記憶體是否為 volatile。</span><span class="sxs-lookup"><span data-stu-id="2983d-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="2983d-555">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="2983d-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2983d-556">備註</span><span class="sxs-lookup"><span data-stu-id="2983d-556">Remarks</span></span>

<span data-ttu-id="2983d-557">**Msvm \_ 記憶體** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="2983d-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2983d-558">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="2983d-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2983d-559">規格需求</span><span class="sxs-lookup"><span data-stu-id="2983d-559">Requirements</span></span>



| <span data-ttu-id="2983d-560">需求</span><span class="sxs-lookup"><span data-stu-id="2983d-560">Requirement</span></span> | <span data-ttu-id="2983d-561">值</span><span class="sxs-lookup"><span data-stu-id="2983d-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2983d-562">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2983d-562">Minimum supported client</span></span><br/> | <span data-ttu-id="2983d-563">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2983d-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2983d-564">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2983d-564">Minimum supported server</span></span><br/> | <span data-ttu-id="2983d-565">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2983d-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2983d-566">命名空間</span><span class="sxs-lookup"><span data-stu-id="2983d-566">Namespace</span></span><br/>                | <span data-ttu-id="2983d-567">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2983d-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2983d-568">MOF</span><span class="sxs-lookup"><span data-stu-id="2983d-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2983d-569"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2983d-570">DLL</span><span class="sxs-lookup"><span data-stu-id="2983d-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2983d-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2983d-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2983d-572">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2983d-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2983d-573">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="2983d-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="2983d-574">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="2983d-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="2983d-575">記憶體類別</span><span class="sxs-lookup"><span data-stu-id="2983d-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 


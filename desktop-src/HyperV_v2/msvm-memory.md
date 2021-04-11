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
# <a name="msvm_memory-class"></a><span data-ttu-id="7f9d6-103">Msvm \_ Memory 類別</span><span class="sxs-lookup"><span data-stu-id="7f9d6-103">Msvm\_Memory class</span></span>

<span data-ttu-id="7f9d6-104">代表目前配置給虛擬機器的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="7f9d6-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9d6-106">語法</span><span class="sxs-lookup"><span data-stu-id="7f9d6-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7f9d6-107">成員</span><span class="sxs-lookup"><span data-stu-id="7f9d6-107">Members</span></span>

<span data-ttu-id="7f9d6-108">**Msvm \_ Memory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f9d6-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="7f9d6-109">方法</span><span class="sxs-lookup"><span data-stu-id="7f9d6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f9d6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7f9d6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f9d6-111">方法</span><span class="sxs-lookup"><span data-stu-id="7f9d6-111">Methods</span></span>

<span data-ttu-id="7f9d6-112">**Msvm \_ Memory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="7f9d6-113">方法</span><span class="sxs-lookup"><span data-stu-id="7f9d6-113">Method</span></span>                                                       | <span data-ttu-id="7f9d6-114">描述</span><span class="sxs-lookup"><span data-stu-id="7f9d6-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="7f9d6-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="7f9d6-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7f9d6-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="7f9d6-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7f9d6-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="7f9d6-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="7f9d6-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="7f9d6-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="7f9d6-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="7f9d6-124">重設虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="7f9d6-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="7f9d6-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7f9d6-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="7f9d6-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7f9d6-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="7f9d6-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f9d6-131">屬性</span><span class="sxs-lookup"><span data-stu-id="7f9d6-131">Properties</span></span>

<span data-ttu-id="7f9d6-132">**Msvm \_ Memory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f9d6-133">**存取**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-136">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="7f9d6-137">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，預設會設定為 3 (讀取/寫入支援的) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-143">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-145">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-146">**可用性**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-149">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-151">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-153">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="7f9d6-154">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-156">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-158">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="7f9d6-159">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="7f9d6-160">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="7f9d6-161">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為1048576。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-162">**標題**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-165">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-165">A short description of the object.</span></span> <span data-ttu-id="7f9d6-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-170">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7f9d6-171">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9d6-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7f9d6-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7f9d6-180">)</span><span class="sxs-lookup"><span data-stu-id="7f9d6-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9d6-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-184">使用 BasedOn 關聯將儲存範圍分層時 **，可** 供取用的區塊數目上限（大小上限）。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="7f9d6-185">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-187">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-189">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-193">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7f9d6-194">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-195">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-198">使用的資料組織類型。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-198">The type of data organization used.</span></span> <span data-ttu-id="7f9d6-199">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為2。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-200">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-203">目前維護之資料的完整複本數目。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="7f9d6-204">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-206">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-208">Delta 保留的目前值。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-208">The current value for delta reservation.</span></span> <span data-ttu-id="7f9d6-209">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-210">**說明**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-213">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-213">A description of the object.</span></span> <span data-ttu-id="7f9d6-214">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-216">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-218">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7f9d6-219">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9d6-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7f9d6-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7f9d6-229">)</span><span class="sxs-lookup"><span data-stu-id="7f9d6-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9d6-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-233">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="7f9d6-234">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-238">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-238">A display name for the object.</span></span> <span data-ttu-id="7f9d6-239">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-243">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7f9d6-244">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-248">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="7f9d6-249">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="7f9d6-250">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="7f9d6-251">值</span><span class="sxs-lookup"><span data-stu-id="7f9d6-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="7f9d6-252">意義</span><span class="sxs-lookup"><span data-stu-id="7f9d6-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="7f9d6-253"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="7f9d6-254">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="7f9d6-255"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="7f9d6-256"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="7f9d6-257">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="7f9d6-258"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="7f9d6-259">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="7f9d6-260">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="7f9d6-261">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="7f9d6-262"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="7f9d6-263">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="7f9d6-264"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="7f9d6-265">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="7f9d6-266"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="7f9d6-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="7f9d6-267">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="7f9d6-268"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="7f9d6-269">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="7f9d6-270"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="7f9d6-271">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="7f9d6-272">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="7f9d6-273">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="7f9d6-274"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="7f9d6-275">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="7f9d6-276">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="7f9d6-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-278">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-280">連續記憶體區塊的結束位址。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="7f9d6-281">由於 **StartingAddress** 屬性一律為0，因此這個值一律會反映虛擬機器中的總記憶體量。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-285">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-287">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-289">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-291">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-293">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-294">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-295">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-297">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-299">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-301">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-305">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-307">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-309">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-313">描述此儲存範圍所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="7f9d6-314">這個屬性會繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，而且一律會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-316">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-318">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-320">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-322">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory) ，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-324">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-326">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-328">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-330">儲存範圍的其他狀態資訊超出在 **OperationalStatus** 中捕捉到的範圍，以及繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="7f9d6-331">這項額外資訊 (例如，「停用保護」、值 = 9) 是在 **VolumeStatus** 屬性中捕捉。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="7f9d6-332">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 2 (無/不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-334">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-336">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-336">The current health of the element.</span></span> <span data-ttu-id="7f9d6-337">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7f9d6-338">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7f9d6-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-341">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-343">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-345">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-347">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7f9d6-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-352">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-353">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7f9d6-354">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-356">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-358">如果基礎儲存範圍參與儲存體冗余群組，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="7f9d6-359">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-361">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-365">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-368">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-371">限定詞： **MaxLen** (1024) ，覆 **寫** ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-372">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-372">The label by which the object is known.</span></span> <span data-ttu-id="7f9d6-373">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="7f9d6-374">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 "*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-378">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-380">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-382">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-384">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-386">如果不存在單一失敗點，**則為 True** 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="7f9d6-387">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-389">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-391">計算值，表示除以 **區塊** 的總記憶體量。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="7f9d6-392">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-394">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-396">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7f9d6-397">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9d6-398">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7f9d6-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7f9d6-418">)</span><span class="sxs-lookup"><span data-stu-id="7f9d6-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9d6-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-420">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-422">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-422">The current statuses of the object.</span></span> <span data-ttu-id="7f9d6-423">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-427">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="7f9d6-428">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7f9d6-429">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-431">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-433">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-435">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-437">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-441">當 **NameFormat** 屬性包含值 1 (其他 ") 時， **Name** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="7f9d6-442">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-444">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-446">當 **NameNamespace** 屬性包含值 1 (其他) 時， **Name** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="7f9d6-447">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-449">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-451">目前無法在不遺失資料的情況下失敗的實體封裝數目。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="7f9d6-452">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-454">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-456">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-458">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-460">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-462">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-464">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-466">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-468">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-468">Provides high level status information.</span></span> <span data-ttu-id="7f9d6-469">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7f9d6-470">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9d6-471">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="7f9d6-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-473"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7f9d6-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="7f9d6-478">)</span><span class="sxs-lookup"><span data-stu-id="7f9d6-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9d6-479">**原始**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-480">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-482">如果包含的系統沒有建立或刪除此操作專案的能力，則 **為 True** 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="7f9d6-483">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-484">**目的**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-485">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-487">描述媒體及其用途的字串。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-487">A string that describes the media and its use.</span></span> <span data-ttu-id="7f9d6-488">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，而且一律設定為「系統記憶體」。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-490">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-491">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-492">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="7f9d6-493">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="7f9d6-494">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="7f9d6-495">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="7f9d6-496">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="7f9d6-497">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-499">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-501">如果媒體存取裝置依序存取儲存體，則 **為 True** 。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="7f9d6-502">磁帶磁碟分割是依序存取的儲存範圍範例。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="7f9d6-503">儲存體磁片區、磁碟分割和邏輯磁片代表隨機存取的範圍。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="7f9d6-504">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，一律設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-505">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-506">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-508">由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應的起始位址。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="7f9d6-509">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設為0。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-510">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-513">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-515">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="7f9d6-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-516">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-517">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7f9d6-518">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-520">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-522">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-524">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-525">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-526">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-526">The scoping system's creation class name.</span></span> <span data-ttu-id="7f9d6-527">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-529">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-531">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，但未使用。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-533">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-535">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="7f9d6-536">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-538">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-539">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-540">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7f9d6-541">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 "Null"。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-543">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-544">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-545">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-547">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-549">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7f9d6-550">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9d6-551">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9d6-552">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9d6-553">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f9d6-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9d6-554">指出記憶體是否為 volatile。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="7f9d6-555">這個屬性繼承自 [**CIM \_ 記憶體**](/windows/desktop/CIMWin32Prov/cim-memory)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f9d6-556">備註</span><span class="sxs-lookup"><span data-stu-id="7f9d6-556">Remarks</span></span>

<span data-ttu-id="7f9d6-557">**Msvm \_ 記憶體** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7f9d6-558">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="7f9d6-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f9d6-559">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f9d6-559">Requirements</span></span>



| <span data-ttu-id="7f9d6-560">需求</span><span class="sxs-lookup"><span data-stu-id="7f9d6-560">Requirement</span></span> | <span data-ttu-id="7f9d6-561">值</span><span class="sxs-lookup"><span data-stu-id="7f9d6-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9d6-562">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f9d6-562">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9d6-563">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f9d6-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7f9d6-564">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f9d6-564">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9d6-565">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f9d6-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f9d6-566">命名空間</span><span class="sxs-lookup"><span data-stu-id="7f9d6-566">Namespace</span></span><br/>                | <span data-ttu-id="7f9d6-567">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7f9d6-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7f9d6-568">MOF</span><span class="sxs-lookup"><span data-stu-id="7f9d6-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f9d6-569"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f9d6-570">DLL</span><span class="sxs-lookup"><span data-stu-id="7f9d6-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f9d6-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d6-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f9d6-572">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f9d6-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9d6-573">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="7f9d6-574">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="7f9d6-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="7f9d6-575">記憶體類別</span><span class="sxs-lookup"><span data-stu-id="7f9d6-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 


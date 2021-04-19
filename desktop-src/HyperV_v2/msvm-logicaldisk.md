---
description: 代表存放磁片磁碟機媒體，用來填入存放磁片磁碟機。
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Msvm_LogicalDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977350"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="5c07c-103">Msvm \_ LogicalDisk 類別</span><span class="sxs-lookup"><span data-stu-id="5c07c-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="5c07c-104">代表存放磁片磁碟機媒體，用來填入存放磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5c07c-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="5c07c-105">支援的媒體類型包括虛擬硬碟、虛擬磁片檔案、ISO 檔案，以及實體裝置媒體。</span><span class="sxs-lookup"><span data-stu-id="5c07c-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="5c07c-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c07c-107">語法</span><span class="sxs-lookup"><span data-stu-id="5c07c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
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
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="5c07c-108">成員</span><span class="sxs-lookup"><span data-stu-id="5c07c-108">Members</span></span>

<span data-ttu-id="5c07c-109">**Msvm \_ LogicalDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c07c-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="5c07c-110">方法</span><span class="sxs-lookup"><span data-stu-id="5c07c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c07c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5c07c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c07c-112">方法</span><span class="sxs-lookup"><span data-stu-id="5c07c-112">Methods</span></span>

<span data-ttu-id="5c07c-113">**Msvm \_ LogicalDisk** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="5c07c-114">方法</span><span class="sxs-lookup"><span data-stu-id="5c07c-114">Method</span></span>                                                            | <span data-ttu-id="5c07c-115">描述</span><span class="sxs-lookup"><span data-stu-id="5c07c-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="5c07c-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5c07c-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="5c07c-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c07c-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5c07c-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="5c07c-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c07c-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5c07c-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="5c07c-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="5c07c-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c07c-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="5c07c-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="5c07c-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="5c07c-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="5c07c-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="5c07c-125">重設服務。</span><span class="sxs-lookup"><span data-stu-id="5c07c-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="5c07c-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="5c07c-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="5c07c-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c07c-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="5c07c-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="5c07c-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5c07c-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="5c07c-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c07c-132">屬性</span><span class="sxs-lookup"><span data-stu-id="5c07c-132">Properties</span></span>

<span data-ttu-id="5c07c-133">**Msvm \_ LogicalDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c07c-134">**存取**</span><span class="sxs-lookup"><span data-stu-id="5c07c-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-137">指出媒體是否為可讀取、可寫入或兩者。</span><span class="sxs-lookup"><span data-stu-id="5c07c-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="5c07c-138">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="5c07c-139">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-139">Value</span></span>                                                                        | <span data-ttu-id="5c07c-140">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="5c07c-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5c07c-142">Unknown</span><span class="sxs-lookup"><span data-stu-id="5c07c-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="5c07c-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5c07c-144">讀。</span><span class="sxs-lookup"><span data-stu-id="5c07c-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="5c07c-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5c07c-146">寫入.</span><span class="sxs-lookup"><span data-stu-id="5c07c-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="5c07c-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5c07c-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5c07c-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="5c07c-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="5c07c-150">寫入一次。</span><span class="sxs-lookup"><span data-stu-id="5c07c-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5c07c-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-152">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-154">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="5c07c-155">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5c07c-156">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-156">Value</span></span>                                                                            | <span data-ttu-id="5c07c-157">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="5c07c-158"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="5c07c-159">不適用。</span><span class="sxs-lookup"><span data-stu-id="5c07c-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-160">**可用性**</span><span class="sxs-lookup"><span data-stu-id="5c07c-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-163">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-163">The primary availability and status of the device.</span></span> <span data-ttu-id="5c07c-164">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5c07c-165">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-165">Value</span></span>                                                                        | <span data-ttu-id="5c07c-166">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="5c07c-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="5c07c-168">不適用。</span><span class="sxs-lookup"><span data-stu-id="5c07c-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-169">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5c07c-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-170">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-172">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="5c07c-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="5c07c-173">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="5c07c-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="5c07c-174">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="5c07c-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="5c07c-175">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5c07c-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="5c07c-176">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c07c-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5c07c-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-178">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-180">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c07c-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="5c07c-181">如果區塊大小為變數，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c07c-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="5c07c-182">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，則會包含1。</span><span class="sxs-lookup"><span data-stu-id="5c07c-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="5c07c-183">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="5c07c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-187">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5c07c-187">A short description of the object.</span></span> <span data-ttu-id="5c07c-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="5c07c-189">「ISO 磁片映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-189">"ISO Disk Image"</span></span>

<span data-ttu-id="5c07c-190">「硬碟映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-190">"Hard Disk Image"</span></span>

<span data-ttu-id="5c07c-191">「磁片磁碟機映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="5c07c-192">「CD/DVD 磁片」</span><span class="sxs-lookup"><span data-stu-id="5c07c-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-196">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="5c07c-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5c07c-197">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c07c-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-199">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="5c07c-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-200">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-202">使用 [**Msvm \_ BasedOn**](msvm-basedon.md)關聯將儲存範圍分層 **時，可** 供取用的區塊數目上限（大小上限）。</span><span class="sxs-lookup"><span data-stu-id="5c07c-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="5c07c-203">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c07c-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-207">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c07c-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5c07c-208">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-209">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="5c07c-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-210">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-212">使用的資料組織類型。</span><span class="sxs-lookup"><span data-stu-id="5c07c-212">The type of data organization used.</span></span> <span data-ttu-id="5c07c-213">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="5c07c-214">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-214">Value</span></span>                                                                        | <span data-ttu-id="5c07c-215">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="5c07c-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5c07c-217">固定區塊。</span><span class="sxs-lookup"><span data-stu-id="5c07c-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-218">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="5c07c-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-221">目前維護的完整資料複本數目。</span><span class="sxs-lookup"><span data-stu-id="5c07c-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="5c07c-222">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-223">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="5c07c-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-224">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="5c07c-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-226">指定要在複本中保留以進行快取變更之空間量的百分比。</span><span class="sxs-lookup"><span data-stu-id="5c07c-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="5c07c-227">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-228">**說明**</span><span class="sxs-lookup"><span data-stu-id="5c07c-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-229">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-231">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5c07c-231">A description of the object.</span></span> <span data-ttu-id="5c07c-232">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-234">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-236">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5c07c-237">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c07c-238">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5c07c-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-242">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="5c07c-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5c07c-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-246">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5c07c-246">A display name for the object.</span></span> <span data-ttu-id="5c07c-247">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="5c07c-248">「ISO 磁片映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-248">"ISO Disk Image"</span></span>

<span data-ttu-id="5c07c-249">「硬碟映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-249">"Hard Disk Image"</span></span>

<span data-ttu-id="5c07c-250">「磁片磁碟機映射」</span><span class="sxs-lookup"><span data-stu-id="5c07c-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="5c07c-251">「CD/DVD 磁片」</span><span class="sxs-lookup"><span data-stu-id="5c07c-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5c07c-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-255">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5c07c-256">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c07c-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-260">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5c07c-261">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="5c07c-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5c07c-262">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c07c-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-263">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5c07c-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-264">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-266">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c07c-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="5c07c-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5c07c-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-271">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5c07c-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="5c07c-272">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-273">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="5c07c-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-276">描述此裝置所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="5c07c-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="5c07c-277">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-278">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-279">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-281">除了在 **OperationalStatus** 中捕捉的任何其他狀態資訊，以及其他繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="5c07c-282">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-282">Value</span></span>                                                                            | <span data-ttu-id="5c07c-283">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="5c07c-284"><dt>二級</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="5c07c-285">無/不適用。</span><span class="sxs-lookup"><span data-stu-id="5c07c-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-287">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-289">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="5c07c-289">The current health of the element.</span></span> <span data-ttu-id="5c07c-290">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="5c07c-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5c07c-291">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5c07c-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5c07c-292">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c07c-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-294">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-296">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5c07c-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="5c07c-297">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5c07c-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c07c-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-299">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5c07c-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-301">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5c07c-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5c07c-302">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c07c-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-306">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5c07c-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-307">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5c07c-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5c07c-308">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-309">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="5c07c-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-310">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-312">指出基礎儲存區是否參與儲存體冗余群組。</span><span class="sxs-lookup"><span data-stu-id="5c07c-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="5c07c-313">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5c07c-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-315">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5c07c-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-317">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c07c-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="5c07c-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-319">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5c07c-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-320">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-322">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="5c07c-322">This property has been deprecated.</span></span> <span data-ttu-id="5c07c-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-324">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5c07c-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-327">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5c07c-327">The label by which the object is known.</span></span> <span data-ttu-id="5c07c-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="5c07c-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="5c07c-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-330">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-332">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="5c07c-333">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-333">Value</span></span>                                                                         | <span data-ttu-id="5c07c-334">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="5c07c-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="5c07c-336">其他</span><span class="sxs-lookup"><span data-stu-id="5c07c-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="5c07c-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="5c07c-338">作業系統裝置名稱</span><span class="sxs-lookup"><span data-stu-id="5c07c-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-339">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="5c07c-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-340">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-342">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="5c07c-343">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-343">Value</span></span>                                                                        | <span data-ttu-id="5c07c-344">意義</span><span class="sxs-lookup"><span data-stu-id="5c07c-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5c07c-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5c07c-346">其他</span><span class="sxs-lookup"><span data-stu-id="5c07c-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="5c07c-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="5c07c-348">作業系統裝置命名空間</span><span class="sxs-lookup"><span data-stu-id="5c07c-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c07c-349">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="5c07c-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-350">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-352">指出是否不存在單一失敗點。</span><span class="sxs-lookup"><span data-stu-id="5c07c-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="5c07c-353">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5c07c-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-355">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-357">連續區塊的數目，每個區塊會封鎖 **區塊** 屬性中包含的值大小，以形成儲存區。</span><span class="sxs-lookup"><span data-stu-id="5c07c-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="5c07c-358">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="5c07c-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="5c07c-359">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="5c07c-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="5c07c-360">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-361">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-364">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5c07c-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5c07c-365">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c07c-366">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-368">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-370">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "OperationalStatus" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) </span><span class="sxs-lookup"><span data-stu-id="5c07c-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-371">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-371">The current statuses of the object.</span></span> <span data-ttu-id="5c07c-372">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="5c07c-373">當無法滿足虛擬磁片所需的 QoS 層級時，會將主要狀態 (OperationalStatus \[ 0 \]) 設定為降級 (3) ，而 OperationalStatus 陣列也會根據此資料表，另外包含指出 QoS 條件特定原因的次要狀態值。</span><span class="sxs-lookup"><span data-stu-id="5c07c-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="5c07c-374">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="5c07c-375">描述</span><span class="sxs-lookup"><span data-stu-id="5c07c-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c07c-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> 輸送量不足 (32788) </span><span class="sxs-lookup"><span data-stu-id="5c07c-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="5c07c-377">裝置目前無法使用要求的最小 IOPS 速率。</span><span class="sxs-lookup"><span data-stu-id="5c07c-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="5c07c-378">您也可以使用 OperationalStatus 來回報其他錯誤或警告狀況 (例如，.VSP 與 VSC) 之間的通訊協定不相符。</span><span class="sxs-lookup"><span data-stu-id="5c07c-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="5c07c-379">如果有多個條件存在，主要狀態會設為降級，而一或多個次要狀態值（以從索引1開始的任何順序）會填入陣列中。</span><span class="sxs-lookup"><span data-stu-id="5c07c-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5c07c-380"><span id="OK"></span><span id="ok"></span>**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="5c07c-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5c07c-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (3) **降級**</span><span class="sxs-lookup"><span data-stu-id="5c07c-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="5c07c-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="5c07c-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="5c07c-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (11) </span><span class="sxs-lookup"><span data-stu-id="5c07c-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-384">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5c07c-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (12) </span><span class="sxs-lookup"><span data-stu-id="5c07c-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="5c07c-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (13) </span><span class="sxs-lookup"><span data-stu-id="5c07c-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="5c07c-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>錯誤 (16) **中支援的實體**</span><span class="sxs-lookup"><span data-stu-id="5c07c-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-388">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="5c07c-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**通訊協定不相符** (32775) </span><span class="sxs-lookup"><span data-stu-id="5c07c-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="5c07c-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**通訊超時** (32783) </span><span class="sxs-lookup"><span data-stu-id="5c07c-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-391">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="5c07c-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**輸送量不足** (32788) </span><span class="sxs-lookup"><span data-stu-id="5c07c-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="5c07c-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**未知的 QoS 原則識別碼** (32791) </span><span class="sxs-lookup"><span data-stu-id="5c07c-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="5c07c-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span> (32792) **不支援 QoS**</span><span class="sxs-lookup"><span data-stu-id="5c07c-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-395">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="5c07c-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration 不符** (32793) </span><span class="sxs-lookup"><span data-stu-id="5c07c-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-397">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="5c07c-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**磁片已滿** (32794) </span><span class="sxs-lookup"><span data-stu-id="5c07c-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5c07c-399">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="5c07c-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5c07c-400">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-403">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5c07c-404">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5c07c-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5c07c-405">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c07c-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5c07c-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-407">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-409">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="5c07c-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="5c07c-410">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5c07c-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-411">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="5c07c-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-412">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-414">字串，描述當 **NameFormat** 包含值 1 (其他) 時， **Name** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="5c07c-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="5c07c-415">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-416">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="5c07c-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-417">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-419">字串，描述當 **NameNamespace** 包含值 1 (其他) 時， **Name** 屬性的命名空間。</span><span class="sxs-lookup"><span data-stu-id="5c07c-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="5c07c-420">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-421">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="5c07c-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-422">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-424">目前無法在不遺失資料的情況下失敗的實體封裝數目。</span><span class="sxs-lookup"><span data-stu-id="5c07c-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="5c07c-425">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-426">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5c07c-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-427">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-429">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="5c07c-429">The power management capabilities of the device.</span></span> <span data-ttu-id="5c07c-430">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5c07c-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-432">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-434">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="5c07c-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="5c07c-435">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5c07c-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-437">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-439">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="5c07c-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="5c07c-440">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-441">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5c07c-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-442">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-444">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="5c07c-444">Provides high level status information.</span></span> <span data-ttu-id="5c07c-445">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="5c07c-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="5c07c-446">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="5c07c-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c07c-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-448">**原始**</span><span class="sxs-lookup"><span data-stu-id="5c07c-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-449">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-451">指出包含的系統是否能夠建立或刪除這個操作專案。</span><span class="sxs-lookup"><span data-stu-id="5c07c-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="5c07c-452">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)，它會針對檔案型媒體將它設為 **False** ，並針對傳遞媒體設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="5c07c-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-453">**目的**</span><span class="sxs-lookup"><span data-stu-id="5c07c-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-456">描述媒體及/或其使用的字串。</span><span class="sxs-lookup"><span data-stu-id="5c07c-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="5c07c-457">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-461">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="5c07c-462">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="5c07c-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5c07c-463">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5c07c-464">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="5c07c-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="5c07c-465">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="5c07c-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="5c07c-466">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="5c07c-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="5c07c-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-468">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5c07c-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-470">指出媒體存取裝置是否依序存取儲存體。</span><span class="sxs-lookup"><span data-stu-id="5c07c-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="5c07c-471">傳遞磁帶媒體是依序存取的儲存區範例。</span><span class="sxs-lookup"><span data-stu-id="5c07c-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="5c07c-472">這個屬性繼承自 [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-473">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5c07c-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-476">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-476">The current status of the object.</span></span> <span data-ttu-id="5c07c-477">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-478">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c07c-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-479">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5c07c-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-481">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="5c07c-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5c07c-482">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5c07c-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-484">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-485">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-486">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-486">The current state of the logical device.</span></span> <span data-ttu-id="5c07c-487">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-488">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c07c-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-489">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-490">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-491">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5c07c-491">The scoping system's creation class name.</span></span> <span data-ttu-id="5c07c-492">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5c07c-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-494">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5c07c-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-496">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c07c-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="5c07c-497">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-498">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c07c-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-499">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5c07c-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-501">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="5c07c-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5c07c-502">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5c07c-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-503">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5c07c-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-504">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5c07c-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-505">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-506">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="5c07c-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="5c07c-507">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c07c-508">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5c07c-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c07c-509">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5c07c-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c07c-510">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5c07c-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c07c-511">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5c07c-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5c07c-512">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="5c07c-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c07c-513">備註</span><span class="sxs-lookup"><span data-stu-id="5c07c-513">Remarks</span></span>

<span data-ttu-id="5c07c-514">存取 **Msvm \_ LogicalDisk** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="5c07c-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5c07c-515">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="5c07c-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c07c-516">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c07c-516">Requirements</span></span>



| <span data-ttu-id="5c07c-517">需求</span><span class="sxs-lookup"><span data-stu-id="5c07c-517">Requirement</span></span> | <span data-ttu-id="5c07c-518">值</span><span class="sxs-lookup"><span data-stu-id="5c07c-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c07c-519">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c07c-519">Minimum supported client</span></span><br/> | <span data-ttu-id="5c07c-520">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c07c-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c07c-521">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c07c-521">Minimum supported server</span></span><br/> | <span data-ttu-id="5c07c-522">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c07c-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c07c-523">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c07c-523">Namespace</span></span><br/>                | <span data-ttu-id="5c07c-524">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5c07c-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c07c-525">MOF</span><span class="sxs-lookup"><span data-stu-id="5c07c-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c07c-526"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c07c-527">DLL</span><span class="sxs-lookup"><span data-stu-id="5c07c-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c07c-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c07c-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c07c-529">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c07c-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c07c-530">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="5c07c-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="5c07c-531">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="5c07c-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="5c07c-532">**Msvm \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="5c07c-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="5c07c-533">儲存類別</span><span class="sxs-lookup"><span data-stu-id="5c07c-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


---
description: 代表虛擬機器內的磁片磁碟機。
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Msvm_DisketteDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693744"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="9cc0a-103">Msvm \_ DisketteDrive 類別</span><span class="sxs-lookup"><span data-stu-id="9cc0a-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="9cc0a-104">代表虛擬機器內的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="9cc0a-105">您可以使用代表軟碟媒體的檔案來填入磁片磁碟機，或磁片磁碟機可以是空的。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="9cc0a-106">不支援實體媒體。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-106">Physical media is not supported.</span></span> <span data-ttu-id="9cc0a-107">每個磁碟控制卡都只有一個磁片磁碟機，而不是可移動的。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="9cc0a-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc0a-109">語法</span><span class="sxs-lookup"><span data-stu-id="9cc0a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="9cc0a-110">成員</span><span class="sxs-lookup"><span data-stu-id="9cc0a-110">Members</span></span>

<span data-ttu-id="9cc0a-111">**Msvm \_ DisketteDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9cc0a-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="9cc0a-112">方法</span><span class="sxs-lookup"><span data-stu-id="9cc0a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9cc0a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9cc0a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9cc0a-114">方法</span><span class="sxs-lookup"><span data-stu-id="9cc0a-114">Methods</span></span>

<span data-ttu-id="9cc0a-115">**Msvm \_ DisketteDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="9cc0a-116">方法</span><span class="sxs-lookup"><span data-stu-id="9cc0a-116">Method</span></span>                                                              | <span data-ttu-id="9cc0a-117">描述</span><span class="sxs-lookup"><span data-stu-id="9cc0a-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9cc0a-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="9cc0a-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9cc0a-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="9cc0a-121">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="9cc0a-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="9cc0a-123">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9cc0a-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="9cc0a-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9cc0a-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="9cc0a-127">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9cc0a-128">**重設**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="9cc0a-129">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9cc0a-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="9cc0a-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9cc0a-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="9cc0a-133">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9cc0a-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="9cc0a-135">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9cc0a-136">屬性</span><span class="sxs-lookup"><span data-stu-id="9cc0a-136">Properties</span></span>

<span data-ttu-id="9cc0a-137">**Msvm \_ DisketteDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cc0a-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-141">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="9cc0a-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9cc0a-143">值</span><span class="sxs-lookup"><span data-stu-id="9cc0a-143">Value</span></span>                                                                        | <span data-ttu-id="9cc0a-144">意義</span><span class="sxs-lookup"><span data-stu-id="9cc0a-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9cc0a-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="9cc0a-146">不適用。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cc0a-147">**可用性**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-150">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-150">The primary availability and status of the device.</span></span> <span data-ttu-id="9cc0a-151">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="9cc0a-152">值</span><span class="sxs-lookup"><span data-stu-id="9cc0a-152">Value</span></span>                                                                        | <span data-ttu-id="9cc0a-153">意義</span><span class="sxs-lookup"><span data-stu-id="9cc0a-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9cc0a-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="9cc0a-155">不適用。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cc0a-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-157">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-159">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9cc0a-160">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="9cc0a-161">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9cc0a-162">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9cc0a-163">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-165">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-167">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-167">The capabilities of the media access device.</span></span> <span data-ttu-id="9cc0a-168">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="9cc0a-169">值</span><span class="sxs-lookup"><span data-stu-id="9cc0a-169">Value</span></span>                                                                                | <span data-ttu-id="9cc0a-170">意義</span><span class="sxs-lookup"><span data-stu-id="9cc0a-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cc0a-171"><dt>{3，4，7}</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="9cc0a-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="9cc0a-173">**CapabilityDescriptions** 中的對應專案是「隨機存取」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="9cc0a-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="9cc0a-175">**CapabilityDescriptions** 中的對應專案是「支援寫入」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="9cc0a-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="9cc0a-177">**CapabilityDescriptions** 中的對應專案是「支援卸載式媒體」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cc0a-178">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-179">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-181">自由格式字串的陣列，提供 **功能** 屬性陣列中指出之存取裝置功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="9cc0a-182">這個陣列的每個專案都與 **功能** 陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="9cc0a-183">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-187">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-187">A short description of the object.</span></span> <span data-ttu-id="9cc0a-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-192">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9cc0a-193">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9cc0a-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-198">字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="9cc0a-199">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="9cc0a-200">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="9cc0a-201">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="9cc0a-202">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="9cc0a-203">「未壓縮」</span><span class="sxs-lookup"><span data-stu-id="9cc0a-203">"Not Compressed"</span></span>

<span data-ttu-id="9cc0a-204">不明</span><span class="sxs-lookup"><span data-stu-id="9cc0a-204">"Unknown"</span></span>

<span data-ttu-id="9cc0a-205">折疊</span><span class="sxs-lookup"><span data-stu-id="9cc0a-205">"Compressed"</span></span>

<span data-ttu-id="9cc0a-206">「未壓縮」</span><span class="sxs-lookup"><span data-stu-id="9cc0a-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-210">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9cc0a-211">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-212">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-213">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-215">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="9cc0a-216">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-217">**說明**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-220">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-220">A description of the object.</span></span> <span data-ttu-id="9cc0a-221">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-225">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9cc0a-226">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9cc0a-227">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-231">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-235">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-235">A display name for the object.</span></span> <span data-ttu-id="9cc0a-236">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-240">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9cc0a-241">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-245">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9cc0a-246">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9cc0a-247">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-248">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-249">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-251">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="9cc0a-252">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-256">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="9cc0a-257">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-258">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-261">描述此裝置所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="9cc0a-262">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-264">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-266">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-266">The current health of the element.</span></span> <span data-ttu-id="9cc0a-267">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9cc0a-268">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9cc0a-269">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-271">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-273">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="9cc0a-274">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-276">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-278">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9cc0a-279">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-283">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-284">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9cc0a-285">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-286">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-287">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-289">上次清除裝置的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="9cc0a-290">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-294">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="9cc0a-295">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-296">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-297">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-299">從載入到讀取或寫入媒體的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="9cc0a-300">例如，對於磁片磁碟機而言，這是磁片未切換至磁片的間隔時間，可供讀取/寫入 (也就是磁片以額定速度) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="9cc0a-301">針對磁帶機，這是從媒體插入的時間，用來報告應用程式已準備好。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="9cc0a-302">這通常位於磁帶的 BOT 區域。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="9cc0a-303">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-304">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-305">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-307">從媒體上的第一個位置移至最晚時間的位置所經過的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="9cc0a-308">若是磁片磁碟機，這代表完整的搜尋 + 完整的旋轉延遲。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="9cc0a-309">針對磁帶機，這代表從磁帶開頭到最遠距離點的搜尋。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="9cc0a-310"> (磁帶的結尾可能是最遠的點，但不一定如此。 ) 此屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-311">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-312">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-314">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="9cc0a-315">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-316">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-317">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-319">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="9cc0a-320">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="9cc0a-321">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-322">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-323">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-325">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-325">This property has been deprecated.</span></span> <span data-ttu-id="9cc0a-326">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-327">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-328">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-330">可以在裝置清理之前使用的最大單位。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="9cc0a-331">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-332">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-333">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-335">如果媒體在裝置中鎖定且無法被退出，則 **為 True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="9cc0a-336">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-337">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-338">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-340">裝置所存取媒體的最社區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="9cc0a-341">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-342">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-343">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-345">若為支援卸載式媒體的裝置，則為已掛接媒體以進行資料傳輸或清除裝置的次數。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9cc0a-346">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="9cc0a-347">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-348">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-351">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-351">The label by which the object is known.</span></span> <span data-ttu-id="9cc0a-352">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-353">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-354">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-356">如果媒體存取裝置需要清除，**則為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="9cc0a-357">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-358">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-359">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-361">可以支援或插入的多個個別媒體的最大數目。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="9cc0a-362">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-364">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-366">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9cc0a-367">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9cc0a-368">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-370">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-372">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-372">The current statuses of the object.</span></span> <span data-ttu-id="9cc0a-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-374">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-375">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-377">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9cc0a-378">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9cc0a-379">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-381">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-383">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="9cc0a-384">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-385">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-386">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-388">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-388">The power management capabilities of the device.</span></span> <span data-ttu-id="9cc0a-389">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-390">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-391">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-393">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="9cc0a-394">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-395">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-396">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-398">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="9cc0a-399">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-400">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-401">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-403">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-403">Provides high level status information.</span></span> <span data-ttu-id="9cc0a-404">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9cc0a-405">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9cc0a-406">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-408">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-410">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="9cc0a-411">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9cc0a-412">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9cc0a-413">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="9cc0a-414">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9cc0a-415">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-416">**安全性**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-417">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-419">為裝置定義的操作安全性。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-419">The operational security defined for the device.</span></span> <span data-ttu-id="9cc0a-420">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="9cc0a-421">值</span><span class="sxs-lookup"><span data-stu-id="9cc0a-421">Value</span></span>                                                                        | <span data-ttu-id="9cc0a-422">意義</span><span class="sxs-lookup"><span data-stu-id="9cc0a-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="9cc0a-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="9cc0a-424">無</span><span class="sxs-lookup"><span data-stu-id="9cc0a-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cc0a-425">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-426">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-428">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-428">The current status of the object.</span></span> <span data-ttu-id="9cc0a-429">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-430">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-431">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9cc0a-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-433">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9cc0a-434">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-436">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-438">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-438">The current state of the logical device.</span></span> <span data-ttu-id="9cc0a-439">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-440">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-441">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-443">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-443">The scoping system's creation class name.</span></span> <span data-ttu-id="9cc0a-444">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-446">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-448">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="9cc0a-449">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-450">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-451">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-452">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-453">針對支援卸載式媒體的裝置，即為媒體掛接在裝置上的最新日期和時間。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="9cc0a-454">對於存取不卸除式媒體的裝置（例如硬碟），此屬性沒有任何意義，也不適用。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="9cc0a-455">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-456">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-457">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-459">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9cc0a-460">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-461">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-462">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-464">針對支援卸載式媒體的裝置，總時間 (秒數，) 該媒體已掛接以進行資料傳輸或清除裝置。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="9cc0a-465">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="9cc0a-466">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-467">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-468">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-470">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="9cc0a-471">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-472">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-473">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-474">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-475">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9cc0a-476">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-477">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-478">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-479">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-480">裝置可以讀取和寫入媒體的持續性資料傳輸速率（KB/秒）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="9cc0a-481">這是持續性的原始資料費率。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="9cc0a-482">若此屬性中不應回報壓縮的最大速率或速率。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="9cc0a-483">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-484">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-485">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-487">相對於在 **MaxUnitsBeforeCleaning** 中使用的單位。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="9cc0a-488">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-489">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-490">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-491">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-492">目前使用的單位數目。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-492">The current number of units used.</span></span> <span data-ttu-id="9cc0a-493">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="9cc0a-494">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc0a-495">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9cc0a-496">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cc0a-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cc0a-497">能夠讀取或寫入媒體至其 ' unload ' 的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="9cc0a-498">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cc0a-499">備註</span><span class="sxs-lookup"><span data-stu-id="9cc0a-499">Remarks</span></span>

<span data-ttu-id="9cc0a-500">存取 **Msvm \_ DisketteDrive** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9cc0a-501">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9cc0a-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc0a-502">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cc0a-502">Requirements</span></span>



| <span data-ttu-id="9cc0a-503">需求</span><span class="sxs-lookup"><span data-stu-id="9cc0a-503">Requirement</span></span> | <span data-ttu-id="9cc0a-504">值</span><span class="sxs-lookup"><span data-stu-id="9cc0a-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc0a-505">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cc0a-505">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc0a-506">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cc0a-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9cc0a-507">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cc0a-507">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc0a-508">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cc0a-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cc0a-509">命名空間</span><span class="sxs-lookup"><span data-stu-id="9cc0a-509">Namespace</span></span><br/>                | <span data-ttu-id="9cc0a-510">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9cc0a-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9cc0a-511">MOF</span><span class="sxs-lookup"><span data-stu-id="9cc0a-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cc0a-512"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cc0a-513">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc0a-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc0a-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9cc0a-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9cc0a-515">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cc0a-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc0a-516">**CIM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="9cc0a-517">**CIM \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="9cc0a-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="9cc0a-518">儲存類別</span><span class="sxs-lookup"><span data-stu-id="9cc0a-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


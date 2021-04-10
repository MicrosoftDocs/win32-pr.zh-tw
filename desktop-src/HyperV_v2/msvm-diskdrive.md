---
description: 代表虛擬機器內的硬碟。
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Msvm_DiskDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851843"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="e5ad5-103">Msvm \_ DiskDrive 類別</span><span class="sxs-lookup"><span data-stu-id="e5ad5-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="e5ad5-104">代表虛擬機器內的硬碟。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="e5ad5-105">如果實體硬碟連接至虛擬機器) 或已填入虛擬硬碟媒體的綜合裝置，則此硬碟可以是傳遞裝置 (。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="e5ad5-106">由於虛擬和實體硬碟可以從虛擬機器新增和移除，因此有兩個資源集區與此類別相關聯，一個用於傳遞硬碟，另一個用於虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="e5ad5-107">只有在虛擬機器上線時，才能在虛擬 SCSI 控制器中新增或移除硬碟。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="e5ad5-108">只有當虛擬機器離線時，才能在虛擬 IDE 控制器中新增或移除磁片。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="e5ad5-109">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ad5-110">語法</span><span class="sxs-lookup"><span data-stu-id="e5ad5-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="e5ad5-111">成員</span><span class="sxs-lookup"><span data-stu-id="e5ad5-111">Members</span></span>

<span data-ttu-id="e5ad5-112">**Msvm \_ DiskDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5ad5-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="e5ad5-113">方法</span><span class="sxs-lookup"><span data-stu-id="e5ad5-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5ad5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e5ad5-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5ad5-115">方法</span><span class="sxs-lookup"><span data-stu-id="e5ad5-115">Methods</span></span>

<span data-ttu-id="e5ad5-116">**Msvm \_ DiskDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="e5ad5-117">方法</span><span class="sxs-lookup"><span data-stu-id="e5ad5-117">Method</span></span>                                                          | <span data-ttu-id="e5ad5-118">描述</span><span class="sxs-lookup"><span data-stu-id="e5ad5-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e5ad5-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="e5ad5-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e5ad5-121">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="e5ad5-122">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="e5ad5-123">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="e5ad5-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5ad5-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="e5ad5-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e5ad5-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="e5ad5-128">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e5ad5-129">**重設**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="e5ad5-130">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e5ad5-131">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="e5ad5-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5ad5-133">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="e5ad5-134">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e5ad5-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="e5ad5-136">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e5ad5-137">屬性</span><span class="sxs-lookup"><span data-stu-id="e5ad5-137">Properties</span></span>

<span data-ttu-id="e5ad5-138">**Msvm \_ DiskDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5ad5-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-140">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e5ad5-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-153">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-155">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-155">The capabilities of the media access device.</span></span> <span data-ttu-id="e5ad5-156">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="e5ad5-157">值</span><span class="sxs-lookup"><span data-stu-id="e5ad5-157">Value</span></span>                                                                        | <span data-ttu-id="e5ad5-158">意義</span><span class="sxs-lookup"><span data-stu-id="e5ad5-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5ad5-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e5ad5-160">**CapabilityDescriptions** 中的對應專案是「隨機存取」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="e5ad5-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="e5ad5-162">**CapabilityDescriptions** 中的對應專案是「支援寫入」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e5ad5-163">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-164">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-166">自由格式字串的陣列，提供 **功能** 屬性陣列中指出之存取裝置功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="e5ad5-167">這個陣列的每個專案都與 **功能** 屬性陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="e5ad5-168">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-169">**標題**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-172">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-172">A short description of the object.</span></span> <span data-ttu-id="e5ad5-173">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-174">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-175">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-177">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e5ad5-178">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5ad5-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5ad5-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5ad5-187">)</span><span class="sxs-lookup"><span data-stu-id="e5ad5-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5ad5-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-191">字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="e5ad5-192">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="e5ad5-193">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="e5ad5-194">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="e5ad5-195">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-197">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-199">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e5ad5-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-201">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-202">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-204">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="e5ad5-205">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為512。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-206">**說明**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-209">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-209">A description of the object.</span></span> <span data-ttu-id="e5ad5-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-214">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e5ad5-215">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5ad5-216">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5ad5-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5ad5-225">)</span><span class="sxs-lookup"><span data-stu-id="e5ad5-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5ad5-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-229">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e5ad5-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-231">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-232">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-234">主控電腦系統上的實體磁片磁碟機數目。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-238">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-238">A display name for the object.</span></span> <span data-ttu-id="e5ad5-239">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-243">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e5ad5-244">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-248">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e5ad5-249">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e5ad5-250">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e5ad5-251">值</span><span class="sxs-lookup"><span data-stu-id="e5ad5-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e5ad5-252">意義</span><span class="sxs-lookup"><span data-stu-id="e5ad5-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e5ad5-253"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="e5ad5-254">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e5ad5-255"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e5ad5-256"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="e5ad5-257">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e5ad5-258"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e5ad5-259">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="e5ad5-260">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="e5ad5-261">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e5ad5-262"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e5ad5-263">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e5ad5-264"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e5ad5-265">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="e5ad5-266"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="e5ad5-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="e5ad5-267">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="e5ad5-268"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="e5ad5-269">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e5ad5-270"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="e5ad5-271">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="e5ad5-272">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="e5ad5-273">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="e5ad5-274"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="e5ad5-275">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="e5ad5-276">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="e5ad5-277">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-278">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-280">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-285">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-288">描述此裝置所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="e5ad5-289">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 "None"。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-291">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-293">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-293">The current health of the element.</span></span> <span data-ttu-id="e5ad5-294">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e5ad5-295">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e5ad5-296">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-298">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-300">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-302">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-304">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e5ad5-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-309">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-310">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e5ad5-311">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-312">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-313">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-315">上次清除裝置的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="e5ad5-316">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-321">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-322">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-324">從載入到讀取或寫入媒體的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="e5ad5-325">例如，對於磁片磁碟機而言，這是磁片未切換至磁片的間隔時間，可供讀取/寫入 (也就是磁片以額定速度) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="e5ad5-326">針對磁帶機，這是從媒體插入的時間，用來報告應用程式已準備好。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="e5ad5-327">這通常位於磁帶的 BOT 區域。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="e5ad5-328">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) ，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-329">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-330">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-332">從媒體上的第一個位置移至最晚時間的位置所經過的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="e5ad5-333">若是磁片磁碟機，這代表完整的搜尋和完整的旋轉延遲。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="e5ad5-334">針對磁帶機，這代表從磁帶開頭到最遠距離點的搜尋。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="e5ad5-335"> (磁帶的結尾可能是最遠的點，但不一定如此。 ) 此屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-336">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-337">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-339">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="e5ad5-340">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，它會設定為512（虛擬硬碟）、傳遞磁片磁碟機的變數。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-341">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-344">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="e5ad5-345">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="e5ad5-346">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，它會設定為2000000000（虛擬硬碟）、傳遞磁片磁碟機的變數。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-347">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-348">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-350">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-351">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-352">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-354">可以在裝置清理之前使用的最大單位。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="e5ad5-355">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為0xffffffffffffffff。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-356">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-357">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-359">如果媒體在裝置中鎖定且無法被退出，則 **為 True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="e5ad5-360">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-361">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-362">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-364">裝置所存取媒體的最社區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="e5ad5-365">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為512。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-366">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-367">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-369">若為支援卸載式媒體的裝置，則為已掛接媒體以進行資料傳輸或清除裝置的次數。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="e5ad5-370">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="e5ad5-371">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-372">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-375">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-375">The label by which the object is known.</span></span> <span data-ttu-id="e5ad5-376">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-377">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-378">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-380">如果媒體存取裝置需要清除，**則為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="e5ad5-381">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且會設為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-382">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-383">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-385">可以支援或插入的多個個別媒體的最大數目。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="e5ad5-386">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為1。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-387">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-388">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-390">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e5ad5-391">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5ad5-392">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5ad5-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5ad5-412">)</span><span class="sxs-lookup"><span data-stu-id="e5ad5-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5ad5-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-414">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-416">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-416">The current statuses of the object.</span></span> <span data-ttu-id="e5ad5-417">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-418">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-419">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-421">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e5ad5-422">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e5ad5-423">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-425">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-427">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-428">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-429">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-432">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-433">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-435">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-437">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-439">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-440">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-441">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-443">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-443">Provides high level status information.</span></span> <span data-ttu-id="e5ad5-444">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e5ad5-445">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e5ad5-446">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e5ad5-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-448"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e5ad5-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e5ad5-453">)</span><span class="sxs-lookup"><span data-stu-id="e5ad5-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e5ad5-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-455">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-457">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="e5ad5-458">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e5ad5-459">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e5ad5-460">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e5ad5-461">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e5ad5-462">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-463">**安全性**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-464">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-466">為裝置定義的操作安全性。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-466">The operational security defined for the device.</span></span> <span data-ttu-id="e5ad5-467">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且設定為 3 (無) 。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-468">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-471">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-472">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-473">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5ad5-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-474">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-475">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e5ad5-476">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-478">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-479">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-480">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-481">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-482">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-484">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-484">The scoping system's creation class name.</span></span> <span data-ttu-id="e5ad5-485">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-487">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-488">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-489">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e5ad5-490">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-491">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-492">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-493">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-494">針對支援卸載式媒體的裝置，即為媒體掛接在裝置上的最新日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="e5ad5-495">對於存取不卸除式媒體的裝置（例如硬碟），此屬性沒有任何意義，也不適用。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="e5ad5-496">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-497">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-498">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-500">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e5ad5-501">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 "Null"。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-502">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-503">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-505">針對支援卸載式媒體的裝置，總時間 (秒數，) 該媒體已掛接以進行資料傳輸或清除裝置。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="e5ad5-506">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="e5ad5-507">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-508">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-509">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-510">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-511">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-512">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-513">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-515">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e5ad5-516">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-517">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-518">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-520">裝置可以讀取和寫入媒體的持續性資料傳輸速率（KB/秒）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="e5ad5-521">這是持續性的原始資料費率。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="e5ad5-522">若此屬性中不應回報壓縮的最大速率或速率。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="e5ad5-523">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-524">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-525">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-526">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-527">相對於在 **MaxUnitsBeforeCleaning** 中使用的單位。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="e5ad5-528">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-529">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-530">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-531">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-532">目前使用的單位數目。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-532">The current number of units used.</span></span> <span data-ttu-id="e5ad5-533">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad5-534">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5ad5-535">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5ad5-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5ad5-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5ad5-537">能夠讀取或寫入媒體至其卸載的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="e5ad5-538">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，且設定為0。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5ad5-539">備註</span><span class="sxs-lookup"><span data-stu-id="e5ad5-539">Remarks</span></span>

<span data-ttu-id="e5ad5-540">存取 **Msvm \_ DiskDrive** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e5ad5-541">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="e5ad5-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ad5-542">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5ad5-542">Requirements</span></span>



| <span data-ttu-id="e5ad5-543">需求</span><span class="sxs-lookup"><span data-stu-id="e5ad5-543">Requirement</span></span> | <span data-ttu-id="e5ad5-544">值</span><span class="sxs-lookup"><span data-stu-id="e5ad5-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ad5-545">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5ad5-545">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ad5-546">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5ad5-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5ad5-547">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5ad5-547">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ad5-548">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5ad5-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5ad5-549">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5ad5-549">Namespace</span></span><br/>                | <span data-ttu-id="e5ad5-550">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e5ad5-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5ad5-551">MOF</span><span class="sxs-lookup"><span data-stu-id="e5ad5-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5ad5-552"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5ad5-553">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ad5-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ad5-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad5-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5ad5-555">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5ad5-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ad5-556">**CIM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="e5ad5-557">**CIM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="e5ad5-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="e5ad5-558">儲存類別</span><span class="sxs-lookup"><span data-stu-id="e5ad5-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


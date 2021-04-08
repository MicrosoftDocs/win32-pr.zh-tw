---
description: 代表虛擬機器內的 DVD 光碟機。
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Msvm_DVDDrive 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851839"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="06916-103">Msvm \_ DVDDrive 類別</span><span class="sxs-lookup"><span data-stu-id="06916-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="06916-104">代表虛擬機器內的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="06916-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="06916-105">此 DVD 磁片磁碟機可以是傳遞裝置 (如果實體硬碟已連接至虛擬機器) 或綜合，並已填入 ISO 檔案媒體。</span><span class="sxs-lookup"><span data-stu-id="06916-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="06916-106">因為可以從虛擬機器新增和移除虛擬和實體 DVD 磁片磁碟機，所以有兩個資源集區與此類別相關聯，一個用於傳遞 DVD 磁片磁碟機，另一個用於虛擬 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="06916-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="06916-107">只有在虛擬機器離線時，才能新增或移除 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="06916-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="06916-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06916-109">語法</span><span class="sxs-lookup"><span data-stu-id="06916-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="06916-110">成員</span><span class="sxs-lookup"><span data-stu-id="06916-110">Members</span></span>

<span data-ttu-id="06916-111">**Msvm \_ DVDDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06916-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="06916-112">方法</span><span class="sxs-lookup"><span data-stu-id="06916-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="06916-113">屬性</span><span class="sxs-lookup"><span data-stu-id="06916-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06916-114">方法</span><span class="sxs-lookup"><span data-stu-id="06916-114">Methods</span></span>

<span data-ttu-id="06916-115">**Msvm \_ DVDDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06916-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="06916-116">方法</span><span class="sxs-lookup"><span data-stu-id="06916-116">Method</span></span>                                                         | <span data-ttu-id="06916-117">描述</span><span class="sxs-lookup"><span data-stu-id="06916-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="06916-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="06916-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="06916-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="06916-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="06916-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="06916-121">鎖定或釋放媒體。</span><span class="sxs-lookup"><span data-stu-id="06916-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="06916-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="06916-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="06916-123">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="06916-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="06916-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="06916-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="06916-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="06916-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="06916-127">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="06916-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="06916-128">**重設**</span><span class="sxs-lookup"><span data-stu-id="06916-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="06916-129">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="06916-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="06916-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="06916-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="06916-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="06916-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="06916-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="06916-133">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="06916-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="06916-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="06916-135">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="06916-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06916-136">屬性</span><span class="sxs-lookup"><span data-stu-id="06916-136">Properties</span></span>

<span data-ttu-id="06916-137">**Msvm \_ DVDDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06916-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="06916-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-141">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="06916-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="06916-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="06916-143">**可用性**</span><span class="sxs-lookup"><span data-stu-id="06916-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-146">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-146">The primary availability and status of the device.</span></span> <span data-ttu-id="06916-147">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="06916-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="06916-148">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="06916-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-149">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-151">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="06916-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="06916-152">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="06916-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="06916-153">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="06916-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="06916-154">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="06916-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="06916-155">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06916-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06916-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="06916-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-157">資料類型： **uint32** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-159">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="06916-159">The capabilities of the media access device.</span></span> <span data-ttu-id="06916-160">這個屬性會繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)，而且會設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="06916-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="06916-161">值</span><span class="sxs-lookup"><span data-stu-id="06916-161">Value</span></span>                                                                             | <span data-ttu-id="06916-162">意義</span><span class="sxs-lookup"><span data-stu-id="06916-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06916-163"><dt>{3，7}</dt></span><span class="sxs-lookup"><span data-stu-id="06916-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="06916-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="06916-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="06916-165">**CapabilityDescriptions** 中的對應專案是「隨機存取」。</span><span class="sxs-lookup"><span data-stu-id="06916-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="06916-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="06916-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="06916-167">**CapabilityDescriptions** 中的對應專案是「支援卸載式媒體」。</span><span class="sxs-lookup"><span data-stu-id="06916-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="06916-168">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06916-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-169">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-171">自由格式字串的陣列，提供 **功能** 屬性陣列中指出之存取裝置功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="06916-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="06916-172">這個陣列的每個專案都與 **功能** 屬性陣列中位於相同索引的專案有關。</span><span class="sxs-lookup"><span data-stu-id="06916-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="06916-173">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-174">**標題**</span><span class="sxs-lookup"><span data-stu-id="06916-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-177">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="06916-177">A short description of the object.</span></span> <span data-ttu-id="06916-178">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-179">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="06916-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-182">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="06916-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="06916-183">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06916-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="06916-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-188">字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="06916-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="06916-189">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="06916-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="06916-190">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="06916-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="06916-191">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="06916-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="06916-192">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="06916-193">「未壓縮」</span><span class="sxs-lookup"><span data-stu-id="06916-193">"Not Compressed"</span></span>

<span data-ttu-id="06916-194">不明</span><span class="sxs-lookup"><span data-stu-id="06916-194">"Unknown"</span></span>

<span data-ttu-id="06916-195">折疊</span><span class="sxs-lookup"><span data-stu-id="06916-195">"Compressed"</span></span>

<span data-ttu-id="06916-196">「未壓縮」</span><span class="sxs-lookup"><span data-stu-id="06916-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="06916-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06916-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-200">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="06916-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="06916-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-202">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="06916-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-205">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="06916-206">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-207">**說明**</span><span class="sxs-lookup"><span data-stu-id="06916-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-210">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="06916-210">A description of the object.</span></span> <span data-ttu-id="06916-211">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="06916-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-215">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="06916-216">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06916-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="06916-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-221">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="06916-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="06916-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="06916-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-225">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="06916-225">A display name for the object.</span></span> <span data-ttu-id="06916-226">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="06916-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-228">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-230">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="06916-231">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06916-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06916-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="06916-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-233">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-235">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="06916-236">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="06916-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="06916-237">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06916-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06916-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="06916-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06916-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06916-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-241">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="06916-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="06916-242">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="06916-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-246">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="06916-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="06916-247">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-248">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="06916-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-251">描述此裝置所支援之錯誤偵測和更正類型的字串。</span><span class="sxs-lookup"><span data-stu-id="06916-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="06916-252">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-253">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="06916-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-254">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-256">此裝置支援的 CD 和 DVD 格式。</span><span class="sxs-lookup"><span data-stu-id="06916-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="06916-257">這個屬性繼承自 [**CIM \_ DVDDrive**](/previous-versions//cc136812(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06916-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="06916-258">此陣列包含 ISO 的下列值。</span><span class="sxs-lookup"><span data-stu-id="06916-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="06916-259">{16，22}</span><span class="sxs-lookup"><span data-stu-id="06916-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="06916-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**Cd-rom** (16) </span><span class="sxs-lookup"><span data-stu-id="06916-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="06916-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22) </span><span class="sxs-lookup"><span data-stu-id="06916-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="06916-262">此陣列包含實體傳遞的下列值。</span><span class="sxs-lookup"><span data-stu-id="06916-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="06916-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06916-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06916-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="06916-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06916-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**Cd-rom** (16) </span><span class="sxs-lookup"><span data-stu-id="06916-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="06916-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**Cd-rom/XA** (17) </span><span class="sxs-lookup"><span data-stu-id="06916-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="06916-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18) </span><span class="sxs-lookup"><span data-stu-id="06916-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="06916-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD 可燒錄** (19) </span><span class="sxs-lookup"><span data-stu-id="06916-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="06916-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22) </span><span class="sxs-lookup"><span data-stu-id="06916-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="06916-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**Dvd-rom +** (23) </span><span class="sxs-lookup"><span data-stu-id="06916-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="06916-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24) </span><span class="sxs-lookup"><span data-stu-id="06916-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="06916-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**Dvd-rom** (25) </span><span class="sxs-lookup"><span data-stu-id="06916-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="06916-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-影片** (26) </span><span class="sxs-lookup"><span data-stu-id="06916-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="06916-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27) </span><span class="sxs-lookup"><span data-stu-id="06916-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="06916-275"><span id="CD-RW"></span><span id="cd-rw"></span>**Cd-rw (33**) </span><span class="sxs-lookup"><span data-stu-id="06916-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="06916-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34) </span><span class="sxs-lookup"><span data-stu-id="06916-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="06916-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35) </span><span class="sxs-lookup"><span data-stu-id="06916-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="06916-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD 可燒錄** (36) </span><span class="sxs-lookup"><span data-stu-id="06916-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="06916-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**Cd-rw** (37) </span><span class="sxs-lookup"><span data-stu-id="06916-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="06916-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-音訊** (38) </span><span class="sxs-lookup"><span data-stu-id="06916-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="06916-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39) </span><span class="sxs-lookup"><span data-stu-id="06916-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="06916-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40) </span><span class="sxs-lookup"><span data-stu-id="06916-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="06916-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41) </span><span class="sxs-lookup"><span data-stu-id="06916-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="06916-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42) </span><span class="sxs-lookup"><span data-stu-id="06916-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06916-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="06916-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-286">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-288">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="06916-288">The current health of the element.</span></span> <span data-ttu-id="06916-289">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="06916-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="06916-290">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="06916-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="06916-291">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06916-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-293">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-295">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06916-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="06916-296">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06916-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06916-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06916-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-298">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06916-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06916-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-300">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06916-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="06916-301">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06916-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06916-305">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="06916-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06916-306">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="06916-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="06916-307">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-308">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="06916-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-309">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06916-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06916-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-311">上次清除裝置的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06916-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="06916-312">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="06916-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-314">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06916-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06916-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-316">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06916-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="06916-317">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-318">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="06916-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-319">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-321">從「載入」到能夠讀取或寫入媒體的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="06916-322">例如，對於磁片磁碟機而言，這是磁片未切換至磁片的間隔時間，可供讀取/寫入 (也就是磁片以額定速度) 。</span><span class="sxs-lookup"><span data-stu-id="06916-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="06916-323">針對磁帶機，這是從媒體插入的時間，用來報告應用程式已準備好。</span><span class="sxs-lookup"><span data-stu-id="06916-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="06916-324">這通常位於磁帶的 BOT 區域。</span><span class="sxs-lookup"><span data-stu-id="06916-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="06916-325">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-326">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="06916-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-327">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-329">從媒體上的第一個位置移至最晚時間的位置所經過的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="06916-330">若是磁片磁碟機，這代表完整的搜尋 + 完整的旋轉延遲。</span><span class="sxs-lookup"><span data-stu-id="06916-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="06916-331">針對磁帶機，這代表從磁帶開頭到最遠距離點的搜尋。</span><span class="sxs-lookup"><span data-stu-id="06916-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="06916-332"> (磁帶的結尾可能是最遠的點，但不一定如此。 ) 此屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-333">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="06916-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-334">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-336">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="06916-337">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-338">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="06916-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-339">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-341">此裝置支援的媒體大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="06916-342">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="06916-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="06916-343">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-344">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="06916-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-345">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-347">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="06916-347">This property has been deprecated.</span></span> <span data-ttu-id="06916-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-349">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="06916-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-350">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-352">可以在裝置清理之前使用的最大單位。</span><span class="sxs-lookup"><span data-stu-id="06916-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="06916-353">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-354">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="06916-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-355">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06916-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06916-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-357">如果媒體在裝置中鎖定且無法被退出，則 **為 True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="06916-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="06916-358">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-359">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="06916-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-360">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-362">裝置所存取媒體的最社區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="06916-363">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-364">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="06916-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-365">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-367">若為支援卸載式媒體的裝置，則為已掛接媒體以進行資料傳輸或清除裝置的次數。</span><span class="sxs-lookup"><span data-stu-id="06916-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="06916-368">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="06916-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="06916-369">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-370">**名稱**</span><span class="sxs-lookup"><span data-stu-id="06916-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-371">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-373">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="06916-373">The label by which the object is known.</span></span> <span data-ttu-id="06916-374">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="06916-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="06916-375">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="06916-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-376">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06916-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06916-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-378">如果媒體存取裝置需要清除，**則為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="06916-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="06916-379">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-380">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="06916-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-381">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06916-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06916-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-383">可以支援或插入的多個個別媒體的最大數目。</span><span class="sxs-lookup"><span data-stu-id="06916-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="06916-384">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-385">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="06916-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-386">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-388">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06916-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="06916-389">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06916-390">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="06916-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-392">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-394">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-394">The current statuses of the object.</span></span> <span data-ttu-id="06916-395">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-396">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="06916-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-397">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-399">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="06916-400">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="06916-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="06916-401">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06916-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06916-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="06916-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-403">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-405">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="06916-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="06916-406">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06916-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06916-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06916-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-408">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-410">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="06916-410">The power management capabilities of the device.</span></span> <span data-ttu-id="06916-411">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-412">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="06916-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-413">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06916-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06916-414">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-415">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="06916-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="06916-416">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-417">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="06916-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-418">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-419">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-420">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="06916-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="06916-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-422">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="06916-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-423">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-425">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="06916-425">Provides high level status information.</span></span> <span data-ttu-id="06916-426">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="06916-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="06916-427">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06916-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06916-428">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="06916-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-430">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-432">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="06916-433">元素的實際狀態是由 **EnabledState** 屬性工作表示。</span><span class="sxs-lookup"><span data-stu-id="06916-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="06916-434">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="06916-435">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="06916-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="06916-436">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="06916-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="06916-437">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="06916-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="06916-438">**安全性**</span><span class="sxs-lookup"><span data-stu-id="06916-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-439">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-441">為裝置定義的操作安全性。</span><span class="sxs-lookup"><span data-stu-id="06916-441">The operational security defined for the device.</span></span> <span data-ttu-id="06916-442">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-443">**狀態**</span><span class="sxs-lookup"><span data-stu-id="06916-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-444">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-445">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-446">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-446">The current status of the object.</span></span> <span data-ttu-id="06916-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-448">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06916-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-449">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06916-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06916-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-451">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="06916-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="06916-452">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06916-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06916-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="06916-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-456">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-456">The current state of the logical device.</span></span> <span data-ttu-id="06916-457">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="06916-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-459">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-461">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="06916-461">The scoping system's creation class name.</span></span> <span data-ttu-id="06916-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="06916-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-464">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-466">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="06916-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="06916-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-468">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="06916-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-469">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06916-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06916-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-471">針對支援卸載式媒體的裝置，即為媒體掛接在裝置上的最新日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06916-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="06916-472">對於存取不卸除式媒體的裝置（例如硬碟），此屬性沒有任何意義，也不適用。</span><span class="sxs-lookup"><span data-stu-id="06916-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="06916-473">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-474">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="06916-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-475">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06916-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06916-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-477">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="06916-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="06916-478">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06916-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06916-479">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="06916-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-480">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-482">針對支援卸載式媒體的裝置，總時間 (秒數，) 該媒體已掛接以進行資料傳輸或清除裝置。</span><span class="sxs-lookup"><span data-stu-id="06916-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="06916-483">對於存取不卸除式媒體的裝置（例如硬碟），此屬性不適用，應設定為0。</span><span class="sxs-lookup"><span data-stu-id="06916-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="06916-484">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="06916-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-486">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-488">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="06916-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="06916-489">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="06916-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-491">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06916-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06916-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-493">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="06916-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="06916-494">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06916-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06916-495">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="06916-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-496">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="06916-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06916-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-498">裝置可以讀取和寫入媒體的持續性資料傳輸速率（KB/秒）。</span><span class="sxs-lookup"><span data-stu-id="06916-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="06916-499">這是持續性的原始資料費率。</span><span class="sxs-lookup"><span data-stu-id="06916-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="06916-500">若此屬性中不應回報壓縮的最大速率或速率。</span><span class="sxs-lookup"><span data-stu-id="06916-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="06916-501">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-502">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="06916-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-503">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06916-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06916-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-505">相對於在 **MaxUnitsBeforeCleaning** 中使用的單位。</span><span class="sxs-lookup"><span data-stu-id="06916-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="06916-506">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-507">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="06916-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-508">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-510">目前使用的單位數目。</span><span class="sxs-lookup"><span data-stu-id="06916-510">The current number of units used.</span></span> <span data-ttu-id="06916-511">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="06916-512">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="06916-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06916-513">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06916-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06916-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06916-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06916-515">能夠讀取或寫入媒體至其 ' unload ' 的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06916-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="06916-516">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)。</span><span class="sxs-lookup"><span data-stu-id="06916-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06916-517">備註</span><span class="sxs-lookup"><span data-stu-id="06916-517">Remarks</span></span>

<span data-ttu-id="06916-518">存取 **Msvm \_ DVDDrive** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="06916-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="06916-519">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="06916-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="06916-520">規格需求</span><span class="sxs-lookup"><span data-stu-id="06916-520">Requirements</span></span>



| <span data-ttu-id="06916-521">需求</span><span class="sxs-lookup"><span data-stu-id="06916-521">Requirement</span></span> | <span data-ttu-id="06916-522">值</span><span class="sxs-lookup"><span data-stu-id="06916-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06916-523">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06916-523">Minimum supported client</span></span><br/> | <span data-ttu-id="06916-524">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06916-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06916-525">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06916-525">Minimum supported server</span></span><br/> | <span data-ttu-id="06916-526">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06916-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06916-527">命名空間</span><span class="sxs-lookup"><span data-stu-id="06916-527">Namespace</span></span><br/>                | <span data-ttu-id="06916-528">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="06916-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06916-529">MOF</span><span class="sxs-lookup"><span data-stu-id="06916-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06916-530"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="06916-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06916-531">DLL</span><span class="sxs-lookup"><span data-stu-id="06916-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06916-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06916-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06916-533">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06916-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06916-534">**CIM \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="06916-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="06916-535">[**CIM \_ DVDDrive**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06916-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06916-536">儲存類別</span><span class="sxs-lookup"><span data-stu-id="06916-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


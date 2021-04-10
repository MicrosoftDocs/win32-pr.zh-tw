---
description: 管理虛擬機器的虛擬媒體 ( .vhd、.vhdx、.iso 或 .vfd 檔案) 。
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Msvm_ImageManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690863"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="a7ec1-103">Msvm \_ ImageManagementService 類別</span><span class="sxs-lookup"><span data-stu-id="a7ec1-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="a7ec1-104">管理虛擬機器的虛擬媒體 ( .vhd、.vhdx、.iso 或 .vfd 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="a7ec1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ec1-106">語法</span><span class="sxs-lookup"><span data-stu-id="a7ec1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
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
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="a7ec1-107">成員</span><span class="sxs-lookup"><span data-stu-id="a7ec1-107">Members</span></span>

<span data-ttu-id="a7ec1-108">**Msvm \_ ImageManagementService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7ec1-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="a7ec1-109">方法</span><span class="sxs-lookup"><span data-stu-id="a7ec1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7ec1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a7ec1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7ec1-111">方法</span><span class="sxs-lookup"><span data-stu-id="a7ec1-111">Methods</span></span>

<span data-ttu-id="a7ec1-112">**Msvm \_ ImageManagementService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="a7ec1-113">方法</span><span class="sxs-lookup"><span data-stu-id="a7ec1-113">Method</span></span>                                                                                                           | <span data-ttu-id="a7ec1-114">描述</span><span class="sxs-lookup"><span data-stu-id="a7ec1-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7ec1-115">**AttachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="a7ec1-116">以回送模式連接虛擬磁片影像檔。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="a7ec1-117">**CompactVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="a7ec1-118">壓縮虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="a7ec1-119">**ConvertVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="a7ec1-120">將現有的虛擬硬碟轉換成不同的類型或格式。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a7ec1-121">**ConvertVirtualHardDiskToVHDSet**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="a7ec1-122">藉由建立新的 VHD 設定檔案與現有的虛擬硬碟來轉換虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="a7ec1-123">**CreateVirtualFloppyDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="a7ec1-124">建立虛擬磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="a7ec1-125">**CreateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="a7ec1-126">建立虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="a7ec1-127">**DeleteVHDSnapshot**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="a7ec1-128">刪除 VHD 設定檔內的 VHD 快照集專案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="a7ec1-129">**FindMountedStorageImageInstance**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="a7ec1-130">尋找 \_ 指定磁片映射路徑的 Msvm MountedStorageImage 物件。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="a7ec1-131">**GetVHDSetInformation**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="a7ec1-132">抓取 VHD 設定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="a7ec1-133">**GetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="a7ec1-134">抓取 VHD 設定檔中 VHD 快照集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="a7ec1-135">**GetVirtualDiskChanges**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="a7ec1-136">從提供的復原變更追蹤識別碼或 VHDSet 快照集識別碼之後，抓取虛擬磁片指定區域的變更清單。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="a7ec1-137">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="a7ec1-138">抓取與虛擬硬碟檔案相關聯的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="a7ec1-139">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="a7ec1-140">捕獲虛擬硬碟檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="a7ec1-141">**MergeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="a7ec1-142">使用鏈中的一或多個父虛擬硬碟，合併差異鏈中的子系虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="a7ec1-143">**OptimizeVHDSet**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="a7ec1-144">將 VHD 設定檔案優化，以使用較少的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="a7ec1-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="a7ec1-146">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="a7ec1-147">**ResizeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="a7ec1-148">調整現有虛擬硬碟的大小。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="a7ec1-149">**SetParentVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="a7ec1-150">更新指定分葉和子虛擬硬碟檔案的父系。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="a7ec1-151">**SetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="a7ec1-152">編輯 VHD 設定檔內的 VHD 快照集專案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="a7ec1-153">如果已有問題的快照集識別碼，則會以新的專案覆寫現有的快照集專案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="a7ec1-154">否則，新的專案會新增至 VHD 設定檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="a7ec1-155">**SetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="a7ec1-156">設定虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="a7ec1-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="a7ec1-158">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="a7ec1-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="a7ec1-160">停止服務。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="a7ec1-161">**ValidatePersistentReservationSupport**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="a7ec1-162">驗證檔案系統是否可以支援啟用持續性保留的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="a7ec1-163">**ValidateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="a7ec1-164">驗證是否可在唯讀模式中開啟虛擬磁片映射。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="a7ec1-165">屬性</span><span class="sxs-lookup"><span data-stu-id="a7ec1-165">Properties</span></span>

<span data-ttu-id="a7ec1-166">**Msvm \_ ImageManagementService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7ec1-167">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-168">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7ec1-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-170">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a7ec1-171">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-172">**標題**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-175">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-175">A short description of the object.</span></span> <span data-ttu-id="a7ec1-176">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「Hyper-v 映射管理服務」。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-180">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a7ec1-181">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7ec1-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7ec1-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7ec1-190">)</span><span class="sxs-lookup"><span data-stu-id="a7ec1-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7ec1-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-194">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a7ec1-195">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ ImageManagementService"。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-196">**說明**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-199">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-199">A description of the object.</span></span> <span data-ttu-id="a7ec1-200">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來的，而且一律設定為「為 Hyper-v 提供映射管理服務」。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-204">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a7ec1-205">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7ec1-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7ec1-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7ec1-215">)</span><span class="sxs-lookup"><span data-stu-id="a7ec1-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7ec1-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-219">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-219">A display name for the object.</span></span> <span data-ttu-id="a7ec1-220">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「Hyper-v 映射管理服務」。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-222">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-224">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a7ec1-225">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-227">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-229">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a7ec1-230">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a7ec1-231">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-233">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-235">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-235">The current health of the element.</span></span> <span data-ttu-id="a7ec1-236">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a7ec1-237">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a7ec1-238">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-240">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-242">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a7ec1-243">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-247">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-248">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a7ec1-249">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-250">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-253">限定詞： **Key**、 **Override** ( "Name" ) 、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-254">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-254">The label by which the object is known.</span></span> <span data-ttu-id="a7ec1-255">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "vhdsvc"。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-259">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a7ec1-260">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7ec1-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7ec1-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7ec1-281">)</span><span class="sxs-lookup"><span data-stu-id="a7ec1-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7ec1-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-283">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7ec1-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-285">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-285">The current status of the object.</span></span> <span data-ttu-id="a7ec1-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-290">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a7ec1-291">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a7ec1-292">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-296">提供如何達到服務主要擁有者的相關資訊 (例如，電話號碼、電子郵件地址等等) 的字串。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="a7ec1-297">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-298">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-301">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="a7ec1-302">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="a7ec1-303">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-304">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-305">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-307">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-307">Provides high level status information.</span></span> <span data-ttu-id="a7ec1-308">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a7ec1-309">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7ec1-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7ec1-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-312"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7ec1-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7ec1-317">)</span><span class="sxs-lookup"><span data-stu-id="a7ec1-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7ec1-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-319">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-321">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="a7ec1-322">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a7ec1-323">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a7ec1-324">**EnabledLogicalElement** 的特定實例可能不支援 **RequestedStateChange**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="a7ec1-325">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="a7ec1-326">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-327">**已開始**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-328">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-330">指出服務是否已啟動。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="a7ec1-331">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-335">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="a7ec1-336">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-337">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-342">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7ec1-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-344">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a7ec1-345">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-349">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-349">The scoping system's creation class name.</span></span> <span data-ttu-id="a7ec1-350">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-354">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-354">The name of the hosting computer system.</span></span> <span data-ttu-id="a7ec1-355">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-357">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-359">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a7ec1-360">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a7ec1-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7ec1-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7ec1-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7ec1-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7ec1-364">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a7ec1-365">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7ec1-366">備註</span><span class="sxs-lookup"><span data-stu-id="a7ec1-366">Remarks</span></span>

<span data-ttu-id="a7ec1-367">存取 **Msvm \_ ImageManagementService** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a7ec1-368">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a7ec1-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ec1-369">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7ec1-369">Requirements</span></span>



| <span data-ttu-id="a7ec1-370">需求</span><span class="sxs-lookup"><span data-stu-id="a7ec1-370">Requirement</span></span> | <span data-ttu-id="a7ec1-371">值</span><span class="sxs-lookup"><span data-stu-id="a7ec1-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ec1-372">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7ec1-372">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ec1-373">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7ec1-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7ec1-374">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7ec1-374">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ec1-375">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7ec1-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7ec1-376">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7ec1-376">Namespace</span></span><br/>                | <span data-ttu-id="a7ec1-377">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a7ec1-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7ec1-378">MOF</span><span class="sxs-lookup"><span data-stu-id="a7ec1-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7ec1-379"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a7ec1-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7ec1-380">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ec1-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ec1-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7ec1-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a7ec1-382">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7ec1-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ec1-383">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="a7ec1-384">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="a7ec1-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="a7ec1-385">儲存類別</span><span class="sxs-lookup"><span data-stu-id="a7ec1-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


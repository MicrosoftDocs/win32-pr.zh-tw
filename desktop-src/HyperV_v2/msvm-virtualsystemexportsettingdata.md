---
description: 提供要與 Msvm VirtualSystemManagementService 類別的 ExportSystemDefinition 方法搭配使用的其他資訊 \_ 。
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979722"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="84039-103">Msvm \_ VirtualSystemExportSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="84039-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="84039-104">提供要與 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)方法搭配使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="84039-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="84039-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="84039-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84039-106">語法</span><span class="sxs-lookup"><span data-stu-id="84039-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="84039-107">成員</span><span class="sxs-lookup"><span data-stu-id="84039-107">Members</span></span>

<span data-ttu-id="84039-108">**Msvm \_ VirtualSystemExportSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84039-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="84039-109">屬性</span><span class="sxs-lookup"><span data-stu-id="84039-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84039-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84039-110">Properties</span></span>

<span data-ttu-id="84039-111">**Msvm \_ VirtualSystemExportSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84039-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84039-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="84039-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-113">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="84039-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84039-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-115">指出如何使用匯出的備份組的意圖。</span><span class="sxs-lookup"><span data-stu-id="84039-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="84039-116">這個屬性是在 Windows 10 和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="84039-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="84039-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0) </span><span class="sxs-lookup"><span data-stu-id="84039-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="84039-118">所有匯出的完整和差異備份集都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="84039-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="84039-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1) </span><span class="sxs-lookup"><span data-stu-id="84039-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="84039-120">匯出的完整和差異備份集會合並到合成的完整備份集。</span><span class="sxs-lookup"><span data-stu-id="84039-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84039-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="84039-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84039-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84039-124">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="84039-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="84039-125">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="84039-125">A short description of the object.</span></span> <span data-ttu-id="84039-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84039-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84039-127">**CaptureLiveState**</span><span class="sxs-lookup"><span data-stu-id="84039-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-128">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="84039-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84039-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-130">指出當匯出的目標是執行中的 VM 時，要捕捉的狀態。</span><span class="sxs-lookup"><span data-stu-id="84039-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="84039-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0) </span><span class="sxs-lookup"><span data-stu-id="84039-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="84039-132">針對執行中的 VM，將不會匯出任何儲存的狀態檔案，使其處於損毀一致狀態。</span><span class="sxs-lookup"><span data-stu-id="84039-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="84039-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1) </span><span class="sxs-lookup"><span data-stu-id="84039-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="84039-134">執行中 VM 的儲存狀態檔案將會連同 VM 設定一起匯出。</span><span class="sxs-lookup"><span data-stu-id="84039-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="84039-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2) </span><span class="sxs-lookup"><span data-stu-id="84039-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="84039-136">將會匯出正在執行之 VM 的應用程式一致狀態。</span><span class="sxs-lookup"><span data-stu-id="84039-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="84039-137">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84039-138">**CopySnapshotConfiguration**</span><span class="sxs-lookup"><span data-stu-id="84039-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-139">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="84039-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84039-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-141">指出要與虛擬機器一起匯出的快照集。</span><span class="sxs-lookup"><span data-stu-id="84039-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="84039-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0) </span><span class="sxs-lookup"><span data-stu-id="84039-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="84039-143">所有快照將會與虛擬機器一起匯出。</span><span class="sxs-lookup"><span data-stu-id="84039-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="84039-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1) </span><span class="sxs-lookup"><span data-stu-id="84039-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="84039-145">虛擬機器將不會匯出任何快照集。</span><span class="sxs-lookup"><span data-stu-id="84039-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="84039-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2) </span><span class="sxs-lookup"><span data-stu-id="84039-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="84039-147">**SnapshotVirtualSystem** 屬性所識別的快照將會連同虛擬機器一起匯出。</span><span class="sxs-lookup"><span data-stu-id="84039-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="84039-148">**CopyVmStorage** 和 **CopyVmRuntimeInformation** 屬性會被忽略，儲存體和執行時間資訊會隨著虛擬機器一起匯出，且任何 vhd 差異磁片都會合並到新的 vhd。</span><span class="sxs-lookup"><span data-stu-id="84039-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="84039-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3) </span><span class="sxs-lookup"><span data-stu-id="84039-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="84039-150">**SnapshotVirtualSystem** 屬性所識別的快照集會基於備份 VM 的目的匯出。</span><span class="sxs-lookup"><span data-stu-id="84039-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="84039-151">匯出的設定將會使用 VM 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="84039-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="84039-152">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84039-153">**CopyVmRuntimeInformation**</span><span class="sxs-lookup"><span data-stu-id="84039-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-154">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84039-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84039-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-156">指出當虛擬機器匯出時，是否將複製虛擬機器執行時間資訊。</span><span class="sxs-lookup"><span data-stu-id="84039-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="84039-157">值</span><span class="sxs-lookup"><span data-stu-id="84039-157">Value</span></span>                                                                                | <span data-ttu-id="84039-158">意義</span><span class="sxs-lookup"><span data-stu-id="84039-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84039-159"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="84039-160">將會複製虛擬機器執行時間資訊。</span><span class="sxs-lookup"><span data-stu-id="84039-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="84039-161"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="84039-162">虛擬機器執行時間資訊將不會複製。</span><span class="sxs-lookup"><span data-stu-id="84039-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84039-163">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="84039-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-164">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84039-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84039-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-166">指出當虛擬機器匯出時，是否複製虛擬機器存放裝置。</span><span class="sxs-lookup"><span data-stu-id="84039-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="84039-167">值</span><span class="sxs-lookup"><span data-stu-id="84039-167">Value</span></span>                                                                                | <span data-ttu-id="84039-168">意義</span><span class="sxs-lookup"><span data-stu-id="84039-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="84039-169"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="84039-170">將會複製虛擬機器存放裝置。</span><span class="sxs-lookup"><span data-stu-id="84039-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="84039-171"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="84039-172">虛擬機器存放裝置將不會複製。</span><span class="sxs-lookup"><span data-stu-id="84039-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84039-173">**CreateVmExportSubdirectory**</span><span class="sxs-lookup"><span data-stu-id="84039-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84039-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84039-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-176">指出當虛擬機器匯出時，是否會建立具有虛擬機器名稱的子目錄。</span><span class="sxs-lookup"><span data-stu-id="84039-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="84039-177">值</span><span class="sxs-lookup"><span data-stu-id="84039-177">Value</span></span>                                                                                | <span data-ttu-id="84039-178">意義</span><span class="sxs-lookup"><span data-stu-id="84039-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="84039-179"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="84039-180">將會建立子目錄。</span><span class="sxs-lookup"><span data-stu-id="84039-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="84039-181"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="84039-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="84039-182">將不會建立子目錄。</span><span class="sxs-lookup"><span data-stu-id="84039-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84039-183">**說明**</span><span class="sxs-lookup"><span data-stu-id="84039-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84039-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84039-186">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="84039-186">A description of the object.</span></span> <span data-ttu-id="84039-187">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84039-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84039-188">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="84039-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-191">差異匯出的基底。</span><span class="sxs-lookup"><span data-stu-id="84039-191">Base for differential export.</span></span> <span data-ttu-id="84039-192">這是 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 實例的路徑，代表 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 實例的參考點或路徑，代表要當做差異匯出基底使用的快照集。</span><span class="sxs-lookup"><span data-stu-id="84039-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="84039-193">如果 **CopySnapshotConfiguration** 屬性未設定為 3 (**ExportOneSnapshotForBackup**) ，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="84039-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="84039-194">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="84039-195">**DisableDifferentialOfIgnoredStorage**</span><span class="sxs-lookup"><span data-stu-id="84039-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84039-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84039-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-198">指出是否要建立差異磁片，而不會在匯出期間忽略儲存體。</span><span class="sxs-lookup"><span data-stu-id="84039-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="84039-199">根據預設，這會設定為 false，這表示會為不會複製到匯出目的地的儲存體建立差異磁片。</span><span class="sxs-lookup"><span data-stu-id="84039-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="84039-200">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="84039-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84039-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84039-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84039-204">這個實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="84039-204">The display name for this instance.</span></span> <span data-ttu-id="84039-205">此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。</span><span class="sxs-lookup"><span data-stu-id="84039-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="84039-206">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84039-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84039-207">**ExcludedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="84039-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-208">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="84039-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84039-209">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-210">[**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)的陣列 (RASD) 實例識別碼，代表要求從匯出作業中排除的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="84039-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="84039-211">如果至少有一個提供的識別碼不是有效的附加虛擬硬碟，則作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="84039-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="84039-212">此屬性所參考的虛擬硬碟可能來自 VM 和/或其任何快照集。</span><span class="sxs-lookup"><span data-stu-id="84039-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="84039-213">當屬性 **CopySnapshotConfiguration** 設定為0時，不支援排除虛擬硬碟 (ExportAllSnapshots) 。</span><span class="sxs-lookup"><span data-stu-id="84039-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="84039-214">請注意，虛擬硬碟的 RASD 實例識別碼代表它們所連接的位置，而透過此識別碼排除的所有虛擬硬碟都不會在整個虛擬機器的快照集樹狀結構中，排除所有連接的虛擬硬碟，而不管它們是否真的是有效的虛擬硬碟鏈。</span><span class="sxs-lookup"><span data-stu-id="84039-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="84039-215">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="84039-216">**ExportForLiveMigration**</span><span class="sxs-lookup"><span data-stu-id="84039-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-217">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84039-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84039-218">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-219">指出匯出的 VM 是否適合用於即時移轉。</span><span class="sxs-lookup"><span data-stu-id="84039-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="84039-220">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="84039-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="84039-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84039-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84039-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84039-224">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="84039-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="84039-225">在具現化命名空間的範圍內，會以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="84039-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="84039-226">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84039-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84039-227">**SnapshotVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="84039-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84039-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84039-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84039-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84039-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84039-230">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例的路徑，代表要與虛擬機器一起匯出的快照集。</span><span class="sxs-lookup"><span data-stu-id="84039-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="84039-231">如果 **CopySnapshotConfiguration** 屬性未設定為 2 (ExportOneSnapshot) ，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="84039-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84039-232">備註</span><span class="sxs-lookup"><span data-stu-id="84039-232">Remarks</span></span>

<span data-ttu-id="84039-233">存取 **Msvm \_ VirtualSystemExportSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="84039-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="84039-234">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="84039-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="84039-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="84039-235">Requirements</span></span>



| <span data-ttu-id="84039-236">需求</span><span class="sxs-lookup"><span data-stu-id="84039-236">Requirement</span></span> | <span data-ttu-id="84039-237">值</span><span class="sxs-lookup"><span data-stu-id="84039-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84039-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84039-238">Minimum supported client</span></span><br/> | <span data-ttu-id="84039-239">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84039-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84039-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84039-240">Minimum supported server</span></span><br/> | <span data-ttu-id="84039-241">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84039-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84039-242">命名空間</span><span class="sxs-lookup"><span data-stu-id="84039-242">Namespace</span></span><br/>                | <span data-ttu-id="84039-243">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="84039-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84039-244">MOF</span><span class="sxs-lookup"><span data-stu-id="84039-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84039-245"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="84039-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84039-246">DLL</span><span class="sxs-lookup"><span data-stu-id="84039-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84039-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84039-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84039-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84039-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84039-249">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="84039-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="84039-250">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="84039-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="84039-251">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="84039-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


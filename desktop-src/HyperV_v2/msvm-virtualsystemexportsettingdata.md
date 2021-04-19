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
# <a name="msvm_virtualsystemexportsettingdata-class"></a>Msvm \_ VirtualSystemExportSettingData 類別

提供要與 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)方法搭配使用的其他資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**Msvm \_ VirtualSystemExportSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemExportSettingData** 類別具有這些屬性。

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出如何使用匯出的備份組的意圖。

> [!Note]  
> 這個屬性是在 Windows 10 和 Windows Server 2016 中新增的。

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0) 


</dt> <dd>

所有匯出的完整和差異備份集都會保持不變。

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1) 


</dt> <dd>

匯出的完整和差異備份集會合並到合成的完整備份集。

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當匯出的目標是執行中的 VM 時，要捕捉的狀態。

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0) 


</dt> <dd>

針對執行中的 VM，將不會匯出任何儲存的狀態檔案，使其處於損毀一致狀態。

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1) 


</dt> <dd>

執行中 VM 的儲存狀態檔案將會連同 VM 設定一起匯出。

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2) 


</dt> <dd>

將會匯出正在執行之 VM 的應用程式一致狀態。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出要與虛擬機器一起匯出的快照集。

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0) 


</dt> <dd>

所有快照將會與虛擬機器一起匯出。

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1) 


</dt> <dd>

虛擬機器將不會匯出任何快照集。

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2) 


</dt> <dd>

**SnapshotVirtualSystem** 屬性所識別的快照將會連同虛擬機器一起匯出。 **CopyVmStorage** 和 **CopyVmRuntimeInformation** 屬性會被忽略，儲存體和執行時間資訊會隨著虛擬機器一起匯出，且任何 vhd 差異磁片都會合並到新的 vhd。

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3) 


</dt> <dd>

**SnapshotVirtualSystem** 屬性所識別的快照集會基於備份 VM 的目的匯出。 匯出的設定將會使用 VM 的識別碼。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當虛擬機器匯出時，是否將複製虛擬機器執行時間資訊。



| 值                                                                                | 意義                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**對**</dt> </dl>  | 將會複製虛擬機器執行時間資訊。<br/>     |
| <dl> <dt>**否**</dt> </dl> | 虛擬機器執行時間資訊將不會複製。<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當虛擬機器匯出時，是否複製虛擬機器存放裝置。



| 值                                                                                | 意義                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**對**</dt> </dl>  | 將會複製虛擬機器存放裝置。<br/>     |
| <dl> <dt>**否**</dt> </dl> | 虛擬機器存放裝置將不會複製。<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出當虛擬機器匯出時，是否會建立具有虛擬機器名稱的子目錄。



| 值                                                                                | 意義                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**對**</dt> </dl>  | 將會建立子目錄。<br/>     |
| <dl> <dt>**否**</dt> </dl> | 將不會建立子目錄。<br/> |



 

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

差異匯出的基底。 這是 [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 實例的路徑，代表 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 實例的參考點或路徑，代表要當做差異匯出基底使用的快照集。 如果 **CopySnapshotConfiguration** 屬性未設定為 3 (**ExportOneSnapshotForBackup**) ，則會忽略這個屬性。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否要建立差異磁片，而不會在匯出期間忽略儲存體。 根據預設，這會設定為 false，這表示會為不會複製到匯出目的地的儲存體建立差異磁片。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個實例的顯示名稱。 此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

[**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)的陣列 (RASD) 實例識別碼，代表要求從匯出作業中排除的虛擬硬碟。 如果至少有一個提供的識別碼不是有效的附加虛擬硬碟，則作業將會失敗。

此屬性所參考的虛擬硬碟可能來自 VM 和/或其任何快照集。 當屬性 **CopySnapshotConfiguration** 設定為0時，不支援排除虛擬硬碟 (ExportAllSnapshots) 。

請注意，虛擬硬碟的 RASD 實例識別碼代表它們所連接的位置，而透過此識別碼排除的所有虛擬硬碟都不會在整個虛擬機器的快照集樹狀結構中，排除所有連接的虛擬硬碟，而不管它們是否真的是有效的虛擬硬碟鏈。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出匯出的 VM 是否適合用於即時移轉。

> [!Note]  
> 已在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

在具現化命名空間的範圍內，會以不透明和唯一的方式識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例的路徑，代表要與虛擬機器一起匯出的快照集。 如果 **CopySnapshotConfiguration** 屬性未設定為 2 (ExportOneSnapshot) ，則會忽略這個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemExportSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


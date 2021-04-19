---
description: 將設定資料匯出為傳入 Msvm CollectionSnapshotService 類別的 ExportSnapshot 方法 \_ 。
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973251"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>Msvm \_ CollectionSnapshotExportSettingData 類別

將設定資料匯出為傳入 [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) 類別的 ExportSnapshot 方法。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>成員

**Msvm \_ CollectionSnapshotExportSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ CollectionSnapshotExportSettingData** 類別具有這些屬性。

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出將如何使用匯出的備份組的意圖：

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1) 


</dt> <dd>

所有匯出的完整和差異備份集都會保持不變。

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2) 


</dt> <dd>

匯出的完整和差異備份集會合並到合成的完整備份集。

</dd> </dl>

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

若 **為 true**，則會在匯出 vm 時複製 vm 儲存體。 否則 **為 false。**

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

差異匯出的基底。 這是代表參考點之 [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) 實例的路徑，或 [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) 實例的路徑，代表要當做差異匯出基底使用的快照集。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 





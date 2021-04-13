---
description: 提供要與 Msvm VirtualSystemSnapshotService 類別的 >icloudblob.createsnapshot 方法搭配使用的其他資訊 \_ 。
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386104"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a>Msvm \_ VirtualSystemSnapshotSettingData 類別

提供要與 [**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)類別的 [**>icloudblob.createsnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md)方法搭配使用的其他資訊。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemSnapshotSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemSnapshotSettingData** 類別具有這些屬性。

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

快照集的一致性層級。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**應用程式一致** (1) 


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

損 **毀一致** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestBackupType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要在來賓內部使用的備份類型。

> [!Note]  
> 在 Windows 10 中新增的屬性，版本1703

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Undefined** (0)


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

**完整** (1) 


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

**複製** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IgnoreNonSnapshottableDisks**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定在建立快照集時，是否要忽略非 snapshottable 磁片，例如傳遞磁片和光纖通道磁片。

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

 

 





---
description: SystemConfig_V0_LogDisk 類別-此類別是邏輯磁片設定事件的事件種類類別。
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 42b17cf31dcb3830cd35f046a7fcbad1858f8ae4f728fc1417339962a4be4441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927518"
---
# <a name="systemconfig_v0_logdisk-class"></a>SystemConfig \_ V0 \_ LogDisk 類別

此類別是邏輯磁片設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>成員

**SystemConfig \_ V0 \_ LogDisk** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ V0 \_ LogDisk** 類別具有這些屬性。

<dl> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) 
</dt> </dl>

每個磁區中實體磁片磁碟機的位元組數目。

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

包含此分割區之磁片的索引編號。

</dd> <dt>

**DriveLetterString**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) ， **最大** (4) 
</dt> </dl>

磁片磁碟機號，格式為 " <letter> ："。

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

磁片磁碟機的類型。 可能的值包括：



| 值                                                                        | 意義                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | 資料分割<br/>                            |
| <dl> <dt>2</dt> </dl> | 磁碟區<br/>                               |
| <dl> <dt>3</dt> </dl> | 多個磁片上的延伸磁碟分割<br/> |



 

</dd> <dt>

**檔**
</dt> <dd> <dl> <dt>

資料類型： **char16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (13) ， **最大** (16) 
</dt> </dl>

邏輯磁片上的檔案系統，例如 NTFS。

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 
</dt> </dl>

指定磁片區中的可用群集數目。

</dd> <dt>

**墊**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 
</dt> </dl>

保留的。

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) 
</dt> </dl>

資料分割的索引編號。

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

分割區的總大小（以位元組為單位）。

</dd> <dt>

**SectorsPerCluster**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) 
</dt> </dl>

磁片區中的磁區數目。

</dd> <dt>

**大小**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 
</dt> </dl>

磁片磁碟機的大小（以位元組為單位）。

</dd> <dt>

**Startoffset 位置**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 
</dt> </dl>

從磁片開頭開始，資料分割的位移 (位元組) 。

</dd> <dt>

**TotalNumberOfClusters**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) 
</dt> </dl>

磁片區中已使用和可用的叢集數目。

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (14) 
</dt> </dl>

保留的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 





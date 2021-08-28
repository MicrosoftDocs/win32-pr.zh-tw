---
description: SystemConfig_LogDisk 類別-此類別是邏輯磁片設定事件的事件種類類別。
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 326509ea080b052c0ff435e0a6e573bf54ac298c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880754"
---
# <a name="systemconfig_logdisk-class"></a>SystemConfig \_ LogDisk 類別

此類別是邏輯磁片設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a>成員

**SystemConfig \_ LogDisk** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ LogDisk** 類別具有這些屬性。

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

限定詞： **WmiDataId** (6) 、 **Max** (4) 、 **Format ( "s" )**
</dt> </dl>

磁片磁碟機號，格式為 " &lt; letter &gt; ："。

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

限定詞： **WmiDataId** (14) 、 **Max** (16) 、 **Format ( "s" )**
</dt> </dl>

邏輯磁片上的檔案系統，例如 NTFS。

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) 
</dt> </dl>

指定磁片區中的可用群集數目。

</dd> <dt>

**Pad1**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 
</dt> </dl>

未使用。

</dd> <dt>

**Pad2**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 
</dt> </dl>

未使用。

</dd> <dt>

**Pad3**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (16) 
</dt> </dl>

未使用。

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

限定詞： **WmiDataId** (13) 
</dt> </dl>

磁片區中已使用和可用的叢集數目。

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (15) 
</dt> </dl>

保留的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 





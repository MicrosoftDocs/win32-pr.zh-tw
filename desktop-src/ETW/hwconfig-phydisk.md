---
description: HWConfig \_ PhyDisk 類別是實體磁片設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: ee8a578154e2acedb5d5c8ca6d5eea4f79737e5a2cfb89b0cb658526094fd09c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086398"
---
# <a name="hwconfig_phydisk-class"></a>HWConfig \_ PhyDisk 類別

**HWConfig \_ PhyDisk** 類別是實體磁片設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  string Manufacturer;
};
```

## <a name="members"></a>成員

**HWConfig \_ PhyDisk** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**HWConfig \_ PhyDisk** 類別具有這些屬性。

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

每個磁區中實體磁片磁碟機的位元組數目。

</dd> <dt>

缸
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

實體磁片磁碟機上的圓柱總數。 注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。 如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。 請洽詢製造商取得準確的磁片磁碟機規格。

</dd> <dt>

DiskNumber
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

包含此分割區之磁片的索引編號。

</dd> <dt>

製造商
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

磁片磁碟機製造商的名稱。

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) 
</dt> </dl>

Scsi 邏輯單元編號 (LUN) 的 SCSI 介面卡。

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 
</dt> </dl>

SCSI 介面卡的 SCSI 匯流排號碼。

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

SCSI 介面卡的 SCSI 號碼。

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

包含目標裝置的編號。

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

此實體磁片磁碟機每個播放軌中的磁區數目。

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

實體磁片磁碟機上每個圓柱的曲目數目。 注意：這個屬性的值是透過 BIOS 中斷13h 的擴充功能取得。 如果磁片磁碟機使用轉譯配置來支援高容量磁片大小，則此值可能不正確。 請洽詢製造商取得準確的磁片磁碟機規格。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 





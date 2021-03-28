---
description: HWConfig \_ LogDisk 類別是邏輯磁片設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513917"
---
# <a name="hwconfig_logdisk-class"></a>HWConfig \_ LogDisk 類別

**HWConfig \_ LogDisk** 類別是邏輯磁片設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>成員

**HWConfig \_ LogDisk** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**HWConfig \_ LogDisk** 類別具有這些屬性。

<dl> <dt>

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

Pad
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

保留的。

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

分割區的總大小（以位元組為單位）。

</dd> <dt>

Startoffset 位置
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

從磁片開頭開始，資料分割的位移 (位元組) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 





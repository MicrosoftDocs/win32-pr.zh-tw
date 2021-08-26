---
description: 此類別是事件種類類別，可標示磁片 i/o 讀取、寫入和清除事件的開頭。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60c1f2be2e90ddb8b3d7a396bfa925f0b7e83181effe7fb8c947bd911133f441
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963138"
---
# <a name="diskio_typegroup2-class"></a>DiskIo \_ TypeGroup2 類別

此類別是事件種類類別，可標示磁片 i/o 讀取、寫入和清除事件的開頭。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>成員

**DiskIo \_ TypeGroup2** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DiskIo \_ TypeGroup2** 類別具有這些屬性。

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) ， [**指標**](event-tracing-mof-qualifiers.md)
</dt> </dl>

I/o 要求封包。 這個屬性會識別 IO 活動。

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) 
</dt> </dl>

發行執行緒的識別碼。

**Windows server 2008 R2、Windows Server 2008、Windows 7 和 Windows Vista：** 不支援這個屬性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 





---
description: 這個類別是磁片 i/o flush 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: DiskIo_TypeGroup3 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e421a8bd596869ac06af61f05ed1af8c633fb23b95e576398de6418620249c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050658"
---
# <a name="diskio_typegroup3-class"></a>DiskIo \_ TypeGroup3 類別

這個類別是磁片 i/o flush 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>成員

**DiskIo \_ TypeGroup3** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DiskIo \_ TypeGroup3** 類別具有這些屬性。

<dl> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) 
</dt> </dl>

識別實體磁片的編號。

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) 
</dt> </dl>

從作業開始到作業結束的 CPU 滴答計數。

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) ， [**指標**](event-tracing-mof-qualifiers.md)
</dt> </dl>

I/o 要求封包。 這個屬性會識別 i/o 活動。

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) ， [**格式**](event-tracing-mof-qualifiers.md) ( "x" ) 
</dt> </dl>

可以包含下列一或多個 (在 Ntddk 中定義的 i/o 要求封包旗標，這是) 的 DDK 標頭檔：

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOCACHE**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **IRP \_ 分頁 \_ IO**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **IRP \_ 掛接 \_ 完成**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **IRP \_ 同步 \_ API**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **IRP \_ 相關聯的 \_ IRP**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **IRP \_ 緩衝 \_ IO**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**IRP \_ 解除配置 \_ 緩衝區**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **IRP \_ 輸入 \_ 作業**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **IRP \_ 同步 \_ 分頁 \_ IO**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **IRP \_ 建立 \_ 作業**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**IRP \_ 讀取 \_ 操作**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **IRP \_ 寫入 \_ 操作**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **IRP \_ 關閉 \_ 操作**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **IRP \_ 延遲 \_ IO \_ 完成**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) 
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

 

 





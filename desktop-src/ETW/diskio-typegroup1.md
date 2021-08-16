---
description: 這個類別是磁片 i/o 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: DiskIo_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3a69643602a59fa7be8cd844f3f2908c92e2e08545f7444d1002ec1542b36730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814974"
---
# <a name="diskio_typegroup1-class"></a>DiskIo \_ TypeGroup1 類別

這個類別是磁片 i/o 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>成員

**DiskIo \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**DiskIo \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) 
</dt> </dl>

從實體磁片開頭的位元組位移。

</dd> <dt>

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

**FileObject**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (6) ， [**指標**](event-tracing-mof-qualifiers.md)
</dt> </dl>

將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷與 i/o 作業相關的檔案。

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (8) 
</dt> </dl>

[**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter)滴答單位) 中，資料分割管理員 (所測量的 i/o 初始和完成之間的時間。

**Windows Server 2003：** 這個屬性的 [**WmiDataId**](event-tracing-mof-qualifiers.md)值為7。

**Windows 2000 伺服器和 Windows 2000 Professional：** 不支援這個屬性。

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (7) ， [**指標**](event-tracing-mof-qualifiers.md)
</dt> </dl>

用來識別 i/o 活動的 i/o 要求封包。

**Windows server 2003、Windows 2000 伺服器和 Windows 2000 Professional：** 不支援這個屬性。

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

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (9) 
</dt> </dl>

發行執行緒的識別碼。

**Windows server 2008 R2、Windows Server 2008、Windows 7、Windows Vista、Windows server 2003 SP1、Windows server 2003、Windows 2000 Server 和 Windows 2000 Professional：** 不支援這個屬性。

</dd> <dt>

**已保留**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) 
</dt> </dl>

保留的。

**Windows server 2008 R2、Windows Server 2008 和 Windows 7：** 屬性的名稱是 **[queuedepth**，其中包含從作業開始到作業結束的 CPU 滴答計數。 請注意，這個值可能溢位。

**Windows Vista、Windows Server 2003 SP1、Windows Server 2003、Windows 2000 Server 和 Windows 2000 Professional：** 屬性的名稱是 **ResponseTime**，其中包含從作業開始到作業結束的 CPU 滴答計數。 請注意，這個值可能溢位。

</dd> <dt>

**TransferSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) 
</dt> </dl>

從磁片讀取或寫入的資料大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

Windows伺服器2003針對 **DiskIo \_ TypeGroup1** 事件種類類別使用下列定義。

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

**ResponseTime** 屬性包含從作業開始到作業結束的 CPU 滴答計數。 請注意，這個值可能溢位。

不支援 **HighResResponseTime** 屬性。

WindowsServer 2003 SP1 和 Windows Vista 針對 **DiskIo \_ TypeGroup1** 事件種類類別使用下列定義。

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

**Irp** 屬性是 i/o 要求封包。 這個屬性會識別 i/o 活動。 您可以使用這個屬性搭配 [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) 事件，將回應時間相互關聯。

支援 **HighResResponseTime** 屬性。 屬性包含 i/o 初始和完成之間的時間，以 KeQueryPerformanceCounter 單位) 的 PartitionManager (來測量。 使用這個屬性來取代 **ResponseTime** 屬性，以判斷磁片 i/o 回應時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 

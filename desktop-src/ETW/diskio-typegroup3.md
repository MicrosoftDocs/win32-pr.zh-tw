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
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971945"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="d5d23-104">DiskIo \_ TypeGroup3 類別</span><span class="sxs-lookup"><span data-stu-id="d5d23-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="d5d23-105">這個類別是磁片 i/o flush 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="d5d23-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="d5d23-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="d5d23-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d23-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5d23-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="d5d23-108">成員</span><span class="sxs-lookup"><span data-stu-id="d5d23-108">Members</span></span>

<span data-ttu-id="d5d23-109">**DiskIo \_ TypeGroup3** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5d23-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="d5d23-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d5d23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5d23-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d5d23-111">Properties</span></span>

<span data-ttu-id="d5d23-112">**DiskIo \_ TypeGroup3** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d5d23-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5d23-113">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="d5d23-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d23-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d5d23-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d23-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-116">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="d5d23-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d5d23-117">識別實體磁片的編號。</span><span class="sxs-lookup"><span data-stu-id="d5d23-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="d5d23-118">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="d5d23-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d23-119">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d5d23-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d23-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-121">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="d5d23-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="d5d23-122">從作業開始到作業結束的 CPU 滴答計數。</span><span class="sxs-lookup"><span data-stu-id="d5d23-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d5d23-123">**Irp**</span><span class="sxs-lookup"><span data-stu-id="d5d23-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d23-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d5d23-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d23-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-126">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) ， [**指標**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d5d23-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d5d23-127">I/o 要求封包。</span><span class="sxs-lookup"><span data-stu-id="d5d23-127">I/O request packet.</span></span> <span data-ttu-id="d5d23-128">這個屬性會識別 i/o 活動。</span><span class="sxs-lookup"><span data-stu-id="d5d23-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="d5d23-129">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="d5d23-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d23-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d5d23-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d23-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-132">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) ， [**格式**](event-tracing-mof-qualifiers.md) ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="d5d23-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="d5d23-133">可以包含下列一或多個 (在 Ntddk 中定義的 i/o 要求封包旗標，這是) 的 DDK 標頭檔：</span><span class="sxs-lookup"><span data-stu-id="d5d23-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="d5d23-134">**IRP \_ NOCACHE**</span><span class="sxs-lookup"><span data-stu-id="d5d23-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="d5d23-135">**IRP \_ 分頁 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="d5d23-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="d5d23-136">**IRP \_ 掛接 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="d5d23-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="d5d23-137">**IRP \_ 同步 \_ API**</span><span class="sxs-lookup"><span data-stu-id="d5d23-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="d5d23-138">**IRP \_ 相關聯的 \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="d5d23-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="d5d23-139">**IRP \_ 緩衝 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="d5d23-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="d5d23-140">**IRP \_ 解除配置 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="d5d23-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="d5d23-141">**IRP \_ 輸入 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="d5d23-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="d5d23-142">**IRP \_ 同步 \_ 分頁 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="d5d23-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="d5d23-143">**IRP \_ 建立 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="d5d23-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="d5d23-144">**IRP \_ 讀取 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="d5d23-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="d5d23-145">**IRP \_ 寫入 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="d5d23-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="d5d23-146">**IRP \_ 關閉 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="d5d23-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="d5d23-147">**IRP \_ 延遲 \_ IO \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="d5d23-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d5d23-148">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="d5d23-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5d23-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d5d23-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d5d23-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5d23-151">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) </span><span class="sxs-lookup"><span data-stu-id="d5d23-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="d5d23-152">發行執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5d23-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="d5d23-153">**Windows server 2008 R2、Windows server 2008、windows 7 和 Windows Vista：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d5d23-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d23-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d23-154">Requirements</span></span>



| <span data-ttu-id="d5d23-155">需求</span><span class="sxs-lookup"><span data-stu-id="d5d23-155">Requirement</span></span> | <span data-ttu-id="d5d23-156">值</span><span class="sxs-lookup"><span data-stu-id="d5d23-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5d23-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5d23-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d23-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5d23-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5d23-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5d23-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d23-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5d23-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5d23-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5d23-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d23-162">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="d5d23-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 





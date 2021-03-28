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
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511905"
---
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="4f0f8-104">DiskIo \_ TypeGroup1 類別</span><span class="sxs-lookup"><span data-stu-id="4f0f8-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="4f0f8-105">這個類別是磁片 i/o 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="4f0f8-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0f8-107">語法</span><span class="sxs-lookup"><span data-stu-id="4f0f8-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4f0f8-108">成員</span><span class="sxs-lookup"><span data-stu-id="4f0f8-108">Members</span></span>

<span data-ttu-id="4f0f8-109">**DiskIo \_ TypeGroup1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f0f8-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4f0f8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4f0f8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f0f8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4f0f8-111">Properties</span></span>

<span data-ttu-id="4f0f8-112">**DiskIo \_ TypeGroup1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f0f8-113">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-114">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-116">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (5) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-117">從實體磁片開頭的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-118">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-119">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-121">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (1) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-122">識別實體磁片的編號。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-126">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (6) ， [**指標**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4f0f8-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-127">將 this 指標的值與 [**FileIo \_ Name**](fileio-name.md)事件中的 **FileObject** 指標值比對，以判斷與 i/o 作業相關的檔案。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-128">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-131">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (8) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-132">[**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter)滴答單位) 中，資料分割管理員 (所測量的 i/o 初始和完成之間的時間。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="4f0f8-133">**Windows Server 2003：** 這個屬性的 [**WmiDataId**](event-tracing-mof-qualifiers.md) 值為7。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="4f0f8-134">**Windows 2000 Server 和 windows 2000 Professional：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-135">**Irp**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-136">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-138">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (7) ， [**指標**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="4f0f8-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-139">用來識別 i/o 活動的 i/o 要求封包。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="4f0f8-140">**Windows Server 2003、windows 2000 伺服器和 windows 2000 Professional：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-141">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-144">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (2) ， [**格式**](event-tracing-mof-qualifiers.md) ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-145">可以包含下列一或多個 (在 Ntddk 中定義的 i/o 要求封包旗標，這是) 的 DDK 標頭檔：</span><span class="sxs-lookup"><span data-stu-id="4f0f8-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="4f0f8-146">**IRP \_ NOCACHE**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="4f0f8-147">**IRP \_ 分頁 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="4f0f8-148">**IRP \_ 掛接 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="4f0f8-149">**IRP \_ 同步 \_ API**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="4f0f8-150">**IRP \_ 相關聯的 \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="4f0f8-151">**IRP \_ 緩衝 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="4f0f8-152">**IRP \_ 解除配置 \_ 緩衝區**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="4f0f8-153">**IRP \_ 輸入 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="4f0f8-154">**IRP \_ 同步 \_ 分頁 \_ IO**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="4f0f8-155">**IRP \_ 建立 \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="4f0f8-156">**IRP \_ 讀取 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="4f0f8-157">**IRP \_ 寫入 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="4f0f8-158">**IRP \_ 關閉 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="4f0f8-159">**IRP \_ 延遲 \_ IO \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4f0f8-160">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-161">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-163">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (9) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-164">發行執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="4f0f8-165">**Windows server 2008 R2、Windows server 2008、windows 7、Windows Vista、Windows server 2003 SP1、Windows Server 2003、windows 2000 Server 及 Windows 2000 Professional：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-166">**已保留**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-169">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (4) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-170">保留的。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-170">Reserved.</span></span>

<span data-ttu-id="4f0f8-171">**Windows server 2008 R2、Windows server 2008 和 windows 7：** 屬性的名稱是 **[queuedepth**，其中包含從作業開始到作業結束的 CPU 滴答計數。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4f0f8-172">請注意，這個值可能溢位。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-172">Note that this value can overflow.</span></span>

<span data-ttu-id="4f0f8-173">**Windows Vista、Windows server 2003 （含 SP1）、Windows server 2003、windows 2000 Server 及 windows 2000 Professional：** 屬性的名稱是 **ResponseTime**，其中包含從作業開始到作業結束的 CPU 滴答計數。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4f0f8-174">請注意，這個值可能溢位。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="4f0f8-175">**TransferSize**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f0f8-176">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4f0f8-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f0f8-178">限定詞： [**WmiDataId**](event-tracing-mof-qualifiers.md) (3) </span><span class="sxs-lookup"><span data-stu-id="4f0f8-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="4f0f8-179">從磁片讀取或寫入的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f0f8-180">備註</span><span class="sxs-lookup"><span data-stu-id="4f0f8-180">Remarks</span></span>

<span data-ttu-id="4f0f8-181">Windows Server 2003 使用 **DiskIo \_ TypeGroup1** 事件種類類別的下列定義。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="4f0f8-182">**ResponseTime** 屬性包含從作業開始到作業結束的 CPU 滴答計數。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="4f0f8-183">請注意，這個值可能溢位。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-183">Note that this value can overflow.</span></span>

<span data-ttu-id="4f0f8-184">不支援 **HighResResponseTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="4f0f8-185">Windows Server 2003 SP1 和 Windows Vista 針對 **DiskIo \_ TypeGroup1** 事件種類類別使用下列定義。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

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

<span data-ttu-id="4f0f8-186">**Irp** 屬性是 i/o 要求封包。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="4f0f8-187">這個屬性會識別 i/o 活動。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="4f0f8-188">您可以使用這個屬性搭配 [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) 事件，將回應時間相互關聯。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="4f0f8-189">支援 **HighResResponseTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="4f0f8-190">屬性包含 i/o 初始和完成之間的時間，以 KeQueryPerformanceCounter 單位) 的 PartitionManager (來測量。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="4f0f8-191">使用這個屬性來取代 **ResponseTime** 屬性，以判斷磁片 i/o 回應時間。</span><span class="sxs-lookup"><span data-stu-id="4f0f8-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0f8-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f0f8-192">Requirements</span></span>



| <span data-ttu-id="4f0f8-193">需求</span><span class="sxs-lookup"><span data-stu-id="4f0f8-193">Requirement</span></span> | <span data-ttu-id="4f0f8-194">值</span><span class="sxs-lookup"><span data-stu-id="4f0f8-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f0f8-195">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f0f8-195">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0f8-196">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f0f8-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f0f8-197">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f0f8-197">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0f8-198">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f0f8-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f0f8-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f0f8-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0f8-200">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="4f0f8-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 

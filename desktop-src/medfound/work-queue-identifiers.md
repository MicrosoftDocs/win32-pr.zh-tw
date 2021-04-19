---
description: 下列常數會識別標準媒體基礎工作佇列。
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: '工作佇列識別碼 (Mfobjects .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977947"
---
# <a name="work-queue-identifiers"></a><span data-ttu-id="9b81c-103">工作佇列識別碼</span><span class="sxs-lookup"><span data-stu-id="9b81c-103">Work Queue Identifiers</span></span>

<span data-ttu-id="9b81c-104">下列常數會識別標準媒體基礎工作佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-104">The following constants identify the standard Media Foundation work queues.</span></span>

<span data-ttu-id="9b81c-105">應用程式應該使用 MFASYNC \_ 回呼 \_ 佇列 \_ 多執行緒，或使用從 [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) 取得的工作佇列（如果他們想要控制執行優先權）。</span><span class="sxs-lookup"><span data-stu-id="9b81c-105">Applications should use MFASYNC\_CALLBACK\_QUEUE\_MULTITHREADED or use a work queue obtained from [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) if they want to control the execution priority.</span></span> <span data-ttu-id="9b81c-106">請注意，當應用程式呼叫 [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)時，預設的平臺工作佇列優先順序可能會動態變更。</span><span class="sxs-lookup"><span data-stu-id="9b81c-106">Note that the default platform work queue priorities can dynamically change when an application calls [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss).</span></span> <span data-ttu-id="9b81c-107">如需工作佇列的詳細資訊，請參閱 [工作佇列](work-queues.md)。</span><span class="sxs-lookup"><span data-stu-id="9b81c-107">For more information about work queues, see [Work Queues](work-queues.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9b81c-108">常數/值</span><span class="sxs-lookup"><span data-stu-id="9b81c-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9b81c-109">Description</span><span class="sxs-lookup"><span data-stu-id="9b81c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <span data-ttu-id="9b81c-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-110"><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-111">在大多數情況下，應用程式應該使用 <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>。</span><span class="sxs-lookup"><span data-stu-id="9b81c-111">In most cases, applications should use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/> <span data-ttu-id="9b81c-112">此工作佇列用於同步作業。</span><span class="sxs-lookup"><span data-stu-id="9b81c-112">This work queue is used for synchronous operations.</span></span> <span data-ttu-id="9b81c-113">使用標準工作佇列可能會造成死結的風險。</span><span class="sxs-lookup"><span data-stu-id="9b81c-113">Using the standard work queue may run the risk of deadlocking.</span></span> <span data-ttu-id="9b81c-114">應用程式可以使用 <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>，在多執行緒佇列之上建立私用同步佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-114">Applications can create a private synchronous queue on top of the multithreaded queue by using <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <span data-ttu-id="9b81c-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-115"><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-116">不適用於一般應用程式的使用。</span><span class="sxs-lookup"><span data-stu-id="9b81c-116">Not for general application use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <span data-ttu-id="9b81c-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-117"><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-118">不適用於一般應用程式的使用。</span><span class="sxs-lookup"><span data-stu-id="9b81c-118">Not for general application use.</span></span><br/> <span data-ttu-id="9b81c-119">此工作佇列會在內部使用，以進行 i/o 作業，例如讀取檔案並從網路讀取。</span><span class="sxs-lookup"><span data-stu-id="9b81c-119">This work queue is used internally for I/O operations such as reading files and reading from the network.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <span data-ttu-id="9b81c-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-120"><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-121">不適用於一般應用程式的使用。</span><span class="sxs-lookup"><span data-stu-id="9b81c-121">Not for general application use.</span></span><br/> <span data-ttu-id="9b81c-122">此工作佇列用於定期回呼和已排程的工作專案。</span><span class="sxs-lookup"><span data-stu-id="9b81c-122">This work queue is used for periodic callbacks and scheduled work items.</span></span> <span data-ttu-id="9b81c-123">下列函式會在此佇列中放置工作專案：</span><span class="sxs-lookup"><span data-stu-id="9b81c-123">The following functions put work items in this queue:</span></span><br/>
<ul>
<li><span data-ttu-id="9b81c-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="9b81c-124"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></span></span></li>
<li><span data-ttu-id="9b81c-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="9b81c-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></span></span></li>
<li><span data-ttu-id="9b81c-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="9b81c-126"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <span data-ttu-id="9b81c-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-127"><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-128">在大部分情況下，都應該使用此多執行緒工作佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-128">This multithreaded work queue should be used in most cases.</span></span> <br/> <span data-ttu-id="9b81c-129">此工作佇列用於媒體基礎中的非同步作業。</span><span class="sxs-lookup"><span data-stu-id="9b81c-129">This work queue is used for asynchronous operations throughout Media Foundation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <span data-ttu-id="9b81c-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span><span class="sxs-lookup"><span data-stu-id="9b81c-130"><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9b81c-131">不適用於一般應用程式的使用。</span><span class="sxs-lookup"><span data-stu-id="9b81c-131">Not for general application use.</span></span> <span data-ttu-id="9b81c-132">應用程式應該改為使用 <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>。</span><span class="sxs-lookup"><span data-stu-id="9b81c-132">Applications should instead use <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="9b81c-133">此外，與工作佇列的連接中會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="9b81c-133">In addition, the following constants are used in connection with work queues.</span></span>



| <span data-ttu-id="9b81c-134">常數/值</span><span class="sxs-lookup"><span data-stu-id="9b81c-134">Constant/value</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="9b81c-135">Description</span><span class="sxs-lookup"><span data-stu-id="9b81c-135">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <span data-ttu-id="9b81c-136"><dt>**MFASYNC \_回呼 \_ 佇列 \_ 未定義**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="9b81c-136"><dt>**MFASYNC\_CALLBACK\_QUEUE\_UNDEFINED**</dt> <dt>0x00000000</dt></span></span> </dl>           | <span data-ttu-id="9b81c-137">未定義的工作佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-137">Undefined work queue.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <span data-ttu-id="9b81c-138"><dt>**MFASYNC \_回呼 \_ 佇列 \_ 私用 \_ 遮罩**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="9b81c-138"><dt>**MFASYNC\_CALLBACK\_QUEUE\_PRIVATE\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl> | <span data-ttu-id="9b81c-139">位元遮罩，可區分平臺工作佇列與透過呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)所建立的佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-139">Bit mask to distinguish platform work queues from those created by calling [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span><br/> <span data-ttu-id="9b81c-140">針對 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)所建立的工作佇列，下列值為非零值：</span><span class="sxs-lookup"><span data-stu-id="9b81c-140">For a work queue created by [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), the following value is nonzero:</span></span><br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <span data-ttu-id="9b81c-141"><dt>**MFASYNC \_回呼 \_ 佇列 \_ 所有**</dt> <dt>0xffffffff</dt></span><span class="sxs-lookup"><span data-stu-id="9b81c-141"><dt>**MFASYNC\_CALLBACK\_QUEUE\_ALL**</dt> <dt>0xFFFFFFFF</dt></span></span> </dl>                             | <span data-ttu-id="9b81c-142">所有平臺的工作佇列。</span><span class="sxs-lookup"><span data-stu-id="9b81c-142">All platform work queues.</span></span><br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="9b81c-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b81c-143">Requirements</span></span>



| <span data-ttu-id="9b81c-144">需求</span><span class="sxs-lookup"><span data-stu-id="9b81c-144">Requirement</span></span> | <span data-ttu-id="9b81c-145">值</span><span class="sxs-lookup"><span data-stu-id="9b81c-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b81c-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b81c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9b81c-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b81c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9b81c-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b81c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9b81c-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b81c-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b81c-150">標頭</span><span class="sxs-lookup"><span data-stu-id="9b81c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b81c-151"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="9b81c-151"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b81c-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b81c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b81c-153">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="9b81c-153">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> <dt>

[<span data-ttu-id="9b81c-154">工作佇列</span><span class="sxs-lookup"><span data-stu-id="9b81c-154">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="9b81c-155">工作佇列和執行緒改進</span><span class="sxs-lookup"><span data-stu-id="9b81c-155">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 





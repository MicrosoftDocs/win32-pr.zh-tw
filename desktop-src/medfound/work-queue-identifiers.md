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
# <a name="work-queue-identifiers"></a>工作佇列識別碼

下列常數會識別標準媒體基礎工作佇列。

應用程式應該使用 MFASYNC \_ 回呼 \_ 佇列 \_ 多執行緒，或使用從 [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) 取得的工作佇列（如果他們想要控制執行優先權）。 請注意，當應用程式呼叫 [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)時，預設的平臺工作佇列優先順序可能會動態變更。 如需工作佇列的詳細資訊，請參閱 [工作佇列](work-queues.md)。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數/值</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">在大多數情況下，應用程式應該使用 <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>。<br/> 此工作佇列用於同步作業。 使用標準工作佇列可能會造成死結的風險。 應用程式可以使用 <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>，在多執行緒佇列之上建立私用同步佇列。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">不適用於一般應用程式的使用。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </dl></td>
<td style="text-align: left;">不適用於一般應用程式的使用。<br/> 此工作佇列會在內部使用，以進行 i/o 作業，例如讀取檔案並從網路讀取。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">不適用於一般應用程式的使用。<br/> 此工作佇列用於定期回呼和已排程的工作專案。 下列函式會在此佇列中放置工作專案：<br/>
<ul>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </dl></td>
<td style="text-align: left;">在大部分情況下，都應該使用此多執行緒工作佇列。 <br/> 此工作佇列用於媒體基礎中的非同步作業。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </dl></td>
<td style="text-align: left;">不適用於一般應用程式的使用。 應用程式應該改為使用 <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>。<br/></td>
</tr>
</tbody>
</table>



此外，與工作佇列的連接中會使用下列常數。



| 常數/值                                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_回呼 \_ 佇列 \_ 未定義**</dt> <dt>0x00000000</dt> </dl>           | 未定義的工作佇列。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_回呼 \_ 佇列 \_ 私用 \_ 遮罩**</dt> <dt>0xFFFF0000</dt> </dl> | 位元遮罩，可區分平臺工作佇列與透過呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)所建立的佇列。<br/> 針對 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)所建立的工作佇列，下列值為非零值：<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_回呼 \_ 佇列 \_ 所有**</dt> <dt>0xffffffff</dt> </dl>                             | 所有平臺的工作佇列。<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> <dt>

[工作佇列](work-queues.md)
</dt> <dt>

[工作佇列和執行緒改進](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 





---
title: 使用視窗或執行緒管理緩衝播放
description: 使用視窗或執行緒管理緩衝播放
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- 音樂檢測數位介面 (MIDI) 、緩衝播放
- MIDI (的音樂檢測數位介面) ，經過緩衝的播放
- 播放 MIDI 檔案，緩衝播放
- 緩衝播放
- MM_MOM_CLOSE 訊息
- MM_MOM_DONE 訊息
- MM_MOM_OPEN 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315013"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a><span data-ttu-id="2fea8-114">使用視窗或執行緒管理緩衝播放</span><span class="sxs-lookup"><span data-stu-id="2fea8-114">Using a Window or Thread to Manage Buffered Playback</span></span>

<span data-ttu-id="2fea8-115">下列訊息可傳送至視窗或執行緒，以管理 MIDI 系統專屬訊息或串流緩衝區的播放。</span><span class="sxs-lookup"><span data-stu-id="2fea8-115">The following messages can be sent to a window or thread for managing playback of MIDI system-exclusive messages or stream buffers.</span></span>



| <span data-ttu-id="2fea8-116">值</span><span class="sxs-lookup"><span data-stu-id="2fea8-116">Value</span></span>                                  | <span data-ttu-id="2fea8-117">意義</span><span class="sxs-lookup"><span data-stu-id="2fea8-117">Meaning</span></span>                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fea8-118">**MM \_ MOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="2fea8-118">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md) | <span data-ttu-id="2fea8-119">在使用 [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) 函式關閉裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="2fea8-119">Sent when the device is closed by using the [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) function.</span></span>                                                                               |
| [<span data-ttu-id="2fea8-120">**MM \_ MOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="2fea8-120">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)   | <span data-ttu-id="2fea8-121">當設備磁碟機使用 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 或 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函數傳送的資料區塊完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="2fea8-121">Sent when the device driver is finished with a data block sent by using the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) or [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function.</span></span> |
| [<span data-ttu-id="2fea8-122">**分鐘 \_ MOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="2fea8-122">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)   | <span data-ttu-id="2fea8-123">在使用 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函式開啟裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="2fea8-123">Sent when the device is opened by using the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function.</span></span>                                                                                 |



 

<span data-ttu-id="2fea8-124">*WParam* 參數和 *lParam* 參數會與這些訊息相關聯。</span><span class="sxs-lookup"><span data-stu-id="2fea8-124">A *wParam* parameter and an *lParam* parameter are associated with each of these messages.</span></span> <span data-ttu-id="2fea8-125">*WParam* 參數一律會指定開啟之 MIDI 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2fea8-125">The *wParam* parameter always specifies the handle of an open MIDI device.</span></span> <span data-ttu-id="2fea8-126">若是 [**\_ MOM \_ 完成**](mm-mom-done.md)， *lParam* 會指定識別已完成資料區塊之 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="2fea8-126">For [**MM\_MOM\_DONE**](mm-mom-done.md), *lParam* specifies an address of a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the completed data block.</span></span> <span data-ttu-id="2fea8-127">*LParam* 參數未用於 [**mm \_ mom \_ CLOSE**](mm-mom-close.md)和 [**mm \_ \_ OPEN**](mm-mom-open.md)。</span><span class="sxs-lookup"><span data-stu-id="2fea8-127">The *lParam* parameter is unused for [**MM\_MOM\_CLOSE**](mm-mom-close.md) and [**MM\_MOM\_OPEN**](mm-mom-open.md).</span></span>

<span data-ttu-id="2fea8-128">最有用的訊息可能是 \_ MOM \_ 完成。</span><span class="sxs-lookup"><span data-stu-id="2fea8-128">The most useful message is probably MM\_MOM\_DONE.</span></span> <span data-ttu-id="2fea8-129">除非您需要配置記憶體或初始化變數，否則您可能不需要處理 MM \_ mom \_ OPEN 和 mm \_ mom \_ CLOSE。</span><span class="sxs-lookup"><span data-stu-id="2fea8-129">Unless you need to allocate memory or initialize variables, you probably do not need to process MM\_MOM\_OPEN and MM\_MOM\_CLOSE.</span></span> <span data-ttu-id="2fea8-130">當資料區塊的播放完成時，您可以清除並釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="2fea8-130">When playback of a data block is complete, you can clean up and free the data block.</span></span>

 

 
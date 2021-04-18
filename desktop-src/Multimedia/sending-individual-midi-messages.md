---
title: 傳送個別的 MIDI 訊息
description: 傳送個別的 MIDI 訊息
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、個別訊息
- MIDI (音樂檢測數位介面) 、個別訊息
- 播放 MIDI 檔案，個別訊息
- 個別的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965423"
---
# <a name="sending-individual-midi-messages"></a><span data-ttu-id="8c167-111">傳送個別的 MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="8c167-111">Sending Individual MIDI Messages</span></span>

<span data-ttu-id="8c167-112">您可以使用下列功能來處理個別的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c167-112">You can work with individual MIDI messages by using the following functions.</span></span>



| <span data-ttu-id="8c167-113">值</span><span class="sxs-lookup"><span data-stu-id="8c167-113">Value</span></span>                                      | <span data-ttu-id="8c167-114">意義</span><span class="sxs-lookup"><span data-stu-id="8c167-114">Meaning</span></span>                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c167-115">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="8c167-115">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | <span data-ttu-id="8c167-116">將 MIDI 資料的緩衝區傳送至指定的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="8c167-116">Sends a buffer of MIDI data to the specified MIDI output device.</span></span> <span data-ttu-id="8c167-117">使用此函式可將系統專屬訊息傳送至 MIDI 裝置。</span><span class="sxs-lookup"><span data-stu-id="8c167-117">Use this function to send system-exclusive messages to a MIDI device.</span></span>                                              |
| [<span data-ttu-id="8c167-118">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="8c167-118">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | <span data-ttu-id="8c167-119">針對指定的 MIDI 輸出裝置，關閉所有通道上的所有附注。</span><span class="sxs-lookup"><span data-stu-id="8c167-119">Turns off all notes on all channels for a specified MIDI output device.</span></span> <span data-ttu-id="8c167-120">任何擱置中的系統專屬緩衝區和資料流程緩衝區都會標示為已完成，並傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c167-120">Any pending system-exclusive buffers and stream buffers are marked as done and returned to the application.</span></span> |
| [<span data-ttu-id="8c167-121">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="8c167-121">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | <span data-ttu-id="8c167-122">將 MIDI 訊息傳送至指定的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="8c167-122">Sends a MIDI message to a specified MIDI output device.</span></span>                                                                                                                             |



 

<span data-ttu-id="8c167-123">若要傳送任何 MIDI 訊息 (除了系統專屬的訊息) 之外，請使用 [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)。</span><span class="sxs-lookup"><span data-stu-id="8c167-123">To send any MIDI message (except for system-exclusive messages), use [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).</span></span>

 

 
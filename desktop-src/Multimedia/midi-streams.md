---
title: MIDI 串流
description: MIDI 串流
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- 音樂檢測數位介面 (MIDI) 、串流
- MIDI (音樂檢測數位介面) 、串流
- 串流緩衝區，MIDI 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092709"
---
# <a name="midi-streams"></a><span data-ttu-id="0d4eb-106">MIDI 串流</span><span class="sxs-lookup"><span data-stu-id="0d4eb-106">MIDI Streams</span></span>

<span data-ttu-id="0d4eb-107">Midi 事件會發生在 MIDI 資料串流的內容中。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="0d4eb-108">雖然應用程式可以使用數個數據流來定義音樂資料，但 MIDI 對應工具無法辨識多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="0d4eb-109">大部分使用串流的應用程式都使用單一的 MIDI 串流。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="0d4eb-110">下列函式可用於資料流程。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-110">The following functions work with streams.</span></span>



| <span data-ttu-id="0d4eb-111">值</span><span class="sxs-lookup"><span data-stu-id="0d4eb-111">Value</span></span>                                            | <span data-ttu-id="0d4eb-112">意義</span><span class="sxs-lookup"><span data-stu-id="0d4eb-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="0d4eb-113">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="0d4eb-114">關閉 MIDI 串流。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="0d4eb-115">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="0d4eb-116">開啟 MIDI 資料流程並抓取控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="0d4eb-117">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="0d4eb-118">將 MIDI 資料的串流 (緩衝區) 播放或佇列至 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="0d4eb-119">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="0d4eb-120">暫停指定之 MIDI 串流的播放。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="0d4eb-121">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="0d4eb-122">抓取 MIDI 串流中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="0d4eb-123">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="0d4eb-124">設定和捕獲資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="0d4eb-125">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="0d4eb-126">重新開機已暫停之 MIDI 串流的播放。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="0d4eb-127">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="0d4eb-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="0d4eb-128">針對指定的 MIDI 串流，關閉所有 MIDI 通道上的所有便箋。</span><span class="sxs-lookup"><span data-stu-id="0d4eb-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 
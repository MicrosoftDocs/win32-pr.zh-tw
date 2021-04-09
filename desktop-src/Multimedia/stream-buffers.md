---
title: 資料流程緩衝區
description: 資料流程緩衝區
ms.assetid: d73209a3-4b9d-4405-9e62-8ecfb94c0bd5
keywords:
- Windows 多媒體，資料流程緩衝區
- 多媒體、串流緩衝區
- 多媒體音訊、串流緩衝區
- 音訊、串流緩衝區
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 串流緩衝區，關於
- MIDIHDR 結構
- MIDIEVENT 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a01862a8a8e6b7846cbe445737bd13422cf0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681870"
---
# <a name="stream-buffers"></a><span data-ttu-id="f0f50-112">資料流程緩衝區</span><span class="sxs-lookup"><span data-stu-id="f0f50-112">Stream Buffers</span></span>

<span data-ttu-id="f0f50-113">應用程式可以使用串流緩衝區將 MIDI 事件的串流傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="f0f50-113">Applications can use stream buffers to send streams of MIDI events to a device.</span></span> <span data-ttu-id="f0f50-114">每個資料流程緩衝區都是 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構所指向的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="f0f50-114">Each stream buffer is a block of memory pointed to by a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span> <span data-ttu-id="f0f50-115">這個記憶體區塊包含一或多個 MIDI 事件的資料，每個事件都是由 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構所定義。</span><span class="sxs-lookup"><span data-stu-id="f0f50-115">This block of memory contains data for one or more MIDI events, each of which is defined by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="f0f50-116">應用程式會藉由呼叫資料流程操作函式（例如 [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)、 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)和 [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)）來控制緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f0f50-116">An application controls the buffer by calling the stream-manipulation functions, such as [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen), [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout), and [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose).</span></span>

-   [<span data-ttu-id="f0f50-117">資料流程緩衝區格式</span><span class="sxs-lookup"><span data-stu-id="f0f50-117">Stream Buffer Format</span></span>](stream-buffer-format.md)
-   [<span data-ttu-id="f0f50-118">計時資訊</span><span class="sxs-lookup"><span data-stu-id="f0f50-118">Timing Information</span></span>](timing-information.md)
-   [<span data-ttu-id="f0f50-119">MIDI 事件種類</span><span class="sxs-lookup"><span data-stu-id="f0f50-119">MIDI Event Types</span></span>](midi-event-types.md)
-   [<span data-ttu-id="f0f50-120">MIDI 串流</span><span class="sxs-lookup"><span data-stu-id="f0f50-120">MIDI Streams</span></span>](midi-streams.md)

 

 
---
title: 使用資料流程緩衝區傳送 MIDI 訊息
description: 使用資料流程緩衝區傳送 MIDI 訊息
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 播放 MIDI 檔案，資料流程緩衝區
- 串流緩衝區，傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681872"
---
# <a name="sending-midi-messages-with-stream-buffers"></a><span data-ttu-id="8b929-111">使用資料流程緩衝區傳送 MIDI 訊息</span><span class="sxs-lookup"><span data-stu-id="8b929-111">Sending MIDI Messages with Stream Buffers</span></span>

<span data-ttu-id="8b929-112">當您的應用程式搭配串流緩衝區使用時，它會使用 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) 函式將所有 (短和長) 的 MIDI 訊息傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="8b929-112">When your application works with stream buffers, it uses the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function to send all (short and long) MIDI messages to the device.</span></span> <span data-ttu-id="8b929-113">若要指定資料流程資料區塊，請使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 和 [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b929-113">To specify stream data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) and [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structures.</span></span> <span data-ttu-id="8b929-114">**MIDIHDR** 結構包含鎖定資料區塊的位址、資料區塊長度，以及一些各式各樣的旗標。</span><span class="sxs-lookup"><span data-stu-id="8b929-114">The **MIDIHDR** structure contains an address of a locked data block, the data-block length, and some assorted flags.</span></span> <span data-ttu-id="8b929-115">資料會以 **MIDIEVENT** 結構的形式儲存。</span><span class="sxs-lookup"><span data-stu-id="8b929-115">The data is stored in the form of **MIDIEVENT** structures.</span></span> <span data-ttu-id="8b929-116">系統會在資料流程緩衝區上強加64的大小限制。</span><span class="sxs-lookup"><span data-stu-id="8b929-116">The system imposes a size limit of 64K on stream buffers.</span></span>

<span data-ttu-id="8b929-117">使用 **midiStreamOut** 傳送資料的資料流程緩衝區之後，您必須等到設備磁碟機完成後再釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="8b929-117">After you use **midiStreamOut** to send a stream buffer of data, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="8b929-118">如果您要傳送多個資料區塊，您必須監視每個資料區塊的完成，讓您知道何時傳送其他區塊。</span><span class="sxs-lookup"><span data-stu-id="8b929-118">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="8b929-119">如需有關監視資料區塊完成的不同技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="8b929-119">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

 

 
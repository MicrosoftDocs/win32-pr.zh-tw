---
title: 傳送 System-Exclusive 訊息
description: 傳送 System-Exclusive 訊息
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- 音樂檢測數位介面 (MIDI) ，傳送訊息
- MIDI (的音樂檢測數位介面) ，傳送訊息
- 播放 MIDI 檔案，傳送訊息
- 傳送 MIDI 訊息
- 音樂檢測數位介面 (MIDI) 、系統專屬的訊息
- MIDI (的音樂檢測數位介面) 、系統專屬的訊息
- 播放 MIDI 檔案，系統專屬訊息
- 系統專屬的 MIDI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842119"
---
# <a name="sending-system-exclusive-messages"></a><span data-ttu-id="bc70d-111">傳送 System-Exclusive 訊息</span><span class="sxs-lookup"><span data-stu-id="bc70d-111">Sending System-Exclusive Messages</span></span>

<span data-ttu-id="bc70d-112">MIDI 系統專屬訊息是唯一不符合單一雙全半值的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="bc70d-112">MIDI system-exclusive messages are the only MIDI messages that will not fit into a single doubleword value.</span></span> <span data-ttu-id="bc70d-113">系統專屬訊息可以是任何長度。</span><span class="sxs-lookup"><span data-stu-id="bc70d-113">System-exclusive messages can be any length.</span></span> <span data-ttu-id="bc70d-114">Windows 提供 [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) 函式，可將系統專屬訊息傳送至 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="bc70d-114">Windows provides the [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) function for sending system-exclusive messages to MIDI output devices.</span></span> <span data-ttu-id="bc70d-115">若要指定 MIDI 系統專屬資料區塊，請使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構。</span><span class="sxs-lookup"><span data-stu-id="bc70d-115">To specify MIDI system-exclusive data blocks, use the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

<span data-ttu-id="bc70d-116">使用 **midiOutLongMsg** 傳送系統專屬的資料區塊之後，您必須等到設備磁碟機使用資料區塊完成後再釋放它。</span><span class="sxs-lookup"><span data-stu-id="bc70d-116">After you send a system-exclusive data block using **midiOutLongMsg**, you must wait until the device driver is finished with the data block before freeing it.</span></span> <span data-ttu-id="bc70d-117">如果您要傳送多個資料區塊，您必須監視每個資料區塊的完成，讓您知道何時傳送其他區塊。</span><span class="sxs-lookup"><span data-stu-id="bc70d-117">If you are sending multiple data blocks, you must monitor the completion of each data block so you know when to send additional blocks.</span></span> <span data-ttu-id="bc70d-118">如需有關監視資料區塊完成的不同技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="bc70d-118">For information about different techniques for monitoring data-block completion, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

> [!Note]  
> <span data-ttu-id="bc70d-119">系統即時訊息以外的任何 MIDI 狀態位元組都將終止系統專屬的訊息。</span><span class="sxs-lookup"><span data-stu-id="bc70d-119">Any MIDI status byte other than a system-real-time message will terminate a system-exclusive message.</span></span> <span data-ttu-id="bc70d-120">如果您使用多個資料區塊來傳送單一系統專屬的訊息，請勿在資料區塊之間傳送系統即時訊息以外的任何 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="bc70d-120">If you are using multiple data blocks to send a single system-exclusive message, do not send any MIDI messages other than system-real-time messages between data blocks.</span></span>

 

 

 
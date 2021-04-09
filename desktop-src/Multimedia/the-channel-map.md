---
title: 通道對應
description: 通道對應
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應工具，通道對應
- 通道對應
- MIDI 對應程式，通道訊息
- MIDI 通道訊息
- 通道訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092288"
---
# <a name="the-channel-map"></a><span data-ttu-id="892cb-110">通道對應</span><span class="sxs-lookup"><span data-stu-id="892cb-110">The Channel Map</span></span>

<span data-ttu-id="892cb-111">通道對應會影響所有的 MIDI 通道訊息。</span><span class="sxs-lookup"><span data-stu-id="892cb-111">The channel map affects all MIDI channel messages.</span></span> <span data-ttu-id="892cb-112">MIDI 通道訊息包括注意事項、注意事項、polyphonic-按鍵 aftertouch、控制項變更、程式變更、通道 aftertouch 和音調彎曲變更訊息。</span><span class="sxs-lookup"><span data-stu-id="892cb-112">MIDI channel messages include note-on, note-off, polyphonic-key-aftertouch, control-change, program-change, channel-aftertouch, and pitch-bend-change messages.</span></span> <span data-ttu-id="892cb-113">MIDI 對應工具使用單一通道對應，其中每個16個 MIDI 通道都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="892cb-113">The MIDI Mapper uses a single channel map with an entry for each of the 16 MIDI channels.</span></span> <span data-ttu-id="892cb-114">每個通道對應專案都會指定下列專案：</span><span class="sxs-lookup"><span data-stu-id="892cb-114">Each channel-map entry specifies the following:</span></span>

-   <span data-ttu-id="892cb-115">MIDI 訊息的目的地通道</span><span class="sxs-lookup"><span data-stu-id="892cb-115">A destination channel for the MIDI message</span></span>
-   <span data-ttu-id="892cb-116">適用于 MIDI 訊息的目的地輸出裝置</span><span class="sxs-lookup"><span data-stu-id="892cb-116">A destination output device for the MIDI message</span></span>
-   <span data-ttu-id="892cb-117">選用的 patch map，可指定其他可能的 MIDI 訊息修改</span><span class="sxs-lookup"><span data-stu-id="892cb-117">An optional patch map specifying other possible modifications for the MIDI message</span></span>

<span data-ttu-id="892cb-118">目的地通道會設定為16個 MIDI 通道的其中一個。</span><span class="sxs-lookup"><span data-stu-id="892cb-118">The destination channel is set to one of the 16 MIDI channels.</span></span> <span data-ttu-id="892cb-119">會修改 MIDI 訊息，以反映每個新的通道指派。</span><span class="sxs-lookup"><span data-stu-id="892cb-119">MIDI messages are modified to reflect each new channel assignment.</span></span> <span data-ttu-id="892cb-120">例如，如果 MIDI 通道4的目的地通道專案設定為6，傳送至通道4的所有 MIDI 訊息都會對應到 channel 6，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="892cb-120">For example, if the destination channel entry for MIDI channel 4 is set to 6, all MIDI messages sent to channel 4 will be mapped to channel 6, as shown in the following illustration.</span></span>

![對應的 midi 映射](images/mmap-a05.gif)

<span data-ttu-id="892cb-122">在此範例中，MIDI 狀態位元組0x93 會對應至0x95。</span><span class="sxs-lookup"><span data-stu-id="892cb-122">In this example, the MIDI status byte 0x93 is mapped to 0x95.</span></span> <span data-ttu-id="892cb-123">MIDI 狀態位元組的低順序會指定頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="892cb-123">The low-order of a MIDI status byte specifies the channel number.</span></span> <span data-ttu-id="892cb-124">來源通道設定為 [作用中] 或 [非使用中]。</span><span class="sxs-lookup"><span data-stu-id="892cb-124">Source channels are set to either active or inactive.</span></span> <span data-ttu-id="892cb-125">傳送至非使用中來源通道的訊息會被忽略，因此非作用中的通道會變成靜音或關閉。</span><span class="sxs-lookup"><span data-stu-id="892cb-125">Messages sent to inactive source channels are ignored, so an inactive channel is in effect muted or turned off.</span></span>

<span data-ttu-id="892cb-126">目的地輸出裝置會設定為其中一個可用的 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="892cb-126">The destination output device is set to one of the available MIDI output devices.</span></span> <span data-ttu-id="892cb-127">MIDI 輸出裝置可以是內部合成器或實體的 MIDI 輸出埠。</span><span class="sxs-lookup"><span data-stu-id="892cb-127">A MIDI output device can be an internal synthesizer or a physical MIDI output port.</span></span>

<span data-ttu-id="892cb-128">MIDI 系統訊息是 (狀態位元組) 從0xF0 到0xFF 的 MIDI 訊息。</span><span class="sxs-lookup"><span data-stu-id="892cb-128">MIDI system messages are MIDI messages (with status bytes) from 0xF0 to 0xFF.</span></span> <span data-ttu-id="892cb-129">沒有與 MIDI 系統訊息相關聯的通道，因此無法對應。</span><span class="sxs-lookup"><span data-stu-id="892cb-129">There is no channel associated with MIDI system messages, so they cannot be mapped.</span></span> <span data-ttu-id="892cb-130">MIDI 系統訊息會傳送至通道對應中列出的所有 MIDI 輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="892cb-130">MIDI system messages are sent to all MIDI output devices listed in a channel map.</span></span>

 

 





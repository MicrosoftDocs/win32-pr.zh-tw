---
title: MIDI 對應程式
description: MIDI 對應程式
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows 多媒體，MIDI 對應程式
- 多媒體，MIDI 對應程式
- 多媒體音訊、MIDI 對應程式
- 音訊、MIDI 對應程式
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應程式，關於
- MIDI 對應程式，來源
- MIDI 對應程式，目的地
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021274"
---
# <a name="the-midi-mapper"></a><span data-ttu-id="0ef90-112">MIDI 對應程式</span><span class="sxs-lookup"><span data-stu-id="0ef90-112">The MIDI Mapper</span></span>

<span data-ttu-id="0ef90-113">MIDI 對應工具的標準修補程式服務可為應用程式提供與裝置無關的 MIDI 檔案播放。</span><span class="sxs-lookup"><span data-stu-id="0ef90-113">The MIDI Mapper's standard patch services provide device-independent MIDI file playback for applications.</span></span> <span data-ttu-id="0ef90-114">MIDI 對應工具可以搭配使用 MCI MIDI sequencer 或低層級的 MIDI 輸出服務。</span><span class="sxs-lookup"><span data-stu-id="0ef90-114">The MIDI Mapper can be used with the MCI MIDI sequencer or with low-level MIDI output services.</span></span>

<span data-ttu-id="0ef90-115">除非另有說明，否則所有對 MIDI 通道編號的參考都會使用邏輯通道編號1到16。</span><span class="sxs-lookup"><span data-stu-id="0ef90-115">Unless stated otherwise, all references to MIDI channel numbers use the logical channel numbers 1 through 16.</span></span> <span data-ttu-id="0ef90-116">這些邏輯通道編號會對應至真正屬於 MIDI 訊息的實體通道編號0到15。</span><span class="sxs-lookup"><span data-stu-id="0ef90-116">These logical channel numbers correspond to the physical channel numbers 0 through 15 that are actually part of the MIDI message.</span></span> <span data-ttu-id="0ef90-117">所有對 MIDI 程式-變更和索引鍵值的參考都會使用實體值0到127。</span><span class="sxs-lookup"><span data-stu-id="0ef90-117">All references to MIDI program-change and key values use the physical values 0 through 127.</span></span> <span data-ttu-id="0ef90-118">除非前面加上 "0x" 前置詞，否則所有數位都是十進位數，在這種情況下，它們是十六進位。</span><span class="sxs-lookup"><span data-stu-id="0ef90-118">All numbers are decimal unless preceded by "0x" prefix, in which case they are hexadecimal.</span></span>

<span data-ttu-id="0ef90-119">在 MIDI 對應工具的討論中，「 *來源* 」一詞是指 midi 對應程式的輸入端。</span><span class="sxs-lookup"><span data-stu-id="0ef90-119">In the discussion of the MIDI Mapper, the term *source* refers to the input side of the MIDI Mapper.</span></span> <span data-ttu-id="0ef90-120">「 *目的地* 」一詞指的是 MIDI 對應程式的輸出端。</span><span class="sxs-lookup"><span data-stu-id="0ef90-120">The term *destination* refers to the output side of the MIDI Mapper.</span></span> <span data-ttu-id="0ef90-121">例如，來源通道是傳送至 MIDI 對應程式之訊息的 MIDI 通道，而目的地通道則是從 MIDI 對應程式傳送到輸出裝置之訊息的 MIDI 通道。</span><span class="sxs-lookup"><span data-stu-id="0ef90-121">For example, a source channel is the MIDI channel of a message sent to the MIDI Mapper, and a destination channel is the MIDI channel of a message sent from the MIDI Mapper to an output device.</span></span>

-   [<span data-ttu-id="0ef90-122">MIDI 對應程式和 Windows</span><span class="sxs-lookup"><span data-stu-id="0ef90-122">The MIDI Mapper and Windows</span></span>](the-midi-mapper-and-windows.md)
-   [<span data-ttu-id="0ef90-123">MIDI 對應程式架構</span><span class="sxs-lookup"><span data-stu-id="0ef90-123">The MIDI Mapper Architecture</span></span>](the-midi-mapper-architecture.md)
-   [<span data-ttu-id="0ef90-124">通道對應</span><span class="sxs-lookup"><span data-stu-id="0ef90-124">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="0ef90-125">修補程式對應</span><span class="sxs-lookup"><span data-stu-id="0ef90-125">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="0ef90-126">磁片區純量</span><span class="sxs-lookup"><span data-stu-id="0ef90-126">The Volume Scalar</span></span>](the-volume-scalar.md)
-   [<span data-ttu-id="0ef90-127">金鑰組應</span><span class="sxs-lookup"><span data-stu-id="0ef90-127">Key Maps</span></span>](key-maps.md)
-   [<span data-ttu-id="0ef90-128">地圖和 MIDI 訊息的摘要</span><span class="sxs-lookup"><span data-stu-id="0ef90-128">Summary of Maps and MIDI Messages</span></span>](summary-of-maps-and-midi-messages.md)

 

 





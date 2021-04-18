---
title: 配置和準備 MIDI 資料區塊
description: 配置和準備 MIDI 資料區塊
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- " (MIDI) 的音樂檢測數位介面，配置資料區塊"
- MIDI (的音樂檢測數位介面) ，配置資料區塊
- MIDI 服務，配置資料區塊
- 配置 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) ，準備資料區塊
- MIDI (的音樂檢測數位介面) ，準備資料區塊
- MIDI 服務，準備資料區塊
- 準備 MIDI 資料區塊
- 音樂檢測數位介面 (MIDI) 、資料區塊
- MIDI (音樂檢測數位介面) 、資料區塊
- MIDI 服務，資料區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965843"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a><span data-ttu-id="83246-114">配置和準備 MIDI 資料區塊</span><span class="sxs-lookup"><span data-stu-id="83246-114">Allocating and Preparing MIDI Data Blocks</span></span>

<span data-ttu-id="83246-115">[**MidiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)、 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)和 [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)函式需要應用程式佈建資料區塊，以傳遞至設備磁碟機以供播放或錄製之用。</span><span class="sxs-lookup"><span data-stu-id="83246-115">The [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer), and [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) functions require that applications to allocate data blocks to pass to the device drivers for playback or recording purposes.</span></span> <span data-ttu-id="83246-116">這些函式中的每一個都會使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構來描述其資料區塊。</span><span class="sxs-lookup"><span data-stu-id="83246-116">Each of these functions uses a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure to describe its data block.</span></span>

<span data-ttu-id="83246-117">使用這些函式的其中一個來將資料區塊傳遞給設備磁碟機之前，您必須為緩衝區和描述資料區塊的標頭結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="83246-117">Before you use one of these functions to pass a data block to a device driver, you must allocate memory for the buffer and the header structure that describes the data block.</span></span>

<span data-ttu-id="83246-118">Windows 提供下列功能來準備和清除 MIDI 資料區塊。</span><span class="sxs-lookup"><span data-stu-id="83246-118">Windows provides the following functions for preparing and cleaning up MIDI data blocks.</span></span>



| <span data-ttu-id="83246-119">值</span><span class="sxs-lookup"><span data-stu-id="83246-119">Value</span></span>                                                    | <span data-ttu-id="83246-120">意義</span><span class="sxs-lookup"><span data-stu-id="83246-120">Meaning</span></span>                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="83246-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="83246-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | <span data-ttu-id="83246-122">準備 MIDI 輸入資料區塊。</span><span class="sxs-lookup"><span data-stu-id="83246-122">Prepares a MIDI input data block.</span></span>                      |
| [<span data-ttu-id="83246-123">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="83246-123">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | <span data-ttu-id="83246-124">清除 MIDI 輸入資料區塊的準備工作。</span><span class="sxs-lookup"><span data-stu-id="83246-124">Cleans up the preparation of a MIDI input data block.</span></span>  |
| [<span data-ttu-id="83246-125">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="83246-125">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | <span data-ttu-id="83246-126">準備 MIDI 輸出資料區塊。</span><span class="sxs-lookup"><span data-stu-id="83246-126">Prepares a MIDI output data block.</span></span>                     |
| [<span data-ttu-id="83246-127">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="83246-127">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | <span data-ttu-id="83246-128">清除 MIDI 輸出資料區塊的準備工作。</span><span class="sxs-lookup"><span data-stu-id="83246-128">Cleans up the preparation of a MIDI output data block.</span></span> |



 

<span data-ttu-id="83246-129">將 MIDI 資料區塊傳遞到設備磁碟機之前，您必須先將緩衝區傳遞給 [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) 或 [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) 函式，以準備緩衝區。</span><span class="sxs-lookup"><span data-stu-id="83246-129">Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) or [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function.</span></span> <span data-ttu-id="83246-130">當設備磁碟機完成緩衝區並傳回時，您必須先將緩衝區傳遞給 [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) 或 [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) 函式，然後再釋放任何配置的記憶體，藉此清除這項準備工作。</span><span class="sxs-lookup"><span data-stu-id="83246-130">When the device driver is finished with the buffer and returns it, you must clean up this preparation by passing the buffer to the [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) or [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) function before any allocated memory can be freed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83246-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="83246-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83246-132">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="83246-132">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 
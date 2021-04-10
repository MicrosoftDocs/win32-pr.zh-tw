---
title: " (MCI) 的 Media Control 介面"
description: " (MCI) 的 Media Control 介面"
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- 'Windows 多媒體、媒體控制介面 (MCI) '
- '多媒體、媒體控制介面 (MCI) '
- '多媒體音訊、媒體控制介面 (MCI) '
- '音訊、媒體控制介面 (MCI) '
- '音樂檢測數位介面 (MIDI) 、媒體控制介面 (MCI) '
- 'MIDI (的音樂檢測數位介面) 、媒體控制介面 (MCI) '
- '媒體控制介面 (MCI) 、音樂檢測數位介面 (MIDI) '
- 'MCI (媒體控制介面) 、音樂檢測數位介面 (MIDI) '
- 媒體控制介面 (MCI) 、MIDI sequencer
- MCI (媒體控制介面) 、MIDI sequencer
- MCI MIDI sequencer，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021373"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="e1845-114"> (MCI) 的 Media Control 介面</span><span class="sxs-lookup"><span data-stu-id="e1845-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="e1845-115">MCI MIDI sequencer 是播放 MIDI 檔案的 MCI 系統元件。</span><span class="sxs-lookup"><span data-stu-id="e1845-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="e1845-116">應用程式可以使用 MCI 輕鬆地播放 MIDI 檔案，但 MCI 對 MIDI 功能有下列限制：</span><span class="sxs-lookup"><span data-stu-id="e1845-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="e1845-117">MCI 僅支援 MIDI 輸出。</span><span class="sxs-lookup"><span data-stu-id="e1845-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="e1845-118">MCI 不允許在 MIDI 事件與其他即時事件之間進行關閉同步處理 (例如影片) 。</span><span class="sxs-lookup"><span data-stu-id="e1845-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="e1845-119">如果您需要精確的 MIDI 同步處理，您必須使用串流緩衝區或 MIDI 服務。</span><span class="sxs-lookup"><span data-stu-id="e1845-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="e1845-120">如果您需要 MIDI 輸入功能，您必須使用 MIDI 服務。</span><span class="sxs-lookup"><span data-stu-id="e1845-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="e1845-121">MCI MIDI sequencer 會播放標準的 MIDI 檔案和資源交換檔案格式 (RIFF) 的 MIDI 檔，稱為 RMID 檔案。</span><span class="sxs-lookup"><span data-stu-id="e1845-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="e1845-122">標準 MIDI 檔案符合標準的 [midi 檔案 1.0](creating-midi-files.md) 規格。</span><span class="sxs-lookup"><span data-stu-id="e1845-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="e1845-123">因為 RMID 檔案是具有 RIFF 標頭的標準 MIDI 檔案，所以標準 MIDI 檔案的相關資訊也適用于 RMID 檔案。</span><span class="sxs-lookup"><span data-stu-id="e1845-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="e1845-124">如需 RIFF 檔的詳細資訊，請參閱 [資源交換檔案格式服務](resource-interchange-file-format-services.md)。</span><span class="sxs-lookup"><span data-stu-id="e1845-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="e1845-125">雖然目前有三種標準的 MIDI 檔案，但 MCI sequencer 只會播放其中兩個： Format 0 和 Format 1 MIDI 檔。</span><span class="sxs-lookup"><span data-stu-id="e1845-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="e1845-126">如需控制多媒體裝置 (包括使用 MCI 命令的 sequencers) 的詳細資訊，請參閱 [mci](mci.md)。</span><span class="sxs-lookup"><span data-stu-id="e1845-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 





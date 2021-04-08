---
title: 關於 MIDI
description: 關於 MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- 'Windows 多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體、音樂檢測數位介面 (MIDI) '
- '多媒體音訊、音樂檢測數位介面 (MIDI) '
- '音訊、音樂檢測數位介面 (MIDI) '
- 音樂檢測數位介面 (MIDI) ，關於
- MIDI (的音樂檢測數位介面) ，關於
- '音樂檢測數位介面 (MIDI) 、媒體控制介面 (MCI) '
- 'MIDI (的音樂檢測數位介面) 、媒體控制介面 (MCI) '
- 音樂檢測數位介面 (MIDI) 、串流緩衝區
- MIDI (音樂檢測數位介面) 、串流緩衝區
- 音樂檢測數位介面 (MIDI) 、MIDI 服務
- MIDI (的音樂檢測數位介面) 、MIDI 服務
- '媒體控制介面 (MCI) 、音樂檢測數位介面 (MIDI) '
- 'MCI (媒體控制介面) 、音樂檢測數位介面 (MIDI) '
- 串流緩衝區，關於
- MIDI 服務，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672151"
---
# <a name="about-midi"></a><span data-ttu-id="46861-119">關於 MIDI</span><span class="sxs-lookup"><span data-stu-id="46861-119">About MIDI</span></span>

<span data-ttu-id="46861-120">Microsoft Win32 應用程式開發介面 (API) 提供下列方法讓應用程式使用 MIDI 資料：</span><span class="sxs-lookup"><span data-stu-id="46861-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="46861-121"> (MCI) 的媒體控制介面。</span><span class="sxs-lookup"><span data-stu-id="46861-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="46861-122">雖然播放 MIDI 檔案最簡單的方式是使用 MCIWnd 視窗類別，您也可以使用 MCI 命令來建立 MIDI 裝置的自訂介面。</span><span class="sxs-lookup"><span data-stu-id="46861-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="46861-123">如需 MCIWnd 視窗類別的詳細資訊，請參閱 [MCIWnd 視窗類別](mciwnd-window-class.md)。</span><span class="sxs-lookup"><span data-stu-id="46861-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="46861-124">如需 MCI 的詳細 [資訊，請參閱 mci](mci.md)或 [Media CONTROL Interface (mci) ](media-control-interface--mci.md)。</span><span class="sxs-lookup"><span data-stu-id="46861-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="46861-125">[資料流程緩衝區](stream-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="46861-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="46861-126">此格式可讓應用程式操作時間戳記之 MIDI 資料的緩衝區以進行播放。</span><span class="sxs-lookup"><span data-stu-id="46861-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="46861-127">串流緩衝區適用于需要比 MCI 提供更精確控制輸出的應用程式。</span><span class="sxs-lookup"><span data-stu-id="46861-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="46861-128">[MIDI 服務](midi-services.md)。</span><span class="sxs-lookup"><span data-stu-id="46861-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="46861-129">需要最精確控制 MIDI 資料的應用程式通常會使用這些低層級的服務。</span><span class="sxs-lookup"><span data-stu-id="46861-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="46861-130">下列主題將討論這些方法的每一種，並提供 MIDI 對應程式的總覽。</span><span class="sxs-lookup"><span data-stu-id="46861-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="46861-131">MIDI 對應程式</span><span class="sxs-lookup"><span data-stu-id="46861-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="46861-132"> (MCI) 的 Media Control 介面 </span><span class="sxs-lookup"><span data-stu-id="46861-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="46861-133">資料流程緩衝區</span><span class="sxs-lookup"><span data-stu-id="46861-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="46861-134">MIDI 服務</span><span class="sxs-lookup"><span data-stu-id="46861-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="46861-135">播放 MIDI 檔案</span><span class="sxs-lookup"><span data-stu-id="46861-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="46861-136">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="46861-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="46861-137">處理來自兩個 MIDI 來源的 MIDI 資料</span><span class="sxs-lookup"><span data-stu-id="46861-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="46861-138">建立 MIDI 檔案</span><span class="sxs-lookup"><span data-stu-id="46861-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 





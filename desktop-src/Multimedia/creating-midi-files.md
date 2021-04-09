---
title: 建立 MIDI 檔案
description: 建立 MIDI 檔案
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows 多媒體，建立 MIDI 檔案
- 多媒體，建立 MIDI 檔案
- 多媒體音訊，建立 MIDI 檔
- 音訊，建立 MIDI 檔案
- " (MIDI) 的音樂檢測數位介面，建立檔案"
- MIDI (的音樂檢測數位介面) ，建立檔案
- 建立 MIDI 檔案，關於
- " (MMA) 的 MIDI 製造商關聯"
- 'MMA (MIDI 製造商關聯) '
- MIDI 詳細規格
- 標準 MIDI 檔案規格
- 一般 MIDI (GM) 規格
- GM (一般 MIDI) 規格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021168"
---
# <a name="creating-midi-files"></a><span data-ttu-id="8c5cf-116">建立 MIDI 檔案</span><span class="sxs-lookup"><span data-stu-id="8c5cf-116">Creating MIDI Files</span></span>

<span data-ttu-id="8c5cf-117">樂器數位介面 (的 MIDI) 規格是由所發佈，而且是「MIDI 製造商」關聯 (MMA) 的受著作權保護的內容。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="8c5cf-118">下列清單描述最大的一般興趣規格：</span><span class="sxs-lookup"><span data-stu-id="8c5cf-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="8c5cf-119">MIDI 詳細規格</span><span class="sxs-lookup"><span data-stu-id="8c5cf-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="8c5cf-120">MIDI 詳細規格說明了 MIDI 硬體和軟體通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="8c5cf-121">這對開發多媒體應用程式很有用，這些應用程式會使用 MIDI 功能來錄製、編輯及/或播放 MIDI 資料，以實行 MIDI 支援。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="8c5cf-122">標準 MIDI 檔案1。0</span><span class="sxs-lookup"><span data-stu-id="8c5cf-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="8c5cf-123">標準 MIDI 檔案規格定義了一種方法，可在相同或不同硬體平臺上的不同應用程式之間交換時間戳記的 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="8c5cf-124">這對於撰寫應用程式以讀取和剖析包含 MIDI 資料的磁片檔案，以及/或將 MIDI 資料檔案寫入磁片的應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="8c5cf-125">一般 MIDI 系統-層級1</span><span class="sxs-lookup"><span data-stu-id="8c5cf-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="8c5cf-126">一般 MIDI (GM) 規格會定義「一般 MIDI 系統」的最小 MIDI 設定。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="8c5cf-127">這個系統是由一種特定的 MIDI 播放裝置類別所組成，而且對撰寫 MIDI 檔案的多媒體開發人員而言也很感興趣。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="8c5cf-128">現今製造的大部分電腦音效卡和 MIDI 合成者都與 GM 規格相容。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="8c5cf-129">針對 GM 規格所撰寫的 MIDI 檔案，通常應該會因為其預定音效而音效，無論是在哪一個 GM 相容裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="8c5cf-130">為了讓 MIDI 檔案成為在多媒體運算中代表音樂的可行格式，Windows 會遵循一般的 MIDI 系統層級1規格。</span><span class="sxs-lookup"><span data-stu-id="8c5cf-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="8c5cf-131">下列主題提供其他的 MIDI 撰寫指導方針：</span><span class="sxs-lookup"><span data-stu-id="8c5cf-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="8c5cf-132">適用于 MIDI 檔案的撰寫指導方針</span><span class="sxs-lookup"><span data-stu-id="8c5cf-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="8c5cf-133">標準 MIDI 修補程式指派</span><span class="sxs-lookup"><span data-stu-id="8c5cf-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="8c5cf-134">標準 MIDI 金鑰指派</span><span class="sxs-lookup"><span data-stu-id="8c5cf-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 





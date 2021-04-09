---
title: 變更內部 MIDI 合成器磁片區
description: 變更內部 MIDI 合成器磁片區
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- 音樂檢測數位介面 (MIDI) 、內部合成工具
- MIDI (的音樂檢測數位介面) ，內部合成
- 播放 MIDI 檔案，內部合成
- 內部 MIDI 合成
- 音樂檢測數位介面 (MIDI) ，變更音量
- MIDI (的音樂檢測數位介面) ，變更音量
- 播放 MIDI 檔案，變更磁片區
- 變更 MIDI 磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933209"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="5e109-111">變更內部 MIDI 合成器磁片區</span><span class="sxs-lookup"><span data-stu-id="5e109-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="5e109-112">Windows 提供下列功能，以抓取並設定內部 MIDI 合成裝置的音量層級：</span><span class="sxs-lookup"><span data-stu-id="5e109-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="5e109-113">值</span><span class="sxs-lookup"><span data-stu-id="5e109-113">Value</span></span>                                        | <span data-ttu-id="5e109-114">意義</span><span class="sxs-lookup"><span data-stu-id="5e109-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5e109-115">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="5e109-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="5e109-116">抓取指定內部 MIDI 合成裝置的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="5e109-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="5e109-117">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="5e109-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="5e109-118">設定指定之內部 MIDI 合成裝置的音量層級。</span><span class="sxs-lookup"><span data-stu-id="5e109-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="5e109-119">並非所有的 MIDI 輸出裝置都支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="5e109-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="5e109-120">某些裝置可支援左右通道上的個別磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="5e109-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="5e109-121">如需如何判斷特定裝置是否支援磁片區變更的相關資訊，請參閱 [查詢 MIDI 輸出裝置](querying-midi-output-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="5e109-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="5e109-122">除非您的應用程式是設計成主要磁片區控制應用程式 (為使用者提供系統) 中所有音訊裝置的音量控制，否則您應該先開啟音訊裝置，再變更其磁片區。</span><span class="sxs-lookup"><span data-stu-id="5e109-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="5e109-123">您也應該先檢查磁片區層級，再進行變更，並儘快將磁片區層級還原至先前的層級。</span><span class="sxs-lookup"><span data-stu-id="5e109-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="5e109-124">磁片區會指定為雙量值。</span><span class="sxs-lookup"><span data-stu-id="5e109-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="5e109-125">上層16位會指定右通道的相對磁片區，而較低的16個位則指定左邊通道的相對磁片區。</span><span class="sxs-lookup"><span data-stu-id="5e109-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="5e109-126">對於不支援左右通道上個別磁片區變更的裝置，較低的16位會指定磁片區層級，而會忽略前16位。</span><span class="sxs-lookup"><span data-stu-id="5e109-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="5e109-127">磁片區層級的值範圍從 0x0 (無回應) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。</span><span class="sxs-lookup"><span data-stu-id="5e109-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="5e109-128">將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。</span><span class="sxs-lookup"><span data-stu-id="5e109-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 
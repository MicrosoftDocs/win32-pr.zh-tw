---
title: 查詢 MIDI 輸出裝置
description: 查詢 MIDI 輸出裝置
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- 音樂檢測數位介面 (MIDI) 、輸出裝置
- MIDI (的音樂檢測數位介面) ，輸出裝置
- 播放 MIDI 檔案，輸出裝置
- MIDI 輸出裝置
- 音樂檢測數位介面 (MIDI) ，查詢輸出裝置
- MIDI (的音樂檢測數位介面) ，查詢輸出裝置
- 播放 MIDI 檔案，查詢輸出裝置
- 查詢 MIDI 輸出裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106978577"
---
# <a name="querying-midi-output-devices"></a><span data-ttu-id="c41e2-111">查詢 MIDI 輸出裝置</span><span class="sxs-lookup"><span data-stu-id="c41e2-111">Querying MIDI Output Devices</span></span>

<span data-ttu-id="c41e2-112">播放 MIDI 檔案之前，您應該使用 [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) 函式來判斷系統中的 midi 輸出裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="c41e2-112">Before playing a MIDI file, you should use the [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) function to determine the capabilities of the MIDI output device that is present in the system.</span></span> <span data-ttu-id="c41e2-113">此函式會採用 [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) 結構的位址，其會填入指定裝置功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c41e2-113">This function takes an address of a [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure, which it fills with information about the capabilities of the given device.</span></span> <span data-ttu-id="c41e2-114">這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及 (在 **wMid**、 **wPid**、 **szPname** 和 **vDriverVersion** 成員中分別指定的設備磁碟機版本號碼) 。</span><span class="sxs-lookup"><span data-stu-id="c41e2-114">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver (specified in the **wMid**, **wPid**, **szPname**, and **vDriverVersion** members, respectively).</span></span>

<span data-ttu-id="c41e2-115">MIDI 輸出裝置可以是內部合成或外部 MIDI 輸出埠。</span><span class="sxs-lookup"><span data-stu-id="c41e2-115">MIDI output devices can be either internal synthesizers or external MIDI output ports.</span></span> <span data-ttu-id="c41e2-116">**MIDIOUTCAPS** 結構的 **wTechnology** 成員會指定裝置的技術。</span><span class="sxs-lookup"><span data-stu-id="c41e2-116">The **wTechnology** member of the **MIDIOUTCAPS** structure specifies the technology of the device.</span></span>

<span data-ttu-id="c41e2-117">如果裝置是內部合成器， **wVoices**、 **wNotes** 和 **wChannelMask** 成員中會提供其他的裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="c41e2-117">If the device is an internal synthesizer, additional device information is available in the **wVoices**, **wNotes**, and **wChannelMask** members.</span></span> <span data-ttu-id="c41e2-118">**WVoices** 成員會指定裝置支援的語音數目。</span><span class="sxs-lookup"><span data-stu-id="c41e2-118">The **wVoices** member specifies the number of voices that the device supports.</span></span> <span data-ttu-id="c41e2-119">每個語音可以有不同的音效或 timbre。</span><span class="sxs-lookup"><span data-stu-id="c41e2-119">Each voice can have a different sound or timbre.</span></span> <span data-ttu-id="c41e2-120">語音會組織成 MIDI 頻道。</span><span class="sxs-lookup"><span data-stu-id="c41e2-120">Voices are organized into MIDI channels.</span></span> <span data-ttu-id="c41e2-121">**WNotes** 成員會指定裝置的 *polyphony* ，也就是可以同時播放的最大附注數目。</span><span class="sxs-lookup"><span data-stu-id="c41e2-121">The **wNotes** member specifies the *polyphony* of the device — that is, the maximum number of notes that can be played simultaneously.</span></span> <span data-ttu-id="c41e2-122">**WChannelMask** 成員是裝置所回應之 MIDI 通道的位標記法。</span><span class="sxs-lookup"><span data-stu-id="c41e2-122">The **wChannelMask** member is a bit representation of the MIDI channels that the device responds to.</span></span> <span data-ttu-id="c41e2-123">例如，如果裝置回應前八個 MIDI 通道，則 **wChannelMask** 為0x00FF。</span><span class="sxs-lookup"><span data-stu-id="c41e2-123">For example, if the device responds to the first eight MIDI channels, **wChannelMask** is 0x00FF.</span></span> <span data-ttu-id="c41e2-124">如果裝置是外部輸出埠，則不會使用 **wVoices** 和 **WNotes** ，而 **wChannelMask** 會設定為0xffff。</span><span class="sxs-lookup"><span data-stu-id="c41e2-124">If the device is an external output port, **wVoices** and **wNotes** are unused, and **wChannelMask** is set to 0xFFFF.</span></span>

<span data-ttu-id="c41e2-125">**MIDIOUTCAPS** 結構的 **dwSupport** 成員會指出設備磁碟機是否支援磁片區變更、修補程式快取，以及串流處理。</span><span class="sxs-lookup"><span data-stu-id="c41e2-125">The **dwSupport** member of the **MIDIOUTCAPS** structure indicates whether the device driver supports volume changes, patch caching, and streaming.</span></span> <span data-ttu-id="c41e2-126">只有內部合成裝置才支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="c41e2-126">Volume changes are supported only by internal synthesizer devices.</span></span> <span data-ttu-id="c41e2-127">外部 MIDI 輸出埠不支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="c41e2-127">External MIDI output ports do not support volume changes.</span></span> <span data-ttu-id="c41e2-128">如需變更磁片區的相關資訊，請參閱 [變更內部 MIDI 合成器磁片](changing-internal-midi-synthesizer-volume.md)區。</span><span class="sxs-lookup"><span data-stu-id="c41e2-128">For information about changing volume, see [Changing Internal MIDI Synthesizer Volume](changing-internal-midi-synthesizer-volume.md).</span></span>

 

 
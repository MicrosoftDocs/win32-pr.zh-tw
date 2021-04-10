---
title: 使用內部 MIDI 合成程式預先載入修補程式
description: 使用內部 MIDI 合成程式預先載入修補程式
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- 音樂檢測數位介面 (MIDI) 、內部合成工具
- MIDI (的音樂檢測數位介面) ，內部合成
- 播放 MIDI 檔案，內部合成
- 內部 MIDI 合成
- " (MIDI) 的音樂檢測數位介面，預先載入修補程式"
- MIDI (的音樂檢測數位介面) ，預先載入修補程式
- 播放 MIDI 檔案，預先載入修補程式
- 預先載入 MIDI 修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933149"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="dedcd-111">使用內部 MIDI 合成程式預先載入修補程式</span><span class="sxs-lookup"><span data-stu-id="dedcd-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="dedcd-112">某些內部的 MIDI 合成器裝置無法同時載入其所有修補程式。</span><span class="sxs-lookup"><span data-stu-id="dedcd-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="dedcd-113">這些裝置必須預先載入其修補程式資料。</span><span class="sxs-lookup"><span data-stu-id="dedcd-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="dedcd-114">Windows 提供下列函式來要求合成器預先載入並快取指定的修補程式。</span><span class="sxs-lookup"><span data-stu-id="dedcd-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="dedcd-115">值</span><span class="sxs-lookup"><span data-stu-id="dedcd-115">Value</span></span>                                                      | <span data-ttu-id="dedcd-116">意義</span><span class="sxs-lookup"><span data-stu-id="dedcd-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dedcd-117">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="dedcd-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="dedcd-118">要求內部 MIDI 合成器裝置預先載入並快取指定的 melodic 修補程式。</span><span class="sxs-lookup"><span data-stu-id="dedcd-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="dedcd-119">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="dedcd-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="dedcd-120">要求內部 MIDI 合成器裝置預先載入並快取指定的金鑰型 percussion 修補程式。</span><span class="sxs-lookup"><span data-stu-id="dedcd-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="dedcd-121">如需如何判斷特定裝置是否支援預先載入修補程式的相關資訊，請參閱 [查詢 MIDI 輸出裝置](querying-midi-output-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="dedcd-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 
---
title: 變更音調和播放速率
description: 變更音調和播放速率
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- 波形音訊、音調
- 波形-音訊介面、音調
- 波形音訊，播放速率
- 波形-音訊介面，播放速率
- 波形音訊，變更音調
- 波形-音訊介面，變更音調
- 波形音訊，變更播放速率
- 波形-音訊介面，變更播放速率
- 變更波形-音訊播放速率
- 變更波形-音訊音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463148"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="5f20e-113">變更音調和播放速率</span><span class="sxs-lookup"><span data-stu-id="5f20e-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="5f20e-114">某些波形音訊輸出裝置可能會改變波形音訊資料的音調和播放速率。</span><span class="sxs-lookup"><span data-stu-id="5f20e-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="5f20e-115">並非所有波形音訊裝置都支援音調和播放速率變更。</span><span class="sxs-lookup"><span data-stu-id="5f20e-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="5f20e-116">如需如何判斷特定波形音訊裝置是否支援音調和播放速率變更的相關資訊，請參閱 [裝置和資料類型](devices-and-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5f20e-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="5f20e-117">變更音調和播放速率之間的差異如下：</span><span class="sxs-lookup"><span data-stu-id="5f20e-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="5f20e-118">變更播放速率是由設備磁碟機所執行，不需要特製化硬體。</span><span class="sxs-lookup"><span data-stu-id="5f20e-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="5f20e-119">取樣率未變更，但驅動程式會略過或合成範例來進行插補。</span><span class="sxs-lookup"><span data-stu-id="5f20e-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="5f20e-120">例如，如果播放速率以二的因數變更，驅動程式會略過每個其他範例。</span><span class="sxs-lookup"><span data-stu-id="5f20e-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="5f20e-121">變更推銷需要特製化硬體。</span><span class="sxs-lookup"><span data-stu-id="5f20e-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="5f20e-122">播放速率和取樣率不會變更。</span><span class="sxs-lookup"><span data-stu-id="5f20e-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="5f20e-123">Windows 提供下列功能來查詢及設定波形-音訊音調和播放速率。</span><span class="sxs-lookup"><span data-stu-id="5f20e-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="5f20e-124">函式</span><span class="sxs-lookup"><span data-stu-id="5f20e-124">Function</span></span>                                                 | <span data-ttu-id="5f20e-125">描述</span><span class="sxs-lookup"><span data-stu-id="5f20e-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="5f20e-126">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="5f20e-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="5f20e-127">抓取指定波形音訊輸出裝置的間距。</span><span class="sxs-lookup"><span data-stu-id="5f20e-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="5f20e-128">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="5f20e-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="5f20e-129">抓取指定波形音訊輸出裝置的播放速率。</span><span class="sxs-lookup"><span data-stu-id="5f20e-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="5f20e-130">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="5f20e-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="5f20e-131">設定指定之波形音訊輸出裝置的間距。</span><span class="sxs-lookup"><span data-stu-id="5f20e-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="5f20e-132">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="5f20e-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="5f20e-133">設定指定之波形音訊輸出裝置的播放速率。</span><span class="sxs-lookup"><span data-stu-id="5f20e-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="5f20e-134">音調和播放速率會以將固定點數位壓縮成雙字值指定的因素來變更。</span><span class="sxs-lookup"><span data-stu-id="5f20e-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="5f20e-135">上層16位會指定數位的整數部分;較低的16位會指定小數部分。</span><span class="sxs-lookup"><span data-stu-id="5f20e-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="5f20e-136">例如，值1.5 表示為0x00018000L。</span><span class="sxs-lookup"><span data-stu-id="5f20e-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="5f20e-137">值0.75 以0x0000C000L 表示。</span><span class="sxs-lookup"><span data-stu-id="5f20e-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="5f20e-138">值為 1.0 (0x00010000) 表示音調或播放速率未變更。</span><span class="sxs-lookup"><span data-stu-id="5f20e-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 
---
title: EQUALIZERSETTINGS 元素
description: EQUALIZERSETTINGS 元素
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Windows Media Player 的 EQUALIZERSETTINGS 元素
- 外觀，EQUALIZERSETTINGS 元素
- EQUALIZERSETTINGS 元素
- EQUALIZERSETTINGS 元素的外觀參考
- 元素，EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507244"
---
# <a name="equalizersettings-element"></a><span data-ttu-id="181b2-108">EQUALIZERSETTINGS 元素</span><span class="sxs-lookup"><span data-stu-id="181b2-108">EQUALIZERSETTINGS Element</span></span>

<span data-ttu-id="181b2-109">**EQUALIZERSETTINGS** 元素會使用此處所列的屬性和方法，提供管理 Windows Media Player 的圖形等化器和其他音訊設定的方式。</span><span class="sxs-lookup"><span data-stu-id="181b2-109">The **EQUALIZERSETTINGS** element provides a way to manipulate the graphic equalizer and other audio settings of Windows Media Player using the attributes and method listed here.</span></span>

<span data-ttu-id="181b2-110">**EQUALIZERSETTINGS** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="181b2-110">The **EQUALIZERSETTINGS** element supports the following attributes.</span></span>



| <span data-ttu-id="181b2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="181b2-111">Attribute</span></span>                                                          | <span data-ttu-id="181b2-112">描述</span><span class="sxs-lookup"><span data-stu-id="181b2-112">Description</span></span>                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="181b2-113">寬線</span><span class="sxs-lookup"><span data-stu-id="181b2-113">bands</span></span>](equalizersettings-bands.md)                               | <span data-ttu-id="181b2-114">抓取支援的頻率區段數目。</span><span class="sxs-lookup"><span data-stu-id="181b2-114">Retrieves the number of frequency bands supported.</span></span>                                                      |
| [<span data-ttu-id="181b2-115">旁路</span><span class="sxs-lookup"><span data-stu-id="181b2-115">bypass</span></span>](equalizersettings-bypass.md)                             | <span data-ttu-id="181b2-116">指定或抓取值，指出是否略過篩選圖形中的等化器篩選。</span><span class="sxs-lookup"><span data-stu-id="181b2-116">Specifies or retrieves a value indicating whether the equalizer filter is bypassed in the filter graph.</span></span> |
| [<span data-ttu-id="181b2-117">crossFade</span><span class="sxs-lookup"><span data-stu-id="181b2-117">crossFade</span></span>](equalizersettings-crossfade.md)                       | <span data-ttu-id="181b2-118">指定或抓取值，指出是否已啟用交叉淡化。</span><span class="sxs-lookup"><span data-stu-id="181b2-118">Specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>                                |
| [<span data-ttu-id="181b2-119">crossFadeWindow</span><span class="sxs-lookup"><span data-stu-id="181b2-119">crossFadeWindow</span></span>](equalizersettings-crossfadewindow.md)           | <span data-ttu-id="181b2-120">指定或抓取交叉淡化重迭量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="181b2-120">Specifies or retrieves the amount of cross-fade overlap in milliseconds.</span></span>                                |
| [<span data-ttu-id="181b2-121">currentPreset</span><span class="sxs-lookup"><span data-stu-id="181b2-121">currentPreset</span></span>](equalizersettings-currentpreset.md)               | <span data-ttu-id="181b2-122">指定或抓取目前預設值的索引。</span><span class="sxs-lookup"><span data-stu-id="181b2-122">Specifies or retrieves the index of the current preset.</span></span>                                                 |
| [<span data-ttu-id="181b2-123">currentPresetTitle</span><span class="sxs-lookup"><span data-stu-id="181b2-123">currentPresetTitle</span></span>](equalizersettings-currentpresettitle.md)     | <span data-ttu-id="181b2-124">抓取目前預設值的標題。</span><span class="sxs-lookup"><span data-stu-id="181b2-124">Retrieves the title of the current preset.</span></span>                                                              |
| [<span data-ttu-id="181b2-125">currentSpeakerName</span><span class="sxs-lookup"><span data-stu-id="181b2-125">currentSpeakerName</span></span>](equalizersettings-currentspeakername.md)     | <span data-ttu-id="181b2-126">抓取目前說話者設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="181b2-126">Retrieves the name of the current speaker setting.</span></span>                                                      |
| [<span data-ttu-id="181b2-127">enableSplineTension</span><span class="sxs-lookup"><span data-stu-id="181b2-127">enableSplineTension</span></span>](equalizersettings-enablesplinetension.md)   | <span data-ttu-id="181b2-128">指定或抓取值，指出是否已啟用或停用曲線張力。</span><span class="sxs-lookup"><span data-stu-id="181b2-128">Specifies or retrieves a value indicating whether spline tension is enabled or disabled.</span></span>                |
| [<span data-ttu-id="181b2-129">enhancedAudio</span><span class="sxs-lookup"><span data-stu-id="181b2-129">enhancedAudio</span></span>](equalizersettings-enhancedaudio.md)               | <span data-ttu-id="181b2-130">指定或抓取指出增強音訊是否已開啟的值。</span><span class="sxs-lookup"><span data-stu-id="181b2-130">Specifies or retrieves a value indicating whether enhanced audio is turned on.</span></span>                          |
| [<span data-ttu-id="181b2-131">gainLevels</span><span class="sxs-lookup"><span data-stu-id="181b2-131">gainLevels</span></span>](equalizersettings-gainlevels.md)                     | <span data-ttu-id="181b2-132">指定或抓取對應于所提供之索引的帶狀增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-132">Specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>                  |
| [<span data-ttu-id="181b2-133">gainLevel1</span><span class="sxs-lookup"><span data-stu-id="181b2-133">gainLevel1</span></span>](equalizersettings-gainlevel1.md)                     | <span data-ttu-id="181b2-134">指定或抓取寬線1的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-134">Specifies or retrieves the gain level of band 1.</span></span>                                                        |
| [<span data-ttu-id="181b2-135">gainLevel2</span><span class="sxs-lookup"><span data-stu-id="181b2-135">gainLevel2</span></span>](equalizersettings-gainlevel2.md)                     | <span data-ttu-id="181b2-136">指定或抓取寬線2的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-136">Specifies or retrieves the gain level of band 2.</span></span>                                                        |
| [<span data-ttu-id="181b2-137">gainLevel3</span><span class="sxs-lookup"><span data-stu-id="181b2-137">gainLevel3</span></span>](equalizersettings-gainlevel3.md)                     | <span data-ttu-id="181b2-138">指定或抓取寬線3的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-138">Specifies or retrieves the gain level of band 3.</span></span>                                                        |
| [<span data-ttu-id="181b2-139">gainLevel4</span><span class="sxs-lookup"><span data-stu-id="181b2-139">gainLevel4</span></span>](equalizersettings-gainlevel4.md)                     | <span data-ttu-id="181b2-140">指定或抓取寬線4的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-140">Specifies or retrieves the gain level of band 4.</span></span>                                                        |
| [<span data-ttu-id="181b2-141">gainLevel5</span><span class="sxs-lookup"><span data-stu-id="181b2-141">gainLevel5</span></span>](equalizersettings-gainlevel5.md)                     | <span data-ttu-id="181b2-142">指定或抓取寬線5的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-142">Specifies or retrieves the gain level of band 5.</span></span>                                                        |
| [<span data-ttu-id="181b2-143">gainLevel6</span><span class="sxs-lookup"><span data-stu-id="181b2-143">gainLevel6</span></span>](equalizersettings-gainlevel6.md)                     | <span data-ttu-id="181b2-144">指定或抓取寬線6的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-144">Specifies or retrieves the gain level of band 6.</span></span>                                                        |
| [<span data-ttu-id="181b2-145">gainLevel7</span><span class="sxs-lookup"><span data-stu-id="181b2-145">gainLevel7</span></span>](equalizersettings-gainlevel7.md)                     | <span data-ttu-id="181b2-146">指定或抓取帶狀7的增益等級。</span><span class="sxs-lookup"><span data-stu-id="181b2-146">Specifies or retrieves the gain level of band 7.</span></span>                                                        |
| [<span data-ttu-id="181b2-147">gainLevel8</span><span class="sxs-lookup"><span data-stu-id="181b2-147">gainLevel8</span></span>](equalizersettings-gainlevel8.md)                     | <span data-ttu-id="181b2-148">指定或抓取寬線8的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-148">Specifies or retrieves the gain level of band 8.</span></span>                                                        |
| [<span data-ttu-id="181b2-149">gainLevel9</span><span class="sxs-lookup"><span data-stu-id="181b2-149">gainLevel9</span></span>](equalizersettings-gainlevel9.md)                     | <span data-ttu-id="181b2-150">指定或抓取寬線9的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-150">Specifies or retrieves the gain level of band 9.</span></span>                                                        |
| [<span data-ttu-id="181b2-151">gainLevel10</span><span class="sxs-lookup"><span data-stu-id="181b2-151">gainLevel10</span></span>](equalizersettings-gainlevel10.md)                   | <span data-ttu-id="181b2-152">指定或抓取帶狀10的增益層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-152">Specifies or retrieves the gain level of band 10.</span></span>                                                       |
| [<span data-ttu-id="181b2-153">正常化</span><span class="sxs-lookup"><span data-stu-id="181b2-153">normalization</span></span>](equalizersettings-normalization.md)               | <span data-ttu-id="181b2-154">指定或抓取表示正規化是否已啟用的值。</span><span class="sxs-lookup"><span data-stu-id="181b2-154">Specifies or retrieves a value indicating whether normalization is enabled.</span></span>                             |
| [<span data-ttu-id="181b2-155">normalizationAverage</span><span class="sxs-lookup"><span data-stu-id="181b2-155">normalizationAverage</span></span>](equalizersettings-normalizationaverage.md) | <span data-ttu-id="181b2-156">抓取平均正規化值。</span><span class="sxs-lookup"><span data-stu-id="181b2-156">Retrieves the average normalization value.</span></span>                                                              |
| [<span data-ttu-id="181b2-157">normalizationPeak</span><span class="sxs-lookup"><span data-stu-id="181b2-157">normalizationPeak</span></span>](equalizersettings-normalizationpeak.md)       | <span data-ttu-id="181b2-158">抓取尖峰標準化值。</span><span class="sxs-lookup"><span data-stu-id="181b2-158">Retrieves the peak normalization value.</span></span>                                                                 |
| [<span data-ttu-id="181b2-159">presetCount</span><span class="sxs-lookup"><span data-stu-id="181b2-159">presetCount</span></span>](equalizersettings-presetcount.md)                   | <span data-ttu-id="181b2-160">抓取可用的預設數目。</span><span class="sxs-lookup"><span data-stu-id="181b2-160">Retrieves the number of presets available.</span></span>                                                              |
| [<span data-ttu-id="181b2-161">speakerSize</span><span class="sxs-lookup"><span data-stu-id="181b2-161">speakerSize</span></span>](equalizersettings-speakersize.md)                   | <span data-ttu-id="181b2-162">指定或抓取目前說話者大小的索引。</span><span class="sxs-lookup"><span data-stu-id="181b2-162">Specifies or retrieves the index of the current speaker size.</span></span>                                           |
| [<span data-ttu-id="181b2-163">splineTension</span><span class="sxs-lookup"><span data-stu-id="181b2-163">splineTension</span></span>](equalizersettings-splinetension.md)               | <span data-ttu-id="181b2-164">指定或抓取等化器控制項的曲線張力。</span><span class="sxs-lookup"><span data-stu-id="181b2-164">Specifies or retrieves the spline tension for the equalizer control.</span></span>                                    |
| [<span data-ttu-id="181b2-165">truBassLevel</span><span class="sxs-lookup"><span data-stu-id="181b2-165">truBassLevel</span></span>](equalizersettings-trubasslevel.md)                 | <span data-ttu-id="181b2-166">指定或抓取 SRS TruBass 層級。</span><span class="sxs-lookup"><span data-stu-id="181b2-166">Specifies or retrieves the SRS TruBass level.</span></span>                                                           |
| [<span data-ttu-id="181b2-167">wowLevel</span><span class="sxs-lookup"><span data-stu-id="181b2-167">wowLevel</span></span>](equalizersettings-wowlevel.md)                         | <span data-ttu-id="181b2-168">指定或抓取 SRS WOW 效果等級。</span><span class="sxs-lookup"><span data-stu-id="181b2-168">Specifies or retrieves the SRS WOW Effect level.</span></span>                                                        |



 

<span data-ttu-id="181b2-169">**EQUALIZERSETTINGS** 元素支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="181b2-169">The **EQUALIZERSETTINGS** element supports the following methods.</span></span>



| <span data-ttu-id="181b2-170">方法</span><span class="sxs-lookup"><span data-stu-id="181b2-170">Method</span></span>                                                 | <span data-ttu-id="181b2-171">描述</span><span class="sxs-lookup"><span data-stu-id="181b2-171">Description</span></span>                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="181b2-172">nextPreset</span><span class="sxs-lookup"><span data-stu-id="181b2-172">nextPreset</span></span>](equalizersettings-nextpreset.md)         | <span data-ttu-id="181b2-173">套用下一個等化器預設值。</span><span class="sxs-lookup"><span data-stu-id="181b2-173">Applies the next equalizer preset.</span></span>                                   |
| [<span data-ttu-id="181b2-174">presetTitle</span><span class="sxs-lookup"><span data-stu-id="181b2-174">presetTitle</span></span>](equalizersettings-presettitle.md)       | <span data-ttu-id="181b2-175">使用指定的索引，抓取等化器預設值的名稱。</span><span class="sxs-lookup"><span data-stu-id="181b2-175">Retrieves the name of the equalizer preset with the specified index.</span></span> |
| [<span data-ttu-id="181b2-176">previousPreset</span><span class="sxs-lookup"><span data-stu-id="181b2-176">previousPreset</span></span>](equalizersettings-previouspreset.md) | <span data-ttu-id="181b2-177">套用先前的等化器預設值。</span><span class="sxs-lookup"><span data-stu-id="181b2-177">Applies the previous equalizer preset.</span></span>                               |
| [<span data-ttu-id="181b2-178">reset</span><span class="sxs-lookup"><span data-stu-id="181b2-178">reset</span></span>](equalizersettings-reset.md)                   | <span data-ttu-id="181b2-179">將所有波段的增益層級重設為零分貝。</span><span class="sxs-lookup"><span data-stu-id="181b2-179">Resets the gain levels of all bands to zero decibels.</span></span>                |



 

<span data-ttu-id="181b2-180">**EQUALIZERSETTINGS** 元素可以執行 [屬性 \_ onchange](attribute-onchange.md)事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="181b2-180">The **EQUALIZERSETTINGS** element can implement the [attribute\_onchange](attribute-onchange.md) event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="181b2-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="181b2-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="181b2-182">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="181b2-182">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





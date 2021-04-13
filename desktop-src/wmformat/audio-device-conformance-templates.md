---
title: 音訊裝置一致性範本
description: 音訊裝置一致性範本
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK，裝置一致性範本
- Advanced Systems Format (ASF) 、裝置一致性範本
- ASF (Advanced Systems Format) 、裝置一致性範本
- Windows Media 格式 SDK、音訊裝置一致性範本
- Advanced Systems Format (ASF) 、音訊裝置一致性範本
- ASF (Advanced Systems Format) 、音訊裝置一致性範本
- Windows Media 音訊9編解碼器、音訊裝置一致性範本
- 編解碼器，Windows Media 音訊9編解碼器
- 裝置一致性範本、影片
- 音訊裝置一致性範本
- 範本、音訊裝置一致性範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300827"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="43511-114">音訊裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="43511-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="43511-115">下表列出 Windows Media 音訊9編解碼器或更新版本的裝置一致性範本和相關聯的參數。</span><span class="sxs-lookup"><span data-stu-id="43511-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="43511-116">範本字串</span><span class="sxs-lookup"><span data-stu-id="43511-116">Template string</span></span> | <span data-ttu-id="43511-117">位元速率範圍</span><span class="sxs-lookup"><span data-stu-id="43511-117">Bit rate range</span></span>     | <span data-ttu-id="43511-118">備註</span><span class="sxs-lookup"><span data-stu-id="43511-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43511-119">L1</span><span class="sxs-lookup"><span data-stu-id="43511-119">"L1"</span></span>            | <span data-ttu-id="43511-120">64 kbps 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="43511-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="43511-121">此範本適用于受限制的僅限音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="43511-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="43511-122">L2</span><span class="sxs-lookup"><span data-stu-id="43511-122">"L2"</span></span>            | <span data-ttu-id="43511-123"><= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="43511-123"><= 160 Kbps</span></span>     | <span data-ttu-id="43511-124">此範本會對應至 Windows Media 音訊移植套件中的類別4，可支援整個 Windows Media 音訊解碼器的執行。</span><span class="sxs-lookup"><span data-stu-id="43511-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="43511-125">L3</span><span class="sxs-lookup"><span data-stu-id="43511-125">"L3"</span></span>            | <span data-ttu-id="43511-126"><= 384 Kbps</span><span class="sxs-lookup"><span data-stu-id="43511-126"><= 384 Kbps</span></span>     | <span data-ttu-id="43511-127">此範本會對應至 Windows Media 音訊移植套件中的類別4，可支援整個 Windows Media 音訊解碼器的執行。位元速率範圍是此範本和 L2 之間的唯一差異。</span><span class="sxs-lookup"><span data-stu-id="43511-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="43511-128">L</span><span class="sxs-lookup"><span data-stu-id="43511-128">"L"</span></span>             | <span data-ttu-id="43511-129">所有位元速率</span><span class="sxs-lookup"><span data-stu-id="43511-129">All bit rates</span></span>      | <span data-ttu-id="43511-130">此範本僅供個人電腦使用，通常用來展示編解碼器的完整功能。</span><span class="sxs-lookup"><span data-stu-id="43511-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="43511-131">下表列出 Windows Media 音訊9語音編解碼器的裝置一致性範本和相關聯的參數。</span><span class="sxs-lookup"><span data-stu-id="43511-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="43511-132">範本字串</span><span class="sxs-lookup"><span data-stu-id="43511-132">Template string</span></span> | <span data-ttu-id="43511-133">位元速率範圍</span><span class="sxs-lookup"><span data-stu-id="43511-133">Bit rate range</span></span> | <span data-ttu-id="43511-134">備註</span><span class="sxs-lookup"><span data-stu-id="43511-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43511-135">S1</span><span class="sxs-lookup"><span data-stu-id="43511-135">"S1"</span></span>            | <span data-ttu-id="43511-136"><= 20 Kbps</span><span class="sxs-lookup"><span data-stu-id="43511-136"><= 20 Kbps</span></span>  | <span data-ttu-id="43511-137">此範本僅適用于非常低複雜性的裝置。此範本僅限語音。</span><span class="sxs-lookup"><span data-stu-id="43511-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="43511-138">S2</span><span class="sxs-lookup"><span data-stu-id="43511-138">"S2"</span></span>            | <span data-ttu-id="43511-139"><= 20 Kbps</span><span class="sxs-lookup"><span data-stu-id="43511-139"><= 20 Kbps</span></span>  | <span data-ttu-id="43511-140">這是大部分應用程式的建議範本。此範本支援語音和音樂的組合。</span><span class="sxs-lookup"><span data-stu-id="43511-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="43511-141">下表列出 Windows Media 音訊 9 Professional 編解碼器或更新版本的裝置一致性範本和相關聯的參數。</span><span class="sxs-lookup"><span data-stu-id="43511-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="43511-142">範本字串</span><span class="sxs-lookup"><span data-stu-id="43511-142">Template string</span></span> | <span data-ttu-id="43511-143">屬性</span><span class="sxs-lookup"><span data-stu-id="43511-143">Properties</span></span>                                                                                   | <span data-ttu-id="43511-144">備註</span><span class="sxs-lookup"><span data-stu-id="43511-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43511-145">M1</span><span class="sxs-lookup"><span data-stu-id="43511-145">"M1"</span></span>            | <span data-ttu-id="43511-146">位元速率 <= 384 KbpsSampling 速率 <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="43511-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="43511-147">通道 <= 5。1</span><span class="sxs-lookup"><span data-stu-id="43511-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="43511-148">此範本建議用於具有環繞音效的標準電影。</span><span class="sxs-lookup"><span data-stu-id="43511-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="43511-149">M2</span><span class="sxs-lookup"><span data-stu-id="43511-149">"M2"</span></span>            | <span data-ttu-id="43511-150">位元速率 <= 768 KbpsSampling 速率 <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="43511-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="43511-151">通道 <= 5。1</span><span class="sxs-lookup"><span data-stu-id="43511-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="43511-152">此範本建議用於具有環繞音效的高定義電影。</span><span class="sxs-lookup"><span data-stu-id="43511-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="43511-153">M3</span><span class="sxs-lookup"><span data-stu-id="43511-153">"M3"</span></span>            | <span data-ttu-id="43511-154">位元速率 <= 1500 KbpsSampling 速率 <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="43511-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="43511-155">通道 <= 7。1</span><span class="sxs-lookup"><span data-stu-id="43511-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="43511-156">此範本建議用於具有8聲道環繞音效的高定義影片，例如在劇院中編碼以呈現的內容。</span><span class="sxs-lookup"><span data-stu-id="43511-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="43511-157">"M"</span><span class="sxs-lookup"><span data-stu-id="43511-157">"M"</span></span>             | <span data-ttu-id="43511-158">所有位 ratesAll 取樣率</span><span class="sxs-lookup"><span data-stu-id="43511-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="43511-159">所有通道</span><span class="sxs-lookup"><span data-stu-id="43511-159">All channels</span></span><br/>                           | <span data-ttu-id="43511-160">此範本僅供個人電腦使用，通常用來展示編解碼器的完整功能。這也是使用 Windows Media 音訊9無失真編解碼器編碼的所有音訊的範本指定。</span><span class="sxs-lookup"><span data-stu-id="43511-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="43511-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="43511-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43511-162">**裝置一致性範本參數**</span><span class="sxs-lookup"><span data-stu-id="43511-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="43511-163">**建議的裝置一致性範本組合**</span><span class="sxs-lookup"><span data-stu-id="43511-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="43511-164">**影片裝置一致性範本**</span><span class="sxs-lookup"><span data-stu-id="43511-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 






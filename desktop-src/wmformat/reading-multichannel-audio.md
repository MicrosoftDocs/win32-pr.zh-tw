---
title: 讀取多頻道音訊
description: 讀取多頻道音訊
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK，讀取多頻道音訊
- Advanced Systems Format (ASF) 、讀取多頻道音訊
- ASF (Advanced Systems Format) ，讀取多頻道音訊
- Advanced Systems Format (ASF) 、多頻道音訊
- ASF (Advanced Systems Format) 、多頻道音訊
- 編解碼器，讀取多頻道音訊
- 多頻道音訊，讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682896"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="6b3ed-110">讀取多頻道音訊</span><span class="sxs-lookup"><span data-stu-id="6b3ed-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="6b3ed-111">Windows Media 音訊 9 Professional 編解碼器可將多頻道音訊編碼 (超過兩個通道) 。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="6b3ed-112">使用多頻道音訊讀取檔案時，您必須正確地設定輸出，否則音訊會以較低的品質和身歷聲傳遞。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="6b3ed-113">若要設定多頻道音訊傳遞的輸出，您必須設定兩個輸出設定： g \_ wszEnableDiscreteOutput 和 g \_ wszSpeakerConfig。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="6b3ed-114">將 g \_ wszEnableDiscreteOutput 設為 **TRUE** ，會設定編解碼器以傳遞高定義音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="6b3ed-115">高定義音訊是由 Windows Media 音訊9編解碼器，以身歷聲或多個通道中的24位樣本進行編碼。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="6b3ed-116">如果此設定為 **FALSE**，則只會傳遞16位的身歷聲輸出。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="6b3ed-117">播放電腦上的喇叭數目設定為 g \_ wszSpeakerConfig。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="6b3ed-118">這項設定是設定為下表所列的其中一個 DirectSound 喇叭常數的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="6b3ed-119">若要為您的編譯器解析這些常數名稱，您必須包含 dsound。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="6b3ed-120">常數</span><span class="sxs-lookup"><span data-stu-id="6b3ed-120">Constant</span></span>             | <span data-ttu-id="6b3ed-121">值</span><span class="sxs-lookup"><span data-stu-id="6b3ed-121">Value</span></span>      | <span data-ttu-id="6b3ed-122">描述</span><span class="sxs-lookup"><span data-stu-id="6b3ed-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6b3ed-123">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="6b3ed-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="6b3ed-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6b3ed-124">0x00000000</span></span> | <span data-ttu-id="6b3ed-125">系統會直接傳遞音訊，而不是針對喇叭進行設定。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="6b3ed-126">DSSPEAKER \_ 耳機</span><span class="sxs-lookup"><span data-stu-id="6b3ed-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="6b3ed-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6b3ed-127">0x00000001</span></span> | <span data-ttu-id="6b3ed-128">用戶端電腦配備耳機。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="6b3ed-129">DSSPEAKER \_ MONO</span><span class="sxs-lookup"><span data-stu-id="6b3ed-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="6b3ed-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6b3ed-130">0x00000002</span></span> | <span data-ttu-id="6b3ed-131">用戶端電腦配備了 monaural 喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="6b3ed-132">DSSPEAKER \_ 四</span><span class="sxs-lookup"><span data-stu-id="6b3ed-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="6b3ed-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="6b3ed-133">0x00000003</span></span> | <span data-ttu-id="6b3ed-134">用戶端電腦配備了 quadraphonic 喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="6b3ed-135">DSSPEAKER \_ 身歷聲</span><span class="sxs-lookup"><span data-stu-id="6b3ed-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="6b3ed-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6b3ed-136">0x00000004</span></span> | <span data-ttu-id="6b3ed-137">用戶端電腦配備了身歷聲喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="6b3ed-138">DSSPEAKER \_ 環繞</span><span class="sxs-lookup"><span data-stu-id="6b3ed-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="6b3ed-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6b3ed-139">0x00000005</span></span> | <span data-ttu-id="6b3ed-140">用戶端電腦配備四個聲道的環繞音效喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="6b3ed-141">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="6b3ed-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="6b3ed-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="6b3ed-142">0x00000006</span></span> | <span data-ttu-id="6b3ed-143">用戶端電腦配備了五個喇叭和一個喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="6b3ed-144">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="6b3ed-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="6b3ed-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="6b3ed-145">0x00000007</span></span> | <span data-ttu-id="6b3ed-146">用戶端電腦配備了七個喇叭和一個喇叭。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="6b3ed-147">若要設定這些設定，請使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="6b3ed-148">最後，若要讓通道成為輸出分開，而不將任何折迭到身歷聲，您必須遵循下列步驟，在輸出上設定正確的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="6b3ed-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="6b3ed-149">呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) 可取得相關音訊輸出的支援格式數目。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="6b3ed-150">輸出格式索引是以零為基底。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="6b3ed-151">針對每個支援的格式，呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) ，以取出輸出媒體屬性物件上的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) 介面。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="6b3ed-152">呼叫 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) 來取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="6b3ed-153">如果取出的媒體類型是所需的多重通道類型，請呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops)來設定它。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="6b3ed-154">設定離散輸出和說話者設定之後，讀取器列舉的輸出格式應包含使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) 結構的多重通道格式。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="6b3ed-155">如果您在設定屬性之前列舉輸出格式，則只會包含1或2個通道的格式，且每個通道最多可包含16個位。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="6b3ed-156">與其他音訊格式一樣，您應該只使用讀取器列舉的格式;請勿設定您自己的。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="6b3ed-157">只有當您的應用程式是在 Microsoft Windows XP 或更新版本的 Microsoft Windows 上執行時，您才可以輸出多頻道音訊。</span><span class="sxs-lookup"><span data-stu-id="6b3ed-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6b3ed-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b3ed-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b3ed-159">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="6b3ed-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="6b3ed-160">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="6b3ed-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="6b3ed-161">**輸出設定**</span><span class="sxs-lookup"><span data-stu-id="6b3ed-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="6b3ed-162">**使用 High-Resolution PCM 音訊**</span><span class="sxs-lookup"><span data-stu-id="6b3ed-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 
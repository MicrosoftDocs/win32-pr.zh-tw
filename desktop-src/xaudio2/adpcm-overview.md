---
description: 彈性差異脈衝程式碼 (ADPCM) 是針對 XAudio2 所執行的失真壓縮格式，可提供額外的功能來指定壓縮範例區塊的大小。
ms.assetid: ae8a0a3e-293c-8193-d252-046d79771cfb
title: ADPCM 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb918a611cb0840b2f02dfb13b547b795fb3304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979221"
---
# <a name="adpcm-overview"></a><span data-ttu-id="bdd68-103">ADPCM 總覽</span><span class="sxs-lookup"><span data-stu-id="bdd68-103">ADPCM Overview</span></span>

<span data-ttu-id="bdd68-104">彈性差異脈衝程式碼 (ADPCM) 是針對 XAudio2 所執行的失真壓縮格式，可提供額外的功能來指定壓縮範例區塊的大小。</span><span class="sxs-lookup"><span data-stu-id="bdd68-104">Adaptive Differential Pulse Code Modulation (ADPCM) is a lossy compression format that is implemented for XAudio2 to provide additional features for specifying the size of the compression sample block.</span></span> <span data-ttu-id="bdd68-105">使用失真壓縮格式時，某些資料會在壓縮期間改變並遺失。</span><span class="sxs-lookup"><span data-stu-id="bdd68-105">With a lossy compression format some data is altered and lost during compression.</span></span> <span data-ttu-id="bdd68-106">ADPCM 可達到最高4:1 的壓縮比例。</span><span class="sxs-lookup"><span data-stu-id="bdd68-106">ADPCM can achieve compression ratios of up to 4:1.</span></span>

<span data-ttu-id="bdd68-107">適用于 XAudio2 的 ADPCM 會提供額外的功能來指定壓縮範例區塊的大小。</span><span class="sxs-lookup"><span data-stu-id="bdd68-107">The implementation of ADPCM for XAudio2 provides additional features to specify the size of the compression sample block.</span></span> <span data-ttu-id="bdd68-108">ADPCM 可讓音訊設計工具選擇適當的折衷方式，也就是將迴圈點放在) 的大小、品質和解析度 (。</span><span class="sxs-lookup"><span data-stu-id="bdd68-108">ADPCM enables the audio designer to choose a setting that is an appropriate compromise among size, quality, and resolution (for placing loop points).</span></span>

<span data-ttu-id="bdd68-109">XAudio2 會使用 Microsoft ADPCM 編解碼器的修改版本，以支援提供自訂範例區塊大小所需的擴充資料格式。</span><span class="sxs-lookup"><span data-stu-id="bdd68-109">XAudio2 uses a modified version of the Microsoft ADPCM codec that supports the extended data formatting required to provide custom sample block sizes.</span></span> <span data-ttu-id="bdd68-110">基於這個理由，不支援這個 ADPCM 編解碼器版本的音訊引擎無法播放 XAudio2 音訊資料。</span><span class="sxs-lookup"><span data-stu-id="bdd68-110">For this reason, XAudio2 audio data cannot be played by audio engines that do not support this version of the ADPCM codec.</span></span>

> [!Note]  
> <span data-ttu-id="bdd68-111">目前，ADPCM 壓縮僅適用于 Windows，包括適用于 Windows 部署的 windows 部署版的 windows 部署。</span><span class="sxs-lookup"><span data-stu-id="bdd68-111">Currently, ADPCM compression is only available for Windows, including XNA Game Studio Express for Windows deployments.</span></span>

 

## <a name="adpcm-encoding"></a><span data-ttu-id="bdd68-112">ADPCM 編碼</span><span class="sxs-lookup"><span data-stu-id="bdd68-112">ADPCM Encoding</span></span>

<span data-ttu-id="bdd68-113">使用 AdpcmEncode 命令列工具，將音訊資料編碼為 ADPCM。</span><span class="sxs-lookup"><span data-stu-id="bdd68-113">Audio data is encoded to ADPCM using the AdpcmEncode command-line tool.</span></span>

-   <span data-ttu-id="bdd68-114">AdpcmEncode</span><span class="sxs-lookup"><span data-stu-id="bdd68-114">AdpcmEncode</span></span>

    <span data-ttu-id="bdd68-115">為了將音訊檔案編碼為 ADPCM 以搭配 XAudio2 使用，請使用 **AdpcmEncode** 命令列工具。</span><span class="sxs-lookup"><span data-stu-id="bdd68-115">In order to encode audio files as ADPCM for use with XAudio2, use the **AdpcmEncode** command-line tool.</span></span>

## <a name="adpcm-decoding"></a><span data-ttu-id="bdd68-116">ADPCM 解碼</span><span class="sxs-lookup"><span data-stu-id="bdd68-116">ADPCM Decoding</span></span>

<span data-ttu-id="bdd68-117">XAudio2 支援 ADPCM 的軟體解碼。</span><span class="sxs-lookup"><span data-stu-id="bdd68-117">Software decoding of ADPCM is supported in XAudio2.</span></span>

-   <span data-ttu-id="bdd68-118">XAudio2</span><span class="sxs-lookup"><span data-stu-id="bdd68-118">XAudio2</span></span>

    <span data-ttu-id="bdd68-119">若要在 XAudio2 中使用 ADPCM 編碼的資料，您必須初始化具有 ADPCM 特定值的 **ADPCMWAVEFORMAT** 結構，並在建立來源語音時，將其當作引數傳遞至 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 。</span><span class="sxs-lookup"><span data-stu-id="bdd68-119">In order to use ADPCM encoded data in XAudio2, you need to initialize a **ADPCMWAVEFORMAT** structure with ADPCM specific values, and pass it as an argument to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) when you create a source voice.</span></span> <span data-ttu-id="bdd68-120">如需在 XAudio2 中載入和播放音效的範例，請參閱 [如何：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)。</span><span class="sxs-lookup"><span data-stu-id="bdd68-120">For an example of loading and playing a sound in XAudio2, see [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md).</span></span>

## <a name="samplesperblock"></a><span data-ttu-id="bdd68-121">SamplesPerBlock</span><span class="sxs-lookup"><span data-stu-id="bdd68-121">SamplesPerBlock</span></span>

<span data-ttu-id="bdd68-122">ADPCM 壓縮的運作方式是將波形分割成區塊，並預測每個區塊內波形取樣的變化。</span><span class="sxs-lookup"><span data-stu-id="bdd68-122">ADPCM compression works by separating the waveform into blocks, and predicting the variation of the waveform samples within each block.</span></span> <span data-ttu-id="bdd68-123">區塊的大小會以範例來測量。</span><span class="sxs-lookup"><span data-stu-id="bdd68-123">The size of the blocks is measured in samples.</span></span> <span data-ttu-id="bdd68-124">最小的區塊大小為32個樣本，最高為512個樣本。</span><span class="sxs-lookup"><span data-stu-id="bdd68-124">The smallest block size is 32 samples, and the highest is 512 samples.</span></span>

<span data-ttu-id="bdd68-125">較大的區塊可提供較佳的壓縮功能，這會產生較小的檔案大小，但代價是要調整迴圈點的音效品質和解析度。</span><span class="sxs-lookup"><span data-stu-id="bdd68-125">Larger blocks allow better compression, which results in smaller file sizes, but at the expense of sound quality and resolution for aligning loop points.</span></span>

<span data-ttu-id="bdd68-126">一般而言，修改 SamplesPerBlock 值會導致這些取捨：</span><span class="sxs-lookup"><span data-stu-id="bdd68-126">In general, modifying the SamplesPerBlock value results in these tradeoffs:</span></span>



| <span data-ttu-id="bdd68-127">如果 SamplesPerBlock .。。</span><span class="sxs-lookup"><span data-stu-id="bdd68-127">If SamplesPerBlock...</span></span>      | <span data-ttu-id="bdd68-128">檔案壓縮</span><span class="sxs-lookup"><span data-stu-id="bdd68-128">File Compression</span></span> | <span data-ttu-id="bdd68-129">音效品質</span><span class="sxs-lookup"><span data-stu-id="bdd68-129">Sound Quality</span></span> | <span data-ttu-id="bdd68-130">迴圈點解析</span><span class="sxs-lookup"><span data-stu-id="bdd68-130">Loop Point Resolution</span></span> |
|----------------------------|------------------|---------------|-----------------------|
| <span data-ttu-id="bdd68-131">將 (增加到最大的 512) </span><span class="sxs-lookup"><span data-stu-id="bdd68-131">Increases (up to max 512)</span></span>  | <span data-ttu-id="bdd68-132">增加</span><span class="sxs-lookup"><span data-stu-id="bdd68-132">Increases</span></span>        | <span data-ttu-id="bdd68-133">減少</span><span class="sxs-lookup"><span data-stu-id="bdd68-133">Decreases</span></span>     | <span data-ttu-id="bdd68-134">減少</span><span class="sxs-lookup"><span data-stu-id="bdd68-134">Decreases</span></span>             |
| <span data-ttu-id="bdd68-135">降低 (到最小的 32) </span><span class="sxs-lookup"><span data-stu-id="bdd68-135">Decreases (down to min 32)</span></span> | <span data-ttu-id="bdd68-136">減少</span><span class="sxs-lookup"><span data-stu-id="bdd68-136">Decreases</span></span>        | <span data-ttu-id="bdd68-137">增加</span><span class="sxs-lookup"><span data-stu-id="bdd68-137">Increases</span></span>     | <span data-ttu-id="bdd68-138">增加</span><span class="sxs-lookup"><span data-stu-id="bdd68-138">Increases</span></span>             |



 

## <a name="restrictions"></a><span data-ttu-id="bdd68-139">限制</span><span class="sxs-lookup"><span data-stu-id="bdd68-139">Restrictions</span></span>

<span data-ttu-id="bdd68-140">由於 ADPCM 會使用彼此對齊的範例區塊，因此以 ADPCM 壓縮的 wave 可能會在結尾處有未完成的部分區塊。</span><span class="sxs-lookup"><span data-stu-id="bdd68-140">Because ADPCM uses sample blocks that are aligned one after the other, a wave compressed with ADPCM may have an unfinished, partial block at its end.</span></span> <span data-ttu-id="bdd68-141">ADPCM 解碼器會針對這個部分區塊的其餘部分產生無回應，讓 wave 無縫地迴圈。</span><span class="sxs-lookup"><span data-stu-id="bdd68-141">The ADPCM decoder generates silence for the remainder of this partial block, which keeps the wave from looping seamlessly.</span></span>

<span data-ttu-id="bdd68-142">*SamplesPerBlock* 參數的值會影響您可以用來對齊 wave 資料和迴圈點的解析度。</span><span class="sxs-lookup"><span data-stu-id="bdd68-142">The value of the *SamplesPerBlock* parameter affects the resolution with which you can align wave data and loop points.</span></span>

<span data-ttu-id="bdd68-143">如果您嘗試將壓縮套用至非對齊的 wave，您將會收到錯誤或警告，取決於是否在任何迴圈播放事件中使用 wave。</span><span class="sxs-lookup"><span data-stu-id="bdd68-143">If you try to apply compression to a non-aligned wave, you will get an error or a warning depending on whether the wave is used in any looping play events.</span></span> <span data-ttu-id="bdd68-144">您無法壓縮任何迴圈播放事件中所使用的 wave。</span><span class="sxs-lookup"><span data-stu-id="bdd68-144">You cannot compress a wave used in any looping play events.</span></span> <span data-ttu-id="bdd68-145">將它從迴圈播放事件中移除，然後重新套用壓縮。</span><span class="sxs-lookup"><span data-stu-id="bdd68-145">Remove it from the looping play events, and re-apply compression.</span></span>

<span data-ttu-id="bdd68-146">如果您在非迴圈模式中以獨佔方式使用 wave，則不適用範例區塊對齊限制。</span><span class="sxs-lookup"><span data-stu-id="bdd68-146">If you use the wave exclusively in non-looping mode, the sample block alignment restriction does not apply.</span></span>

## <a name="adpcm-file-structure"></a><span data-ttu-id="bdd68-147">ADPCM 檔案結構</span><span class="sxs-lookup"><span data-stu-id="bdd68-147">ADPCM File Structure</span></span>

<span data-ttu-id="bdd68-148">ADPCM 檔案是具有下列區塊類型的標準 RIFF 檔。</span><span class="sxs-lookup"><span data-stu-id="bdd68-148">An ADPCM file is a standard RIFF file with the following chunk types.</span></span>



| <span data-ttu-id="bdd68-149">區塊 FCC</span><span class="sxs-lookup"><span data-stu-id="bdd68-149">Chunk FCC</span></span>     | <span data-ttu-id="bdd68-150">Description</span><span class="sxs-lookup"><span data-stu-id="bdd68-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd68-151">RIFF</span><span class="sxs-lookup"><span data-stu-id="bdd68-151">RIFF</span></span>          | <span data-ttu-id="bdd68-152">標準 RIFF 區塊包含檔案類型，其資料區段的前四個位元組中的值為 WAVE，以及其資料區段其餘部分中檔案的其他區塊。</span><span class="sxs-lookup"><span data-stu-id="bdd68-152">Standard RIFF chunk containing a file type with the value WAVE in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="bdd68-153">Fmt</span><span class="sxs-lookup"><span data-stu-id="bdd68-153">fmt</span></span>           | <span data-ttu-id="bdd68-154">包含 ADPCM 檔案的格式標頭。</span><span class="sxs-lookup"><span data-stu-id="bdd68-154">Contains the format header for the ADPCM file.</span></span> <span data-ttu-id="bdd68-155">這個區塊中的資料會對應至 **ADPCMWAVEFORMAT** 結構。</span><span class="sxs-lookup"><span data-stu-id="bdd68-155">The data in this chunk corresponds to a **ADPCMWAVEFORMAT** structure.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="bdd68-156">data</span><span class="sxs-lookup"><span data-stu-id="bdd68-156">data</span></span>          | <span data-ttu-id="bdd68-157">包含編碼的 ADPCM 音訊資料。</span><span class="sxs-lookup"><span data-stu-id="bdd68-157">Contains the encoded ADPCM audio data.</span></span> <span data-ttu-id="bdd68-158">當您在 XAudio2 中使用 ADPCM 時，您需要將資料區塊的內容讀取至緩衝區，並將其傳遞至來源聲音，作為 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **pAudioData** 成員。</span><span class="sxs-lookup"><span data-stu-id="bdd68-158">When you use ADPCM in XAudio2, you need to read the contents of the data chunk into a buffer, and pass it to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="bdd68-159">您不需要位元組交換資料區塊的內容。</span><span class="sxs-lookup"><span data-stu-id="bdd68-159">You don't need to byte swap the contents of the data chunk.</span></span>                                                                                                                            |
| <span data-ttu-id="bdd68-160">smpl 和 wsmp</span><span class="sxs-lookup"><span data-stu-id="bdd68-160">smpl and wsmp</span></span> | <span data-ttu-id="bdd68-161">選用的區塊類型，包含 ADPCM 檔案的迴圈資訊。</span><span class="sxs-lookup"><span data-stu-id="bdd68-161">Optional chunk types containing the looping information for the ADPCM file.</span></span> <span data-ttu-id="bdd68-162">當您在 XAudio2 中使用 ADPCM 時，smpl 或 wsmp 區塊中包含的值會用來填入 [**LoopBeginLoopLength \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **LoopCount** 和 **XAudio2** 成員。</span><span class="sxs-lookup"><span data-stu-id="bdd68-162">When you use ADPCM in XAudio2, the values contained in the smpl or wsmp chunks are used to populate the **LoopBeginLoopLength** and **LoopCount** members of the [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="bdd68-163">在 Xbox 360 上，您必須以位元組交換從 smpl 區塊載入的資料，以考慮 Windows 與 Xbox 360 之間的位元組順序差異。</span><span class="sxs-lookup"><span data-stu-id="bdd68-163">On the Xbox 360, you need to byte swap the data loaded from a smpl chunk to account for the endianness difference between Windows and Xbox 360.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bdd68-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdd68-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdd68-165">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="bdd68-165">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 

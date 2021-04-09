---
title: 使用 High-Resolution PCM 音訊
description: 使用 High-Resolution PCM 音訊
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF) 、高解析度 PCM 音訊
- ASF (Advanced Systems Format) 、高解析度 PCM 音訊
- 設定檔，高解析度 PCM 音訊
- 編解碼器、高解析度 PCM 音訊
- Advanced Systems Format (ASF) 、PCM 音訊
- ASF (Advanced Systems Format) 、PCM 音訊
- 設定檔，PCM 音訊
- 編解碼器、PCM 音訊
- 高解析度 PCM 音訊
- PCM 音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933354"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="cbfdc-113">使用 High-Resolution PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="cbfdc-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="cbfdc-114">Windows Media 音訊 9 Professional 編解碼器和 Windows Media 音訊9無失真編解碼器的一些輸入格式為高解析度 PCM 格式。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="cbfdc-115">這些 PCM 格式有兩個以上的通道，或每個樣本超過16個位 (音訊具有兩個以上的通道，也稱為多頻道音訊) 。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="cbfdc-116">這些格式是使用 [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) 結構的結構化延伸來設定，稱為 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="cbfdc-117">**WAVEFORMATEXTENSIBLE** 結構包含音訊中所含通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="cbfdc-118">使用高解析度 PCM 音訊時需要此結構，因為某些 Windows Api 不會接受包含高解析度值的 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="cbfdc-119">高解析度 PCM 格式有22個位元組的擴充資料，其指定于 **WAVEFORMATEX** 結構的 **cbSize** 成員中。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="cbfdc-120">高解析度的 Windows Media 音訊格式不會使用 **WAVEFORMATEXTENSIBLE** 結構，但會將擴充的資料附加至 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="cbfdc-121">當應用程式在 Windows XP 或更新版本上執行時，Windows Media audio 編解碼器只支援解碼為高解析度 PCM 格式。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="cbfdc-122">在舊版的 Microsoft Windows 上，編解碼器會解碼成格式，每個樣本最多16個位和2個通道。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="cbfdc-123">此外，您必須 \_ 使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)方法，將 g wszEnableDiscreteOutput 輸出設定設為 **TRUE** ，以指定要將編解碼器解碼為高定義 PCM。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="cbfdc-124">進行此呼叫之後，讀取器列舉的輸出會包含高定義格式。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="cbfdc-125">多頻道音訊需要更多設定。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="cbfdc-126">如需詳細資訊，請參閱 [讀取多頻道音訊](reading-multichannel-audio.md)。</span><span class="sxs-lookup"><span data-stu-id="cbfdc-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbfdc-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbfdc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbfdc-128">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="cbfdc-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 
---
description: 音訊功能
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: 音訊功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510293"
---
# <a name="audio-capabilities"></a><span data-ttu-id="f9452-103">音訊功能</span><span class="sxs-lookup"><span data-stu-id="f9452-103">Audio Capabilities</span></span>

<span data-ttu-id="f9452-104">針對音訊功能， [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 會傳回一組 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 和 [**音訊串流設定 \_ \_ \_ cap**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="f9452-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="f9452-105">如同影片，您可以使用這種方式來公開 pin 的所有音訊功能，例如資料速率，以及它是否支援 mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="f9452-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="f9452-106">如需與 GetStreamCaps 相關的影片相關範例，請參閱 [影片功能](video-capabilities.md)。</span><span class="sxs-lookup"><span data-stu-id="f9452-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="f9452-107">假設您支援脈衝程式碼調整 (PCM) wave 格式 (如 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構所表示) 以每秒11025、22050和44100樣本的取樣率，全都以8或16位 mono 或身歷聲表示。</span><span class="sxs-lookup"><span data-stu-id="f9452-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="f9452-108">在此情況下，您會提供兩組結構。</span><span class="sxs-lookup"><span data-stu-id="f9452-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="f9452-109">第一組會有 **音訊 \_ 串流設定 \_ \_ cap** 功能結構，指出您最多可支援每秒11025到22050個樣本，每秒最多可有11025個樣本 (資料細微性是支援值之間的差異) ; 每個樣本最多16位的16位最大位，每個樣本有8位的資料細微性，以及最少一個通道和兩個通道的最大值。</span><span class="sxs-lookup"><span data-stu-id="f9452-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="f9452-110">第一個配對的媒體類型會是您在該範圍內的預設 PCM 格式，可能是22千赫茲 (kHz) 16 位的身歷聲。</span><span class="sxs-lookup"><span data-stu-id="f9452-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="f9452-111">您的第二組是一項功能，顯示每秒最小和最大樣本的 44100;8位 (最小) 和16位 (每個樣本最多) 位，每個樣本的資料細微性為8位;以及最少一個通道和兩個通道。</span><span class="sxs-lookup"><span data-stu-id="f9452-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="f9452-112">媒體類型會是預設的 44 kHz 格式，可能是 44 kHz 16 位的身歷聲。</span><span class="sxs-lookup"><span data-stu-id="f9452-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="f9452-113">如果您支援非 PCM wave 格式，這個方法所傳回的媒體類型可顯示您支援的非 PCM 格式 (預設的取樣率、位元速率和通道) ，以及媒體類型所附的功能結構，可描述您所支援的其他範例速率、位元速率和通道。</span><span class="sxs-lookup"><span data-stu-id="f9452-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9452-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9452-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9452-115">公開捕捉和壓縮格式</span><span class="sxs-lookup"><span data-stu-id="f9452-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 

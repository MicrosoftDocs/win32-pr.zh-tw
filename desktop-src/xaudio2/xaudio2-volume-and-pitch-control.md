---
description: 本主題說明 XAudio2 音量和音調控制。
ms.assetid: dedc2d01-af83-d7d2-5b64-743dcebc83f7
title: XAudio2 音量和音調控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2526cfa50c0260e90e1aae9e2bce21d507dc2e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193693"
---
# <a name="xaudio2-volume-and-pitch-control"></a><span data-ttu-id="eedf8-103">XAudio2 音量和音調控制</span><span class="sxs-lookup"><span data-stu-id="eedf8-103">XAudio2 Volume and Pitch Control</span></span>

<span data-ttu-id="eedf8-104">本主題說明 XAudio2 音量和音調控制。</span><span class="sxs-lookup"><span data-stu-id="eedf8-104">This topic describes XAudio2 volume and pitch control.</span></span>

## <a name="volume-control"></a><span data-ttu-id="eedf8-105">音量控制</span><span class="sxs-lookup"><span data-stu-id="eedf8-105">Volume Control</span></span>

<span data-ttu-id="eedf8-106">磁片區層級會表示為-XAUDIO2 \_ max \_ 磁片區 \_ 層級與 XAUDIO2 max 磁片區層級之間的浮點振幅， \_ \_ \_ (-224 到 224) ，最大增益為 144.5 dB。</span><span class="sxs-lookup"><span data-stu-id="eedf8-106">Volume levels are expressed as floating-point amplitude multipliers between -XAUDIO2\_MAX\_VOLUME\_LEVEL and XAUDIO2\_MAX\_VOLUME\_LEVEL (-224 to 224), with a maximum gain of 144.5 dB.</span></span> <span data-ttu-id="eedf8-107">磁片區1.0 表示沒有衰減或增益;0表示無聲;和負數層級可以用來將音訊的階段反轉。</span><span class="sxs-lookup"><span data-stu-id="eedf8-107">A volume of 1.0 means there is no attenuation or gain; 0 means silence; and negative levels can be used to invert the audio's phase.</span></span> <span data-ttu-id="eedf8-108">XAudio2 中提供兩個內嵌函數以在磁片區單位之間轉換： [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) 和 [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)。</span><span class="sxs-lookup"><span data-stu-id="eedf8-108">Two inline functions are provided in XAudio2.h to convert between volume units: [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio) and [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels).</span></span>

<span data-ttu-id="eedf8-109">當音訊流經 XAudio2 圖時，您可以在數個點將磁片區層級套用至音訊：</span><span class="sxs-lookup"><span data-stu-id="eedf8-109">You can apply a volume level to the audio at several points as it flows through the XAudio2 graph:</span></span>

-   <span data-ttu-id="eedf8-110">所有語音類型都會將整體磁片區層級套用至其輸入，其會使用 [**IXAudio2Voice：： SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 方法來控制。</span><span class="sxs-lookup"><span data-stu-id="eedf8-110">All voice types apply an overall volume level to their input, which they control using the [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) method.</span></span> <span data-ttu-id="eedf8-111">在 submix 和掌控語音中，整體音量層級會在語音的內建篩選和效果鏈之前套用。</span><span class="sxs-lookup"><span data-stu-id="eedf8-111">In submix and mastering voices, the overall volume level is applied just before the voice's built-in filter and effect chain.</span></span> <span data-ttu-id="eedf8-112">在來源語音中，整體音量層級會在語音的內建篩選和效果鏈之後套用。</span><span class="sxs-lookup"><span data-stu-id="eedf8-112">In source voices, the overall volume level is applied after the voice's built-in filter and effect chain.</span></span>
-   <span data-ttu-id="eedf8-113">語音會將每個通道的磁片區層級套用至其輸出，其會使用 [**IXAudio2Voice：： SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) 方法來控制它們。</span><span class="sxs-lookup"><span data-stu-id="eedf8-113">Voices apply a per-channel volume level to their output, which they control using the [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) method.</span></span> <span data-ttu-id="eedf8-114">每個頻道的音量層級會在語音的最終取樣率轉換之後，以及傳送到其他語音之前套用。</span><span class="sxs-lookup"><span data-stu-id="eedf8-114">The per-channel volume level is applied just after the voice's final sample rate conversion, and before it is sent to other voices.</span></span>
-   <span data-ttu-id="eedf8-115">每個語音之間的每個連線都有一份層級表格，可用來從每個來源頻道將音訊傳送至每個目標通道（使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 方法來控制）。</span><span class="sxs-lookup"><span data-stu-id="eedf8-115">Every connection between one voice and another has a table of levels used to send audio from each source channel to each target channel, which is controlled using the [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) method.</span></span>

<span data-ttu-id="eedf8-116">所有的整體磁片區和通道磁片區一開始都會預設為1.0。</span><span class="sxs-lookup"><span data-stu-id="eedf8-116">All overall volumes and channel volumes default to 1.0 initially.</span></span> <span data-ttu-id="eedf8-117">所有的傳送層級矩陣都會預設為適當的值，以盡可能精確地保留信號電源和通道定位。</span><span class="sxs-lookup"><span data-stu-id="eedf8-117">All send-level matrices default to appropriate values that preserve signal power and channel positioning as accurately as possible.</span></span> <span data-ttu-id="eedf8-118">如需詳細資訊，請參閱 [XAudio2 預設通道對應](xaudio2-default-channel-mapping.md) 總覽。</span><span class="sxs-lookup"><span data-stu-id="eedf8-118">See the [XAudio2 Default Channel Mapping](xaudio2-default-channel-mapping.md) overview for details.</span></span>

> [!Note]  
> <span data-ttu-id="eedf8-119">XAudio2 會根據使用者的說話者設定自動調整音量層級，以維持一致的磁片區層級之間的設定。</span><span class="sxs-lookup"><span data-stu-id="eedf8-119">XAudio2 automatically adjusts volume levels based on the user's speaker settings to maintain a consistent volume level across configurations.</span></span> <span data-ttu-id="eedf8-120">如果使用者的設定不符合其實體設定，則磁片區會太遠或太過軟，相較于具有正確設定的系統。</span><span class="sxs-lookup"><span data-stu-id="eedf8-120">If the user's settings don't match their physical configuration the volume will either be too loud or too soft compared to a system with accurate settings.</span></span> <span data-ttu-id="eedf8-121">例如，針對5.1 設定的系統會將只有兩個喇叭連線的音效喇叭設為不太軟。</span><span class="sxs-lookup"><span data-stu-id="eedf8-121">For example, a system configured for 5.1 surround sound speakers that only has two speakers connected will sound too soft.</span></span> <span data-ttu-id="eedf8-122">XAudio2 無法偵測使用者說話者設定是否正確地符合其實體安裝。</span><span class="sxs-lookup"><span data-stu-id="eedf8-122">XAudio2 is unable to detect whether the user speaker settings correctly match their physical setup.</span></span>

 

## <a name="pitch-control"></a><span data-ttu-id="eedf8-123">音調控制項</span><span class="sxs-lookup"><span data-stu-id="eedf8-123">Pitch Control</span></span>

<span data-ttu-id="eedf8-124">簡報會表示為輸入速率/輸出速率比例，介於 1/1024 與 1024/1 （含）之間。</span><span class="sxs-lookup"><span data-stu-id="eedf8-124">Pitches are expressed as input rate/output rate ratios between 1/1,024 and 1,024/1, inclusive.</span></span> <span data-ttu-id="eedf8-125">1/1024 的比率會減少 10 octaves，而 1024/1 的比率則會引發 10 octaves。</span><span class="sxs-lookup"><span data-stu-id="eedf8-125">A ratio of 1/1,024 lowers pitch by 10 octaves, while a ratio of 1,024/1 raises it by 10 octaves.</span></span> <span data-ttu-id="eedf8-126">您只能使用 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 方法，將音調調整套用至來源語音，而且只有在不是使用 XAUDIO2 \_ VOICE NOPITCH 旗標建立時 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eedf8-126">You can only use the [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) method to apply pitch adjustments to source voices, and only if they were not created with the XAUDIO2\_VOICE\_NOPITCH flag.</span></span> <span data-ttu-id="eedf8-127">預設頻率比例為1/1：也就是不會有任何間距變更。</span><span class="sxs-lookup"><span data-stu-id="eedf8-127">The default frequency ratio is 1/1: that is, no pitch change.</span></span> <span data-ttu-id="eedf8-128">XAudio2 中提供兩個內嵌函式，以便在頻率比例和 semitones： [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) 和 [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="eedf8-128">Two inline functions are provided in XAudio2.h to convert between frequency ratios and semitones: [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones) and [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eedf8-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="eedf8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eedf8-130">音量和音調控制項</span><span class="sxs-lookup"><span data-stu-id="eedf8-130">Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> <dt>

[<span data-ttu-id="eedf8-131">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="eedf8-131">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="eedf8-132">如何：變更聲音音調</span><span class="sxs-lookup"><span data-stu-id="eedf8-132">How to: Change Voice Pitch</span></span>](how-to--change-voice-pitch.md)
</dt> <dt>

[<span data-ttu-id="eedf8-133">如何：變更聲音音量</span><span class="sxs-lookup"><span data-stu-id="eedf8-133">How to: Change Voice Volume</span></span>](how-to--change-voice-volume.md)
</dt> </dl>

 

 

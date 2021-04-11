---
description: 本主題說明如何將效果鏈套用至語音，以允許自訂該聲音音訊資料的處理。 本主題說明如何使用「回音」效果，這是其中一個內建的 XAudio2 效果。
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 使用方法：建立效果鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113653"
---
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="32f32-104">使用方法：建立效果鏈</span><span class="sxs-lookup"><span data-stu-id="32f32-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="32f32-105">本主題說明如何將效果鏈套用至語音，以允許自訂該聲音音訊資料的處理。</span><span class="sxs-lookup"><span data-stu-id="32f32-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="32f32-106">本主題說明如何使用「回音」效果，這是其中一個內建的 XAudio2 效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="32f32-107">建立將效果套用至語音的基本效果鏈</span><span class="sxs-lookup"><span data-stu-id="32f32-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="32f32-108">建立效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-108">Create the effect.</span></span>

    <span data-ttu-id="32f32-109">在此範例中， [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) 函數會建立一個回音效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="32f32-110">請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) ，以取得搭配 XAudio2 使用之可能效果來源的清單。</span><span class="sxs-lookup"><span data-stu-id="32f32-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="32f32-111">以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。</span><span class="sxs-lookup"><span data-stu-id="32f32-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="32f32-112">如果鏈中有多個效果，則每個效果都需要 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 元結構。</span><span class="sxs-lookup"><span data-stu-id="32f32-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="32f32-113">以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。</span><span class="sxs-lookup"><span data-stu-id="32f32-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="32f32-114">在此情況下，鏈只會有一個效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="32f32-115">如果鏈有一個以上的效果，EffectCount 成員會包含效果的計數，而 pEffectDescriptors 成員將指向 XAUDIO2 \_ 效果描述元結構的陣列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="32f32-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="32f32-116">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 函式將效果鏈套用至語音。</span><span class="sxs-lookup"><span data-stu-id="32f32-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="32f32-117">您可以將效果鏈套用至主要語音、來源語音和 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="32f32-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="32f32-118">使用 IUnknown：： Release 來釋放效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="32f32-119">當您建立 XAPO 時，它的參考計數會是1。</span><span class="sxs-lookup"><span data-stu-id="32f32-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="32f32-120">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="32f32-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="32f32-121">釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="32f32-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="32f32-122">如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用它時，它就會被處置。</span><span class="sxs-lookup"><span data-stu-id="32f32-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="32f32-123">如果用戶端程式代碼需要維護 XAPO 的參考，例如為了稍後重複使用，您應該略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="32f32-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="32f32-124">填入與效果相關聯的參數結構（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="32f32-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="32f32-125">「回音」效果使用 [**XAUDIO2FX 的「 \_ 回音」 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) 結構。</span><span class="sxs-lookup"><span data-stu-id="32f32-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  <span data-ttu-id="32f32-126">在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="32f32-127">如果適合，請停用或啟用效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="32f32-128">您可以隨時使用 [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) 來關閉效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="32f32-129">您可以使用 [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)再次開啟效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="32f32-130">[**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)和 [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)的參數會指定要啟用或停用鏈中的效果。</span><span class="sxs-lookup"><span data-stu-id="32f32-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32f32-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="32f32-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32f32-132">音訊效果</span><span class="sxs-lookup"><span data-stu-id="32f32-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="32f32-133">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="32f32-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="32f32-134">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="32f32-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="32f32-135">XAPO 概觀</span><span class="sxs-lookup"><span data-stu-id="32f32-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="32f32-136">如何：在 XAudio2 中使用 XAOPFX</span><span class="sxs-lookup"><span data-stu-id="32f32-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="32f32-137">如何：在 XAudio2 中使用 XAOP</span><span class="sxs-lookup"><span data-stu-id="32f32-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 

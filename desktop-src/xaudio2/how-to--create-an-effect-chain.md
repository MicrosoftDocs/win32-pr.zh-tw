---
description: 本主題說明如何將效果鏈套用至語音，以允許自訂該聲音音訊資料的處理。 本主題說明如何使用「回音」效果，這是其中一個內建的 XAudio2 效果。
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 使用方法：建立效果鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abd6372fe07f71d75a4963f6617cdeda15ecf8390e3142fcf110029bd8f6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838410"
---
# <a name="how-to-create-an-effect-chain"></a>使用方法：建立效果鏈

本主題說明如何將效果鏈套用至語音，以允許自訂該聲音音訊資料的處理。 本主題說明如何使用「回音」效果，這是其中一個內建的 XAudio2 效果。

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>建立將效果套用至語音的基本效果鏈

1.  建立效果。

    在此範例中， [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) 函數會建立一個回音效果。 請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) ，以取得搭配 XAudio2 使用之可能效果來源的清單。

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。

    如果鏈中有多個效果，則每個效果都需要 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 元結構。

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。 在此情況下，鏈只會有一個效果。 如果鏈有一個以上的效果，EffectCount 成員會包含效果的計數，而 pEffectDescriptors 成員將指向 XAUDIO2 \_ 效果描述元結構的陣列 \_ 。

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 函式將效果鏈套用至語音。

    您可以將效果鏈套用至主要語音、來源語音和 submix 語音。

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  使用 IUnknown：： Release 來釋放效果。

    當您建立 XAPO 時，它的參考計數會是1。 使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。 釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。 如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用它時，它就會被處置。 如果用戶端程式代碼需要維護 XAPO 的參考，例如為了稍後重複使用，您應該略過此步驟。

    ```
    pXAPO->Release();
    ```

    

6.  填入與效果相關聯的參數結構（如果有的話）。 「回音」效果使用 [**XAUDIO2FX 的「 \_ 回音」 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) 結構。

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

    

7.  在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  如果適合，請停用或啟用效果。

    您可以隨時使用 [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) 來關閉效果。

    ```
    pVoice->DisableEffect(0);
    ```

    

    您可以使用 [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)再次開啟效果。

    ```
    pVoice->EnableEffect(0);
    ```

    

    [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)和 [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)的參數會指定要啟用或停用鏈中的效果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAPO 概觀](xapo-overview.md)
</dt> <dt>

[如何：在 XAudio2 中使用 XAOPFX](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[如何：在 XAudio2 中使用 XAOP](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 

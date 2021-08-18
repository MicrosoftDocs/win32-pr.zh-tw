---
description: 本主題說明如何整合 X3DAudio 與 XAudio2。
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 使用方法：整合 X3DAudio 與 XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c940acbe78e8d4ca4247f77500adeeca7c9619057a3008dea50fc8b55a9f364e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962687"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>使用方法：整合 X3DAudio 與 XAudio2

本主題說明如何整合 X3DAudio 與 XAudio2。 您可以使用 X3DAudio 來提供 XAudio2 聲音的音量和音調值，以及 XAudio2 內建的回音效果參數。 本主題假設您已依照[如何：建立基本音訊處理 Graph](how-to--build-a-basic-audio-processing-graph.md)中所述，建立音訊圖表。 如果您尚未建立音訊圖形， [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) 將會失敗。

**若要初始化 X3DAudio**

1.  藉由呼叫 [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)來初始化 X3DAudio。

    [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)函式會接受旗標，指出喇叭設定、使用者定義的世界單位中的音效速度，以及傳回 X3DAudio 引擎實例的控制碼。 呼叫 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) 以取得輸出格式的通道遮罩。

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  建立 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構的實例。

    [**X3DAUDIO 接聽 \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)程式結構代表聽聽音效的位置。 一般來說，這是相機的位置或接近的位置。 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)結構代表製作音效的位置。 每個要追蹤的音效都會有一個 **X3DAUDIO 的 \_ 發射器** 結構。

    將不會在遊戲迴圈中更新之結構的成員應在此初始化。 結構的大部分成員都可以直接初始化為零。 不過， [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 的某些成員必須設定為初始化為非零值。 **X3DAUDIO \_ 發射器** 的 ChannelCount 成員必須初始化為發射器所代表之聲音中的通道數目。 此外， **X3DAUDIO \_ 發射器** 的 CurveDistanceScaler 成員必須在 FLT \_ MIN 到 FLT MAX 的範圍內 \_ 。

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  建立 [**X3DAUDIO \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) 結構的實例。

    [**X3DAUDIO 的 \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)結構是用來傳回 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)所計算的結果。 **X3DAudioCalculate** 函式不會為其任何參數配置記憶體。 這表示，如果您想要使用 **X3DAUDIO \_ DSP \_ 設定** 結構的 pMatrixCoefficients 和 pDelayTimes 成員，您必須為這些成員配置陣列。 此外，您還需要將 SrcChannelCount 和 DstChannelCount 成員設定為發射器的來源和目的地語音中的通道數目。

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > 在「控制」聲音上使用 [**IXAudio2Voice：： GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) ，以取得 **nChannels** 的 InputChannels 數目。 針對 XAUDIO2 Windows 8 之前的 DirectX SDK 版本，請使用 IXAudio2：： GetDeviceDetails。

     

每兩到三個框架執行這些步驟一次，以計算新的設定並加以套用。 在此範例中，來源語音會直接傳送至「控制」語音，並傳送至 submix 的語音，並套用「回音」效果。

**使用 X3DAudio 來計算及套用新的3D 音訊設定**

1.  以目前的位置、速度和方向，更新 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構。

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  呼叫 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) 來計算語音的新設定。

    [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)的參數將會是已更新的 X3DAUDIO 接聽程式和 [**X3DAUDIO 的 \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)結構。 [**\_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 旗標會指出 **X3DAudioCalculate** 應該計算的值，以及哪個 [**X3DAUDIO 的 \_ DSP \_ 設定**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) 結構會保存所執行計算的結果。

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 和 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 將磁片區和音調值套用至來源聲音。

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  您可以使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 將計算的回音等級套用至 submix 語音。

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  使用 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) 將計算出的低通過篩選準則直接係數套用至來源聲音。

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[X3DAudio 總覽](x3daudio-overview.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[XAudio2 音量和音調控制](volume-and-pitch-control.md)
</dt> </dl>

 

 

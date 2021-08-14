---
description: 本主題說明如何使用 XAudio2 效果鏈中 XAPOFX 所包含的其中一個效果。
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 使用方法：在 XAudio2 中使用 XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618e508d5e023c29c373193aa38da9d0e7f9f76c94a57f63e50df0c346426b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696149"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>使用方法：在 XAudio2 中使用 XAPOFX

本主題說明如何使用 XAudio2 效果鏈中 XAPOFX 所包含的其中一個效果。

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>在 XAudio2 效果鏈中使用 XAPOFX 的效果

1.  將 XAPOFX 效果的 CLSID 傳遞給 [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 函數，以建立效果。

    在此情況下，會建立簡化的「FXReverb」效果。

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 功能將效果鏈套用至 XAudio2 聲音。

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > 當您以參數的形式傳遞 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)、 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)或 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)時，您也可以在建立語音時將效果鏈套用至語音。

     

5.  使用 IUnknown：： Release 來釋放效果。 當您建立 XAPO 時，它的參考計數會是1。 使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。 釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。 如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用此參考時，就會處置此參考。 如果用戶端程式代碼需要維護 XAPO 的參考（例如，稍後重複使用），您可以略過此步驟。

    ```
    pXAPO->Release();
    ```

    

6.  填入與效果相關聯的參數結構（如果有的話）。

    在此情況下， [**FXREVERB \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) 結構是用來設定應該使用的擴散和空間大小。

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 

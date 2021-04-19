---
description: 本主題說明如何在 XAudio2 效果鏈中使用以 XAPO API 建立的效果。
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 使用方法：在 XAudio2 中使用 XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981427"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>使用方法：在 XAudio2 中使用 XAPO

本主題說明如何在 XAudio2 效果鏈中使用以 XAPO API 建立的效果。

1.  建立 XAPO，如 [如何：建立 XAPO](how-to--create-an-xapo.md)中所述。

    您也可以依照 [如何：將執行時間參數支援加入至 XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md)中所述，來執行執行時間參數功能。

2.  建立 XAPO 的實例。

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 功能將效果鏈套用至 XAudio2 聲音。

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > 藉由將鏈作為參數傳遞給 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)、 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)或 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)，也可以在建立語音時，將效果鏈套用至語音。

     

6.  使用 IUnknown：： Release 來釋放效果。

    當您建立 XAPO 時，它的參考計數會是1。 使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。 釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。 如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用它時，它就會被處置。 例如，如果用戶端程式代碼需要維護 XAPO 的參考，以供稍後重複使用，則您應該略過此步驟。

    ```
    pXAPO->Release();
    ```

    

7.  填入與效果相關聯的參數結構（如果有的話）。 在此情況下，應套用效果的完整強度百分比。

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAPO 概觀](xapo-overview.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 

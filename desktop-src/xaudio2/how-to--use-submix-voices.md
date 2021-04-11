---
description: 本主題說明如何設定語音群組，以將其輸出傳送至相同的 submix 語音。 這可讓 submix 語音的單一變更影響整個語音群組。
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 使用方法：使用次混音聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193534"
---
# <a name="how-to-use-submix-voices"></a>使用方法：使用次混音聲音

本主題說明如何設定語音群組，以將其輸出傳送至相同的 submix 語音。 這可讓 submix 語音的單一變更影響整個語音群組。

1.  建立 [**submix 聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) ，讓所有遊戲的音效效果都能傳送。
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  建立 [**XAUDIO2 \_ voice \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) 傳送結構，其中包含 submix 聲音的參考。
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  將 [**XAUDIO2 \_ VOICE \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) 傳送結構傳遞給新的來源語音。
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  藉由調整 submix 聲音，將變更套用至所有音效效果的聲音。

    在此範例中，使用 [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 函式來變更 submix 聲音的音量，實際上會變更輸出的所有語音音量。

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[語音](voices.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 

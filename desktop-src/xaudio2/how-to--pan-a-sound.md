---
description: 本主題將說明如何設定 mono 來源聲音的輸出矩陣，輸出到身歷聲主控聲音，以達成左右喇叭之間的移動。
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 如何：平移音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850367"
---
# <a name="how-to-pan-a-sound"></a>如何：平移音效

本主題將說明如何設定 mono 來源聲音的輸出矩陣，輸出到身歷聲主控聲音，以達成左右喇叭之間的移動。

## <a name="to-setup-panning"></a>設定移動流覽

1.  使用 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)取得說話者設定。

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  建立陣列來保存輸出矩陣。 輸出矩陣的最小大小是來源語音中的通道數目乘以輸出聲音中的聲道數目。 在此情況下，八個元素陣列將會處理 mono 聲音輸出到任何輸出格式，最高可達7.1 的環繞音效。

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  根據左邊和右邊喇叭之間的所需移動來計算傳送層級。 在此範例中，平移值的範圍從-1 到1，-1 表示左方喇叭的所有音效，而1表示右邊喇叭的所有音效。

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  使用上一個步驟中所計算的值，設定對應至左邊和右邊喇叭的輸出矩陣索引。 左邊和右邊的喇叭是藉由查看 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)所傳回的通道遮罩來決定。 由於通道必須一律以 [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) 參考頁面上指定的順序進行編碼，因此可以判斷對應至個別說話者的陣列索引。

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)將輸出矩陣套用至原始語音。 原始的聲音將會是傳送至 submix 語音或精通聲音的來源語音或 submix 聲音。 您可以使用 [**IXAudio2Voice：： GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails)，取得有關來源和目的地聲音的資訊，例如通道數目。

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 音量和音調控制](volume-and-pitch-control.md)
</dt> </dl>

 

 

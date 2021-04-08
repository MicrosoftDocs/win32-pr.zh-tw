---
description: 本主題說明如何在整體層級、每個輸出頻道，或在聲音的每個通道與 sendlist 中的另一個聲音之間變更聲音的音量。
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 如何：變更聲音音量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693771"
---
# <a name="how-to-change-voice-volume"></a>如何：變更聲音音量

本主題說明如何在整體層級、每個輸出頻道，或在聲音的每個通道與 [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)中的另一個聲音之間變更聲音的音量。

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>設定語音輸入的整體音量層級

-   使用 [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) 函數。

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>設定語音輸出通道的音量

1.  建立浮點數的陣列，其中包含語音中所有輸出通道所需的磁片區。

    陣列中的每個通道都會有一個專案。

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  您可以使用 [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) 函數來設定輸出通道的音量。

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>設定連接的數量

在語音和語音之間的 [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)中設定連接量。

1.  建立浮點數的陣列，以定義輸出矩陣（如果語音傳送至另一個聲音）。

    > [!Note]  
    > 陣列的專案數目必須等於來源語音通道×目的地語音訊道。 在此範例中，對應是從具有一個通道的語音，到具有兩個通道的聲音。

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  您可以使用 [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 函數來設定輸出矩陣。

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 音量和音調控制](volume-and-pitch-control.md)
</dt> </dl>

 

 

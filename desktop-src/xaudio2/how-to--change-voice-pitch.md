---
description: 本主題說明如何使用來源語音上的 SetFrequencyRatio 函式變更播放速率來提高或降低音訊資料的音調。
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 如何：變更聲音音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926468"
---
# <a name="how-to-change-voice-pitch"></a>如何：變更聲音音調

本主題說明如何使用來源語音上的 [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 函式變更播放速率來提高或降低音訊資料的音調。

## <a name="to-change-the-pitch-of-a-source-voice"></a>變更來源聲音的音調

1.  判斷 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)所需的頻率比例。

    如需計算頻率比例的詳細資訊，請參閱 [XAudio2 音量和音調控制](xaudio2-volume-and-pitch-control.md) 。

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  使用 [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 函式來設定來源聲音的頻率比例。

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 音量和音調控制](volume-and-pitch-control.md)
</dt> </dl>

 

 

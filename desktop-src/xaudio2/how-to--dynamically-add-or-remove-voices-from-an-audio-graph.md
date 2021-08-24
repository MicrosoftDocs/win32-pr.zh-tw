---
description: 您可以隨時變更音訊圖形，以新增或移除語音或整個 subgraphs。
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 使用方法：從音訊圖形動態新增或移除聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a49cfc88e89884b63484b7bd58f7f5d96020cd21f8d1147794b840f00258fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082932"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a>使用方法：從音訊圖形動態新增或移除聲音

您可以隨時變更音訊圖形，以新增或移除語音或整個 subgraphs。 本主題說明如何根據[如何：建立基本音訊處理 Graph](how-to--build-a-basic-audio-processing-graph.md)中的步驟，在建立的圖形中新增或移除 submix 語音。 單一語音可以將其輸出傳送到數個聲音或一環長的聲音。 移除或新增單一聲音可能會對音訊圖形產生很大的影響。

## <a name="to-dynamically-change-an-audio-graph"></a>動態變更音訊圖形

從音訊圖形新增和移除語音，與從單一連結清單或圖形新增或移除節點非常類似。

-   將語音或性子圖形新增至音訊圖形

    使用 [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) 函式將圖形中的聲音輸出（父語音）設定為要新增的聲音。 將新聲音的輸出設定為父系聲音的原始子系。

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   移除音訊圖形中的聲音或性子圖形

    將正在移除的聲音父系的輸出聲音設定為已移除的聲音子系。 如果要移除的聲音是在圖形的結尾，則應該將父系聲音變更為指向主要語音。

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

請注意，為了清楚起見，每個父系在這些範例中只有一個子系。 如果父節點有多個子節點，它的 sendlist 會包含一組語音，而不是只包含一個語音的指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊圖形](audio-graphs.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[使用方法：使用次混音聲音](how-to--use-submix-voices.md)
</dt> <dt>

[使用方法：建立效果鏈](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 

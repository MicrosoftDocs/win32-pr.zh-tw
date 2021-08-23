---
description: 使用 Windows Media 音訊語音編解碼器
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: 使用 Windows Media 音訊語音編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e53c84a6915b8bc118015f1524e5126085e7ac199cc4726c88739b0a82738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972667"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>使用 Windows Media 音訊語音編解碼器

Windows Media 音訊語音編解碼器可針對包含語音的音訊提供較低的位元速率壓縮。 編解碼器產生這類小型範例的能力，是因為人類聲音的音效範圍有限。 這種優化表示專用的語音編碼器會針對包含更複雜聲音的內容（例如音樂）建立品質不良的輸出。 不過，Windows Media 音訊語音編解碼器會針對語音、音樂和混合內容提供不同的模式，以彌補此潛在品質問題。 編解碼器會分析混合的內容，以決定要針對檔案的每個部分使用哪一個模式。

Windows Media 音訊語音編解碼器會在類別識別碼 clsid CWMSPEncMediaObject2 所識別的編碼器物件中執行 \_ ，並在類別識別碼 clsid CWMSPDecMediaObject 所識別的解碼器物件中執行 \_ 。 使用此編解碼器之媒體類型的格式標記為0x00A。

## <a name="configuring-the-encoder"></a>設定編碼器

語音編碼器支援三種模式：語音、音樂和混合。 每個模式都經過優化，以取得該內容類型的最佳結果。 您可以使用 **IPropertyStore** 的方法設定 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性，設定語音編碼器的模式。

針對混合內容設定時，Windows Media 音訊的語音編解碼器會自動偵測內容中的音樂段落。 如果您對結果不滿意，您可以使用編輯決策清單 (EDL) ，在內容中指定音樂的位置。 如需詳細資訊，請參閱 [使用編碼語音的編輯決策清單](usingavoiceeditingdecisionlist.md)。

不同于其他音訊編碼器，您可以使用 [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) 屬性來設定語音內容的緩衝區視窗值。 不過，在大部分情況下，預設值應該會正常運作。

> [!Note]  
>    設定語音編碼器時，請務必先設定輸出類型，然後再設定輸入類型。 這是建議的所有音訊編解碼器作業順序，但如果在您呼叫 **IMediaObject：： GetOutputType** 或 **IMFTransform：： GetOutputType** 時設定輸入，則語音編碼器可以報告錯誤的輸出類型。

 

## <a name="decoding"></a>解碼

解碼語音音訊沒有特殊需求。 如需詳細資訊，請參閱設定 [音訊解碼](configuringaudiodecoding.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用音訊](workingwithaudio.md)
</dt> </dl>

 

 




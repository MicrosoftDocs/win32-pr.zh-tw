---
description: 有三種類型的 XAudio2 語音物件：來源、submix 和主控語音。
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: XAudio2 聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b756033be5b64dbf03e3b3756902014774a53c9aebc8f41a1df1f982685cca16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025936"
---
# <a name="xaudio2-voices"></a>XAudio2 聲音

有三種類型的 XAudio2 語音物件： *來源*、 *submix* 和 *主控* 語音。 來源聲音在用戶端提供的音訊資料上操作。 來源和次混音聲音會將它們的輸出傳送到一或多個次混音或主播放聲音。 次混音和主播放聲音會將傳入的所有聲音的音訊混合在一起，然後在結果上操作。 主播放聲音會將音訊資料寫入音訊裝置。

## <a name="actions-performed-by-all-voices"></a>所有語音執行的動作

所有語音都會在移動時的音訊上依序執行下列動作。

1.  整體磁片區調整，會影響所有音訊頻道。 請參閱 [**IXAudio2Voice：： SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)。
2.  一或多個 DSP 效果的選擇性用戶端指定鏈，例如內建的回音或 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面所定義的使用者效果。 請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md)。
3.  每個通道的輸出磁片區調整。 請參閱 [**IXAudio2Voice：： SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)。
4.  將矩陣混合到每個目的地語音或音訊輸出裝置，以取得語音。 此混合會視需要變更音訊中的通道數目。

## <a name="source-voices"></a>來源語音

使用來源語音將音訊資料提交至 XAudio2 處理管線。 它們是[XAudio2 音訊 Graph](xaudio2-audio-graph.md)的進入點。 您必須直接或透過中繼 submix 語音，將語音資料傳送給要聽到的主控聲音。

除了所有語音執行的動作之外，來源語音也會執行下列動作。

-   必要時，會先執行一個解碼，將編碼的來源資料轉換成脈衝程式碼， (PCM) 。
-   可變速率的取樣率轉換 (SRC) 將語音的來源音訊資料轉換為目的地語音預期的取樣率（如有必要），也支援動態的音調變更。
-   您可以使用選擇性的狀態變數篩選器，以各種方式將音效色彩。 請參閱 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)。
-   選擇性篩選準則可以套用至語音的輸出。 請參閱 [**IXAudio2Voice：： SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)。

## <a name="submix-voices"></a>Submix 語音

Submix 語音主要用於效能改進和效果處理。 您無法將資料緩衝區直接提交至 submix 語音。 除非您將它提交給「主控」聲音，否則它將不會有任何聲音。 您可以使用 submix 語音來確保一組特定的語音資料會轉換成相同的格式，並在集體結果上處理特定的效果鏈。

除了所有語音執行的動作之外，submix 語音也會執行下列動作。

-   如果有需要，固定速率的 SRC 會在聲音的輸出上執行，以將音訊轉換為目的地語音預期的取樣率。
-   您可以使用選擇性的狀態變數篩選器，以各種方式將音效色彩。 請參閱 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)。
-   選擇性篩選準則可以套用至語音的輸出。 請參閱 [**IXAudio2Voice：： SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters)。

## <a name="mastering-voices"></a>主控語音

使用主控語音來代表音訊輸出裝置。 您無法直接提交資料緩衝區來掌控聲音，但提交給其他類型語音的資料必須移至要聽到的主控聲音。

除了所有語音執行的動作之外，主控語音也會執行下列動作。

-   如果您使用音訊裝置不支援的明確 *InputSampleRate* 值來建立主控語音，則會使用固定速率的 SRC 來轉換成裝置所支援的最接近取樣率。
-   如果輸出裝置需要，請裁剪最終輸出音訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[語音](voices.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 

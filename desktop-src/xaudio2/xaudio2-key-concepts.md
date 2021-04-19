---
description: 本總覽介紹一些使用 XAudio2 的重要概念。
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: XAudio2 重要概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990436"
---
# <a name="xaudio2-key-concepts"></a>XAudio2 重要概念

本總覽介紹一些使用 XAudio2 的重要概念。

-   [XAudio2 引擎](#xaudio2-engine)
-   [語音](#voices)
-   [音訊圖形](#audio-graph)
-   [回撥](#callbacks)
-   [相關主題](#related-topics)

## <a name="xaudio2-engine"></a>XAudio2 引擎

[**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面是 XAudio2 引擎的核心。 建立 **IXAudio2** 介面的實例，可讓用戶端列舉可用的音訊裝置、設定全域 API 屬性、建立語音，以及監視效能。 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper 函式會針對 XAudio2 執行具現化和初始作業。

您可以在單一進程內多次建立 XAudio2 的實例。 每個 XAudio2 物件會獨立運作，而且有自己的音訊處理執行緒。 只有 debug 設定是共用的。 這在 Windows 上很重要，因為在單一進程中可以載入數個不同的元件。 例如，Internet Explorer 可能會同時使用多個 XAudio2 元件。 雖然可以在單一用戶端應用程式內建立多個 XAudio2 引擎物件，但您不應該在其各自的圖形之間傳遞資訊。

如需初始化 XAudio2 引擎的範例，請參閱 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)。

## <a name="voices"></a>語音

語音是 XAudio2 用來處理、操作及播放音訊資料的物件。 XAudio2 中有三種類型的語音。

-   [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    來源語音代表音訊資料的資料流程。 來源語音會將其資料傳送至其他類型的語音。

-   [**Submix 語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    Submix 語音會對其所接收的音訊資料執行某些操作。 音訊資料操作的其中一個範例可能是取樣率轉換。 在 submix 聲音處理資料之後，它會將該資料傳遞給另一個 submix 聲音或主要語音。

-   [**主控語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    「掌控語音」會從來源語音和 submix 語音接收資料，並將該資料傳送到音訊硬體。

如需 XAudio2 聲音的總覽，請參閱 [XAudio2 語音](voices.md) 。

## <a name="audio-graph"></a>音訊圖形

音訊圖形是一組 XAudio2 語音。 音訊會以來源語音中音訊圖表的一端開始，選擇性地通過一或多個 submix 語音，並以精通聲音結束。 音訊圖形會包含每個目前播放的音效、零個或更多的 submix 語音，以及一個主控聲音的來源聲音。 最簡單的音訊圖形，以及在 XAudio2 中發出雜訊所需的最小值，都是單一來源語音，直接輸出至主控語音。 請參閱 [如何：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md) ，以取得使用 XAudio2 播放音效所需的最少步驟範例。

如需 XAudio2 音訊圖表的總覽，請參閱 [XAudio2 音訊圖形](audio-graphs.md) 。

## <a name="callbacks"></a>回撥

回呼是 XAudio2 用來信號用戶端程式代碼的機制，也就是某個事件發生在聲音或引擎物件中。 由於音訊播放在 XAudio2 引擎中是非同步，因此回呼提供唯一的方法來判斷音效何時完成播放。

如需 XAudio2 回呼的總覽，請參閱 [XAudio2 回呼](callbacks.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[XAudio2 版本](xaudio2-versions.md)
</dt> <dt>

[使用方法：初始化 XAudio2](how-to--initialize-xaudio2.md)
</dt> <dt>

[操作說明：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 




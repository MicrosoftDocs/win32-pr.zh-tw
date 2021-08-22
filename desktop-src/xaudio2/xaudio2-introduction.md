---
description: XAudio2 是低層級的音訊 API。 它會針對類似于前身、DirectSound 和 XAudio 的遊戲，提供信號處理和混合基礎。
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: XAudio2 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a966e9682a7f605864c0374a588d4b7eb3724036fe284bd6d92c64080e9225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589898"
---
# <a name="xaudio2-introduction"></a>XAudio2 簡介

XAudio2 是低層級的音訊 API。 它會針對類似于前身、DirectSound 和 XAudio 的遊戲，提供信號處理和混合基礎。

XAudio2 是適用于 DirectSound 的長時間等待取代。 它解決了數個未處理的問題和功能要求。

## <a name="xaudio2-features"></a>XAudio2 功能

以下是可讓開發人員改善其遊戲效能的 XAudio2 功能和新功能清單。

-   DSP 效果和每一語音篩選

    數位信號處理 (DSP) 效果是音訊的圖元著色器。 它們都能處理轉換音效的一切問題—將 pig squeal 變成低、令人驚訝的怪物音效，以使用回音和遮蔽或障礙物篩選來放置遊戲環境中的聲音。 XAudio2 提供有彈性且功能強大的 DSP 架構。 它也會針對每個語音提供內建的篩選準則，以提供有效率的低/高/頻外篩選效果。

    如需有關 DSP 效果及每個語音篩選的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) 和 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) 。

-   Submixing

    Submixing 會將數個音效合併成單一音訊串流，例如，引擎音效由複合元件組成，全都是同時播放。 此外，您也可以使用 submixing 來處理和合併遊戲的相似部分。 例如，您可以結合所有遊戲音效效果，讓使用者音量設定可以在個別設定控制音樂音量時套用。 Submixing 結合了 DSP，提供現今遊戲所需的資料路由與處理類型。 XAudio2 允許任意層級的 submixing，讓您能夠建立複雜的音效和遊戲混合。

    如需 submixing 的詳細資訊，請參閱[XAudio2 音訊 Graph](xaudio2-audio-graph.md)和[XAudio2 聲音](xaudio2-voices.md)。

-   壓縮的音訊支援

    DirectSound 的其中一個主要功能要求是針對壓縮的音訊支援。 XAudio2 支援壓縮格式（ADPCM），以原生方式解壓縮執行時間。

-   增強的多重通道和環繞音效支援

    多重通道、3D 和環繞音效支援都已展開。 3D 和環繞音效現在更有彈性且更透明。 XAudio2 會移除多聲道音效的6個通道限制，並支援任何具備多處理器功能的音訊卡上的多頻道音訊。 卡片不需要硬體加速。

-   Multirate 處理

    為了協助將 CPU 使用率降至最低，XAudio2 提供了建立多個低比率音訊處理圖形的技術。 如此一來，如果速率小於 48 kHz，可讓遊戲以來源資料的速率處理音訊，以大幅降低 CPU 的使用量。

-   非封鎖 API 模型

    有幾個例外狀況，XAudio2 方法呼叫不會封鎖音訊處理引擎。 這表示用戶端可以在任何時間安全地進行一組方法呼叫，而不會封鎖長時間執行的呼叫而導致延遲。 例外狀況是 [**IXAudio2Voice：:D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) 方法 (這種方法可能會封鎖引擎，直到終結的聲音已完成處理) 以及終止音訊執行緒的方法： [**IXAudio2：： StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) 和 [**IXAudio2：： Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release)。 請注意，雖然 XAudio2 方法呼叫不會封鎖音訊處理引擎，但 XAudio2 方法包含重要區段，而且在某些情況下可能會遭到封鎖。

## <a name="when-to-use-xaudio2"></a>使用 XAudio2 的時機

XAudio2 主要是用來開發適用于遊戲的高效能音訊引擎。 對於想在新型遊戲中增加音效和背景音樂的遊戲開發人員而言，XAudio2 可提供低延遲的音訊圖形和混合引擎，並且支援動態緩衝區、同步取樣精確播放，以及隱含的來源速率轉換。 相較于 WASAPI，XAudio2 只需要最少量的程式碼，即使是複雜的音訊解決方案也一樣。 相較于媒體基礎引擎，XAudio2 是一種低層級的低延遲 c + + API，專為在遊戲中使用而設計。

針對只需要定期播放音樂的應用程式，媒體基礎引擎可能與應用程式的需求更相符。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[XAudio2 程式設計參考](programming-reference.md)
</dt> </dl>

 

 

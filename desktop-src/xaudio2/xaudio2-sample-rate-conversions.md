---
description: 如果 XAudio2 語音的輸入取樣率與輸出語音的輸入取樣率不同，則可以執行自動取樣速率轉換。
ms.assetid: be34ce62-6552-45e2-a247-830ab55ea9ec
title: XAudio2 取樣率轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82983d1d9307551e516f1b8b60676b4b250450da65f416c340446c5a906f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962515"
---
# <a name="xaudio2-sample-rate-conversions"></a>XAudio2 取樣率轉換

如果 XAudio2 語音的輸入取樣率與輸出語音的輸入取樣率不同，則可以執行自動取樣速率轉換。

取樣率轉換會遵循下列規則：

-   語音輸入取樣率已修正。

    語音只能處理建立時所指定的輸入取樣率。 針對精通 [**語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)和 [**submix 聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)，輸入取樣率會以 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)和 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)函式的 *InputSampleRate* 引數來指定。 針對來源語音，語音的輸入取樣率是由 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) 函式的 pSourceFormat 引數所指定。

-   所有聲音的輸出語音都必須有相同的輸入取樣率。

    語音可以從其輸入取樣率轉換成任何輸出取樣率，但所有聲音的輸出語音都必須具有相同的輸入取樣率。 例如，語音可以輸出到任何數目的語音，輸入取樣率為 22 kHz。 不過，如果相同的聲音有數個輸出語音，每個輸出都有不同的輸入取樣率，音訊圖形將會無效。

-   取樣率轉換處理只會在必要時進行。

    將音訊資料轉換成不同的取樣率會產生更多處理額外負荷，因此最好避免使用。 如果語音的輸入取樣率符合輸出語音的輸入取樣率，則不會進行這項轉換，而且會縮短處理時間。

-   輸出取樣率可能會隨著聲音的存留期而改變。

    語音的輸出取樣率不是固定的。 只要其所有輸出語音都有相同的輸入取樣率，音訊圖表就會是有效的。 如果聲音變更為輸出到具有不同輸入取樣率的新語音，則語音會轉換成新聲音的輸入取樣率。

在某些情況下，必須新增 submix 聲音以執行語音之間的取樣率轉換。 如果聲音需要以各種輸入取樣率輸出至語音，則只有其中一個語音可以是原始語音的直接輸出。 因為所有聲音的輸出語音都必須具有相同的輸入取樣率，所以其他語音會間接接收輸出。 必須有一個 submix 的語音，並具有正確的輸入取樣率，以在原始語音和預期的輸出語音之間進行。

例如，假設來源語音的輸入取樣率為 22 kHz，這需要輸出至輸入取樣率為 11 kHz 的 submix 語音，以及輸入取樣率為 44.1 kHz 的主控語音。 因為這兩個輸出語音的輸入取樣率不同，所以您必須在原始語音和其預期的輸出語音之間插入更 submix 的聲音。 為了保持來源語音的精確度，並避免不必要的昂貴轉換成較高的取樣率，您需要在圖形中插入兩個 submix 的語音，並以 22 khz 的取樣輸入費率。 其中一個 submix 聲音會以 submix 聲音輸出至語音，並使用「回音」效果，而其他 submix 聲音則會輸出至 44.1 khz 的「控制」聲音。

## <a name="examples-of-sample-rate-conversion-in-audio-graphs"></a>音訊圖形中的取樣率轉換範例

所有語音都有相同的取樣輸入率;在音訊圖形中未進行採樣速率轉換。![在音訊圖形中未進行採樣速率轉換。](images/xaudio2-sample-rate-conversions-1.png)

所有語音都有相同的取樣輸入率，但不含「控制」聲音;取樣率轉換只會在資料進入「主控」聲音的資料上執行。 ![取樣率轉換只會在資料進入「主控」聲音的資料上執行。](images/xaudio2-sample-rate-conversions-2.png)

語音具有不同的取樣輸入率，而且需要更 submix 的語音來執行取樣率轉換;取樣速率轉換會在音訊圖形中的多個位置執行。 ![取樣速率轉換會在音訊圖形中的多個位置執行。](images/xaudio2-sample-rate-conversions-3.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[語音](voices.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 

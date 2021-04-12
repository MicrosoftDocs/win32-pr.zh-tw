---
description: 所有語音的組合（包含其內含效果和其相互連線）稱為音訊處理圖形。
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: XAudio2 音訊圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195300"
---
# <a name="xaudio2-audio-graph"></a>XAudio2 音訊圖形

所有語音的組合（包含其內含效果和其相互連線）稱為音訊處理圖形。 圖形會接受來自用戶端的一組音訊串流作為輸入、進行處理，並將最終結果傳遞給音訊裝置。 所有音訊處理都是在不同的執行緒中進行，而且其週期性是由圖形的量子所定義 (目前在 Microsoft Windows 上為10毫秒，Xbox 360) 則為 5 1/3 毫秒。 在每個量子毫秒，執行緒會透過整個圖形喚醒和 disperses 音訊資料的量子毫秒。 如需建立基本音訊圖形的範例，請參閱 how to： [建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)。

簡單的音訊圖形：

![簡單的音訊圖形](images/xaudio2-audio-graph.png)

用戶端可以在執行時動態控制圖形的狀態。 控制動作可能包括新增和移除輸入和輸出、變更內部效果和互相連線、設定效果的參數、啟用和停用圖形的元件等等。 如需動態變更音訊圖形的範例，請參閱 [如何：以動態方式新增或移除音訊圖形中的聲音](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)。

## <a name="processing-the-graph"></a>處理圖形

任何會影響圖形中任何物件的方法呼叫都會被視為影響圖形狀態變更。 圖形狀態變更包括下列各項：

-   建立和終結語音
-   啟動或停止語音
-   變更聲音的目的地
-   修改效果鏈
-   啟用或停用效果
-   設定效果或內建 SRCs、篩選、磁片區和 mixers 的參數

任何一組圖形狀態變更都可以合併並執行為不可部分完成的交易。 這些不可部分完成的作業稱為操作集。 它們會在 XAudio2 作業 [集](xaudio2-operation-sets.md) 總覽中討論。

## <a name="internal-data-representation"></a>內部資料表示

XAudio2 圖內的音訊資料一律會以32位浮點 PCM 形式儲存和處理。 不過，圖表內的頻道計數和取樣率可能會有所不同。 指定語音處理音訊的格式是由用來建立語音的語音類型和參數所決定。



| 語音類型                                                                                                      | 參數                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | 來源聲音傳送音訊的語音聲道計數和取樣率。         |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)和 [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) | 用來建立 submix/主控聲音的 *InputChannels* 和 *InputSampleRate* 引數。 |



 

## <a name="format-conversion"></a>格式轉換

XAudio2 會處理音訊從某個語音傳送到另一個語音時所需的任何取樣率或通道轉換，但有下列限制：

-   特定語音的所有目的地語音都必須以相同的取樣率執行
-   效果鏈中的效果可能會變更音訊的頻道計數，但不能變更其取樣率
-   效果鏈的輸出通道計數必須符合其傳送的聲音
-   無法進行動態圖形變更，因此會中斷上述規則

在輸入端，來源語音可以讀取任何有效 PCM 格式的資料，或是 XAudio2 所支援的任何壓縮格式的資料。 如果輸入資料已壓縮，則會先將其解碼為浮點 PCM，再進行任何進一步的處理。

在輸出端，主控語音只能產生 PCM 資料。 這種資料一律會滿足上述對輸入 PCM 資料所述的相同限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊圖形](audio-graphs.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[使用方法：從音訊圖形動態新增或移除聲音](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[使用方法：使用次混音聲音](how-to--use-submix-voices.md)
</dt> <dt>

[使用方法：建立效果鏈](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 




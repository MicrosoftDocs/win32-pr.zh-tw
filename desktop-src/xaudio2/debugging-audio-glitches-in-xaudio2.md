---
description: 問題可能會發生在 XAudio2 中，本主題會說明如何報告這些問題，以及解決這些問題的一些方法。
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: 對 XAudio2 中的音訊問題進行偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8856defc67bc9453b9d83f5ed369bfb96f48b8c2c16c92ea535a0c1b648402b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703618"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a>對 XAudio2 中的音訊問題進行偵錯

問題可能會發生在 XAudio2 中，本主題會說明如何報告這些問題，以及解決這些問題的一些方法。

本總覽涵蓋下列主題：

-   [音訊輸出問題或問題的原因](#causes-of-audio-output-problems-or-glitches)
-   [XAudio2 如何報告問題](#how-xaudio2-reports-problems)
-   [修正問題的方法](#approaches-to-fixing-problems)
-   [相關主題](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a>音訊輸出問題或問題的原因

XAudio2 輸出可能發生問題的原因有好幾個。

-   XAudio2 來源語音為耗盡。 用戶端不會將新音訊提交到足夠的速度。 因為沒有任何資料可供播放，所以您會收到無回應。
-   XAudio2 整體會有過重的負擔。 產生 *x* 毫秒的音訊需要比 *x* 毫秒更長的時間。 您會收到中斷，因為 XAudio2 無法像音訊裝置需要一樣快速產生資料。 您可能一次執行太多聲音或效果、在 XAudio2 回呼中執行太多工作，或太頻繁地進行 XAudio2 API 呼叫。
-   音訊處理執行緒很拖延，因為用戶端在執行某些 XAudio2 回呼時，會執行一些作業來封鎖執行緒。 例如，它可能會存取磁片、與其他執行緒進行同步處理，或呼叫可能封鎖的其他函式。 使用回呼可發出的較低優先順序背景執行緒來執行這類工作。
-   整個系統都會超載。 執行的其他執行緒與 XAudio2 相同或更高的優先順序正在執行太多工作。 它們會與音訊執行緒爭用 CPU 時間。

## <a name="how-xaudio2-reports-problems"></a>XAudio2 如何報告問題

XAudio2 可以透過數種方式來傳達 debug 組建中的問題。

-   如果正在耗盡語音，XAudio2 會顯示此表單中的訊息。

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   如果音訊執行緒執行太長的時間，XAudio2 會顯示此表單中的訊息。

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    一般來說，此訊息會出現在下一個訊息中。

-   如果音訊驅動程式無法及時送入新的音訊資料，XAudio2 會顯示此表單中的訊息。

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   呼叫 [**IXAudio2：： GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) 會提供 XAudio2 的效能資料，包括自 XAudio2 引擎啟動以來的問題總數。

## <a name="approaches-to-fixing-problems"></a>修正問題的方法

減少音訊問題的可能方式包括下列各項。

-   在語音耗盡案例中：增加聲音上排入佇列的音訊資料量。 您可以使用 [**IXAudio2SourceVoice：： >getstate**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) 來探索任何時間佇列的緩衝區數目。 如果您仍然看到「聲音耗盡」的錯誤，但聽不到任何問題，請確定您正在設定 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)。在音效的 \_ \_ \_ 最終緩衝區上 XAUDIO2 資料流程結尾的旗標。 如此一來，XAudio2 就不會預期任何緩衝區都必須在這個動作完成後立即可用。

    在其他情況下：

    -   減少圖形中的作用中語音和效果的數目，特別是高成本的效果，例如「回音」。
    -   停用您未使用的語音和效果。
    -   盡可能 \_ \_ \_ \_ 在 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)中使用 XAUDIO2 voice NOSRC 和 XAUDIO2 voice NOPITCH 旗標。 取樣率轉換很昂貴。
    -   減少個別聲音的取樣率。 例如，submix 聲音裝載的「回音」效果，其取樣率會低於傳送給它的來源語音。 不需要高精確度的音效（例如爆炸和 gunshots）也可以記錄較低的取樣率。
    -   確定回呼的執行工作盡可能少，而且永遠不會封鎖。
    -   對 XAudio2 發出較少的呼叫。 音訊參數通常不需要針對每個影片畫面更新。 每隔30毫秒就夠了。 您應消除重複的呼叫，例如快速連續地設定磁片區數次。
    -   減少遊戲的整體 CPU 使用率。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[調試功能](debugging-facilities.md)
</dt> <dt>

[XAudio2 程式設計參考](programming-reference.md)
</dt> </dl>

 

 

---
description: CBaseVideoRenderer 基類是用來建立影片轉譯器篩選器。
ms.assetid: 659ce3d4-8702-4daf-9242-787d67758d90
title: CBaseVideoRenderer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0f174254314656d153fdb568b9a9fa457775282
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688463"
---
# <a name="cbasevideorenderer-class"></a>CBaseVideoRenderer 類別

![cbasevideorenderer 類別階層](images/rbase03.png)

`CBaseVideoRenderer`基底類別是用來建立影片轉譯器篩選器。



| 受保護的資料成員                                                                 | Description                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bDrawLateFrames                                                                     | 表示不會卸載任何框架的旗標。 僅限 Debug。 這會破壞同步處理。                                                                                                                                          |
| m \_ bSupplierHandlingQuality                                                            | **TRUE** 表示正在處理品質控制訊息。 這可讓轉譯器知道要盡可能延遲，以卸載框架本身，並在供應商卸載框架之後，提早顯示下一個畫面格。 |
| m \_ cFramesDrawn                                                                        | 自從串流開始之後，已繪製的框架總數。                                                                                                                                                                 |
| m \_ cFramesDropped                                                                      | 自從串流開始後，已在轉譯器中捨棄的累計框架。 您也可以在未辨識轉譯器的情況下，將框架卸載至上游。                                                                         |
| m \_ idDecision                                                                          | \_ [**ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)決策碼的 MSR 識別碼。                                                                                                                              |
| m \_ idDuration                                                                          | \_框架期間的 MSR 識別碼。                                                                                                                                                                                                 |
| m \_ idFrameAccuracy                                                                     | 框架延遲時間的效能記錄識別碼（以毫秒為單位）。                                                                                                                                                     |
| m \_ idFrameAvg                                                                          | 用於同步處理和品質控制的平均幀時間的效能記錄識別碼。                                                                                                                          |
| m \_ idQualityRate                                                                       | 所 \_ 要求品質率的 MSR 識別碼。                                                                                                                                                                                              |
| m \_ idQualityTime                                                                       | \_要求的品質時間的 MSR 識別碼。                                                                                                                                                                                              |
| m \_ idRenderAvg                                                                         | 記錄的平均轉譯器時間的效能記錄識別碼。                                                                                                                                                                   |
| m \_ idSchLateTime                                                                       | \_已排程之框架延遲時間的 MSR 識別碼。                                                                                                                                                                                   |
| m \_ idSendQuality                                                                       | \_用於計時通知的 MSR 識別碼 (未使用的) 。                                                                                                                                                                                       |
| m \_ idTimeStamp                                                                         | \_框架時間戳記的 MSR 識別碼。                                                                                                                                                                                                      |
| m \_ idWait                                                                              | 記錄等候時間的效能記錄識別碼 (未使用的) 。                                                                                                                                                                      |
| m \_ idWaitReal                                                                          | 真正等候時間的效能記錄識別碼。                                                                                                                                                                                   |
| m \_ iSumFrameTime                                                                       | 總幀時間的總和;屬性頁所需。                                                                                                                                                                           |
| m \_ iSumSqAcc                                                                           | 屬性頁所需的精確度 (的平方總和，以毫秒為單位) 。                                                                                                                                                 |
| m \_ iSumSqFrameTime                                                                     | 總幀時間的平方總和;屬性頁所需。                                                                                                                                                                |
| m \_ iTotAcc                                                                             | 屬性頁所需的精確度 (的總和，以毫秒為單位) 。                                                                                                                                                                |
| m \_ nNormal                                                                             | 在排程的時間繪製的連續框架數目。 負數表示轉譯器剛卸載框架。                                                                                          |
| m \_ trDuration                                                                          | 最後一個畫面格的持續時間 (開始與結束時間) 之間的差異。                                                                                                                                                             |
| m \_ trEarliness                                                                         | 當畫面格剛卸載時，允許畫面的早期播放方式。                                                                                                                                                        |
| m \_ trFrame                                                                             | 畫面格之間最近錄製的時間。 用於統計度量。                                                                                                                                                        |
| m \_ trFrameAvg                                                                          | 參考時間單位中的平均幀時間。                                                                                                                                                                                     |
| m \_ trLastDraw                                                                          | 上一個畫面格的時間。 用於幀時間參考。                                                                                                                                                                         |
| m \_ trLate                                                                              | 目前框架延遲的時間量。 用於統計度量。                                                                                                                                                    |
| m \_ trRenderAvg                                                                         | 畫面格執行位區塊傳輸所花費的時間。                                                                                                                                                                       |
| m \_ trRenderLast                                                                        | 最後一個畫面格位封鎖傳送的時間。                                                                                                                                                                                          |
| m \_ trRenderStart                                                                       | 位區區塊轉送的開始時間。 用來取得 **m \_ trRenderLast**。                                                                                                                                                                |
| m \_ trThrottle                                                                          | 轉譯每個畫面格之後要插入的期間，通常會在音訊品質增加且影片效能必須減少以允許時使用。                                                                             |
| m \_ trWaitAvg                                                                           | 參考時間單位中的平均等候時間。                                                                                                                                                                                           |
| m \_ tStreamingStart                                                                     | 用於屬性頁面統計資料。 代表目前串流處理常式的開始時間，或先前的串流處理常式（如果目前未進行串流處理）。                                                                          |
| 成員函數                                                                       | Description                                                                                                                                                                                                                          |
| [**CBaseVideoRenderer**](cbasevideorenderer-cbasevideorenderer.md)                    | 結構 **CBaseVideoRenderer** 物件。                                                                                                                                                                                          |
| [**GetStdDev**](cbasevideorenderer-getstddev.md)                                      | 預估每個畫面格的統計資料，以毫秒為單位來估計每個框架的到期時間和實際轉譯的標準差（以毫秒為單位）。                                                                                          |
| [**PreparePerformanceData**](cbasevideorenderer-prepareperformancedata.md)            | 設定目前框架的 **m \_ trLate** 和 **m \_ trFrame** 值。                                                                                                                                                               |
| [**ThrottleWait**](cbasevideorenderer-throttlewait.md)                                | 在每個畫面格之後插入等待期間。                                                                                                                                                                                              |
| 可覆寫的成員函式                                                           | Description                                                                                                                                                                                                                          |
| [**JoinFilterGraph**](cbasevideorenderer-joinfiltergraph.md)                          | 從篩選圖形移除篩選時，傳送 [**EC \_ 視窗 \_ 損毀**](ec-window-destroyed.md) 事件。                                                                                                                    |
| [**OnDirectRender**](cbasevideorenderer-ondirectrender.md)                            | 收集控制同步處理和品質控制的時間資訊。                                                                                                                                                       |
| [**OnRenderEnd**](cbasevideorenderer-onrenderend.md)                                  | 記錄品質控制和同步處理的資訊。                                                                                                                                                                         |
| [**OnRenderStart**](cbasevideorenderer-onrenderstart.md)                              | 記錄品質控制和同步處理的資訊。                                                                                                                                                                         |
| [**OnStartStreaming**](cbasevideorenderer-onstartstreaming.md)                        | 重設控制串流的所有時間。                                                                                                                                                                                             |
| [**OnStopStreaming**](cbasevideorenderer-onstopstreaming.md)                          | 在串流結束時呼叫，以修正屬性頁報表的時間。                                                                                                                                                            |
| [**OnWaitEnd**](cbasevideorenderer-onwaitend.md)                                      | 在等待時間結束時呼叫。 僅限效能記錄。                                                                                                                                                                              |
| [**OnWaitStart**](cbasevideorenderer-onwaitstart.md)                                  | 更新花費在等候和不等待的時間。 僅限效能記錄。                                                                                                                                                               |
| [**RecordFrameLateness**](cbasevideorenderer-recordframelateness.md)                  | 記錄轉譯發生的及時時間，並收集屬性頁面的統計資料。                                                                                                                                              |
| [**ResetStreamingTimes**](cbasevideorenderer-resetstreamingtimes.md)                  | 重設控制串流的所有時間。                                                                                                                                                                                         |
| [**ScheduleSample**](cbasevideorenderer-schedulesample.md)                            | 使用時鐘設定建議連結。                                                                                                                                                                                               |
| [**SendQuality**](cbasevideorenderer-sendquality.md)                                  | 傳送品質訊息以指出供應商應該如何處理品質。                                                                                                                                                       |
| [**ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)                  | 判斷影片是否應在到期時繪製，而不需要使用時鐘來設定計時器建議連結。                                                                                                                          |
| IQualProp 方法                                                                      | Description                                                                                                                                                                                                                          |
| [**取得 \_ 平均幀率**](cbasevideorenderer-get-avgframerate.md)                      | 抓取從每100秒的畫面格開始串流之後的平均畫面播放速率。                                                                                                                                                  |
| [**取得 \_ AvgSyncOffset**](cbasevideorenderer-get-avgsyncoffset.md)                     | 以毫秒為單位，抓取每個框架到期和實際轉譯時的平均時間（以毫秒為單位）。 這適用于自從串流開始之後的所有框架。                                                             |
| [**取得 \_ DevSyncOffset**](cbasevideorenderer-get-devsyncoffset.md)                     | 以毫秒為單位，抓取每個框架的到期時間，以及從串流開始之後針對所有框架實際轉譯的時間（以毫秒為單位）。                                                               |
| [**取得 \_ FramesDrawn**](cbasevideorenderer-get-framesdrawn.md)                         | 抓取串流開始之後所繪製的框架數目。                                                                                                                                                                        |
| [**取得 \_ FramesDroppedInRenderer**](cbasevideorenderer-get-framesdroppedinrenderer.md) | 抓取轉譯器捨棄的框架數目。 框架也可以卸載上游。                                                                                                                                         |
| [**取得 \_ 抖動**](cbasevideorenderer-get-jitter.md)                                   | 抓取每個畫面和下一個畫面格之間時間的標準差（以毫秒為單位）。 這適用于自從串流開始之後的所有框架。                                                                                    |
| IQualityControl 方法                                                                | Description                                                                                                                                                                                                                          |
| [**Notify**](cbasevideorenderer-notify.md)                                            | 告知收件者要求品質變更。                                                                                                                                                                           |
| [**SetSink**](cbasevideorenderer-setsink.md)                                          | 設定將接收品質訊息的 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 物件。                                                                                                                                       |



 

 

 




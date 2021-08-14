---
description: CBaseRenderer 類別是用來執行轉譯器篩選器的基類。
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: 'CBaseRenderer 類別 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954800"
---
# <a name="cbaserenderer-class"></a>CBaseRenderer 類別

![cbaserenderer 類別階層](images/rbase02.png)

`CBaseRenderer`類別是用來執行轉譯器篩選器的基類。 它支援 [**CRendererInputPin**](crendererinputpin.md) 類別所執行的一個輸入 pin。 若要使用這個類別，請宣告繼承的衍生類別 `CBaseRenderer` 。 衍生類別至少必須執行下列方法，這些方法會在基類中宣告為純虛擬：

-   [**CBaseRenderer：： CheckMediaType**](cbaserenderer-checkmediatype.md)：接受或拒絕建議的媒體類型。 篩選會在 pin 連線程式期間呼叫這個方法。
-   [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md)：呈現範例。 篩選準則會針對它在執行時所收到的每個範例，呼叫這個方法。

基底類別會處理狀態變更和同步處理問題。 它也會排程轉譯的範例，不過它不會執行任何品質控制量值。 基類也會宣告數個 "handler" 方法。 這些是篩選準則在串流處理常式中的特定點呼叫的方法。 它們不會在基類中執行任何動作，但衍生類別可以覆寫它們。 在接下來的表格中，它們會列在 [公用方法：處理常式] 標題下方。

[**CBaseRenderer：： OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)處理常式值得特別提及。 篩選準則會在篩選暫停時，呼叫此方法以接收範例。 如果圖形從停止切換為已暫停，或圖形在暫停時 seeked，可能會發生這種情況。 影片轉譯器通常會使用範例來顯示靜止框架。 當篩選從暫停切換為執行時，它會將相同的範例傳送至 [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md) 方法，作為串流中的第一個範例。

`CBaseRenderer`類別會透過 [**CRendererPosPassThru**](crendererpospassthru.md)物件公開 **IMediaSeeking** 和 **IMediaPosition** 介面。 它會將所有搜尋要求傳遞至下一個篩選上游。

## <a name="scheduling"></a>排程

當上游篩選呼叫輸入 pin 的 [**IMemInputPin：： receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法來傳遞範例時，pin 會將此呼叫傳遞給篩選器的 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法。 篩選器會卸載範例、立即加以轉譯，或排程它以進行轉譯。

如果範例沒有時間戳記，或沒有可用的參考時鐘，則篩選會立即轉譯範例。 否則，篩選準則會呼叫 [**CBaseRenderer：： ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) 方法來判斷要執行的動作。 根據預設，範例會根據其時間戳記進行排程。 衍生類別可以覆寫 **ShouldDrawSampleNow** 以支援品質控制。

若要排程範例，篩選準則會呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法，以建立建議要求。 接收方法接著 [**會**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 封鎖直到排定的時間為止，或直到篩選變更狀態為止。 封鎖可防止上游篩選器傳遞更多範例，直到轉譯目前的樣本為止。

當上游篩選準則呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法以表示資料流程的結尾時，篩選會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。 篩選準則會在傳送事件之前等候目前的範例停止時間。



| 受保護的成員變數                                                   | Description                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | 旗標，指出是否要停止轉譯和拒絕進一步的範例。                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | 指出是否已到達資料流程結尾的旗標。                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | 指出篩選是否已張貼 EC COMPLETE 事件的旗標 \_ 。                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | 指出篩選是否正在處理 **接收** 呼叫的旗標。                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | 啟用或停用重繪事件的旗標。                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | 指出篩選是否為數據流資料的旗標。                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | 排程轉譯之計時器事件的識別碼。                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | 計時器-事件識別碼，用於排程 EC \_ 完成通知。                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | 狀態轉換完成時收到通知的事件。                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | 篩選準則狀態鎖定。                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | 鎖定以保護在篩選內建立物件。                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | 篩選的輸入圖釘指標。                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | 目前媒體範例的指標。                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | 要傳遞向上游傳遞搜尋命令的 Helper 物件。                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | 物件的指標，該物件會接收品質控制訊息。                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | 串流鎖定。                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | 用來排程轉譯的事件。                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | 目前範例的停止時間。                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | 用來釋放串流執行緒的事件。                                                                                             |
| 公用方法                                                               | Description                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | 取消排程轉譯的計時器事件。 虛擬。                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | 函式方法。                                                                                                                     |
| [**~ CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | 函式方法。                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | 捕獲篩選的 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面指標。 虛擬。 |
| [**GetPin**](cbaserenderer-getpin.md)                                       | 捕獲 pin。 虛擬。                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | 抓取釘選數目。 虛擬。                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | 抓取範例中的時間戳記。 虛擬。                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | 將 [**EC \_ 顯示 \_ 變更**](ec-display-changed.md) 事件張貼至篩選圖形管理員。                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | 準備轉譯範例。 虛擬。                                                                                                   |
| [**收到**](cbaserenderer-receive.md)                                     | 接收資料流程中的下一個媒體範例。 虛擬。                                                                                  |
| [**呈現**](cbaserenderer-render.md)                                       | 呈現範例。 虛擬。                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | 排定轉譯的範例。 虛擬。                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | 通知影片視窗控制碼的上游篩選。                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | 將重新繪製事件傳送至篩選圖形管理員。                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | 當釘選的媒體類型設定時呼叫。 虛擬。                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | 清除用來排程轉譯的計時器識別碼。                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | 保存或釋放串流執行緒。 虛擬。                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | 等候 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法完成。                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | 等候目前樣本的呈現時間。 虛擬。                                                                              |
| 公用方法：存取子方法                                             | Description                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | 釋放目前的範例。 虛擬。                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | 抓取目前的範例。 虛擬。                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | 捕獲篩選狀態。                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | 捕獲排程轉譯的事件。                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | 判斷篩選是否有範例。 虛擬。                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | 查詢是否已收到資料流程結尾通知。                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | 查詢 EC \_ 完成事件是否已傳遞至篩選圖形管理員。                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | 查詢篩選是否為數據流處理資料。                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | 設定旗標，指出是否要停止轉譯和拒絕進一步的範例。                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | 啟用或停用重新繪製事件。                                                                                                     |
| 公用方法： State-Change 方法                                         | Description                                                                                                                             |
| [**使用中**](cbaserenderer-active.md)                                       | 當狀態切換為已暫停或正在執行時呼叫。 虛擬。                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | 開始清除作業。 虛擬。                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | 從連接釋放輸入的 pin。 虛擬。                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | 查詢狀態轉換是否已完成。                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | 完成輸入 pin 與另一個 pin 的連接。 虛擬。                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | 判斷轉換為暫停狀態是否已完成。 虛擬。                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | 結束清除操作。 虛擬。                                                                                                        |
| [**非使用中**](cbaserenderer-inactive.md)                                   | 當狀態切換為 [已停止] 時呼叫。 虛擬。                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | 指示狀態轉換尚未完成。                                                                                    |
| [**就緒**](cbaserenderer-ready.md)                                         | 指示狀態轉換已完成。                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | 當篩選參數切換到執行中狀態時，起始串流處理。 虛擬。                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | 當篩選參數切換到執行中狀態時，就會停止串流。 虛擬。                                                             |
| 公用方法：資料流程結束方法                                        | Description                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | 通知篩選輸入 pin 收到資料流程結束通知。 虛擬。                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | 將 [**EC \_ 完成**](ec-complete.md) 事件張貼至篩選圖形管理員。                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | 重設資料流程結尾旗標。                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | 取消排定 EC \_ 完成通知的計時器。 虛擬。                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | 如果已到達資料流程結尾， \_ 則會為篩選圖形管理員排定 EC 完成事件。 虛擬。                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | 結束資料流程計時器事件的回呼方法。                                                                                      |
| 公用方法：處理常式                                                     | Description                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | 當篩選準則在暫停時收到範例時呼叫。 虛擬。                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | 在呈現樣本之後呼叫。 虛擬。                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | 當轉譯即將開始時呼叫。 虛擬。                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | 當篩選開始串流時呼叫。 虛擬。                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | 當篩選停止串流時呼叫。 虛擬。                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | 當篩選完成等候樣本的呈現時間時呼叫。 虛擬。                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | 當篩選開始等候樣本的呈現時間時呼叫。 虛擬。                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | 在篩選器呈現範例之前呼叫。 虛擬。                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | 決定如何排程範例以呈現。 虛擬。                                                                            |
| 純虛擬方法                                                         | Description                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | 判斷篩選是否接受特定的媒體類型。                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | 呈現範例。                                                                                                                       |
| IMediaFilter 方法                                                         | Description                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | 抓取篩選器的狀態 (執行中、已停止或已暫停) 。                                                                             |
| [**暫停**](cbaserenderer-pause.md)                                         | 暫停篩選。                                                                                                                      |
| [**執行**](cbaserenderer-run.md)                                             | 執行篩選。                                                                                                                        |
| [**停止**](cbaserenderer-stop.md)                                           | 停止篩選。                                                                                                                       |
| IBaseFilter 方法                                                          | Description                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | 使用指定的識別碼抓取 pin。                                                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 





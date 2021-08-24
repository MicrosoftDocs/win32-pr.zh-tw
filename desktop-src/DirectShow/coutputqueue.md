---
description: COutputQueue 類別會執行傳遞媒體範例的佇列。
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: 'COutputQueue 類別 (Outputq) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8911c7261af0bf2e140a551b0146b7764cd541368898e6d3905f5dee2eaa4c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813431"
---
# <a name="coutputqueue-class"></a>COutputQueue 類別

![coutputqueue](images/oput01.png)

`COutputQueue`類別會執行佇列以傳遞媒體範例。

此類別可讓輸出圖釘以非同步方式傳遞範例。 範例會放置在佇列中，而背景工作執行緒會將它們傳遞給輸入的 pin。 佇列也可以保存表示新區段、資料流程結束通知或清除作業的控制訊息。

若要使用這個類別，請針對篩選上的每個輸出圖釘建立 **COutputQueue** 物件。 在 [函式] 方法中，指定連接到該輸出 pin 的輸入 pin。 使用這個類別時，輸出釘選不會直接在輸入 pin 上呼叫方法。 相反地，它會在中呼叫對應的方法 `COutputQueue` ，如下表所示。



| Pin 方法                                                            | COutputQueue 方法                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**EOS**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**收到**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

（選擇性）您可以將 `COutputQueue` 物件設定為同步傳遞範例，而不需要工作者執行緒。 物件也可以根據輸入釘選的特性，在執行時間決定是否要使用背景工作執行緒。 如需詳細資訊，請參閱 [**COutputQueue：： COutputQueue**](coutputqueue-coutputqueue.md)。



| 受保護的成員變數                                   | 描述                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | 輸入釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | 輸入釘選 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的指標。                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | 旗標，指定物件是否以精確的批次傳遞範例。                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | 批次大小。                                                                                              |
| [**m \_ 清單**](coutputqueue-m-list.md)                       | 媒體範例佇列。                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | 信號的控制碼，由執行緒用來等候樣本。                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | 發出清除作業完成時發出信號的事件。                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | 工作者執行緒的控制碼。                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | 大小為 [**COutputQueue：： m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)的範例陣列。               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | 目前批次處理和等候處理的樣本數。                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | 當執行緒正在等候範例時，具有非零值的旗標。                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | 旗標，指定物件是否正在執行清除作業。                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | 指定是否應終止執行緒的旗標。                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | 覆寫批次處理的旗標。                                                                       |
| [**m \_ 小時**](coutputqueue-m-hr.md)                           | **HRESULT** 值，指出物件是否會接受範例。                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | 每次物件從佇列中移除範例時發出信號的事件。                              |
| 保護方法                                            | 描述                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | 在建立執行緒時，呼叫 [**COutputQueue：： ThreadProc**](coutputqueue-threadproc.md) 方法。 |
| [**ThreadProc**](coutputqueue-threadproc.md)                | 從佇列中取出範例，並將其傳遞至輸入圖釘。                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | 判斷物件是否使用背景工作執行緒來傳遞範例。                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | 將媒體範例或控制訊息排在佇列中。                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | 判斷佇列資料是否為控制訊息。                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | 釋出所有暫止的範例。                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | 通知執行緒佇列包含資料。                                                        |
| 公用方法                                               | 描述                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | 函式方法。                                                                                      |
| [**~ COutputQueue**](coutputqueue--coutputqueue.md)          | 函式方法。                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | 開始清除作業。                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | 結束清除操作。                                                                                  |
| [**EOS**](coutputqueue-eos.md)                              | 傳遞輸入圖釘的資料流程結束呼叫。                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | 提供任何暫止的範例。                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | 將新區段傳遞至輸入圖釘。                                                                 |
| [**收到**](coutputqueue-receive.md)                      | 傳遞媒體範例至輸入 pin。                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | 傳遞一批媒體範例至輸入 pin。                                                      |
| [**重設**](coutputqueue-reset.md)                          | 重設物件，使其可以接收更多資料。                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | 判斷物件是否正在等候資料。                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | 指定當物件從佇列中移除範例時，會發出信號的事件。                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 





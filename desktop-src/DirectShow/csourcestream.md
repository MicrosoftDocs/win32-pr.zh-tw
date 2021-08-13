---
description: CSourceStream 類別提供 CSource 篩選類別的輸出圖釘。
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: 'CSourceStream 類別 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f7563cabff97626ac45a150e9a763033d9ce9261e5ae528e83d174e35d4f0d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428780"
---
# <a name="csourcestream-class"></a>CSourceStream 類別

![csourcestream 類別階層](images/source02.png)

**CSourceStream** 類別提供 [**CSource**](csource.md)篩選類別的輸出圖釘。

如需使用這個類別的詳細資訊，請參閱 [**CSource**](csource.md)。 此類別會繼承 [**CAMThread**](camthread.md) 類別，此類別會提供背景工作執行緒來串流處理來自 pin 的資料。 **CSourceStream** 類別會執行下列 helper 方法，以將要求傳送至執行緒：

-   [**CSourceStream：： Exit**](csourcestream-exit.md)
-   [**CSourceStream：： Init**](csourcestream-init.md)
-   [**CSourceStream：:P ause**](csourcestream-pause.md)
-   [**CSourceStream：： Run**](csourcestream-run.md)
-   [**CSourceStream：： Stop**](csourcestream-stop.md)

對執行緒的第一個要求必須是 [**Init**](csourcestream-init.md)。 [**Exit**](csourcestream-exit.md)要求會終止執行緒。 在實務上，不需要直接呼叫任何方法，因為釘選的 [**CSourceStream：： Active**](csourcestream-active.md) 和 [**CSourceStream：：非**](csourcestream-inactive.md) 使用中方法會視需要呼叫這些方法。

類別也提供數個「處理常式」方法：

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

這些都不會在基類中執行任何動作，但衍生類別可以覆寫它們。



| 受保護的成員變數                                             | 描述                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ pFilter**](csourcestream-m-pfilter.md)                          | 包含此 pin 之篩選準則的指標。                                                                                     |
| 保護方法                                                      | 描述                                                                                                                       |
| [**OnThreadCreate**](csourcestream-onthreadcreate.md)                 | 在串流處理執行緒初始化時呼叫。 虛擬。                                                                         |
| [**OnThreadDestroy**](csourcestream-onthreaddestroy.md)               | 當串流執行緒即將結束時呼叫。 虛擬。                                                                       |
| [**OnThreadStartPlay**](csourcestream-onthreadstartplay.md)           | 在 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法開始時呼叫。 虛擬。 |
| [**使用中**](csourcestream-active.md)                                 | 通知釘選篩選現在已啟用。                                                                                   |
| [**非使用中**](csourcestream-inactive.md)                             | 通知 pin 此篩選已不再有效。                                                                             |
| [**GetRequest**](csourcestream-getrequest.md)                         | 等候下一個執行緒要求。                                                                                                |
| [**CheckRequest**](csourcestream-checkrequest.md)                     | 檢查是否有線程要求，而不封鎖。                                                                            |
| [**ThreadProc**](csourcestream-threadproc.md)                         | 執行緒程式。 虛擬。                                                                                                        |
| [**DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) | 產生媒體資料，並將其傳遞至下游輸入 pin。 虛擬。                                                        |
| [**CheckMediaType**](csourcestream-checkmediatype.md)                 | 判斷 pin 是否接受特定的媒體類型。 虛擬。                                                                     |
| [**GetMediaType**](csourcestream-getmediatype.md)                     | 捕獲慣用的媒體類型。 虛擬。                                                                                        |
| 公用方法                                                         | 描述                                                                                                                       |
| [**CSourceStream**](csourcestream-csourcestream.md)                   | 函式方法。                                                                                                               |
| [**~ CSourceStream**](csourcestream--csourcestream.md)                | 函式方法。 虛擬。                                                                                                       |
| [**Init**](csourcestream-init.md)                                     | 初始化串流執行緒。                                                                                                 |
| [**結束**](csourcestream-exit.md)                                     | 通知串流執行緒結束。                                                                                             |
| [**執行**](csourcestream-run.md)                                       | 指示要執行的串流執行緒。                                                                                              |
| [**暫停**](csourcestream-pause.md)                                   | 通知串流執行緒成為作用中。                                                                                    |
| [**停止**](csourcestream-stop.md)                                     | 通知串流執行緒停止。                                                                                             |
| 純虛擬方法                                                   | 描述                                                                                                                       |
| [**FillBuffer**](csourcestream-fillbuffer.md)                         | 使用資料填滿媒體範例。                                                                                                   |
| IPin 方法                                                           | 描述                                                                                                                       |
| [**QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | 抓取 pin 的識別碼。                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[寫入來源篩選](writing-source-filters.md)
</dt> </dl>

 

 





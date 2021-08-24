---
description: CDynamicOutputPin 類別會實作為支援動態重新連接和格式變更的輸出 pin。
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: 'CDynamicOutputPin 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e0b8903f83c372aa85bd1c41fb12ce9065798d79dc4dbd940df926a395f8bc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871798"
---
# <a name="cdynamicoutputpin-class"></a>CDynamicOutputPin 類別

`CDynamicOutputPin`類別會實作為支援動態重新連接和格式變更的輸出 pin。

這個類別衍生自 [**CBaseOutputPin**](cbaseoutputpin.md) 類別，並會執行 [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) 介面。 它支援數個對動態圖形建立很重要的作業：

-   動態重新連接：當篩選仍在作用中時，pin 可以中斷連接並重新連接 (已暫停或正在執行) 。
-   動態格式變更：當篩選仍在作用中時，pin 可以協商新的媒體類型，而不需要重新連接。
-   Flow 控制項：擁有篩選 (或應用程式) 可以封鎖來自 pin 的資料流程，而不需要停止篩選。

如需詳細資訊，請參閱[動態 Graph 建立](dynamic-graph-building.md)。

Pin 有三個可能的狀態：已封鎖、已解除封鎖和擱置。 在 *暫* 止狀態中，pin 正在等候某些作業在另一個執行緒上完成，然後再切換到 [已封鎖] 狀態。 當 pin 遭到封鎖時，篩選器無法透過 pin 傳遞資料，或變更 pin 的連接。

若要在多個執行緒之間進行協調，擁有篩選準則必須遵循特定規則。  (如需有關篩選圖形中線程的詳細資訊，請參閱 [執行緒和重要區段](threads-and-critical-sections.md)。首先 ) ，資料流程執行緒必須一律呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法，才能呼叫下列任何方法：

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin：:D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin：:D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin：:D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

之後，它必須呼叫 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) 方法。

第二，應用程式執行緒不能呼叫上一個清單中的任何方法。 第三，串流執行緒不能呼叫封鎖或解除封鎖 pin 的類別方法。 這些方法包括： [**CDynamicOutputPin：： Block**](cdynamicoutputpin-block.md)、 [**CDynamicOutputPin：： SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)、 [**CDynamicOutputPin：： AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)和 [**CDynamicOutputPin：： UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)。

這些規則可確保應用程式執行緒無法在串流執行緒使用時封鎖 pin，反之亦然。 在串流執行緒呼叫 **StartUsingOutputPin** 之後，將不會封鎖 pin，直到串流執行緒呼叫 **StopUsingOutputPin** 為止。 相反地，如果 pin 被封鎖， **StartUsingOutputPin** 會等到 pin 解除封鎖為止。

若要避免忘記呼叫 **StopUsingOutputPin**，您可以使用 [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) 類別。 它會在超出範圍時自動呼叫 **StopUsingOutputPin** 。

當擁有篩選器在其 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法) 中加入或 leaveds 篩選圖形 (時，必須呼叫釘選的 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 方法。



| 受保護的成員變數                                                                      | 描述                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | 保護封鎖狀態的重要區段。                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | 未封鎖 pin 時發出信號的事件。                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | 當 pin 成功封鎖或使用者取消暫止的區塊時，會發出信號的事件。                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | 封鎖狀態。                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | 此 pin 上最後一次呼叫 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 方法之執行緒的識別碼。 |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | 使用此 pin 的串流執行緒數目。                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | 當篩選準則停止或釘選清除資料時，所發出的事件。                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)介面的指標，可執行動態重新連結。                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | 旗標，指定來自釘選配置器的樣本是否為唯讀。                                                   |
| 保護方法                                                                               | 描述                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | 封鎖釘選;在封鎖 pin 之前，不會返回。                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | 封鎖釘選;在封鎖 pin 之前可能會傳回。                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | 解除封鎖 pin。                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | 封鎖 pin。                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | 等候指定的事件收到信號。                                                                                  |
| 公用方法                                                                                  | 描述                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | 函式方法。                                                                                                           |
| [**~ CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | 函式方法。                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | 指定 [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) 指標和停止事件。                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | 要求連接的輸入 pin 以開始清除作業。                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | 要求連接的輸入 pin 以結束排清操作。                                                                    |
| [**非使用中**](cdynamicoutputpin-inactive.md)                                                  | 通知釘選篩選已停止。                                                                                 |
| [**使用中**](cdynamicoutputpin-active.md)                                                      | 通知釘選篩選現在已啟用。                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | 完成輸入 pin 的連接。 虛擬。                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | 取得串流作業的 pin 存取權。 虛擬。                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | 在串流作業之後釋放對 pin 的存取。 虛擬。                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | 判斷任何執行緒是否正在執行釘選的串流作業。 虛擬。                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | 動態變更連接的媒體類型，並提供新的區段資訊。                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | 動態變更連接的媒體類型。                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | 以新的媒體類型執行動態重新連接。                                                                        |
| IPin 方法                                                                                    | 描述                                                                                                                   |
| [**中斷連線**](cdynamicoutputpin-disconnect.md)                                              | 中斷目前的 pin 連接。                                                                                            |
| IPinFlowControl 方法                                                                         | 描述                                                                                                                   |
| [**封鎖**](cdynamicoutputpin-block.md)                                                        | 封鎖或解除封鎖來自 pin 的資料流程程。                                                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 





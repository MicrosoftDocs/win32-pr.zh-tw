---
description: 延後的命令會藉由呼叫 IQueueCommand 介面上的方法來排入佇列，並由篩選圖形管理員和某些篩選器公開。
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: CDeferredCommand 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109701"
---
# <a name="cdeferredcommand-class"></a>CDeferredCommand 類別

![cdeferredcommand 類別階層](images/cutil13.png)

延後的命令會藉由呼叫 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) 介面上的方法來排入佇列，並由篩選圖形管理員和某些篩選器公開。 成功呼叫其中一個方法會傳回 [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) 介面，代表已排入佇列的命令。

`CDeferredCommand`物件代表單一延後命令，並公開 [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand)介面，以及允許時間檢查和實際執行的其他方法。 `CDeferredCommand`物件包含其排入佇列之 [**CCmdQueue**](ccmdqueue.md)物件的參考。

參考計數控制類別的存留期 `CDeferredCommand` 。 呼叫 [**CDeferredCommand：： Invoke**](cdeferredcommand-invoke.md) 成員函式時，呼叫端應用程式會取得參考計數的介面指標，而 [**CCmdQueue**](ccmdqueue.md) 物件也會在延後的命令上保存參考計數。 呼叫 [**IDeferredCommand：： Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) 成員函式會從命令佇列中取出延後的命令，因此會將參考計數減少一。 從佇列中移除之後，就無法將命令放回佇列中。



| 受保護的資料成員                                        | Description                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | [**資料流程時間**](stream-time.md)或呈現時間的旗標。 傳遞給叫用的方法。                   |
| m \_ 分派                                                   | 存取 **ITypeInfo** 介面。                                                                                   |
| m \_ dispidMethod                                               | 要執行之介面上的方法。                                                                                         |
| m \_ DispParams                                                 | 包含 **DISPPARAMS** 參數清單的 [**CDispParams**](cdispparams.md)物件                                  |
| m \_ hrResult                                                   | 儲存傳回的 **HRESULT** 值。                                                                                  |
| m \_ iid                                                        | 介面 (**GUID**) 的全域唯一識別碼。                                                                 |
| m \_ pQueue                                                     | 公開 [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)介面之 [**CCmdQueue**](ccmdqueue.md)物件的指標。 |
| m \_ pUnk                                                       | 將在其上執行命令之介面的 **IUnknown** 指標。                                                 |
| m \_ pvarResult                                                 | 來自已叫用方法的結果資訊（如果有的話）。                                                                 |
| m \_ 時間                                                       | 執行命令的時間。                                                                                  |
| m \_ wFlags                                                     | 指定調用內容的旗標。                                                                         |
| 成員函數                                              | Description                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | 結構 **CDeferredCommand** 物件。                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | 抓取與延後命令相關聯的內容旗標。                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | 抓取將在其上執行方法之介面 (IID) 的介面識別碼。                              |
| [**GetMethod**](cdeferredcommand-getmethod.md)               | 捕獲要執行之方法的分派識別碼。                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | 抓取方法的 **DISPPARAMS** 引數清單。                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | 抓取產生的引數清單（如果有的話）。                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | 抓取方法將執行的時間。                                                                         |
| [**調用**](cdeferredcommand-invoke.md)                     | 提供物件所公開之方法和屬性的存取權。                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | 指定是否要在資料流程時間或呈現時間執行命令。                                         |
| IDeferredCommand 方法                                      | Description                                                                                                             |
| [**取消**](cdeferredcommand-cancel.md)                     | 取消先前已排入佇列的 [**CDeferredCommand：： Invoke**](cdeferredcommand-invoke.md) 要求。                        |
| [**信賴度**](cdeferredcommand-confidence.md)             | 目前未實作。                                                                                              |
| [**延期**](cdeferredcommand-postpone.md)                 | 為先前佇列的命令指定新的呈現時間。                                                      |
| [**GetHResult**](cdeferredcommand-gethresult.md)             | 抓取已叫用方法的 **HRESULT** 值。                                                                  |



 

 

 




---
description: 正在抓取事件
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: 正在抓取事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1132b2b0140c86c2be1e7916e8d1de28e231b2eca50596714aaa82346aaf83eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072722"
---
# <a name="retrieving-events"></a>正在抓取事件

篩選 Graph 管理員會公開支援事件通知的三個介面。

-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 包含篩選準則以張貼事件的方法。
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 包含應用程式取出事件的方法。
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 繼承自 [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) 介面並加以擴充。

藉由在篩選 Graph 管理員上呼叫 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)方法，篩選 post 事件通知。 事件通知是由定義事件種類的事件程式碼，以及提供額外資訊的兩個參數所組成。 視事件程式碼而定，參數可能包含指標、傳回碼、參考時間或其他資訊。 如需事件代碼和參數的完整清單，請參閱 [事件通知碼](event-notification-codes.md)。

若要從佇列中取出事件，應用程式會在篩選 Graph 管理員上呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)方法。 這個方法會封鎖，直到有要傳回的事件或超過指定的時間為止。 假設有一個已排入佇列的事件，則方法會傳回，其中包含事件程式碼和兩個事件參數。 在呼叫 **GetEvent** 之後，應用程式一律會呼叫 [**IMediaEvent：： FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) 方法來釋放任何與事件參數相關聯的資源。 例如，參數可能是篩選圖形所配置的 **BSTR** 值。

下列程式碼範例提供如何從佇列中取出事件的大綱。


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



若要覆寫篩選 Graph 管理員的預設處理事件，請以事件程式碼做為參數來呼叫 [**IMediaEvent：： CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling)方法。 您可以藉由呼叫 [**IMediaEvent：： RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) 方法，恢復預設處理。 如果篩選圖形針對指定的事件程式碼不會執行任何預設處理，則呼叫這些方法並不會有任何作用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




---
description: 清除資料
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: 清除資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687495"
---
# <a name="flushing-data"></a>清除資料

下列虛擬虛擬顯示如何執行 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法：


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



當排清開始時， **BeginFlush** 方法會採用篩選鎖定，以序列化狀態變更。 由於清除作業會在應用程式執行緒上進行，而且串流執行緒可能會在 **接收** 呼叫的過程中，因此無法安全地使用串流鎖定。 Pin 必須保證 **接收** 未遭到封鎖，且任何後續的 **接收** 呼叫都將會失敗。 [**CBaseInputPin：： BeginFlush**](cbaseinputpin-beginflush.md)方法會設定內部旗標（ [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md)）。 當旗標為 **TRUE** 時， **Receive** 方法會失敗。

藉由提供下游的 **BeginFlush** 呼叫，pin 可保證所有下游篩選器都會釋放其範例，並從 **接收** 呼叫傳回。 這接著保證輸入的 pin 不會被封鎖等候 **GetBuffer** 或 **接收**。 如果您的 pin **接收方法會** 等待事件 (例如，若要取得資源) ， **BeginFlush** 方法應藉由設定事件來強制終止等候。 此時， **Receive** 方法保證會傳回，而 **m \_ bFlushing** 旗標會防止新的 **接收** 呼叫執行任何工作。

針對某些篩選器，所有 **BeginFlush** 都需要這麼做。 **EndFlush** 方法會向篩選發出通知，讓它可以再次開始接收範例。 其他篩選器可能需要在 **BeginFlush** 中使用也可用於 **接收** 的變數或資源。 在這種情況下，篩選應先保存串流鎖定。 在上述任何步驟之前，請務必不要這麼做，因為您可能會造成鎖死。

**EndFlush** 方法會保存篩選鎖定，並傳播呼叫下游：


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



[**CBaseInputPin：： EndFlush**](cbaseinputpin-endflush.md)方法會將 **m \_ bFlushing** 旗標重設為 **FALSE**，讓 **Receive** 方法再次開始接收範例。 這應該是 **EndFlush** 中的最後一個步驟，因為 pin 必須等到清除完成，而且所有下游篩選都收到通知，才能接收任何範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行緒和重要區段](threads-and-critical-sections.md)
</dt> </dl>

 

 




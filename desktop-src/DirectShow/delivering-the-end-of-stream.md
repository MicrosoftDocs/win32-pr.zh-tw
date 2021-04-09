---
description: 傳遞資料流程結尾
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: 傳遞資料流程結尾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845859"
---
# <a name="delivering-the-end-of-stream"></a>傳遞資料流程結尾

當輸入 pin 收到資料流程結束通知時，它會傳播呼叫下游。 從這個輸入 pin 接收資料的任何下游篩選也都應該取得資料流程結束通知。 同樣地，請採用資料流程鎖定而不是篩選鎖定。 如果篩選準則有尚未傳遞的暫止資料，則篩選準則應該會在傳送資料流程結束通知之前立即傳遞。 它不應該在資料流程結尾之後傳送任何資料。


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



[**CBaseOutputPin：:D eliverendofstream**](cbaseoutputpin-deliverendofstream.md)方法會在下游輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行緒和重要區段](threads-and-critical-sections.md)
</dt> </dl>

 

 




---
description: 接收和傳遞範例
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: 接收和傳遞範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846155"
---
# <a name="receiving-and-delivering-samples"></a>接收和傳遞範例

下列虛擬虛擬顯示如何執行 **IMemInput：： Receive** 方法：


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



**Receive 方法會** 保存串流鎖定，而不是篩選鎖定。 篩選可能需要等待某個事件，才能處理資料，如下所示，呼叫 **WaitForSingleObject**。 並非每個篩選都需要這麼做。 [**CBaseInputPin：： Receive 方法會**](cbaseinputpin-receive.md)驗證一些一般串流狀況。 \_ \_ 如果篩選已停止，則會傳回 VFW E 錯誤的 \_ 狀態， \_ 如果篩選器正在排清，則傳回 FALSE。 S \_ [確定] 以外的任何傳回碼表示 **Receive** 方法應該立即傳回，而不是處理範例。

處理範例之後，請呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md)，將它傳遞至下游篩選器。 此 helper 方法會在下游輸入 pin 上呼叫 **IMemInputPin：： Receive** 。 篩選器可能會將範例傳遞給數個 pin。

 

 




---
title: 啟動單一計時器事件
description: 啟動單一計時器事件
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- 多媒體計時器，事件
- 計時器，事件
- 多媒體計時器，啟動事件
- 計時器，啟動事件
- timeSetEvent 函式
- 啟動計時器事件
- 單一計時器事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc3a4c69aefe8df3310c8ff974ef7592b435eabccd661bdbeb1ebbf85dc3c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037168"
---
# <a name="starting-a-single-timer-event"></a>啟動單一計時器事件

> [!Note]  
> 本主題說明過時的函式。 新的應用程式應該使用 [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函式來建立計時器。

 

若要啟動單一計時器事件，請呼叫 [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) 函式，並指定回呼發生之前的時間量、解析度、回呼函式的位址 (查看 [**TimeProc**](/previous-versions//dd757631(v=vs.85))) ，以及要提供給回呼函數的使用者資料。 應用程式可以使用類似下列的函式來啟動單一計時器事件。


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



如需回呼函式 OneShotCallback 的範例，請參閱 [撰寫計時器回呼函數](writing-a-timer-callback-function.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多媒體計時器](using-multimedia-timers.md)
</dt> </dl>

 

 
---
title: 取消計時器事件
description: 取消計時器事件
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- 多媒體計時器，事件
- 計時器，事件
- timeKillEvent 函式
- 取消計時器事件
- 多媒體計時器，取消事件
- 計時器，取消事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4e9a92a02dca8ffd4723685fc96cdb0f82fc34a0fa2e3481a71a51997c316
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691789"
---
# <a name="canceling-a-timer-event"></a>取消計時器事件

> [!Note]  
> 本主題說明過時的函式。 新的應用程式應該使用 [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函式來建立計時器。

 

針對透過呼叫 [**timeSetEvent**](/previous-versions//dd757634(v=vs.85))來建立的每個定期計時器，應用程式必須在釋放包含回呼函式的記憶體之前，先呼叫 [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) 函數來取消計時器。 若要取消計時器事件，它可能會呼叫下列函數。


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多媒體計時器](using-multimedia-timers.md)
</dt> </dl>

 

 
---
title: 撰寫計時器回呼函數
description: 撰寫計時器回呼函數
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- 多媒體計時器，回呼函數
- 計時器，回呼函數
- 撰寫計時器回呼函數
- 多媒體計時器，撰寫回呼函式
- 計時器，撰寫回呼函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933147"
---
# <a name="writing-a-timer-callback-function"></a>撰寫計時器回呼函數

> [!Note]  
> 本主題說明過時的函式。 新的應用程式應該使用 [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) 函式來建立計時器。

 

下列回呼函式 OneShotTimer 會使單一計時器事件的識別碼失效，並呼叫計時器常式來處理應用程式特定的工作。 如需詳細資訊，請參閱 [**TimeProc**](/previous-versions//dd757631(v=vs.85))。


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多媒體計時器](using-multimedia-timers.md)
</dt> </dl>

 

 
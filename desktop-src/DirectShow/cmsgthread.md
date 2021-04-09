---
description: CMsgThread 類別是一個背景工作執行緒類別，會將要求排入佇列執行緒以進行非同步完成。
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: CMsgThread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688452"
---
# <a name="cmsgthread-class"></a>CMsgThread 類別

`CMsgThread`類別是一種背景工作執行緒類別，會將要求排入佇列執行緒以進行非同步完成。 若要使用此類別，請從它衍生您的類別，並覆寫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。 **ThreadMessageProc** 成員函式會執行每個要求。 您的用戶端函數和 **ThreadMessageProc** 成員函式必須共用 [**CMsg**](cmsg.md) 物件中參數的一般定義。

協商的機制會告知工作者執行緒結束。 一般來說，這會是 [**CMsg**](cmsg.md) 類別的 **uMsg** 訊息代碼的其中一個值。

最好從衍生類別的函式傳送此訊息，並在完成衍生類別的終結之前呼叫 [**CMsgThread：： WaitForThreadExit**](cmsgthread-waitforthreadexit.md) 成員函式。



| 受保護的資料成員                                    | Description                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | 指出用於信號的控制碼。                                                                                                |
| m \_ 鎖定                                                   | 保護對清單的存取。                                                                                                             |
| m \_ lWaiting                                               | 指出等候可用的執行緒。                                                                                                  |
| m \_ ThreadQueue                                            | 覆寫 [**CMsgThread：： GetThreadMsg**](cmsgthread-getthreadmsg.md) 成員函式和封鎖非此佇列的專案。 |
| 成員函數                                          | Description                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | 結構 **CMsgThread** 物件。                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | 建立執行緒。                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | 抓取執行緒控制碼。                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | 抓取執行緒的識別碼。                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | 抓取目前的執行緒優先權。                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | 將背景工作執行緒執行的要求排在佇列中。                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | 繼續進行工作者執行緒的操作。                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | 將執行緒的優先權設定為新的值。                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | 暫停執行中線程的操作。                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | 封鎖直到執行緒在呼叫 [**CMsgThread：： SuspendThread**](cmsgthread-suspendthread.md) 成員函式之後結束為止。 |
| 可覆寫的成員函式                              | Description                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | 抓取包含要求的佇列 [**CMsg**](cmsg.md) 物件。                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | 提供執行緒的初始化。                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | 處理要求。 這是單純的虛擬成員函式。                                                                           |



 

 

 




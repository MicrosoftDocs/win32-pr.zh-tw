---
description: 執行緒可以暫停和繼續執行另一個執行緒。 當執行緒暫停時，不會排定在處理器上的時間。
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: 暫停執行緒執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf3ecf2bee1f14ae8571cb7e7402e32a636f4a35ca5c182d32a2a636ed85dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793155"
---
# <a name="suspending-thread-execution"></a>暫停執行緒執行

執行緒可以暫停和繼續執行另一個執行緒。 當執行緒暫停時，不會排定在處理器上的時間。

如果以暫停狀態建立執行緒 (使用 [ [**建立 \_ 擱置**](process-creation-flags.md) ] 旗標) ，則在另一個執行緒呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函式時，將不會開始執行，直到另一個執行緒呼叫已暫止執行緒的控制碼為止。 這有助於線上程開始執行之前初始化執行緒的狀態。 在建立時暫停執行緒可能有助於單次同步處理，因為這樣可確保當您呼叫 **ResumeThread** 時，暫停的執行緒將會執行其程式碼的起始點。

[**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)函式不適合用于執行緒同步處理，因為它不會控制在程式碼中暫停執行緒執行的時間點。 這項功能主要是設計來供偵錯工具使用。

執行緒可能會藉由呼叫 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) 或 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) 函式來暫時產生其執行，這線上程回應使用者互動的情況下特別有用，因為它可能會順延強制的時間足以讓使用者觀察其動作的結果。 在睡眠間隔期間，執行緒不會排定在處理器上的時間。

[**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)函式類似于 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep)和 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)，不同之處在于您無法指定間隔。 **SwitchToThread** 可讓執行緒產生其時間配量。

 

 

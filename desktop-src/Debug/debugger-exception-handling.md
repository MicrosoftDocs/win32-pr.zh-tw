---
description: 系統的使用者模式例外狀況處理可支援精密的偵錯工具。
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: 偵錯工具例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467957"
---
# <a name="debugger-exception-handling"></a>偵錯工具例外狀況處理

系統的使用者模式例外狀況處理可支援精密的偵錯工具。 如果發生例外狀況的處理常式正在進行中，系統會產生一個 debug 事件。 如果偵錯工具使用 [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) 函式，debug 事件會導致該函式以指向 [**debug \_ 事件**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) 結構的指標傳回。 此結構包含偵錯工具和執行緒識別碼，可供偵錯工具用來存取執行緒的內容記錄。 此結構也包含例外狀況的 [**\_ DEBUG \_ 資訊**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) 結構，其中包含例外狀況記錄的複本。

當系統搜尋例外狀況處理常式時，會進行兩次嘗試來通知進程的偵錯工具。 第一個通知嘗試會提供偵錯工具處理中斷點或單一步驟例外狀況的機會。 這就是所謂的 *第一次通知*。 然後，使用者就可以在執行任何例外狀況處理常式之前，發出偵錯工具命令來操作進程的環境。 只有當系統找不到處理例外狀況的以框架為基礎的例外狀況處理常式時，才會嘗試第二次通知偵錯工具。 這就是所謂的 *最後機會通知*。 如果偵錯工具未在最後一次發生通知之後處理例外狀況，則系統會終止正在進行調試的進程。

在每次嘗試時，偵錯工具都會使用 [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) 函式將控制權交還給系統。 在傳回控制權之前，偵錯工具可以處理例外狀況，並適當地修改執行緒狀態，也可以選擇不要處理例外狀況。 使用 **ContinueDebugEvent** 時，偵錯工具可能會指出它已處理例外狀況，在此情況下，電腦狀態會還原，而執行緒執行會在發生例外狀況的時間點繼續執行。 偵錯工具也可以表示它未處理例外狀況，這會導致系統繼續搜尋例外狀況處理常式。

 

 

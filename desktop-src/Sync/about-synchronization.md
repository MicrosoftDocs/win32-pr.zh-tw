---
description: 若要同步存取資源，請使用其中一個 wait 函數中的其中一個同步處理物件。
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: 關於同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983791"
---
# <a name="about-synchronization"></a>關於同步處理

若要同步存取資源，請使用其中一個[wait 函數](wait-functions.md)中的其中一個[同步處理物件](synchronization-objects.md)。 同步處理物件的狀態為「已 *發出信號* 」或「 *未收到信號*」。 等候函式可讓執行緒封鎖本身的執行，直到指定的未收到信號物件設定為已發出信號的狀態。 如需詳細資訊，請參閱 [進程間同步](interprocess-synchronization.md)處理。

以下是其他同步處理機制：

-   [重迭的輸入和輸出](synchronization-and-overlapped-input-and-output.md)
-   [非同步程序呼叫](asynchronous-procedure-calls.md)
-   [重要區段物件](critical-section-objects.md)
-   [條件變數](condition-variables.md)
-   [超薄讀取器/寫入器鎖定](slim-reader-writer--srw--locks.md)
-   [單次初始化](one-time-initialization.md)
-   [連鎖變數存取](interlocked-variable-access.md)
-   [連鎖單向連結清單](interlocked-singly-linked-lists.md)
-   [計時器佇列](timer-queues.md)
-   [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)宏

如需同步處理的詳細資訊，請參閱 [同步處理和多處理器問題](synchronization-and-multiprocessor-issues.md)。

 

 

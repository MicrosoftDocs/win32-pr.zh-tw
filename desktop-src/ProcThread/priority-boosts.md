---
description: 每個執行緒都有動態優先權。
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: 優先權提升
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192758"
---
# <a name="priority-boosts"></a>優先權提升

每個執行緒都有 *動態優先權*。 這是排程器用來判斷要執行哪個執行緒的優先權。 一開始，執行緒的動態優先權與其基底優先權相同。 系統可以提升和降低動態優先順序，以確保它有回應，而且沒有任何執行緒會耗盡處理器時間。 系統不會提高基底優先權層級介於16到31之間的執行緒優先順序。 只有基底優先順序介於0和15之間的執行緒才能獲得動態優先權。

系統會提高執行緒的動態優先順序，以增強其回應性，如下所示。

-   當使用 NORMAL \_ PRIORITY 類別的進程 \_ 進入前景時，排程器會提高與前景視窗相關聯之進程的優先權類別，使其大於或等於任何背景進程的 priority 類別。 當進程不再存在於前景時，優先順序類別會回到其原始的設定。
-   當視窗接收到輸入（例如計時器訊息、滑鼠訊息或鍵盤輸入）時，排程器會提高擁有視窗之執行緒的優先順序。
-   當滿足已封鎖執行緒的等候條件時，排程器會提高執行緒的優先順序。 例如，當與磁片或鍵盤 i/o 相關聯的等候操作完成時，執行緒會獲得優先權提升。

    您可以藉由呼叫 [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) 或 [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) 函式來停用優先權提升功能。 若要判斷是否已停用此功能，請呼叫 [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) 或 [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) 函式。

在引發執行緒的動態優先順序之後，排程器會在每次執行緒完成時間配量時，將該優先權降到一層級，直到執行緒回復為其基底優先順序為止。 執行緒的動態優先權絕對不會小於其基底優先順序。

 

 

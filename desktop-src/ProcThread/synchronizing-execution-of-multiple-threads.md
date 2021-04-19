---
description: 為了避免競爭情況和鎖死，必須將多個執行緒的存取權同步至共用資源。 也需要同步處理，以確保相依的程式碼會以正確的循序執行。
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: 同步處理多個執行緒的執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986931"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>同步處理多個執行緒的執行

為了避免競爭情況和鎖死，必須將多個執行緒的存取權同步至共用資源。 也需要同步處理，以確保相依的程式碼會以正確的循序執行。

有一些物件可以用來同步處理多個執行緒。 這些物件包括：

-   主控台輸入緩衝區
-   事件
-   Mutex
-   處理序
-   信號燈
-   執行緒
-   計時器

每個物件的狀態為已發出信號或未收到信號。 當您在其中一個 [等候](../sync/wait-functions.md)函式的呼叫中指定任何這些物件的控制碼時，會封鎖呼叫執行緒的執行，直到指定物件的狀態變成發出信號為止。

在某些事件發生之前，這些物件中的某些物件很適合用來封鎖執行緒。 例如，當有未讀取的輸入時（例如擊鍵或按滑鼠按鍵），主控台輸入緩衝區控制碼就會收到信號。 進程和執行緒控制碼會在進程或執行緒終止時收到信號。 例如，這可以讓進程建立子進程，然後封鎖它自己的執行，直到新的進程終止為止。

其他物件適用于保護共用資源免于同時存取。 例如，多個執行緒可以有 mutex 物件的控制碼。 在存取共用資源之前，執行緒必須呼叫其中一個 [等候](../sync/wait-functions.md) 函式，等候 mutex 的狀態被告知。 當 mutex 變成信號時，只會釋放一個等候中的執行緒以存取資源。 Mutex 的狀態會立即重設為未收到信號，因此任何其他等候中的執行緒都會保持封鎖狀態。 當執行緒完成資源時，它必須將 mutex 的狀態設定為已收到信號，以允許其他執行緒存取資源。

針對單一進程的執行緒，重要區段物件提供比 mutex 更有效率的同步處理方法。 重要區段會像 mutex 一樣用來一次啟用一個執行緒，以使用受保護的資源。 執行緒可以使用 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) 函數來要求重要區段的擁有權。 如果它已經由另一個執行緒所擁有，則會封鎖要求的執行緒。 執行緒可以使用 [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) 函數來要求重要區段的擁有權，而不會在無法取得重要區段時封鎖。 在接收到擁有權之後，執行緒就可以自由使用受保護的資源。 除非進程的其他執行緒嘗試進入相同的重要區段，否則這些執行緒的執行不會受到影響。

[**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)函式會讓執行緒等候，直到指定的進程初始化，並等候使用者輸入，但沒有任何暫止的輸入。 呼叫 **WaitForInputIdle** 有助於同步處理父系和子進程，因為 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 會傳回，而不會等待子進程完成其初始化。

如需詳細資訊，請參閱 [同步](../sync/synchronization.md)處理。

 

 

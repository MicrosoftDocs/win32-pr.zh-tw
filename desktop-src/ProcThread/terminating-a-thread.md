---
description: 終止執行緒的結果如下：會釋放執行緒所擁有的任何資源，例如 windows 和勾點。已設定執行緒結束代碼。執行緒物件已收到信號。如果執行緒是進程中唯一的作用中線程，進程就會終止。 如需詳細資訊，請參閱終止進程。
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: "  終結執行緒"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978961"
---
# <a name="terminating-a-thread"></a>  終結執行緒

終止執行緒有下列結果：

-   執行緒所擁有的任何資源（例如 windows 和勾點）都會釋出。
-   已設定執行緒結束代碼。
-   執行緒物件已收到信號。
-   如果執行緒是進程中唯一的作用中線程，進程就會終止。 如需詳細資訊，請參閱 [終止進程](terminating-a-process.md)。

[**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)函數會傳回執行緒的終止狀態。 當執行緒正在執行時，其終止狀態仍在作用中 \_ 。 當執行緒終止時，它的終止狀態會從 [作用中] 變更 \_ 為 [執行緒的結束代碼]。

當執行緒終止時，執行緒物件的狀態會變更為 [已發出信號]，釋出等候執行緒終止的任何其他執行緒。 如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。

當執行緒終止時，除非關閉執行緒的所有開啟控制碼，否則它的執行緒物件不會釋放。

## <a name="how-threads-are-terminated"></a>如何終止執行緒

執行緒會執行，直到發生下列其中一個事件為止：

-   執行緒會呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) 函數。
-   進程的任何執行緒都會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。
-   執行緒函數會傳回。
-   任何執行緒都會以執行緒的控制碼呼叫 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) 函數。
-   任何執行緒都會以進程的控制碼呼叫 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 函數。

執行緒的結束代碼是對 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)、 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)、 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)或 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)的呼叫中指定的值，或執行緒函數所傳回的值。

如果執行緒終止 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)，系統就會呼叫每個附加 DLL 的進入點函式，其值表示執行緒從 DLL 卸離 (除非您) 呼叫 [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) 函數。 如果執行緒由 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)終止，則會叫用 DLL 進入點函數一次，以表示進程正在卸離。 [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)或 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止執行緒時，不會通知 dll。 如需 Dll 的詳細資訊，請參閱 [動態連結程式庫](../dlls/dynamic-link-libraries.md)。

[**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)和 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)函式應該只在極端的情況下使用，因為它們不允許執行緒清除，也不會通知附加的 dll，也不會釋放初始堆疊。 此外，在進程終止之前，不會關閉執行緒所擁有之物件的控制碼。 下列步驟提供更好的解決方案：

-   使用 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數建立事件物件。
-   建立執行緒。
-   每個執行緒藉由呼叫 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 函數來監視事件狀態。 使用零的等候逾時間隔。
-   當事件設定為信號狀態時，每個執行緒都會終止本身的執行 ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 會傳回 WAIT \_ 物件 \_ 0) 。

 

 

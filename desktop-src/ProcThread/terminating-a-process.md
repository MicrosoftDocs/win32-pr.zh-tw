---
description: 終止處理常式的結果如下：進程中所有剩餘的執行緒都會標示為終止。進程所配置的任何資源都會釋出。所有核心物件都已關閉。處理常式程式碼會從記憶體中移除。已設定進程結束代碼。進程物件有信號。
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: 終止進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d1a97b2b7342b67eaab72cae244b188df4cfeafbf2875d3bd62136ab6139748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081298"
---
# <a name="terminating-a-process"></a>終止進程

終止進程有下列結果：

-   進程中的其餘執行緒都會標示為終止。
-   進程所配置的任何資源都會釋出。
-   所有核心物件都已關閉。
-   處理常式程式碼會從記憶體中移除。
-   已設定進程結束代碼。
-   進程物件有信號。

當進程終止時，核心物件的開啟控制碼會自動關閉，物件本身會一直存在，直到所有開啟的控制碼都關閉為止。 因此，如果另一個進程具有開啟的控制碼，則在使用它的進程結束之後，物件將會保持有效。

[**>Getexitcodeprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)函數會傳回進程的終止狀態。 當進程正在執行時，其終止狀態仍在作用中 \_ 。 當進程結束時，其終止狀態會從 [作用中] 變更為 [進程的結束 \_ 代碼]。

當進程結束時，進程物件的狀態會變成發出信號，釋出等候進程終止的任何執行緒。 如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。

當系統結束進程時，不會終止進程所建立的任何子進程。 終止進程並不會產生 WH CBT 攔截 \_ 程式的通知。

您可以使用 [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) 函式來指定系統關機時進程終止的某些層面，例如，當進程相對於系統中的其他進程時，就會終止。

## <a name="how-processes-are-terminated"></a>進程如何終止

進程會執行，直到發生下列其中一個事件為止：

-   進程的任何執行緒都會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。 請注意，如果進程的主要執行緒傳回，某些 C 執行時間程式庫的執行 (CRT) 呼叫 **ExitProcess** 。
-   進程的最後一個執行緒終止。
-   任何執行緒都會以進程的控制碼呼叫 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 函數。
-   若為主控台進程，當主控台收到 CTRL + C 或 CTRL + 中斷信號時，預設的 [主控台控制處理常式](/windows/console/console-control-handlers) 會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 。
-   使用者關閉系統或登出。

除非進程的執行緒處於已知狀態，否則請勿終止進程。 如果執行緒在核心物件上等候，則在等候完成之前，將不會終止。 這可能會導致應用程式停止回應。

主要執行緒可以避免終止其他執行緒，方法是將它們導向以呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ，然後再使進程終止 (如需詳細資訊，請參閱 [終止執行緒](terminating-a-thread.md)) 。 主要執行緒仍可以在之後呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ，以確保所有線程都會終止。

進程的結束代碼是 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 或 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)呼叫中所指定的值，或是進程的 main 或 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函數所傳回的值。 如果進程因為嚴重的例外狀況而終止，結束代碼就是造成終止的例外狀況值。 此外，當發生例外狀況時，會使用這個值做為所有執行中線程的結束代碼。

如果 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)終止進程，系統就會呼叫每個附加 DLL 的進入點函式，其值表示進程會從 DLL 卸離。 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止進程時，不會通知 dll。 如需 Dll 的詳細資訊，請參閱 [動態連結程式庫](../dlls/dynamic-link-libraries.md)。

如果 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止進程，進程的所有線程都會立即終止，而不會有機會執行其他程式碼。 這表示執行緒不會在終止處理常式區塊中執行程式碼。 此外，也不會通知進程正在卸離的任何附加 Dll。 如果您需要讓一個進程終止另一個進程，下列步驟會提供較佳的解決方案：

-   這兩個進程都呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) 函式來建立私用訊息。
-   一個進程可以使用 [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) 函式廣播私用訊息來終止另一個進程，如下所示：

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   接收私用訊息的處理常式會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 來終止其執行。

[**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)、 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)、 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)、 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函數的執行會在位址空間內進行序列化。 適用以下限制：

-   在處理常式啟動和 DLL 初始化常式期間，可以建立新的執行緒，但在處理常式的 DLL 初始化完成之前，不會開始執行。
-   一次只能有一個執行緒在 DLL 初始化或卸離常式中。
-   除非執行緒的 DLL 初始化或卸離常式中沒有任何執行緒，否則 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式不會傳回。

 

 

---
description: 終止處理常式的結果如下：進程中所有剩餘的執行緒都會標示為終止。進程所配置的任何資源都會釋出。所有核心物件都已關閉。處理常式程式碼會從記憶體中移除。已設定進程結束代碼。進程物件有信號。
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: 終止進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983629"
---
# <a name="terminating-a-process"></a><span data-ttu-id="23170-103">終止進程</span><span class="sxs-lookup"><span data-stu-id="23170-103">Terminating a Process</span></span>

<span data-ttu-id="23170-104">終止進程有下列結果：</span><span class="sxs-lookup"><span data-stu-id="23170-104">Terminating a process has the following results:</span></span>

-   <span data-ttu-id="23170-105">進程中的其餘執行緒都會標示為終止。</span><span class="sxs-lookup"><span data-stu-id="23170-105">Any remaining threads in the process are marked for termination.</span></span>
-   <span data-ttu-id="23170-106">進程所配置的任何資源都會釋出。</span><span class="sxs-lookup"><span data-stu-id="23170-106">Any resources allocated by the process are freed.</span></span>
-   <span data-ttu-id="23170-107">所有核心物件都已關閉。</span><span class="sxs-lookup"><span data-stu-id="23170-107">All kernel objects are closed.</span></span>
-   <span data-ttu-id="23170-108">處理常式程式碼會從記憶體中移除。</span><span class="sxs-lookup"><span data-stu-id="23170-108">The process code is removed from memory.</span></span>
-   <span data-ttu-id="23170-109">已設定進程結束代碼。</span><span class="sxs-lookup"><span data-stu-id="23170-109">The process exit code is set.</span></span>
-   <span data-ttu-id="23170-110">進程物件有信號。</span><span class="sxs-lookup"><span data-stu-id="23170-110">The process object is signaled.</span></span>

<span data-ttu-id="23170-111">當進程終止時，核心物件的開啟控制碼會自動關閉，物件本身會一直存在，直到所有開啟的控制碼都關閉為止。</span><span class="sxs-lookup"><span data-stu-id="23170-111">While open handles to kernel objects are closed automatically when a process terminates, the objects themselves exist until all open handles to them are closed.</span></span> <span data-ttu-id="23170-112">因此，如果另一個進程具有開啟的控制碼，則在使用它的進程結束之後，物件將會保持有效。</span><span class="sxs-lookup"><span data-stu-id="23170-112">Therefore, an object will remain valid after a process that is using it terminates if another process has an open handle to it.</span></span>

<span data-ttu-id="23170-113">[**>getexitcodeprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)函數會傳回進程的終止狀態。</span><span class="sxs-lookup"><span data-stu-id="23170-113">The [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) function returns the termination status of a process.</span></span> <span data-ttu-id="23170-114">當進程正在執行時，其終止狀態仍在作用中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="23170-114">While a process is executing, its termination status is STILL\_ACTIVE.</span></span> <span data-ttu-id="23170-115">當進程結束時，其終止狀態會從 [作用中] 變更為 [進程的結束 \_ 代碼]。</span><span class="sxs-lookup"><span data-stu-id="23170-115">When a process terminates, its termination status changes from STILL\_ACTIVE to the exit code of the process.</span></span>

<span data-ttu-id="23170-116">當進程結束時，進程物件的狀態會變成發出信號，釋出等候進程終止的任何執行緒。</span><span class="sxs-lookup"><span data-stu-id="23170-116">When a process terminates, the state of the process object becomes signaled, releasing any threads that had been waiting for the process to terminate.</span></span> <span data-ttu-id="23170-117">如需同步處理的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="23170-117">For more about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="23170-118">當系統結束進程時，不會終止進程所建立的任何子進程。</span><span class="sxs-lookup"><span data-stu-id="23170-118">When the system is terminating a process, it does not terminate any child processes that the process has created.</span></span> <span data-ttu-id="23170-119">終止進程並不會產生 WH CBT 攔截 \_ 程式的通知。</span><span class="sxs-lookup"><span data-stu-id="23170-119">Terminating a process does not generate notifications for WH\_CBT hook procedures.</span></span>

<span data-ttu-id="23170-120">您可以使用 [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) 函式來指定系統關機時進程終止的某些層面，例如，當進程相對於系統中的其他進程時，就會終止。</span><span class="sxs-lookup"><span data-stu-id="23170-120">Use the [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) function to specify certain aspects of the process termination at system shutdown, such as when a process should terminate relative to the other processes in the system.</span></span>

## <a name="how-processes-are-terminated"></a><span data-ttu-id="23170-121">進程如何終止</span><span class="sxs-lookup"><span data-stu-id="23170-121">How Processes are Terminated</span></span>

<span data-ttu-id="23170-122">進程會執行，直到發生下列其中一個事件為止：</span><span class="sxs-lookup"><span data-stu-id="23170-122">A process executes until one of the following events occurs:</span></span>

-   <span data-ttu-id="23170-123">進程的任何執行緒都會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。</span><span class="sxs-lookup"><span data-stu-id="23170-123">Any thread of the process calls the [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function.</span></span> <span data-ttu-id="23170-124">請注意，如果進程的主要執行緒傳回，某些 C 執行時間程式庫的執行 (CRT) 呼叫 **ExitProcess** 。</span><span class="sxs-lookup"><span data-stu-id="23170-124">Note that some implementation of the C run-time library (CRT) call **ExitProcess** if the primary thread of the process returns.</span></span>
-   <span data-ttu-id="23170-125">進程的最後一個執行緒終止。</span><span class="sxs-lookup"><span data-stu-id="23170-125">The last thread of the process terminates.</span></span>
-   <span data-ttu-id="23170-126">任何執行緒都會以進程的控制碼呼叫 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) 函數。</span><span class="sxs-lookup"><span data-stu-id="23170-126">Any thread calls the [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) function with a handle to the process.</span></span>
-   <span data-ttu-id="23170-127">若為主控台進程，當主控台收到 CTRL + C 或 CTRL + 中斷信號時，預設的 [主控台控制處理常式](/windows/console/console-control-handlers) 會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 。</span><span class="sxs-lookup"><span data-stu-id="23170-127">For console processes, the default [console control handler](/windows/console/console-control-handlers) calls [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) when the console receives a CTRL+C or CTRL+BREAK signal.</span></span>
-   <span data-ttu-id="23170-128">使用者關閉系統或登出。</span><span class="sxs-lookup"><span data-stu-id="23170-128">The user shuts down the system or logs off.</span></span>

<span data-ttu-id="23170-129">除非進程的執行緒處於已知狀態，否則請勿終止進程。</span><span class="sxs-lookup"><span data-stu-id="23170-129">Do not terminate a process unless its threads are in known states.</span></span> <span data-ttu-id="23170-130">如果執行緒在核心物件上等候，則在等候完成之前，將不會終止。</span><span class="sxs-lookup"><span data-stu-id="23170-130">If a thread is waiting on a kernel object, it will not be terminated until the wait has completed.</span></span> <span data-ttu-id="23170-131">這可能會導致應用程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="23170-131">This can cause the application to stop responding.</span></span>

<span data-ttu-id="23170-132">主要執行緒可以避免終止其他執行緒，方法是將它們導向以呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ，然後再使進程終止 (如需詳細資訊，請參閱 [終止執行緒](terminating-a-thread.md)) 。</span><span class="sxs-lookup"><span data-stu-id="23170-132">The primary thread can avoid terminating other threads by directing them to call [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) before causing the process to terminate (for more information, see [Terminating a Thread](terminating-a-thread.md)).</span></span> <span data-ttu-id="23170-133">主要執行緒仍可以在之後呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ，以確保所有線程都會終止。</span><span class="sxs-lookup"><span data-stu-id="23170-133">The primary thread can still call [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) afterwards to ensure that all threads are terminated.</span></span>

<span data-ttu-id="23170-134">進程的結束代碼是 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 或 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)呼叫中所指定的值，或是進程的 main 或 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函數所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="23170-134">The exit code for a process is either the value specified in the call to [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) or [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), or the value returned by the main or [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function of the process.</span></span> <span data-ttu-id="23170-135">如果進程因為嚴重的例外狀況而終止，結束代碼就是造成終止的例外狀況值。</span><span class="sxs-lookup"><span data-stu-id="23170-135">If a process is terminated due to a fatal exception, the exit code is the value of the exception that caused the termination.</span></span> <span data-ttu-id="23170-136">此外，當發生例外狀況時，會使用這個值做為所有執行中線程的結束代碼。</span><span class="sxs-lookup"><span data-stu-id="23170-136">In addition, this value is used as the exit code for all the threads that were executing when the exception occurred.</span></span>

<span data-ttu-id="23170-137">如果 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)終止進程，系統就會呼叫每個附加 DLL 的進入點函式，其值表示進程會從 DLL 卸離。</span><span class="sxs-lookup"><span data-stu-id="23170-137">If a process is terminated by [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), the system calls the entry-point function of each attached DLL with a value indicating that the process is detaching from the DLL.</span></span> <span data-ttu-id="23170-138">[**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止進程時，不會通知 dll。</span><span class="sxs-lookup"><span data-stu-id="23170-138">DLLs are not notified when a process is terminated by [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="23170-139">如需 Dll 的詳細資訊，請參閱 [動態連結程式庫](../dlls/dynamic-link-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="23170-139">For more information about DLLs, see [Dynamic-Link Libraries](../dlls/dynamic-link-libraries.md).</span></span>

<span data-ttu-id="23170-140">如果 [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)終止進程，進程的所有線程都會立即終止，而不會有機會執行其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="23170-140">If a process is terminated by [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), all threads of the process are terminated immediately with no chance to run additional code.</span></span> <span data-ttu-id="23170-141">這表示執行緒不會在終止處理常式區塊中執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="23170-141">This means that the thread does not execute code in termination handler blocks.</span></span> <span data-ttu-id="23170-142">此外，也不會通知進程正在卸離的任何附加 Dll。</span><span class="sxs-lookup"><span data-stu-id="23170-142">In addition, no attached DLLs are notified that the process is detaching.</span></span> <span data-ttu-id="23170-143">如果您需要讓一個進程終止另一個進程，下列步驟會提供較佳的解決方案：</span><span class="sxs-lookup"><span data-stu-id="23170-143">If you need to have one process terminate another process, the following steps provide a better solution:</span></span>

-   <span data-ttu-id="23170-144">這兩個進程都呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) 函式來建立私用訊息。</span><span class="sxs-lookup"><span data-stu-id="23170-144">Have both processes call the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to create a private message.</span></span>
-   <span data-ttu-id="23170-145">一個進程可以使用 [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) 函式廣播私用訊息來終止另一個進程，如下所示：</span><span class="sxs-lookup"><span data-stu-id="23170-145">One process can terminate the other process by broadcasting a private message using the [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) function as follows:</span></span>

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

-   <span data-ttu-id="23170-146">接收私用訊息的處理常式會呼叫 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 來終止其執行。</span><span class="sxs-lookup"><span data-stu-id="23170-146">The process receiving the private message calls [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) to terminate its execution.</span></span>

<span data-ttu-id="23170-147">[**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)、 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)、 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)、 [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函數的執行會在位址空間內進行序列化。</span><span class="sxs-lookup"><span data-stu-id="23170-147">The execution of the [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread), and [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions is serialized within an address space.</span></span> <span data-ttu-id="23170-148">適用以下限制：</span><span class="sxs-lookup"><span data-stu-id="23170-148">The following restrictions apply:</span></span>

-   <span data-ttu-id="23170-149">在處理常式啟動和 DLL 初始化常式期間，可以建立新的執行緒，但在處理常式的 DLL 初始化完成之前，不會開始執行。</span><span class="sxs-lookup"><span data-stu-id="23170-149">During process startup and DLL initialization routines, new threads can be created, but they do not begin execution until DLL initialization is finished for the process.</span></span>
-   <span data-ttu-id="23170-150">一次只能有一個執行緒在 DLL 初始化或卸離常式中。</span><span class="sxs-lookup"><span data-stu-id="23170-150">Only one thread at a time can be in a DLL initialization or detach routine.</span></span>
-   <span data-ttu-id="23170-151">除非執行緒的 DLL 初始化或卸離常式中沒有任何執行緒，否則 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式不會傳回。</span><span class="sxs-lookup"><span data-stu-id="23170-151">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function does not return until there are no threads are in their DLL initialization or detach routines.</span></span>

 

 

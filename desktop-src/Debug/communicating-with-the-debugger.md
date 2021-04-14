---
description: OutputDebugString 函式會藉由產生輸出 \_ DEBUG \_ 字串事件的偵錯工具，從正在調試的進程傳送字串至偵錯工具 \_ 。 進程可以藉由呼叫 IsDebuggerPresent 函式來偵測是否正在進行調試。
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: 與偵錯工具通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846948"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="eeb5e-104">與偵錯工具通訊</span><span class="sxs-lookup"><span data-stu-id="eeb5e-104">Communicating with the Debugger</span></span>

<span data-ttu-id="eeb5e-105">[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)函式會藉由產生輸出 \_ DEBUG \_ 字串事件的偵錯工具，從正在調試的進程傳送字串至偵錯工具 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="eeb5e-106">進程可以藉由呼叫 [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) 函式來偵測是否正在進行調試。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="eeb5e-107">[**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)函式會在目前的進程中造成中斷點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="eeb5e-108">中斷點是程式中停止執行的位置，可讓開發人員檢查程式的程式碼、變數和暫存器值，並視需要進行變更、繼續執行或終止執行。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="eeb5e-109">[**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)函式會終止目前的進程，並提供偵錯工具的執行控制權，但與 [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)不同的是，它不會產生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="eeb5e-110">這個函式只能用來做為最後的手段，因為它不一定會釋放進程的記憶體或關閉其檔案。</span><span class="sxs-lookup"><span data-stu-id="eeb5e-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 

---
description: CreateProcess 函式可讓偵錯工具啟動處理常式並進行調試。
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: 用於偵錯工具的進程函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936208"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="bba9a-103">用於偵錯工具的進程函式</span><span class="sxs-lookup"><span data-stu-id="bba9a-103">Process Functions for Debugging</span></span>

<span data-ttu-id="bba9a-104">[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式可讓偵錯工具啟動處理常式並進行調試。</span><span class="sxs-lookup"><span data-stu-id="bba9a-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="bba9a-105">**CreateProcess** 的 *fdwCreate* 參數是用來指定偵錯工具的類型。</span><span class="sxs-lookup"><span data-stu-id="bba9a-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="bba9a-106">如果為 \_ 參數指定了 DEBUG PROCESS 旗標，則偵錯工具會將新的進程以及所有進程的下階，都在不使用 DEBUG PROCESS 旗標的情況下建立 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bba9a-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="bba9a-107">如果 \_ \_ 只 \_ 針對 fdwCreate 指定 DEBUG 程式和 debug debug 這個 \_ 進程旗標，偵錯工具就會將新的進程（而非其子系）進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="bba9a-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="bba9a-108">有一個偵錯工具可以使用 DEBUG 流程旗標建立進程，以進行另一個偵錯工具的偵錯工具 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bba9a-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="bba9a-109"> (偵錯工具的新進程) 必須使用 DEBUG process 旗標建立處理常式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bba9a-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="bba9a-110">[**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)函式可讓偵錯工具取得現有進程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bba9a-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="bba9a-111"> ([**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) 函式會使用這個識別碼，將偵錯工具附加至進程。通常 ) ，偵錯工具會使用進程 \_ VM \_ 讀取和處理 \_ vm \_ 寫入旗標來開啟進程。</span><span class="sxs-lookup"><span data-stu-id="bba9a-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="bba9a-112">使用這些旗標，可讓偵錯工具使用 [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) 和 [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) 函式來讀取和寫入進程的虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="bba9a-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="bba9a-113">如需詳細資訊，請參閱 [**進程和執行緒**](../procthread/processes-and-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="bba9a-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 

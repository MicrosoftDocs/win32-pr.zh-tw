---
description: 瞭解如何使用 CreateThread 函式來建立進程的新執行緒。 偵錯工具通常需要檢查或變更執行緒的暫存器內容。
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: 用於偵錯工具的執行緒函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403981"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="2c980-104">用於偵錯工具的執行緒函數</span><span class="sxs-lookup"><span data-stu-id="2c980-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="2c980-105">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式會為進程建立新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="2c980-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="2c980-106">偵錯工具通常需要檢查或變更執行緒的暫存器內容。</span><span class="sxs-lookup"><span data-stu-id="2c980-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="2c980-107">若要達成此目的，偵錯工具必須使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式來取得執行緒的控制碼，並指定適當的執行緒存取 (執行緒 \_ 取得 \_ 內容、執行緒 \_ 集 \_ 內容，或這兩個) 。</span><span class="sxs-lookup"><span data-stu-id="2c980-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="2c980-108">[**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)函式可讓偵錯工具取得現有線程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c980-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="2c980-109">具有適當執行緒存取權的進程可以使用 [**GetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) 函式來檢查執行緒的暫存器，並使用 [**SetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) 函式來設定執行緒的暫存器內容。</span><span class="sxs-lookup"><span data-stu-id="2c980-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="2c980-110">進程也可以取得執行緒 \_ 的執行緒暫停 \_ 繼續存取。</span><span class="sxs-lookup"><span data-stu-id="2c980-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="2c980-111">這種類型的存取可讓偵錯工具使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 和 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函數來控制執行緒的執行。</span><span class="sxs-lookup"><span data-stu-id="2c980-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="2c980-112">如需執行緒的詳細資訊，請參閱 [進程和執行緒](../procthread/processes-and-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="2c980-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 

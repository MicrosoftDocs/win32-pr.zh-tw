---
description: '\_ \_ Try 和 \_ \_ finally 關鍵字是用來建立終止處理常式。 下列範例顯示終止處理常式的結構。'
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967048"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="fe950-104">Termination-Handler 語法</span><span class="sxs-lookup"><span data-stu-id="fe950-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="fe950-105">**\_ \_ Try** 和 **\_ \_ finally** 關鍵字是用來建立終止處理常式。</span><span class="sxs-lookup"><span data-stu-id="fe950-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="fe950-106">下列範例顯示終止處理常式的結構。</span><span class="sxs-lookup"><span data-stu-id="fe950-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="fe950-107">如需範例，請參閱 [使用終止處理常式](using-a-termination-handler.md)。</span><span class="sxs-lookup"><span data-stu-id="fe950-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="fe950-108">如同例外狀況處理常式一樣， **\_ \_ try** 區塊和 **\_ \_ finally** 區塊都需要大括弧 ({}) ，而且不允許使用 **goto** 語句跳到任一個區塊。</span><span class="sxs-lookup"><span data-stu-id="fe950-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="fe950-109">**\_ \_ Try** 區塊包含受終止處理常式保護的程式碼受防護主體。</span><span class="sxs-lookup"><span data-stu-id="fe950-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="fe950-110">函數可以有任意數目的終止處理常式，而這些終止處理區塊可以嵌套在相同函式或不同函式中。</span><span class="sxs-lookup"><span data-stu-id="fe950-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="fe950-111">當控制權的流程離開 **\_ \_ try** 區塊時，就會執行 **\_ \_ finally** 區塊。</span><span class="sxs-lookup"><span data-stu-id="fe950-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="fe950-112">但是，如果您在 **\_ \_ try** 區塊內呼叫下列任何函式，則不會執行 **\_ \_ finally** 區塊： [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)、 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)或 **abort**。</span><span class="sxs-lookup"><span data-stu-id="fe950-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="fe950-113">**\_ \_ Finally** 區塊會在終止處理常式所在的函數內容中執行。</span><span class="sxs-lookup"><span data-stu-id="fe950-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="fe950-114">這表示 **\_ \_ finally** 區塊可以存取該函數的區域變數。</span><span class="sxs-lookup"><span data-stu-id="fe950-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="fe950-115">**\_ \_ Finally** 區塊的執行可透過下列任何方式來終止。</span><span class="sxs-lookup"><span data-stu-id="fe950-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="fe950-116">執行區塊中的最後一個語句，並接續至下一個指令</span><span class="sxs-lookup"><span data-stu-id="fe950-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="fe950-117">使用 control 語句 (**return**、 **break**、 **continue** 或 **goto**) </span><span class="sxs-lookup"><span data-stu-id="fe950-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="fe950-118">使用 **longjmp** 或跳到例外狀況處理常式</span><span class="sxs-lookup"><span data-stu-id="fe950-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="fe950-119">如果因為叫用以框架為基礎之例外狀況處理常式之例外狀況處理區塊的例外狀況而終止 **\_ \_ try** 區塊的執行，則會在執行例外狀況處理區塊之前執行 **\_ \_ finally** 區塊。</span><span class="sxs-lookup"><span data-stu-id="fe950-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="fe950-120">同樣地，從 **\_ \_ try** 區塊呼叫 **longjmp** C 執行時間程式庫函式會造成 **\_ \_ finally** 區塊執行，然後繼續執行 **longjmp** 作業的目標。</span><span class="sxs-lookup"><span data-stu-id="fe950-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="fe950-121">如果 **\_ \_ try** 區塊執行由於 control 語句 (**return**、 **break**、 **continue** 或 **goto**) 而終止，則會執行 **\_ \_ finally** 區塊。</span><span class="sxs-lookup"><span data-stu-id="fe950-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="fe950-122">[**AbnormalTermination**](abnormaltermination.md)函式可以在 **\_ \_ finally** 區塊中使用，以判斷 **\_ \_ try** 區塊是否順序終止，也就是是否到達右大括弧 (} ) 。</span><span class="sxs-lookup"><span data-stu-id="fe950-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="fe950-123">由於呼叫 **longjmp**、跳到例外狀況處理常式，或 **傳回、\*\*\*\*中斷**、**繼續** 或 **goto** 語句，因此離開 **\_ \_ try** 區塊會被視為異常終止。</span><span class="sxs-lookup"><span data-stu-id="fe950-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="fe950-124">請注意，順序結束失敗會導致系統以反向順序搜尋所有堆疊框架，以判斷是否必須呼叫任何終止處理常式。</span><span class="sxs-lookup"><span data-stu-id="fe950-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="fe950-125">這可能會導致效能降低，因為執行數百個指令。</span><span class="sxs-lookup"><span data-stu-id="fe950-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="fe950-126">為了避免終止處理常式異常終止，執行應該會繼續到區塊結尾。</span><span class="sxs-lookup"><span data-stu-id="fe950-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="fe950-127">您也可以執行 **\_ \_ leave** 語句。</span><span class="sxs-lookup"><span data-stu-id="fe950-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="fe950-128">**\_ \_ Leave** 語句允許立即終止 **\_ \_ try** 區塊，而不會造成異常終止和其效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="fe950-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="fe950-129">請檢查您的編譯器檔，以判斷是否支援 **\_ \_ leave** 語句。</span><span class="sxs-lookup"><span data-stu-id="fe950-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="fe950-130">如果 **\_ \_ finally** 區塊的執行因為 **return** control 語句而終止，它相當於封閉函數中右大括弧的 **goto** 。</span><span class="sxs-lookup"><span data-stu-id="fe950-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="fe950-131">因此，封入函數將會傳回。</span><span class="sxs-lookup"><span data-stu-id="fe950-131">Therefore, the enclosing function will return.</span></span>

 

 

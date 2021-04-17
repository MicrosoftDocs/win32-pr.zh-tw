---
description: '\_ \_ Try 和 \_ \_ except 關鍵字是用來建立以框架為基礎的例外狀況處理常式。 下列範例會顯示例外狀況處理常式的結構。'
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Exception-Handler 語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510380"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="e82e0-104">Exception-Handler 語法</span><span class="sxs-lookup"><span data-stu-id="e82e0-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="e82e0-105">**\_ \_ Try** 和 **\_ \_ except** 關鍵字是用來建立以框架為基礎的例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="e82e0-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="e82e0-106">下列範例會顯示例外狀況處理常式的結構。</span><span class="sxs-lookup"><span data-stu-id="e82e0-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="e82e0-107">請注意， **\_ \_ try** 區塊和例外狀況處理常式區塊需要大括弧 ({}) 。</span><span class="sxs-lookup"><span data-stu-id="e82e0-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="e82e0-108">不允許使用 **goto** 語句跳到 **\_ \_ try** 區塊的主體或進入例外狀況處理常式區塊。</span><span class="sxs-lookup"><span data-stu-id="e82e0-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="e82e0-109">這項規則適用于例外狀況處理常式和終止處理常式。</span><span class="sxs-lookup"><span data-stu-id="e82e0-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="e82e0-110">**\_ \_ Try** 區塊包含例外狀況處理常式保護的程式碼受防護主體。</span><span class="sxs-lookup"><span data-stu-id="e82e0-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="e82e0-111">函式可以有任意數目的例外狀況處理常式，而且這些例外狀況處理語句可以嵌套在相同函式或不同函式中。</span><span class="sxs-lookup"><span data-stu-id="e82e0-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="e82e0-112">如果 **\_ \_ try** 區塊中發生例外狀況，系統會接受控制權，並開始搜尋例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="e82e0-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="e82e0-113">如需此搜尋的詳細說明，請參閱 [例外狀況處理](exception-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="e82e0-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="e82e0-114">例外狀況處理常式只接收在單一執行緒內發生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e82e0-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="e82e0-115">這表示，如果 **\_ \_ try** 區塊包含 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)或 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式的呼叫，則在新的進程或執行緒內發生的例外狀況不會分派至此處理程式。</span><span class="sxs-lookup"><span data-stu-id="e82e0-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="e82e0-116">系統會評估每個例外狀況處理常式的篩選運算式，以防止發生例外狀況的程式碼，直到處理例外狀況或不再有處理常式為止。</span><span class="sxs-lookup"><span data-stu-id="e82e0-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="e82e0-117">篩選運算式必須評估為下列三個值的其中一個。</span><span class="sxs-lookup"><span data-stu-id="e82e0-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="e82e0-118">值</span><span class="sxs-lookup"><span data-stu-id="e82e0-118">Value</span></span>                              | <span data-ttu-id="e82e0-119">意義</span><span class="sxs-lookup"><span data-stu-id="e82e0-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e82e0-120">**例外狀況 \_ 執行 \_ 處理常式**</span><span class="sxs-lookup"><span data-stu-id="e82e0-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="e82e0-121">系統會將控制項傳送至例外狀況處理常式，然後在找到處理程式的堆疊框架中繼續執行。</span><span class="sxs-lookup"><span data-stu-id="e82e0-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="e82e0-122">**例外狀況 \_ 繼續 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="e82e0-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="e82e0-123">系統會繼續搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="e82e0-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="e82e0-124">**例外狀況 \_ 繼續 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="e82e0-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="e82e0-125">系統會停止其搜尋處理常式，並將控制權傳回給發生例外狀況的時間點。</span><span class="sxs-lookup"><span data-stu-id="e82e0-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="e82e0-126">如果例外狀況是 noncontinuable，這會導致 **例外狀況 \_ noncontinuable \_ 例外** 狀況例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e82e0-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="e82e0-127">篩選運算式會在例外狀況處理常式所在的函式內容中進行評估，即使例外狀況可能發生在不同的函式中也一樣。</span><span class="sxs-lookup"><span data-stu-id="e82e0-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="e82e0-128">這表示篩選運算式可以存取函式的本機變數。</span><span class="sxs-lookup"><span data-stu-id="e82e0-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="e82e0-129">同樣地，例外狀況處理常式區塊可以存取它所在之函式的本機變數。</span><span class="sxs-lookup"><span data-stu-id="e82e0-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="e82e0-130">如需更多範例，請參閱 [使用例外狀況處理常式](using-an-exception-handler.md)。</span><span class="sxs-lookup"><span data-stu-id="e82e0-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="e82e0-131">如需篩選運算式和篩選函數的詳細資訊，請參閱以 [框架為基礎的例外狀況處理](frame-based-exception-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="e82e0-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 

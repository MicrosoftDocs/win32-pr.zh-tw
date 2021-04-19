---
description: 下列範例示範如何使用例外狀況處理常式。
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: 使用例外狀況處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971134"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="c71de-103">使用例外狀況處理常式</span><span class="sxs-lookup"><span data-stu-id="c71de-103">Using an Exception Handler</span></span>

<span data-ttu-id="c71de-104">下列範例示範如何使用例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="c71de-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="c71de-105">範例 1</span><span class="sxs-lookup"><span data-stu-id="c71de-105">Example 1</span></span>

<span data-ttu-id="c71de-106">下列程式碼片段會使用結構化例外狀況處理來檢查 2 32 位整數的除法運算是否會導致零除的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c71de-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="c71de-107">如果發生這種情況，函數會傳回 **FALSE**，否則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c71de-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="c71de-108">範例 2</span><span class="sxs-lookup"><span data-stu-id="c71de-108">Example 2</span></span>

<span data-ttu-id="c71de-109">下列範例函數會呼叫 [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) 函數，並使用結構化例外狀況處理來檢查中斷點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c71de-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="c71de-110">如果發生這種情況，函數會傳回 **FALSE**，否則會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c71de-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="c71de-111">範例中的篩選運算式在執行處理常式之前，會使用 [**GetExceptionCode**](getexceptioncode.md) 函數來檢查例外狀況類型。</span><span class="sxs-lookup"><span data-stu-id="c71de-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="c71de-112">這可讓系統在某些其他類型的例外狀況發生時，繼續搜尋適當的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c71de-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="c71de-113">此外，在例外狀況處理常式的 **\_ \_ try** 區塊中使用 **return** 語句，與終止處理常式的 **\_ \_ try** 區塊中使用 **return** 不同，這會導致 **\_ \_ try** 區塊的異常終止。</span><span class="sxs-lookup"><span data-stu-id="c71de-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="c71de-114">這是在例外狀況處理常式中有效使用 return 語句。</span><span class="sxs-lookup"><span data-stu-id="c71de-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="c71de-115">只有在 \_ \_ 預期例外狀況類型且已知錯誤位址時，才會從例外狀況篩選準則傳回例外狀況執行處理常式。</span><span class="sxs-lookup"><span data-stu-id="c71de-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="c71de-116">您應允許預設的例外狀況處理常式處理未預期的例外狀況類型和錯誤位址。</span><span class="sxs-lookup"><span data-stu-id="c71de-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="c71de-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="c71de-117">Example 3</span></span>

<span data-ttu-id="c71de-118">下列範例顯示的是嵌套處理常式的互動。</span><span class="sxs-lookup"><span data-stu-id="c71de-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="c71de-119">[**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)函式會在例外狀況處理常式的受防護主體內，于終止處理常式的受防護主體內引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c71de-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="c71de-120">例外狀況會導致系統評估 FilterFunction 函式，而其傳回值接著會導致叫用例外狀況處理常式。</span><span class="sxs-lookup"><span data-stu-id="c71de-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="c71de-121">不過，在執行例外狀況處理常式區塊之前，會執行終止處理常式的 **\_ \_ finally** 區塊，因為控制權的流程已離開終止處理常式的 **\_ \_ try** 區塊。</span><span class="sxs-lookup"><span data-stu-id="c71de-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 

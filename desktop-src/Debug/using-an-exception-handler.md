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
# <a name="using-an-exception-handler"></a>使用例外狀況處理常式

下列範例示範如何使用例外狀況處理常式。

## <a name="example-1"></a>範例 1

下列程式碼片段會使用結構化例外狀況處理來檢查 2 32 位整數的除法運算是否會導致零除的錯誤。 如果發生這種情況，函數會傳回 **FALSE**，否則會傳回 **TRUE**。


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



## <a name="example-2"></a>範例 2

下列範例函數會呼叫 [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) 函數，並使用結構化例外狀況處理來檢查中斷點例外狀況。 如果發生這種情況，函數會傳回 **FALSE**，否則會傳回 **TRUE**。

範例中的篩選運算式在執行處理常式之前，會使用 [**GetExceptionCode**](getexceptioncode.md) 函數來檢查例外狀況類型。 這可讓系統在某些其他類型的例外狀況發生時，繼續搜尋適當的處理常式。

此外，在例外狀況處理常式的 **\_ \_ try** 區塊中使用 **return** 語句，與終止處理常式的 **\_ \_ try** 區塊中使用 **return** 不同，這會導致 **\_ \_ try** 區塊的異常終止。 這是在例外狀況處理常式中有效使用 return 語句。


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



只有在 \_ \_ 預期例外狀況類型且已知錯誤位址時，才會從例外狀況篩選準則傳回例外狀況執行處理常式。 您應允許預設的例外狀況處理常式處理未預期的例外狀況類型和錯誤位址。

## <a name="example-3"></a>範例 3

下列範例顯示的是嵌套處理常式的互動。 [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)函式會在例外狀況處理常式的受防護主體內，于終止處理常式的受防護主體內引發例外狀況。 例外狀況會導致系統評估 FilterFunction 函式，而其傳回值接著會導致叫用例外狀況處理常式。 不過，在執行例外狀況處理常式區塊之前，會執行終止處理常式的 **\_ \_ finally** 區塊，因為控制權的流程已離開終止處理常式的 **\_ \_ try** 區塊。


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



 

 

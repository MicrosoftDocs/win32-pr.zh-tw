---
title: 使用系結控制碼並進行 RPC 呼叫
description: RPC 程式設計師間常見的錯誤是處理所有例外狀況。
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682745"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="747f1-103">使用系結控制碼並進行 RPC 呼叫</span><span class="sxs-lookup"><span data-stu-id="747f1-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="747f1-104">RPC 程式設計師間常見的錯誤是處理所有例外狀況。</span><span class="sxs-lookup"><span data-stu-id="747f1-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="747f1-105">許多程式設計人員會將它們的例外狀況處理常式結構如下：</span><span class="sxs-lookup"><span data-stu-id="747f1-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="747f1-106">此處理程式的問題在於它會捕捉所有錯誤，包括用戶端程式中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="747f1-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="747f1-107">攔截用戶端程式中的錯誤會讓偵錯工具更困難。</span><span class="sxs-lookup"><span data-stu-id="747f1-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="747f1-108">適當的結構處理例外狀況處理常式如下：</span><span class="sxs-lookup"><span data-stu-id="747f1-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="747f1-109">這個例外狀況處理常式的優點是讓特定範圍的錯誤通過。</span><span class="sxs-lookup"><span data-stu-id="747f1-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="747f1-110">伺服器永遠不會傳回這些錯誤，因為它們表示用戶端的問題。</span><span class="sxs-lookup"><span data-stu-id="747f1-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="747f1-111">此外，建議使用 **\[** [strict \_ 內容 \_ 控制碼](/windows/desktop/Midl/strict-context-handle) **\]** 和 **\[** [類型 \_ 嚴格的 \_ 內容 \_ 控制碼](/windows/desktop/Midl/type-strict-context-handle) **\]** 屬性，以確保 RPC 執行時間會在一個介面上建立內容控制碼，該介面只能做為引數傳遞給該介面的方法。</span><span class="sxs-lookup"><span data-stu-id="747f1-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="747f1-112">這麼做可防止在相同進程記憶體在的不同介面之間開啟和傳遞內容控制碼時，發生伺服器失敗。</span><span class="sxs-lookup"><span data-stu-id="747f1-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="747f1-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="747f1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="747f1-114">strict \_ 內容 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="747f1-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="747f1-115">輸入 \_ strict \_ 內容 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="747f1-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 
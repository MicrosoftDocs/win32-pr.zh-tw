---
title: 使用系結控制碼並進行 RPC 呼叫
description: RPC 程式設計師間常見的錯誤是處理所有例外狀況。
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1350e29344d09f42417a30fa3d32729d7ddd02247b17f80bccd0ae537c6c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010806"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>使用系結控制碼並進行 RPC 呼叫

RPC 程式設計師間常見的錯誤是處理所有例外狀況。 許多程式設計人員會將它們的例外狀況處理常式結構如下：

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

此處理程式的問題在於它會捕捉所有錯誤，包括用戶端程式中的錯誤。 攔截用戶端程式中的錯誤會讓偵錯工具更困難。 適當的結構處理例外狀況處理常式如下：

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

這個例外狀況處理常式的優點是讓特定範圍的錯誤通過。 伺服器永遠不會傳回這些錯誤，因為它們表示用戶端的問題。

此外，建議使用 **\[** [strict \_ 內容 \_ 控制碼](/windows/desktop/Midl/strict-context-handle) **\]** 和 **\[** [類型 \_ 嚴格的 \_ 內容 \_ 控制碼](/windows/desktop/Midl/type-strict-context-handle) **\]** 屬性，以確保 RPC 執行時間會在一個介面上建立內容控制碼，該介面只能做為引數傳遞給該介面的方法。 這麼做可防止在相同進程記憶體在的不同介面之間開啟和傳遞內容控制碼時，發生伺服器失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[strict \_ 內容 \_ 控制碼](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[輸入 \_ strict \_ 內容 \_ 控制碼](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 
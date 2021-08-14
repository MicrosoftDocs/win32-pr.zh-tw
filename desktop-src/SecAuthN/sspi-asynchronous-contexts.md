---
title: 非同步內容
description: 非同步內容和非同步 SSPI 標頭的總覽。
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e83dbab8c20dd9f9cfe13ec579db304aabd491cba92ab0cd6a9c8afcf4e4af8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917227"
---
# <a name="asynchronous-contexts"></a>非同步內容

非同步 SSPI 安全性內容可讓呼叫端在未封鎖的情況下繼續進行，並在呼叫完成時收到通知。 目前只有核心模式 TLS 用戶端和伺服器支援非同步內容。 下列非同步 SSPI 函數會在非同步安全性內容上運作：

## <a name="async-context-management-types"></a>非同步內容管理類型

| 物件名稱 | Description |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | 用來通知完成非同步 SSPI 呼叫的回呼。 |


## <a name="async-context-management-functions"></a>非同步內容管理函數

| API 名稱 | Description |
|-------------|--------------|
| [SspiCreateAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | 建立用來追蹤非同步呼叫的 SspiAsyncCoNtext 實例。 |
| [SspiReinitAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | 標記非同步內容以供重複使用。 |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | 註冊在非同步呼叫完成時收到通知的回呼。 |
| [SspiAsyncCoNtextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | 判斷指定的非同步內容是否需要在呼叫完成時收到通知。 |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | 取得與所提供內容相關聯之非同步呼叫的目前狀態。  |
| [SspiFreeAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | 釋放在呼叫 SspiCreateAsyncCoNtext 函式時所建立的內容。 |

## <a name="async-sspi-functions"></a>非同步 SSPI 函數

除了與同步對應的所有參數相同的參數之外，下列函數還接受非同步內容。

| API 名稱 | Description |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | 以非同步方式取得安全性主體預先存在的認證控制碼。 |
| [SspiAcceptSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | 讓傳輸應用程式的伺服器元件以非同步方式在伺服器與遠端用戶端之間建立安全性內容。 |
| [SspiInitializeSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | 初始化非同步安全性內容。 |
| [SspiDeleteSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | 刪除與先前呼叫 SspiInitializeSecurityCoNtextAsync 函數或 SspiAcceptSecurityCoNtextAsync 函數所起始的指定安全性內容相關聯的本機資料結構。 |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | 釋出認證控制碼。 |

## <a name="api-sample"></a>API 範例

一般呼叫流程的運作方式如下：
1) 使用[SspiCreateAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)建立 SspiAsyncCoNtext 內容來追蹤呼叫
2) 註冊內容的[SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback)
3) 使用[SspiAcceptSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)進行非同步呼叫
4) 在回呼上，使用[SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)取得結果
5) 使用 [SspiDeleteSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync)刪除 SspiAsyncCoNtext。 如果使用 [SspiReinitAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)重複使用內容，請返回步驟2。

下列範例示範 SspiAcceptSecurityCoNtextAsync 的調用。 此範例會等待來電完成，並取得結果。

在完整的 SSPI 交握中，SspiAcceptSecurityCoNtextAsync 和 SspiInitializeSecurityCoNtextAsync 會被呼叫多次，直到傳回 SEC_E_OK 為止。 為了方便使用，我們提供了 SspiReinitAsyncCoNtext，讓您在這種情況下可加速效能。

判斷提示是用來反白顯示在成功情況下的預期。

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a>另請參閱

[sspi. h 標頭](/windows/win32/api/sspi/)

[SSPI 函數](/windows/win32/api/sspi/#functions)

[SSPI 結構](/windows/win32/api/sspi/#structures)



---
title: 非同步 SSPI
description: 非同步 SSPI 標頭的總覽。
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990378"
---
# <a name="asynchronous-sspi"></a><span data-ttu-id="ffddf-103">非同步 SSPI</span><span class="sxs-lookup"><span data-stu-id="ffddf-103">Asynchronous SSPI</span></span>

<span data-ttu-id="ffddf-104">非同步 SSPI 標頭包含支援非同步內容物件的函式，可讓呼叫端透過非同步 SSPI 呼叫生命週期，在伺服器與遠端用戶端之間建立安全性內容。</span><span class="sxs-lookup"><span data-stu-id="ffddf-104">The asynchronous SSPI header includes functions that support async context objects, allowing callers to establish security contexts between server and remote clients concurrently through an async SSPI call lifecycle.</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="ffddf-105">非同步內容管理類型</span><span class="sxs-lookup"><span data-stu-id="ffddf-105">Async context management types</span></span>

| <span data-ttu-id="ffddf-106">物件名稱</span><span class="sxs-lookup"><span data-stu-id="ffddf-106">Object Name</span></span> | <span data-ttu-id="ffddf-107">Description</span><span class="sxs-lookup"><span data-stu-id="ffddf-107">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="ffddf-108">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="ffddf-108">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="ffddf-109">用來通知完成非同步 SSPI 呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="ffddf-109">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="ffddf-110">非同步內容管理函數</span><span class="sxs-lookup"><span data-stu-id="ffddf-110">Async context management functions</span></span>

| <span data-ttu-id="ffddf-111">API 名稱</span><span class="sxs-lookup"><span data-stu-id="ffddf-111">API Name</span></span> | <span data-ttu-id="ffddf-112">Description</span><span class="sxs-lookup"><span data-stu-id="ffddf-112">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="ffddf-113">SspiCreateAsyncCoNtext</span><span class="sxs-lookup"><span data-stu-id="ffddf-113">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="ffddf-114">建立用來追蹤非同步呼叫的 SspiAsyncCoNtext 實例。</span><span class="sxs-lookup"><span data-stu-id="ffddf-114">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="ffddf-115">SspiReinitAsyncCoNtext</span><span class="sxs-lookup"><span data-stu-id="ffddf-115">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="ffddf-116">標記非同步內容以供重複使用。</span><span class="sxs-lookup"><span data-stu-id="ffddf-116">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="ffddf-117">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="ffddf-117">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="ffddf-118">註冊在非同步呼叫完成時收到通知的回呼。</span><span class="sxs-lookup"><span data-stu-id="ffddf-118">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="ffddf-119">SspiAsyncCoNtextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="ffddf-119">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="ffddf-120">判斷指定的非同步內容是否需要在呼叫完成時收到通知。</span><span class="sxs-lookup"><span data-stu-id="ffddf-120">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="ffddf-121">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="ffddf-121">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="ffddf-122">取得與所提供內容相關聯之非同步呼叫的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ffddf-122">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="ffddf-123">SspiFreeAsyncCoNtext</span><span class="sxs-lookup"><span data-stu-id="ffddf-123">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="ffddf-124">釋放在呼叫 SspiCreateAsyncCoNtext 函式時所建立的內容。</span><span class="sxs-lookup"><span data-stu-id="ffddf-124">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="ffddf-125">非同步 SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="ffddf-125">Async SSPI functions</span></span>

<span data-ttu-id="ffddf-126">除了與同步對應的所有參數相同的參數之外，下列函數還接受非同步內容。</span><span class="sxs-lookup"><span data-stu-id="ffddf-126">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="ffddf-127">API 名稱</span><span class="sxs-lookup"><span data-stu-id="ffddf-127">API Name</span></span> | <span data-ttu-id="ffddf-128">Description</span><span class="sxs-lookup"><span data-stu-id="ffddf-128">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="ffddf-129">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="ffddf-129">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="ffddf-130">以非同步方式取得安全性主體預先存在的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffddf-130">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="ffddf-131">SspiAcceptSecurityCoNtextAsync</span><span class="sxs-lookup"><span data-stu-id="ffddf-131">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="ffddf-132">讓傳輸應用程式的伺服器元件以非同步方式在伺服器與遠端用戶端之間建立安全性內容。</span><span class="sxs-lookup"><span data-stu-id="ffddf-132">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="ffddf-133">SspiInitializeSecurityCoNtextAsync</span><span class="sxs-lookup"><span data-stu-id="ffddf-133">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="ffddf-134">初始化非同步安全性內容。</span><span class="sxs-lookup"><span data-stu-id="ffddf-134">Initializes an async security context.</span></span> |
| [<span data-ttu-id="ffddf-135">SspiDeleteSecurityCoNtextAsync</span><span class="sxs-lookup"><span data-stu-id="ffddf-135">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="ffddf-136">刪除與先前呼叫 SspiInitializeSecurityCoNtextAsync 函數或 SspiAcceptSecurityCoNtextAsync 函數所起始的指定安全性內容相關聯的本機資料結構。</span><span class="sxs-lookup"><span data-stu-id="ffddf-136">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="ffddf-137">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="ffddf-137">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="ffddf-138">釋出認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffddf-138">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="ffddf-139">API 範例</span><span class="sxs-lookup"><span data-stu-id="ffddf-139">API Sample</span></span>

<span data-ttu-id="ffddf-140">一般呼叫流程的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="ffddf-140">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="ffddf-141">使用[SspiCreateAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)建立 SspiAsyncCoNtext 內容來追蹤呼叫</span><span class="sxs-lookup"><span data-stu-id="ffddf-141">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="ffddf-142">註冊內容的[SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback)</span><span class="sxs-lookup"><span data-stu-id="ffddf-142">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="ffddf-143">使用[SspiAcceptSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="ffddf-143">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="ffddf-144">在回呼上，使用[SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)取得結果</span><span class="sxs-lookup"><span data-stu-id="ffddf-144">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="ffddf-145">使用 [SspiDeleteSecurityCoNtextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync)刪除 SspiAsyncCoNtext。</span><span class="sxs-lookup"><span data-stu-id="ffddf-145">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="ffddf-146">如果使用 [SspiReinitAsyncCoNtext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)重複使用內容，請返回步驟2。</span><span class="sxs-lookup"><span data-stu-id="ffddf-146">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="ffddf-147">下列範例示範 SspiAcceptSecurityCoNtextAsync 的調用。</span><span class="sxs-lookup"><span data-stu-id="ffddf-147">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="ffddf-148">此範例會等待來電完成，並取得結果。</span><span class="sxs-lookup"><span data-stu-id="ffddf-148">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="ffddf-149">在完整的 SSPI 交握中，SspiAcceptSecurityCoNtextAsync 和 SspiInitializeSecurityCoNtextAsync 會被呼叫多次，直到傳回 SEC_E_OK 為止。</span><span class="sxs-lookup"><span data-stu-id="ffddf-149">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="ffddf-150">為了方便使用，我們提供了 SspiReinitAsyncCoNtext，讓您在這種情況下可加速效能。</span><span class="sxs-lookup"><span data-stu-id="ffddf-150">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="ffddf-151">判斷提示是用來反白顯示在成功情況下的預期。</span><span class="sxs-lookup"><span data-stu-id="ffddf-151">Asserts are used to highlight what we would expect in the case of success.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="ffddf-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffddf-152">See Also</span></span>

[<span data-ttu-id="ffddf-153">sspi. h 標頭</span><span class="sxs-lookup"><span data-stu-id="ffddf-153">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="ffddf-154">SSPI 函數</span><span class="sxs-lookup"><span data-stu-id="ffddf-154">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="ffddf-155">SSPI 結構</span><span class="sxs-lookup"><span data-stu-id="ffddf-155">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)



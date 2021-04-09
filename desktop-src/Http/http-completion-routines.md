---
title: HTTP 完成常式
description: 應用程式有數個選項可接收完成指示，並為開發人員提供一些彈性。
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee05efc8284cb29130efae4bcaefb4834a3fb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933223"
---
# <a name="http-completion-routines"></a><span data-ttu-id="340fb-103">HTTP 完成常式</span><span class="sxs-lookup"><span data-stu-id="340fb-103">HTTP Completion Routines</span></span>

<span data-ttu-id="340fb-104">應用程式有數個選項可接收完成指示，並為開發人員提供一些彈性。</span><span class="sxs-lookup"><span data-stu-id="340fb-104">Applications have several options for receiving completion indications and providing some flexibility for developers.</span></span> <span data-ttu-id="340fb-105">這些選項會在等候 API 呼叫完成時封鎖，或使用完成常式進行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="340fb-105">The options are to block while waiting for an API call to complete or to use completion routines for asynchronous operations.</span></span> <span data-ttu-id="340fb-106">使用非同步作業的優點是可增加應用程式的回應能力。</span><span class="sxs-lookup"><span data-stu-id="340fb-106">The advantage of using asynchronous operations is an increase in responsiveness of the application.</span></span>

## <a name="blocked-io"></a><span data-ttu-id="340fb-107">封鎖的 i/o</span><span class="sxs-lookup"><span data-stu-id="340fb-107">Blocked I/O</span></span>

<span data-ttu-id="340fb-108">應用程式可以在等候 API 呼叫完成時封鎖，方法是將重 [**迭結構設定**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="340fb-108">Applications can block while waiting for the API call to complete by setting the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to **NULL**.</span></span> <span data-ttu-id="340fb-109">這真的會封鎖執行緒上的所有作業。</span><span class="sxs-lookup"><span data-stu-id="340fb-109">This truly blocks all operations on the thread.</span></span> <span data-ttu-id="340fb-110">例如，在呼叫 [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)時，呼叫會封鎖，直到連接中斷為止。</span><span class="sxs-lookup"><span data-stu-id="340fb-110">For example, in calls to [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), the call blocks until the connection is broken.</span></span>

## <a name="asynchronous-io"></a><span data-ttu-id="340fb-111">非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="340fb-111">Asynchronous I/O</span></span>

<span data-ttu-id="340fb-112">偏好不封鎖的應用程式可以使用重迭 [**的結構來**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 取得完成結果。</span><span class="sxs-lookup"><span data-stu-id="340fb-112">Applications that prefer not to block can use the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to obtain the completion results.</span></span> <span data-ttu-id="340fb-113">應用程式會提供重 **迭結構的** 指標，該指標會與事件物件或完成埠一起使用。</span><span class="sxs-lookup"><span data-stu-id="340fb-113">The application supplies a pointer to an **OVERLAPPED** structure, which is used with an event object or a completion port.</span></span> <span data-ttu-id="340fb-114">使用 i/o 完成埠時，會使用 HTTP 控制碼做為檔案控制代碼，在非同步檔案 i/o 作業中。</span><span class="sxs-lookup"><span data-stu-id="340fb-114">With an I/O completion port, an HTTP handle is used as a file handle would be in an asynchronous file I/O operation.</span></span> <span data-ttu-id="340fb-115">下表摘要說明應用程式可用的完成選項。</span><span class="sxs-lookup"><span data-stu-id="340fb-115">The following table summarizes the completion options available to the applications.</span></span>



| <span data-ttu-id="340fb-116">重迭結構</span><span class="sxs-lookup"><span data-stu-id="340fb-116">Overlapped structure</span></span> | <span data-ttu-id="340fb-117">事件物件</span><span class="sxs-lookup"><span data-stu-id="340fb-117">Event object</span></span>   | <span data-ttu-id="340fb-118">完成埠</span><span class="sxs-lookup"><span data-stu-id="340fb-118">Completion port</span></span> | <span data-ttu-id="340fb-119">Completion</span><span class="sxs-lookup"><span data-stu-id="340fb-119">Completion</span></span>                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340fb-120">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-120">**NULL**</span></span>             | <span data-ttu-id="340fb-121">不適用</span><span class="sxs-lookup"><span data-stu-id="340fb-121">Not Applicable</span></span> | <span data-ttu-id="340fb-122">忽略</span><span class="sxs-lookup"><span data-stu-id="340fb-122">Ignored</span></span>         | <span data-ttu-id="340fb-123">作業以同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="340fb-123">Operation completes synchronously.</span></span>                                                                           |
| <span data-ttu-id="340fb-124">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-124">Non-**NULL**</span></span>         | <span data-ttu-id="340fb-125">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-125">Non-**NULL**</span></span>   | <span data-ttu-id="340fb-126">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-126">**NULL**</span></span>        | <span data-ttu-id="340fb-127">作業會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="340fb-127">Operation completes asynchronously.</span></span> <span data-ttu-id="340fb-128">重迭通知是藉由向事件物件發出信號來執行。</span><span class="sxs-lookup"><span data-stu-id="340fb-128">Overlapped notification is performed by signaling an event object.</span></span>       |
| <span data-ttu-id="340fb-129">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-129">Non-**NULL**</span></span>         | <span data-ttu-id="340fb-130">忽略</span><span class="sxs-lookup"><span data-stu-id="340fb-130">Ignored</span></span>        | <span data-ttu-id="340fb-131">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-131">Non-**NULL**</span></span>    | <span data-ttu-id="340fb-132">作業會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="340fb-132">Operation completes asynchronously.</span></span> <span data-ttu-id="340fb-133">重迭通知是藉由排程完成常式來執行。</span><span class="sxs-lookup"><span data-stu-id="340fb-133">Overlapped notification is performed by scheduling a completion routine.</span></span> |



 

## <a name="returning-the-number-of-bytes-read"></a><span data-ttu-id="340fb-134">傳回讀取的位元組數目</span><span class="sxs-lookup"><span data-stu-id="340fb-134">Returning the Number of Bytes Read</span></span>

<span data-ttu-id="340fb-135">某些使用重 [**迭結構進行**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 非同步完成的函式會傳回 *PBytesReceived* (或 *pBytesSent* 或 *pBytesRead*) 參數，指出同步傳輸的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="340fb-135">Some of the functions that use the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure for asynchronous completion return a *pBytesReceived* (or *pBytesSent* or *pBytesRead*) parameter that indicates the number of bytes transferred synchronously.</span></span> <span data-ttu-id="340fb-136">若為非同步呼叫，這個參數應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="340fb-136">For asynchronous calls, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="340fb-137">針對同步呼叫， *pBytesReceived* 參數是選擇性的，而且可以是 **Null** 或非 **null**。</span><span class="sxs-lookup"><span data-stu-id="340fb-137">For synchronous calls, the *pBytesReceived* parameter is optional and can be either **NULL** or non-**NULL**.</span></span>

<span data-ttu-id="340fb-138">如果事件物件用於非同步完成，則會呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="340fb-138">If the event object is used for asynchronous completion, the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function is called to determine the number of bytes read.</span></span> <span data-ttu-id="340fb-139">如果使用完成埠 (*hFile* 參數與 i/o 完成埠) 相關聯，則應用程式會呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式來判斷讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="340fb-139">If the completion port is used (the *hFile* parameter is associated with an I/O completion port), the application calls the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function to determine the number of bytes read.</span></span> <span data-ttu-id="340fb-140">如果非同步作業尚未完成，應用程式可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="340fb-140">If the asynchronous operations have not completed, applications can call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function to obtain extended error information.</span></span>

<span data-ttu-id="340fb-141">下表摘要說明函式（例如使用 *pBytesReceived* 參數的 [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) ）中同步和非同步完成的完成行為。</span><span class="sxs-lookup"><span data-stu-id="340fb-141">The following table summarizes the completion behavior for synchronous and asynchronous completion in functions such as [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) that use the *pBytesReceived* parameter.</span></span>



| <span data-ttu-id="340fb-142">pBytesReceived\*</span><span class="sxs-lookup"><span data-stu-id="340fb-142">pBytesReceived\*</span></span> | <span data-ttu-id="340fb-143">pOverlapped</span><span class="sxs-lookup"><span data-stu-id="340fb-143">pOverlapped</span></span>  | <span data-ttu-id="340fb-144">Description</span><span class="sxs-lookup"><span data-stu-id="340fb-144">Description</span></span>                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="340fb-145">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-145">**NULL**</span></span>         | <span data-ttu-id="340fb-146">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-146">**NULL**</span></span>     | <span data-ttu-id="340fb-147">應用程式不會收到傳回的位元組數目資訊。</span><span class="sxs-lookup"><span data-stu-id="340fb-147">The application does not receive information on the number of bytes returned.</span></span>           |
| <span data-ttu-id="340fb-148">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-148">**NULL**</span></span>         | <span data-ttu-id="340fb-149">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-149">Non-**NULL**</span></span> | <span data-ttu-id="340fb-150">非同步作業， *pBytesReceived* 沒有意義。</span><span class="sxs-lookup"><span data-stu-id="340fb-150">Asynchronous operation, *pBytesReceived* is meaningless.</span></span>                                |
| <span data-ttu-id="340fb-151">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-151">Non-**NULL**</span></span>     | <span data-ttu-id="340fb-152">**NULL**</span><span class="sxs-lookup"><span data-stu-id="340fb-152">**NULL**</span></span>     | <span data-ttu-id="340fb-153">同步作業， *pBytesReceived* 中傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="340fb-153">Synchronous operation, number of bytes returned in *pBytesReceived*.</span></span>                    |
| <span data-ttu-id="340fb-154">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-154">Non-**NULL**</span></span>     | <span data-ttu-id="340fb-155">非 **Null**</span><span class="sxs-lookup"><span data-stu-id="340fb-155">Non-**NULL**</span></span> | <span data-ttu-id="340fb-156">非同步作業，即使它不是 **Null**，也會忽略 *pBytesReceived* 。\*\*</span><span class="sxs-lookup"><span data-stu-id="340fb-156">Asynchronous operation, *pBytesReceived* is ignored even though it is not **NULL**.\*\*</span></span> |



 

> [!Note]  
> <span data-ttu-id="340fb-157">\*此參數也可以是 *pBytesSent* 或 *pBytesRead*。</span><span class="sxs-lookup"><span data-stu-id="340fb-157">\*This parameter can also be *pBytesSent* or *pBytesRead*.</span></span>

 

> [!Note]  
> <span data-ttu-id="340fb-158">\*\*建議應用程式在 *pBytesReceived* 中傳遞 **Null** 以進行非同步作業，並取得從 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)或 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)接收的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="340fb-158">\*\*It is recommended that applications pass a **NULL** in *pBytesReceived* for asynchronous operations and obtain the number of bytes received from either [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) or [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

 

## <a name="return-codes"></a><span data-ttu-id="340fb-159">傳回碼</span><span class="sxs-lookup"><span data-stu-id="340fb-159">Return Codes</span></span>

<span data-ttu-id="340fb-160">HTTP 伺服器 API 會針對非同步函式呼叫傳回三個程式碼類別。</span><span class="sxs-lookup"><span data-stu-id="340fb-160">The HTTP Server API returns three classes of codes for asynchronous function calls.</span></span>

-   <span data-ttu-id="340fb-161">沒有 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="340fb-161">NO\_ERROR</span></span>
-   <span data-ttu-id="340fb-162">錯誤 \_ IO \_ 暫止</span><span class="sxs-lookup"><span data-stu-id="340fb-162">ERROR\_IO\_PENDING</span></span>
-   <span data-ttu-id="340fb-163">任何其他 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="340fb-163">Any other [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="340fb-164">當錯誤 \_ IO \_ 暫止或 \_ 從非同步函式呼叫傳回錯誤時，使用者應該會預期事件或完成常式會收到信號。</span><span class="sxs-lookup"><span data-stu-id="340fb-164">When ERROR\_IO\_PENDING or NO\_ERROR are returned from the asynchronous function call, users should expect the event or completion routine to be signaled.</span></span> <span data-ttu-id="340fb-165">針對事件或完成埠的 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)函式，會傳回完成狀態。</span><span class="sxs-lookup"><span data-stu-id="340fb-165">Calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function for the event or the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function for the completion port returns the completion status.</span></span> <span data-ttu-id="340fb-166">此外，如果未 \_ 傳回任何錯誤，應用程式可以在進行 API 呼叫的相同執行緒上執行後續處理。</span><span class="sxs-lookup"><span data-stu-id="340fb-166">In addition, if NO\_ERROR is returned, applications can perform post-processing on the same thread that made the API call.</span></span>

<span data-ttu-id="340fb-167">如果 HTTP 伺服器 API 傳回錯誤 \_ IO \_ 暫止或沒有錯誤的任何作業 \_ ，則從非同步函式呼叫中，完成常式不會收到信號，且 API 會直接傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="340fb-167">If the HTTP Server API returns anything other than ERROR\_IO\_PENDING or NO\_ERROR, from the asynchronous function call, the completion routine is not signaled, and the error is directly returned by the API.</span></span>

 

 
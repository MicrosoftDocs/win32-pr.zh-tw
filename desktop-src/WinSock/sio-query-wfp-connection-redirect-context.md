---
description: 控制項程式碼會抓取 Windows 篩選平台重新導向服務所使用之重新導向記錄的重新導向內容。
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113012"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="ad9c6-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="ad9c6-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="ad9c6-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad9c6-104">Description</span></span>

<span data-ttu-id="ad9c6-105">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 內容** 控制程式代碼會針對 Windows 篩選平台 (WFP) 重新導向服務所使用的重新導向記錄，抓取重新導向內容。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="ad9c6-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure 
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="ad9c6-107">參數</span><span class="sxs-lookup"><span data-stu-id="ad9c6-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="ad9c6-108">s</span><span class="sxs-lookup"><span data-stu-id="ad9c6-108">s</span></span>

<span data-ttu-id="ad9c6-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="ad9c6-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="ad9c6-110">dwIoControlCode</span></span>

<span data-ttu-id="ad9c6-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-111">The control code for the operation.</span></span>
<span data-ttu-id="ad9c6-112">針對此作業使用 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 內容** 。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="ad9c6-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad9c6-113">lpvInBuffer</span></span>

<span data-ttu-id="ad9c6-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="ad9c6-115">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="ad9c6-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad9c6-116">cbInBuffer</span></span>

<span data-ttu-id="ad9c6-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="ad9c6-118">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="ad9c6-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad9c6-119">lpvOutBuffer</span></span>

<span data-ttu-id="ad9c6-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="ad9c6-121">如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數應指向 **ULONG** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="ad9c6-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad9c6-122">cbOutBuffer</span></span>

<span data-ttu-id="ad9c6-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="ad9c6-124">此參數必須至少為 **ULONG** 資料類型的大小。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="ad9c6-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="ad9c6-125">lpcbBytesReturned</span></span>

<span data-ttu-id="ad9c6-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="ad9c6-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="ad9c6-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="ad9c6-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="ad9c6-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="ad9c6-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="ad9c6-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="ad9c6-132">lpvOverlapped</span></span>

<span data-ttu-id="ad9c6-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad9c6-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="ad9c6-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="ad9c6-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad9c6-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="ad9c6-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="ad9c6-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="ad9c6-139">lpCompletionRoutine</span></span>

<span data-ttu-id="ad9c6-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="ad9c6-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="ad9c6-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="ad9c6-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="ad9c6-142">lpThreadId</span></span>

<span data-ttu-id="ad9c6-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="ad9c6-144">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="ad9c6-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="ad9c6-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="ad9c6-146">lpErrno</span></span>

<span data-ttu-id="ad9c6-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-147">A pointer to the error code.</span></span>

<span data-ttu-id="ad9c6-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad9c6-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad9c6-149">Return value</span></span>

<span data-ttu-id="ad9c6-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="ad9c6-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="ad9c6-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="ad9c6-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ad9c6-153">Error code</span></span> | <span data-ttu-id="ad9c6-154">意義</span><span class="sxs-lookup"><span data-stu-id="ad9c6-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="ad9c6-155">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="ad9c6-156">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="ad9c6-157">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="ad9c6-158">因為通訊端關閉或 SIO_FLUSH IOCTL 命令的執行，所以重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="ad9c6-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-159">**WSAEFAULT**</span></span> | <span data-ttu-id="ad9c6-160">*LpvOutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="ad9c6-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="ad9c6-162">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="ad9c6-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-163">**WSAEINTR**</span></span> | <span data-ttu-id="ad9c6-164">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="ad9c6-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-165">**WSAEINVAL**</span></span> | <span data-ttu-id="ad9c6-166">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="ad9c6-167">如果 *cbOutBuffer* 參數小於 **ULONG** 資料類型的大小，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="ad9c6-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="ad9c6-169">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="ad9c6-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="ad9c6-171">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="ad9c6-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="ad9c6-173">*通訊端未連線*。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="ad9c6-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="ad9c6-175">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="ad9c6-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="ad9c6-177">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="ad9c6-178">如果傳輸提供者不支援 **SIO \_ QUERY \_ WFP \_ 連接 \_ \_ 內容** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="ad9c6-179">備註</span><span class="sxs-lookup"><span data-stu-id="ad9c6-179">Remarks</span></span>

<span data-ttu-id="ad9c6-180">在 Windows 8、Windows Server 2012 和更新版本的作業系統上，都支援 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 內容** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="ad9c6-181">WFP 允許存取 TCP/IP 封包處理路徑，也就是傳出和傳入的封包可以進行檢查或變更，然後再讓它們進一步處理。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="ad9c6-182">藉由使用 TCP/IP 處理路徑，獨立軟體廠商 (Isv) 可以更輕鬆地建立防火牆、防毒軟體、診斷軟體及其他類型的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="ad9c6-183">WFP 提供使用者模式和核心模式元件，讓協力廠商 Isv 可以參與在 TCP/IP 通訊協定堆疊和整個作業系統中的數個層級進行的篩選決策。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="ad9c6-184">[WFP 連接重新導向] 功能可讓 WFP 標注核心驅動程式將連接重新導向至使用者模式進程、在使用者模式中執行內容檢查，以及使用不同的連線將已檢查的內容轉送到原始目的地。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="ad9c6-185">**SIO \_ QUERY WFP 連線重新 \_ \_ \_ 導向 \_ 內容** IOCTL 和數個其他相關 IOCTLS 是使用者模式元件，用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="ad9c6-186">每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="ad9c6-187">由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="ad9c6-188">如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="ad9c6-189">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 內容** IOCTL 可用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="ad9c6-190">每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="ad9c6-191">由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="ad9c6-192">如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="ad9c6-193">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 內容** IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="ad9c6-194">這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="ad9c6-195">**SIO \_ QUERY \_ wfp 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 是由 WFP 型重新導向服務用來從已接受的 tcp/ip 封包連線取得重新導向記錄， (tcp 通訊端或 UDP 通訊端的連線通訊端，例如) 重新導向至以核心模式驅動程式中的 **ALE 連接重新 \_ \_ 導向** 層所註冊的隨附核心模式注標。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="ad9c6-196">以 WFP 為基礎的重新導向服務會使用 **SIO \_ QUERY WFP 連線重新 \_ \_ \_ 導向 \_ 內容** IOCTL，以針對 tcp 通訊端或 UDP 通訊端的連線通訊端，從接受的 tcp/ip 封 (包連線取得重新導向記錄的重新導向內容，例如，) 透過其在 **ALE_CONNECT_REDIRECT** 層級註冊的隨附注標重新導向。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="ad9c6-197">重新導向內容是選擇性的，如果連接目前的重新導向狀態是由呼叫重新導向服務重新導向連接，或先前被呼叫重新導向服務重新導向，但稍後又由不同的重新導向服務重新導向，則會使用。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="ad9c6-198">重新導向服務會使用 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL，將抓取的重新導向記錄傳輸至它用來 proxy 原始內容的 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="ad9c6-199">因為 WFP 重新導向內容是重新導向服務所設定的可變長度資料 blob，所以呼叫端可以提供大型的輸出緩衝區 (*lpvOutBuffer* 參數所指向的1千個緩衝區，例如) 或可在 *cbOutBuffer* 參數為0的輸出緩衝區大小中傳遞，以查詢保存所傳回之 blob 所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="ad9c6-200">如果輸出緩衝區大小不足以保存資料，則 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會傳回 **錯誤的 \_ \_ 緩衝區** ，而所需的緩衝區大小將會以 *lpcbBytesReturned* 參數所指向的值傳回。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="ad9c6-201">呼叫 **SIO \_ QUERY \_ WF \ P_CONNECTION 重新 \_ 導向 \_ 記錄** 的應用程式不需要瞭解包含已抓取之重新導向記錄的 blob。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="ad9c6-202">這是不透明的資料 blob，應用程式需要將其取出並傳回至新的通訊端。</span><span class="sxs-lookup"><span data-stu-id="ad9c6-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad9c6-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad9c6-203">See also</span></span>

[<span data-ttu-id="ad9c6-204">**IPPROTO_IP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="ad9c6-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="ad9c6-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="ad9c6-207">**插座**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="ad9c6-208">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="ad9c6-209">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="ad9c6-210">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="ad9c6-211">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="ad9c6-212">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="ad9c6-213">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="ad9c6-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

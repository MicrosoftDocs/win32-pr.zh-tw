---
description: 控制項程式碼會查詢通訊端與 RSS 處理器核心和 NUMA 節點之間的關聯。
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943417"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="30dc4-103">SIO_QUERY_RSS_PROCESSOR_INFO 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="30dc4-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="30dc4-104">Description</span><span class="sxs-lookup"><span data-stu-id="30dc4-104">Description</span></span>

<span data-ttu-id="30dc4-105">**SIO \_ QUERY \_ RSS \_ 處理器 \_ 資訊** 控制項程式碼會查詢通訊端與 RSS 處理器核心和 NUMA 節點之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="30dc4-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="30dc4-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="30dc4-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="30dc4-107">參數</span><span class="sxs-lookup"><span data-stu-id="30dc4-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="30dc4-108">s</span><span class="sxs-lookup"><span data-stu-id="30dc4-108">s</span></span>

<span data-ttu-id="30dc4-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="30dc4-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="30dc4-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="30dc4-110">dwIoControlCode</span></span>

<span data-ttu-id="30dc4-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="30dc4-111">The control code for the operation.</span></span>
<span data-ttu-id="30dc4-112">使用 **SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="30dc4-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="30dc4-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="30dc4-113">lpvInBuffer</span></span>

<span data-ttu-id="30dc4-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="30dc4-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="30dc4-115">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="30dc4-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="30dc4-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="30dc4-116">cbInBuffer</span></span>

<span data-ttu-id="30dc4-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="30dc4-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="30dc4-118">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="30dc4-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="30dc4-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="30dc4-119">lpvOutBuffer</span></span>

<span data-ttu-id="30dc4-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="30dc4-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="30dc4-121">如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數應指向 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)結構。</span><span class="sxs-lookup"><span data-stu-id="30dc4-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="30dc4-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="30dc4-122">cbOutBuffer</span></span>

<span data-ttu-id="30dc4-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="30dc4-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="30dc4-124">此參數至少必須是 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="30dc4-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="30dc4-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="30dc4-125">lpcbBytesReturned</span></span>

<span data-ttu-id="30dc4-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="30dc4-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="30dc4-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 *DWORD* 值零。</span><span class="sxs-lookup"><span data-stu-id="30dc4-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="30dc4-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="30dc4-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="30dc4-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="30dc4-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="30dc4-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="30dc4-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="30dc4-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="30dc4-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="30dc4-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="30dc4-132">lpvOverlapped</span></span>

<span data-ttu-id="30dc4-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="30dc4-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="30dc4-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="30dc4-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="30dc4-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="30dc4-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="30dc4-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="30dc4-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="30dc4-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="30dc4-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="30dc4-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="30dc4-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="30dc4-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="30dc4-139">lpCompletionRoutine</span></span>

<span data-ttu-id="30dc4-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="30dc4-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="30dc4-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="30dc4-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="30dc4-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="30dc4-142">lpThreadId</span></span>

<span data-ttu-id="30dc4-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="30dc4-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="30dc4-144">在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="30dc4-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="30dc4-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="30dc4-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="30dc4-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="30dc4-146">lpErrno</span></span>

<span data-ttu-id="30dc4-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="30dc4-147">A pointer to the error code.</span></span>

<span data-ttu-id="30dc4-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="30dc4-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="30dc4-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="30dc4-149">Return value</span></span>

<span data-ttu-id="30dc4-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="30dc4-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="30dc4-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="30dc4-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="30dc4-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="30dc4-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="30dc4-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="30dc4-153">Error code</span></span> | <span data-ttu-id="30dc4-154">意義</span><span class="sxs-lookup"><span data-stu-id="30dc4-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="30dc4-155">**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="30dc4-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="30dc4-156">傳遞給系統呼叫的資料區域太小。</span><span class="sxs-lookup"><span data-stu-id="30dc4-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="30dc4-157">如果 *lpvOutBuffer* 參數所指向的緩衝區的緩衝區大小超過 *cbOutBuffer* 參數，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="30dc4-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="30dc4-158">所需的緩衝區大小將會在 *lpcbBytesReturned* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="30dc4-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="30dc4-159">如果 *cbOutBuffer* 參數小於 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) 結構的大小，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="30dc4-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="30dc4-160">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="30dc4-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="30dc4-161">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="30dc4-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="30dc4-162">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="30dc4-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="30dc4-163">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="30dc4-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="30dc4-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="30dc4-164">**WSAEFAULT**</span></span> | <span data-ttu-id="30dc4-165">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="30dc4-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="30dc4-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="30dc4-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="30dc4-167">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="30dc4-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="30dc4-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="30dc4-168">**WSAEINTR**</span></span> | <span data-ttu-id="30dc4-169">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="30dc4-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="30dc4-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="30dc4-170">**WSAEINVAL**</span></span> | <span data-ttu-id="30dc4-171">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="30dc4-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="30dc4-172">如果 *cbOutBuffer* 參數小於 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) 結構的大小，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="30dc4-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="30dc4-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="30dc4-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="30dc4-174">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="30dc4-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="30dc4-175">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="30dc4-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="30dc4-176">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="30dc4-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="30dc4-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="30dc4-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="30dc4-178">*通訊端未連線*。</span><span class="sxs-lookup"><span data-stu-id="30dc4-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="30dc4-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="30dc4-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="30dc4-180">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="30dc4-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="30dc4-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="30dc4-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="30dc4-182">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="30dc4-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="30dc4-183">如果傳輸提供者不支援 **SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="30dc4-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="30dc4-184">備註</span><span class="sxs-lookup"><span data-stu-id="30dc4-184">Remarks</span></span>

<span data-ttu-id="30dc4-185">Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="30dc4-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="30dc4-186">**SIO \_ 查詢 \_ RSS \_ 處理器 \_ 資訊** IOCTL 可用來決定通訊端與 rss 處理器核心和 NUMA 節點之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="30dc4-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="30dc4-187">這個 IOCTL 會傳回 [**通訊端 \_ 處理器 \_ 親和性**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) 結構，其中包含 [**處理器 \_ 編號**](/windows/desktop/api/winnt/ns-winnt-processor_number) 和 NUMA 節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="30dc4-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="30dc4-188">傳回的 [**處理器 \_ 編號**](/windows/desktop/api/winnt/ns-winnt-processor_number) 結構包含群組中的群組編號和相對處理器號碼。</span><span class="sxs-lookup"><span data-stu-id="30dc4-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="30dc4-189">如果通訊端是 UDP 通訊端，則必須連接通訊端， **SIO \_ QUERY \_ RSS \_ 處理器 \_ 資訊** IOCTL 才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="30dc4-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="30dc4-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30dc4-190">See also</span></span>

[<span data-ttu-id="30dc4-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="30dc4-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="30dc4-192">**插座**</span><span class="sxs-lookup"><span data-stu-id="30dc4-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="30dc4-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="30dc4-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="30dc4-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="30dc4-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="30dc4-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="30dc4-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="30dc4-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="30dc4-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="30dc4-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="30dc4-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="30dc4-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="30dc4-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="30dc4-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="30dc4-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

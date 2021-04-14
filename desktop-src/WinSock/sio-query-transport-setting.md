---
description: 控制項程式碼會查詢通訊端上的傳輸設定。
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848634"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="60826-103">SIO_QUERY_TRANSPORT_SETTING 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="60826-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="60826-104">Description</span><span class="sxs-lookup"><span data-stu-id="60826-104">Description</span></span>

<span data-ttu-id="60826-105">**SIO \_ QUERY \_ 傳輸 \_ 設定** 控制程式代碼會查詢通訊端上的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="60826-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="60826-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="60826-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="60826-107">參數</span><span class="sxs-lookup"><span data-stu-id="60826-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="60826-108">s</span><span class="sxs-lookup"><span data-stu-id="60826-108">s</span></span>

<span data-ttu-id="60826-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="60826-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="60826-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="60826-110">dwIoControlCode</span></span>

<span data-ttu-id="60826-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="60826-111">The control code for the operation.</span></span>
<span data-ttu-id="60826-112">使用 **SIO \_ 查詢 \_ 傳輸 \_ 設定** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="60826-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="60826-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="60826-113">lpvInBuffer</span></span>

<span data-ttu-id="60826-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="60826-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="60826-115">此參數包含結構的指標，其中結構的第一個成員是 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 結構，可判斷正在查詢的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="60826-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="60826-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="60826-116">cbInBuffer</span></span>

<span data-ttu-id="60826-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60826-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="60826-118">此參數取決於正在查詢的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="60826-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="60826-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="60826-119">lpvOutBuffer</span></span>

<span data-ttu-id="60826-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="60826-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="60826-121">如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數取決於正在查詢的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="60826-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="60826-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="60826-122">cbOutBuffer</span></span>

<span data-ttu-id="60826-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60826-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="60826-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="60826-124">lpcbBytesReturned</span></span>

<span data-ttu-id="60826-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60826-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="60826-126">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="60826-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="60826-127">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="60826-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="60826-128">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="60826-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="60826-129">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="60826-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="60826-130">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="60826-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="60826-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="60826-131">lpvOverlapped</span></span>

<span data-ttu-id="60826-132">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60826-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="60826-133">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="60826-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="60826-134">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="60826-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="60826-135">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="60826-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="60826-136">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="60826-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="60826-137">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="60826-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="60826-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="60826-138">lpCompletionRoutine</span></span>

<span data-ttu-id="60826-139">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="60826-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="60826-140">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="60826-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="60826-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="60826-141">lpThreadId</span></span>

<span data-ttu-id="60826-142">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="60826-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="60826-143">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="60826-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="60826-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="60826-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="60826-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="60826-145">lpErrno</span></span>

<span data-ttu-id="60826-146">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="60826-146">A pointer to the error code.</span></span>

<span data-ttu-id="60826-147">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="60826-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="60826-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="60826-148">Return value</span></span>

<span data-ttu-id="60826-149">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="60826-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="60826-150">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="60826-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="60826-151">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="60826-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="60826-152">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="60826-152">Error code</span></span> | <span data-ttu-id="60826-153">意義</span><span class="sxs-lookup"><span data-stu-id="60826-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="60826-154">**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="60826-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="60826-155">傳遞給系統呼叫的資料區域太小。</span><span class="sxs-lookup"><span data-stu-id="60826-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="60826-156">如果 *lpvOutBuffer* 參數所指向的緩衝區的緩衝區大小超過 *cbOutBuffer* 參數，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="60826-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="60826-157">所需的緩衝區大小將會在 *lpcbBytesReturned* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="60826-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="60826-158">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="60826-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="60826-159">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="60826-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="60826-160">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="60826-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="60826-161">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="60826-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="60826-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="60826-162">**WSAEFAULT**</span></span> | <span data-ttu-id="60826-163">*LpvOutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="60826-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="60826-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="60826-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="60826-165">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="60826-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="60826-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="60826-166">**WSAEINTR**</span></span> | <span data-ttu-id="60826-167">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="60826-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="60826-168">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="60826-168">**WSAEINVAL**</span></span> | <span data-ttu-id="60826-169">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="60826-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="60826-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="60826-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="60826-171">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="60826-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="60826-172">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="60826-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="60826-173">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="60826-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="60826-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="60826-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="60826-175">通訊端未連線。</span><span class="sxs-lookup"><span data-stu-id="60826-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="60826-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="60826-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="60826-177">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="60826-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="60826-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="60826-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="60826-179">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="60826-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="60826-180">如果傳輸提供者不支援 **SIO \_ 查詢 \_ 傳輸 \_ 設定** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="60826-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="60826-181">備註</span><span class="sxs-lookup"><span data-stu-id="60826-181">Remarks</span></span>

<span data-ttu-id="60826-182">Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO \_ 查詢 \_ 傳輸 \_ 設定** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="60826-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="60826-183">**SIO \_ 查詢 \_ 傳輸 \_ 設定** IOCTL 是一般的 ioctl，用來查詢通訊端上的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="60826-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="60826-184">正在查詢的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)為基礎。</span><span class="sxs-lookup"><span data-stu-id="60826-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="60826-185">目前唯一定義的傳輸設定是用於 TCP 通訊端上的 **即時 \_ \_ 通知 \_ 功能** 功能。</span><span class="sxs-lookup"><span data-stu-id="60826-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="60826-186">如果傳入 *lpvInBuffer* 參數的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)將 Guid 成員設為 **即時 \_ \_ 通知 \_ 功能**，則這是要求查詢與 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)搭配使用的 TCP 通訊端即時通知設定，以在 Windows Store 應用程式中接收背景網路通知。</span><span class="sxs-lookup"><span data-stu-id="60826-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="60826-187">*LpvInBuffer* 參數應指向 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)結構。</span><span class="sxs-lookup"><span data-stu-id="60826-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="60826-188">*LpvOutBuffer* 參數應指向 **即時 \_ \_ 通知 \_ 設定 \_ 輸出** 結構。</span><span class="sxs-lookup"><span data-stu-id="60826-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="60826-189">此傳輸設定只適用于 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="60826-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="60826-190">此傳輸設定提供一種方式，讓 WinInet 或類似的網路服務查詢指定的 TCP 通訊端，以判斷 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 狀態。</span><span class="sxs-lookup"><span data-stu-id="60826-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="60826-191">Windows Store 應用程式不會直接呼叫這個 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="60826-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="60826-192">如果 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 呼叫成功，這個 IOCTL 會以目前的狀態傳回 **即時 \_ \_ 通知 \_ 設定 \_ 輸出** 結構。</span><span class="sxs-lookup"><span data-stu-id="60826-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="60826-193">**SIO \_ QUERY \_ 傳輸 \_ 設定** IOCTL 提供一種方式，可讓 WinInet 或類似的網路服務查詢指定 TCP 通訊端的傳輸設定狀態，以判斷是否已在通訊端上啟用 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 。</span><span class="sxs-lookup"><span data-stu-id="60826-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="60826-194">Windows Store 應用程式不會直接呼叫這個 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="60826-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="60826-195">這個 IOCTL 只適用于 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="60826-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="60826-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60826-196">See also</span></span>

[<span data-ttu-id="60826-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="60826-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="60826-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="60826-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="60826-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="60826-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="60826-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="60826-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="60826-201">插座</span><span class="sxs-lookup"><span data-stu-id="60826-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="60826-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="60826-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="60826-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="60826-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="60826-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="60826-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="60826-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="60826-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="60826-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="60826-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="60826-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="60826-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

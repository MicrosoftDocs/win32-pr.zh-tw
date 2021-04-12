---
description: 在通訊端上設定初始重新傳輸超時 (RTO) 參數的控制項程式碼。
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/09/2020
ms.locfileid: "104463884"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="9b4f5-103">SIO_TCP_INITIAL_RTO 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="9b4f5-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="9b4f5-104">Description</span><span class="sxs-lookup"><span data-stu-id="9b4f5-104">Description</span></span>

<span data-ttu-id="9b4f5-105">**SIO_TCP_INITIAL_RTO** 控制程式代碼會設定通訊端上的初始重新傳輸超時 (RTO) 參數。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="9b4f5-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="9b4f5-107">參數</span><span class="sxs-lookup"><span data-stu-id="9b4f5-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="9b4f5-108">s</span><span class="sxs-lookup"><span data-stu-id="9b4f5-108">s</span></span>

<span data-ttu-id="9b4f5-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="9b4f5-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="9b4f5-110">dwIoControlCode</span></span>

<span data-ttu-id="9b4f5-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-111">The control code for the operation.</span></span>
<span data-ttu-id="9b4f5-112">使用 **SIO_TCP_INITIAL_RTO** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="9b4f5-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="9b4f5-113">lpvInBuffer</span></span>

<span data-ttu-id="9b4f5-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="9b4f5-115">此參數包含與通訊端相關聯之 [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="9b4f5-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="9b4f5-116">cbInBuffer</span></span>

<span data-ttu-id="9b4f5-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="9b4f5-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="9b4f5-118">lpvOutBuffer</span></span>

<span data-ttu-id="9b4f5-119">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="9b4f5-120">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="9b4f5-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="9b4f5-121">cbOutBuffer</span></span>

<span data-ttu-id="9b4f5-122">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="9b4f5-123">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="9b4f5-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="9b4f5-124">lpcbBytesReturned</span></span>

<span data-ttu-id="9b4f5-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="9b4f5-126">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="9b4f5-127">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="9b4f5-128">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="9b4f5-129">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="9b4f5-130">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="9b4f5-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="9b4f5-131">lpvOverlapped</span></span>

<span data-ttu-id="9b4f5-132">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="9b4f5-133">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="9b4f5-134">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="9b4f5-135">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="9b4f5-136">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="9b4f5-137">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="9b4f5-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="9b4f5-138">lpCompletionRoutine</span></span>

<span data-ttu-id="9b4f5-139">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="9b4f5-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="9b4f5-140">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="9b4f5-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="9b4f5-141">lpThreadId</span></span>

<span data-ttu-id="9b4f5-142">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="9b4f5-143">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="9b4f5-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="9b4f5-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="9b4f5-145">lpErrno</span></span>

<span data-ttu-id="9b4f5-146">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-146">A pointer to the error code.</span></span>

<span data-ttu-id="9b4f5-147">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b4f5-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b4f5-148">Return value</span></span>

<span data-ttu-id="9b4f5-149">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="9b4f5-150">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="9b4f5-151">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="9b4f5-152">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9b4f5-152">Error code</span></span> | <span data-ttu-id="9b4f5-153">意義</span><span class="sxs-lookup"><span data-stu-id="9b4f5-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="9b4f5-154">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="9b4f5-155">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="9b4f5-156">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="9b4f5-157">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="9b4f5-158">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="9b4f5-159">如果因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="9b4f5-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-160">**WSAEACCES**</span></span> | <span data-ttu-id="9b4f5-161">嘗試以存取權限禁止的方式存取通訊端。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="9b4f5-162">這項錯誤會在包含下列各項的條件下傳回：使用者缺少本機電腦上所需的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="9b4f5-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-163">**WSAEFAULT**</span></span> | <span data-ttu-id="9b4f5-164">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="9b4f5-165">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="9b4f5-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="9b4f5-167">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="9b4f5-168">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="9b4f5-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-169">**WSAEINTR**</span></span> | <span data-ttu-id="9b4f5-170">呼叫 *WSACancelBlockingCall* 時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="9b4f5-171">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="9b4f5-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-172">**WSAEINVAL**</span></span> | <span data-ttu-id="9b4f5-173">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-173">An invalid argument was supplied.</span></span> <span data-ttu-id="9b4f5-174">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="9b4f5-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="9b4f5-176">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="9b4f5-177">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="9b4f5-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="9b4f5-179">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="9b4f5-180">如果描述項不是通訊端，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="9b4f5-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="9b4f5-182">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="9b4f5-183">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="9b4f5-184">如果傳輸提供者不支援 **SIO_TCP_INITIAL_RTO** 的 IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="9b4f5-185">備註</span><span class="sxs-lookup"><span data-stu-id="9b4f5-185">Remarks</span></span>

<span data-ttu-id="9b4f5-186">應用程式可以使用 **SIO_TCP_INITIAL_RTO** 的 IOCTL 來控制 TCP 通訊端的初始 (SYN/SYN + ACK) 重新傳輸特性（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="9b4f5-187">如果使用此選項，應用程式必須在啟動通訊端上的 TCP 連線嘗試之前提供適當的值。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="9b4f5-188">[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)的 IOCTL 可讓應用程式設定第一次 (SYN) 通訊端所使用的重新傳輸超時 (RTO) 。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="9b4f5-189">*LpvInBuffer* 參數中所傳遞之 [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)結構的指標，可讓應用程式設定 (RTT) 用來計算重新傳輸超時時間的初始來回行程時間。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="9b4f5-190">應用程式也可以設定在連接嘗試失敗之前嘗試的重新傳輸數目。</span><span class="sxs-lookup"><span data-stu-id="9b4f5-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b4f5-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b4f5-191">See also</span></span>

[<span data-ttu-id="9b4f5-192">插座</span><span class="sxs-lookup"><span data-stu-id="9b4f5-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="9b4f5-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="9b4f5-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="9b4f5-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="9b4f5-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="9b4f5-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="9b4f5-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="9b4f5-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="9b4f5-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

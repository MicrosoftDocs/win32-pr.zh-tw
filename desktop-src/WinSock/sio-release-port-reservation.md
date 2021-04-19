---
description: 控制項程式碼會針對 TCP 或 UDP 埠的區塊釋放執行時間保留。
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: SIO_RELEASE_PORT_RESER加值稅ION 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976814"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="eb79e-103">SIO_RELEASE_PORT_RESER加值稅ION 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="eb79e-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="eb79e-104">Description</span><span class="sxs-lookup"><span data-stu-id="eb79e-104">Description</span></span>

<span data-ttu-id="eb79e-105">**SIO \_ RELEASE \_ PORT \_ 保留** 控制項程式碼會釋放 TCP 或 UDP 埠區塊的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="eb79e-106">使用 [**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md) IOCTL 時，必須從發行程式取得要發行的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="eb79e-107">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="eb79e-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="eb79e-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb79e-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="eb79e-109">s</span><span class="sxs-lookup"><span data-stu-id="eb79e-109">s</span></span>

<span data-ttu-id="eb79e-110">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="eb79e-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="eb79e-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="eb79e-111">dwIoControlCode</span></span>

<span data-ttu-id="eb79e-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="eb79e-112">The control code for the operation.</span></span>
<span data-ttu-id="eb79e-113">針對此作業使用 **SIO \_ 發行 \_ 埠 \_ 保留** 。</span><span class="sxs-lookup"><span data-stu-id="eb79e-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="eb79e-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="eb79e-114">lpvInBuffer</span></span>

<span data-ttu-id="eb79e-115">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="eb79e-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="eb79e-116">此參數包含 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的指標，其中包含要釋放之 TCP 或 UDP 埠保留的權杖。</span><span class="sxs-lookup"><span data-stu-id="eb79e-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="eb79e-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="eb79e-117">cbInBuffer</span></span>

<span data-ttu-id="eb79e-118">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb79e-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="eb79e-119">此參數必須至少為 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="eb79e-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="eb79e-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="eb79e-120">lpvOutBuffer</span></span>

<span data-ttu-id="eb79e-121">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="eb79e-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="eb79e-122">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="eb79e-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="eb79e-123">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="eb79e-123">cbOutBuffer</span></span>

<span data-ttu-id="eb79e-124">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb79e-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="eb79e-125">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="eb79e-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="eb79e-126">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="eb79e-126">lpcbBytesReturned</span></span>

<span data-ttu-id="eb79e-127">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb79e-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="eb79e-128">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="eb79e-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="eb79e-129">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="eb79e-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="eb79e-130">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="eb79e-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="eb79e-131">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="eb79e-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="eb79e-132">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="eb79e-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="eb79e-133">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="eb79e-133">lpvOverlapped</span></span>

<span data-ttu-id="eb79e-134">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="eb79e-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="eb79e-135">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="eb79e-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="eb79e-136">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="eb79e-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="eb79e-137">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="eb79e-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="eb79e-138">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="eb79e-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="eb79e-139">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="eb79e-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="eb79e-140">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="eb79e-140">lpCompletionRoutine</span></span>

<span data-ttu-id="eb79e-141">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="eb79e-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="eb79e-142">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="eb79e-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="eb79e-143">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="eb79e-143">lpThreadId</span></span>

<span data-ttu-id="eb79e-144">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="eb79e-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="eb79e-145">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="eb79e-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="eb79e-146">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="eb79e-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="eb79e-147">lpErrno</span><span class="sxs-lookup"><span data-stu-id="eb79e-147">lpErrno</span></span>

<span data-ttu-id="eb79e-148">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="eb79e-148">A pointer to the error code.</span></span>

<span data-ttu-id="eb79e-149">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="eb79e-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb79e-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb79e-150">Return value</span></span>

<span data-ttu-id="eb79e-151">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="eb79e-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="eb79e-152">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="eb79e-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="eb79e-153">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="eb79e-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="eb79e-154">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="eb79e-154">Error code</span></span> | <span data-ttu-id="eb79e-155">意義</span><span class="sxs-lookup"><span data-stu-id="eb79e-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="eb79e-156">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="eb79e-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="eb79e-157">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="eb79e-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="eb79e-158">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="eb79e-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="eb79e-159">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="eb79e-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="eb79e-160">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="eb79e-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="eb79e-161">如果因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="eb79e-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="eb79e-162">**WSAEFAULT**</span></span> | <span data-ttu-id="eb79e-163">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="eb79e-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="eb79e-164">*LpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="eb79e-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="eb79e-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="eb79e-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="eb79e-166">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="eb79e-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="eb79e-167">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="eb79e-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="eb79e-168">**WSAEINTR**</span></span> | <span data-ttu-id="eb79e-169">呼叫 **WSACancelBlockingCall** 時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="eb79e-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="eb79e-170">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="eb79e-171">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="eb79e-171">**WSAEINVAL**</span></span> | <span data-ttu-id="eb79e-172">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="eb79e-172">An invalid argument was supplied.</span></span> <span data-ttu-id="eb79e-173">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="eb79e-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="eb79e-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="eb79e-175">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="eb79e-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="eb79e-176">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="eb79e-177">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="eb79e-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="eb79e-178">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="eb79e-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="eb79e-179">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="eb79e-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="eb79e-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="eb79e-181">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="eb79e-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="eb79e-182">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="eb79e-183">如果傳輸提供者不支援 **SIO \_ 發行 \_ 埠 \_ 保留** IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="eb79e-184">當嘗試在 UDP 或 TCP 以外的通訊端上進行使用 **SIO \_ RELEASE \_ PORT \_ 保留** IOCTL 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb79e-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="eb79e-185">備註</span><span class="sxs-lookup"><span data-stu-id="eb79e-185">Remarks</span></span>

<span data-ttu-id="eb79e-186">在 Windows Vista 和更新版本的作業系統上，支援 **SIO \_ 發行 \_ 埠 \_ 保留** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="eb79e-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="eb79e-187">需要保留埠的應用程式和服務可以分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="eb79e-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="eb79e-188">第一個類別包含元件，而這些元件需要特定的埠做為其作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="eb79e-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="eb79e-189">這類元件通常會偏好在安裝期間指定其必要的埠 (在應用程式資訊清單中，例如) 。</span><span class="sxs-lookup"><span data-stu-id="eb79e-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="eb79e-190">第二個類別包含在執行時間需要任何可用埠或埠區塊的元件。</span><span class="sxs-lookup"><span data-stu-id="eb79e-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="eb79e-191">這兩個類別對應于特定和萬用字元埠保留要求。</span><span class="sxs-lookup"><span data-stu-id="eb79e-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="eb79e-192">特定的保留要求可能是持續性或執行時間，而萬用字元埠保留要求只在執行時間支援。</span><span class="sxs-lookup"><span data-stu-id="eb79e-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="eb79e-193">[**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md)的 IOCTL 可用來要求 TCP 或 UDP 埠區塊的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="eb79e-194">針對執行時間埠保留，埠集區會要求從其通訊端已授與保留的進程取用保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="eb79e-195">執行時間埠保留最後只會在呼叫 [**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md) IOCTL 的通訊端存留期內。</span><span class="sxs-lookup"><span data-stu-id="eb79e-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="eb79e-196">相反地，使用 [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) 或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) 函式所建立的持續性埠保留，可供任何程式使用，以取得持續保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="eb79e-197">**SIO \_ 發行 \_ 埠 \_ 保留** 的 IOCTL 可用來釋放 TCP 或 UDP 埠區塊的執行時間保留專案。</span><span class="sxs-lookup"><span data-stu-id="eb79e-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="eb79e-198">如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 **Null**，則會將此函式中的通訊端視為非重迭的通訊端。</span><span class="sxs-lookup"><span data-stu-id="eb79e-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="eb79e-199">若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。</span><span class="sxs-lookup"><span data-stu-id="eb79e-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="eb79e-200">如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。</span><span class="sxs-lookup"><span data-stu-id="eb79e-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="eb79e-201">針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="eb79e-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="eb79e-202">任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。</span><span class="sxs-lookup"><span data-stu-id="eb79e-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="eb79e-203">如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="eb79e-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="eb79e-204">**SIO \_ 發行 \_ 埠 \_ 保留** 的 IOCTL 可能會因為 **WSAEINTR** 或 WSA 作業在下列情況下 **\_ \_ 中止** 而失敗：</span><span class="sxs-lookup"><span data-stu-id="eb79e-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="eb79e-205">I/o 管理員會取消要求。</span><span class="sxs-lookup"><span data-stu-id="eb79e-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="eb79e-206">通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="eb79e-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="eb79e-207">範例</span><span class="sxs-lookup"><span data-stu-id="eb79e-207">Examples</span></span>

<span data-ttu-id="eb79e-208">下列範例會取得執行時間埠保留，然後釋放執行時間埠保留。</span><span class="sxs-lookup"><span data-stu-id="eb79e-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="eb79e-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb79e-209">See also</span></span>

[<span data-ttu-id="eb79e-210">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="eb79e-211">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="eb79e-212">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="eb79e-213">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="eb79e-214">**INET_PORT_RESER加值稅ION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="eb79e-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="eb79e-215">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="eb79e-216">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="eb79e-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="eb79e-217">**SIO_ACQUIRE_PORT_RESER加值稅ION**</span><span class="sxs-lookup"><span data-stu-id="eb79e-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="eb79e-218">**SIO_ASSOCIATE_PORT_RESER加值稅ION**</span><span class="sxs-lookup"><span data-stu-id="eb79e-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="eb79e-219">插座</span><span class="sxs-lookup"><span data-stu-id="eb79e-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="eb79e-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="eb79e-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="eb79e-221">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="eb79e-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="eb79e-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="eb79e-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="eb79e-223">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="eb79e-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="eb79e-224">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="eb79e-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="eb79e-225">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="eb79e-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

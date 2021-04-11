---
description: 控制項程式碼會將一個通訊端與在埠保留權杖所識別之 TCP 或 UDP 區塊的持續或執行時間保留產生關聯。
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: SIO_ASSOCIATE_PORT_RESER加值稅ION 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194031"
---
# <a name="sio_associate_port_reservation-control-code"></a><span data-ttu-id="cd376-103">SIO_ASSOCIATE_PORT_RESER加值稅ION 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="cd376-103">SIO_ASSOCIATE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="cd376-104">Description</span><span class="sxs-lookup"><span data-stu-id="cd376-104">Description</span></span>

<span data-ttu-id="cd376-105">**SIO 會 \_ 將通訊 \_ 埠 \_ 保留** 控制項程式碼與埠保留權杖所識別之 TCP 或 UDP 區塊的持續或執行時間保留產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cd376-105">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** control code associates a socket with a persistent or runtime reservation for a block of TCP or UDP identified by the port reservation token.</span></span>
<span data-ttu-id="cd376-106">這個 IOCTL 必須在系結器之前發出。</span><span class="sxs-lookup"><span data-stu-id="cd376-106">This IOCTL must be issued before the socket is bound.</span></span>
<span data-ttu-id="cd376-107">當通訊端系結時，會從指定權杖所識別的埠保留中選取指派給它的通訊埠。</span><span class="sxs-lookup"><span data-stu-id="cd376-107">If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token.</span></span>
<span data-ttu-id="cd376-108">如果指定的保留中沒有任何可用的埠，系 [**結函數呼叫**](/windows/desktop/api/winsock/nf-winsock-bind) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cd376-108">If no ports are available from the specified reservation, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function call will fail.</span></span>

<span data-ttu-id="cd376-109">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="cd376-109">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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

## <a name="parameters"></a><span data-ttu-id="cd376-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd376-110">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="cd376-111">s</span><span class="sxs-lookup"><span data-stu-id="cd376-111">s</span></span>

<span data-ttu-id="cd376-112">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="cd376-112">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="cd376-113">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="cd376-113">dwIoControlCode</span></span>

<span data-ttu-id="cd376-114">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="cd376-114">The control code for the operation.</span></span>
<span data-ttu-id="cd376-115">使用 **SIO \_ 將 \_ 埠 \_ 保留關聯** 于此作業。</span><span class="sxs-lookup"><span data-stu-id="cd376-115">Use **SIO\_ASSOCIATE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="cd376-116">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="cd376-116">lpvInBuffer</span></span>

<span data-ttu-id="cd376-117">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="cd376-117">A pointer to the input buffer.</span></span>
<span data-ttu-id="cd376-118">此參數包含 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的指標，其中包含要與通訊端產生關聯之 TCP 或 UDP 埠保留的權杖。</span><span class="sxs-lookup"><span data-stu-id="cd376-118">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to associate with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="cd376-119">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="cd376-119">cbInBuffer</span></span>

<span data-ttu-id="cd376-120">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd376-120">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="cd376-121">此參數必須至少為 [**INET_PORT_RESER加值稅ION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="cd376-121">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="cd376-122">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="cd376-122">lpvOutBuffer</span></span>

<span data-ttu-id="cd376-123">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="cd376-123">A pointer to the output buffer.</span></span>
<span data-ttu-id="cd376-124">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="cd376-124">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="cd376-125">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="cd376-125">cbOutBuffer</span></span>

<span data-ttu-id="cd376-126">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd376-126">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="cd376-127">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="cd376-127">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="cd376-128">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="cd376-128">lpcbBytesReturned</span></span>

<span data-ttu-id="cd376-129">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd376-129">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="cd376-130">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="cd376-130">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="cd376-131">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="cd376-131">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="cd376-132">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="cd376-132">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="cd376-133">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="cd376-133">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="cd376-134">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="cd376-134">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="cd376-135">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="cd376-135">lpvOverlapped</span></span>

<span data-ttu-id="cd376-136">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cd376-136">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="cd376-137">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="cd376-137">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="cd376-138">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="cd376-138">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="cd376-139">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="cd376-139">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="cd376-140">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="cd376-140">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="cd376-141">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="cd376-141">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="cd376-142">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="cd376-142">lpCompletionRoutine</span></span>

<span data-ttu-id="cd376-143">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="cd376-143">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="cd376-144">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="cd376-144">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="cd376-145">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="cd376-145">lpThreadId</span></span>

<span data-ttu-id="cd376-146">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="cd376-146">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="cd376-147">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="cd376-147">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="cd376-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="cd376-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="cd376-149">lpErrno</span><span class="sxs-lookup"><span data-stu-id="cd376-149">lpErrno</span></span>

<span data-ttu-id="cd376-150">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="cd376-150">A pointer to the error code.</span></span>

<span data-ttu-id="cd376-151">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="cd376-151">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd376-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd376-152">Return value</span></span>

<span data-ttu-id="cd376-153">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="cd376-153">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="cd376-154">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="cd376-154">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="cd376-155">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="cd376-155">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="cd376-156">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="cd376-156">Error code</span></span> | <span data-ttu-id="cd376-157">意義</span><span class="sxs-lookup"><span data-stu-id="cd376-157">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="cd376-158">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="cd376-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="cd376-159">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="cd376-159">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="cd376-160">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="cd376-160">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="cd376-161">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="cd376-161">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="cd376-162">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="cd376-162">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="cd376-163">如果因為通訊端關閉或 **SIO \_ FLUSH IOCTL** 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-163">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="cd376-164">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="cd376-164">**WSAEACCES**</span></span> | <span data-ttu-id="cd376-165">嘗試以存取權限禁止的方式存取通訊端。</span><span class="sxs-lookup"><span data-stu-id="cd376-165">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="cd376-166">持續性埠保留的幾個條件下會傳回此錯誤，包括下列各項：使用者在本機電腦上缺少必要的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。</span><span class="sxs-lookup"><span data-stu-id="cd376-166">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="cd376-167">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cd376-167">**WSAEFAULT**</span></span> | <span data-ttu-id="cd376-168">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="cd376-168">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="cd376-169">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="cd376-169">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="cd376-170">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="cd376-170">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="cd376-171">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="cd376-171">A blocking operation is currently executing.</span></span> <span data-ttu-id="cd376-172">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-172">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="cd376-173">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="cd376-173">**WSAEINTR**</span></span> | <span data-ttu-id="cd376-174">呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="cd376-174">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="cd376-175">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-175">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="cd376-176">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="cd376-176">**WSAEINVAL**</span></span> | <span data-ttu-id="cd376-177">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="cd376-177">An invalid argument was supplied.</span></span> <span data-ttu-id="cd376-178">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-178">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="cd376-179">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="cd376-179">**WSAENETDOWN**</span></span> | <span data-ttu-id="cd376-180">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="cd376-180">A socket operation encountered a dead network.</span></span> <span data-ttu-id="cd376-181">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-181">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="cd376-182">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="cd376-182">**WSAENOTSOCK**</span></span> | <span data-ttu-id="cd376-183">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="cd376-183">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="cd376-184">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-184">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="cd376-185">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="cd376-185">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="cd376-186">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="cd376-186">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="cd376-187">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-187">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="cd376-188">如果傳輸提供者不支援 **SIO \_ 相關聯的 \_ 埠 \_ 保留** 專案 IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-188">This error is also returned if the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="cd376-189">當嘗試使用 SIO 在 UDP 或 TCP 以外的通訊端上建立 **\_ \_ 埠 \_ 保留** IOCTL 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd376-189">This error is also returned when an attempt to use the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="cd376-190">備註</span><span class="sxs-lookup"><span data-stu-id="cd376-190">Remarks</span></span>

<span data-ttu-id="cd376-191">在 Windows Vista 和更新版本的作業系統上，支援 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="cd376-191">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="cd376-192">需要保留埠的應用程式和服務可以分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="cd376-192">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="cd376-193">第一個類別包含元件，而這些元件需要特定的埠做為其作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd376-193">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="cd376-194">這類元件通常會偏好在安裝期間指定其必要的埠 (在應用程式資訊清單中，例如) 。</span><span class="sxs-lookup"><span data-stu-id="cd376-194">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="cd376-195">第二個類別包含在執行時間需要任何可用埠或埠區塊的元件。</span><span class="sxs-lookup"><span data-stu-id="cd376-195">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="cd376-196">這兩個類別對應于特定和萬用字元埠保留要求。</span><span class="sxs-lookup"><span data-stu-id="cd376-196">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="cd376-197">特定的保留要求可能是持續性或執行時間，而萬用字元埠保留要求只在執行時間支援。</span><span class="sxs-lookup"><span data-stu-id="cd376-197">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="cd376-198">**SIO 會 \_ 建立 \_ 埠 \_ 保留** 專案 IOCTL 的關聯，以將 TCP 或 UDP 埠保留與持續或執行時間保留建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cd376-198">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used to associate a TCP or UDP port reservation with either a persistent or runtime reservation.</span></span>

<span data-ttu-id="cd376-199">[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)函數可讓應用程式或服務保留 TCP 或 UDP 埠的持續性區塊。</span><span class="sxs-lookup"><span data-stu-id="cd376-199">The [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function provides the ability for an application or service to reserve a persistent block of TCP or UDP ports.</span></span>
<span data-ttu-id="cd376-200">持續性埠保留會記錄在 Windows 中 TCP 或 UDP 模組的持續性存放區中。</span><span class="sxs-lookup"><span data-stu-id="cd376-200">Persistent port reservations are recorded in a persistent store for the TCP or UDP module in Windows.</span></span>
<span data-ttu-id="cd376-201">請注意，每次重新開機系統時，指定的持續埠保留的權杖可能會變更。</span><span class="sxs-lookup"><span data-stu-id="cd376-201">Note that the token for a given persistent port reservation may change each time the system is restarted.</span></span>

<span data-ttu-id="cd376-202">一旦取得持續性 TCP 或 UDP 埠保留，應用程式就可以藉由開啟 TCP 或 UDP 通訊端，然後呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 函式來指定 **SIO \_ 建立 \_ 埠 \_ 保留** 型 [**IOCTL 的**](/windows/desktop/api/winsock/nf-winsock-bind) 關聯並傳遞保留權杖，然後再發出對通訊端之系結函式的呼叫，藉此從埠保留要求埠指派。</span><span class="sxs-lookup"><span data-stu-id="cd376-202">Once a persistent TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="cd376-203">[**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md)的 IOCTL 可以用來要求 TCP 或 UDP 埠區塊的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="cd376-203">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="cd376-204">針對執行時間埠保留，埠集區會要求從其通訊端已授與保留的進程取用保留。</span><span class="sxs-lookup"><span data-stu-id="cd376-204">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="cd376-205">執行時間埠保留最後只會在呼叫 [**SIO_ACQUIRE_PORT_RESER加值稅ION**](sio-acquire-port-reservation.md) IOCTL 的通訊端存留期內。</span><span class="sxs-lookup"><span data-stu-id="cd376-205">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="cd376-206">相反地，使用 [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) 或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) 函式所建立的持續性埠保留，可供任何程式使用，以取得持續保留。</span><span class="sxs-lookup"><span data-stu-id="cd376-206">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="cd376-207">一旦取得執行時間 TCP 或 UDP 埠保留之後，應用程式就可以開啟 TCP 或 UDP 通訊端，然後呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 函式來指定 **SIO \_ 建立 \_ 埠 \_ 保留** 專案 IOCTL 的關聯，並在發出對套 [**接字的系**](/windows/desktop/api/winsock/nf-winsock-bind) 結函式的呼叫之前傳遞保留權杖，藉此要求埠保留中的埠指派。</span><span class="sxs-lookup"><span data-stu-id="cd376-207">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="cd376-208">如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 Null，則會將此函式中的通訊端視為非重迭的通訊端。</span><span class="sxs-lookup"><span data-stu-id="cd376-208">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="cd376-209">若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。</span><span class="sxs-lookup"><span data-stu-id="cd376-209">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="cd376-210">如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。</span><span class="sxs-lookup"><span data-stu-id="cd376-210">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="cd376-211">針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="cd376-211">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="cd376-212">任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。</span><span class="sxs-lookup"><span data-stu-id="cd376-212">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="cd376-213">如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="cd376-213">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="cd376-214">SIO 會在下列情況下， **\_ 將 \_ 埠 \_ 保留** 的 IOCTL 關聯于 **WSAEINTR** 或 **WSA_OPERATION_ABORTED** ：</span><span class="sxs-lookup"><span data-stu-id="cd376-214">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA_OPERATION_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="cd376-215">I/o 管理員會取消要求。</span><span class="sxs-lookup"><span data-stu-id="cd376-215">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="cd376-216">通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="cd376-216">The socket is closed.</span></span>

<span data-ttu-id="cd376-217">SIO 會將傳遞給 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)或 **WSPIoctl** 函式的 **\_ \_ 埠 \_ 保留** 專案 IOCTL 關聯到持續性埠保留，只可在使用者以系統管理員群組成員的身分登入時，于應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="cd376-217">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function for a persistent port reservation can only be used in an application when the user is logged on as a member of the Administrators group.</span></span>
<span data-ttu-id="cd376-218">如果當使用者不是系統管理員群組的成員時，在應用程式中使用 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL，函式呼叫將會失敗，並傳回 **WSAEACCES** 。</span><span class="sxs-lookup"><span data-stu-id="cd376-218">If **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used in an application when the user is not a member of the Administrators group, the function call will fail and **WSAEACCES** is returned.</span></span>
<span data-ttu-id="cd376-219">使用 **SIO \_ 關聯 \_ 埠 \_ 保留** 的 IOCTL 也可能會因為使用者帳戶控制 (Windows Vista 和更新版本上的 UAC) 而失敗。</span><span class="sxs-lookup"><span data-stu-id="cd376-219">The use of the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can also fail because of user account control (UAC) on Windows Vista and later.</span></span>
<span data-ttu-id="cd376-220">如果使用此 IOCTL 搭配持續性埠保留的應用程式是以內建系統管理員以外的 Administrators 群組成員身分登入，則此呼叫會失敗，除非應用程式已標示為 **並無 requestedexecutionlevel** 設定為 *requireAdministrator* 的資訊清單檔。</span><span class="sxs-lookup"><span data-stu-id="cd376-220">If an application that uses this IOCTL with a persistent port reservation is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to *requireAdministrator*.</span></span>
<span data-ttu-id="cd376-221">如果應用程式缺少此資訊清單檔，以內建系統管理員以外的 Administrators 群組成員身分登入的使用者，就必須在增強型 shell 中執行該應用程式，因為內建的系統管理員 (`RunAs administrator`) 讓此功能成功。</span><span class="sxs-lookup"><span data-stu-id="cd376-221">If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (`RunAs administrator`) for this function to succeed.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd376-222">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd376-222">See also</span></span>

[<span data-ttu-id="cd376-223">**綁定**</span><span class="sxs-lookup"><span data-stu-id="cd376-223">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="cd376-224">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-224">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="cd376-225">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-225">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="cd376-226">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-226">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="cd376-227">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-227">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="cd376-228">**INET_PORT_RESER加值稅ION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="cd376-228">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="cd376-229">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-229">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="cd376-230">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="cd376-230">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="cd376-231">**SIO_ACQUIRE_PORT_RESER加值稅ION**</span><span class="sxs-lookup"><span data-stu-id="cd376-231">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="cd376-232">**SIO_RELEASE_PORT_RESER加值稅ION**</span><span class="sxs-lookup"><span data-stu-id="cd376-232">**SIO_RELEASE_PORT_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="cd376-233">插座</span><span class="sxs-lookup"><span data-stu-id="cd376-233">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="cd376-234">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="cd376-234">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="cd376-235">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="cd376-235">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="cd376-236">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="cd376-236">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="cd376-237">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="cd376-237">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="cd376-238">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="cd376-238">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="cd376-239">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="cd376-239">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

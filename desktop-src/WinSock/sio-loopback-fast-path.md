---
description: 控制項程式碼會在回送介面上設定 TCP 通訊端，以提供較低的延遲和更快速的作業。
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999920"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="3b6e3-103">SIO_LOOPBACK_FAST_PATH 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="3b6e3-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="3b6e3-104">Description</span><span class="sxs-lookup"><span data-stu-id="3b6e3-104">Description</span></span>

<span data-ttu-id="3b6e3-105">**SIO \_ 回送 \_ 快速 \_ 路徑** 控制程式代碼會設定 TCP 通訊端，以在回送介面上進行較低的延遲和更快速的作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="3b6e3-106">**重要** **SIO \_ 回送 \_ 快速 \_ 路徑** 已被取代，不建議在您的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="3b6e3-107">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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

## <a name="parameters"></a><span data-ttu-id="3b6e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b6e3-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="3b6e3-109">s</span><span class="sxs-lookup"><span data-stu-id="3b6e3-109">s</span></span>

<span data-ttu-id="3b6e3-110">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="3b6e3-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="3b6e3-111">dwIoControlCode</span></span>

<span data-ttu-id="3b6e3-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-112">The control code for the operation.</span></span>
<span data-ttu-id="3b6e3-113">使用 **SIO \_ 回送 \_ 快速 \_ 路徑** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="3b6e3-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="3b6e3-114">lpvInBuffer</span></span>

<span data-ttu-id="3b6e3-115">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="3b6e3-116">此參數包含布林值的指標，指出是否應針對快速回送作業設定通訊端。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="3b6e3-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="3b6e3-117">cbInBuffer</span></span>

<span data-ttu-id="3b6e3-118">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="3b6e3-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="3b6e3-119">lpvOutBuffer</span></span>

<span data-ttu-id="3b6e3-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="3b6e3-121">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="3b6e3-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="3b6e3-122">cbOutBuffer</span></span>

<span data-ttu-id="3b6e3-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="3b6e3-124">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="3b6e3-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="3b6e3-125">lpcbBytesReturned</span></span>

<span data-ttu-id="3b6e3-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="3b6e3-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="3b6e3-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="3b6e3-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="3b6e3-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="3b6e3-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="3b6e3-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="3b6e3-132">lpvOverlapped</span></span>

<span data-ttu-id="3b6e3-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3b6e3-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="3b6e3-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="3b6e3-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3b6e3-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="3b6e3-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="3b6e3-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="3b6e3-139">lpCompletionRoutine</span></span>

<span data-ttu-id="3b6e3-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="3b6e3-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="3b6e3-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="3b6e3-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="3b6e3-142">lpThreadId</span></span>

<span data-ttu-id="3b6e3-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="3b6e3-144">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="3b6e3-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="3b6e3-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="3b6e3-146">lpErrno</span></span>

<span data-ttu-id="3b6e3-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-147">A pointer to the error code.</span></span>

<span data-ttu-id="3b6e3-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b6e3-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b6e3-149">Return value</span></span>

<span data-ttu-id="3b6e3-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="3b6e3-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="3b6e3-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="3b6e3-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3b6e3-153">Error code</span></span> | <span data-ttu-id="3b6e3-154">意義</span><span class="sxs-lookup"><span data-stu-id="3b6e3-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="3b6e3-155">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="3b6e3-156">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="3b6e3-157">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="3b6e3-158">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="3b6e3-159">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="3b6e3-160">如果因為通訊端關閉或 **SIO \_ FLUSH IOCTL** 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="3b6e3-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-161">**WSAEACCES**</span></span> | <span data-ttu-id="3b6e3-162">嘗試以存取權限禁止的方式存取通訊端。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="3b6e3-163">持續性埠保留的幾個條件下會傳回此錯誤，包括下列各項：使用者在本機電腦上缺少必要的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="3b6e3-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-164">**WSAEFAULT**</span></span> | <span data-ttu-id="3b6e3-165">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="3b6e3-166">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="3b6e3-167">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="3b6e3-168">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="3b6e3-169">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="3b6e3-170">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-170">**WSAEINTR**</span></span> | <span data-ttu-id="3b6e3-171">呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="3b6e3-172">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="3b6e3-173">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-173">**WSAEINVAL**</span></span> | <span data-ttu-id="3b6e3-174">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-174">An invalid argument was supplied.</span></span> <span data-ttu-id="3b6e3-175">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="3b6e3-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="3b6e3-177">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="3b6e3-178">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="3b6e3-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="3b6e3-180">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="3b6e3-181">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="3b6e3-182">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="3b6e3-183">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="3b6e3-184">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="3b6e3-185">如果傳輸提供者不支援 **SIO \_ 回送 \_ 快速 \_ 路徑** IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="3b6e3-186">備註</span><span class="sxs-lookup"><span data-stu-id="3b6e3-186">Remarks</span></span>

<span data-ttu-id="3b6e3-187">應用程式可以使用 **SIO \_ 回送 \_ 快速 \_ 路徑** IOCTL 來降低延遲，並改善 TCP 通訊端上的回送作業效能。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="3b6e3-188">此 IOCTL 要求 TCP/IP 堆疊針對此通訊端上的回送作業使用特殊的快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="3b6e3-189">**SIO \_ 回送 \_ 快速 \_ 路徑** IOCTL 只能用於 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="3b6e3-190">這個 IOCTL 必須用於回送會話的兩端。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="3b6e3-191">您可以使用 IPv4 或 IPv6 回送介面，來支援 TCP 回送快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="3b6e3-192">計畫起始連接要求的通訊端必須先套用此 IOCTL，然後再進行連線要求。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="3b6e3-193">因此 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) 函式用來起始連接的通訊端必須套用此 IOCTL，才能使用回送作業的快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="3b6e3-194">接聽連接要求的通訊端必須在接受連接之前套用此 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="3b6e3-195">因此，接聽函式所使用的通訊端必須套用此 IOCTL，因此任何接受的通訊端都將使用快速路徑進行回送。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="3b6e3-196">接聽函式所傳回並傳遞至 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) 函式的任何通訊端，都會標示為針對回送作業使用特殊的快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="3b6e3-197">當應用程式使用快速路徑在回送介面上建立連接時，連接存留期的所有封包都必須使用快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="3b6e3-198">將 **SIO \_ 回送的 \_ 快速 \_ 路徑** 套用至將連接至非回送路徑的通訊端，將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="3b6e3-199">此 TCP 回送優化會導致封包流經傳輸層 (TL) ，而不是透過網路層進行傳統的回送。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="3b6e3-200">此優化可改善回送封包的延遲。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="3b6e3-201">一旦應用程式將連接層級設定為使用回送快速路徑之後，所有封包都會遵循回送路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="3b6e3-202">針對回送通訊，不需要擁塞和封包捨棄。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="3b6e3-203">TCP 中的擁塞控制和可靠傳遞的概念不是必要的。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="3b6e3-204">但是，流程式控制制的情況並不成立。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="3b6e3-205">如果沒有流量控制，傳送者可能會造成接收緩衝區負荷，並導致錯誤的 TCP 回送行為。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="3b6e3-206">TCP 優化回送路徑中的流程式控制制是藉由在佇列中放置傳送要求來維護的。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="3b6e3-207">當接收緩衝區已滿時，TCP/IP 堆疊保證傳送將不會完成，直到佇列維修維護流量控制為止。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="3b6e3-208">在 Windows 篩選平台 (WFP) 注標中，連接資料的 TCP 快速路徑回送連線，必須採用非優化的緩慢路徑進行回送。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="3b6e3-209">因此，WFP 篩選器會防止使用這個新的回送快速路徑。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="3b6e3-210">啟用 WFP 篩選器時，系統會使用慢速路徑，即使已設定 **SIO \_ 回送 \_ 快速 \_ 路徑** IOCTL 也是如此。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="3b6e3-211">這可確保使用者模式應用程式具有完整的 WFP 安全性功能。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="3b6e3-212">預設會停用 **SIO \_ 回送 \_ 快速 \_ 路徑** 。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="3b6e3-213">當使用 **SIO \_ 回送 \_ 快速 \_ 路徑** IOCTL 來啟用通訊端上的回送快速路徑時，僅支援 tcp/ip 通訊端選項的子集。</span><span class="sxs-lookup"><span data-stu-id="3b6e3-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="3b6e3-214">支援的選項清單包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="3b6e3-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="3b6e3-215">**IP \_ TTL**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-215">**IP\_TTL**</span></span>
* <span data-ttu-id="3b6e3-216">**IP \_ 單播（ \_ 如果**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3b6e3-217">**IPV6 \_ 單播 \_ 躍點**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="3b6e3-218">**IPV6 \_ 單播 \_ IF**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3b6e3-219">**IPV6 \_ V6ONLY**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="3b6e3-220">**因此 \_ 條件 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="3b6e3-221">**\_EXCLUSIVEADDRUSE**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="3b6e3-222">**因此， \_ 埠擴充 \_ 性**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="3b6e3-223">**\_RCVBUF**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="3b6e3-224">**\_REUSEADDR**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="3b6e3-225">**TCP \_ BSDURGENT**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="3b6e3-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b6e3-226">See also</span></span>

[<span data-ttu-id="3b6e3-227">**IPPROTO_IP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="3b6e3-228">**IPPROTO_IPV6 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="3b6e3-229">**IPPROTO_TCP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="3b6e3-230">**插座**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="3b6e3-231">**SOL_SOCKET 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="3b6e3-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="3b6e3-233">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="3b6e3-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="3b6e3-235">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="3b6e3-236">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="3b6e3-237">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="3b6e3-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

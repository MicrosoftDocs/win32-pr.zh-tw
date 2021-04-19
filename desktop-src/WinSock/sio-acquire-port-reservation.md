---
description: 控制項程式碼會取得 TCP 或 UDP 埠區塊的執行時間保留。
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: SIO_ACQUIRE_PORT_RESER加值稅ION 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987477"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="df037-103">SIO_ACQUIRE_PORT_RESER加值稅ION 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="df037-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="df037-104">Description</span><span class="sxs-lookup"><span data-stu-id="df037-104">Description</span></span>

<span data-ttu-id="df037-105">**SIO \_ 取得 \_ 埠 \_ 保留** 控制項程式碼會取得 TCP 或 UDP 埠區塊的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="df037-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="df037-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="df037-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="df037-107">參數</span><span class="sxs-lookup"><span data-stu-id="df037-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="df037-108">s</span><span class="sxs-lookup"><span data-stu-id="df037-108">s</span></span>

<span data-ttu-id="df037-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="df037-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="df037-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="df037-110">dwIoControlCode</span></span>

<span data-ttu-id="df037-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="df037-111">The control code for the operation.</span></span>
<span data-ttu-id="df037-112">使用 **SIO \_ 取得 \_ 埠 \_ 保留**  區進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="df037-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="df037-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="df037-113">lpvInBuffer</span></span>

<span data-ttu-id="df037-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="df037-115">此參數包含 [**INET \_ 埠 \_ 範圍**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) 結構的指標，該結構可指定要保留的起始點和埠數目。</span><span class="sxs-lookup"><span data-stu-id="df037-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="df037-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="df037-116">cbInBuffer</span></span>

<span data-ttu-id="df037-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="df037-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="df037-118">此參數應為 [**INET \_ 埠 \_ 範圍**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="df037-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="df037-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="df037-119">lpvOutBuffer</span></span>

<span data-ttu-id="df037-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="df037-121">成功輸出時，此參數會包含 [**INET \_ 埠 \_ 保留 \_ 實例**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="df037-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="df037-122">cbOutBuffer</span></span>

<span data-ttu-id="df037-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="df037-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="df037-124">此參數必須至少為 [**INET \_ 埠 \_ 保留 \_ 實例**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="df037-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="df037-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="df037-125">lpcbBytesReturned</span></span>

<span data-ttu-id="df037-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="df037-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="df037-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="df037-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="df037-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="df037-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="df037-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="df037-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="df037-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="df037-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="df037-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="df037-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="df037-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="df037-132">lpvOverlapped</span></span>

<span data-ttu-id="df037-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="df037-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="df037-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="df037-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="df037-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="df037-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="df037-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="df037-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="df037-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="df037-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="df037-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="df037-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="df037-139">lpCompletionRoutine</span></span>

<span data-ttu-id="df037-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="df037-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="df037-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="df037-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="df037-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="df037-142">lpThreadId</span></span>

<span data-ttu-id="df037-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 **WPUQueueApc** 呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="df037-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="df037-144">在 **WPUQueueApc** 函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="df037-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="df037-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="df037-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="df037-146">lpErrno</span></span>

<span data-ttu-id="df037-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="df037-147">A pointer to the error code.</span></span>

<span data-ttu-id="df037-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="df037-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="df037-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="df037-149">Return value</span></span>

<span data-ttu-id="df037-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="df037-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="df037-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="df037-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="df037-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="df037-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="df037-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="df037-153">Error code</span></span> | <span data-ttu-id="df037-154">意義</span><span class="sxs-lookup"><span data-stu-id="df037-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="df037-155">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="df037-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="df037-156">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="df037-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="df037-157">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="df037-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="df037-158">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="df037-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="df037-159">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="df037-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="df037-160">如果因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="df037-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="df037-161">**WSAEFAULT**</span></span> | <span data-ttu-id="df037-162">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="df037-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="df037-163">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="df037-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="df037-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="df037-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="df037-165">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="df037-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="df037-166">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="df037-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="df037-167">**WSAEINTR**</span></span> | <span data-ttu-id="df037-168">呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="df037-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="df037-169">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="df037-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="df037-170">**WSAEINVAL**</span></span> | <span data-ttu-id="df037-171">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="df037-171">An invalid argument was supplied.</span></span> <span data-ttu-id="df037-172">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="df037-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="df037-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="df037-174">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="df037-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="df037-175">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="df037-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="df037-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="df037-177">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="df037-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="df037-178">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="df037-179">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="df037-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="df037-180">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="df037-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="df037-181">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="df037-182">如果傳輸提供者不支援 **SIO \_ 取得 \_ 埠 \_ 保留** 的 IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="df037-183">當嘗試在 UDP 或 TCP 以外的通訊端上進行使用 **SIO \_ 取得 \_ 埠 \_ 保留** IOCTL 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="df037-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="df037-184">備註</span><span class="sxs-lookup"><span data-stu-id="df037-184">Remarks</span></span>

<span data-ttu-id="df037-185">在 Windows Vista 和更新版本的作業系統上，支援 **SIO \_ 取得 \_ 埠 \_ 保留**  的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="df037-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="df037-186">需要保留埠的應用程式和服務可以分為兩個類別。</span><span class="sxs-lookup"><span data-stu-id="df037-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="df037-187">第一個類別包含元件，而這些元件需要特定的埠做為其作業的一部分。</span><span class="sxs-lookup"><span data-stu-id="df037-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="df037-188">這類元件通常會偏好在安裝期間指定其必要的埠 (在應用程式資訊清單中，例如) 。</span><span class="sxs-lookup"><span data-stu-id="df037-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="df037-189">第二個類別包含在執行時間需要任何可用埠或埠區塊的元件。</span><span class="sxs-lookup"><span data-stu-id="df037-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="df037-190">這兩個類別對應于特定和萬用字元埠保留要求。</span><span class="sxs-lookup"><span data-stu-id="df037-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="df037-191">特定的保留要求可能是持續性或執行時間，而萬用字元埠保留要求只在執行時間支援。</span><span class="sxs-lookup"><span data-stu-id="df037-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="df037-192">**SIO \_ 取得 \_ 埠 \_ 保留** IOCTL 可用來要求 TCP 或 UDP 埠區塊的執行時間保留。</span><span class="sxs-lookup"><span data-stu-id="df037-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="df037-193">針對執行時間埠保留，埠集區會要求從其通訊端已授與保留的進程取用保留。</span><span class="sxs-lookup"><span data-stu-id="df037-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="df037-194">執行時間埠保留最後只會在呼叫 **SIO \_ 取得 \_ 埠 \_ 保留**  IOCTL 的通訊端存留期內。</span><span class="sxs-lookup"><span data-stu-id="df037-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="df037-195">相反地，使用 [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) 或 [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) 函式所建立的持續性埠保留，可供任何程式使用，以取得持續保留。</span><span class="sxs-lookup"><span data-stu-id="df037-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="df037-196">一旦取得執行時間 TCP 或 UDP 埠保留之後，應用程式就可以開啟 TCP 或 UDP 通訊端，然後呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 函式來指定 [**SIO \_ 建立 \_ 埠 \_ 保留**](sio-associate-port-reservation.md) 專案 IOCTL 的關聯，並在發出對通訊端的系結函式的呼叫之前傳遞保留權杖，藉此要求埠保留中的埠指派。</span><span class="sxs-lookup"><span data-stu-id="df037-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="df037-197">如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 **Null**，則會將此函式中的通訊端視為非重迭的通訊端。</span><span class="sxs-lookup"><span data-stu-id="df037-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="df037-198">若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。</span><span class="sxs-lookup"><span data-stu-id="df037-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="df037-199">如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。</span><span class="sxs-lookup"><span data-stu-id="df037-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="df037-200">針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="df037-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="df037-201">任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。</span><span class="sxs-lookup"><span data-stu-id="df037-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="df037-202">如果應用程式無法容忍 WSAIoctl 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="df037-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="df037-203">**SIO \_ 取得 \_ 埠 \_ 保留** 的 IOCTL 可能會在下列情況下，因為 **WSAEINTR** 或 **WSA 作業 \_ \_ 中止** 而失敗：</span><span class="sxs-lookup"><span data-stu-id="df037-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="df037-204">I/o 管理員會取消要求。</span><span class="sxs-lookup"><span data-stu-id="df037-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="df037-205">通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="df037-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="df037-206">範例</span><span class="sxs-lookup"><span data-stu-id="df037-206">Examples</span></span>

<span data-ttu-id="df037-207">下列範例會取得執行時間埠保留區，然後建立通訊端，並從通訊端的執行時間埠保留配置埠，然後關閉通訊端，然後釋放執行時間埠保留。</span><span class="sxs-lookup"><span data-stu-id="df037-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="df037-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df037-208">See also</span></span>

[<span data-ttu-id="df037-209">**接受**</span><span class="sxs-lookup"><span data-stu-id="df037-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="df037-210">**綁定**</span><span class="sxs-lookup"><span data-stu-id="df037-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="df037-211">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="df037-212">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="df037-213">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="df037-214">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="df037-215">**INET \_ 埠 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="df037-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="df037-216">**INET \_ 埠 \_ 保留 \_ 實例**</span><span class="sxs-lookup"><span data-stu-id="df037-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="df037-217">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="df037-218">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="df037-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="df037-219">**SIO \_ 建立 \_ 埠 \_ 保留區的關聯**</span><span class="sxs-lookup"><span data-stu-id="df037-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="df037-220">**SIO \_ 發行 \_ 埠 \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="df037-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="df037-221">**插座**</span><span class="sxs-lookup"><span data-stu-id="df037-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="df037-222">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="df037-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="df037-223">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="df037-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="df037-224">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="df037-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="df037-225">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="df037-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="df037-226">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="df037-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="df037-227">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="df037-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

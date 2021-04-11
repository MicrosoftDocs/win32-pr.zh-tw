---
description: 當連接的理想傳送待處理專案值變更時，控制項程式碼會通知應用程式。
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692212"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="a3632-103">SIO_IDEAL_SEND_BACKLOG_CHANGE 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="a3632-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a3632-104">Description</span><span class="sxs-lookup"><span data-stu-id="a3632-104">Description</span></span>

<span data-ttu-id="a3632-105">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更控制程式碼會在理想的傳送待處理專案 (ISB) 值變更時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="a3632-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="a3632-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="a3632-107">參數</span><span class="sxs-lookup"><span data-stu-id="a3632-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a3632-108">s</span><span class="sxs-lookup"><span data-stu-id="a3632-108">s</span></span>

<span data-ttu-id="a3632-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="a3632-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a3632-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a3632-110">dwIoControlCode</span></span>

<span data-ttu-id="a3632-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="a3632-111">The control code for the operation.</span></span>
<span data-ttu-id="a3632-112">針對此作業，請使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更。</span><span class="sxs-lookup"><span data-stu-id="a3632-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a3632-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a3632-113">lpvInBuffer</span></span>

<span data-ttu-id="a3632-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a3632-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="a3632-115">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="a3632-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a3632-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a3632-116">cbInBuffer</span></span>

<span data-ttu-id="a3632-117">輸入緩衝區的大小（以位元組為單位）。此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="a3632-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a3632-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a3632-118">lpvOutBuffer</span></span>

<span data-ttu-id="a3632-119">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a3632-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="a3632-120">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="a3632-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a3632-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a3632-121">cbOutBuffer</span></span>

<span data-ttu-id="a3632-122">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a3632-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a3632-123">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="a3632-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a3632-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a3632-124">lpcbBytesReturned</span></span>

<span data-ttu-id="a3632-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a3632-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="a3632-126">這項作業的傳回參數指向 **DWORD** 值零，因為沒有任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a3632-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a3632-127">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a3632-127">lpvOverlapped</span></span>

<span data-ttu-id="a3632-128">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a3632-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a3632-129">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="a3632-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a3632-130">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="a3632-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a3632-131">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="a3632-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a3632-132">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="a3632-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a3632-133">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="a3632-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a3632-134">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a3632-134">lpCompletionRoutine</span></span>

<span data-ttu-id="a3632-135">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a3632-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a3632-136">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="a3632-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a3632-137">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a3632-137">lpThreadId</span></span>

<span data-ttu-id="a3632-138">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="a3632-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a3632-139">在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a3632-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a3632-140">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a3632-141">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a3632-141">lpErrno</span></span>

<span data-ttu-id="a3632-142">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="a3632-142">A pointer to the error code.</span></span>

<span data-ttu-id="a3632-143">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3632-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3632-144">Return value</span></span>

<span data-ttu-id="a3632-145">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a3632-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a3632-146">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="a3632-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a3632-147">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="a3632-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a3632-148">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a3632-148">Error code</span></span> | <span data-ttu-id="a3632-149">意義</span><span class="sxs-lookup"><span data-stu-id="a3632-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="a3632-150">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="a3632-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a3632-151">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="a3632-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a3632-152">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="a3632-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a3632-153">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="a3632-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="a3632-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a3632-154">**WSAEFAULT**</span></span> | <span data-ttu-id="a3632-155">*LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="a3632-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a3632-156">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a3632-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a3632-157">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a3632-158">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a3632-158">**WSAEINTR**</span></span> | <span data-ttu-id="a3632-159">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="a3632-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a3632-160">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a3632-160">**WSAEINVAL**</span></span> | <span data-ttu-id="a3632-161">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="a3632-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="a3632-162">如果 *cbOutBuffer* 參數不是零，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3632-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="a3632-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a3632-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="a3632-164">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="a3632-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="a3632-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="a3632-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="a3632-166">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="a3632-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="a3632-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="a3632-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="a3632-168">*通訊端未連線*。</span><span class="sxs-lookup"><span data-stu-id="a3632-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="a3632-169">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a3632-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a3632-170">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="a3632-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a3632-171">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a3632-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a3632-172">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="a3632-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="a3632-173">如果傳輸提供者不支援 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3632-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a3632-174">當嘗試在資料包通訊端上進行使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3632-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a3632-175">備註</span><span class="sxs-lookup"><span data-stu-id="a3632-175">Remarks</span></span>

<span data-ttu-id="a3632-176">Windows Server 2008、Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統都支援 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="a3632-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="a3632-177">使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。</span><span class="sxs-lookup"><span data-stu-id="a3632-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="a3632-178">若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。</span><span class="sxs-lookup"><span data-stu-id="a3632-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="a3632-179">ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。</span><span class="sxs-lookup"><span data-stu-id="a3632-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="a3632-180">您可以從 Windows Server 2008、Windows Vista SP1 和更新版本的作業系統中的 TCP 通訊協定，取得每個連接的 ISB 值。</span><span class="sxs-lookup"><span data-stu-id="a3632-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="a3632-181">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 可供應用程式使用，以在 ISB 值針對連接動態變更時取得通知。</span><span class="sxs-lookup"><span data-stu-id="a3632-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="a3632-182">在 Windows Server 2008、Windows Vista （含 SP1）及更新版本的作業系統上， **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案（backlog）變更和 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-query.md) 處理專案（backlog）查詢 IOCTLs 可在已線上狀態的資料流程導向通訊端上受到支援。</span><span class="sxs-lookup"><span data-stu-id="a3632-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="a3632-183">TCP 連接的 ISB 值範圍理論上可能會因0到 16 mb 而異。</span><span class="sxs-lookup"><span data-stu-id="a3632-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="a3632-184">請參閱 [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-query.md) 處理專案查詢 IOCTL 參考頁面，以取得 ISB 機制的一般使用方式，以透過高頻寬延遲的產品連線達到更佳的輸送量。</span><span class="sxs-lookup"><span data-stu-id="a3632-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="a3632-185">只有在已線上狀態的資料流程通訊端上，才允許 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="a3632-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="a3632-186">否則， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式將會失敗，並出現 **WSAENOTCONN**。</span><span class="sxs-lookup"><span data-stu-id="a3632-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="a3632-187">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 在基礎連接上發生 ISB 變更之前，不會使用輸入或輸出緩衝區和 pends 或區塊。</span><span class="sxs-lookup"><span data-stu-id="a3632-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="a3632-188">當這個 IOCTL 完成時，Winsock 應用程式可以使用 [**SIO 理想的傳送待處理專案（ \_ \_ \_ BACKLOG） \_ 查詢**](sio-ideal-send-backlog-query.md) IOCTL 來取得連接上的新 ISB 值。</span><span class="sxs-lookup"><span data-stu-id="a3632-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="a3632-189">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 不支援非封鎖模式。</span><span class="sxs-lookup"><span data-stu-id="a3632-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="a3632-190">允許應用程式在非封鎖通訊端上發出這個 IOCTL，但在 ISB 值變更之前，只會封鎖或暫止 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="a3632-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="a3632-191">如果 *lpOverlapped* 和 *lpCompletionRoutine* 參數都是 Null，則會將此函式中的通訊端視為非重迭的通訊端。</span><span class="sxs-lookup"><span data-stu-id="a3632-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="a3632-192">若為非重迭的通訊端，則會忽略 *lpOverlapped* 和 *lpCompletionRoutine* 參數，不同之處在于如果通訊端 *s* 處於封鎖模式，函數可以封鎖。</span><span class="sxs-lookup"><span data-stu-id="a3632-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="a3632-193">如果通訊端 *s* 處於非封鎖模式中，此函式仍會封鎖，因為這個特定的 IOCTL 不支援非封鎖模式。</span><span class="sxs-lookup"><span data-stu-id="a3632-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="a3632-194">針對重迭的通訊端，將會起始無法立即完成的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="a3632-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="a3632-195">任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。</span><span class="sxs-lookup"><span data-stu-id="a3632-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="a3632-196">如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="a3632-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="a3632-197">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 會提供通知，在 ISB 值變更之前，預期會封鎖或暫止。</span><span class="sxs-lookup"><span data-stu-id="a3632-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="a3632-198">因此，通常會以非同步方式呼叫 *lpOverlapped* 參數，並將其設定為有效的 WSAOVERLAPPED 結構。</span><span class="sxs-lookup"><span data-stu-id="a3632-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="a3632-199">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL 可能會失敗，並在下列情況下 **\_ \_ 中止** **WSAEINTR** 或 WSA 作業：</span><span class="sxs-lookup"><span data-stu-id="a3632-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="a3632-200">TCP 連接會正常地在傳送方向中斷連線。</span><span class="sxs-lookup"><span data-stu-id="a3632-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="a3632-201">這可能是因為呼叫 shutdown 函式，並將參數設定為 **SD \_ SEND**、呼叫 **DisconnectEx** 函式，或是呼叫 **TransmitFile** 或 **TransmitPackets** 函式（ *dwFlags* 參數設定為 **tf \_ DISCONNECT** 或 **tf \_ 重複使用**）的結果。</span><span class="sxs-lookup"><span data-stu-id="a3632-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="a3632-202">TCP 連接已重設或中止。</span><span class="sxs-lookup"><span data-stu-id="a3632-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="a3632-203">當已經有暫止的通知要求時，應用程式會發出 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="a3632-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="a3632-204">一次只允許 1 1 暫止的 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案變更要求。</span><span class="sxs-lookup"><span data-stu-id="a3632-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="a3632-205">I/o 管理員會取消要求。</span><span class="sxs-lookup"><span data-stu-id="a3632-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="a3632-206">通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="a3632-206">The socket is closed.</span></span>

<span data-ttu-id="a3632-207">這些 IOCTLs 的兩個內嵌包裝函式是在 *Ws2tcpip .h* 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="a3632-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="a3632-208">建議使用這些內嵌函式，而不是使用 **SIO 理想的 \_ \_ 傳送 \_ 待 \_** 處理專案變更和 [**SIO 理想的傳送待處理專案 \_ \_ \_ （backlog） \_ 查詢**](sio-ideal-send-backlog-query.md) IOCTLs。</span><span class="sxs-lookup"><span data-stu-id="a3632-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="a3632-209">**SIO \_ 理想 \_ 傳送 \_ 待辦專案 \_ 變更** IOCTL 的內嵌包裝函式是 **idealsendbacklognotify** 函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="a3632-210">[**SIO \_ 理想 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢**](sio-ideal-send-backlog-query.md)IOCTL 的內嵌包裝函式是 **idealsendbacklogquery** 函數。</span><span class="sxs-lookup"><span data-stu-id="a3632-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3632-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3632-211">See also</span></span>

[<span data-ttu-id="a3632-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="a3632-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="a3632-213">**插座**</span><span class="sxs-lookup"><span data-stu-id="a3632-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a3632-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a3632-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="a3632-215">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a3632-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a3632-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a3632-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a3632-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a3632-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a3632-218">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a3632-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a3632-219">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a3632-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

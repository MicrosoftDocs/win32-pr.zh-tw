---
description: 控制項程式碼會啟用或停用 TCP keep-alive 選項的每一連接設定，以指定 TCP keep-alive timeout 和 interval。
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114904"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="c2ac9-103">SIO_KEEPALIVE_VALS 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="c2ac9-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="c2ac9-104">Description</span><span class="sxs-lookup"><span data-stu-id="c2ac9-104">Description</span></span>

<span data-ttu-id="c2ac9-105">**SIO \_ KEEPALIVE \_ VALS** control 程式碼會啟用或停用 tcp keep-alive 選項的每一連接設定，以指定 tcp 保持連線的超時和間隔。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="c2ac9-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="c2ac9-107">參數</span><span class="sxs-lookup"><span data-stu-id="c2ac9-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="c2ac9-108">s</span><span class="sxs-lookup"><span data-stu-id="c2ac9-108">s</span></span>

<span data-ttu-id="c2ac9-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="c2ac9-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="c2ac9-110">dwIoControlCode</span></span>

<span data-ttu-id="c2ac9-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-111">The control code for the operation.</span></span>
<span data-ttu-id="c2ac9-112">使用 **SIO \_ KEEPALIVE \_ VALS** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="c2ac9-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="c2ac9-113">lpvInBuffer</span></span>

<span data-ttu-id="c2ac9-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="c2ac9-115">此參數應指向 **tcp \_ keepalive** 結構。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="c2ac9-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="c2ac9-116">cbInBuffer</span></span>

<span data-ttu-id="c2ac9-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="c2ac9-118">此參數應等於或大於 *lpvInBuffer* 參數所指向之 **tcp \_ keepalive** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="c2ac9-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="c2ac9-119">lpvOutBuffer</span></span>

<span data-ttu-id="c2ac9-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="c2ac9-121">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="c2ac9-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="c2ac9-122">cbOutBuffer</span></span>

<span data-ttu-id="c2ac9-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="c2ac9-124">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="c2ac9-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="c2ac9-125">lpcbBytesReturned</span></span>

<span data-ttu-id="c2ac9-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="c2ac9-127">這項作業的傳回參數指向 **DWORD** 值零，因為沒有任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="c2ac9-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="c2ac9-128">lpvOverlapped</span></span>

<span data-ttu-id="c2ac9-129">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="c2ac9-130">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="c2ac9-131">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="c2ac9-132">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="c2ac9-133">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="c2ac9-134">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="c2ac9-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="c2ac9-135">lpCompletionRoutine</span></span>

<span data-ttu-id="c2ac9-136">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="c2ac9-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="c2ac9-137">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="c2ac9-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="c2ac9-138">lpThreadId</span></span>

<span data-ttu-id="c2ac9-139">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="c2ac9-140">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="c2ac9-141">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="c2ac9-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="c2ac9-142">lpErrno</span></span>

<span data-ttu-id="c2ac9-143">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-143">A pointer to the error code.</span></span>

<span data-ttu-id="c2ac9-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2ac9-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2ac9-145">Return value</span></span>

<span data-ttu-id="c2ac9-146">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="c2ac9-147">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="c2ac9-148">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="c2ac9-149">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c2ac9-149">Error code</span></span> | <span data-ttu-id="c2ac9-150">意義</span><span class="sxs-lookup"><span data-stu-id="c2ac9-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="c2ac9-151">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="c2ac9-152">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="c2ac9-153">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="c2ac9-154">因為通訊端關閉或 **SIO_FLUSH IOCTL** 命令的執行，所以重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="c2ac9-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-155">**WSAEFAULT**</span></span> | <span data-ttu-id="c2ac9-156">*LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="c2ac9-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="c2ac9-158">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="c2ac9-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-159">**WSAEINTR**</span></span> | <span data-ttu-id="c2ac9-160">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="c2ac9-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-161">**WSAEINVAL**</span></span> | <span data-ttu-id="c2ac9-162">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="c2ac9-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="c2ac9-164">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="c2ac9-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="c2ac9-166">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="c2ac9-167">資料包通訊端會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="c2ac9-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="c2ac9-169">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="c2ac9-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="c2ac9-171">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="c2ac9-172">如果傳輸提供者不支援 **SIO \_ KEEPALIVE \_ VALS** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="c2ac9-173">備註</span><span class="sxs-lookup"><span data-stu-id="c2ac9-173">Remarks</span></span>

<span data-ttu-id="c2ac9-174">在 Windows 2000 和更新版本的作業系統上，支援 **SIO \_ KEEPALIVE \_ VALS** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="c2ac9-175">**SIO \_ KEEPALIVE \_ VALS** control 程式碼會啟用或停用 tcp keep-alive 選項的每個連線設定，以指定 tcp keep-alive 封包所使用的 tcp keep-alive timeout 和間隔。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="c2ac9-176">如需保持連線選項的詳細資訊，請參閱4.2.3.6 中的「網際網路主機需求」一節：在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1122 中所指定的通訊層。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="c2ac9-177"> (此資源可能僅提供英文版。 ) </span><span class="sxs-lookup"><span data-stu-id="c2ac9-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="c2ac9-178">*LpvInBuffer* 參數應指向 *Mstcpip .h* 標頭檔中定義的 **tcp \_ keepalive** 結構。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="c2ac9-179">此結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="c2ac9-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="c2ac9-180">**Onoff** 成員中指定的值會決定是否啟用或停用 TCP 保持連線。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="c2ac9-181">如果 **onoff** 成員設定為非零值，則會啟用 TCP 保持運作，並使用結構中的其他成員。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="c2ac9-182">**Keepalivetime** 成員會指定在第一個 keep-alive 封包傳送之前沒有任何活動的超時時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="c2ac9-183">**Keepaliveinterval** 成員會指定在未收到任何通知時，連續的 keep-alive 封包傳送的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="c2ac9-184">[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)選項（這是其中一個 [**SOL_SOCKET 通訊端選項**](/windows/desktop/winsock/sol-socket-socket-options)）也可用來啟用或停用連接上的 TCP keep-alive，以及查詢此選項的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="c2ac9-185">若要查詢通訊端上是否啟用 TCP keep-alive，可以使用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) 選項來呼叫 getsockopt 函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="c2ac9-186">若要啟用或停用 TCP keep-alive，可以使用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)選項來呼叫 **setsockopt** 函數。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="c2ac9-187">如果已啟用 [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)的 tcp keep-alive，則預設 TCP 設定會用於 keep-alive timeout 和 interval，除非使用 **SIO \_ KEEPALIVE \_ VALS** 變更這些值。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="c2ac9-188">Keep-alive timeout 的預設全系統值可透過 [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="c2ac9-189">如果未設定索引鍵，則預設的 keep-alive timeout 為2小時。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="c2ac9-190">Keep-alive 間隔的預設全系統值可透過 [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="c2ac9-191">如果未設定索引鍵，則預設的 keep-alive 間隔為1秒。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="c2ac9-192">在 Windows Vista 和更新版本上， (資料重新傳輸) 的 keep-alive 探查數目設定為10，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="c2ac9-193">在 Windows Server 2003、Windows XP 及 Windows 2000 上，保持運作探查數目的預設設定為5。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="c2ac9-194">Keep-alive 探查的數目可透過 **TcpMaxDataRetransmissions** 和 [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) 登錄設定來控制。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="c2ac9-195">Keep-alive 探查的數目會設定為兩個登錄機碼值的較大值。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="c2ac9-196">如果這個數位為0，則不會傳送 keep-alive 探查。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="c2ac9-197">如果此數位大於255，則會調整為255。</span><span class="sxs-lookup"><span data-stu-id="c2ac9-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2ac9-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2ac9-198">See also</span></span>

<span data-ttu-id="c2ac9-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c2ac9-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="c2ac9-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c2ac9-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="c2ac9-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c2ac9-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="c2ac9-202">插座</span><span class="sxs-lookup"><span data-stu-id="c2ac9-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="c2ac9-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="c2ac9-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="c2ac9-205">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="c2ac9-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="c2ac9-207">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="c2ac9-208">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="c2ac9-209">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="c2ac9-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

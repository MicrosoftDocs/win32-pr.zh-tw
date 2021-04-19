---
description: 控制項程式碼會抓取基礎連接的理想傳送待辦專案值。
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971516"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="bcd50-103">SIO_IDEAL_SEND_BACKLOG_QUERY 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="bcd50-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="bcd50-104">Description</span><span class="sxs-lookup"><span data-stu-id="bcd50-104">Description</span></span>

<span data-ttu-id="bcd50-105">**SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案查詢控制項程式碼會針對基礎連接，取得理想的傳送待處理專案 (ISB) 值。</span><span class="sxs-lookup"><span data-stu-id="bcd50-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="bcd50-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="bcd50-107">參數</span><span class="sxs-lookup"><span data-stu-id="bcd50-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="bcd50-108">s</span><span class="sxs-lookup"><span data-stu-id="bcd50-108">s</span></span>

<span data-ttu-id="bcd50-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="bcd50-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="bcd50-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="bcd50-110">dwIoControlCode</span></span>

<span data-ttu-id="bcd50-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="bcd50-111">The control code for the operation.</span></span>
<span data-ttu-id="bcd50-112">使用 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案查詢進行此作業。</span><span class="sxs-lookup"><span data-stu-id="bcd50-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="bcd50-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="bcd50-113">lpvInBuffer</span></span>

<span data-ttu-id="bcd50-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd50-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="bcd50-115">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="bcd50-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="bcd50-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="bcd50-116">cbInBuffer</span></span>

<span data-ttu-id="bcd50-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bcd50-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="bcd50-118">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="bcd50-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="bcd50-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="bcd50-119">lpvOutBuffer</span></span>

<span data-ttu-id="bcd50-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd50-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="bcd50-121">如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數應指向 **ULONG** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="bcd50-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="bcd50-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="bcd50-122">cbOutBuffer</span></span>

<span data-ttu-id="bcd50-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bcd50-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="bcd50-124">此參數必須至少為 **ULONG** 資料類型的大小。</span><span class="sxs-lookup"><span data-stu-id="bcd50-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="bcd50-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="bcd50-125">lpcbBytesReturned</span></span>

<span data-ttu-id="bcd50-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bcd50-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="bcd50-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="bcd50-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="bcd50-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="bcd50-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="bcd50-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="bcd50-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="bcd50-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="bcd50-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="bcd50-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="bcd50-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="bcd50-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="bcd50-132">lpvOverlapped</span></span>

<span data-ttu-id="bcd50-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd50-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bcd50-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="bcd50-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="bcd50-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="bcd50-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="bcd50-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bcd50-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="bcd50-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="bcd50-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="bcd50-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="bcd50-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="bcd50-139">lpCompletionRoutine</span></span>

<span data-ttu-id="bcd50-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="bcd50-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="bcd50-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="bcd50-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="bcd50-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="bcd50-142">lpThreadId</span></span>

<span data-ttu-id="bcd50-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="bcd50-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="bcd50-144">在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd50-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="bcd50-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="bcd50-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="bcd50-146">lpErrno</span></span>

<span data-ttu-id="bcd50-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd50-147">A pointer to the error code.</span></span>

<span data-ttu-id="bcd50-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcd50-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcd50-149">Return value</span></span>

<span data-ttu-id="bcd50-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bcd50-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="bcd50-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="bcd50-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="bcd50-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="bcd50-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="bcd50-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bcd50-153">Error code</span></span> | <span data-ttu-id="bcd50-154">意義</span><span class="sxs-lookup"><span data-stu-id="bcd50-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="bcd50-155">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="bcd50-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="bcd50-156">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="bcd50-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="bcd50-157">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="bcd50-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="bcd50-158">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="bcd50-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="bcd50-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="bcd50-159">**WSAEFAULT**</span></span> | <span data-ttu-id="bcd50-160">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="bcd50-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="bcd50-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="bcd50-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="bcd50-162">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="bcd50-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="bcd50-163">**WSAEINTR**</span></span> | <span data-ttu-id="bcd50-164">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="bcd50-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="bcd50-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="bcd50-165">**WSAEINVAL**</span></span> | <span data-ttu-id="bcd50-166">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="bcd50-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="bcd50-167">如果 *cbOutBuffer* 參數小於 **ULONG** 資料類型的大小，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bcd50-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="bcd50-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="bcd50-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="bcd50-169">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="bcd50-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="bcd50-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="bcd50-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="bcd50-171">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="bcd50-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="bcd50-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="bcd50-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="bcd50-173">通訊端未連線。</span><span class="sxs-lookup"><span data-stu-id="bcd50-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="bcd50-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="bcd50-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="bcd50-175">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="bcd50-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="bcd50-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="bcd50-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="bcd50-177">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="bcd50-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="bcd50-178">如果傳輸提供者不支援 **SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bcd50-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="bcd50-179">嘗試使用 **SIO \_ 理想的傳送待處理專案 \_ \_ （BACKLOG） \_ 查詢** IOCTL 是在資料包通訊端上進行時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bcd50-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="bcd50-180">備註</span><span class="sxs-lookup"><span data-stu-id="bcd50-180">Remarks</span></span>

<span data-ttu-id="bcd50-181">Windows Server 2008、Windows Vista Service Pack 1 (SP1) 和更新版本的作業系統都支援 **SIO \_ 理想的傳送待處理專案 \_ \_ （BACKLOG） \_ 查詢** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="bcd50-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="bcd50-182">使用 Windows sockets 透過 TCP 連線傳送資料時，請務必保留足夠的資料量， (傳送但尚未認可到 TCP 中的) ，以達到最高的輸送量。</span><span class="sxs-lookup"><span data-stu-id="bcd50-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="bcd50-183">若要達到 TCP 連接的最佳輸送量，最理想的資料量值就稱為「理想的傳送待處理專案」 (ISB) 大小。</span><span class="sxs-lookup"><span data-stu-id="bcd50-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="bcd50-184">ISB 值是 TCP 連線之頻寬延遲乘積的函式，而接收者的通告接收視窗 (以及網路) 中的擁塞量部分。</span><span class="sxs-lookup"><span data-stu-id="bcd50-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="bcd50-185">您可以從 Windows Server 2008、Windows Vista SP1 和更新版本的作業系統中的 TCP 通訊協定，取得每個連接的 ISB 值。</span><span class="sxs-lookup"><span data-stu-id="bcd50-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="bcd50-186">**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 可供應用程式用來在 ISB 值針對連接動態變更時取得通知。</span><span class="sxs-lookup"><span data-stu-id="bcd50-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="bcd50-187">在 Windows Server 2008、Windows Vista （含 SP1）及更新版本的作業系統上， [**SIO \_ 理想的 \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案（backlog）變更和 **SIO \_ 理想的 \_ 傳送 \_ 待 \_** 處理專案（backlog）查詢 IOCTLs 可在已線上狀態的資料流程導向通訊端上受到支援。</span><span class="sxs-lookup"><span data-stu-id="bcd50-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="bcd50-188">TCP 連接的 ISB 值範圍理論上可能會因0到 16 mb 而異。</span><span class="sxs-lookup"><span data-stu-id="bcd50-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="bcd50-189">[**SIO 理想的傳送待處理 \_ 專案 \_ \_ \_ 變更**](sio-ideal-send-backlog-change.md)和 **SIO 理想的 \_ 傳送待處理專案 \_ \_ （backlog） \_ 查詢** IOCTLs 是根據應用程式所使用的傳送方法。</span><span class="sxs-lookup"><span data-stu-id="bcd50-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="bcd50-190">討論兩個常見的案例。</span><span class="sxs-lookup"><span data-stu-id="bcd50-190">Two common cases are discussed.</span></span>

<span data-ttu-id="bcd50-191">一次執行一個封鎖或非封鎖傳送要求的應用程式，通常會依賴 Winsock 的內部傳送緩衝處理，以達到較佳的輸送量。</span><span class="sxs-lookup"><span data-stu-id="bcd50-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="bcd50-192">給定連接的傳送緩衝區限制是由 **SO \_ SNDBUF** 通訊端選項控制。</span><span class="sxs-lookup"><span data-stu-id="bcd50-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="bcd50-193">對於封鎖和非封鎖傳送方法，傳送緩衝區限制會決定 TCP 中保留的資料量。</span><span class="sxs-lookup"><span data-stu-id="bcd50-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="bcd50-194">如果連接的 ISB 值大於傳送緩衝區限制，則在連接上達成的輸送量將不會是最佳的。</span><span class="sxs-lookup"><span data-stu-id="bcd50-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="bcd50-195">為了達到較佳的輸送量，應用程式可以根據 ISB 查詢的結果設定傳送緩衝區限制，因為連接上發生 ISB 變更通知。</span><span class="sxs-lookup"><span data-stu-id="bcd50-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="bcd50-196">針對使用重迭傳送方法的應用程式，如果有多個未處理的傳送要求，TCP 中未完成的資料量會由 Winsock 中的傳送緩衝區限制和未處理的重迭傳送要求中包含的總數據量來決定。</span><span class="sxs-lookup"><span data-stu-id="bcd50-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="bcd50-197">在此情況下，應用程式應該使用 ISB 值來判斷它們應該保留多少未處理的傳送要求，以及每個傳送要求的資料大小。</span><span class="sxs-lookup"><span data-stu-id="bcd50-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="bcd50-198">在理想的情況下，應用程式應該嘗試保持下列方程式的滿意：</span><span class="sxs-lookup"><span data-stu-id="bcd50-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="bcd50-199">請注意，以上述方式使用 ISB IOCTLs over TCP 通訊端可能會導致 exchange 中的記憶體使用量增加，以增加頻寬延遲最高的連接輸送量。</span><span class="sxs-lookup"><span data-stu-id="bcd50-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="bcd50-200">Windows 中的 TCP 執行會根據整體系統記憶體使用量，視需要節流 ISB 值。</span><span class="sxs-lookup"><span data-stu-id="bcd50-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="bcd50-201">**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 只允許在處於已連接狀態的資料流程通訊端上。</span><span class="sxs-lookup"><span data-stu-id="bcd50-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="bcd50-202">否則， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式將會失敗，並出現 **WSAENOTCONN**。</span><span class="sxs-lookup"><span data-stu-id="bcd50-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="bcd50-203">任何 IOCTL 可能會無限期地封鎖，視服務提供者的執行而定。</span><span class="sxs-lookup"><span data-stu-id="bcd50-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="bcd50-204">如果應用程式無法容忍 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式呼叫中的封鎖，則會建議對可能封鎖的 IOCTLs 進行重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="bcd50-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="bcd50-205">**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 不太可能會封鎖，因此通常會在 *lpOverlapped* 和 *lpCompletionRoutine* 參數設定為 **Null** 的情況下同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="bcd50-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="bcd50-206">**SIO \_ 理想的 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 可能會失敗，並在下列情況下 **\_ \_ 中止** **WSAEINTR** 或 WSA 作業：</span><span class="sxs-lookup"><span data-stu-id="bcd50-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="bcd50-207">TCP 連接會正常地在傳送方向中斷連線。</span><span class="sxs-lookup"><span data-stu-id="bcd50-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="bcd50-208">這可能是因為呼叫 shutdown 函式，並將參數設定為 **SD \_ SEND**、呼叫 **DisconnectEx** 函式，或是呼叫 **TransmitFile** 或 **TransmitPackets** 函式（ *dwFlags* 參數設定為 **tf \_ DISCONNECT** 或 **tf \_ 重複使用**）的結果。</span><span class="sxs-lookup"><span data-stu-id="bcd50-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="bcd50-209">TCP 連接已重設或中止。</span><span class="sxs-lookup"><span data-stu-id="bcd50-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="bcd50-210">I/o 管理員會取消要求。</span><span class="sxs-lookup"><span data-stu-id="bcd50-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="bcd50-211">這些 IOCTLs 的兩個內嵌包裝函式是在 *Ws2tcpip .h* 標頭檔中定義。</span><span class="sxs-lookup"><span data-stu-id="bcd50-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="bcd50-212">建議使用這些內嵌函式，而不是使用 [**SIO 理想的 \_ \_ 傳送 \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案變更和 **SIO 理想的傳送待處理專案 \_ \_ \_ （backlog） \_ 查詢** IOCTLs。</span><span class="sxs-lookup"><span data-stu-id="bcd50-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="bcd50-213">[**SIO \_ 理想 \_ 傳送 \_ 待辦專案 \_ 變更**](sio-ideal-send-backlog-change.md)IOCTL 的內嵌包裝函式是 **idealsendbacklognotify** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="bcd50-214">**SIO \_ 理想 \_ 傳送待處理專案 \_ （BACKLOG） \_ 查詢** IOCTL 的內嵌包裝函式是 **idealsendbacklogquery** 函數。</span><span class="sxs-lookup"><span data-stu-id="bcd50-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="bcd50-215">在 Windows 7 和 Windows Server 2008 R2 上新增了 TCP 的動態傳送緩衝。</span><span class="sxs-lookup"><span data-stu-id="bcd50-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="bcd50-216">除非應用程式在資料流程通訊端上設定 **\_ SNDBUF** 通訊端選項，否則預設會啟用 TCP 的動態傳送緩衝。</span><span class="sxs-lookup"><span data-stu-id="bcd50-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="bcd50-217">使用 netsh 是查詢或設定 TCP 動態傳送緩衝的建議方法。</span><span class="sxs-lookup"><span data-stu-id="bcd50-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="bcd50-218">您可以使用下列命令來抓取 TCP 動態傳送緩衝的目前值：</span><span class="sxs-lookup"><span data-stu-id="bcd50-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="bcd50-219">您可以使用下列命令來停用 TCP 的動態傳送緩衝：</span><span class="sxs-lookup"><span data-stu-id="bcd50-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="bcd50-220">您可以使用下列命令來啟用 TCP 的動態傳送緩衝：</span><span class="sxs-lookup"><span data-stu-id="bcd50-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="bcd50-221">雖然不建議這麼做，您可以藉由將下列登錄值設定為零，從應用程式停用動態傳送緩衝：</span><span class="sxs-lookup"><span data-stu-id="bcd50-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="bcd50-222">使用 NetSh.exe 變更動態傳送緩衝的值或變更登錄值時，必須重新開機電腦，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="bcd50-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="bcd50-223">在 Windows 7 和 Windows Server 2008 R2 上使用動態傳送緩衝處理， [**SIO 理想的 \_ 傳送 \_ \_ 待 \_**](sio-ideal-send-backlog-change.md) 處理專案變更和 **SIO 理想的傳送待處理專案（ \_ \_ \_ backlog） \_ 查詢** IOCTLs 只有在特殊情況下才需要使用。</span><span class="sxs-lookup"><span data-stu-id="bcd50-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcd50-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcd50-224">See also</span></span>

[<span data-ttu-id="bcd50-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="bcd50-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="bcd50-226">**插座**</span><span class="sxs-lookup"><span data-stu-id="bcd50-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="bcd50-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="bcd50-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="bcd50-228">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="bcd50-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="bcd50-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="bcd50-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="bcd50-230">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="bcd50-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="bcd50-231">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="bcd50-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="bcd50-232">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="bcd50-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

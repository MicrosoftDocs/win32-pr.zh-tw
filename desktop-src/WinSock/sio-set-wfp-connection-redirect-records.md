---
description: 控制項程式碼會將重新導向記錄設定為用於連接重新導向服務的新 TCP 通訊端。
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS 控制碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981018"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="617b6-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS 控制碼</span><span class="sxs-lookup"><span data-stu-id="617b6-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="617b6-104">Description</span><span class="sxs-lookup"><span data-stu-id="617b6-104">Description</span></span>

<span data-ttu-id="617b6-105">**SIO \_ SET WFP 連線重新 \_ \_ \_ 導向 \_ 記錄** 控制程式代碼會將重新導向記錄設定為用於連接到最終目的地的新 TCP 通訊端，以供 Windows 篩選平台 (WFP) 重新導向服務使用。</span><span class="sxs-lookup"><span data-stu-id="617b6-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="617b6-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="617b6-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="617b6-107">參數</span><span class="sxs-lookup"><span data-stu-id="617b6-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="617b6-108">s</span><span class="sxs-lookup"><span data-stu-id="617b6-108">s</span></span>

<span data-ttu-id="617b6-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="617b6-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="617b6-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="617b6-110">dwIoControlCode</span></span>

<span data-ttu-id="617b6-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="617b6-111">The control code for the operation.</span></span>
<span data-ttu-id="617b6-112">使用 **SIO 設定此作業的 \_ \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 。</span><span class="sxs-lookup"><span data-stu-id="617b6-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="617b6-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="617b6-113">lpvInBuffer</span></span>

<span data-ttu-id="617b6-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="617b6-115">此參數包含與通訊端相關聯的 WFP 重新導向記錄指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="617b6-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="617b6-116">cbInBuffer</span></span>

<span data-ttu-id="617b6-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="617b6-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="617b6-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="617b6-118">lpvOutBuffer</span></span>

<span data-ttu-id="617b6-119">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="617b6-120">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="617b6-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="617b6-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="617b6-121">cbOutBuffer</span></span>

<span data-ttu-id="617b6-122">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="617b6-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="617b6-123">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="617b6-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="617b6-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="617b6-124">lpcbBytesReturned</span></span>

<span data-ttu-id="617b6-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="617b6-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="617b6-126">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="617b6-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="617b6-127">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="617b6-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="617b6-128">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="617b6-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="617b6-129">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="617b6-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="617b6-130">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="617b6-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="617b6-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="617b6-131">lpvOverlapped</span></span>

<span data-ttu-id="617b6-132">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="617b6-133">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="617b6-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="617b6-134">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="617b6-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="617b6-135">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="617b6-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="617b6-136">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="617b6-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="617b6-137">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="617b6-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="617b6-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="617b6-138">lpCompletionRoutine</span></span>

<span data-ttu-id="617b6-139">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="617b6-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="617b6-140">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="617b6-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="617b6-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="617b6-141">lpThreadId</span></span>

<span data-ttu-id="617b6-142">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="617b6-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="617b6-143">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="617b6-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="617b6-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="617b6-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="617b6-145">lpErrno</span></span>

<span data-ttu-id="617b6-146">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="617b6-146">A pointer to the error code.</span></span>

<span data-ttu-id="617b6-147">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="617b6-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="617b6-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="617b6-148">Return value</span></span>

<span data-ttu-id="617b6-149">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="617b6-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="617b6-150">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="617b6-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="617b6-151">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="617b6-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="617b6-152">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="617b6-152">Error code</span></span> | <span data-ttu-id="617b6-153">意義</span><span class="sxs-lookup"><span data-stu-id="617b6-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="617b6-154">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="617b6-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="617b6-155">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="617b6-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="617b6-156">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="617b6-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="617b6-157">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="617b6-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="617b6-158">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="617b6-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="617b6-159">如果因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="617b6-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="617b6-160">**WSAEACCES**</span></span> | <span data-ttu-id="617b6-161">嘗試以存取權限禁止的方式存取通訊端。</span><span class="sxs-lookup"><span data-stu-id="617b6-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="617b6-162">這項錯誤會在包含下列各項的條件下傳回：使用者缺少本機電腦上所需的系統管理許可權，或應用程式未在增強型 shell 中執行，因為內建的系統管理員 (`RunAs administrator`) 。</span><span class="sxs-lookup"><span data-stu-id="617b6-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="617b6-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="617b6-163">**WSAEFAULT**</span></span> | <span data-ttu-id="617b6-164">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="617b6-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="617b6-165">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="617b6-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="617b6-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="617b6-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="617b6-167">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="617b6-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="617b6-168">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="617b6-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="617b6-169">**WSAEINTR**</span></span> | <span data-ttu-id="617b6-170">呼叫 **WSACancelBlockingCall** 時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="617b6-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="617b6-171">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="617b6-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="617b6-172">**WSAEINVAL**</span></span> | <span data-ttu-id="617b6-173">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="617b6-173">An invalid argument was supplied.</span></span> <span data-ttu-id="617b6-174">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="617b6-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="617b6-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="617b6-176">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="617b6-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="617b6-177">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="617b6-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="617b6-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="617b6-179">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="617b6-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="617b6-180">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="617b6-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="617b6-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="617b6-182">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="617b6-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="617b6-183">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="617b6-184">如果傳輸提供者不支援 **SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="617b6-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="617b6-185">備註</span><span class="sxs-lookup"><span data-stu-id="617b6-185">Remarks</span></span>

<span data-ttu-id="617b6-186">Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="617b6-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="617b6-187">WFP 允許存取 TCP/IP 封包處理路徑，也就是傳出和傳入的封包可以進行檢查或變更，然後再讓它們進一步處理。</span><span class="sxs-lookup"><span data-stu-id="617b6-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="617b6-188">藉由使用 TCP/IP 處理路徑，獨立軟體廠商 (Isv) 可以更輕鬆地建立防火牆、防毒軟體、診斷軟體及其他類型的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="617b6-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="617b6-189">WFP 提供使用者模式和核心模式元件，讓協力廠商 Isv 可以參與在 TCP/IP 通訊協定堆疊和整個作業系統中的數個層級進行的篩選決策。</span><span class="sxs-lookup"><span data-stu-id="617b6-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="617b6-190">[WFP 連接重新導向] 功能可讓 WFP 標注核心驅動程式將連接重新導向至使用者模式進程、在使用者模式中執行內容檢查，以及使用不同的連線將已檢查的內容轉送到原始目的地。</span><span class="sxs-lookup"><span data-stu-id="617b6-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="617b6-191">**SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 和數個其他相關 IOCTLS 是使用者模式元件，可用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。</span><span class="sxs-lookup"><span data-stu-id="617b6-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="617b6-192">每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。</span><span class="sxs-lookup"><span data-stu-id="617b6-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="617b6-193">由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。</span><span class="sxs-lookup"><span data-stu-id="617b6-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="617b6-194">如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。</span><span class="sxs-lookup"><span data-stu-id="617b6-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="617b6-195">**SIO \_ SET \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。</span><span class="sxs-lookup"><span data-stu-id="617b6-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="617b6-196">這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。</span><span class="sxs-lookup"><span data-stu-id="617b6-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="617b6-197">[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)的 IOCTL 會由 WFP 型重新導向服務用來從已接受的 tcp/ip 封包連線取得重新導向記錄， (tcp 通訊端或 UDP 通訊端的已連接通訊端，例如，) 透過在核心模式驅動程式中的 **ALE \_ 連接重新 \_ 導向** 層所註冊的隨附核心模式注標重新導向至該連接。</span><span class="sxs-lookup"><span data-stu-id="617b6-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="617b6-198">[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)的 IOCTL 會取得重新導向記錄的重新導向內容，這是使用的。</span><span class="sxs-lookup"><span data-stu-id="617b6-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="617b6-199">重新導向內容是選擇性的，如果連接目前的重新導向狀態是由呼叫重新導向服務重新導向連接，或先前被呼叫重新導向服務重新導向，但稍後又由不同的重新導向服務重新導向，則會使用。重新導向服務會使用 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL，將抓取的重新導向記錄傳輸至它用來 proxy 原始內容的 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="617b6-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="617b6-200">呼叫 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 的應用程式不需要瞭解包含要設定之重新導向記錄的 blob。</span><span class="sxs-lookup"><span data-stu-id="617b6-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="617b6-201">這是不透明的資料 blob，應用程式必須將其傳回至新的通訊端。</span><span class="sxs-lookup"><span data-stu-id="617b6-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="617b6-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="617b6-202">See also</span></span>

[<span data-ttu-id="617b6-203">**IPPROTO_IP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="617b6-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="617b6-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="617b6-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="617b6-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="617b6-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="617b6-206">**插座**</span><span class="sxs-lookup"><span data-stu-id="617b6-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="617b6-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="617b6-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="617b6-208">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="617b6-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="617b6-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="617b6-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="617b6-210">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="617b6-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="617b6-211">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="617b6-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="617b6-212">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="617b6-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

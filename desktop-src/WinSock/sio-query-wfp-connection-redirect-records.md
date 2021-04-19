---
description: 控制項程式碼會抓取已接受 TCP/IP 連接的重新導向記錄，以供 Windows 篩選平台重新導向服務使用。
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988722"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="70c6b-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="70c6b-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="70c6b-104">Description</span><span class="sxs-lookup"><span data-stu-id="70c6b-104">Description</span></span>

<span data-ttu-id="70c6b-105">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** 控制程式代碼會抓取已接受 tcp/ip 連接的重新導向記錄，以供 Windows 篩選平台 (WFP) 重新導向服務使用。</span><span class="sxs-lookup"><span data-stu-id="70c6b-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="70c6b-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="70c6b-107">參數</span><span class="sxs-lookup"><span data-stu-id="70c6b-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="70c6b-108">s</span><span class="sxs-lookup"><span data-stu-id="70c6b-108">s</span></span>

<span data-ttu-id="70c6b-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="70c6b-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="70c6b-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="70c6b-110">dwIoControlCode</span></span>

<span data-ttu-id="70c6b-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="70c6b-111">The control code for the operation.</span></span>
<span data-ttu-id="70c6b-112">使用 **SIO \_ 查詢 \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="70c6b-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="70c6b-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="70c6b-113">lpvInBuffer</span></span>

<span data-ttu-id="70c6b-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="70c6b-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="70c6b-115">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="70c6b-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="70c6b-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="70c6b-116">cbInBuffer</span></span>

<span data-ttu-id="70c6b-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70c6b-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="70c6b-118">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="70c6b-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="70c6b-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="70c6b-119">lpvOutBuffer</span></span>

<span data-ttu-id="70c6b-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="70c6b-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="70c6b-121">如果 *lpOverlapped* 和 *LpCompletionRoutine* 參數為 **Null**，則此參數應指向 **ULONG** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="70c6b-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="70c6b-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="70c6b-122">cbOutBuffer</span></span>

<span data-ttu-id="70c6b-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70c6b-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="70c6b-124">此參數必須至少為 **ULONG** 資料類型的大小。</span><span class="sxs-lookup"><span data-stu-id="70c6b-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="70c6b-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="70c6b-125">lpcbBytesReturned</span></span>

<span data-ttu-id="70c6b-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="70c6b-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="70c6b-127">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="70c6b-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="70c6b-128">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="70c6b-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="70c6b-129">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="70c6b-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="70c6b-130">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="70c6b-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="70c6b-131">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="70c6b-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="70c6b-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="70c6b-132">lpvOverlapped</span></span>

<span data-ttu-id="70c6b-133">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="70c6b-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="70c6b-134">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="70c6b-135">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="70c6b-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="70c6b-136">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="70c6b-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="70c6b-137">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="70c6b-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="70c6b-138">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="70c6b-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="70c6b-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="70c6b-139">lpCompletionRoutine</span></span>

<span data-ttu-id="70c6b-140">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="70c6b-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="70c6b-141">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="70c6b-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="70c6b-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="70c6b-142">lpThreadId</span></span>

<span data-ttu-id="70c6b-143">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="70c6b-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="70c6b-144">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="70c6b-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="70c6b-145">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="70c6b-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="70c6b-146">lpErrno</span></span>

<span data-ttu-id="70c6b-147">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="70c6b-147">A pointer to the error code.</span></span>

<span data-ttu-id="70c6b-148">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="70c6b-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="70c6b-149">Return value</span></span>

<span data-ttu-id="70c6b-150">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="70c6b-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="70c6b-151">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="70c6b-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="70c6b-152">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="70c6b-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="70c6b-153">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="70c6b-153">Error code</span></span> | <span data-ttu-id="70c6b-154">意義</span><span class="sxs-lookup"><span data-stu-id="70c6b-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="70c6b-155">**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="70c6b-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="70c6b-156">傳遞給系統呼叫的資料區域太小。</span><span class="sxs-lookup"><span data-stu-id="70c6b-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="70c6b-157">如果 *lpvOutBuffer* 參數所指向的緩衝區的緩衝區大小超過 *cbOutBuffer* 參數，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="70c6b-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="70c6b-158">所需的緩衝區大小將會在 *lpcbBytesReturned* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="70c6b-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="70c6b-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="70c6b-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="70c6b-160">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="70c6b-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="70c6b-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="70c6b-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="70c6b-162">因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行，所以重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="70c6b-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="70c6b-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="70c6b-163">**WSAEFAULT**</span></span> | <span data-ttu-id="70c6b-164">*LpvOutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="70c6b-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="70c6b-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="70c6b-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="70c6b-166">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="70c6b-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="70c6b-167">**WSAEINTR**</span></span> | <span data-ttu-id="70c6b-168">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="70c6b-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="70c6b-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="70c6b-169">**WSAEINVAL**</span></span> | <span data-ttu-id="70c6b-170">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="70c6b-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="70c6b-171">如果 *cbOutBuffer* 參數小於 **ULONG** 資料類型的大小，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="70c6b-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="70c6b-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="70c6b-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="70c6b-173">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="70c6b-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="70c6b-174">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="70c6b-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="70c6b-175">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="70c6b-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="70c6b-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="70c6b-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="70c6b-177">*通訊端未連線*。</span><span class="sxs-lookup"><span data-stu-id="70c6b-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="70c6b-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="70c6b-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="70c6b-179">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="70c6b-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="70c6b-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="70c6b-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="70c6b-181">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="70c6b-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="70c6b-182">如果傳輸提供者不支援 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="70c6b-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="70c6b-183">備註</span><span class="sxs-lookup"><span data-stu-id="70c6b-183">Remarks</span></span>

<span data-ttu-id="70c6b-184">Windows 8、Windows Server 2012 和更新版本的作業系統上都支援 **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="70c6b-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="70c6b-185">WFP 允許存取 TCP/IP 封包處理路徑，也就是傳出和傳入的封包可以進行檢查或變更，然後再讓它們進一步處理。</span><span class="sxs-lookup"><span data-stu-id="70c6b-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="70c6b-186">藉由使用 TCP/IP 處理路徑，獨立軟體廠商 (Isv) 可以更輕鬆地建立防火牆、防毒軟體、診斷軟體及其他類型的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="70c6b-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="70c6b-187">WFP 提供使用者模式和核心模式元件，讓協力廠商 Isv 可以參與在 TCP/IP 通訊協定堆疊和整個作業系統中的數個層級進行的篩選決策。</span><span class="sxs-lookup"><span data-stu-id="70c6b-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="70c6b-188">[WFP 連接重新導向] 功能可讓 WFP 標注核心驅動程式將連接重新導向至使用者模式進程、在使用者模式中執行內容檢查，以及使用不同的連線將已檢查的內容轉送到原始目的地。</span><span class="sxs-lookup"><span data-stu-id="70c6b-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="70c6b-189">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 和數個其他相關 IOCTLS 是使用者模式元件，用來允許多個以 WFP 為基礎的連線 proxy 應用程式以合作方式檢查相同的流量流程。</span><span class="sxs-lookup"><span data-stu-id="70c6b-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="70c6b-190">每個檢查代理程式都可以安全地重新檢查已由另一個檢查代理程式檢查的網路流量。</span><span class="sxs-lookup"><span data-stu-id="70c6b-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="70c6b-191">由於有多個 proxy (由不同的 Isv 開發，例如) 某個 proxy 用來與最終目的地通訊的連線，可能會被第二個 proxy 重新導向，而且原始 proxy 可以再次重新導向新的連接。</span><span class="sxs-lookup"><span data-stu-id="70c6b-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="70c6b-192">如果沒有連線追蹤，原始連接可能永遠不會到達它的最終目的地，因為它卡在無限的 proxy 迴圈中。</span><span class="sxs-lookup"><span data-stu-id="70c6b-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="70c6b-193">**SIO \_ QUERY \_ WFP 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 可用來在重新導向的通訊端連線上提供代理的連接追蹤。</span><span class="sxs-lookup"><span data-stu-id="70c6b-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="70c6b-194">這種 WFP 功能可從連接的初始重新導向到目的地的最終連接，來協助追蹤重新導向記錄。</span><span class="sxs-lookup"><span data-stu-id="70c6b-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="70c6b-195">**SIO \_ QUERY \_ wfp 連接重新 \_ \_ 導向 \_ 記錄** IOCTL 是由 WFP 型重新導向服務用來從已接受的 tcp/ip 封包連線取得重新導向記錄， (tcp 通訊端或 UDP 通訊端的連線通訊端，例如) 由在核心模式驅動程式中 **ALE_CONNECT_REDIRECT** 層級註冊的隨附核心模式注標重新導向。</span><span class="sxs-lookup"><span data-stu-id="70c6b-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="70c6b-196">**SIO \_ QUERY wfp 連線重新 \_ \_ \_ 導向 \_ 內容** IOCTL 會由 WFP 型重新導向服務用來從已接受的 TCP/IP 封包連線中，取得 tcp 通訊端或 UDP 通訊端的連線通訊端之重新導向記錄的重新導向內容，例如，) 由在 ALE 連線重新 **\_ \_ 導向** 層級註冊的隨附注標重新導向至該 (連接。</span><span class="sxs-lookup"><span data-stu-id="70c6b-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="70c6b-197">重新導向內容是選擇性的驅動程式配置內容，如果連接目前的重新導向狀態是由呼叫重新導向服務重新導向連接，或先前被呼叫的重新導向服務重新導向，但稍後又由不同的重新導向服務重新導向，則會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="70c6b-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="70c6b-198">若為 TCP proxy 連線，重新導向服務會將抓取的重新導向記錄傳輸至它用來 proxy 原始內容的 TCP 通訊端，並使用 **SIO \_ SET \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="70c6b-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="70c6b-199">當重新導向服務將非 TCP 通訊端重新導向 (UDP （例如) ）時， **SIO \_ QUERY \_ WFP \_ 連接重新 \_ 導向 \_ 記錄** 的重新導向記錄會使用與 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函數搭配使用的 [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)結構，向重新導向服務表示這一點。</span><span class="sxs-lookup"><span data-stu-id="70c6b-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="70c6b-200">[**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)結構的控制項成員會在 **WSACMSGHDR** 結構中設定為 **IP \_ 連接重新 \_ 導向 \_ 記錄** 的 cmsg_type。</span><span class="sxs-lookup"><span data-stu-id="70c6b-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="70c6b-201">在接受非 TCP 重新導向時，重新導向服務必須提供 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 參數。</span><span class="sxs-lookup"><span data-stu-id="70c6b-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="70c6b-202">針對非 TCP 流量，重新導向記錄會使用 [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) 結構與 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 函式進行轉送。</span><span class="sxs-lookup"><span data-stu-id="70c6b-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="70c6b-203">請注意，針對非 TCP 流量，只有流程建立封包會包含 **IP 連接重新 \_ \_ 導向 \_ 記錄**。</span><span class="sxs-lookup"><span data-stu-id="70c6b-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="70c6b-204">因此，只有第一個 proxy 封包需要使用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式來包含此資訊。</span><span class="sxs-lookup"><span data-stu-id="70c6b-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="70c6b-205">因為 WFP 重新導向記錄是可變長度的資料 blob，所以呼叫端可以提供大型的輸出緩衝區 (*lpvOutBuffer* 參數所指向的1024位元組緩衝區，例如) 或可傳遞 *cbOutBuffer* 參數0的輸出緩衝區大小，以查詢保存所傳回之 blob 所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="70c6b-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="70c6b-206">如果輸出緩衝區大小不足以保存資料，則 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會傳回 **錯誤的 \_ \_ 緩衝區** ，而且所需的緩衝區大小將會以 *lpcbBytesReturned* 參數所指向的值傳回。</span><span class="sxs-lookup"><span data-stu-id="70c6b-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="70c6b-207">呼叫 [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) 的應用程式不需要瞭解包含已抓取之重新導向內容的 blob。</span><span class="sxs-lookup"><span data-stu-id="70c6b-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="70c6b-208">這是不透明的資料 blob，應用程式需要將其取出並傳回至新的通訊端。</span><span class="sxs-lookup"><span data-stu-id="70c6b-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="70c6b-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70c6b-209">See also</span></span>

[<span data-ttu-id="70c6b-210">**IPPROTO_IP 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="70c6b-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="70c6b-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="70c6b-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="70c6b-212">**插座**</span><span class="sxs-lookup"><span data-stu-id="70c6b-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="70c6b-213">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="70c6b-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="70c6b-214">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="70c6b-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="70c6b-215">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="70c6b-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="70c6b-216">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="70c6b-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="70c6b-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="70c6b-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="70c6b-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="70c6b-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="70c6b-219">**WSASendMsg**</span><span class="sxs-lookup"><span data-stu-id="70c6b-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="70c6b-220">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="70c6b-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="70c6b-221">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="70c6b-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

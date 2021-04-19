---
description: 控制項程式碼會將一或多個傳輸設定套用至通訊端。
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: SIO_APPLY_TRANSPORT_SETTING 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977830"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="2305f-103">SIO_APPLY_TRANSPORT_SETTING 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="2305f-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2305f-104">Description</span><span class="sxs-lookup"><span data-stu-id="2305f-104">Description</span></span>

<span data-ttu-id="2305f-105">**SIO 套用 \_ \_ 傳輸 \_ 設定** 控制程式代碼會將一或多個傳輸設定套用至通訊端。</span><span class="sxs-lookup"><span data-stu-id="2305f-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="2305f-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2305f-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="2305f-107">參數</span><span class="sxs-lookup"><span data-stu-id="2305f-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2305f-108">s</span><span class="sxs-lookup"><span data-stu-id="2305f-108">s</span></span>

<span data-ttu-id="2305f-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="2305f-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2305f-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="2305f-110">dwIoControlCode</span></span>

<span data-ttu-id="2305f-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="2305f-111">The control code for the operation.</span></span>
<span data-ttu-id="2305f-112">使用 **SIO \_ 適用于此作業的 \_ 傳輸 \_ 設定** 。</span><span class="sxs-lookup"><span data-stu-id="2305f-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2305f-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="2305f-113">lpvInBuffer</span></span>

<span data-ttu-id="2305f-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2305f-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="2305f-115">此參數包含結構的指標，其中結構的第一個成員是 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 結構，可判斷要套用的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="2305f-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2305f-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="2305f-116">cbInBuffer</span></span>

<span data-ttu-id="2305f-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2305f-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="2305f-118">此參數取決於所套用的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="2305f-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2305f-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2305f-119">lpvOutBuffer</span></span>

<span data-ttu-id="2305f-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2305f-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2305f-121">此參數取決於所套用的傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="2305f-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2305f-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2305f-122">cbOutBuffer</span></span>

<span data-ttu-id="2305f-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2305f-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2305f-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="2305f-124">lpcbBytesReturned</span></span>

<span data-ttu-id="2305f-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2305f-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="2305f-126">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="2305f-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="2305f-127">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="2305f-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="2305f-128">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="2305f-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="2305f-129">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="2305f-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="2305f-130">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="2305f-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2305f-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="2305f-131">lpvOverlapped</span></span>

<span data-ttu-id="2305f-132">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2305f-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2305f-133">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="2305f-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2305f-134">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="2305f-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2305f-135">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="2305f-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2305f-136">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="2305f-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2305f-137">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="2305f-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2305f-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="2305f-138">lpCompletionRoutine</span></span>

<span data-ttu-id="2305f-139">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2305f-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2305f-140">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="2305f-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2305f-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="2305f-141">lpThreadId</span></span>

<span data-ttu-id="2305f-142">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="2305f-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2305f-143">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="2305f-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2305f-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2305f-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2305f-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="2305f-145">lpErrno</span></span>

<span data-ttu-id="2305f-146">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="2305f-146">A pointer to the error code.</span></span>

<span data-ttu-id="2305f-147">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2305f-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2305f-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="2305f-148">Return value</span></span>

<span data-ttu-id="2305f-149">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2305f-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2305f-150">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="2305f-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2305f-151">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="2305f-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2305f-152">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2305f-152">Error code</span></span> | <span data-ttu-id="2305f-153">意義</span><span class="sxs-lookup"><span data-stu-id="2305f-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="2305f-154">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="2305f-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2305f-155">重迭的 i/o 作業正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2305f-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="2305f-156">如果已成功起始重迭作業，並將在稍後指出完成，則會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="2305f-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2305f-157">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="2305f-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2305f-158">I/o 作業因為執行緒結束或應用程式要求而中止。</span><span class="sxs-lookup"><span data-stu-id="2305f-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="2305f-159">如果因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行而取消重迭的作業，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="2305f-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2305f-160">**WSAEFAULT**</span></span> | <span data-ttu-id="2305f-161">系統在嘗試使用呼叫中的指標引數時偵測到不正確指標位址。</span><span class="sxs-lookup"><span data-stu-id="2305f-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="2305f-162">*LpvInBuffer*、 *lpvoutBuffer*、 *lpcbBytesReturned*、 *lpOverlapped* 或 *lpCompletionRoutine* 參數所傳回的錯誤，不會完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="2305f-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2305f-163">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2305f-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2305f-164">正在執行封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="2305f-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="2305f-165">如果回呼正在進行中，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2305f-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="2305f-166">**WSAEINTR**</span></span> | <span data-ttu-id="2305f-167">呼叫 [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)時，封鎖作業中斷。</span><span class="sxs-lookup"><span data-stu-id="2305f-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="2305f-168">當封鎖作業中斷時，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2305f-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="2305f-169">**WSAEINVAL**</span></span> | <span data-ttu-id="2305f-170">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="2305f-170">An invalid argument was supplied.</span></span> <span data-ttu-id="2305f-171">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="2305f-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2305f-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="2305f-173">通訊端作業遇到停止的網路。</span><span class="sxs-lookup"><span data-stu-id="2305f-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="2305f-174">如果網路子系統失敗，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="2305f-175">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="2305f-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2305f-176">嘗試對不是通訊端的某個作業進行作業。</span><span class="sxs-lookup"><span data-stu-id="2305f-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="2305f-177">如果 *描述項不是套* 接字，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="2305f-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="2305f-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2305f-179">所參考的物件類型不支援所嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="2305f-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="2305f-180">如果不支援指定的 IOCTL 命令，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="2305f-181">如果傳輸提供者不支援 **SIO \_ APPLY \_ 傳輸 \_ 設定** IOCTL，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="2305f-182">當嘗試在 UDP 或 TCP 以外的通訊端上進行使用 **SIO 套用 \_ \_ 傳輸 \_ 設定** 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2305f-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2305f-183">備註</span><span class="sxs-lookup"><span data-stu-id="2305f-183">Remarks</span></span>

<span data-ttu-id="2305f-184">Windows 8、Windows Server 2012 和更新版本的作業系統都支援 **SIO 套用 \_ \_ 傳輸 \_ 設定** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="2305f-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="2305f-185">**SIO 套用 \_ \_ 傳輸 \_ 設定** IOCTL 是用來將傳輸設定套用至通訊端的一般 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="2305f-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="2305f-186">所要套用的傳輸設定是以 *lpvInBuffer* 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)為基礎。</span><span class="sxs-lookup"><span data-stu-id="2305f-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="2305f-187">從 Windows 8 和 Windows Server 2012 開始，系統會定義 TCP 通訊端上的 **REAL_TIME_NOTIFICATION_CAPABILITY** 功能。</span><span class="sxs-lookup"><span data-stu-id="2305f-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="2305f-188">從 Windows 10 和 Windows Server 2016 開始，也會定義 **\_ NAMERES \_ 內容的關聯** 。</span><span class="sxs-lookup"><span data-stu-id="2305f-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="2305f-189">如需詳細資訊，請參閱 [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) 和 [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input)。</span><span class="sxs-lookup"><span data-stu-id="2305f-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="2305f-190">如果在 lpvInBuffer 參數中傳遞的 [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) 將 Guid 成員設為 **即時 \_ \_ 通知 \_ 功能**，則這是要求套用適用于 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 的 TCP 通訊端的即時通知設定，以在 Windows Store 應用程式中接收背景網路通知。</span><span class="sxs-lookup"><span data-stu-id="2305f-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="2305f-191">*LpvInBuffer* 參數應指向 **REAL_TIME_NOTIFICATION_SETTING_INPUT** 結構。</span><span class="sxs-lookup"><span data-stu-id="2305f-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="2305f-192">此作業未使用 *lpvOutBuffer* 參數。</span><span class="sxs-lookup"><span data-stu-id="2305f-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="2305f-193">此傳輸設定只適用于 TCP 通訊端。</span><span class="sxs-lookup"><span data-stu-id="2305f-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="2305f-194">此傳輸設定提供一種方式，讓 WinInet 或類似的網路服務將指定的 TCP 通訊端標示為已啟用 [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) 。</span><span class="sxs-lookup"><span data-stu-id="2305f-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="2305f-195">當呼叫這個選項時，Windows 會標示對應的 TCP 通訊端，並設定適當的硬體和軟體設定。</span><span class="sxs-lookup"><span data-stu-id="2305f-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="2305f-196">Windows Store 應用程式不會直接呼叫這個 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="2305f-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="2305f-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2305f-197">See also</span></span>

[<span data-ttu-id="2305f-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="2305f-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="2305f-199">插座</span><span class="sxs-lookup"><span data-stu-id="2305f-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2305f-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="2305f-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="2305f-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="2305f-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="2305f-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="2305f-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="2305f-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="2305f-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2305f-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="2305f-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2305f-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="2305f-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2305f-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="2305f-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2305f-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="2305f-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

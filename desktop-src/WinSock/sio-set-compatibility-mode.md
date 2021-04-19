---
description: 要求網路堆疊應該如何處理特定行為，而這種行為的預設處理方式可能會在 Windows 版本之間不同。
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: SIO_SET_COMPATIBILITY_MODE 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977017"
---
# <a name="sio_set_compatibility_mode-control-code"></a><span data-ttu-id="2cd88-103">SIO_SET_COMPATIBILITY_MODE 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="2cd88-103">SIO_SET_COMPATIBILITY_MODE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2cd88-104">Description</span><span class="sxs-lookup"><span data-stu-id="2cd88-104">Description</span></span>

<span data-ttu-id="2cd88-105">**SIO \_ SET \_ 相容性 \_ 模式** 控制程式代碼會要求網路堆疊應該如何處理在不同 Windows 版本之間，其行為的預設處理方式可能不同的特定行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-105">The **SIO\_SET\_COMPATIBILITY\_MODE** control code requests how the networking stack should handle certain behaviors for which the default way of handling the behavior may differ across Windows versions.</span></span>

<span data-ttu-id="2cd88-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
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

## <a name="parameters"></a><span data-ttu-id="2cd88-107">參數</span><span class="sxs-lookup"><span data-stu-id="2cd88-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2cd88-108">s</span><span class="sxs-lookup"><span data-stu-id="2cd88-108">s</span></span>

<span data-ttu-id="2cd88-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="2cd88-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2cd88-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="2cd88-110">dwIoControlCode</span></span>

<span data-ttu-id="2cd88-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="2cd88-111">The control code for the operation.</span></span>
<span data-ttu-id="2cd88-112">使用 **SIO 設定此作業的 \_ \_ 相容性 \_ 模式** 。</span><span class="sxs-lookup"><span data-stu-id="2cd88-112">Use **SIO\_SET\_COMPATIBILITY\_MODE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2cd88-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="2cd88-113">lpvInBuffer</span></span>

<span data-ttu-id="2cd88-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="2cd88-115">此參數應指向 **WSA \_ 相容性 \_ 模式** 結構。</span><span class="sxs-lookup"><span data-stu-id="2cd88-115">This parameter should point to a **WSA\_COMPATIBILITY\_MODE** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2cd88-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="2cd88-116">cbInBuffer</span></span>

<span data-ttu-id="2cd88-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2cd88-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="2cd88-118">此參數應等於或大於 *lpvInBuffer* 參數所指向的 **WSA \_ 相容性 \_ 模式** 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-118">This parameter should equal to or greater than the size of the **WSA\_COMPATIBILITY\_MODE** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2cd88-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2cd88-119">lpvOutBuffer</span></span>

<span data-ttu-id="2cd88-120">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2cd88-121">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="2cd88-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2cd88-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2cd88-122">cbOutBuffer</span></span>

<span data-ttu-id="2cd88-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2cd88-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="2cd88-124">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="2cd88-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2cd88-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="2cd88-125">lpcbBytesReturned</span></span>

<span data-ttu-id="2cd88-126">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2cd88-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="2cd88-127">這項作業的傳回參數指向 **DWORD** 值零，因為沒有任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2cd88-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2cd88-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="2cd88-128">lpvOverlapped</span></span>

<span data-ttu-id="2cd88-129">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2cd88-130">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2cd88-131">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="2cd88-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2cd88-132">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="2cd88-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2cd88-133">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="2cd88-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2cd88-134">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="2cd88-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2cd88-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="2cd88-135">lpCompletionRoutine</span></span>

<span data-ttu-id="2cd88-136">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2cd88-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2cd88-137">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="2cd88-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2cd88-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="2cd88-138">lpThreadId</span></span>

<span data-ttu-id="2cd88-139">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="2cd88-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2cd88-140">在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2cd88-141">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2cd88-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="2cd88-142">lpErrno</span></span>

<span data-ttu-id="2cd88-143">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-143">A pointer to the error code.</span></span>

<span data-ttu-id="2cd88-144">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cd88-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cd88-145">Return value</span></span>

<span data-ttu-id="2cd88-146">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2cd88-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2cd88-147">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="2cd88-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2cd88-148">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="2cd88-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2cd88-149">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2cd88-149">Error code</span></span> | <span data-ttu-id="2cd88-150">意義</span><span class="sxs-lookup"><span data-stu-id="2cd88-150">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="2cd88-151">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="2cd88-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2cd88-152">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="2cd88-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2cd88-153">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="2cd88-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2cd88-154">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="2cd88-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="2cd88-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2cd88-155">**WSAEFAULT**</span></span> | <span data-ttu-id="2cd88-156">*LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="2cd88-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2cd88-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2cd88-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2cd88-158">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2cd88-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="2cd88-159">**WSAEINTR**</span></span> | <span data-ttu-id="2cd88-160">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="2cd88-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2cd88-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="2cd88-161">**WSAEINVAL**</span></span> | <span data-ttu-id="2cd88-162">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="2cd88-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="2cd88-163">如果 *cbInBuffer* 參數小於 **WSA \_ 相容性 \_ 模式** 結構的 sizeof，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cd88-163">This error is returned if the *cbInBuffer* parameter is less than the sizeof the **WSA\_COMPATIBILITY\_MODE** structure.</span></span>
| <span data-ttu-id="2cd88-164">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2cd88-164">**WSAENETDOWN**</span></span> | <span data-ttu-id="2cd88-165">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="2cd88-165">The network subsystem has failed.</span></span> |
| <span data-ttu-id="2cd88-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="2cd88-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="2cd88-167">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="2cd88-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="2cd88-168">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="2cd88-168">**WSAENOTCONN**</span></span> | <span data-ttu-id="2cd88-169">通訊端未連線。</span><span class="sxs-lookup"><span data-stu-id="2cd88-169">The socket s is not connected.</span></span> |
| <span data-ttu-id="2cd88-170">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="2cd88-170">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2cd88-171">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="2cd88-171">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="2cd88-172">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="2cd88-172">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2cd88-173">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="2cd88-173">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="2cd88-174">如果傳輸提供者不支援 **SIO \_ SET \_ 相容性 \_ 模式** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cd88-174">This error is returned if the **SIO\_SET\_COMPATIBILITY\_MODE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="2cd88-175">當嘗試在資料包通訊端上進行使用 **SIO \_ SET \_ 相容性 \_ 模式** IOCTL 時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cd88-175">This error is also returned when an attempt to use the **SIO\_SET\_COMPATIBILITY\_MODE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2cd88-176">備註</span><span class="sxs-lookup"><span data-stu-id="2cd88-176">Remarks</span></span>

<span data-ttu-id="2cd88-177">**SIO \_ 設定的 \_ 相容性 \_ 模式** IOCTL 會要求網路堆疊應該如何處理在不同 Windows 版本之間，其行為的預設處理方式可能不同的特定行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-177">the **SIO\_SET\_COMPATIBILITY\_MODE** IOCTL requests how the networking stack should handle certain behaviors for which the default way of handling the behavior may differ across Windows versions.</span></span>
<span data-ttu-id="2cd88-178">**SIO \_ 集 \_ 相容性 \_ 模式** 的輸入引數結構是在 *Mswsockdef .H* 標頭檔中定義的 **WSA \_ 相容性 \_ 模式** 結構中指定。</span><span class="sxs-lookup"><span data-stu-id="2cd88-178">The input argument structure for **SIO\_SET\_COMPATIBILITY\_MODE** is specified in the **WSA\_COMPATIBILITY\_MODE** structure defined in the *Mswsockdef.h* header file.</span></span>
<span data-ttu-id="2cd88-179">在 *cbInBuffer* 參數中傳遞 **WSA \_ 相容性 \_ 模式** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd88-179">A pointer to the **WSA\_COMPATIBILITY\_MODE** structure is passed in the *cbInBuffer* parameter.</span></span>
<span data-ttu-id="2cd88-180">此結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="2cd88-180">This structure is defined as follows:</span></span>

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

<span data-ttu-id="2cd88-181">**BehaviorId** 成員中指定的值會指出所要求的行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-181">The value specified in the **BehaviorId** member indicates the behavior requested.</span></span>
<span data-ttu-id="2cd88-182">**TargetOsVersion** 成員中指定的值會指出所要求的行為的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="2cd88-182">The value specified in the **TargetOsVersion** member indicates the Windows version that is being requested for the behavior.</span></span>

<span data-ttu-id="2cd88-183">**BehaviorId** 成員可以是 *Mswsockdef .h* 標頭檔中所定義之 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 列舉類型的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2cd88-183">The **BehaviorId** member can be one of the values from the **WSA\_COMPATIBILITY\_BEHAVIOR\_ID** enumeration type defined in the *Mswsockdef.h* header file.</span></span>
<span data-ttu-id="2cd88-184">**BehaviorId** 成員的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="2cd88-184">The possible values for the **BehaviorId** member are as follows:</span></span>

| <span data-ttu-id="2cd88-185">詞彙</span><span class="sxs-lookup"><span data-stu-id="2cd88-185">Term</span></span> | <span data-ttu-id="2cd88-186">描述</span><span class="sxs-lookup"><span data-stu-id="2cd88-186">Description</span></span> |
|------|-------------|
| <span data-ttu-id="2cd88-187">WsaBehaviorAll</span><span class="sxs-lookup"><span data-stu-id="2cd88-187">WsaBehaviorAll</span></span> | <span data-ttu-id="2cd88-188">這相當於要求針對 **WSA \_ 相容性 \_ 行為 \_ 識別碼** 定義的所有可能相容行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-188">This is equivalent to requesting all of the possible compatible behaviors defined for **WSA\_COMPATIBILITY\_BEHAVIOR\_ID**.</span></span> |
| <span data-ttu-id="2cd88-189">WsaBehaviorReceiveBuffering</span><span class="sxs-lookup"><span data-stu-id="2cd88-189">WsaBehaviorReceiveBuffering</span></span> | <span data-ttu-id="2cd88-190">當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，即使在建立 tcp 連線之後，也允許使用 **SO \_ RCVBUF** 通訊端選項減少此通訊端上的 TCP 接收緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-190">When the **TargetOsVersion** member is set to a value for Windows Vista or later, reductions to the TCP receive buffer size on this socket using the **SO\_RCVBUF** socket option are allowed even after a TCP connection has been establishment.</span></span> <span data-ttu-id="2cd88-191">當 **TargetOsVersion** 成員設定為早于 Windows Vista 的值時，在連線建立之後，就不允許使用 **\_ RCVBUF** 通訊端選項來降低此通訊端上的 TCP 接收緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-191">When the **TargetOsVersion** member is set to a value earlier than Windows Vista, reductions to the TCP receive buffer size on this socket using the **SO\_RCVBUF** socket option are not allowed after connection establishment.</span></span> |
| <span data-ttu-id="2cd88-192">WsaBehaviorAutoTuning</span><span class="sxs-lookup"><span data-stu-id="2cd88-192">WsaBehaviorAutoTuning</span></span> | <span data-ttu-id="2cd88-193">當 **TargetOsVersion** 成員設定為 Windows Vista 或更新版本的值時，會啟用 [接收視窗自動調整]，並將 [TCP 視窗縮放比例] 從預設值8縮減為2。</span><span class="sxs-lookup"><span data-stu-id="2cd88-193">When the **TargetOsVersion** member is set to a value for Windows Vista or later, receive window auto-tuning is enabled and the TCP window scale factor is reduced to 2 from the default value of 8.</span></span> <span data-ttu-id="2cd88-194">當 **TargetOsVersion** 設定為 Windows Vista 之前的值時，會停用 [接收視窗自動調整]。</span><span class="sxs-lookup"><span data-stu-id="2cd88-194">When the **TargetOsVersion** is set to a value earlier than Windows Vista, receive window auto-tuning is disabled.</span></span> <span data-ttu-id="2cd88-195">[TCP 視窗調整] 選項也會停用，而 [最大值] 接收視窗大小則限制為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-195">The TCP window scaling option is also disabled and the maximum true receive window size is limited to 65,535 bytes.</span></span> <span data-ttu-id="2cd88-196">即使在此通訊端上呼叫 **\_ RCVBUF** 通訊端選項，在建立連接之前指定大於65535個位元組的值，也無法在連接上協商 TCP 視窗調整選項。</span><span class="sxs-lookup"><span data-stu-id="2cd88-196">The TCP window scaling option can't be negotiated on the connection even if the **SO\_RCVBUF** socket option was called on this socket specifying a value greater than 65,535 bytes before the connection was established.</span></span> |

<span data-ttu-id="2cd88-197">**TargetOsVersion** 成員可以是 *sdkddkver.h .h* 標頭檔中定義的其中一個 NTDDI 版本常數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-197">The **TargetOsVersion** member can be one of the NTDDI version constants defined in the *Sdkddkver.h* header file.</span></span>
<span data-ttu-id="2cd88-198">**TargetOsVersion** 成員的一些可能值如下：</span><span class="sxs-lookup"><span data-stu-id="2cd88-198">Some of the possible values for the **TargetOsVersion** member are as follows:</span></span>

| <span data-ttu-id="2cd88-199">詞彙</span><span class="sxs-lookup"><span data-stu-id="2cd88-199">Term</span></span> | <span data-ttu-id="2cd88-200">描述</span><span class="sxs-lookup"><span data-stu-id="2cd88-200">Description</span></span> |
|------|-------------|
| <span data-ttu-id="2cd88-201">NTDDI \_ LONGHORN</span><span class="sxs-lookup"><span data-stu-id="2cd88-201">NTDDI\_LONGHORN</span></span> | <span data-ttu-id="2cd88-202">目標行為是 Windows Vista 的預設行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-202">The target behavior is the default for Windows Vista.</span></span> |
| <span data-ttu-id="2cd88-203">NTDDI \_ WS03</span><span class="sxs-lookup"><span data-stu-id="2cd88-203">NTDDI\_WS03</span></span> | <span data-ttu-id="2cd88-204">目標行為是 Windows Server 2003 的預設行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-204">The target behavior is the default for Windows Server 2003.</span></span> |
| <span data-ttu-id="2cd88-205">NTDDI \_ >TEST-WINXP</span><span class="sxs-lookup"><span data-stu-id="2cd88-205">NTDDI\_WINXP</span></span> | <span data-ttu-id="2cd88-206">目標行為是 Windows XP 的預設行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-206">The target behavior is the default for Windows XP.</span></span> |
| <span data-ttu-id="2cd88-207">NTDDI \_ WIN2K</span><span class="sxs-lookup"><span data-stu-id="2cd88-207">NTDDI\_WIN2K</span></span> | <span data-ttu-id="2cd88-208">目標行為是 Windows 2000 的預設行為。</span><span class="sxs-lookup"><span data-stu-id="2cd88-208">The target behavior is the default for Windows 2000.</span></span> |

<span data-ttu-id="2cd88-209">**TargetOsVersion** 成員的主要影響是此成員是否設定為等於或大於 **NTDDI \_ LONGHORN** 的值。</span><span class="sxs-lookup"><span data-stu-id="2cd88-209">The primary impact of the **TargetOsVersion** member is whether this member is set to a value equal or greater than **NTDDI\_LONGHORN**.</span></span>

<span data-ttu-id="2cd88-210">TCP 效能不僅取決於傳輸速率本身，而是取決於傳輸速率和來回延遲時間的乘積。</span><span class="sxs-lookup"><span data-stu-id="2cd88-210">TCP performance depends not only on the transfer rate itself, but rather on the product of the transfer rate and the round-trip delay time.</span></span>
<span data-ttu-id="2cd88-211">這個頻寬延遲乘積會測量「填滿管道」的資料量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-211">This bandwidth-delay product measures the amount of data that would "fill the pipe".</span></span>
<span data-ttu-id="2cd88-212">此頻寬延遲產品是傳送者和接收者所需的緩衝區空間，可在路徑上取得 TCP 連接的最大輸送量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-212">This bandwidth-delay product is the buffer space required at sender and receiver to obtain maximum throughput on the TCP connection over the path.</span></span>
<span data-ttu-id="2cd88-213">此緩衝區空間代表 TCP 必須處理才能讓管線保持完整的未認可資料量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-213">This buffer space represents the amount of unacknowledged data that TCP must handle in order to keep the pipeline full.</span></span>
<span data-ttu-id="2cd88-214">當頻寬延遲乘積很大時，就會發生 TCP 效能問題。</span><span class="sxs-lookup"><span data-stu-id="2cd88-214">TCP performance problems arise when the bandwidth-delay product is large.</span></span>
<span data-ttu-id="2cd88-215">在這些情況下運作的網路路徑通常稱為「長的 fat 管道」。</span><span class="sxs-lookup"><span data-stu-id="2cd88-215">A network path operating under these conditions is often called a "long, fat pipe".</span></span>
<span data-ttu-id="2cd88-216">範例包括高容量封包附屬連結、高速無線連結，以及遠距離的地面光纖連結。</span><span class="sxs-lookup"><span data-stu-id="2cd88-216">Examples include high-capacity packet satellite links, high-speed wireless links, and terrestrial fiber-optical links over long distances.</span></span>

<span data-ttu-id="2cd88-217">TCP 標頭會使用16位資料欄位 (TCP 封包標頭中的 [視窗] 欄位) 將接收視窗大小報告給傳送者。</span><span class="sxs-lookup"><span data-stu-id="2cd88-217">The TCP header uses a 16-bit data field (the Window field in the TCP packet header) to report the receive window size to the sender.</span></span>
<span data-ttu-id="2cd88-218">因此，可以使用的最大視窗為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-218">Therefore, the largest window that can be used is 65,535 bytes.</span></span>
<span data-ttu-id="2cd88-219">為了規避這項限制，已為高效能 TCP 新增 tcp 延伸模組選項，以允許超過65535個位元組的 windows。</span><span class="sxs-lookup"><span data-stu-id="2cd88-219">To circumvent this limitation a TCP extension option, TCP Window Scale, was added for high-performance TCP to allow windows larger than 65,535 bytes.</span></span>
<span data-ttu-id="2cd88-220">「TCP 視窗調整」選項 (WSopt) 是在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1323 中定義。</span><span class="sxs-lookup"><span data-stu-id="2cd88-220">The TCP Window Scale option (WSopt) is defined in RFC 1323 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="2cd88-221">WSopt 擴充功能會使用單一位元組的對數縮放比例，將 TCP 視窗的定義擴充至32位，以擴充 TCP 標頭中的16位視窗欄位。</span><span class="sxs-lookup"><span data-stu-id="2cd88-221">The WSopt extension expands the definition of the TCP window to 32 bits using a one-byte logarithmic scale factor to extend the 16-bit Window field in the TCP header.</span></span>
<span data-ttu-id="2cd88-222">WSopt 延伸模組會定義隱含的縮放比例 (2 到某些電源) ，用來將 TCP 標頭中找到的視窗大小值乘以以取得真正的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-222">The WSopt extension defines an implicit scale factor (2 to some power), which is used to multiply the window size value found in a TCP header to obtain the true window size.</span></span>
<span data-ttu-id="2cd88-223">因此，視窗比例因數8會導致真正的視窗大小等於 TCP 標頭中的 [視窗] 欄位值乘以 2 ^ 8 或256。</span><span class="sxs-lookup"><span data-stu-id="2cd88-223">So a window scale factor of 8 would result in a true window size equal to the value in the Window field in the TCP header multiplied by 2^8 or 256.</span></span>
<span data-ttu-id="2cd88-224">因此，如果 TCP 標頭中的視窗欄位設定為65535個位元組的最大值，且 WSopt 縮放比例已協商為8的值，則真正的視窗大小會是16776960個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-224">So if the Window field in the TCP header was set to the maximum value of 65,535 bytes and the WSopt scale factor was negotiated to a value of 8, the true window size would be 16,776,960 bytes.</span></span>

<span data-ttu-id="2cd88-225">真正的接收視窗大小，因此，縮放比例取決於接收緩衝區的最大空間。</span><span class="sxs-lookup"><span data-stu-id="2cd88-225">The true receive window size and therefore the scale factor is determined by the maximum receive buffer space.</span></span>
<span data-ttu-id="2cd88-226">此最大緩衝區空間是 TCP 寄件者在等待通知之前，允許 TCP 寄件者傳送的資料量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-226">This maximum buffer space is the amount of data that a TCP receiver allows a TCP sender to send before having to wait for an acknowledgement.</span></span>
<span data-ttu-id="2cd88-227">建立連線之後，會在每個 TCP 區段中通告接收視窗大小， (TCP 標頭中的視窗欄位) 。</span><span class="sxs-lookup"><span data-stu-id="2cd88-227">After the connection is established, the receive window size is advertised in each TCP segment (the Window field in the TCP header).</span></span>
<span data-ttu-id="2cd88-228">通告傳送者可以傳送的最大資料量是接收端流程式控制制機制，可防止寄件者傳送接收者無法儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="2cd88-228">Advertising the maximum amount of data that the sender can send is a receiver-side flow control mechanism that prevents the sender from sending data that the receiver cannot store.</span></span>
<span data-ttu-id="2cd88-229">傳送主機只能在等待通知和接收視窗大小更新之前，傳送接收端所通告的資料量上限。</span><span class="sxs-lookup"><span data-stu-id="2cd88-229">A sending host can only send the maximum amount of data advertised by the receiver before waiting for an acknowledgment and a receive window size update.</span></span>

<span data-ttu-id="2cd88-230">在 Windows Server 2003 和 Windows XP 上，根據傳送介面的連結速度，最大的接收緩衝區空間（代表 TCP/IP 堆疊的接收視窗大小）有預設值。</span><span class="sxs-lookup"><span data-stu-id="2cd88-230">On Windows Server 2003 and Windows XP, the maximum receive buffer space which represents the receive window size for the TCP/IP stack has a default value based on the link speed of the sending interface.</span></span>
<span data-ttu-id="2cd88-231">實際的值會自動調整為偶數的區段大小上限， (MSS) 在 TCP 連線建立期間協商。</span><span class="sxs-lookup"><span data-stu-id="2cd88-231">The actual value automatically adjusts to even increments of the maximum segment size (MSS) negotiated during TCP connection establishment.</span></span>
<span data-ttu-id="2cd88-232">因此，若是 10 Mbit/sec 的連結，預設的接收視窗大小通常會設定為16K 位元組，而在 100 MBit/sec 連結上，預設的接收視窗大小會設為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-232">So for a 10 Mbit/sec link, the default receive window size would normally be set to 16K bytes, while on a 100 MBit/sec link the default receive window size would be set to 65,535 bytes.</span></span>

<span data-ttu-id="2cd88-233">在 Windows Server 2003 和 Windows XP 上，您可以使用特定介面或整個系統上的下列登錄值，手動設定 TCP/IP 堆疊的真正最大接收視窗大小：</span><span class="sxs-lookup"><span data-stu-id="2cd88-233">On Windows Server 2003 and Windows XP, the true maximum receive window size for the TCP/IP stack can be manually configured using the following registry values on a specific interface or for the entire system:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

<span data-ttu-id="2cd88-234">當 (使用 WSopt 擴充功能時， **TCPWindowSize** 的登錄值最多可設為65535個1073741823位元組（最大值為），) 支援最大的縮放因數4。</span><span class="sxs-lookup"><span data-stu-id="2cd88-234">The registry value for **TCPWindowSize** can be set to a maximum of 65,535 bytes when not using the WSopt extension or a maximum of 1,073,741,823 bytes when the WSopt extension is used (a maximum scale factor of 4 is supported).</span></span>
<span data-ttu-id="2cd88-235">如果沒有視窗調整，應用程式只能達到大約每秒 5 mb 的輸送量 (Mbps) 在具有100毫秒的往返時間 (RTT) ，不論路徑頻寬為何。</span><span class="sxs-lookup"><span data-stu-id="2cd88-235">Without window scaling, an application can only achieve a throughput of approximately 5 megabits per second (Mbps) on a path with a 100 millisecond round-trip time (RTT), regardless of the path bandwidth.</span></span>
<span data-ttu-id="2cd88-236">此輸送量可以調整為超過每秒 gigabit (Gbps) 搭配視窗調整，這可讓 TCP 在建立連線時，協調視窗大小的縮放係數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-236">This throughput can be scaled to over a gigabit per second (Gbps) with window scaling, which allows TCP to negotiate the scaling factor for the window size during connection establishment.</span></span>

<span data-ttu-id="2cd88-237">在 Windows Server 2003 和 Windows XP 上，您可以藉由設定下列登錄值來啟用 WSopt 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2cd88-237">On Windows Server 2003 and Windows XP, the WSopt extension can be enabled by setting the following registry value.</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

<span data-ttu-id="2cd88-238">**Tcp1323Opts** 登錄值是 **DWORD** 編碼的，因此當設定位0時，會啟用 TCP WSopt 延伸。</span><span class="sxs-lookup"><span data-stu-id="2cd88-238">The **Tcp1323Opts** registry value is a **DWORD** encoded such that when bit 0 is set, TCP WSopt extension is enabled.</span></span>
<span data-ttu-id="2cd88-239">當設定位1時，會啟用在 RFC 1323 中定義 (TSopt) 的 TCP 時間戳記選項。</span><span class="sxs-lookup"><span data-stu-id="2cd88-239">When bit 1 is set, the TCP Timestamp option (TSopt) defined in RFC 1323 is enabled.</span></span>
<span data-ttu-id="2cd88-240">因此，1或3的值會啟用 WSopt 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-240">So a value of either 1 or 3 will enable the WSopt extension.</span></span>

<span data-ttu-id="2cd88-241">在 Windows Server 2003 和 Windows XP 上，預設為不會建立 TCPWindowSize 和 Tcp1323Opts 登錄值。</span><span class="sxs-lookup"><span data-stu-id="2cd88-241">On Windows Server 2003 and Windows XP, the default is that the TCPWindowSize and the Tcp1323Opts registry values are not created.</span></span>
<span data-ttu-id="2cd88-242">因此，預設值是停用 WSopt 延伸模組，而且 TCP 接收視窗大小是由系統設定為最大值，最大值為65535個位元組（以連結速度為基礎）。</span><span class="sxs-lookup"><span data-stu-id="2cd88-242">So the default is that the WSopt extension is disabled and the TCP receive window size is set by the system to maximum value of up to 65,535 bytes based on the link speed.</span></span>
<span data-ttu-id="2cd88-243">藉由設定 Tcp1323Opts 登錄值，在 Windows Server 2003 和 Windows XP 上啟用視窗調整功能時，仍然只會在傳送者和接收者將 [同步處理 (SYN) 區段中包含 [TCP 視窗調整] 選項，以協調視窗縮放比例時使用 TCP 連接。</span><span class="sxs-lookup"><span data-stu-id="2cd88-243">When window scaling is enabled on Windows Server 2003 and Windows XP by setting the Tcp1323Opts registry value, window scaling on a TCP connection is still only used when both the sender and receiver include a TCP window scale option in the synchronize (SYN) segment sent to each other to negotiate a window scale factor.</span></span>
<span data-ttu-id="2cd88-244">在連接上使用視窗調整時，TCP 標頭中的 [視窗] 欄位會設為65535個位元組，而 [視窗縮放比例] 則是用來在建立連接時，以協調的視窗縮放因數來調整真正的接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-244">When window scaling is used on a connection, the Window field in the TCP header is set to 65,535 bytes and the window scale factor is used to adjust the true receive window size upward by the window scale factor negotiated when the connection is established.</span></span>

<span data-ttu-id="2cd88-245">應用程式可以使用 **\_ RCVBUF** 通訊端選項來指定連接的 TCP 接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-245">An application can specify the TCP receive window size for a connection by using the **SO\_RCVBUF** socket option.</span></span>
<span data-ttu-id="2cd88-246">您可以使用 **\_ RCVBUF**，隨時增加通訊端的 TCP 接收視窗大小，但只能在建立連線之前降低。</span><span class="sxs-lookup"><span data-stu-id="2cd88-246">The TCP receive window size for a socket can be increased at any time using **SO\_RCVBUF**, but it can only be decreased prior to establishing a connection.</span></span>
<span data-ttu-id="2cd88-247">若要使用視窗調整，應用程式必須在建立連線之前，使用 **\_ RCVBUF** 通訊端選項來指定大於65535位元組的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-247">In order to use window scaling, an application must specify a window size larger than 65,535 bytes when using the **SO\_RCVBUF** socket option before the connection is established.</span></span>

<span data-ttu-id="2cd88-248">TCP 接收視窗大小的理想值通常很難判斷。</span><span class="sxs-lookup"><span data-stu-id="2cd88-248">The ideal value for the TCP receive window size is often difficult to determine.</span></span>
<span data-ttu-id="2cd88-249">為了填滿傳送者與接收者之間的網路容量，接收視窗大小應設定為連線的頻寬延遲產品，也就是頻寬乘以來回時間。</span><span class="sxs-lookup"><span data-stu-id="2cd88-249">In order to fill the capacity of the network between the sender and receiver, the receive window size should be set to the bandwidth-delay product for the connection, which is the bandwidth multiplied by the round-trip time.</span></span>
<span data-ttu-id="2cd88-250">即使應用程式可以正確地判斷頻寬延遲的產品，仍不知道接收應用程式從傳入資料緩衝區取出資料的速度， (應用程式取得速率) 。</span><span class="sxs-lookup"><span data-stu-id="2cd88-250">Even if an application can correctly determine the bandwidth-delay product, it is still not known how quickly the receiving application will retrieve data from the incoming data buffer (the application retrieve rate).</span></span>
<span data-ttu-id="2cd88-251">雖然支援 TCP 視窗調整，但 Windows Server 2003 和 Windows XP 中的接收視窗大小上限仍然會限制輸送量，因為它是所有 TCP 連線的固定大小上限 (除非使用 **\_ RCVBUF**) 為每個應用程式指定，這樣可以增強某些連線的輸送量，並降低其他連線的輸送量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-251">Despite the support for TCP window scaling, the maximum receive window size in Windows Server 2003 and Windows XP can still limit throughput because it is a fixed maximum size for all TCP connections (unless specified per application using **SO\_RCVBUF**), which can enhance throughput for some connections and decrease throughput for others.</span></span>
<span data-ttu-id="2cd88-252">此外，TCP 連線的固定接收視窗大小上限，不會隨著網路狀況的變更而改變。</span><span class="sxs-lookup"><span data-stu-id="2cd88-252">Additionally, the fixed maximum receive window size for a TCP connection does not vary with changing network conditions.</span></span>

<span data-ttu-id="2cd88-253">為了解決根據網路目前狀況正確判斷 TCP 連接之接收視窗大小上限值的問題，Windows Vista 中的 TCP/IP 堆疊支援「接收視窗自動微調」功能。</span><span class="sxs-lookup"><span data-stu-id="2cd88-253">To solve the problem of correctly determining the value of the maximum receive window size for a TCP connection based on the current conditions of the network, the TCP/IP stack in Windows Vista supports a receive window auto-tuning feature.</span></span>
<span data-ttu-id="2cd88-254">啟用這項功能時，「接收視窗自動微調」會藉由測量頻寬延遲產品和應用程式取出率，持續判斷最佳的真正接收視窗大小，並根據變更的網路狀況調整真正的最大接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-254">When this feature is enabled, receive window auto-tuning continually determines the optimal true receive window size by measuring the bandwidth-delay product and the application retrieve rate, and adjusts the true maximum receive window size based on changing network conditions.</span></span>
<span data-ttu-id="2cd88-255">依預設，[接收視窗自動調整] 會啟用 TCP WSopt 延伸模組，為真正的視窗大小允許最多16776960個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-255">Receive window auto-tuning enables the TCP WSopt extension by default, allowing up to 16,776,960 bytes for the true window size.</span></span>
<span data-ttu-id="2cd88-256">當資料在連線上流動時，TCP/IP 堆疊會監視連線、測量連接目前的頻寬延遲產品和應用程式接收率，以及調整實際的接收視窗大小以優化輸送量。</span><span class="sxs-lookup"><span data-stu-id="2cd88-256">As the data flows over the connection, the TCP/IP stack monitors the connection, measures the current bandwidth-delay product for the connection and the application receive rate, and adjusts the actual receive window size to optimize throughput.</span></span>
<span data-ttu-id="2cd88-257">TCP/IP 堆疊會根據網路條件變更 TCP 標頭中的 [視窗] 欄位的值，因為 WSopt 縮放比例是在第一次建立連接時固定的。</span><span class="sxs-lookup"><span data-stu-id="2cd88-257">The TCP/IP stack changes the value of the Window field in the TCP header based on network conditions, since the WSopt scale factor is fixed when the connection is first established.</span></span>

<span data-ttu-id="2cd88-258">Windows Vista 中的 TCP/IP 堆疊不再使用 **TCPWindowSize** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="2cd88-258">The TCP/IP stack in Windows Vista no longer uses the **TCPWindowSize** registry values.</span></span>
<span data-ttu-id="2cd88-259">TCP 對等互連之間有更高的輸送量，則會在資料傳輸期間增加網路頻寬的使用率。</span><span class="sxs-lookup"><span data-stu-id="2cd88-259">With better throughput between TCP peers, the utilization of network bandwidth increases during data transfer.</span></span>
<span data-ttu-id="2cd88-260">如果所有應用程式都經過優化以接收 TCP 資料，則網路的整體使用率可能會大幅增加，而使用服務品質 (QoS) 更重要的是在運作或接近容量的網路上。</span><span class="sxs-lookup"><span data-stu-id="2cd88-260">If all the applications are optimized to receive TCP data, then the overall utilization of the network can increase substantially, making the use of Quality of Service (QoS) more important on networks that are operating at or near capacity.</span></span>

<span data-ttu-id="2cd88-261">當您未使用 **WsaBehaviorReceiveBuffering** 指定 **SIO \_ SET \_ 相容性 \_ 模式** 時，Windows Vista 上的 [接收緩衝處理] 的預設行為是，在建立連線之後，不允許使用 [允許 **\_ RCVBUF** 通訊端] 選項來降低接收視窗大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-261">The default behavior on Windows Vista for receive buffering when **SIO\_SET\_COMPATIBILITY\_MODE** is not specified using **WsaBehaviorReceiveBuffering** is that no receive window size reductions using **SO\_RCVBUF** socket option are allowed after a connection is established.</span></span>

<span data-ttu-id="2cd88-262">當您未使用 **WsaBehaviorAutoTuning** 指定 **SIO \_ SET \_ 相容性 \_ 模式** 時，Windows Vista 上的預設行為會自動調整，因為堆疊將會使用視窗比例因數8來自動調整視窗。</span><span class="sxs-lookup"><span data-stu-id="2cd88-262">The default behavior on Windows Vista for auto-tuning when **SIO\_SET\_COMPATIBILITY\_MODE** is not specified using **WsaBehaviorAutoTuning** is that the stack will do receive window auto-tuning using a window scale factor of 8.</span></span>
<span data-ttu-id="2cd88-263">請注意，如果應用程式使用 **\_ RCVBUF** 通訊端選項設定有效的接收視窗大小，堆疊將會使用指定的大小，且將停用 [視窗接收自動調整]。</span><span class="sxs-lookup"><span data-stu-id="2cd88-263">Note that if an application sets a valid receive window size with the **SO\_RCVBUF** socket option, the stack will use the size specified and window receive auto-tuning will disabled.</span></span>
<span data-ttu-id="2cd88-264">您也可以使用下列命令，完全停用 Windows 自動優化功能， `netsh interface tcp set global autotuninglevel=disabled` 在這種情況下，指定 **WsaBehaviorAutoTuning** 不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="2cd88-264">Windows autotuning may also be disabled completely using the following command, `netsh interface tcp set global autotuninglevel=disabled`, in which case specifying **WsaBehaviorAutoTuning** will have no affect.</span></span>
<span data-ttu-id="2cd88-265">您也可以根據 Windows Server 2008 上設定的群組原則來停用視窗接收自動優化。</span><span class="sxs-lookup"><span data-stu-id="2cd88-265">Window receive autotuning can also be disabled based on group policy set on Windows Server 2008.</span></span>

<span data-ttu-id="2cd88-266">某些網際網路閘道裝置和防火牆無法正確支援使用 WSopt 擴充功能和 Windows 縮放比例之 TCP 連線的資料流程時，Windows Vista 上需要 **WsaBehaviorAutoTuning** 選項。</span><span class="sxs-lookup"><span data-stu-id="2cd88-266">The **WsaBehaviorAutoTuning** option is needed on Windows Vista for some Internet gateway devices and firewalls that do not correctly support data flows for TCP connections that use the WSopt extension and a windows scale factor.</span></span>
<span data-ttu-id="2cd88-267">在 Windows Vista 上，接收器預設會將視窗縮放比例（最大值為16776960個位元組的視窗大小）協調為8。</span><span class="sxs-lookup"><span data-stu-id="2cd88-267">On Windows Vista, a receiver by default negotiates a window scale factor of 8 for a maximum true window size of 16,776,960 bytes.</span></span>
<span data-ttu-id="2cd88-268">當資料開始在快速連結上流動時，Windows 一開始會先將 TCP 標頭的視窗欄位設定為256，並在 TCP 選項中將視窗比例因數設定為8，以在 [TCP 選項 (256 \* 2 ^ 8 = 64KB) 的情況下，以 64 Kb 的真正視窗大小開始。</span><span class="sxs-lookup"><span data-stu-id="2cd88-268">When data begins to flow on a fast link, Windows initially starts with a 64 Kilobyte true window size by setting the Window field of the TCP header to 256 and setting the window scale factor to 8 in the TCP options (256\*2^8=64KB).</span></span>
<span data-ttu-id="2cd88-269">某些網際網路閘道裝置和防火牆會忽略視窗調整比例，並只查看指定為256的 TCP 標頭中的 [通告的視窗] 欄位，然後針對包含超過256個位元組之 TCP 資料的連接卸載連入封包。</span><span class="sxs-lookup"><span data-stu-id="2cd88-269">Some Internet gateway devices and firewalls ignore the window scale factor and only look at the advertised Window field in the TCP header specified as 256, and drop incoming packets for the connection that contain more than 256 bytes of TCP data.</span></span>
<span data-ttu-id="2cd88-270">若要支援 TCP 接收視窗調整，閘道裝置或防火牆必須監視 TCP 交握，並在 TCP 連線資料中追蹤已協商的視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-270">To support TCP receive window scaling, a gateway device or firewall must monitor the TCP handshake and track the negotiated window scale factor as part of the TCP connection data.</span></span>
<span data-ttu-id="2cd88-271">此外，其他平臺上的某些應用程式和 TCP 堆疊會忽略 TCP WSopt 延伸模組和視窗調整係數。</span><span class="sxs-lookup"><span data-stu-id="2cd88-271">Also some applications and TCP stack implementations on other platforms ignore the TCP WSopt extension and the window scaling factor.</span></span>
<span data-ttu-id="2cd88-272">因此傳送資料的遠端主機可能會以 TCP 標頭的 [時間範圍] 欄位中通告的速率傳送資料 (256 個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="2cd88-272">So the remote host sending the data may send data at the rate advertised in the Window field of the TCP header (256 bytes).</span></span>
<span data-ttu-id="2cd88-273">這可能會導致接收端的資料接收速度非常緩慢。</span><span class="sxs-lookup"><span data-stu-id="2cd88-273">This can result in data being received very slowly by the receiver.</span></span>

<span data-ttu-id="2cd88-274">將 **BehaviorId** 成員設定為 **WsaBehaviorAutoTuning** ，並將 **TargetOsVersion** 到 Windows Vista，將視窗縮放比例縮減為2，因此 TCP 標頭中的 [視窗] 欄位一開始會設定為16384個位元組，而 [視窗縮放比例] 會設定為 [2]，表示初始真正的視窗接收大小為64k 個位元組。</span><span class="sxs-lookup"><span data-stu-id="2cd88-274">Setting the **BehaviorId** member to **WsaBehaviorAutoTuning** and the **TargetOsVersion** to Windows Vista reduces the window scale factor to 2, so the Window field in the TCP header is initially set to 16,384 bytes and the window scale factor is set to 2 for an initial true window receive size of 64K bytes.</span></span>
<span data-ttu-id="2cd88-275">然後，視窗自動調整功能可將 TCP 標頭中的視窗欄位設定為65535個位元組，以增加最多262140個位元組的真正視窗接收大小。</span><span class="sxs-lookup"><span data-stu-id="2cd88-275">The window auto-tuning feature can then increase the true window receive size up to 262,140 bytes by setting the Window field in the TCP header to 65,535 bytes.</span></span>
<span data-ttu-id="2cd88-276">一旦建立通訊端之後，應用程式應該立即設定 **SIO \_ set \_ 相容性 \_ 模式** 的 IOCTL，因為在傳送 SYN 之後，這個選項並不合理或不適用。</span><span class="sxs-lookup"><span data-stu-id="2cd88-276">An application should set the **SIO\_SET\_COMPATIBILITY\_MODE** IOCTL as soon as a socket is created, since this option doesn't make sense or apply after a SYN is sent.</span></span>
<span data-ttu-id="2cd88-277">設定此選項的影響與下列命令相同： `netsh interface tcp set global autotuninglevel=highlyrestricted`</span><span class="sxs-lookup"><span data-stu-id="2cd88-277">Setting this option has the same impact as the following command: `netsh interface tcp set global autotuninglevel=highlyrestricted`</span></span>

<span data-ttu-id="2cd88-278">請注意， *Mswsockdef .h* 標頭檔會自動包含在 *Mswsock .h* 或 *Netiodef* 中，而且不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="2cd88-278">Note that the *Mswsockdef.h* header file is automatically included in *Mswsock.h* or *Netiodef.h*, and should not be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cd88-279">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cd88-279">See also</span></span>

[<span data-ttu-id="2cd88-280">**插座**</span><span class="sxs-lookup"><span data-stu-id="2cd88-280">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2cd88-281">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="2cd88-281">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="2cd88-282">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="2cd88-282">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2cd88-283">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="2cd88-283">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2cd88-284">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="2cd88-284">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2cd88-285">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="2cd88-285">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2cd88-286">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="2cd88-286">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

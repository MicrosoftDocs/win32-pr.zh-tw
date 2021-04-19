---
description: 控制項程式碼會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988915"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="169b0-103">SIO_ADDRESS_LIST_QUERY 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="169b0-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="169b0-104">Description</span><span class="sxs-lookup"><span data-stu-id="169b0-104">Description</span></span>

<span data-ttu-id="169b0-105">**SIO \_ ADDRESS \_ LIST \_ QUERY** control code 會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。</span><span class="sxs-lookup"><span data-stu-id="169b0-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="169b0-106">地址清單會根據地址系列而有所不同，而某些位址會從清單中排除。</span><span class="sxs-lookup"><span data-stu-id="169b0-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="169b0-107">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="169b0-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="169b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="169b0-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="169b0-109">s</span><span class="sxs-lookup"><span data-stu-id="169b0-109">s</span></span>

<span data-ttu-id="169b0-110">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="169b0-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="169b0-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="169b0-111">dwIoControlCode</span></span>

<span data-ttu-id="169b0-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="169b0-112">The control code for the operation.</span></span>
<span data-ttu-id="169b0-113">使用 **SIO \_ 位址 \_ 清單 \_ 查詢** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="169b0-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="169b0-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="169b0-114">lpvInBuffer</span></span>

<span data-ttu-id="169b0-115">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="169b0-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="169b0-116">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="169b0-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="169b0-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="169b0-117">cbInBuffer</span></span>

<span data-ttu-id="169b0-118">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="169b0-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="169b0-119">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="169b0-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="169b0-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="169b0-120">lpvOutBuffer</span></span>

<span data-ttu-id="169b0-121">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="169b0-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="169b0-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="169b0-122">cbOutBuffer</span></span>

<span data-ttu-id="169b0-123">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="169b0-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="169b0-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="169b0-124">lpcbBytesReturned</span></span>

<span data-ttu-id="169b0-125">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="169b0-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="169b0-126">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="169b0-126">lpvOverlapped</span></span>

<span data-ttu-id="169b0-127">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="169b0-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="169b0-128">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="169b0-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="169b0-129">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="169b0-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="169b0-130">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="169b0-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="169b0-131">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="169b0-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="169b0-132">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="169b0-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="169b0-133">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="169b0-133">lpCompletionRoutine</span></span>

<span data-ttu-id="169b0-134">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="169b0-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="169b0-135">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="169b0-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="169b0-136">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="169b0-136">lpThreadId</span></span>

<span data-ttu-id="169b0-137">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="169b0-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="169b0-138">在 [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="169b0-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="169b0-139">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="169b0-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="169b0-140">lpErrno</span><span class="sxs-lookup"><span data-stu-id="169b0-140">lpErrno</span></span>

<span data-ttu-id="169b0-141">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="169b0-141">A pointer to the error code.</span></span>

<span data-ttu-id="169b0-142">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="169b0-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="169b0-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="169b0-143">Return value</span></span>

<span data-ttu-id="169b0-144">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="169b0-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="169b0-145">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="169b0-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="169b0-146">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="169b0-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="169b0-147">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="169b0-147">Error code</span></span> | <span data-ttu-id="169b0-148">意義</span><span class="sxs-lookup"><span data-stu-id="169b0-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="169b0-149">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="169b0-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="169b0-150">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="169b0-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="169b0-151">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="169b0-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="169b0-152">因為通訊端關閉或 **SIO \_ FLUSH** IOCTL 命令的執行，重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="169b0-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="169b0-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="169b0-153">**WSAEFAULT**</span></span> | <span data-ttu-id="169b0-154">*LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="169b0-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="169b0-155">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="169b0-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="169b0-156">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="169b0-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="169b0-157">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="169b0-157">**WSAEINTR**</span></span> | <span data-ttu-id="169b0-158">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="169b0-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="169b0-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="169b0-159">**WSAEINVAL**</span></span> | <span data-ttu-id="169b0-160">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="169b0-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="169b0-161">如果 *cbInBuffer* 參數未設定為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="169b0-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="169b0-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="169b0-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="169b0-163">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="169b0-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="169b0-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="169b0-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="169b0-165">沒有可用的緩衝區空間。</span><span class="sxs-lookup"><span data-stu-id="169b0-165">No buffer space available.</span></span> |
| <span data-ttu-id="169b0-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="169b0-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="169b0-167">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="169b0-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="169b0-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="169b0-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="169b0-169">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="169b0-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="169b0-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="169b0-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="169b0-171">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="169b0-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="169b0-172">如果傳輸提供者不支援 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="169b0-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="169b0-173">備註</span><span class="sxs-lookup"><span data-stu-id="169b0-173">Remarks</span></span>

<span data-ttu-id="169b0-174">在 Windows 2000 和更新版本的作業系統上，支援 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL。</span><span class="sxs-lookup"><span data-stu-id="169b0-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="169b0-175">**SIO \_ ADDRESS \_ LIST \_ QUERY** control code 會取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。</span><span class="sxs-lookup"><span data-stu-id="169b0-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="169b0-176">地址清單會根據地址系列而有所不同。</span><span class="sxs-lookup"><span data-stu-id="169b0-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="169b0-177">若為 AF \_ INET6 位址系列，則會傳回除了下列以外的所有位址：</span><span class="sxs-lookup"><span data-stu-id="169b0-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="169b0-178">未 IpDadStatePreferred 重複位址偵測 (DAD) 狀態的任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="169b0-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="169b0-179">在介面類別型為的介面上，任何範圍層級低於 ScopeLevelSubnet 的 IP 位址會 **是 \_ 類型 \_ 軟體 \_ 回送**。</span><span class="sxs-lookup"><span data-stu-id="169b0-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="169b0-180">這表示 **如果排除 \_ 型別 \_ 軟體 \_ 回送** 類型，則在介面上的 (fe80： \* ) 和回送 (：： 1) 位址，但如果這些位址位於不同類型的介面上，則不是。</span><span class="sxs-lookup"><span data-stu-id="169b0-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="169b0-181">若為 **AF \_ INET** 位址系列，則會傳回除了下列以外的所有位址：</span><span class="sxs-lookup"><span data-stu-id="169b0-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="169b0-182">未 IpDadStatePreferred 重複位址偵測 (DAD) 狀態的任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="169b0-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="169b0-183">介面類別型為的介面上的任何 IP 位址， **如果 \_ 類型 \_ 軟體 \_ 回送** 和連結是本機的，則為。</span><span class="sxs-lookup"><span data-stu-id="169b0-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="169b0-184">這表示連結-本機 (169.254。*) 和回送 (127。\*\*\*如果排除 \_ 型別 \_ 軟體 \_ 回送*\* 類型，則在介面上) 位址，但如果這些位址位於不同類型的介面上，則不是。</span><span class="sxs-lookup"><span data-stu-id="169b0-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="169b0-185">如需有關 DAD 狀態的詳細資訊，請參閱有關 [**MIB \_ UNICASTIPADDRESS 資料 \_ 列**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)結構上 ip [**\_ DAD \_ 狀態**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)列舉和 [**IP \_ 配接器 \_ 單播 \_ 位址**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)結構和 mib 檔的 ip 協助程式檔。</span><span class="sxs-lookup"><span data-stu-id="169b0-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="169b0-186">如需介面類別型的詳細資訊，請參閱 ip [**\_ 配接器 \_ 位址**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) 結構上的 ip 協助程式檔和 [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) 函式，以及有關 [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) 結構的 MIB 檔。</span><span class="sxs-lookup"><span data-stu-id="169b0-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="169b0-187">如需範圍層級的詳細資訊，請參閱 [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) 結構和 [**範圍 \_ 層級**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) 列舉的 IP 協助程式檔。</span><span class="sxs-lookup"><span data-stu-id="169b0-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="169b0-188">*LpvOutBuffer* 參數所指向之輸出緩衝區中傳回的清單是 [**通訊端 \_ 位址 \_ 清單**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)結構的形式。</span><span class="sxs-lookup"><span data-stu-id="169b0-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="169b0-189">如果 *lpvOutBuffer* 參數中指定的輸出緩衝區不夠大，無法包含地址清單，則會傳回 **通訊端 \_ 錯誤** ，因為這個 IOCTL 的結果和 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)。</span><span class="sxs-lookup"><span data-stu-id="169b0-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="169b0-190">在此情況下，輸出緩衝區所需的大小（以位元組為單位）會在 *lpcbBytesReturned* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="169b0-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="169b0-191">請注意，如果 *lpvInBuffer*、 *lpvOutBuffer* 或 *lpcbBytesReturned* 參數未完全包含在使用者位址空間的有效部分中，也會傳回 [WSAEFAULT](windows-sockets-error-codes-2.md)錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="169b0-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="169b0-192">**SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL 通常會以同步方式呼叫，並將 *lpvOverlapped* 參數設定為 **Null**，因為會立即傳回地址清單。</span><span class="sxs-lookup"><span data-stu-id="169b0-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="169b0-193">**注意**  在 Windows 隨插即用環境中，可以動態新增和移除位址。</span><span class="sxs-lookup"><span data-stu-id="169b0-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="169b0-194">因此，應用程式無法依賴 **SIO \_ 位址 \_ 清單 \_ 查詢** 所傳回的資訊來持續存在。</span><span class="sxs-lookup"><span data-stu-id="169b0-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="169b0-195">應用程式可以透過 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 來登入位址變更通知，以透過重迭的 I/o 或 **FD \_ 通訊 \_ 清單 \_ 變更** 事件提供通知。</span><span class="sxs-lookup"><span data-stu-id="169b0-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="169b0-196">下列動作順序可以用來保證應用程式一律具有目前的通訊清單資訊：</span><span class="sxs-lookup"><span data-stu-id="169b0-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="169b0-197">發出 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL</span><span class="sxs-lookup"><span data-stu-id="169b0-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="169b0-198">發出 **SIO \_ 位址 \_ 清單 \_ 查詢** IOCTL</span><span class="sxs-lookup"><span data-stu-id="169b0-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="169b0-199">只要 **SIO \_ 位址 \_ 清單 \_ 變更** IOCTL 呼叫，就會通知應用程式地址清單變更 (透過重迭的 I/o 或) 的 **FD \_ 通訊 \_ 清單 \_ 變更** 事件，就應該重複執行一系列的動作。</span><span class="sxs-lookup"><span data-stu-id="169b0-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="169b0-200">在 Windows Vista （含）以後版本的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已變更，且 **SIO \_ ADDRESS \_ LIST \_ 查詢** 控制項程式碼定義于 *Ws2def .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="169b0-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="169b0-201">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="169b0-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="169b0-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="169b0-202">See also</span></span>

[<span data-ttu-id="169b0-203">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="169b0-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="169b0-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="169b0-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="169b0-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="169b0-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="169b0-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="169b0-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="169b0-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="169b0-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="169b0-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="169b0-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="169b0-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="169b0-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="169b0-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="169b0-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="169b0-211">**插座**</span><span class="sxs-lookup"><span data-stu-id="169b0-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="169b0-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="169b0-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="169b0-213">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="169b0-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="169b0-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="169b0-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="169b0-215">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="169b0-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="169b0-216">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="169b0-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="169b0-217">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="169b0-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

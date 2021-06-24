---
description: 控制項程式碼會抓取傳輸控制通訊協定， (指定之通訊端的 TCP) 統計資料。
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f6076440f117ed287ad544c308e574454f33e2b7
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587796"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="d8555-103">SIO_TCP_INFO 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="d8555-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="d8555-104">描述</span><span class="sxs-lookup"><span data-stu-id="d8555-104">Description</span></span>

<span data-ttu-id="d8555-105">**SIO \_ tcp \_ 資訊** 控制程式代碼會抓取傳輸控制通訊協定， (指定之通訊端的 TCP) 統計資料。</span><span class="sxs-lookup"><span data-stu-id="d8555-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="d8555-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="d8555-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="d8555-107">參數</span><span class="sxs-lookup"><span data-stu-id="d8555-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="d8555-108">s</span><span class="sxs-lookup"><span data-stu-id="d8555-108">s</span></span>

<span data-ttu-id="d8555-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="d8555-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="d8555-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="d8555-110">dwIoControlCode</span></span>

<span data-ttu-id="d8555-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="d8555-111">The control code for the operation.</span></span>
<span data-ttu-id="d8555-112">使用 **SIO \_ TCP \_ 資訊** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="d8555-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="d8555-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="d8555-113">lpvInBuffer</span></span>

<span data-ttu-id="d8555-114">輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d8555-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="d8555-115">此參數包含 **DWORD** 的指標，可指定您所使用的 **SIO \_ TCP \_ 資訊** 控制程式代碼版本。</span><span class="sxs-lookup"><span data-stu-id="d8555-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="d8555-116">指定0會使用 [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)。</span><span class="sxs-lookup"><span data-stu-id="d8555-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="d8555-117">指定1可使用 [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)，以提供更多欄位。</span><span class="sxs-lookup"><span data-stu-id="d8555-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which provides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="d8555-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="d8555-118">cbInBuffer</span></span>

<span data-ttu-id="d8555-119">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8555-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="d8555-120">此參數應為 **DWORD** 資料類型的大小。</span><span class="sxs-lookup"><span data-stu-id="d8555-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="d8555-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d8555-121">lpvOutBuffer</span></span>

<span data-ttu-id="d8555-122">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d8555-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="d8555-123">成功輸出時，此參數會包含 [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構的指標，其中包含指定之通訊端的 TCP 統計資料。</span><span class="sxs-lookup"><span data-stu-id="d8555-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="d8555-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="d8555-124">cbOutBuffer</span></span>

<span data-ttu-id="d8555-125">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8555-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="d8555-126">此參數必須至少為 [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="d8555-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="d8555-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="d8555-127">lpcbBytesReturned</span></span>

<span data-ttu-id="d8555-128">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8555-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="d8555-129">如果輸出緩衝區太小，則呼叫會失敗， [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [**WSAEINVAL**](windows-sockets-error-codes-2.md)，而且 *lpcbBytesReturned* 參數會指向 **DWORD** 值零。</span><span class="sxs-lookup"><span data-stu-id="d8555-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="d8555-130">如果 *lpOverlapped* 為 **Null**，則在成功呼叫時所傳回的 *LpcbBytesReturned* 參數所指向的 **DWORD** 值不可以是零。</span><span class="sxs-lookup"><span data-stu-id="d8555-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="d8555-131">如果重迭通訊端的 *lpOverlapped* 參數不是 **Null** ，就會起始無法立即完成的作業，而且稍後將會指出完成的作業。</span><span class="sxs-lookup"><span data-stu-id="d8555-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="d8555-132">傳回的 *lpcbBytesReturned* 參數所指向的 **DWORD** 值可能是零，因為無法判斷儲存的資料大小，直到重迭的作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="d8555-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="d8555-133">當作業完成時，將會收到適當的完成方法通知，以抓取最終完成狀態。</span><span class="sxs-lookup"><span data-stu-id="d8555-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="d8555-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="d8555-134">lpvOverlapped</span></span>

<span data-ttu-id="d8555-135">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d8555-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d8555-136">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="d8555-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="d8555-137">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="d8555-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="d8555-138">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="d8555-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="d8555-139">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="d8555-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="d8555-140">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="d8555-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="d8555-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="d8555-141">lpCompletionRoutine</span></span>

<span data-ttu-id="d8555-142">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="d8555-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="d8555-143">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="d8555-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="d8555-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="d8555-144">lpThreadId</span></span>

<span data-ttu-id="d8555-145">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="d8555-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="d8555-146">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="d8555-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="d8555-147">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="d8555-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="d8555-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="d8555-148">lpErrno</span></span>

<span data-ttu-id="d8555-149">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="d8555-149">A pointer to the error code.</span></span>

<span data-ttu-id="d8555-150">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="d8555-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8555-151">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8555-151">Return value</span></span>

<span data-ttu-id="d8555-152">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d8555-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="d8555-153">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="d8555-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="d8555-154">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="d8555-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="d8555-155">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d8555-155">Error code</span></span> | <span data-ttu-id="d8555-156">意義</span><span class="sxs-lookup"><span data-stu-id="d8555-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="d8555-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="d8555-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="d8555-158">輸入緩衝區的指標為 **Null**，或輸入緩衝區的指定大小不正確。</span><span class="sxs-lookup"><span data-stu-id="d8555-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="d8555-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="d8555-159">**WSAEINVAL**</span></span> | <span data-ttu-id="d8555-160">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="d8555-160">An invalid argument was supplied.</span></span> <span data-ttu-id="d8555-161">如果 *dwIoControlCode* 參數不是有效的命令，或是無法接受指定的輸入參數，或命令不適用於指定的通訊端類型，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d8555-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d8555-162">備註</span><span class="sxs-lookup"><span data-stu-id="d8555-162">Remarks</span></span>

<span data-ttu-id="d8555-163">與使用 [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) 函式來抓取 tcp 統計資料不同的是，使用這個控制項程式碼來抓取 tcp 統計資料並不需要使用者程式碼來載入、儲存和篩選 tcp 連接資料表，也不需要使用較高的許可權。</span><span class="sxs-lookup"><span data-stu-id="d8555-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8555-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8555-164">See also</span></span>

[<span data-ttu-id="d8555-165">插座</span><span class="sxs-lookup"><span data-stu-id="d8555-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="d8555-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="d8555-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="d8555-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="d8555-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="d8555-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="d8555-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="d8555-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="d8555-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="d8555-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="d8555-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="d8555-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="d8555-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="d8555-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="d8555-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="d8555-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="d8555-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

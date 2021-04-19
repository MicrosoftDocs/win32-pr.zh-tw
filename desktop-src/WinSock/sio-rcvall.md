---
description: 控制項程式碼可讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL 控制程式代碼
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973638"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="7d539-103">SIO_RCVALL 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="7d539-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="7d539-104">Description</span><span class="sxs-lookup"><span data-stu-id="7d539-104">Description</span></span>
<span data-ttu-id="7d539-105">**SIO \_ RCVALL** control 程式碼可讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="7d539-106">若要執行這項作業，請使用下列參數呼叫 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="7d539-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="7d539-107">參數</span><span class="sxs-lookup"><span data-stu-id="7d539-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="7d539-108">s</span><span class="sxs-lookup"><span data-stu-id="7d539-108">s</span></span>

<span data-ttu-id="7d539-109">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="7d539-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="7d539-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="7d539-110">dwIoControlCode</span></span>

<span data-ttu-id="7d539-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="7d539-111">The control code for the operation.</span></span>
<span data-ttu-id="7d539-112">使用 **SIO \_ RCVALL** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="7d539-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="7d539-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="7d539-113">lpvInBuffer</span></span>

<span data-ttu-id="7d539-114">應包含選項值之輸入緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7d539-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="7d539-115">**SIO \_ RCVALL** IOCTL 選項的可能值是在 *Mstcpip .h* 標頭檔中定義的 **RCVALL_VALUE** 列舉中指定。</span><span class="sxs-lookup"><span data-stu-id="7d539-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="7d539-116">**SIO \_ RCVALL** 的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="7d539-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="7d539-117">值</span><span class="sxs-lookup"><span data-stu-id="7d539-117">Value</span></span> | <span data-ttu-id="7d539-118">意義</span><span class="sxs-lookup"><span data-stu-id="7d539-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="7d539-119">**RCVALL \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="7d539-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="7d539-120">停用此選項，讓通訊端不會收到透過網路介面傳遞的所有 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="7d539-121">**RCVALL \_ 于**</span><span class="sxs-lookup"><span data-stu-id="7d539-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="7d539-122">啟用此選項，讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="7d539-123">如果 NIC 支援混合模式，此選項會在網路介面卡上啟用混合模式 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="7d539-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="7d539-124">在網路中樞的 LAN 區段上，支援混合模式的 NIC 會在 LAN 上捕捉所有 IPv4 或 IPv6 流量，包括相同 LAN 區段上其他電腦之間的流量。</span><span class="sxs-lookup"><span data-stu-id="7d539-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="7d539-125">所有 (IPv4 或 IPv6 的已捕捉封包，視通訊端) 將會傳遞至原始通訊端而定。</span><span class="sxs-lookup"><span data-stu-id="7d539-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="7d539-126">此選項不會將其他封包捕獲 (ARP、IPX 和 NetBEUI 封包，例如介面上的) 。</span><span class="sxs-lookup"><span data-stu-id="7d539-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="7d539-127">Netmon 針對網路介面使用相同的模式，但不會使用此選項來捕捉流量。</span><span class="sxs-lookup"><span data-stu-id="7d539-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="7d539-128">**RCVALL \_ SOCKETLEVELONLY**</span><span class="sxs-lookup"><span data-stu-id="7d539-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="7d539-129">這項功能目前未執行，因此設定此選項不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="7d539-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="7d539-130">**RCVALL \_ IPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="7d539-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="7d539-131">啟用此選項，讓 IPv4 或 IPv6 通訊端接收通過網路介面之 IP 層級的所有封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="7d539-132">此選項不會在網路介面卡上啟用混合模式。</span><span class="sxs-lookup"><span data-stu-id="7d539-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="7d539-133">此選項只會影響在 IP 層級的封包處理。</span><span class="sxs-lookup"><span data-stu-id="7d539-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="7d539-134">NIC 仍只接收導向至其設定之單播和多播位址的封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="7d539-135">不過，啟用此選項的通訊端不只會接收導向至特定 IP 位址的封包，而是會接收 NIC 接收的所有 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="7d539-136">此選項不會將其他封包捕捉 (ARP、IPX 和 NetBEUI 封包，例如在介面上收到) 。</span><span class="sxs-lookup"><span data-stu-id="7d539-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="7d539-137">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="7d539-137">cbInBuffer</span></span>

<span data-ttu-id="7d539-138">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d539-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="7d539-139">此參數應等於或大於 *lpvInBuffer* 參數所指向的 **RCVALL_VALUE** 列舉值的大小。</span><span class="sxs-lookup"><span data-stu-id="7d539-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="7d539-140">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7d539-140">lpvOutBuffer</span></span>

<span data-ttu-id="7d539-141">輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7d539-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="7d539-142">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="7d539-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="7d539-143">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="7d539-143">cbOutBuffer</span></span>

<span data-ttu-id="7d539-144">輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d539-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="7d539-145">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="7d539-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="7d539-146">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="7d539-146">lpcbBytesReturned</span></span>

<span data-ttu-id="7d539-147">變數的指標，此變數會接收儲存在輸出緩衝區中資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d539-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="7d539-148">此參數未用來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="7d539-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="7d539-149">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="7d539-149">lpvOverlapped</span></span>

<span data-ttu-id="7d539-150">[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d539-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7d539-151">如果通訊端 *s* 是在沒有重迭屬性的情況下建立的，則會忽略 *lpOverlapped* 參數。</span><span class="sxs-lookup"><span data-stu-id="7d539-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="7d539-152">如果 *以* 重迭的屬性開啟，且 *lpOverlapped* 參數不是 **Null**，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="7d539-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="7d539-153">在此情況下， *lpOverlapped* 參數必須指向有效的 [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) 結構。</span><span class="sxs-lookup"><span data-stu-id="7d539-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7d539-154">針對重迭的作業， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函式會立即傳回，而當作業完成時，就會發出適當的完成方法。</span><span class="sxs-lookup"><span data-stu-id="7d539-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="7d539-155">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="7d539-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="7d539-156">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="7d539-156">lpCompletionRoutine</span></span>

<span data-ttu-id="7d539-157">類型： \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="7d539-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="7d539-158">當作業完成時所呼叫的完成常式指標 (針對非重迭通訊端) 略過。</span><span class="sxs-lookup"><span data-stu-id="7d539-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="7d539-159">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="7d539-159">lpThreadId</span></span>

<span data-ttu-id="7d539-160">[**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構的指標，可供提供者在後續的 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="7d539-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="7d539-161">在 [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)函式傳回之前，提供者應該將參考的 [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid)結構 (而不是指向相同) 的指標。</span><span class="sxs-lookup"><span data-stu-id="7d539-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="7d539-162">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="7d539-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="7d539-163">lpErrno</span><span class="sxs-lookup"><span data-stu-id="7d539-163">lpErrno</span></span>

<span data-ttu-id="7d539-164">錯誤碼的指標。</span><span class="sxs-lookup"><span data-stu-id="7d539-164">A pointer to the error code.</span></span>

<span data-ttu-id="7d539-165">**注意**  這個參數只適用于 **WSPIoctl** 函數。</span><span class="sxs-lookup"><span data-stu-id="7d539-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d539-166">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d539-166">Return value</span></span>

<span data-ttu-id="7d539-167">如果作業順利完成， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7d539-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="7d539-168">如果作業失敗或擱置中， [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數會傳回 **通訊端 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="7d539-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="7d539-169">若要取得延伸錯誤資訊，請呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)。</span><span class="sxs-lookup"><span data-stu-id="7d539-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="7d539-170">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7d539-170">Error code</span></span> | <span data-ttu-id="7d539-171">意義</span><span class="sxs-lookup"><span data-stu-id="7d539-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="7d539-172">**WSA \_ IO \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="7d539-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="7d539-173">已成功起始重迭的作業，並會在稍後指出完成的時間。</span><span class="sxs-lookup"><span data-stu-id="7d539-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="7d539-174">**已 \_ 中止 WSA 作業 \_**</span><span class="sxs-lookup"><span data-stu-id="7d539-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="7d539-175">因為通訊端關閉或 **SIO_FLUSH** IOCTL 命令的執行，所以重迭的作業已取消。</span><span class="sxs-lookup"><span data-stu-id="7d539-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="7d539-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7d539-176">**WSAEFAULT**</span></span> | <span data-ttu-id="7d539-177">*LpOverlapped* 或 *lpCompletionRoutine* 參數並未完全包含在使用者位址空間的有效部分中。</span><span class="sxs-lookup"><span data-stu-id="7d539-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="7d539-178">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="7d539-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="7d539-179">當回呼正在進行時，就會叫用此函數。</span><span class="sxs-lookup"><span data-stu-id="7d539-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="7d539-180">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="7d539-180">**WSAEINTR**</span></span> | <span data-ttu-id="7d539-181">封鎖作業已中斷。</span><span class="sxs-lookup"><span data-stu-id="7d539-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="7d539-182">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="7d539-182">**WSAEINVAL**</span></span> | <span data-ttu-id="7d539-183">*DwIoControlCode* 參數不是有效的命令，或指定的輸入參數無法接受，或命令不適用於指定的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="7d539-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="7d539-184">如果 *cbInBuffer* 參數小於， `sizeof(UCHAR)` 或 *lpvInBuffer* 參數指向不是 **RCVALL_VALUE** 列舉值的值，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d539-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="7d539-185">如果找不到與通訊端關聯的網路介面，也可能會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d539-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="7d539-186">如果與通訊端相關聯的網路介面已刪除或移除 (移除 PCMCIA 或 USB 網路裝置，例如) ，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="7d539-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="7d539-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="7d539-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="7d539-188">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="7d539-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="7d539-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="7d539-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="7d539-190">沒有可用的緩衝區空間。</span><span class="sxs-lookup"><span data-stu-id="7d539-190">No buffer space available.</span></span> |
| <span data-ttu-id="7d539-191">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="7d539-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="7d539-192">指定的通訊協定不支援通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="7d539-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="7d539-193">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="7d539-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="7d539-194">*描述項不是* 通訊端。</span><span class="sxs-lookup"><span data-stu-id="7d539-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="7d539-195">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="7d539-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="7d539-196">不支援指定的 IOCTL 命令。</span><span class="sxs-lookup"><span data-stu-id="7d539-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="7d539-197">如果傳輸提供者不支援 **SIO \_ RCVALL** IOCTL，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d539-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="7d539-198">備註</span><span class="sxs-lookup"><span data-stu-id="7d539-198">Remarks</span></span>

<span data-ttu-id="7d539-199">在 Windows 2000 和更新版本的作業系統上，支援 **SIO \_ RCVALL** 的 IOCTL。</span><span class="sxs-lookup"><span data-stu-id="7d539-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="7d539-200">**SIO \_ RCVALL** IOCTL 可讓通訊端接收網路介面上的所有 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="7d539-201">傳遞給 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) 或 **WSPIoctl** 函數的通訊端控制碼必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="7d539-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="7d539-202">以位址系列設定為 AF_INET、通訊端類型設定為 SOCK_RAW，以及將通訊協定設定為 [IPPROTO_IP] 建立的 IPv4 通訊端。</span><span class="sxs-lookup"><span data-stu-id="7d539-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="7d539-203">以位址系列設定為 AF_INET6、通訊端類型設定為 [SOCK_RAW，並將通訊協定設定為 [IPPROTO_IPV6] 建立的 IPv6 通訊端。</span><span class="sxs-lookup"><span data-stu-id="7d539-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="7d539-204">如需有關原始通訊端的詳細資訊，請參閱 [**Tcp/ip 原始通訊端**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)。</span><span class="sxs-lookup"><span data-stu-id="7d539-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="7d539-205">通訊端也必須系結至明確的本機 IPv4 或 IPv6 介面，這表示您無法系結至 **INADDR \_ any** 或 **in6addr \_ any**。</span><span class="sxs-lookup"><span data-stu-id="7d539-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="7d539-206">當通訊端系結且 IOCTL 順利完成之後，對 [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) 或 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 函式的呼叫會傳回通過指定 IPv4 介面傳遞的 ipv4 資料包，或傳回通過指定 ipv6 介面的 ipv6 資料包。</span><span class="sxs-lookup"><span data-stu-id="7d539-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="7d539-207">請注意，您必須提供夠大的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7d539-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="7d539-208">設定這個 IOCTL 只會在指定的介面上捕獲 IPv4 或 IPv6 封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="7d539-209">這個 IOCTL 不會將其他封包捕捉 (ARP、IPX 和 NetBEUI 封包，例如介面上的) 。</span><span class="sxs-lookup"><span data-stu-id="7d539-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="7d539-210">使用 **SIO \_ RCVALL** IOCTL 系結至特定本機介面的通訊端，只會接收通過該介面的封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="7d539-211">它不會接收在另一個介面上收到的封包，並在與 **SIO \_ RCVALL** IOCTL 系結之通訊端不同的其他介面上轉寄。</span><span class="sxs-lookup"><span data-stu-id="7d539-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="7d539-212">在 Windows Server 2008 及更早版本中， **SIO \_ RCVALL** IOCTL 設定不會捕捉從網路介面送出的本機封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="7d539-213">這包含在另一個介面上收到的封包，並將針對 **SIO \_ RCVALL** IOCTL 指定的網路介面轉送出去。</span><span class="sxs-lookup"><span data-stu-id="7d539-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="7d539-214">在 Windows 7 和 Windows Server 2008 R2 上，這項變更已變更，因此也會捕捉從網路介面送出的本機封包。</span><span class="sxs-lookup"><span data-stu-id="7d539-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="7d539-215">這包括在另一個介面上收到的封包，然後使用 **SIO \_ RCVALL** IOCTL 轉送系結至通訊端的網路介面。</span><span class="sxs-lookup"><span data-stu-id="7d539-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="7d539-216">設定這個 IOCTL 需要本機電腦的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="7d539-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="7d539-217">這項功能有時稱為混合模式。</span><span class="sxs-lookup"><span data-stu-id="7d539-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="7d539-218">在某個介面上套用此選項，然後再到另一個使用此 IOCTL 的單一呼叫的介面，則不支援任何直接變更。</span><span class="sxs-lookup"><span data-stu-id="7d539-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="7d539-219">應用程式必須先使用這個 IOCTL 來關閉第一個介面上的行為，然後使用這個 IOCTL 來啟用新介面的行為。</span><span class="sxs-lookup"><span data-stu-id="7d539-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d539-220">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d539-220">See also</span></span>

[<span data-ttu-id="7d539-221">**插座**</span><span class="sxs-lookup"><span data-stu-id="7d539-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="7d539-222">**TCP/IP 原始通訊端**</span><span class="sxs-lookup"><span data-stu-id="7d539-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="7d539-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="7d539-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="7d539-224">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="7d539-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="7d539-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="7d539-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="7d539-226">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="7d539-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="7d539-227">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="7d539-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="7d539-228">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="7d539-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)

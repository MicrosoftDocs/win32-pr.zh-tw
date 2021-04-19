---
description: 允許應用程式啟用或停用 IPv6 通訊端上 WSARecvMsg 函式的封包資訊傳回。
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: 'IPV6_PKTINFO 通訊端選項 (Ws2ipdef) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970807"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="4b7a3-103">IPV6 \_ PKTINFO 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="4b7a3-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="4b7a3-104">IPV6 \_ PKTINFO 通訊端選項可讓應用程式啟用或停用 ipv6 通訊端上的 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式的封包資訊。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="4b7a3-105">若要查詢此通訊端選項的狀態，請呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="4b7a3-106">若要設定此選項，請使用下列參數呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="4b7a3-107">通訊端選項值</span><span class="sxs-lookup"><span data-stu-id="4b7a3-107">Socket option value</span></span>

<span data-ttu-id="4b7a3-108">表示這個通訊端選項的常數是19。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7a3-109">語法</span><span class="sxs-lookup"><span data-stu-id="4b7a3-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="4b7a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b7a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b7a3-111"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7a3-112">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="4b7a3-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7a3-114">定義選項的層級。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-114">The level at which the option is defined.</span></span> <span data-ttu-id="4b7a3-115">使用 **IPPROTO \_ IPV6** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4b7a3-116">*optname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7a3-117">要取得或設定其值的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="4b7a3-118">使用 IPV6 \_ PKTINFO 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="4b7a3-119">*optval* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7a3-120">緩衝區的指標，其中包含要設定之選項的值。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="4b7a3-121">此參數應指向等於或大於 **DWORD** 值大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="4b7a3-122">此值會被視為布林值，0用來指出 **FALSE** (停用的) ，而非零值 **則表示 (啟用**) 。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="4b7a3-123">*optlen* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b7a3-124">*Optval* 緩衝區大小的指標，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="4b7a3-125">此大小必須等於或大於 **DWORD** 值的大小。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b7a3-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b7a3-126">Return value</span></span>

<span data-ttu-id="4b7a3-127">如果作業順利完成， [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 或 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="4b7a3-128">如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="4b7a3-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4b7a3-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="4b7a3-130">意義</span><span class="sxs-lookup"><span data-stu-id="4b7a3-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b7a3-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="4b7a3-132">在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="4b7a3-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="4b7a3-134">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="4b7a3-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="4b7a3-136">其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="4b7a3-137">如果 *optlen* 參數所指向的值小於 **DWORD** 值的大小，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="4b7a3-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="4b7a3-139">封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="4b7a3-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="4b7a3-141">提供的引數無效。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-141">An invalid argument was supplied.</span></span> <span data-ttu-id="4b7a3-142">如果 *層級* 參數未知或無效，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="4b7a3-143">在 Windows Vista 和更新版本上，如果通訊端處於過渡狀態，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4b7a3-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="4b7a3-145">指定的通訊協定系列未知或不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="4b7a3-146">如果傳入 *s* 參數的通訊端描述項的 *類型* 參數不是 **SOCK \_ DGRAM** 或 **SOCK \_ RAW**，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="4b7a3-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="4b7a3-148">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="4b7a3-149">備註</span><span class="sxs-lookup"><span data-stu-id="4b7a3-149">Remarks</span></span>

<span data-ttu-id="4b7a3-150">使用 [](/windows/desktop/api/winsock/nf-winsock-getsockopt) ipv6 \_ PKTINFO 通訊端選項呼叫的 getsockopt 函式，可讓應用程式判斷 IPV6 通訊端的 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式是否會傳回封包資訊。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="4b7a3-151">使用 [](/windows/desktop/api/winsock/nf-winsock-setsockopt) IPV6 \_ PKTINFO 通訊端選項呼叫的 setsockopt 函式可讓應用程式啟用或停用 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式的封包資訊傳回。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="4b7a3-152">\_預設會停用通訊端的 IPV6 PKTINFO 選項 (設定為 **FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="4b7a3-153">在 **SOCK \_ DGRAM** 或 **SOCK \_ RAW** 類型的 IPv6 通訊端上啟用這個通訊端選項時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式會傳回 *WSAMSG* 參數所指向之 [**lpMsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)結構中的封包資訊。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="4b7a3-154">所傳回 **WSAMSG** 結構中的其中一個控制資料物件將包含用來儲存所接收封包位址資訊的 [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="4b7a3-155">針對 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)函式透過 IPv6 接收的資料包，所接收之 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)結構的 **控制項** 成員將包含包含 **WSACMSGHDR** 結構的 [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf)結構。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="4b7a3-156">此 **WSACMSGHDR** 結構的 **cmsg \_ 層級** 成員會包含 **IPPROTO \_ ipv6**，此結構的 **cmsg \_ 類型** 成員會包含 **IPV6 \_ PKTINFO**，而 **cmsg \_ 資料** 成員會包含用來儲存所接收之 IPV6 封包位址資訊的 [**in6 \_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)結構。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="4b7a3-157">**In6 \_ pktinfo** 結構中的 ipv6 位址是接收封包的 ipv6 位址。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="4b7a3-158">對於雙重堆疊資料包通訊端，如果應用程式需要 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式以針對透過 IPv4 接收的資料包來傳回 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中的封包資訊，則必須在通訊端上將 [IP \_ PKTINFO](ip-pktinfo.md) 通訊端選項設定為 true。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="4b7a3-159">如果 \_ 通訊端上的 ipv6 PKTINFO 選項設定為 true，封包資訊將會提供給透過 IPV6 接收的資料包，但可能不會提供給透過 IPv4 接收的資料包。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="4b7a3-160">請注意， *Ws2ipdef .h* 標頭檔會自動包含在 *Ws2tcpip* 中，而且永遠不會直接使用。</span><span class="sxs-lookup"><span data-stu-id="4b7a3-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7a3-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b7a3-161">Requirements</span></span>



| <span data-ttu-id="4b7a3-162">需求</span><span class="sxs-lookup"><span data-stu-id="4b7a3-162">Requirement</span></span> | <span data-ttu-id="4b7a3-163">值</span><span class="sxs-lookup"><span data-stu-id="4b7a3-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7a3-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b7a3-164">Minimum supported client</span></span><br/> | <span data-ttu-id="4b7a3-165">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="4b7a3-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b7a3-166">Minimum supported server</span></span><br/> | <span data-ttu-id="4b7a3-167">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b7a3-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4b7a3-168">標頭</span><span class="sxs-lookup"><span data-stu-id="4b7a3-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b7a3-169"><dt>Ws2ipdef (包含 Ws2tcpip) </dt></span><span class="sxs-lookup"><span data-stu-id="4b7a3-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7a3-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b7a3-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7a3-171">雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="4b7a3-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="4b7a3-172">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="4b7a3-173">**in6 \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="4b7a3-174">IP \_ PKTINFO</span><span class="sxs-lookup"><span data-stu-id="4b7a3-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="4b7a3-175">**IPPROTO \_ IPV6 通訊端選項**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="4b7a3-176">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="4b7a3-177">**插座**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="4b7a3-178">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="4b7a3-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="4b7a3-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 

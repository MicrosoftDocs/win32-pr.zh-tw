---
description: 的設計目的是允許應用程式啟用通訊端連線的 keep-alive 封包。
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: 'SO_KEEPALIVE 通訊端選項 (Ws2def) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980577"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="8a96c-103">所以 \_ KEEPALIVE 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="8a96c-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="8a96c-104">此「持續連線 **」通訊端 \_ 選項的設計** 目的是允許應用程式啟用通訊端連線的 keep-alive 封包。</span><span class="sxs-lookup"><span data-stu-id="8a96c-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="8a96c-105">若要查詢此通訊端選項的狀態，請呼叫 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 函數。</span><span class="sxs-lookup"><span data-stu-id="8a96c-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="8a96c-106">若要設定此選項，請使用下列參數呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數。</span><span class="sxs-lookup"><span data-stu-id="8a96c-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="8a96c-107">通訊端選項值</span><span class="sxs-lookup"><span data-stu-id="8a96c-107">Socket option value</span></span>

<span data-ttu-id="8a96c-108">表示這個通訊端選項的常數是0x0008。</span><span class="sxs-lookup"><span data-stu-id="8a96c-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a96c-109">語法</span><span class="sxs-lookup"><span data-stu-id="8a96c-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="8a96c-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a96c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a96c-111"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a96c-112">識別通訊端的描述元。</span><span class="sxs-lookup"><span data-stu-id="8a96c-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="8a96c-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a96c-114">定義選項的層級。</span><span class="sxs-lookup"><span data-stu-id="8a96c-114">The level at which the option is defined.</span></span> <span data-ttu-id="8a96c-115">使用 **SOL \_ 通訊端** 進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="8a96c-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a96c-116">*optname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a96c-117">要設定其值的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="8a96c-118">請使用此操作的 **\_ KEEPALIVE** 。</span><span class="sxs-lookup"><span data-stu-id="8a96c-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a96c-119">*optval* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a96c-120">緩衝區的指標，其中包含要設定之選項的值。</span><span class="sxs-lookup"><span data-stu-id="8a96c-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="8a96c-121">此參數應指向等於或大於 **DWORD** 值大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8a96c-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="8a96c-122">此值會被視為布林值，0用來指出 **FALSE** (停用的) ，而非零值 **則表示 (啟用**) 。</span><span class="sxs-lookup"><span data-stu-id="8a96c-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8a96c-123">*optlen* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a96c-124">*Optval* 緩衝區大小的指標，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="8a96c-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="8a96c-125">此大小必須等於或大於 **DWORD** 值的大小。</span><span class="sxs-lookup"><span data-stu-id="8a96c-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a96c-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a96c-126">Return value</span></span>

<span data-ttu-id="8a96c-127">如果作業順利完成， [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8a96c-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="8a96c-128">如果作業失敗， \_ 則會傳回 SOCKET 錯誤的值，並藉由呼叫 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)來取出特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a96c-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="8a96c-129">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8a96c-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="8a96c-130">意義</span><span class="sxs-lookup"><span data-stu-id="8a96c-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a96c-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="8a96c-132">在使用此函式之前，必須先進行成功的 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="8a96c-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="8a96c-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8a96c-134">網路子系統失敗。</span><span class="sxs-lookup"><span data-stu-id="8a96c-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="8a96c-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8a96c-136">其中一個 *optval* 或 *optlen* 參數指向不在使用者位址空間有效部分的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8a96c-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="8a96c-137">如果 *optlen* 參數所指向的值小於 **DWORD** 值的大小，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a96c-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="8a96c-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8a96c-139">封鎖的 Windows 通訊端1.1 呼叫正在進行中，或服務提供者仍在處理回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8a96c-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="8a96c-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8a96c-141">*層級* 參數未知或無效。</span><span class="sxs-lookup"><span data-stu-id="8a96c-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="8a96c-142">在 Windows Vista 和更新版本上，如果通訊端處於過渡狀態，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a96c-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="8a96c-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8a96c-144">指定的通訊協定系列未知或不支援此選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="8a96c-145">如果為資料包通訊端傳入 *s* 參數的通訊端描述元，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a96c-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="8a96c-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8a96c-147">描述項不是通訊端。</span><span class="sxs-lookup"><span data-stu-id="8a96c-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8a96c-148">備註</span><span class="sxs-lookup"><span data-stu-id="8a96c-148">Remarks</span></span>

<span data-ttu-id="8a96c-149">使用「使用 **\_ KEEPALIVE** 通訊端」選項呼叫的 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函式可讓應用程式取出 KEEPALIVE 選項的目前狀態，不過這是通常不使用的功能。</span><span class="sxs-lookup"><span data-stu-id="8a96c-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="8a96c-150">如果應用程式需要在通訊端上啟用 keepalive 封包，它 justs 會呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式來啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="8a96c-151">以 with **\_ KEEPALIVE** 通訊端選項呼叫的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式，可讓應用程式啟用通訊端連線的 keep-alive 封包。</span><span class="sxs-lookup"><span data-stu-id="8a96c-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="8a96c-152">預設會停用通訊端的 [ **SO \_ KEEPALIVE** ] 選項 (設定為 [ **FALSE** ]) 。</span><span class="sxs-lookup"><span data-stu-id="8a96c-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="8a96c-153">當這個通訊端選項啟用時，TCP 堆疊會在間隔內未收到連接的資料或通知封包時，傳送 keep-alive 封包。</span><span class="sxs-lookup"><span data-stu-id="8a96c-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="8a96c-154">如需保持連線選項的詳細資訊，請參閱4.2.3.6 中的「 *網際網路主機需求* 」一節：在 [IETF 網站](https://www.ietf.org/rfc/rfc1122.txt)提供的 RFC 1122 中所指定的通訊層。</span><span class="sxs-lookup"><span data-stu-id="8a96c-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="8a96c-155"> (此資源可能僅提供英文版。 ) </span><span class="sxs-lookup"><span data-stu-id="8a96c-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="8a96c-156">此 **「 \_** 持續連線」通訊端選項僅適用于支援保持運作 (連接導向的通訊協定) 概念的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8a96c-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="8a96c-157">若為 TCP，預設的 keep-alive timeout 為2小時，而 keep-alive 間隔為1秒。</span><span class="sxs-lookup"><span data-stu-id="8a96c-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="8a96c-158">預設的 keep-alive 探查數目會根據 Windows 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="8a96c-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="8a96c-159">您可以使用 [**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control 程式碼來啟用或停用持續運作，以及調整單一連接的超時和間隔。</span><span class="sxs-lookup"><span data-stu-id="8a96c-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="8a96c-160">如果啟用 keep-alive，則 **會使用預設 \_** 的 TCP 設定來進行保持連線的超時時間和間隔，除非這些值已使用 **SIO \_ KEEPALIVE \_ VALS** 變更。</span><span class="sxs-lookup"><span data-stu-id="8a96c-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="8a96c-161">Keep-alive timeout 的預設全系統值可透過 [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。</span><span class="sxs-lookup"><span data-stu-id="8a96c-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="8a96c-162">Keep-alive 間隔的預設全系統值可透過 [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) 登錄設定來控制，此設定會採用以毫秒為單位的值。</span><span class="sxs-lookup"><span data-stu-id="8a96c-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="8a96c-163">在 Windows Vista 和更新版本上， (資料重新傳輸) 的 keep-alive 探查數目設定為10，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="8a96c-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="8a96c-164">在 Windows Server 2003、Windows XP 及 Windows 2000 上，保持運作探查數目的預設設定為5。</span><span class="sxs-lookup"><span data-stu-id="8a96c-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="8a96c-165">Keep-alive 探查的數目可透過 [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) 和 [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) 登錄設定來控制。</span><span class="sxs-lookup"><span data-stu-id="8a96c-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="8a96c-166">Keep-alive 探查的數目會設定為兩個登錄機碼值的較大值。</span><span class="sxs-lookup"><span data-stu-id="8a96c-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="8a96c-167">如果這個數位為0，則不會傳送 keep-alive 探查。</span><span class="sxs-lookup"><span data-stu-id="8a96c-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="8a96c-168">如果此數位大於255，則會調整為255。</span><span class="sxs-lookup"><span data-stu-id="8a96c-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="8a96c-169">在 Windows Vista 和更新版本上，只有當通訊端處於已知狀態，而不是過渡狀態時，才能使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式來設定此「持續連線 **」通訊端 \_** 選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="8a96c-170">若為 TCP，則應該在 connect 函式 ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) 呼叫之前，或在連接要求實際完成之後，設定 [ **SO \_ KEEPALIVE** 通訊端] 選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="8a96c-171">如果以非同步方式呼叫 connect 函式，則需要先等待連接完成，然後再嘗試設定「 **讓 \_ KEEPALIVE** 通訊端」選項。</span><span class="sxs-lookup"><span data-stu-id="8a96c-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="8a96c-172">如果應用程式在連線要求仍在處理時嘗試設定 [使用 **\_ KEEPALIVE** 通訊端] 選項， **setsockopt** 函式將會失敗，並傳回 [WSAEINVAL](windows-sockets-error-codes-2.md)。</span><span class="sxs-lookup"><span data-stu-id="8a96c-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="8a96c-173">在 Windows Server 2003、Windows XP 及 Windows 2000 上，如果通訊端是過渡狀態 (連接要求仍在進行中，則可以使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式來設定 [ **SO \_ KEEPALIVE** 通訊端] 選項，) 和已知狀態。</span><span class="sxs-lookup"><span data-stu-id="8a96c-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="8a96c-174">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="8a96c-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a96c-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a96c-175">Requirements</span></span>



| <span data-ttu-id="8a96c-176">需求</span><span class="sxs-lookup"><span data-stu-id="8a96c-176">Requirement</span></span> | <span data-ttu-id="8a96c-177">值</span><span class="sxs-lookup"><span data-stu-id="8a96c-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a96c-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a96c-178">Minimum supported client</span></span><br/> | <span data-ttu-id="8a96c-179">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8a96c-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a96c-180">Minimum supported server</span></span><br/> | <span data-ttu-id="8a96c-181">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a96c-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8a96c-182">標頭</span><span class="sxs-lookup"><span data-stu-id="8a96c-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a96c-183"><dt>Ws2def (包含 Winsock2) </dt></span><span class="sxs-lookup"><span data-stu-id="8a96c-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a96c-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a96c-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a96c-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="8a96c-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="8a96c-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="8a96c-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="8a96c-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8a96c-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="8a96c-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8a96c-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="8a96c-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8a96c-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="8a96c-190">**插座**</span><span class="sxs-lookup"><span data-stu-id="8a96c-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="8a96c-191">[**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a96c-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8a96c-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8a96c-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="8a96c-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="8a96c-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 

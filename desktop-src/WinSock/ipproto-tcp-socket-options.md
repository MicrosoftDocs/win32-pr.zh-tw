---
description: 下表說明適用于 \_ IPv4 和 IPv6 位址系列所建立之通訊端的 IPPROTO TCP 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ protocol 參數指定為 tcp (IPPROTO \_ tcp) 。
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: IPPROTO_TCP 通訊端選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994251"
---
# <a name="ipproto_tcp-socket-options"></a><span data-ttu-id="30815-103">IPPROTO \_ TCP 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="30815-103">IPPROTO\_TCP socket options</span></span>

<span data-ttu-id="30815-104">下表說明適用于 IPv4 和 IPv6 位址系列所建立之通訊端的 **IPPROTO \_ TCP** 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ *PROTOCOL* 參數 [](/windows/desktop/api/Winsock2/nf-winsock2-socket)指定為 tcp (IPPROTO \_ tcp) 。</span><span class="sxs-lookup"><span data-stu-id="30815-104">The following table describes **IPPROTO\_TCP** socket options that apply to sockets created for the IPv4 and IPv6 address families (AF\_INET and AF\_INET6) with the *protocol* parameter to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function specified as TCP (IPPROTO\_TCP).</span></span> <span data-ttu-id="30815-105">如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。</span><span class="sxs-lookup"><span data-stu-id="30815-105">See the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function reference pages for more information on getting and setting socket options.</span></span>

<span data-ttu-id="30815-106">若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。</span><span class="sxs-lookup"><span data-stu-id="30815-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols), or [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) function.</span></span>

## <a name="options"></a><span data-ttu-id="30815-107">選項。</span><span class="sxs-lookup"><span data-stu-id="30815-107">Options</span></span>

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30815-108">選項</span><span class="sxs-lookup"><span data-stu-id="30815-108">Option</span></span></th>
<th><span data-ttu-id="30815-109">Get</span><span class="sxs-lookup"><span data-stu-id="30815-109">Get</span></span></th>
<th><span data-ttu-id="30815-110">設定</span><span class="sxs-lookup"><span data-stu-id="30815-110">Set</span></span></th>
<th><span data-ttu-id="30815-111">Optval 類型</span><span class="sxs-lookup"><span data-stu-id="30815-111">Optval type</span></span></th>
<th><span data-ttu-id="30815-112">Description</span><span class="sxs-lookup"><span data-stu-id="30815-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="30815-113">TCP_BSDURGENT</span><span class="sxs-lookup"><span data-stu-id="30815-113">TCP_BSDURGENT</span></span></td>
<td><span data-ttu-id="30815-114">是</span><span class="sxs-lookup"><span data-stu-id="30815-114">yes</span></span></td>
<td><span data-ttu-id="30815-115">是</span><span class="sxs-lookup"><span data-stu-id="30815-115">yes</span></span></td>
<td><span data-ttu-id="30815-116">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-116">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-117">若 <strong>為 TRUE</strong>，則服務提供者會將 Berkeley 軟體散發 (BSD) 樣式 (預設) 來處理快速資料。</span><span class="sxs-lookup"><span data-stu-id="30815-117">If <strong>TRUE</strong>, the service provider implements the Berkeley Software Distribution (BSD) style (default) for handling expedited data.</span></span> <span data-ttu-id="30815-118">此選項是 TCP_EXPEDITED_1122 選項的反向。</span><span class="sxs-lookup"><span data-stu-id="30815-118">This option is the inverse of the TCP_EXPEDITED_1122 option.</span></span> <span data-ttu-id="30815-119">此選項只能在連接上設定一次。</span><span class="sxs-lookup"><span data-stu-id="30815-119">This option can be set on the connection only once.</span></span> <span data-ttu-id="30815-120">一旦將此選項設為 on，就無法關閉這個選項。</span><span class="sxs-lookup"><span data-stu-id="30815-120">Once this option is set on, this option cannot be turned off.</span></span> <span data-ttu-id="30815-121">服務提供者不需要執行這個選項。</span><span class="sxs-lookup"><span data-stu-id="30815-121">This option is not required to be implemented by service providers.</span></span> <span data-ttu-id="30815-122">預設會啟用此選項 (設定為 <strong>TRUE</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="30815-122">The option is enabled (set to <strong>TRUE</strong>) by default.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-123">TCP_EXPEDITED_1122</span><span class="sxs-lookup"><span data-stu-id="30815-123">TCP_EXPEDITED_1122</span></span></td>
<td><span data-ttu-id="30815-124">是</span><span class="sxs-lookup"><span data-stu-id="30815-124">yes</span></span></td>
<td><span data-ttu-id="30815-125">是</span><span class="sxs-lookup"><span data-stu-id="30815-125">yes</span></span></td>
<td><span data-ttu-id="30815-126">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-126">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-127">若 <strong>為 TRUE</strong>，則服務提供者會依照 RFC-1222 中指定的方式來執行快速資料。</span><span class="sxs-lookup"><span data-stu-id="30815-127">If <strong>TRUE</strong>, the service provider implements the expedited data as specified in RFC-1222.</span></span> <span data-ttu-id="30815-128">否則，會使用 Berkeley 軟體散發 (BSD) 樣式 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="30815-128">Otherwise, the Berkeley Software Distribution (BSD) style (default) is used.</span></span> <span data-ttu-id="30815-129">此選項只能在連接上設定一次。</span><span class="sxs-lookup"><span data-stu-id="30815-129">This option can be set on the connection only once.</span></span> <span data-ttu-id="30815-130">一旦將此選項設為 on，就無法關閉這個選項。</span><span class="sxs-lookup"><span data-stu-id="30815-130">Once this option is set on, this option cannot be turned off.</span></span> <span data-ttu-id="30815-131">服務提供者不需要執行這個選項。</span><span class="sxs-lookup"><span data-stu-id="30815-131">This option is not required to be implemented by service providers.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-132">TCP_FAIL_CONNECT_ON_ICMP_ERROR</span><span class="sxs-lookup"><span data-stu-id="30815-132">TCP_FAIL_CONNECT_ON_ICMP_ERROR</span></span></td>
<td><span data-ttu-id="30815-133">是</span><span class="sxs-lookup"><span data-stu-id="30815-133">yes</span></span></td>
<td><span data-ttu-id="30815-134">是</span><span class="sxs-lookup"><span data-stu-id="30815-134">yes</span></span></td>
<td><span data-ttu-id="30815-135">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-135">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-136">若 <strong>為 TRUE</strong>，connect API 呼叫將會在接收到具有值 WSAEHOSTUNREACH 的 ICMP 錯誤時傳回。</span><span class="sxs-lookup"><span data-stu-id="30815-136">If <strong>TRUE</strong>, a connect API call will return upon reception of an ICMP error with value WSAEHOSTUNREACH.</span></span> <span data-ttu-id="30815-137">錯誤的來源位址接著會透過 TCP_ICMP_ERROR_INFO 通訊端選項提供。</span><span class="sxs-lookup"><span data-stu-id="30815-137">The source address of the error will then be available via the TCP_ICMP_ERROR_INFO socket option.</span></span> <span data-ttu-id="30815-138">如果 <strong>為 FALSE</strong>，則通訊端會正常運作。</span><span class="sxs-lookup"><span data-stu-id="30815-138">If <strong>FALSE</strong>, the socket behaves normally.</span></span> <span data-ttu-id="30815-139">預設為停用 (設定為 <strong>FALSE</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="30815-139">The default is disabled (set to <strong>FALSE</strong>).</span></span> <span data-ttu-id="30815-140">針對型別安全，您應該使用 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> 和 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> 函式，而不是直接使用通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="30815-140">For type-safety, you should use the <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> and <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> functions instead of using the socket option directly.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-141">TCP_ICMP_ERROR_INFO</span><span class="sxs-lookup"><span data-stu-id="30815-141">TCP_ICMP_ERROR_INFO</span></span></td>
<td><span data-ttu-id="30815-142">是</span><span class="sxs-lookup"><span data-stu-id="30815-142">yes</span></span></td>
<td><span data-ttu-id="30815-143">不可以</span><span class="sxs-lookup"><span data-stu-id="30815-143">no</span></span></td>
<td><span data-ttu-id="30815-144"><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></span><span class="sxs-lookup"><span data-stu-id="30815-144"><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></span></span></td>
<td><span data-ttu-id="30815-145">抓取 TCP 通訊端在失敗的連接呼叫期間收到的 ICMP 錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="30815-145">Retrieves the info of an ICMP error received by the TCP socket during a failed connect call.</span></span> <span data-ttu-id="30815-146">只有在先前已啟用 TCP_FAIL_CONNECT_ON_ICMP_ERROR 的 TCP 通訊端上有效，且 <strong>CONNECT</strong> 已傳回 WSAEHOSTUNREACH。</span><span class="sxs-lookup"><span data-stu-id="30815-146">Only valid on a TCP socket where TCP_FAIL_CONNECT_ON_ICMP_ERROR has previously been enabled, and <strong>connect</strong> has returned WSAEHOSTUNREACH.</span></span> <span data-ttu-id="30815-147">查詢未封鎖。</span><span class="sxs-lookup"><span data-stu-id="30815-147">The query is non-blocking.</span></span> <span data-ttu-id="30815-148">如果查詢成功，且傳回的 optlen 值為0，則自上次連接呼叫後，就不會收到任何 ICMP 錯誤。</span><span class="sxs-lookup"><span data-stu-id="30815-148">If queried successfully and the returned optlen value is 0, then no ICMP error has been received since the last connect call.</span></span> <span data-ttu-id="30815-149">如果收到 ICMP 錯誤，則其資訊將可供使用，直到再次呼叫 <strong>connect</strong> 為止。</span><span class="sxs-lookup"><span data-stu-id="30815-149">If an ICMP error was received, its info will be available until <strong>connect</strong> is called again.</span></span> <span data-ttu-id="30815-150">這項資訊會以 <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> 結構的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="30815-150">The info is returned as an <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> structure.</span></span> <span data-ttu-id="30815-151">針對型別安全，您應該使用 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> 函式，而不是直接使用通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="30815-151">For type-safety, you should use the <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> function instead of using the socket option directly.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-152">TCP_KEEPCNT</span><span class="sxs-lookup"><span data-stu-id="30815-152">TCP_KEEPCNT</span></span></td>
<td><span data-ttu-id="30815-153">是</span><span class="sxs-lookup"><span data-stu-id="30815-153">yes</span></span></td>
<td><span data-ttu-id="30815-154">是</span><span class="sxs-lookup"><span data-stu-id="30815-154">yes</span></span></td>
<td><span data-ttu-id="30815-155">DWORD</span><span class="sxs-lookup"><span data-stu-id="30815-155">DWORD</span></span></td>
<td><span data-ttu-id="30815-156">取得或設定要在連接結束之前傳送的 TCP 保持運作探查數目。</span><span class="sxs-lookup"><span data-stu-id="30815-156">Gets or sets the number of TCP keep alive probes that will be sent before the connection is terminated.</span></span> <span data-ttu-id="30815-157">將 TCP_KEEPCNT 設定為大於255的值是不合法的。</span><span class="sxs-lookup"><span data-stu-id="30815-157">It is illegal to set TCP_KEEPCNT to a value greater than 255.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-158">TCP_MAXRT</span><span class="sxs-lookup"><span data-stu-id="30815-158">TCP_MAXRT</span></span></td>
<td><span data-ttu-id="30815-159">是</span><span class="sxs-lookup"><span data-stu-id="30815-159">yes</span></span></td>
<td><span data-ttu-id="30815-160">是</span><span class="sxs-lookup"><span data-stu-id="30815-160">yes</span></span></td>
<td><span data-ttu-id="30815-161">DWORD</span><span class="sxs-lookup"><span data-stu-id="30815-161">DWORD</span></span></td>
<td><span data-ttu-id="30815-162">如果此值為非負數，表示所需的連接逾時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="30815-162">If this value is non-negative, it represents the desired connection timeout in seconds.</span></span> <span data-ttu-id="30815-163">如果是-1，則表示停用連接逾時的要求 (亦即，連接將永遠重新傳輸) 。</span><span class="sxs-lookup"><span data-stu-id="30815-163">If it is -1, it represents a request to disable connection timeout (i.e. the connection will retransmit forever).</span></span> <span data-ttu-id="30815-164">如果已停用連接逾時，則每次重新傳輸的重新傳輸超時會以指數方式增加到最大值60sec，然後保持在該處。</span><span class="sxs-lookup"><span data-stu-id="30815-164">If the connection timeout is disabled, the retransmit timeout increases exponentially for each retransmission up to its maximum value of 60sec and then stays there.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-165">TCP_NODELAY</span><span class="sxs-lookup"><span data-stu-id="30815-165">TCP_NODELAY</span></span></td>
<td><span data-ttu-id="30815-166">是</span><span class="sxs-lookup"><span data-stu-id="30815-166">yes</span></span></td>
<td><span data-ttu-id="30815-167">是</span><span class="sxs-lookup"><span data-stu-id="30815-167">yes</span></span></td>
<td><span data-ttu-id="30815-168">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-168">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-169">啟用或停用 TCP 通訊端的 Nagle 演算法。</span><span class="sxs-lookup"><span data-stu-id="30815-169">Enables or disables the Nagle algorithm for TCP sockets.</span></span> <span data-ttu-id="30815-170">預設會停用此選項 (設定為 FALSE) 。</span><span class="sxs-lookup"><span data-stu-id="30815-170">This option is disabled (set to FALSE) by default.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-171">TCP_TIMESTAMPS</span><span class="sxs-lookup"><span data-stu-id="30815-171">TCP_TIMESTAMPS</span></span></td>
<td><span data-ttu-id="30815-172">是</span><span class="sxs-lookup"><span data-stu-id="30815-172">yes</span></span></td>
<td><span data-ttu-id="30815-173">是</span><span class="sxs-lookup"><span data-stu-id="30815-173">yes</span></span></td>
<td><span data-ttu-id="30815-174">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-174">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-175">啟用或停用 RFC 1323 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="30815-175">Enables or disables RFC 1323 time stamps.</span></span> <span data-ttu-id="30815-176">請注意，也有時間戳記的全域設定 (預設值為 off) &quot; 、 &quot; (set/get) -nettcpsetting 中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="30815-176">Note that there is also a global configuration for timestamps (default is off), &quot;Timestamps&quot; in (set/get)-nettcpsetting.</span></span> <span data-ttu-id="30815-177">設定此通訊端選項會覆寫全域設定設定。</span><span class="sxs-lookup"><span data-stu-id="30815-177">Setting this socket option overrides that global configuration setting.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-178">TCP_FASTOPEN</span><span class="sxs-lookup"><span data-stu-id="30815-178">TCP_FASTOPEN</span></span></td>
<td><span data-ttu-id="30815-179">是</span><span class="sxs-lookup"><span data-stu-id="30815-179">yes</span></span></td>
<td><span data-ttu-id="30815-180">是</span><span class="sxs-lookup"><span data-stu-id="30815-180">yes</span></span></td>
<td><span data-ttu-id="30815-181">DWORD (布林值) </span><span class="sxs-lookup"><span data-stu-id="30815-181">DWORD (Boolean)</span></span></td>
<td><span data-ttu-id="30815-182">啟用或停用「 <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP 快速開啟」，這可讓您在開啟連線的三向交握階段期間開始傳送資料。</span><span class="sxs-lookup"><span data-stu-id="30815-182">Enables or disables <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, which enables you to start sending data during the three-way handshake phase of opening a connection.</span></span> <span data-ttu-id="30815-183">請注意，若要使用快速開啟，您應該使用 <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> 進行初始連線，並指定該函式之 <em>lpSendBuffer</em> 參數中的資料，以便在交握程式期間傳送。</span><span class="sxs-lookup"><span data-stu-id="30815-183">Note that to make use of fast opens, you should use <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> to make the initial connection, and specify data in that function's <em>lpSendBuffer</em> parameter to be transferred during the handshake process.</span></span> <span data-ttu-id="30815-184"><em>LpSendBuffer</em>中的某些資料將會以 Fast Open 通訊協定來傳送。</span><span class="sxs-lookup"><span data-stu-id="30815-184">Some of the data in <em>lpSendBuffer</em> will be transferred under the Fast Open protocol.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="30815-185">TCP_KEEPIDLE</span><span class="sxs-lookup"><span data-stu-id="30815-185">TCP_KEEPIDLE</span></span></td>
<td><span data-ttu-id="30815-186">是</span><span class="sxs-lookup"><span data-stu-id="30815-186">yes</span></span></td>
<td><span data-ttu-id="30815-187">是</span><span class="sxs-lookup"><span data-stu-id="30815-187">yes</span></span></td>
<td><span data-ttu-id="30815-188">DWORD</span><span class="sxs-lookup"><span data-stu-id="30815-188">DWORD</span></span></td>
<td><span data-ttu-id="30815-189">取得或設定在將 keepalive 探查傳送至遠端之前，TCP 連線將維持閒置的秒數。</span><span class="sxs-lookup"><span data-stu-id="30815-189">Gets or sets the number of seconds a TCP connection will remain idle before keepalive probes are sent to the remote.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="30815-190">從 Windows 10 1709 版開始，可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="30815-190">This option is available starting with Windows 10, version 1709.</span></span>
</blockquote>
<br/></td>
</tr>
<tr>
<td><span data-ttu-id="30815-191">TCP_KEEPINTVL</span><span class="sxs-lookup"><span data-stu-id="30815-191">TCP_KEEPINTVL</span></span></td>
<td><span data-ttu-id="30815-192">是</span><span class="sxs-lookup"><span data-stu-id="30815-192">yes</span></span></td>
<td><span data-ttu-id="30815-193">是</span><span class="sxs-lookup"><span data-stu-id="30815-193">yes</span></span></td>
<td><span data-ttu-id="30815-194">DWORD</span><span class="sxs-lookup"><span data-stu-id="30815-194">DWORD</span></span></td>
<td><span data-ttu-id="30815-195">取得或設定 TCP 連線在傳送另一個 keepalive 探查之前，會等候 keepalive 回應的秒數。</span><span class="sxs-lookup"><span data-stu-id="30815-195">Gets or sets the number of seconds a TCP connection will wait for a keepalive response before sending another keepalive probe.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="30815-196">從 Windows 10 1709 版開始，可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="30815-196">This option is available starting with Windows 10, version 1709.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a><span data-ttu-id="30815-197">IPPROTO TCP 選項的 Windows 支援 \_</span><span class="sxs-lookup"><span data-stu-id="30815-197">Windows support for IPPROTO\_TCP options</span></span>

| <span data-ttu-id="30815-198">選項</span><span class="sxs-lookup"><span data-stu-id="30815-198">Option</span></span> | <span data-ttu-id="30815-199">Windows 10</span><span class="sxs-lookup"><span data-stu-id="30815-199">Windows 10</span></span> | <span data-ttu-id="30815-200">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30815-200">Windows 7</span></span> | <span data-ttu-id="30815-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30815-201">Windows Server 2008</span></span> | <span data-ttu-id="30815-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30815-202">Windows Vista</span></span> |
|-|-|-|-|-|
| <span data-ttu-id="30815-203">TCP \_ BSDURGENT</span><span class="sxs-lookup"><span data-stu-id="30815-203">TCP\_BSDURGENT</span></span> | <span data-ttu-id="30815-204">x</span><span class="sxs-lookup"><span data-stu-id="30815-204">x</span></span> | <span data-ttu-id="30815-205">x</span><span class="sxs-lookup"><span data-stu-id="30815-205">x</span></span> | <span data-ttu-id="30815-206">x</span><span class="sxs-lookup"><span data-stu-id="30815-206">x</span></span> | <span data-ttu-id="30815-207">x</span><span class="sxs-lookup"><span data-stu-id="30815-207">x</span></span> |
| <span data-ttu-id="30815-208">TCP \_ 加速 \_ 1122</span><span class="sxs-lookup"><span data-stu-id="30815-208">TCP\_EXPEDITED\_1122</span></span> | <span data-ttu-id="30815-209">x</span><span class="sxs-lookup"><span data-stu-id="30815-209">x</span></span> | <span data-ttu-id="30815-210">x</span><span class="sxs-lookup"><span data-stu-id="30815-210">x</span></span> | <span data-ttu-id="30815-211">x</span><span class="sxs-lookup"><span data-stu-id="30815-211">x</span></span> | <span data-ttu-id="30815-212">x</span><span class="sxs-lookup"><span data-stu-id="30815-212">x</span></span> |
| <span data-ttu-id="30815-213">TCP \_ KEEPCNT</span><span class="sxs-lookup"><span data-stu-id="30815-213">TCP\_KEEPCNT</span></span> | <span data-ttu-id="30815-214">從 Windows 10 開始，版本1703</span><span class="sxs-lookup"><span data-stu-id="30815-214">Starting with Windows 10, version 1703</span></span> | | | |
| <span data-ttu-id="30815-215">TCP \_ MAXRT</span><span class="sxs-lookup"><span data-stu-id="30815-215">TCP\_MAXRT</span></span> | <span data-ttu-id="30815-216">x</span><span class="sxs-lookup"><span data-stu-id="30815-216">x</span></span> | <span data-ttu-id="30815-217">x</span><span class="sxs-lookup"><span data-stu-id="30815-217">x</span></span> | <span data-ttu-id="30815-218">x</span><span class="sxs-lookup"><span data-stu-id="30815-218">x</span></span> | <span data-ttu-id="30815-219">x</span><span class="sxs-lookup"><span data-stu-id="30815-219">x</span></span> |
| <span data-ttu-id="30815-220">TCP \_ NODELAY</span><span class="sxs-lookup"><span data-stu-id="30815-220">TCP\_NODELAY</span></span> | <span data-ttu-id="30815-221">x</span><span class="sxs-lookup"><span data-stu-id="30815-221">x</span></span> | <span data-ttu-id="30815-222">x</span><span class="sxs-lookup"><span data-stu-id="30815-222">x</span></span> | <span data-ttu-id="30815-223">x</span><span class="sxs-lookup"><span data-stu-id="30815-223">x</span></span> | <span data-ttu-id="30815-224">x</span><span class="sxs-lookup"><span data-stu-id="30815-224">x</span></span> |
| <span data-ttu-id="30815-225">TCP \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="30815-225">TCP\_TIMESTAMPS</span></span> | <span data-ttu-id="30815-226">x</span><span class="sxs-lookup"><span data-stu-id="30815-226">x</span></span> | <span data-ttu-id="30815-227">x</span><span class="sxs-lookup"><span data-stu-id="30815-227">x</span></span> | <span data-ttu-id="30815-228">x</span><span class="sxs-lookup"><span data-stu-id="30815-228">x</span></span> | <span data-ttu-id="30815-229">x</span><span class="sxs-lookup"><span data-stu-id="30815-229">x</span></span> |
| <span data-ttu-id="30815-230">TCP \_ FASTOPEN</span><span class="sxs-lookup"><span data-stu-id="30815-230">TCP\_FASTOPEN</span></span> | <span data-ttu-id="30815-231">從 Windows 10 開始，版本1607</span><span class="sxs-lookup"><span data-stu-id="30815-231">Starting with Windows 10, version 1607</span></span> | | | |

<br/>

 | <span data-ttu-id="30815-232">選項</span><span class="sxs-lookup"><span data-stu-id="30815-232">Option</span></span> | <span data-ttu-id="30815-233">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30815-233">Windows Server 2003</span></span> | <span data-ttu-id="30815-234">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30815-234">Windows XP</span></span> | <span data-ttu-id="30815-235">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="30815-235">Windows 2000</span></span> | <span data-ttu-id="30815-236">Windows NT4</span><span class="sxs-lookup"><span data-stu-id="30815-236">Windows NT4</span></span> | <span data-ttu-id="30815-237">Windows 9x/我</span><span class="sxs-lookup"><span data-stu-id="30815-237">Windows 9x/Me</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="30815-238">TCP \_ BSDURGENT</span><span class="sxs-lookup"><span data-stu-id="30815-238">TCP\_BSDURGENT</span></span> | <span data-ttu-id="30815-239">x</span><span class="sxs-lookup"><span data-stu-id="30815-239">x</span></span> | <span data-ttu-id="30815-240">x</span><span class="sxs-lookup"><span data-stu-id="30815-240">x</span></span> | <span data-ttu-id="30815-241">x</span><span class="sxs-lookup"><span data-stu-id="30815-241">x</span></span> | <span data-ttu-id="30815-242">x</span><span class="sxs-lookup"><span data-stu-id="30815-242">x</span></span> | |
| <span data-ttu-id="30815-243">TCP \_ 加速 \_ 1122</span><span class="sxs-lookup"><span data-stu-id="30815-243">TCP\_EXPEDITED\_1122</span></span> | <span data-ttu-id="30815-244">x</span><span class="sxs-lookup"><span data-stu-id="30815-244">x</span></span> | <span data-ttu-id="30815-245">x</span><span class="sxs-lookup"><span data-stu-id="30815-245">x</span></span> | <span data-ttu-id="30815-246">x</span><span class="sxs-lookup"><span data-stu-id="30815-246">x</span></span> | | |
| <span data-ttu-id="30815-247">TCP \_ KEEPCNT</span><span class="sxs-lookup"><span data-stu-id="30815-247">TCP\_KEEPCNT</span></span> | | | | | |
| <span data-ttu-id="30815-248">TCP \_ MAXRT</span><span class="sxs-lookup"><span data-stu-id="30815-248">TCP\_MAXRT</span></span> | | | | | |
| <span data-ttu-id="30815-249">TCP \_ NODELAY</span><span class="sxs-lookup"><span data-stu-id="30815-249">TCP\_NODELAY</span></span> | <span data-ttu-id="30815-250">x</span><span class="sxs-lookup"><span data-stu-id="30815-250">x</span></span> | <span data-ttu-id="30815-251">x</span><span class="sxs-lookup"><span data-stu-id="30815-251">x</span></span> | <span data-ttu-id="30815-252">x</span><span class="sxs-lookup"><span data-stu-id="30815-252">x</span></span> | <span data-ttu-id="30815-253">x</span><span class="sxs-lookup"><span data-stu-id="30815-253">x</span></span> | |
| <span data-ttu-id="30815-254">TCP \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="30815-254">TCP\_TIMESTAMPS</span></span> | | | | | |
| <span data-ttu-id="30815-255">TCP \_ FASTOPEN</span><span class="sxs-lookup"><span data-stu-id="30815-255">TCP\_FASTOPEN</span></span> | | | | | |

## <a name="remarks"></a><span data-ttu-id="30815-256">備註</span><span class="sxs-lookup"><span data-stu-id="30815-256">Remarks</span></span>

<span data-ttu-id="30815-257">在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中，標頭檔的組織已變更，且 **IPPROTO \_ TCP** 層級定義于 *Ws2def .h* 標頭檔中，該檔案會自動包含在 *Winsock2* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="30815-257">In the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **IPPROTO\_TCP** level is defined in the *Ws2def.h* header file which is automatically included in the *Winsock2.h* header file.</span></span> <span data-ttu-id="30815-258">**IPPROTO \_ tcp** 通訊端選項（ **tcp \_ BSDURGENT** 除外）定義于 *Ws2ipdef .h* 標頭檔中，該檔案會自動包含于 *Ws2tcpip .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="30815-258">The **IPPROTO\_TCP** socket options, with the exception of **TCP\_BSDURGENT**, are defined in the *Ws2ipdef.h* header file which is automatically included in the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="30815-259">適用于歷史原因的 **TCP \_ BSDURGENT** 選項定義于 *Mswsock .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="30815-259">The **TCP\_BSDURGENT** option for historic reasons is defined in the *Mswsock.h* header file.</span></span> <span data-ttu-id="30815-260">不應直接使用 *Ws2def .h* 和 *Ws2ipdef* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="30815-260">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="30815-261">規格需求</span><span class="sxs-lookup"><span data-stu-id="30815-261">Requirements</span></span>

| <span data-ttu-id="30815-262">需求</span><span class="sxs-lookup"><span data-stu-id="30815-262">Requirement</span></span> | <span data-ttu-id="30815-263">值</span><span class="sxs-lookup"><span data-stu-id="30815-263">Value</span></span> |
|-|-|
| <span data-ttu-id="30815-264">標頭</span><span class="sxs-lookup"><span data-stu-id="30815-264">Header</span></span> | <dl> <span data-ttu-id="30815-265"><dt>Ws2def (包含 Winsock2. h) ;</dt><dt>Windows Server 2003、WINDOWS XP 和 windows 2000 上的 Winsock2</dt></span><span class="sxs-lookup"><span data-stu-id="30815-265"><dt>Ws2def.h (include Winsock2.h); </dt> <dt>Winsock2.h on Windows Server 2003, Windows XP and Windows 2000</dt></span></span> </dl> |

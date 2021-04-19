---
description: SO \_ EXCLUSIVEADDRUSE 通訊端選項可防止其他通訊端強制系結至相同的位址和埠。
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: 'SO_EXCLUSIVEADDRUSE 通訊端選項 (Winsock2) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972032"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="05093-103">所以 \_ EXCLUSIVEADDRUSE 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="05093-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="05093-104">SO \_ EXCLUSIVEADDRUSE 通訊端選項可防止其他通訊端強制系結至相同的位址和埠。</span><span class="sxs-lookup"><span data-stu-id="05093-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="05093-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05093-105">Syntax</span></span>

<span data-ttu-id="05093-106">SO \_ EXCLUSIVEADDRUSE 選項可防止其他通訊端強制系結至相同的位址和埠，這是由 SO \_ REUSEADDR 通訊端選項所啟用的作法。</span><span class="sxs-lookup"><span data-stu-id="05093-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="05093-107">惡意應用程式可能會執行這類重複使用，以中斷應用程式。</span><span class="sxs-lookup"><span data-stu-id="05093-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="05093-108">\_EXCLUSIVEADDRUSE 選項對於需要高可用性的系統服務非常有用。</span><span class="sxs-lookup"><span data-stu-id="05093-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="05093-109">下列程式碼範例將說明如何設定這個選項。</span><span class="sxs-lookup"><span data-stu-id="05093-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="05093-110">若要有任何效果，必須在呼叫系結函式 \_ 之前[](/windows/desktop/api/winsock/nf-winsock-bind)設定 EXCLUSIVADDRUSE 選項， (這也適用于 \_ REUSEADDR 選項) 。</span><span class="sxs-lookup"><span data-stu-id="05093-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="05093-111">[表 1] 列出設定 \_ EXCLUSIVEADDRUSE 選項的效果。</span><span class="sxs-lookup"><span data-stu-id="05093-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="05093-112">萬用字元表示系結至萬用字元位址，例如0.0.0.0 （IPv4）和：：（用於 IPv6）。</span><span class="sxs-lookup"><span data-stu-id="05093-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="05093-113">特定表示系結至特定介面，例如系結指派給介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="05093-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="05093-114">Specific2 表示在特定情況下系結至特定位址，而不是系結至的位址。</span><span class="sxs-lookup"><span data-stu-id="05093-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="05093-115">只有在第一個系結以特定位址執行時，才適用 Specific2 案例;如果第一個通訊端系結至萬用字元，則特定的專案會涵蓋所有特定的位址案例。</span><span class="sxs-lookup"><span data-stu-id="05093-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="05093-116">例如，假設電腦具有兩個 IP 介面：10.0.0.1 和10.99.99.99。</span><span class="sxs-lookup"><span data-stu-id="05093-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="05093-117">如果第一次系結為10.0.0.1 和埠5150，並 \_ 設定 EXCLUSIVEADDRUSE 選項，則第二個系結至10.99.99.99 和埠5150，並設定任何或未設定任何選項。</span><span class="sxs-lookup"><span data-stu-id="05093-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="05093-118">但是，如果第一個通訊端系結至萬用字元位址 (0.0.0.0) 和埠5150，並 \_ 將 EXCLUSIVEADDRUSE 設定為，則任何後續系結至相同的埠（不論 IP 位址為何）都會失敗，並出現 WSAEADDRINUSE (10048) 或 WSAEACCESS (10013) ，這取決於第二個系結通訊端上所設定的選項。</span><span class="sxs-lookup"><span data-stu-id="05093-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="05093-119">設定各種選項的系結行為</span><span class="sxs-lookup"><span data-stu-id="05093-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="05093-120">第二個系結</span><span class="sxs-lookup"><span data-stu-id="05093-120">Second bind</span></span>

<span data-ttu-id="05093-121">第一個系結</span><span class="sxs-lookup"><span data-stu-id="05093-121">First bind</span></span>

<span data-ttu-id="05093-122">*\_EXCLUSIVEADDRUSE*</span><span class="sxs-lookup"><span data-stu-id="05093-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="05093-123">*沒有任何選項* 或 *\_ REUSEADDR*</span><span class="sxs-lookup"><span data-stu-id="05093-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="05093-124">*通 配 符*</span><span class="sxs-lookup"><span data-stu-id="05093-124">*Wildcard*</span></span>

<span data-ttu-id="05093-125">*特定*</span><span class="sxs-lookup"><span data-stu-id="05093-125">*Specific*</span></span>

<span data-ttu-id="05093-126">*通 配 符*</span><span class="sxs-lookup"><span data-stu-id="05093-126">*Wildcard*</span></span>

<span data-ttu-id="05093-127">*特定*</span><span class="sxs-lookup"><span data-stu-id="05093-127">*Specific*</span></span>

<span data-ttu-id="05093-128">$ {ROWSPAN3} $*SO \_ EXCLUSIVEADDRUSE*$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05093-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="05093-129">*通 配 符*</span><span class="sxs-lookup"><span data-stu-id="05093-129">*Wildcard*</span></span>

<span data-ttu-id="05093-130">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-130">Fail (10048)</span></span>

<span data-ttu-id="05093-131">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-131">Fail (10048)</span></span>

<span data-ttu-id="05093-132">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-132">Fail (10048)</span></span>

<span data-ttu-id="05093-133">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-133">Fail (10048)</span></span>

<span data-ttu-id="05093-134">*特定*</span><span class="sxs-lookup"><span data-stu-id="05093-134">*Specific*</span></span>

<span data-ttu-id="05093-135">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-135">Fail (10048)</span></span>

<span data-ttu-id="05093-136">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-136">Fail (10048)</span></span>

<span data-ttu-id="05093-137">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-137">Fail (10048)</span></span>

<span data-ttu-id="05093-138">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-138">Fail (10048)</span></span>

<span data-ttu-id="05093-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="05093-139">*Specific2*</span></span>

<span data-ttu-id="05093-140">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-140">n/a</span></span>

<span data-ttu-id="05093-141">Success</span><span class="sxs-lookup"><span data-stu-id="05093-141">Success</span></span>

<span data-ttu-id="05093-142">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-142">n/a</span></span>

<span data-ttu-id="05093-143">Success</span><span class="sxs-lookup"><span data-stu-id="05093-143">Success</span></span>

<span data-ttu-id="05093-144">$ {ROWSPAN3} $*No options*$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05093-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="05093-145">*通 配 符*</span><span class="sxs-lookup"><span data-stu-id="05093-145">*Wildcard*</span></span>

<span data-ttu-id="05093-146">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-146">Fail (10048)</span></span>

<span data-ttu-id="05093-147">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-147">Fail (10048)</span></span>

<span data-ttu-id="05093-148">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-148">Fail (10048)</span></span>

<span data-ttu-id="05093-149">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-149">Fail (10048)</span></span>

<span data-ttu-id="05093-150">*特定*</span><span class="sxs-lookup"><span data-stu-id="05093-150">*Specific*</span></span>

<span data-ttu-id="05093-151">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-151">Fail (10048)</span></span>

<span data-ttu-id="05093-152">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-152">Fail (10048)</span></span>

<span data-ttu-id="05093-153">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-153">Fail (10048)</span></span>

<span data-ttu-id="05093-154">失敗 (10048) </span><span class="sxs-lookup"><span data-stu-id="05093-154">Fail (10048)</span></span>

<span data-ttu-id="05093-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="05093-155">*Specific2*</span></span>

<span data-ttu-id="05093-156">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-156">n/a</span></span>

<span data-ttu-id="05093-157">Success</span><span class="sxs-lookup"><span data-stu-id="05093-157">Success</span></span>

<span data-ttu-id="05093-158">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-158">n/a</span></span>

<span data-ttu-id="05093-159">Success</span><span class="sxs-lookup"><span data-stu-id="05093-159">Success</span></span>

<span data-ttu-id="05093-160">$ {ROWSPAN3} $*SO \_ REUSEADDR*$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05093-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="05093-161">*通 配 符*</span><span class="sxs-lookup"><span data-stu-id="05093-161">*Wildcard*</span></span>

<span data-ttu-id="05093-162">失敗 (10013) </span><span class="sxs-lookup"><span data-stu-id="05093-162">Fail (10013)</span></span>

<span data-ttu-id="05093-163">失敗 (10013) </span><span class="sxs-lookup"><span data-stu-id="05093-163">Fail (10013)</span></span>

<span data-ttu-id="05093-164">成功\*</span><span class="sxs-lookup"><span data-stu-id="05093-164">Success\*</span></span>

<span data-ttu-id="05093-165">Success</span><span class="sxs-lookup"><span data-stu-id="05093-165">Success</span></span>

<span data-ttu-id="05093-166">*特定*</span><span class="sxs-lookup"><span data-stu-id="05093-166">*Specific*</span></span>

<span data-ttu-id="05093-167">失敗 (10013) </span><span class="sxs-lookup"><span data-stu-id="05093-167">Fail (10013)</span></span>

<span data-ttu-id="05093-168">失敗 (10013) </span><span class="sxs-lookup"><span data-stu-id="05093-168">Fail (10013)</span></span>

<span data-ttu-id="05093-169">Success</span><span class="sxs-lookup"><span data-stu-id="05093-169">Success</span></span>

<span data-ttu-id="05093-170">成功\*</span><span class="sxs-lookup"><span data-stu-id="05093-170">Success\*</span></span>

<span data-ttu-id="05093-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="05093-171">*Specific2*</span></span>

<span data-ttu-id="05093-172">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-172">n/a</span></span>

<span data-ttu-id="05093-173">Success</span><span class="sxs-lookup"><span data-stu-id="05093-173">Success</span></span>

<span data-ttu-id="05093-174">n/a</span><span class="sxs-lookup"><span data-stu-id="05093-174">n/a</span></span>

<span data-ttu-id="05093-175">Success</span><span class="sxs-lookup"><span data-stu-id="05093-175">Success</span></span>

<span data-ttu-id="05093-176">\* 未定義任何通訊端將接收封包的行為。</span><span class="sxs-lookup"><span data-stu-id="05093-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="05093-177">如果第一個系結未設定任何選項或 \_ REUSEADDR，而第二個系結會執行 \_ REUSEADDR，則第二個通訊端已 overtaken 埠，以及與哪些通訊端將接收封包的行為不確定。</span><span class="sxs-lookup"><span data-stu-id="05093-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="05093-178">\_為了解決這種情況，我們引進了 EXCLUSIVEADDRUSE。</span><span class="sxs-lookup"><span data-stu-id="05093-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="05093-179">在 \_ 通訊端關閉之後，不能一律立即重複使用具有 EXCLUSIVEADDRUSE 集的通訊端。</span><span class="sxs-lookup"><span data-stu-id="05093-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="05093-180">例如，如果具有獨佔旗標的接聽通訊端已設定接受接聽通訊端關閉之後的連接，則另一個通訊端無法系結至具有獨佔旗標的第一個接聽通訊端的相同埠，直到接受的連接不再使用中為止。</span><span class="sxs-lookup"><span data-stu-id="05093-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="05093-181">這種情況可能相當複雜;雖然通訊端已關閉，但基礎傳輸可能不會終止其連線。</span><span class="sxs-lookup"><span data-stu-id="05093-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="05093-182">即使在關閉通訊端之後，系統也必須傳送所有緩衝的資料、將正常的中斷連接傳送給對等，並等候對等的正常中斷連線。</span><span class="sxs-lookup"><span data-stu-id="05093-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="05093-183">因此，基礎傳輸可能永遠不會釋放連線，例如當對等通告零大小的視窗或其他這類攻擊時。</span><span class="sxs-lookup"><span data-stu-id="05093-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="05093-184">在上述範例中，在接受用戶端連線之後，接聽通訊端已關閉。</span><span class="sxs-lookup"><span data-stu-id="05093-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="05093-185">現在即使用戶端連接已關閉，如果用戶端連線因為未確認的資料而保持在作用中狀態，埠仍可能不會重複使用。</span><span class="sxs-lookup"><span data-stu-id="05093-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="05093-186">為了避免這種情況，應用程式應該確保正常關機：使用 SD SEND 旗標來呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) \_ ，然後等候 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 迴圈，直到傳回零個位元組為止。</span><span class="sxs-lookup"><span data-stu-id="05093-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="05093-187">這麼做可避免與埠重複使用相關的問題，並保證對等的所有資料都已成功接收。</span><span class="sxs-lookup"><span data-stu-id="05093-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="05093-188">\_您可以在通訊端上設定此等量選項，以防止埠進入其中一個作用中的等候狀態; 不過，不建議這麼做，因為它可能會導致不想要的效果，因為這可能會導致連線重設。</span><span class="sxs-lookup"><span data-stu-id="05093-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="05093-189">例如，如果已接收資料，但對等尚未認可資料，而且本機電腦關閉具有此設定的資料 \_ 集，則會重設連線，對等會捨棄未認可的資料。</span><span class="sxs-lookup"><span data-stu-id="05093-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="05093-190">此外，挑選適當的時間來進行逗留很困難;值太小會導致許多已中止的連線，而較大的超時可能會讓系統容易遭受拒絕服務的攻擊，方法是建立許多連接，進而拖延許多應用程式執行緒。</span><span class="sxs-lookup"><span data-stu-id="05093-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="05093-191">使用 EXCLUSIVEADDRUSE 選項的通訊端 \_ 必須在關閉之前適當地關閉。</span><span class="sxs-lookup"><span data-stu-id="05093-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="05093-192">如果相關聯的服務需要重新開機，則無法這樣做可能會造成阻絕服務攻擊。</span><span class="sxs-lookup"><span data-stu-id="05093-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05093-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="05093-193">Requirements</span></span>



| <span data-ttu-id="05093-194">需求</span><span class="sxs-lookup"><span data-stu-id="05093-194">Requirement</span></span> | <span data-ttu-id="05093-195">值</span><span class="sxs-lookup"><span data-stu-id="05093-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05093-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05093-196">Minimum supported client</span></span><br/> | <span data-ttu-id="05093-197">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05093-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="05093-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05093-198">Minimum supported server</span></span><br/> | <span data-ttu-id="05093-199">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05093-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05093-200">標頭</span><span class="sxs-lookup"><span data-stu-id="05093-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="05093-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="05093-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 





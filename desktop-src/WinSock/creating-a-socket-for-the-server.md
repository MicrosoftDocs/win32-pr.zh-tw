---
description: 初始化之後，必須具現化通訊端物件以供伺服器使用。
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: 建立伺服器的通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113089"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="7e95c-103">建立伺服器的通訊端</span><span class="sxs-lookup"><span data-stu-id="7e95c-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="7e95c-104">初始化之後，必須具現化 **通訊端** 物件以供伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="7e95c-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="7e95c-105">**若要建立伺服器的通訊端**</span><span class="sxs-lookup"><span data-stu-id="7e95c-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="7e95c-106">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數是用來判斷 [**sockaddr**](sockaddr-2.md)結構中的值：</span><span class="sxs-lookup"><span data-stu-id="7e95c-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="7e95c-107">**AF \_INET** 用來指定 IPv4 位址系列。</span><span class="sxs-lookup"><span data-stu-id="7e95c-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="7e95c-108">**SOCK \_串流** 是用來指定資料流程通訊端。</span><span class="sxs-lookup"><span data-stu-id="7e95c-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="7e95c-109">**IPPROTO \_TCP** 用來指定 tcp 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7e95c-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="7e95c-110">**AI \_被動式** 旗標表示呼叫端要在系結函式的呼叫中使用 [**傳回的套**](/windows/desktop/api/winsock/nf-winsock-bind) 接字位址結構。</span><span class="sxs-lookup"><span data-stu-id="7e95c-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="7e95c-111">當 **AI \_ 被動** 旗標已設定，而且 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函式的 *nodename* 參數為 **Null** 指標時，通訊端位址結構的 IP 位址部分會設定為 IPv4 位址的 **INADDR \_ any** ，或 **IN6ADDR \_ 任何 \_ INIT** 的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="7e95c-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="7e95c-112">27015是與用戶端所連接之伺服器相關聯的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7e95c-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="7e95c-113">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數會使用 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)結構。</span><span class="sxs-lookup"><span data-stu-id="7e95c-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="7e95c-114">建立名為 ListenSocket 的 **通訊端** 物件，讓伺服器接聽用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="7e95c-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="7e95c-115">呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式，並將其值傳回給 ListenSocket 變數。</span><span class="sxs-lookup"><span data-stu-id="7e95c-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="7e95c-116">針對此伺服器應用程式，請使用符合 *提示* 參數中指定的位址系列、通訊端類型和通訊協定的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)呼叫所傳回的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="7e95c-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="7e95c-117">在此範例中，會使用 IPv4 的位址系列、SOCK 資料流程的通訊端類型以及 IPPROTO TCP 的通訊協定來要求 IPv4 的 TCP 串流通訊端 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7e95c-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="7e95c-118">因此，會要求 ListenSocket 的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="7e95c-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="7e95c-119">如果伺服器應用程式想要接聽 IPv6，則必須 \_ 在 *提示* 參數中將位址家族設定為 AF INET6。</span><span class="sxs-lookup"><span data-stu-id="7e95c-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="7e95c-120">如果伺服器想要同時接聽 IPv6 和 IPv4，則必須建立兩個接聽通訊端，一個用於 IPv6，另一個用於 IPv4。</span><span class="sxs-lookup"><span data-stu-id="7e95c-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="7e95c-121">這兩個通訊端必須由應用程式分開處理。</span><span class="sxs-lookup"><span data-stu-id="7e95c-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="7e95c-122">Windows Vista 和更新版本可讓您建立單一 IPv6 通訊端，以雙重堆疊模式來接聽 IPv6 和 IPv4。</span><span class="sxs-lookup"><span data-stu-id="7e95c-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="7e95c-123">如需這項功能的詳細資訊，請參閱 [雙重堆疊通訊端](dual-stack-sockets.md)。</span><span class="sxs-lookup"><span data-stu-id="7e95c-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="7e95c-124">檢查是否有錯誤，以確定通訊端是有效的通訊端。</span><span class="sxs-lookup"><span data-stu-id="7e95c-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="7e95c-125">下一步：系 [結通訊端](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="7e95c-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e95c-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e95c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e95c-127">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="7e95c-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="7e95c-128">初始化 Winsock</span><span class="sxs-lookup"><span data-stu-id="7e95c-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="7e95c-129">Winsock 伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="7e95c-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 

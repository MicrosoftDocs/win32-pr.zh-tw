---
description: IPv6 支援、TCP/IP 附錄和 Windows 通訊端。
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: IPv6 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113052"
---
# <a name="ipv6-support"></a><span data-ttu-id="74729-103">IPv6 支援</span><span class="sxs-lookup"><span data-stu-id="74729-103">IPv6 Support</span></span>

<span data-ttu-id="74729-104">為了在 Windows XP Service Pack 1 上支援 IPv4 和 IPv6 (SP1) 和 Windows Server 2003 上的應用程式，應用程式必須建立兩個通訊端，一個通訊端用於 IPv4，另一個通訊端用於 IPv6。</span><span class="sxs-lookup"><span data-stu-id="74729-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="74729-105">這兩個通訊端必須由應用程式分開處理。</span><span class="sxs-lookup"><span data-stu-id="74729-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="74729-106">如果 Windows XP SP1 和 Windows Server 2003 上的 TCP/IP 服務提供者支援 IPv4 和 IPv6 位址，則必須建立兩個不同的通訊端，並在這些通訊端上分開接聽：</span><span class="sxs-lookup"><span data-stu-id="74729-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="74729-107">適用于 IPv4 的一次。</span><span class="sxs-lookup"><span data-stu-id="74729-107">Once for IPv4.</span></span>
-   <span data-ttu-id="74729-108">IPv6 位址系列的一次。</span><span class="sxs-lookup"><span data-stu-id="74729-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="74729-109">Windows Vista 和更新版本可讓您建立單一 IPv6 通訊端，以同時處理 IPv6 和 IPv4 流量。</span><span class="sxs-lookup"><span data-stu-id="74729-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="74729-110">例如，會建立 IPv6 的 TCP 接聽通訊端，並進入雙堆疊模式，並系結至埠5001。</span><span class="sxs-lookup"><span data-stu-id="74729-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="74729-111">此雙重堆疊通訊端可以接受從連線到埠5001的 IPv6 TCP 用戶端，以及從連線到埠5001的 IPv4 TCP 用戶端的連線。</span><span class="sxs-lookup"><span data-stu-id="74729-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="74729-112">這項功能可大幅簡化應用程式設計，並減少在兩個不同的通訊端上張貼作業所需的資源負擔。</span><span class="sxs-lookup"><span data-stu-id="74729-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="74729-113">不過，必須符合一些限制才能使用雙重堆疊通訊端。</span><span class="sxs-lookup"><span data-stu-id="74729-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="74729-114">如需詳細資訊，請參閱 [雙重堆疊通訊端](dual-stack-sockets.md)。</span><span class="sxs-lookup"><span data-stu-id="74729-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="74729-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 會針對每個支援的通訊端類型傳回兩個 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構 (SOCK \_ STREAM、SOCK \_ DGRAM、SOCK \_ RAW) 。</span><span class="sxs-lookup"><span data-stu-id="74729-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="74729-116">**IAddressFamily** 必須設定為 af \_ INET，才能進行 IPv4 定址，並設定為 Af \_ INET6 進行 IPv6 定址。</span><span class="sxs-lookup"><span data-stu-id="74729-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="74729-117">下列結構描述 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="74729-117">The IPv6 addresses are described in the following structures.</span></span>

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

<span data-ttu-id="74729-118">如果應用程式使用 Windows 通訊端1.1 函式，而且想要使用 IPv6 位址，它可能會繼續使用所有舊的函 [**式，這些**](/windows/desktop/api/winsock/nf-winsock-bind)函式會採用 [**sockaddr**](sockaddr-2.md)結構作為其中一個參數 (系結、[**連接**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)和 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)、[**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept)等等) 。</span><span class="sxs-lookup"><span data-stu-id="74729-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="74729-119">唯一需要的變更是 **\_ 在中** 使用 **sockaddr \_ in6** ，而不是 sockaddr。</span><span class="sxs-lookup"><span data-stu-id="74729-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="74729-120">不過，名稱解析函式 ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)、 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)等) 和位址轉換函式 ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)， [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) 無法重複使用，因為它們假設 IP 位址的長度是4個位元組。</span><span class="sxs-lookup"><span data-stu-id="74729-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="74729-121">如果應用程式想要執行 IPv6 位址的名稱解析和位址轉換，則必須使用 Windows 通訊端2特定的功能。</span><span class="sxs-lookup"><span data-stu-id="74729-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="74729-122">引進許多新功能，讓 Windows 通訊端2應用程式能夠利用 IPv6，包括 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 功能。</span><span class="sxs-lookup"><span data-stu-id="74729-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="74729-123">如需有關如何在應用程式中啟用 IPv6 功能的詳細資訊，請參閱 [Windows 通訊端應用程式的 Ipv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)。</span><span class="sxs-lookup"><span data-stu-id="74729-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 

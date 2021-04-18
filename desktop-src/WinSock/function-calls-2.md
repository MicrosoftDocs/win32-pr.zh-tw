---
description: Windows 通訊端介面引進了新的功能，其設計目的是要讓 Windows 通訊端程式設計更容易。 這些新的 Windows 通訊端函式的優點之一，就是 IPv6 和 IPv4 的整合支援。
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: IPv6 Winsock 應用程式的函式呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971209"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="fb5ae-104">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="fb5ae-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="fb5ae-105">Windows 通訊端介面引進了新的功能，其設計目的是要讓 Windows 通訊端程式設計更容易。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="fb5ae-106">這些新的 Windows 通訊端函式的優點之一，就是 IPv6 和 IPv4 的整合支援。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="fb5ae-107">這些新的 Windows 通訊端功能包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="fb5ae-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="fb5ae-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="fb5ae-109">**WSAConnectByList**</span><span class="sxs-lookup"><span data-stu-id="fb5ae-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="fb5ae-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 系列函數 (**getaddrinfo**、 [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)、 [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)、 [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo)、 [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex)、 [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)和 [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa)) </span><span class="sxs-lookup"><span data-stu-id="fb5ae-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="fb5ae-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 系列函數 (**getnameinfo** 和 [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)) </span><span class="sxs-lookup"><span data-stu-id="fb5ae-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="fb5ae-112">此外，已新增新的 IP Helper 函式，同時支援 IPv6 和 IPv4，以簡化 Windows 通訊端程式設計。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="fb5ae-113">這些新的 IP Helper 函式包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="fb5ae-114">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="fb5ae-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="fb5ae-115">將 IPv6 支援新增至應用程式時，應使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="fb5ae-116">您可以使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ，透過指定的主機名稱和埠建立端點的連接。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="fb5ae-117">**WSAConnectByName** 函式可在 Windows Vista 和更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="fb5ae-118">您可以使用 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 來建立一組目的地位址（)  (主機名稱和埠）所代表之可能端點集合中的一個連接。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="fb5ae-119">**WSAConnectByList** 函式可在 Windows Vista 和更新版本上使用。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="fb5ae-120">使用其中一個新的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows 通訊端函數呼叫來取代 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="fb5ae-121">具有 IPv6 通訊協定支援的 **getaddrinfo** 函式可在 Windows XP 和更新版本上取得。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="fb5ae-122">當安裝適用于 Windows 2000 的 IPv6 技術預覽時，Windows 2000 也支援 IPv6 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="fb5ae-123">使用其中一個新的 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows 通訊端函數呼叫來取代 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="fb5ae-124">具有 IPv6 通訊協定支援的 **getnameinfo** 函式可在 Windows XP 和更新版本上取得。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="fb5ae-125">當安裝適用于 Windows 2000 的 IPv6 技術預覽時，Windows 2000 也支援 IPv6 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="fb5ae-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="fb5ae-126">WSAConnectByName</span></span>

<span data-ttu-id="fb5ae-127">[**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)函式會使用以資料流程為基礎的通訊端，將目的地的主機名稱或 IP 位址 (IPv4 或 IPv6) ，以簡化連接至端點的程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="fb5ae-128">此函式會減少建立 IP 應用程式所需的原始程式碼，此應用程式與所使用的 IP 通訊協定版本無關。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="fb5ae-129">**WSAConnectByName** 會將一般 TCP 應用程式中的下列步驟取代為單一函式呼叫：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="fb5ae-130">將主機名稱解析為一組 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="fb5ae-131">針對每個 IP 位址：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-131">For each IP address:</span></span>
    -   <span data-ttu-id="fb5ae-132">建立適當位址系列的通訊端。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="fb5ae-133">嘗試連接到遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="fb5ae-134">如果連接成功，則會傳回;否則會嘗試主機的下一個遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="fb5ae-135">[**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)函式不僅會解析名稱，還會嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="fb5ae-136">此函數會使用名稱解析和所有本機電腦的來源 IP 位址所傳回的所有遠端位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="fb5ae-137">它會先嘗試使用位址組進行連線，並獲得最高的成功機會。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="fb5ae-138">因此， **WSAConnectByName** 不僅可確保建立連接，還能將建立連線的時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="fb5ae-139">若要同時啟用 IPv6 和 IPv4 通訊，請使用下列方法：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="fb5ae-140">您必須在為 AF INET6 位址系列建立的通訊端上呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式 \_ ，才能在呼叫 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)之前停用 **IPV6 \_ V6ONLY** 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="fb5ae-141">這是藉由呼叫通訊端上的 **setsockopt** 函數，並 *將 level* 參數設定為 **IPPROTO \_ IPV6** (請參閱 [IPPROTO \_ ipv6 通訊端選項](ipproto-ipv6-socket-options.md)) 、將 *optname* 參數設定為 **IPV6 \_ V6ONLY**，以及將 *optvalue* 參數值設定為零。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="fb5ae-142">如果應用程式需要系結至特定的本機位址或埠，則無法使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ，因為 **WSAConnectByName** 的 socket 參數必須是未系結的通訊端。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="fb5ae-143">下列程式碼範例只會顯示需要幾行程式碼，才能使用此函式來執行與 IP 版本無關的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="fb5ae-144">使用 WSAConnectByName 建立連接[ ](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="fb5ae-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="fb5ae-145">WSAConnectByList</span><span class="sxs-lookup"><span data-stu-id="fb5ae-145">WSAConnectByList</span></span>

<span data-ttu-id="fb5ae-146">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)函式會根據一組目的地 IP 位址和埠) ，來建立與主機的連線 (。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="fb5ae-147">此函式會取得端點的所有 IP 位址和埠，以及所有本機電腦的 IP 位址，並使用所有可能的位址組合來嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="fb5ae-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 與 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 函數有關。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="fb5ae-149">**WSAConnectByList** 會接受主機清單 (目的地位址和埠) 配對，而不是採用單一主機名稱，而是會連接到所提供清單中的其中一個位址和埠。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="fb5ae-150">此功能的設計目的是要支援應用程式必須從潛在主機清單中連接到任何可用主機的案例。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="fb5ae-151">類似于 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)， [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 函式可大幅減少建立、系結和連接通訊端所需的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="fb5ae-152">這項功能可讓您更輕鬆地執行與 IP 版本無關的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="fb5ae-153">此函式所接受的主機位址清單可能是 IPv6 或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="fb5ae-154">若要同時在函式接受的單一通訊清單中傳遞 IPv6 和 IPv4 位址，必須先執行下列步驟，然後再呼叫函式：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="fb5ae-155">您必須在為 AF INET6 位址系列建立的通訊端上呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式 \_ ，才能在呼叫 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)之前停用 **IPV6 \_ V6ONLY** 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="fb5ae-156">這是藉由呼叫通訊端上的 **setsockopt** 函數，並 *將 level* 參數設定為 **IPPROTO \_ IPV6** (請參閱 [IPPROTO \_ ipv6 通訊端選項](ipproto-ipv6-socket-options.md)) 、將 *optname* 參數設定為 **IPV6 \_ V6ONLY**，以及將 *optvalue* 參數值設定為零。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="fb5ae-157">任何 IPv4 位址都必須以 IPv4 對應的 IPv6 位址格式表示，讓 IPv6 的應用程式能夠與 IPv4 節點進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="fb5ae-158">IPv4 對應的 IPv6 位址格式允許 IPv4 節點的 IPv4 位址以 IPv6 位址表示。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="fb5ae-159">IPv4 位址會編碼為 IPv6 位址的低序位32位，而高序位96位會保存固定的前置詞0：0：0：0：0： FFFF。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="fb5ae-160">IPv4 對應的 IPv6 位址格式是在 RFC 4291 中指定的。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="fb5ae-161">如需詳細資訊，請參閱 [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291)。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="fb5ae-162">\_ *Mstcpip* 中的 IN6ADDR SETV4MAPPED 宏可以用來將 ipv4 位址轉換為所需的 ipv4 對應 IPv6 位址格式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="fb5ae-163">使用 WSAConnectByList 建立連接[ ](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="fb5ae-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="fb5ae-164">getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="fb5ae-164">getaddrinfo</span></span>

<span data-ttu-id="fb5ae-165">**Getaddrinfo** 函數也會執行許多函數的處理工作。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="fb5ae-166">之前，需要對許多 Windows 通訊端函式進行呼叫，以建立、開啟，然後將位址系結至通訊端。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="fb5ae-167">使用 **getaddrinfo** 函式時，執行這類工作所需的源程式碼可大幅減少。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="fb5ae-168">下列兩個範例說明使用和不使用 **getaddrinfo** 函式執行這些工作所需的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="fb5ae-169">使用 **getaddrinfo** 執行 Open、Connect 和 Bind</span><span class="sxs-lookup"><span data-stu-id="fb5ae-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="fb5ae-170">在不使用 **getaddrinfo** 的情況下，執行 Open、Connect 和 Bind</span><span class="sxs-lookup"><span data-stu-id="fb5ae-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="fb5ae-171">請注意，這兩個原始程式碼範例都會執行相同的工作，但第一個範例是使用 **getaddrinfo** 函式，需要較少的原始程式碼，並且可以處理 IPv6 或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="fb5ae-172">使用 **getaddrinfo** 函數刪除的源程式碼數會有所不同。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="fb5ae-173">在實際執行的原始程式碼中，您的應用程式會逐一查看 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 或 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函數所傳回的一組位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="fb5ae-174">這些範例會略過此步驟，以利簡化。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="fb5ae-175">在修改現有的 IPv4 應用程式以支援 IPv6 時，您必須解決的另一個問題是，與呼叫函式的順序相關聯。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="fb5ae-176">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)和 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)都需要以特定順序進行函式呼叫的順序。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="fb5ae-177">在同時使用 IPv4 和 IPv6 的平臺上，不會事先知道遠端主機名的位址系列。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="fb5ae-178">因此，必須先執行使用 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式的位址解析，以判斷遠端主機的 IP 位址和位址系列。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="fb5ae-179">然後，您可以呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式來開啟 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)所傳回之位址系列的通訊端。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="fb5ae-180">這是 Windows 通訊端應用程式撰寫方式的重要變更，因為許多 IPv4 應用程式傾向于使用不同的函式呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="fb5ae-181">大部分的 IPv4 應用程式首先會建立 AF \_ INET 位址系列的通訊端，然後進行名稱解析，然後使用通訊端連線到已解析的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="fb5ae-182">當您使這類應用程式具備 IPv6 能力時，必須先延遲 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式呼叫，才能在 deteremined 位址系列時進行名稱解析。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="fb5ae-183">請注意，如果名稱解析同時傳回 IPv4 和 IPv6 位址，則必須使用個別的 IPv4 和 IPv6 通訊端來連接這些目的地位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="fb5ae-184">您可以使用 Windows Vista 和更新版本上的 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 功能來避免這些複雜性，讓應用程式開發人員可以使用這個新的函式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="fb5ae-185">下列程式碼範例會顯示正確的順序來執行名稱解析，先 (在下列原始程式碼範例的第四行中執行) ，然後在下列程式碼範例) 的<sup>第19行</sup> 中開啟通訊端 (執行。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="fb5ae-186">此範例是在附錄 B 中，已 [啟用 IPv6 的用戶端程式代碼](ipv6-enabled-client-code-2.md) 中找到的用戶端 .c 檔案摘錄。下列程式碼範例中所呼叫的 PrintError 函式會列在用戶端 .c 範例中。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="fb5ae-187">IP 協助程式函式</span><span class="sxs-lookup"><span data-stu-id="fb5ae-187">IP Helper Functions</span></span>

<span data-ttu-id="fb5ae-188">最後，使用 IP 協助程式函式 [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)的應用程式及其相關聯的結構 [**IP \_ 介面卡 \_ 資訊**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)，必須辨識此函式和結構僅限於 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="fb5ae-189">此函式和結構的啟用 IPv6 的取代為 [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) 函式和 [**IP \_ 介面卡 \_ 位址**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) 結構。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="fb5ae-190">使用 IP 協助程式 API 的已啟用 IPv6 的應用程式，應該使用 **GetAdaptersAddresses** 函式和對應的已啟用 ipv6 **IP \_ 介面卡 \_ 位址** 結構（兩者都定義于 Microsoft Windows 軟體開發套件 (SDK) ）。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="fb5ae-191">建議</span><span class="sxs-lookup"><span data-stu-id="fb5ae-191">Recommendations</span></span>

<span data-ttu-id="fb5ae-192">確保您的應用程式使用 IPv6 相容函式呼叫的最佳方法是使用 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式來取得主機對位址轉譯。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="fb5ae-193">從 Windows XP 開始， **getaddrinfo** 函式會讓 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 函式變得不必要，因此您的應用程式應該改為使用 **getaddrinfo** 函式來進行未來的程式設計專案。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="fb5ae-194">雖然 Microsoft 會繼續支援 **gethostbyname**，但不會擴充此功能以支援 IPv6。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="fb5ae-195">如需取得 IPv6 和 IPv4 主機資訊的透明支援，您必須使用 **getaddrinfo**。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="fb5ae-196">下列範例示範如何使用 **getaddrinfo** 函數。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="fb5ae-197">請注意，如下列範例所示，此函式會適當地處理 IPv6 和 IPv4 的主機對位址轉譯，但它也會取得主機的其他有用資訊，例如支援的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="fb5ae-198">此範例是來自于附錄 B 中所找到的用戶端 c 範例摘要。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="fb5ae-199">支援 IPv6 的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式版本是 windows XP 版 windows 的新功能。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="fb5ae-200">要避免的程式碼</span><span class="sxs-lookup"><span data-stu-id="fb5ae-200">Code to Avoid</span></span>

<span data-ttu-id="fb5ae-201">傳統上使用 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 函式來達成主機位址轉換。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="fb5ae-202">從 Windows XP 開始：</span><span class="sxs-lookup"><span data-stu-id="fb5ae-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="fb5ae-203">**Getaddrinfo** 函式會讓 **gethostbyname** 函式過時。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="fb5ae-204">您的應用程式應該使用 **getaddrinfo** 函式，而不是 **gethostbyname** 函數。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="fb5ae-205">編寫工作的程式碼</span><span class="sxs-lookup"><span data-stu-id="fb5ae-205">Coding Tasks</span></span>

<span data-ttu-id="fb5ae-206">**若要修改現有的 IPv4 應用程式以新增 IPv6 的支援**</span><span class="sxs-lookup"><span data-stu-id="fb5ae-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="fb5ae-207">取得 Checkv4.exe 公用程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="fb5ae-208">此公用程式會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="fb5ae-209">Windows SDK 可透過 MSDN 訂閱取得，也可以從 Microsoft 網站 (下載 https://msdn.microsoft.com) 。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="fb5ae-210">舊版的 *Checkv4.exe* 工具也隨附于 Windows 2000 的 Microsoft IPv6 技術預覽中。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="fb5ae-211">針對您的程式碼執行 *Checkv4.exe* 公用程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="fb5ae-212">請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md) 來瞭解如何針對您的檔案執行版本公用程式。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="fb5ae-213">此公用程式會警示您使用 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)、 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)和其他僅限 IPv4 的函式，並提供如何以與 IPv6 相容的函式（例如 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)）取代這些函式的建議。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="fb5ae-214">使用 **getaddrinfo** 函數，將 **gethostbyname** 函式的任何實例和相關聯的程式碼取代為適當的。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="fb5ae-215">在 Windows Vista 上，請在適當的情況下使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 或 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 函數。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="fb5ae-216">使用 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)函數，將 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式的任何實例和相關聯的程式碼取代為適當的。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="fb5ae-217">或者，您可以在程式碼基底中搜尋 **gethostbyname** 和 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) 函式的實例，並視需要將所有 (和其他相關聯的程式碼) 變更為 **getaddrinfo** 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="fb5ae-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb5ae-218">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb5ae-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb5ae-219">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="fb5ae-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="fb5ae-220">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="fb5ae-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="fb5ae-221">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="fb5ae-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="fb5ae-222">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="fb5ae-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="fb5ae-223">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="fb5ae-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="fb5ae-224">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="fb5ae-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 

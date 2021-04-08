---
description: 初始化之後，必須具現化通訊端物件以供用戶端使用。
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: 建立用戶端的通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848020"
---
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="8ea8b-103">建立用戶端的通訊端</span><span class="sxs-lookup"><span data-stu-id="8ea8b-103">Creating a socket for the client</span></span>

<span data-ttu-id="8ea8b-104">初始化之後，必須具現化 **通訊端** 物件以供用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="8ea8b-105">**建立通訊端**</span><span class="sxs-lookup"><span data-stu-id="8ea8b-105">**To create a socket**</span></span>

1.  <span data-ttu-id="8ea8b-106">宣告包含 [**sockaddr**](sockaddr-2.md)結構的 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)物件，並將這些值初始化。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="8ea8b-107">針對此應用程式，未指定網際網路位址系列，因此可以傳回 IPv6 或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="8ea8b-108">應用程式要求通訊端類型為 TCP 通訊協定的資料流程通訊端。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="8ea8b-109">呼叫 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函數，要求在命令列上傳遞的伺服器名稱的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="8ea8b-110">用戶端將連線之伺服器上的 TCP 埠， \_ 在此範例中是以27015的預設埠定義。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="8ea8b-111">**Getaddrinfo** 函式會將其值傳回為已檢查錯誤的整數。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  <span data-ttu-id="8ea8b-112">建立名為 ConnectSocket 的 **通訊端** 物件。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="8ea8b-113">呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式，並將其值傳回給 ConnectSocket 變數。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="8ea8b-114">針對此應用程式，請使用符合 *提示* 參數中指定的位址系列、通訊端類型和通訊協定的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)呼叫所傳回的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="8ea8b-115">在此範例中，TCP 資料流程通訊端是使用 SOCK 資料流程的通訊端類型 \_ 以及 IPPROTO TCP 的通訊協定所指定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="8ea8b-116">位址系列未指定 (AF \_ UNSPEC) ，因此傳回的 IP 位址可能是伺服器的 IPv6 或 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="8ea8b-117">如果用戶端應用程式只想要使用 IPv6 或 IPv4 進行連線，則必須在提示參數中將位址家族設定為適用于 IPv6 的 AF \_ INET6 或適用于 ipv4 的 af \_ INET。 </span><span class="sxs-lookup"><span data-stu-id="8ea8b-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="8ea8b-118">檢查是否有錯誤，以確定通訊端是有效的通訊端。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="8ea8b-119">您可以針對不同的執行方式變更傳遞至 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數的參數。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="8ea8b-120">錯誤偵測是成功網路程式碼的重要部分。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="8ea8b-121">如果 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 呼叫失敗，則會傳回不正確 \_ 通訊端。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="8ea8b-122">先前程式碼中的 **if** 語句會用來攔截建立通訊端時可能發生的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="8ea8b-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回與最後發生之錯誤相關聯的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="8ea8b-124">視應用程式而定，可能需要更廣泛的錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="8ea8b-125">例如，將 *hints.ai_family* 設定為 **AF_UNSPEC** 可能會導致連接呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="8ea8b-126">如果發生這種情況，請改用特定的 IPv4 (**AF_INET**) 或 IPv6 (**AF_INET6**) 值。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="8ea8b-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 用來終止 WS2 \_ 32 DLL 的使用。</span><span class="sxs-lookup"><span data-stu-id="8ea8b-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="8ea8b-128">下一步： [連接至通訊端](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="8ea8b-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ea8b-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ea8b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea8b-130">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="8ea8b-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="8ea8b-131">初始化 Winsock</span><span class="sxs-lookup"><span data-stu-id="8ea8b-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="8ea8b-132">Winsock 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="8ea8b-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 

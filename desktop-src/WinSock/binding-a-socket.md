---
description: 若要讓伺服器接受用戶端連線，它必須系結至系統內的網路位址。
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: 系結通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970606"
---
# <a name="binding-a-socket"></a><span data-ttu-id="70cb9-103">系結通訊端</span><span class="sxs-lookup"><span data-stu-id="70cb9-103">Binding a Socket</span></span>

<span data-ttu-id="70cb9-104">若要讓伺服器接受用戶端連線，它必須系結至系統內的網路位址。</span><span class="sxs-lookup"><span data-stu-id="70cb9-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="70cb9-105">下列程式碼示範如何將已建立的通訊端系結至 IP 位址和埠。</span><span class="sxs-lookup"><span data-stu-id="70cb9-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="70cb9-106">用戶端應用程式會使用 IP 位址和埠來連接至主機網路。</span><span class="sxs-lookup"><span data-stu-id="70cb9-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="70cb9-107">系結通訊端</span><span class="sxs-lookup"><span data-stu-id="70cb9-107">To bind a socket</span></span>

<span data-ttu-id="70cb9-108">[**Sockaddr**](sockaddr-2.md)結構會保存位址系列、IP 位址和埠號碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="70cb9-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="70cb9-109">呼叫系 [](/windows/desktop/api/winsock/nf-winsock-bind)結函式，將從 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函式傳回的已建立 **通訊端** 和 [**sockaddr**](sockaddr-2.md)結構作為參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="70cb9-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="70cb9-110">檢查是否有一般錯誤。</span><span class="sxs-lookup"><span data-stu-id="70cb9-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="70cb9-111">一旦呼叫 [](/windows/desktop/api/winsock/nf-winsock-bind)系結函式，就不再需要 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數所傳回的位址資訊。</span><span class="sxs-lookup"><span data-stu-id="70cb9-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="70cb9-112">呼叫 [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) 函式來釋放 **getaddrinfo** 函式針對此位址資訊所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="70cb9-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="70cb9-113">下一步： [在通訊端上接聽](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="70cb9-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="70cb9-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="70cb9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70cb9-115">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="70cb9-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="70cb9-116">Winsock 伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="70cb9-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="70cb9-117">建立伺服器的通訊端</span><span class="sxs-lookup"><span data-stu-id="70cb9-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 




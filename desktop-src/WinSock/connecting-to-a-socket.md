---
description: 用戶端必須連接到伺服器，用戶端才能在網路上進行通訊。
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: 連接至通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972037"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="2f18d-103">連接至通訊端</span><span class="sxs-lookup"><span data-stu-id="2f18d-103">Connecting to a Socket</span></span>

<span data-ttu-id="2f18d-104">用戶端必須連接到伺服器，用戶端才能在網路上進行通訊。</span><span class="sxs-lookup"><span data-stu-id="2f18d-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="2f18d-105">連接至通訊端</span><span class="sxs-lookup"><span data-stu-id="2f18d-105">To connect to a socket</span></span>

<span data-ttu-id="2f18d-106">呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式，並將建立的通訊端和 [**sockaddr**](sockaddr-2.md) 結構作為參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="2f18d-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="2f18d-107">檢查是否有一般錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f18d-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="2f18d-108">[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數是用來判斷 [**sockaddr**](sockaddr-2.md)結構中的值。</span><span class="sxs-lookup"><span data-stu-id="2f18d-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="2f18d-109">在此範例中， **getaddrinfo** 函數所傳回的第一個 IP 位址會用來指定傳遞給 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)的 **sockaddr** 結構。</span><span class="sxs-lookup"><span data-stu-id="2f18d-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="2f18d-110">如果 **連接** 呼叫失敗至第一個 IP 位址，請嘗試從 **getaddrinfo** 函數傳回的連結清單中的下一個 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)結構。</span><span class="sxs-lookup"><span data-stu-id="2f18d-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="2f18d-111">[**Sockaddr**](sockaddr-2.md)結構中指定的資訊包括：</span><span class="sxs-lookup"><span data-stu-id="2f18d-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="2f18d-112">用戶端將嘗試連接之伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2f18d-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="2f18d-113">用戶端將連接之伺服器上的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2f18d-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="2f18d-114">當用戶端呼叫 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式時，此埠已指定為埠27015。</span><span class="sxs-lookup"><span data-stu-id="2f18d-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="2f18d-115">下一步： [在用戶端上傳送和接收資料](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="2f18d-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f18d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f18d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f18d-117">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="2f18d-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="2f18d-118">Winsock 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="2f18d-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="2f18d-119">建立用戶端的通訊端</span><span class="sxs-lookup"><span data-stu-id="2f18d-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 

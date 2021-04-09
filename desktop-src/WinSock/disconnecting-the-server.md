---
description: 一旦伺服器完成從用戶端接收資料，並將資料傳送回用戶端之後，伺服器會中斷與用戶端的連線，並關閉通訊端。
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: 中斷伺服器的連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848018"
---
# <a name="disconnecting-the-server"></a><span data-ttu-id="c2a26-103">中斷伺服器的連線</span><span class="sxs-lookup"><span data-stu-id="c2a26-103">Disconnecting the Server</span></span>

<span data-ttu-id="c2a26-104">一旦伺服器完成從用戶端接收資料，並將資料傳送回用戶端之後，伺服器會中斷與用戶端的連線，並關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="c2a26-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="c2a26-105">**中斷和關閉通訊端**</span><span class="sxs-lookup"><span data-stu-id="c2a26-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="c2a26-106">當伺服器完成將資料傳送至用戶端時，可以呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) \_ 傳送來指定 SD SEND，以關閉通訊端的傳送端。</span><span class="sxs-lookup"><span data-stu-id="c2a26-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="c2a26-107">這可讓用戶端釋放此通訊端的部分資源。</span><span class="sxs-lookup"><span data-stu-id="c2a26-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="c2a26-108">伺服器應用程式仍然可以接收通訊端上的資料。</span><span class="sxs-lookup"><span data-stu-id="c2a26-108">The server application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="c2a26-109">當用戶端應用程式完成接收資料時，會呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="c2a26-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="c2a26-110">使用 Windows 通訊端 DLL 完成用戶端應用程式時，會呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 函式來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="c2a26-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="c2a26-111">完整的伺服器原始程式碼</span><span class="sxs-lookup"><span data-stu-id="c2a26-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="c2a26-112">完成伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="c2a26-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="c2a26-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2a26-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2a26-114">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="c2a26-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="c2a26-115">Winsock 伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="c2a26-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="c2a26-116">接收和傳送伺服器上的資料</span><span class="sxs-lookup"><span data-stu-id="c2a26-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="c2a26-117">執行 Winsock 用戶端和伺服器程式碼範例</span><span class="sxs-lookup"><span data-stu-id="c2a26-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 




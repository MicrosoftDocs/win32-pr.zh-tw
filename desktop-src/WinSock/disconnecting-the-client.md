---
description: 用戶端完成傳送和接收資料之後，用戶端就會中斷與伺服器的連線，然後關閉通訊端。
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: 中斷用戶端連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318388"
---
# <a name="disconnecting-the-client"></a><span data-ttu-id="25bf0-103">中斷用戶端連線</span><span class="sxs-lookup"><span data-stu-id="25bf0-103">Disconnecting the Client</span></span>

<span data-ttu-id="25bf0-104">用戶端完成傳送和接收資料之後，用戶端就會中斷與伺服器的連線，然後關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="25bf0-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="25bf0-105">**中斷和關閉通訊端**</span><span class="sxs-lookup"><span data-stu-id="25bf0-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="25bf0-106">當用戶端將資料傳送至伺服器時，可以呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 功能來指定 SD SEND， \_ 以關閉通訊端的傳送端。</span><span class="sxs-lookup"><span data-stu-id="25bf0-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="25bf0-107">這可讓伺服器釋放此通訊端的部分資源。</span><span class="sxs-lookup"><span data-stu-id="25bf0-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="25bf0-108">用戶端應用程式仍然可以接收通訊端上的資料。</span><span class="sxs-lookup"><span data-stu-id="25bf0-108">The client application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="25bf0-109">當用戶端應用程式完成接收資料時，會呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="25bf0-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="25bf0-110">使用 Windows 通訊端 DLL 完成用戶端應用程式時，會呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 函式來釋放資源。</span><span class="sxs-lookup"><span data-stu-id="25bf0-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="25bf0-111">完成用戶端原始程式碼</span><span class="sxs-lookup"><span data-stu-id="25bf0-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="25bf0-112">完成用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="25bf0-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="25bf0-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="25bf0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25bf0-114">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="25bf0-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="25bf0-115">Winsock 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="25bf0-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="25bf0-116">在用戶端上傳送和接收資料</span><span class="sxs-lookup"><span data-stu-id="25bf0-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 




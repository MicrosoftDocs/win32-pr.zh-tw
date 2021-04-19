---
description: 一旦通訊端接聽連線，程式就必須處理該通訊端上的連線要求。
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: " (Windows 通訊端 2) 接受連接"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970607"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="5660a-103"> (Windows 通訊端 2) 接受連接</span><span class="sxs-lookup"><span data-stu-id="5660a-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="5660a-104">一旦通訊端接聽連線，程式就必須處理該通訊端上的連線要求。</span><span class="sxs-lookup"><span data-stu-id="5660a-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="5660a-105">**接受通訊端上的連接**</span><span class="sxs-lookup"><span data-stu-id="5660a-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="5660a-106">建立名為 ClientSocket 的暫時 **通訊端** 物件，以接受來自用戶端的連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="5660a-107">伺服器應用程式通常是設計來接聽來自多個用戶端的連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="5660a-108">針對高效能伺服器，通常會使用多個執行緒來處理多個用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="5660a-109">有幾種不同的程式設計技術，使用 Winsock 來接聽多個用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="5660a-110">其中一個程式設計技巧是建立連續迴圈，以使用 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函數檢查連接要求 (查看 [在通訊端) 上接聽](listening-on-a-socket.md) 。</span><span class="sxs-lookup"><span data-stu-id="5660a-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="5660a-111">如果發生連接要求，應用程式會呼叫 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函式，並將工作傳遞至另一個執行緒來處理要求。</span><span class="sxs-lookup"><span data-stu-id="5660a-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="5660a-112">可能有數種其他程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="5660a-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="5660a-113">請注意，這個基本範例非常簡單，而且不會使用多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="5660a-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="5660a-114">此範例也只會接聽並接受單一連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="5660a-115">當用戶端連線已被接受時，伺服器應用程式通常會將上述範例程式碼中的 ClientSocket 變數傳遞 (的已接受用戶端通訊端) 至背景工作執行緒或 i/o 完成埠，然後繼續接受其他連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="5660a-116">在此基本範例中，伺服器會繼續進行下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="5660a-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="5660a-117">還有一些其他程式設計技巧可用來接聽和接受多個連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="5660a-118">這些包括使用 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函數。</span><span class="sxs-lookup"><span data-stu-id="5660a-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="5660a-119">Microsoft Windows 軟體開發套件 (SDK) 隨附的 [Advanced Winsock 範例](getting-started-with-winsock.md) 說明其中一些各種程式設計技術的範例。</span><span class="sxs-lookup"><span data-stu-id="5660a-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="5660a-120">在 Unix 系統上，伺服器的常見程式設計技巧是讓應用程式接聽連接。</span><span class="sxs-lookup"><span data-stu-id="5660a-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="5660a-121">當接受連接時，父進程會呼叫 **分叉** 函式來建立新的子進程，以處理用戶端連接，從父系繼承通訊端。</span><span class="sxs-lookup"><span data-stu-id="5660a-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="5660a-122">Windows 不支援這個程式設計技術，因為不支援 **分叉** 函數。</span><span class="sxs-lookup"><span data-stu-id="5660a-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="5660a-123">這項技術通常也不適合高效能伺服器，因為建立新進程所需的資源，遠高於執行緒所需的資源。</span><span class="sxs-lookup"><span data-stu-id="5660a-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="5660a-124">下一步：在 [伺服器上接收和傳送資料](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="5660a-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5660a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="5660a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5660a-126">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="5660a-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="5660a-127">Winsock 伺服器應用程式</span><span class="sxs-lookup"><span data-stu-id="5660a-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="5660a-128">在通訊端上接聽</span><span class="sxs-lookup"><span data-stu-id="5660a-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 

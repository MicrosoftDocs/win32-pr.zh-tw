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
# <a name="accepting-a-connection-windows-sockets-2"></a> (Windows 通訊端 2) 接受連接

一旦通訊端接聽連線，程式就必須處理該通訊端上的連線要求。

**接受通訊端上的連接**

1.  建立名為 ClientSocket 的暫時 **通訊端** 物件，以接受來自用戶端的連接。
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  伺服器應用程式通常是設計來接聽來自多個用戶端的連接。 針對高效能伺服器，通常會使用多個執行緒來處理多個用戶端連接。

    有幾種不同的程式設計技術，使用 Winsock 來接聽多個用戶端連接。 其中一個程式設計技巧是建立連續迴圈，以使用 [**接聽**](/windows/desktop/api/Winsock2/nf-winsock2-listen) 函數檢查連接要求 (查看 [在通訊端) 上接聽](listening-on-a-socket.md) 。 如果發生連接要求，應用程式會呼叫 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函式，並將工作傳遞至另一個執行緒來處理要求。 可能有數種其他程式設計技術。

    請注意，這個基本範例非常簡單，而且不會使用多個執行緒。 此範例也只會接聽並接受單一連接。

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

    

3.  當用戶端連線已被接受時，伺服器應用程式通常會將上述範例程式碼中的 ClientSocket 變數傳遞 (的已接受用戶端通訊端) 至背景工作執行緒或 i/o 完成埠，然後繼續接受其他連接。 在此基本範例中，伺服器會繼續進行下一個步驟。

    還有一些其他程式設計技巧可用來接聽和接受多個連接。 這些包括使用 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函數。 Microsoft Windows 軟體開發套件 (SDK) 隨附的 [Advanced Winsock 範例](getting-started-with-winsock.md) 說明其中一些各種程式設計技術的範例。

    > [!Note]  
    > 在 Unix 系統上，伺服器的常見程式設計技巧是讓應用程式接聽連接。 當接受連接時，父進程會呼叫 **分叉** 函式來建立新的子進程，以處理用戶端連接，從父系繼承通訊端。 Windows 不支援這個程式設計技術，因為不支援 **分叉** 函數。 這項技術通常也不適合高效能伺服器，因為建立新進程所需的資源，遠高於執行緒所需的資源。

     

下一步：在 [伺服器上接收和傳送資料](receiving-and-sending-data-on-the-server.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> <dt>

[在通訊端上接聽](listening-on-a-socket.md)
</dt> </dl>

 

 

---
description: 用戶端完成傳送和接收資料之後，用戶端就會中斷與伺服器的連線，然後關閉通訊端。
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: 中斷用戶端連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9689a1877ee015188583ef4a530dbd054cd47a2b7ecf2da1c89d4f341e90bc8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927877"
---
# <a name="disconnecting-the-client"></a>中斷用戶端連線

用戶端完成傳送和接收資料之後，用戶端就會中斷與伺服器的連線，然後關閉通訊端。

**中斷和關閉通訊端**

1.  當用戶端將資料傳送至伺服器時，可以呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 功能來指定 SD SEND， \_ 以關閉通訊端的傳送端。 這可讓伺服器釋放此通訊端的部分資源。 用戶端應用程式仍然可以接收通訊端上的資料。
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

    

2.  當用戶端應用程式完成接收資料時，會呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來關閉通訊端。

    當用戶端應用程式使用 Windows 通訊端 DLL 完成時，會呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup)函式來釋放資源。

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>完成用戶端原始程式碼

-   [完成用戶端程式代碼](complete-client-code.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 用戶端應用程式](winsock-client-application.md)
</dt> <dt>

[在用戶端上傳送和接收資料](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 




---
description: 一旦伺服器完成從用戶端接收資料，並將資料傳送回用戶端之後，伺服器會中斷與用戶端的連線，並關閉通訊端。
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: 中斷伺服器的連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898358"
---
# <a name="disconnecting-the-server"></a>中斷伺服器的連線

一旦伺服器完成從用戶端接收資料，並將資料傳送回用戶端之後，伺服器會中斷與用戶端的連線，並關閉通訊端。

**中斷和關閉通訊端**

1.  當伺服器完成將資料傳送至用戶端時，可以呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) \_ 傳送來指定 SD SEND，以關閉通訊端的傳送端。 這可讓用戶端釋放此通訊端的部分資源。 伺服器應用程式仍然可以接收通訊端上的資料。
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

    

2.  當用戶端應用程式完成接收資料時，會呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式來關閉通訊端。

    當用戶端應用程式使用 Windows 通訊端 DLL 完成時，會呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup)函式來釋放資源。

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>完整的伺服器原始程式碼

-   [完成伺服器程式碼](complete-server-code.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> <dt>

[接收和傳送伺服器上的資料](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[執行 Winsock 用戶端和伺服器程式碼範例](finished-server-and-client-code.md)
</dt> </dl>

 

 




---
description: 用戶端必須連接到伺服器，用戶端才能在網路上進行通訊。
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: 連接至通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132671"
---
# <a name="connecting-to-a-socket"></a>連接至通訊端

用戶端必須連接到伺服器，用戶端才能在網路上進行通訊。

## <a name="to-connect-to-a-socket"></a>連接至通訊端

呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 函式，並將建立的通訊端和 [**sockaddr**](sockaddr-2.md) 結構作為參數傳遞。 檢查是否有一般錯誤。


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



[**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數是用來判斷 [**sockaddr**](sockaddr-2.md)結構中的值。 在此範例中， **getaddrinfo** 函數所傳回的第一個 IP 位址會用來指定傳遞給 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)的 **sockaddr** 結構。 如果 **連接** 呼叫失敗至第一個 IP 位址，請嘗試從 **getaddrinfo** 函數傳回的連結清單中的下一個 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)結構。

[**Sockaddr**](sockaddr-2.md)結構中指定的資訊包括：

-   用戶端將嘗試連接之伺服器的 IP 位址。
-   用戶端將連接之伺服器上的埠號碼。 當用戶端呼叫 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式時，此埠已指定為埠27015。

下一步： [在用戶端上傳送和接收資料](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 用戶端應用程式](winsock-client-application.md)
</dt> <dt>

[建立用戶端的通訊端](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 

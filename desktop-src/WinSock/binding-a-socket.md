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
# <a name="binding-a-socket"></a>系結通訊端

若要讓伺服器接受用戶端連線，它必須系結至系統內的網路位址。 下列程式碼示範如何將已建立的通訊端系結至 IP 位址和埠。 用戶端應用程式會使用 IP 位址和埠來連接至主機網路。

## <a name="to-bind-a-socket"></a>系結通訊端

[**Sockaddr**](sockaddr-2.md)結構會保存位址系列、IP 位址和埠號碼的相關資訊。

呼叫系 [](/windows/desktop/api/winsock/nf-winsock-bind)結函式，將從 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函式傳回的已建立 **通訊端** 和 [**sockaddr**](sockaddr-2.md)結構作為參數傳遞。 檢查是否有一般錯誤。


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



一旦呼叫 [](/windows/desktop/api/winsock/nf-winsock-bind)系結函式，就不再需要 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數所傳回的位址資訊。 呼叫 [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) 函式來釋放 **getaddrinfo** 函式針對此位址資訊所配置的記憶體。


```C++
    freeaddrinfo(result);

```



下一步： [在通訊端上接聽](listening-on-a-socket.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> <dt>

[建立伺服器的通訊端](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 




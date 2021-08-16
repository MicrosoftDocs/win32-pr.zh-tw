---
description: 初始化之後，必須具現化通訊端物件以供伺服器使用。
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: 建立伺服器的通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e71d6ee0117153b00a9ab77c53bd7555aa031b3fa9d1f7a425ea9aaf0e358f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322198"
---
# <a name="creating-a-socket-for-the-server"></a>建立伺服器的通訊端

初始化之後，必須具現化 **通訊端** 物件以供伺服器使用。

**若要建立伺服器的通訊端**

1.  [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數是用來判斷 [**sockaddr**](sockaddr-2.md)結構中的值：

    -   **AF \_INET** 用來指定 IPv4 位址系列。
    -   **SOCK \_串流** 是用來指定資料流程通訊端。
    -   **IPPROTO \_TCP** 用來指定 tcp 通訊協定。
    -   **AI \_被動式** 旗標表示呼叫端要在系結函式的呼叫中使用 [**傳回的套**](/windows/desktop/api/winsock/nf-winsock-bind) 接字位址結構。 當 **AI \_ 被動** 旗標已設定，而且 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函式的 *nodename* 參數為 **Null** 指標時，通訊端位址結構的 IP 位址部分會設定為 IPv4 位址的 **INADDR \_ any** ，或 **IN6ADDR \_ 任何 \_ INIT** 的 IPv6 位址。
    -   27015是與用戶端所連接之伺服器相關聯的埠號碼。

    [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函數會使用 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)結構。

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  建立名為 ListenSocket 的 **通訊端** 物件，讓伺服器接聽用戶端連接。
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式，並將其值傳回給 ListenSocket 變數。 針對此伺服器應用程式，請使用符合 *提示* 參數中指定的位址系列、通訊端類型和通訊協定的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)呼叫所傳回的第一個 IP 位址。 在此範例中，會使用 IPv4 的位址系列、SOCK 資料流程的通訊端類型以及 IPPROTO TCP 的通訊協定來要求 IPv4 的 TCP 串流通訊端 \_ \_ 。 因此，會要求 ListenSocket 的 IPv4 位址。

    如果伺服器應用程式想要接聽 IPv6，則必須 \_ 在 *提示* 參數中將位址家族設定為 AF INET6。 如果伺服器想要同時接聽 IPv6 和 IPv4，則必須建立兩個接聽通訊端，一個用於 IPv6，另一個用於 IPv4。 這兩個通訊端必須由應用程式分開處理。

    WindowsVista 和更新版本可讓您建立單一 IPv6 通訊端，以在 IPv6 和 IPv4 上以雙重堆疊模式接聽。 如需這項功能的詳細資訊，請參閱 [雙重堆疊通訊端](dual-stack-sockets.md)。

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  檢查是否有錯誤，以確定通訊端是有效的通訊端。
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

下一步：系 [結通訊端](binding-a-socket.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[初始化 Winsock](initializing-winsock.md)
</dt> <dt>

[Winsock 伺服器應用程式](winsock-server-application.md)
</dt> </dl>

 

 

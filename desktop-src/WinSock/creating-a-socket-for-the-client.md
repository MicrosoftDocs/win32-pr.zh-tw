---
description: 初始化之後，必須具現化通訊端物件以供用戶端使用。
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: 建立用戶端的通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848020"
---
# <a name="creating-a-socket-for-the-client"></a>建立用戶端的通訊端

初始化之後，必須具現化 **通訊端** 物件以供用戶端使用。

**建立通訊端**

1.  宣告包含 [**sockaddr**](sockaddr-2.md)結構的 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)物件，並將這些值初始化。 針對此應用程式，未指定網際網路位址系列，因此可以傳回 IPv6 或 IPv4 位址。 應用程式要求通訊端類型為 TCP 通訊協定的資料流程通訊端。
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  呼叫 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函數，要求在命令列上傳遞的伺服器名稱的 IP 位址。 用戶端將連線之伺服器上的 TCP 埠， \_ 在此範例中是以27015的預設埠定義。 **Getaddrinfo** 函式會將其值傳回為已檢查錯誤的整數。
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  建立名為 ConnectSocket 的 **通訊端** 物件。
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式，並將其值傳回給 ConnectSocket 變數。 針對此應用程式，請使用符合 *提示* 參數中指定的位址系列、通訊端類型和通訊協定的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)呼叫所傳回的第一個 IP 位址。 在此範例中，TCP 資料流程通訊端是使用 SOCK 資料流程的通訊端類型 \_ 以及 IPPROTO TCP 的通訊協定所指定 \_ 。 位址系列未指定 (AF \_ UNSPEC) ，因此傳回的 IP 位址可能是伺服器的 IPv6 或 IPv4 位址。

    如果用戶端應用程式只想要使用 IPv6 或 IPv4 進行連線，則必須在提示參數中將位址家族設定為適用于 IPv6 的 AF \_ INET6 或適用于 ipv4 的 af \_ INET。 

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  檢查是否有錯誤，以確定通訊端是有效的通訊端。
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

您可以針對不同的執行方式變更傳遞至 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函數的參數。

錯誤偵測是成功網路程式碼的重要部分。 如果 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 呼叫失敗，則會傳回不正確 \_ 通訊端。 先前程式碼中的 **if** 語句會用來攔截建立通訊端時可能發生的任何錯誤。 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回與最後發生之錯誤相關聯的錯誤號碼。

> [!Note]  
> 視應用程式而定，可能需要更廣泛的錯誤檢查。
>
> 例如，將 *hints.ai_family* 設定為 **AF_UNSPEC** 可能會導致連接呼叫失敗。 如果發生這種情況，請改用特定的 IPv4 (**AF_INET**) 或 IPv6 (**AF_INET6**) 值。

[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 用來終止 WS2 \_ 32 DLL 的使用。

下一步： [連接至通訊端](connecting-to-a-socket.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[初始化 Winsock](initializing-winsock.md)
</dt> <dt>

[Winsock 用戶端應用程式](winsock-client-application.md)
</dt> </dl>

 

 

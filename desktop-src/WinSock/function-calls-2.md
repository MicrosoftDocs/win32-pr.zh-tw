---
description: Windows 通訊端介面引進了新的函式，其設計目的是為了讓 Windows 通訊端程式設計更容易。 這些新的 Windows 通訊端函式的優點之一，是 IPv6 和 IPv4 的整合支援。
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: IPv6 Winsock 應用程式的函式呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051666"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>IPv6 Winsock 應用程式的函式呼叫

Windows 通訊端介面引進了新的函式，其設計目的是為了讓 Windows 通訊端程式設計更容易。 這些新的 Windows 通訊端函式的優點之一，是 IPv6 和 IPv4 的整合支援。

這些新的 Windows 通訊端函數包括下列各項：

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 系列函數 (**getaddrinfo**、 [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)、 [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)、 [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo)、 [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex)、 [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)和 [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa)) 
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 系列函數 (**getnameinfo** 和 [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)) 

此外，已新增新的 IP Helper 函式，同時支援 IPv6 和 IPv4，以簡化 Windows 通訊端程式設計。 這些新的 IP Helper 函式包含下列各項：

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

將 IPv6 支援新增至應用程式時，應使用下列指導方針：

-   您可以使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ，透過指定的主機名稱和埠建立端點的連接。 **WSAConnectByName** 函式可在 Windows Vista 和更新版本上取得。
-   您可以使用 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 來建立一組目的地位址（)  (主機名稱和埠）所代表之可能端點集合中的一個連接。 **WSAConnectByList** 函式可在 Windows Vista 和更新版本上取得。
-   將 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)函式呼叫取代為其中一個新的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows 通訊端函數的呼叫。 Windows XP 及更新版本提供支援 IPv6 通訊協定的 **getaddrinfo** 函數。 安裝 Windows 2000 的 ipv6 技術預覽時，Windows 2000 也支援 ipv6 通訊協定。
-   將 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式呼叫取代為其中一個新的 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows 通訊端函數的呼叫。 Windows XP 及更新版本提供支援 IPv6 通訊協定的 **getnameinfo** 函數。 安裝 Windows 2000 的 ipv6 技術預覽時，Windows 2000 也支援 ipv6 通訊協定。

## <a name="wsaconnectbyname"></a>WSAConnectByName

[**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)函式會使用以資料流程為基礎的通訊端，將目的地的主機名稱或 IP 位址 (IPv4 或 IPv6) ，以簡化連接至端點的程式。 此函式會減少建立 IP 應用程式所需的原始程式碼，此應用程式與所使用的 IP 通訊協定版本無關。 **WSAConnectByName** 會將一般 TCP 應用程式中的下列步驟取代為單一函式呼叫：

-   將主機名稱解析為一組 IP 位址。
-   針對每個 IP 位址：
    -   建立適當位址系列的通訊端。
    -   嘗試連接到遠端 IP 位址。 如果連接成功，則會傳回;否則會嘗試主機的下一個遠端 IP 位址。

[**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)函式不僅會解析名稱，還會嘗試連接。 此函數會使用名稱解析和所有本機電腦的來源 IP 位址所傳回的所有遠端位址。 它會先嘗試使用位址組進行連線，並獲得最高的成功機會。 因此， **WSAConnectByName** 不僅可確保建立連接，還能將建立連線的時間降到最低。

若要同時啟用 IPv6 和 IPv4 通訊，請使用下列方法：

-   您必須在為 AF INET6 位址系列建立的通訊端上呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式 \_ ，才能在呼叫 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)之前停用 **IPV6 \_ V6ONLY** 通訊端選項。 這是藉由呼叫通訊端上的 **setsockopt** 函數，並 *將 level* 參數設定為 **IPPROTO \_ IPV6** (請參閱 [IPPROTO \_ ipv6 通訊端選項](ipproto-ipv6-socket-options.md)) 、將 *optname* 參數設定為 **IPV6 \_ V6ONLY**，以及將 *optvalue* 參數值設定為零。

如果應用程式需要系結至特定的本機位址或埠，則無法使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ，因為 **WSAConnectByName** 的 socket 參數必須是未系結的通訊端。

下列程式碼範例只會顯示需要幾行程式碼，才能使用此函式來執行與 IP 版本無關的應用程式。

使用 WSAConnectByName 建立連接[ ](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a>WSAConnectByList

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)函式會根據一組目的地 IP 位址和埠) ，來建立與主機的連線 (。 此函式會取得端點的所有 IP 位址和埠，以及所有本機電腦的 IP 位址，並使用所有可能的位址組合來嘗試連接。

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 與 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 函數有關。 **WSAConnectByList** 會接受主機清單 (目的地位址和埠) 配對，而不是採用單一主機名稱，而是會連接到所提供清單中的其中一個位址和埠。 此功能的設計目的是要支援應用程式必須從潛在主機清單中連接到任何可用主機的案例。

類似于 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)， [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) 函式可大幅減少建立、系結和連接通訊端所需的原始程式碼。 這項功能可讓您更輕鬆地執行與 IP 版本無關的應用程式。 此函式所接受的主機位址清單可能是 IPv6 或 IPv4 位址。

若要同時在函式接受的單一通訊清單中傳遞 IPv6 和 IPv4 位址，必須先執行下列步驟，然後再呼叫函式：

-   您必須在為 AF INET6 位址系列建立的通訊端上呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式 \_ ，才能在呼叫 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)之前停用 **IPV6 \_ V6ONLY** 通訊端選項。 這是藉由呼叫通訊端上的 **setsockopt** 函數，並 *將 level* 參數設定為 **IPPROTO \_ IPV6** (請參閱 [IPPROTO \_ ipv6 通訊端選項](ipproto-ipv6-socket-options.md)) 、將 *optname* 參數設定為 **IPV6 \_ V6ONLY**，以及將 *optvalue* 參數值設定為零。
-   任何 IPv4 位址都必須以 IPv4 對應的 IPv6 位址格式表示，讓 IPv6 的應用程式能夠與 IPv4 節點進行通訊。 IPv4 對應的 IPv6 位址格式允許 IPv4 節點的 IPv4 位址以 IPv6 位址表示。 IPv4 位址會編碼為 IPv6 位址的低序位32位，而高序位96位會保存固定的前置詞0：0：0：0：0： FFFF。 IPv4 對應的 IPv6 位址格式是在 RFC 4291 中指定的。 如需詳細資訊，請參閱 [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291)。 \_ *Mstcpip* 中的 IN6ADDR SETV4MAPPED 宏可以用來將 ipv4 位址轉換為所需的 ipv4 對應 IPv6 位址格式。

使用 WSAConnectByList 建立連接[ ](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a>getaddrinfo

**Getaddrinfo** 函數也會執行許多函數的處理工作。 之前，需要對多個 Windows 通訊端函式進行呼叫，以建立、開啟，然後將位址系結至通訊端。 使用 **getaddrinfo** 函式時，執行這類工作所需的源程式碼可大幅減少。 下列兩個範例說明使用和不使用 **getaddrinfo** 函式執行這些工作所需的原始程式碼。

使用 **getaddrinfo** 執行開啟、連線和系結


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



在不使用 **getaddrinfo** 的情況下，執行 Open、連線和 Bind


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



請注意，這兩個原始程式碼範例都會執行相同的工作，但第一個範例是使用 **getaddrinfo** 函式，需要較少的原始程式碼，並且可以處理 IPv6 或 IPv4 位址。 使用 **getaddrinfo** 函數刪除的源程式碼數會有所不同。

> [!Note]  
> 在實際執行的原始程式碼中，您的應用程式會逐一查看 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 或 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函數所傳回的一組位址。 這些範例會略過此步驟，以利簡化。

 

在修改現有的 IPv4 應用程式以支援 IPv6 時，您必須解決的另一個問題是，與呼叫函式的順序相關聯。 [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)和 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)都需要以特定順序進行函式呼叫的順序。

在同時使用 IPv4 和 IPv6 的平臺上，不會事先知道遠端主機名的位址系列。 因此，必須先執行使用 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式的位址解析，以判斷遠端主機的 IP 位址和位址系列。 然後，您可以呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式來開啟 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)所傳回之位址系列的通訊端。 這是 Windows 通訊端應用程式撰寫方式的重要變更，因為許多 IPv4 應用程式傾向于使用不同的函式呼叫順序。

大部分的 IPv4 應用程式首先會建立 AF \_ INET 位址系列的通訊端，然後進行名稱解析，然後使用通訊端連線到已解析的 IP 位址。 當您使這類應用程式具備 IPv6 能力時，必須先延遲 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 函式呼叫，才能在 deteremined 位址系列時進行名稱解析。 請注意，如果名稱解析同時傳回 IPv4 和 IPv6 位址，則必須使用個別的 IPv4 和 IPv6 通訊端來連接這些目的地位址。 您可以使用 Windows Vista 和更新版本上的 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)函式來避免這些複雜性，讓應用程式開發人員可以使用這項新功能。

下列程式碼範例會顯示正確的順序來執行名稱解析，先 (在下列原始程式碼範例的第四行中執行) ，然後在下列程式碼範例) 的<sup>第19行</sup> 中開啟通訊端 (執行。 此範例是在附錄 B 中，已 [啟用 IPv6 的用戶端程式代碼](ipv6-enabled-client-code-2.md) 中找到的用戶端 .c 檔案摘錄。下列程式碼範例中所呼叫的 PrintError 函式會列在用戶端 .c 範例中。


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a>IP 協助程式函式

最後，使用 IP 協助程式函式 [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)的應用程式及其相關聯的結構 [**IP \_ 介面卡 \_ 資訊**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)，必須辨識此函式和結構僅限於 IPv4 位址。 此函式和結構的啟用 IPv6 的取代為 [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) 函式和 [**IP \_ 介面卡 \_ 位址**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) 結構。 使用 IP 協助程式 API 的已啟用 ipv6 的應用程式，應該使用 **GetAdaptersAddresses** 函式和對應的已啟用 ipv6 **IP \_ 介面卡 \_ 位址** 結構（兩者都定義于 Microsoft Windows 軟體開發套件 (SDK) ）。

## <a name="recommendations"></a>建議

確保您的應用程式使用 IPv6 相容函式呼叫的最佳方法是使用 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式來取得主機對位址轉譯。 從 Windows XP 開始， **getaddrinfo** 函式會使 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)函式不必要，因此您的應用程式應該改為使用 **getaddrinfo** 函式來進行未來的程式設計專案。 雖然 Microsoft 會繼續支援 **gethostbyname**，但不會擴充此功能以支援 IPv6。 如需取得 IPv6 和 IPv4 主機資訊的透明支援，您必須使用 **getaddrinfo**。

下列範例示範如何使用 **getaddrinfo** 函數。 請注意，如下列範例所示，此函式會適當地處理 IPv6 和 IPv4 的主機對位址轉譯，但它也會取得主機的其他有用資訊，例如支援的通訊端類型。 此範例是來自于附錄 B 中所找到的用戶端 c 範例摘要。


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> 支援 IPv6 的 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)函式版本是 Windows Windows XP 版本的新功能。

 

要避免的程式碼

傳統上使用 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) 函式來達成主機位址轉換。 從 Windows XP 開始：

-   **Getaddrinfo** 函式會讓 **gethostbyname** 函式過時。
-   您的應用程式應該使用 **getaddrinfo** 函式，而不是 **gethostbyname** 函數。

編寫工作的程式碼

**若要修改現有的 IPv4 應用程式以新增 IPv6 的支援**

1.  取得 Checkv4.exe 公用程式。 此公用程式會安裝為 Windows SDK 的一部分。 Windows SDK 可透過 MSDN 訂閱取得，也可以從 Microsoft 網站 (下載 https://msdn.microsoft.com) 。 舊版的 *Checkv4.exe* 工具也隨附于 Windows 2000 的 Microsoft IPv6 技術預覽中。
2.  針對您的程式碼執行 *Checkv4.exe* 公用程式。 請參閱 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md) 來瞭解如何針對您的檔案執行版本公用程式。
3.  此公用程式會警示您使用 [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)、 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)和其他僅限 IPv4 的函式，並提供如何以與 IPv6 相容的函式（例如 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)）取代這些函式的建議。
4.  使用 **getaddrinfo** 函數，將 **gethostbyname** 函式的任何實例和相關聯的程式碼取代為適當的。 在 Windows Vista 上，請在適當的情況下使用 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)或 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)函數。
5.  使用 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)函數，將 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式的任何實例和相關聯的程式碼取代為適當的。

或者，您可以在程式碼基底中搜尋 **gethostbyname** 和 [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) 函式的實例，並視需要將所有 (和其他相關聯的程式碼) 變更為 **getaddrinfo** 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[變更 IPv6 Winsock Html5 應用程式的資料結構](changing-data-structures-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的雙重堆疊通訊端](dual-stack-sockets.md)
</dt> <dt>

[使用硬式編碼的 IPv4 位址](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的消費者介面問題](user-interface-issues-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
</dt> </dl>

 

 

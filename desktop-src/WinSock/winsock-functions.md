---
description: 下列清單提供每個 Winsock 函數的精確描述。 如需任何函數的詳細資訊，請按一下函式名稱。
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Winsock 函式s
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978231"
---
# <a name="winsock-functions"></a>Winsock 函式s

下列清單提供每個 Winsock 函數的精確描述。 如需任何函數的詳細資訊，請按一下函式名稱。

| 函式 | 描述 |
|-|-|
| [**接受**](/windows/win32/api/Winsock2/nf-winsock2-accept) | 允許通訊端上的連入連線嘗試。 |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | 接受新的連接、傳回本機和遠端位址，並接收用戶端應用程式傳送的第一個資料區塊。 |
| [**綁定**](/windows/win32/api/winsock/nf-winsock-bind) | 將本機位址與通訊端產生關聯。 |
| [**導致 closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | 關閉現有的通訊端。 |
| [**連線**](/windows/win32/api/Winsock2/nf-winsock2-connect) | 建立與指定之通訊端的連接。 |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | 建立與指定之通訊端的連接，並在建立連線之後選擇性地傳送資料。 只有連接導向的通訊端才支援。 |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | 關閉通訊端上的連接，並允許使用通訊端控制碼。 |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | 抓取本機主機上作用中的一組指定網路通訊協定的相關資訊。 |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | 釋放 [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 函式在 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) 結構中動態配置的位址資訊。 |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | 釋放 [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) 函式在 [**addrinfoex**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) 結構中動態配置的位址資訊。 |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | 釋放 [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) 函式在 [**addrinfoW**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) 結構中動態配置的位址資訊。 |
| [**gai \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | 協助根據 getaddrinfo 函式所傳回的 EAI \_ \* 錯誤來[](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)列印錯誤訊息。 |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | 剖析從呼叫 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函數取得的資料。 |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | 查詢命名空間（或一組預設的命名空間），以取得指定之網路服務的網路位址資訊。 此處理程式稱為服務名稱解析。 網路服務也可以使用函式取得可搭配 [**bind**](/windows/win32/api/winsock/nf-winsock-bind) 函式使用的本機位址資訊。 |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | 提供從 ANSI 主機名稱到位址的通訊協定無關轉譯。 |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | 使用其他參數提供與通訊協定無關的名稱解析，以限定哪些命名空間提供者應該處理要求。 |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | 取消 [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) 函式的非同步作業。 |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | 取得 [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)函式的非同步作業所使用之重 **迭結構的** 傳回碼。 |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | 提供從 Unicode 主機名稱到位址的通訊協定無關轉譯。 |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | 抓取對應于網路位址的主機資訊。 |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | 從主資料庫抓取對應于主機名稱的主機資訊。 已淘汰：請改用 [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 。 |
| [**gethostname**](/windows/win32/api/winsock/nf-winsock-gethostname) | 抓取本機電腦的標準主機名稱。 |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | 以 Unicode 字串形式抓取本機電腦的標準主機名稱。 |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | 抓取 IPv4 通訊端的多播篩選狀態。 |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | 針對指定的服務類型，抓取網路服務的名稱。 |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | 提供從 IPv4 或 IPv6 位址到 ansi 主機名稱的名稱解析，以及從埠號碼到 ANSI 服務名稱的名稱解析。 |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | 提供從 IPv4 或 IPv6 位址到 unicode 主機名稱的名稱解析，以及從埠號碼到 Unicode 服務名稱的名稱解析。 |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | 抓取通訊端所連接之對等的位址。 |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | 抓取對應通訊協定名稱的通訊協定資訊。 |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | 抓取對應通訊協定編號的通訊協定資訊。 |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | 抓取對應到服務名稱和通訊協定的服務資訊。 |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | 抓取對應至埠和通訊協定的服務資訊。 |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | 在一組預設的命名空間或指定的命名空間內容中，抓取網路服務的相關資訊。 |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | 抓取通訊端的本機名稱。 |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | 捕獲通訊端選項。 |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | 抓取 IPv4 或 IPv6 通訊端的多播篩選器狀態。 |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | 抓取名稱所指定之網路服務的服務類型 GUID。 |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | 將 **雙精度浮點數** 從主機轉換成 tcp/ip 網路位元組順序 (也就是位元組由大到小的) 。 |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | 將 **float** 從主機轉換成 tcp/ip 網路位元組順序 (也就是位元組由大到小的) 。 |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | 將 [ **u \_ long** from host] 轉換為 [tcp/ip 網路位元組順序] (是位元組由大到小的) 。 |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | 將不 **帶正負號的 \_ \_ int64** 從主機轉換成 tcp/ip 網路位元組順序 (也就是位元組由大到小的) 。 |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | 從主機轉換為位元組由) 大到 **\_ 小** 的 (，從主機轉換成 tcp/ip 網路位元組順序。 |
| [**inet \_ 位址**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | 將包含 (Ipv4) 網際網路通訊協定點位址的字串，轉換成位址結構 [**中的 \_**](/windows/win32/api/winsock2/ns-winsock2-in_addr) 適當位址。 |
| [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | 將 (IPv4) 網際網路網路位址轉譯成網際網路標準點格式的字串。 |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | 將 IPv4 或 IPv6 網際網路網路位址轉譯成網際網路標準格式的字串。 此函數的 ANSI 版本是 [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw)。 |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | 將其標準文字呈現形式的 IPv4 或 IPv6 網際網路網路位址轉譯成其數值二進位格式。 此函數的 ANSI 版本是 [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw)。 |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | 控制通訊端的 i/o 模式。 |
| [**聽**](/windows/win32/api/Winsock2/nf-winsock2-listen) | 讓通訊端成為接聽連入連線的狀態。 |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | 將不 **帶正負號的 \_ \_ int64** 從 tcp/ip 網路順序轉換為主機位元組順序 (在 Intel 處理器上以位元組由小到大的順序) 並傳回 **雙精度浮點數**。 |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | 將不 **帶正負號的 \_ \_ int32** 從 tcp/ip 網路順序轉換為主機位元組順序 (在 Intel 處理器上以位元組由小到大的順序，) 並傳回 **浮點數**。 |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | 將 u 的 \_ long 從 tcp/ip 網路順序轉換為主機位元組順序 (這在 Intel 處理器) 的位元組由大到小。 |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | 將不 **帶正負號的 \_ \_ int64** 從 tcp/ip 網路順序轉換為主機位元組順序 (這在 Intel 處理器) 的位元組由小到大。 |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | 將 u \_ 從 tcp/ip 網路位元組順序轉換為主機位元組順序 (這在 Intel 處理器) 的位元組由小到大。 |
| [**recv**](/windows/win32/api/winsock/nf-winsock-recv) | 從已連接或系結的通訊端接收資料。 |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | 接收資料包並儲存來源位址。 |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | 使用 Winsock 註冊的 i/o 延伸模組，關閉用於 i/o 完成通知的現有完成佇列。 |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | 建立特定大小的 i/o 完成佇列，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | 使用指定的通訊端和 i/o 完成佇列來建立已註冊的 i/o 通訊端描述元，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | 從 i/o 完成佇列中移除專案，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | 取消註冊已註冊的緩衝區搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | 註冊方法以用於具有 i/o 完成佇列的通知行為，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | 在連接的已註冊 i/o TCP 通訊端或系結的已註冊 i/o UDP 通訊端上接收網路資料，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | 在連接的已註冊 i/o TCP 通訊端或系結的已註冊 i/o UDP 通訊端上接收網路資料，搭配 Winsock 註冊的 i/o 擴充功能使用其他選項。 |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | 使用指定的緩衝區註冊 [**RIO \_ BUFFERID**](rio-bufferid.md)（已註冊的緩衝區描述項），以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | 將 i/o 完成佇列的大小調整為較大或較小，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | 將要求佇列的大小調整為較大或較小，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | 在連接的已註冊 i/o TCP 通訊端或系結的已註冊 i/o UDP 通訊端上傳送網路資料，以搭配 Winsock 註冊的 i/o 擴充功能使用。 |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | 使用與 Winsock 註冊的 i/o 延伸模組搭配使用的其他選項，在連接的已註冊 i/o TCP 通訊端或系結的已註冊 i/o UDP 通訊端上傳送網路資料。 |
| [**選擇**](/windows/win32/api/Winsock2/nf-winsock2-select) | 判斷一或多個通訊端的狀態，並在必要時等候，以執行同步 i/o。 |
| [**發送**](/windows/win32/api/Winsock2/nf-winsock2-send) | 在連接的通訊端上傳送資料。 |
| [**sendto**](/windows/win32/api/winsock/nf-winsock-sendto) | 將資料傳送至特定目的地。 |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | 註冊主機和服務名稱，以及與特定命名空間提供者相關聯的位址。 |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | 設定 IPv4 通訊端的多播篩選器狀態。 |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | 在一或多個命名空間內登錄或移除登錄中的網路服務。 也可以新增或移除一或多個命名空間內的網路服務類型。 |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | 指出是否要使用網路來傳輸需要服務品質的串流媒體。 |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | 設定通訊端選項。 |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | 設定 IPv4 或 IPv6 通訊端的多播篩選器狀態。 |
| [**關閉**](/windows/win32/api/winsock/nf-winsock-shutdown) | 停用通訊端上的傳送或接收。 |
| [**插座**](/windows/win32/api/Winsock2/nf-winsock2-socket) | 建立系結至特定服務提供者的通訊端。 |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | 透過連接的通訊端控制碼傳輸檔案資料。 |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | 透過已連接的通訊端傳輸記憶體中的資料或檔案資料。 |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | 有條件地根據條件函式的傳回值來接受連線、提供服務流程規格的品質，以及允許傳輸連接資料。 |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | 將 [**sockaddr**](sockaddr-2.md) 結構的所有元件轉換成該位址的人們可讀取字串表示。 |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | 以非同步方式抓取對應至位址的主機資訊。 |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | 以非同步方式抓取對應于主機名稱的主機資訊。 |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | 以非同步方式抓取對應至通訊協定名稱的通訊協定資訊。 |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | 以非同步方式抓取對應至通訊協定編號的通訊協定資訊。 |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | 以非同步方式抓取對應到服務名稱和埠的服務資訊。 |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | 以非同步方式抓取對應至埠和通訊協定的服務資訊。 |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | 要求通訊端的網路事件以 Windows 訊息為基礎的通知。 |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | 取消不完整的非同步作業。 |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | 終止使用 Ws2 \_32.DLL。 |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | 關閉開啟的事件物件控制碼。 |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | 建立與另一個通訊端應用程式的連接、交換連接資料，並根據指定的 [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) 結構指定所需的服務品質。 |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | 從一組目的地位址所表示的可能端點集合中建立一個連接， (主機名稱和埠) 。 |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | 在指定的主機和埠上建立與另一個通訊端應用程式的連接 |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | 建立新的事件物件。 |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | 移除對等目標名稱與通訊端 IP 位址之間的關聯。 |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | 傳回結構，可用來建立共用通訊端的新通訊端描述項。 |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | 抓取可用命名空間的相關資訊。 |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | 抓取可用命名空間的相關資訊。 |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | 探索指定之通訊端的網路事件出現次數、清除內部網路事件記錄，以及重設事件物件 (選擇性) 。 |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | 抓取可用傳輸通訊協定的相關資訊。 |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | 指定要與指定的 FD XXX 網路事件集關聯的事件物件 \_ 。 |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | 指定通訊端是否包含在一組通訊端描述項中。 |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | 查詢 [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) 通訊端選項的狀態。 |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | 查詢連接設定期間，在 TCP 通訊端上收到的 ICMP 錯誤來源位址。 |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | 抓取通訊端的使用者定義 IP 層 MTU。 |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | 傳回最後一個作業失敗的錯誤狀態。 |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | 抓取指定之通訊端上重迭運算的結果。 |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | 初始化以命名範本為基礎的 [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) 結構，或提供緩衝區來取得可用範本名稱的列舉。 |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | 從指定的命名空間提供者中，抓取與指定的服務類別有關的類別資訊 (架構) 。 |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | 抓取與指定類型相關聯的服務名稱。 |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | 抓取 UDP 通訊端已接收、已合併訊息的大小上限。 |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | 捕獲 UDP 通訊端的分割訊息大小。 |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | 將 u \_ long 從主機位元組順序轉換成網路位元組順序。 |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | 將 u \_ short 從主機位元組順序轉換成網路位元組順序。 |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | 用來模擬對應至通訊端對等的安全性主體，以便執行應用層級授權。 |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | 在命名空間內註冊服務類別架構。 |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | 控制通訊端的模式。 |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | 將分葉節點聯結至 multipoint 會話、交換連接資料，並根據指定的結構指定所需的服務品質。 |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | 起始用戶端查詢，該查詢會受限於 [**WSAQUERYSET**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) 結構內所含的資訊。 |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | 釋放先前呼叫 [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) 和 [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta)所使用的控制碼。 |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | 取出要求的服務資訊。 |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | 開發人員可對已註冊的命名空間進行 i/o 控制項呼叫。 |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | 將 u \_ long 從網路位元組順序轉換為主機位元組順序。 |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | 將 u \_ short 從網路位元組順序轉換成主機位元組順序。 |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | 判斷一或多個通訊端的狀態。 |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | 在提供者設定變更時通知應用程式。 |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | 查詢通訊端上的連接所套用之安全性的相關資訊。 |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | 從已連線的通訊端擷取資料。 |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | 終止通訊端上的接收，如果通訊端為連線導向，則抓取中斷連接資料。 |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | 從已連線的通訊端擷取資料。 |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | 接收資料包並儲存來源位址。 |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | 從連接和未連接的通訊端接收資料和選擇性的控制項資訊。 |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | 從登錄中永久移除服務類別架構。 |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | 將指定之事件物件的狀態重設為未收到信號。 |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | 終止通訊端對等的模擬。 |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | 在連接的通訊端上傳送資料。 |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | 起始通訊端的連線終止，並傳送中斷連接的資料。 |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | 從已連線和未連接的通訊端傳送資料和選擇性的控制項資訊。 |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | 使用重迭的 i/o （適用時）將資料傳送至特定的目的地。 |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | 將指定之事件物件的狀態設定為已發出信號。 |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | 設定 [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) 通訊端選項的狀態。 |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | 在通訊端上設定使用者定義的 IP 層 MTU。 |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | 設定錯誤碼。 |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | 在一或多個命名空間內登錄或移除登錄中的服務實例。 |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | 用來指定對應至對等 IP 位址 (SPN) 的對等目標名稱。 此目標名稱的目的是要讓用戶端應用程式指定，以安全地識別應該驗證的對等。 |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | 啟用並套用通訊端的安全性。 |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | 設定 UDP 通訊端上合併訊息集的大小上限。 |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | 設定 UDP 通訊端上的分割訊息大小。 |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | 建立系結至特定傳輸服務提供者的通訊端。 |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | 啟始 \_ 進程32.DLL 使用 WS2。 |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | 將數值字串轉換成 [**sockaddr**](sockaddr-2.md) 結構。 |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | 當其中一個或所有指定的事件物件處於已發出信號的狀態，或當逾時間隔到期時，會傳回。 |

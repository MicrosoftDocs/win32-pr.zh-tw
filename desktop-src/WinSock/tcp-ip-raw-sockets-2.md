---
description: 原始通訊端是允許存取基礎傳輸提供者的通訊端類型。
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: TCP/IP 原始通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25cc08d59d80089a4e655f363e4a899edac8d2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989333"
---
# <a name="tcpip-raw-sockets"></a>TCP/IP 原始通訊端

原始通訊端是允許存取基礎傳輸提供者的通訊端類型。 本主題只著重于原始通訊端和 IPv4 與 IPv6 通訊協定。 這是因為除了 ATM 以外的其他大部分通訊協定不支援原始通訊端。 若要使用原始通訊端，應用程式必須有所使用之基礎通訊協定的詳細資訊。

IP 通訊協定的 Winsock 服務提供者可能會支援 **SOCK \_ RAW** 的通訊端 *類型*。 包含在 Windows 上的 TCP/IP 適用的 Windows 通訊端2提供者支援此 **SOCK \_ 原始** 通訊端類型。

這類原始通訊端有兩種基本類型：

-   第一個類型會使用由 Winsock 服務提供者所辨識的 IP 標頭中所寫入的已知通訊協定類型。 第一個通訊端類型的範例是 ICMP 通訊協定的通訊端， (IP 通訊協定類型 = 1) 或 ICMPv6 通訊協定 (IP 通訊協定 type = 58) 。
-   第二種類型可指定任何通訊協定類型。 第二種類型的範例是，Winsock 服務提供者不直接支援的實驗性通訊協定，例如 Stream Control 傳輸通訊協定 (SCTP) 。

## <a name="determining-if-raw-sockets-are-supported"></a>判斷是否支援原始通訊端

如果 Winsock 服務提供者支援 AF INET 或 AF INET6 位址系列的 **SOCK \_ 原始** 通訊端 \_ \_ ，則 **SOCK \_ RAW** 的通訊端類型應該包含在 [**WSAPROTOCOL**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)函數針對一或多個可用的傳輸提供者所傳回的 [**WSAEnumProtocols \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中。

[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中的 **IADDRESSFAMILY** 成員應指定 af \_ INET 或 af \_ INET6， **iSocketType \_ 資訊** 結構的 **WSAPROTOCOL** 成員應針對其中一個傳輸提供者指定 **SOCK \_ RAW** 。

[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **iProtocol** 成員可以設定為 **IPROTO \_ IP**。 如果服務提供者允許應用程式針對位址系列的網際網路通訊協定以外的其他網路通訊協定使用 **SOCK \_ 原始** 通訊端類型，則 **WSAPROTOCOL \_ 資訊** 結構的 **iProtocol** 成員也可以設定為零。

[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中的其他成員表示 **SOCK \_ RAW** 之通訊協定支援的其他屬性，並指出應該如何處理 **SOCK \_ 原始** 的通訊端。 **SOCK \_ 原始** 的其他 **WSAPROTOCOL \_ 資訊** 成員通常會指定通訊協定為無訊息導向、支援廣播/多播 (XP1 \_ 無連接、XP1 \_ 訊息 \_ 導向、XP1 \_ 支援 \_ 廣播，以及 XP1 \_ \_ 成員) 中設定 dwServiceFlags1 支援 MULTIPOINT 位，且最大訊息大小為65467個位元組。

在 Windows XP 和更新版本上， *NetSh.exe* 命令可用於判斷是否支援原始通訊端。 下列從 CMD 視窗執行的命令會在主控台上顯示 Winsock 目錄中的資料：

**netsh winsock show catalog**

輸出會包含一份清單，其中包含本機電腦上所支援之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中的部分資料。 在 [描述] 欄位中搜尋 RAW/IP 或 RAW/IPv6 一詞，以找出支援原始通訊端的通訊協定。

## <a name="creating-a-raw-socket"></a>建立原始通訊端

若要建立 **SOCK \_ RAW** 型別的通訊端，請使用 *af* 參數呼叫 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式 (位址家族) 設定為 af \_ INET 或 af \_ INET6、將 *type* 參數設定為 **SOCK \_ RAW**，以及將 *protocol* 參數設定為所需的通訊協定號碼。 *通訊協定* 參數會成為 IP 標頭中的通訊協定值， (SCTP 是132，例如) 。

> [!Note]  
> 如果 *類型* 參數設定為 **SOCK \_ RAW**，應用程式可能不會指定零 (0) 作為 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)、 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)和 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)函數的 *通訊協定* 參數。

 

原始通訊端提供操作基礎傳輸的功能，因此可用於造成安全性威脅的惡意用途。 因此，只有 Administrators 群組的成員可以 \_ 在 Windows 2000 和更新版本上建立 SOCK RAW 類型的通訊端。

## <a name="send-and-receive-operations"></a>傳送和接收作業

一旦應用程式建立 **SOCK \_ RAW** 型別的通訊端，就可以使用這個通訊端來傳送和接收資料。 在 **SOCK \_ RAW** 類型的通訊端上傳送或接收的所有封包，都會被視為未連接之通訊端上的資料包。

下列規則適用于透過 **SOCK \_ 原始** 通訊端的作業：

-   [**Sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)或 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)函式通常用來在 **SOCK \_ RAW** 類型的通訊端上傳送資料。 目的地位址可以是通訊端位址家族中的任何有效位址，包括廣播或多播位址。 若要傳送至廣播位址，應用程式必須已使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 並 \_ 啟用廣播。 否則， **sendto** 或 **WSASendTo** 將會失敗，並出現錯誤碼 [WSAEACCES](windows-sockets-error-codes-2.md)。 若為 IP，應用程式可以傳送至任何多播位址 (而不會成為群組成員) 。
-   傳送 IPv4 資料時，應用程式可選擇是否要在封包的傳出資料包前端指定 IPv4 標頭。 如果 IPv4 通訊端的 **IP \_ HDRINCL** 通訊端選項設定為 true （ (位址系列為 AF \_ INET) ），則應用程式必須在傳出的資料中提供傳送作業的 IPv4 標頭。 如果這個通訊端選項是 false (預設設定) ，則 IPv4 標頭不應該包含在傳送作業的傳出資料中。
-   傳送 IPv6 資料時，應用程式可選擇是否要在封包的傳出資料包前端指定 IPv6 標頭。 如果 ipv6 通訊端的 **ipv6 \_ HDRINCL** 通訊端選項設定為 true (位址系列為 AF \_ INET6) ，則應用程式必須在傳出的資料中提供 ipv6 標頭，以進行傳送作業。 此選項的預設設定為 [false]。 如果這個通訊端選項為 false (預設設定) ，則不應將 IPv6 標頭包含在傳送作業的傳出資料中。 若為 IPv6，則應該不需要包含 IPv6 標頭。 如果可以使用通訊端函式提供資訊，則不應納入 IPv6 標頭，以避免未來發生相容性問題。 這些問題會在 IETF 發行的 RFC 3542 中討論。 不建議使用 **IPV6 \_ HDRINCL** 通訊端選項，而且未來可能會淘汰。
-   [**Recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)函數通常用來接收 **SOCK \_ RAW** 類型之通訊端上的資料。 這兩個函式都有一個選項，可傳回傳送封包的來源 IP 位址。 收到的資料是來自未連接之通訊端的資料包。
-   針對 IPv4 (位址系列的 AF \_ INET) ，應用程式會在每個收到的資料包前端收到 ip 標頭，不論 **ip \_ HDRINCL** 通訊端選項為何。
-   針對 IPv6 (位址系列的 AF \_ INET6) ，應用程式會在每個收到的資料包中的最後一個 IPv6 標頭之後收到所有內容，不論 **IPv6 \_ HDRINCL** 通訊端選項為何。 應用程式不會使用原始通訊端接收任何 IPv6 標頭。
-   收到的資料包會複製到所有符合下列條件的 **SOCK \_ 原始** 通訊端：

    -   當通訊端建立時， *protocol* 參數中所指定的通訊協定號碼應符合所接收資料包的 IP 標頭中的通訊協定號碼。
    -   如果為通訊端定義了本機 IP 位址，則應該對應至接收資料包的 IP 標頭中所指定的目的地位址。 應用程式可以藉由呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函式來指定本機 IP 位址。 如果未指定通訊端的本機 IP 位址，則不論收到的資料包 IP 標頭中的目的地 IP 位址為何，資料包都會複製到通訊端中。
    -   如果為通訊端定義了外部地址，則應該對應至接收資料包的 IP 標頭中所指定的來源位址。 應用程式可以藉由呼叫 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 或 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) 函數來指定外部 IP 位址。 如果未指定通訊端的外部 IP 位址，則不論收到的資料包 IP 標頭中的來源 IP 位址為何，資料包都會複製到通訊端中。

請務必瞭解， **SOCK \_ RAW** 類型的某些通訊端可能會收到許多未預期的資料包。 例如，偵測程式可能會建立 **SOCK \_ RAW** 類型的通訊端，以傳送 ICMP echo 要求和接收回應。 雖然應用程式預期會有 ICMP echo 回應，但其他所有的 ICMP 訊息 (例如，ICMP 主機 \_ 無法連線) 也可以傳遞到此應用程式。 此外，如果在電腦上同時開啟數個 **SOCK \_ 原始** 通訊端，則可以將相同的資料包傳遞給所有開啟的通訊端。 應用程式必須有一種機制來辨識感興趣的資料包，並忽略所有其他資料包。 針對 PING 程式，這類機制可能包括檢查 ICMP 標頭中唯一識別碼的已接收 IP 標頭 (應用程式的處理序識別碼，例如) 。

> [!Note]  
> 若要使用 **SOCK \_ RAW** 型別的通訊端，需要系統管理許可權。 執行使用原始通訊端之 Winsock 應用程式的使用者必須是本機電腦上 Administrators 群組的成員，否則原始通訊端呼叫會失敗，並出現錯誤碼 [WSAEACCES](windows-sockets-error-codes-2.md)。 在 Windows Vista 和更新版本上，會在建立通訊端時強制執行原始通訊端的存取。 在舊版的 Windows 中，會在其他通訊端作業期間強制執行原始通訊端的存取。

 

## <a name="common-uses-of-raw-sockets"></a>原始通訊端的常見用法

原始通訊端的常見用法之一，是針對需要詳細檢查 IP 封包和標頭的應用程式進行疑難排解。 例如，原始通訊端可以搭配 SIO RCVALL IOCTL 使用， \_ 以便讓通訊端接收透過網路介面傳遞的所有 IPv4 或 IPv6 封包。 如需詳細資訊，請參閱 [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) 參考。

## <a name="limitations-on-raw-sockets"></a>原始通訊端的限制

在 Windows 7、Windows Vista、Windows XP （含 Service Pack 2） (SP2) ，以及 Windows XP Service Pack 3 (SP3) 上，透過原始通訊端傳送流量的功能有數種限制：

-   無法透過原始通訊端傳送 TCP 資料。
-   具有無效來源位址的 UDP 資料包無法透過原始通訊端傳送。 任何外寄 UDP 資料包的 IP 來源位址都必須存在於網路介面上，否則資料包會卸載。 這項變更是為了限制惡意程式碼建立分散式阻絕服務攻擊的能力，並限制傳送詐騙封包 (具有偽造來源 IP 位址) 的 TCP/IP 封包的能力。
-   不允許使用 IPPROTO TCP 通訊協定的原始通訊端呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) 函數 \_ 。
    > [!Note]  
    > 具有原始套 [**接字的系**](/windows/desktop/api/winsock/nf-winsock-bind) 結函式可用於其他通訊協定 (IPPROTO \_ IP、IPPROTO \_ UDP 或 IPPROTO \_ SCTP，例如) 。

     

上述的限制不適用於 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003，或 Windows XP SP2 之前的作業系統版本。

> [!Note]  
> Microsoft 在 Windows 上執行 TCP/IP 的功能，能夠根據上述限制開啟原始的 UDP 或 TCP 通訊端。 其他 Winsock 提供者可能不支援使用原始通訊端。

 

使用 **SOCK \_ RAW** 類型之通訊端的應用程式會有更多的限制。 例如，所有接聽特定通訊協定的應用程式都會收到針對此通訊協定接收的所有封包。 這可能不是使用通訊協定的多個應用程式所需的內容。 這也不適合高效能應用程式。 若要解決這些問題，可能需要為特定的網路通訊協定撰寫 Windows 網路通訊協定驅動程式 (設備磁碟機) 。 在 Windows Vista 和更新版本上，Winsock 核心 (WSK) ，這是一個新的傳輸獨立核心模式網路程式設計介面，可用來撰寫網路通訊協定驅動程式。 在 Windows Server 2003 及更早版本上，可以撰寫傳輸驅動程式介面 (TDI) 提供者和 Winsock helper DLL，以支援網路通訊協定。 接著會將網路通訊協定新增至 Winsock 目錄作為支援的通訊協定。 這可讓多個應用程式開啟此特定通訊協定的通訊端，而設備磁碟機可以追蹤哪個通訊端接收特定的封包和錯誤。 如需有關撰寫網路通訊協定提供者的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 的 WSK 和 TDI 章節。

應用程式也必須留意防火牆設定可能對使用原始通訊端傳送和接收封包造成的影響。

 

 

---
description: 為了在 Windows XP Service Pack 1 (SP1) 和 Windows Server 2003 上同時支援 IPv4 和 IPv6，應用程式必須建立兩個通訊端，一個通訊端用於 IPv4，另一個通訊端用於 IPv6。
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: IPv6 Winsock 應用程式 Dual-Stack 通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132661"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>IPv6 Winsock 應用程式 Dual-Stack 通訊端

為了在 Windows XP Service Pack 1 (SP1) 和 Windows Server 2003 上同時支援 IPv4 和 IPv6，應用程式必須建立兩個通訊端，一個通訊端用於 IPv4，另一個通訊端用於 IPv6。 這兩個通訊端必須由應用程式分開處理。

WindowsVista 和更新版本可讓您建立單一 IPv6 通訊端，以同時處理 IPv6 和 IPv4 流量。 例如，會建立 IPv6 的 TCP 接聽通訊端，並進入雙堆疊模式，並系結至埠5001。 此雙重堆疊通訊端可以接受從連線到埠5001的 IPv6 TCP 用戶端，以及從連線到埠5001的 IPv4 TCP 用戶端的連線。 這項功能可大幅簡化應用程式設計，並減少在兩個不同的通訊端上張貼作業所需的資源負擔。

## <a name="creating-a-dual-stack-socket"></a>建立 Dual-Stack 通訊端

根據預設，在 Windows Vista 和更新版本上建立的 ipv6 通訊端只會透過 IPv6 通訊協定運作。 若要讓 IPv6 通訊端成為雙重堆疊通訊端，必須使用 **IPv6 \_ V6ONLY** 通訊端選項呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函式，將此值設定為零，再將通訊端系結至 IP 位址。 當 **ipv6 \_ V6ONLY** 通訊端選項設定為零時，為 **AF \_ INET6** 位址系列建立的通訊端可以用來在 IPV6 位址或 IPv4 對應位址之間傳送和接收封包。

## <a name="ip-addresses-with-a-dual-stack-socket"></a>具有 Dual-Stack 通訊端的 IP 位址

雙堆疊通訊端一律需要 IPv6 位址。 與 IPv4 位址互動的能力需要使用 IPv4 對應的 IPv6 位址格式。 任何 IPv4 位址都必須以 IPv4 對應的 IPv6 位址格式表示，讓 IPv6 的應用程式能夠與 IPv4 節點進行通訊。 IPv4 對應的 IPv6 位址格式允許 IPv4 節點的 IPv4 位址以 IPv6 位址表示。 IPv4 位址會編碼為 IPv6 位址的低序位32位，而高序位96位會保存固定的前置詞0：0：0：0：0： FFFF。 IPv4 對應的 IPv6 位址格式是在 RFC 4291 中指定的。 如需詳細資訊，請參閱 [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291)。 \_ *Mstcpip* 中的 IN6ADDR SETV4MAPPED 宏可以用來將 ipv4 位址轉換為所需的 ipv4 對應 IPv6 位址格式。

如果基礎通訊協定實際上是 IPv4，則 IPv4 位址會對應至 IPv4 對應的 IPv6 位址格式。 亦即， [SOCKADDR](sockaddr-2.md) 結構中的 [系列] 欄位會指出 AF \_ INET6，但 IPv4 對應的 ipv6 位址會編碼于 IPv6 位址結構中。 在接聽模式的雙重堆疊通訊端中，這表示任何已接受的 IPv4 連線都會傳回 IPv4 對應的 IPv6 位址。 若為連接至 IPv4 目的地的雙重堆疊通訊端，傳遞給 connect 的 SOCKADDR 結構必須是 IPv4 對應的 IPv6 位址。 應用程式必須小心地處理這些 IPv4 對應的 IPv6 位址，並只搭配雙重堆疊通訊端使用它們。 如果要將 IP 位址傳遞給一般 IPv4 通訊端，位址必須是一般的 IPv4 位址，而不是 IPv4 對應的 IPv6 位址。

## <a name="potential-issues-using-a-dual-stack-socket"></a>使用 Dual-Stack 通訊端的潛在問題

應用程式的潛在缺陷是在雙重堆疊通訊端上取得 IPv4 對應的 IPv6 位址，然後嘗試在不同的 IPv6 專用通訊端上使用傳回的 IP 位址。 例如，在雙重堆疊通訊端上使用時， [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) 或 [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) 函式可能會傳回 IPv4 對應的 IPv6 位址。 如果接著在未設定為雙協定的不同通訊端上使用傳回的 IPv4 對應 IPv6 位址， (IPv6 專用通訊端（當建立) 通訊端時是預設行為），則使用此僅限 IPv6 的通訊端（具有 IPv4 對應的 IPv6 位址）將會失敗。 IPv4 對應的 IPv6 位址格式只能用於雙重堆疊通訊端。

在雙重堆疊資料包通訊端上，如果應用程式需要 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式以針對透過 IPv4 接收的資料包來傳回 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中的封包資訊，則在通訊端上的 [IP \_ PKTINFO](ip-pktinfo.md) 通訊端選項必須設為 true。 如果通訊端上的 [ipv6 \_ PKTINFO](ipv6-pktinfo.md) 選項設定為 true，封包資訊將會提供給透過 IPV6 接收的資料包，但可能不會提供給透過 IPv4 接收的資料包。

如果應用程式嘗試設定雙重堆疊資料包通訊端上的 [IP \_ PKTINFO](ip-pktinfo.md) 通訊端選項，而且系統上已停用 IPv4，則 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函式將會失敗，且 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 會傳回 [WSAEINVAL](windows-sockets-error-codes-2.md)錯誤。 **Setsockopt** 函式也會傳回這個相同的錯誤，作為其他錯誤的結果。 如果應用程式嘗試 \_ 在雙重堆疊通訊端上設定 IPPROTO IP 層級通訊端選項，而該選項因為 [WSAEINVAL](windows-sockets-error-codes-2.md)而失敗，則應用程式應判斷本機電腦上是否已停用 IPv4。 可以用來偵測 IPv4 是否已啟用或停用的一個方法，是呼叫具有 *af* 參數設定為 af INET 的 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函式， \_ 以嘗試並建立 IPv4 通訊端。 如果 **通訊端** 函式失敗，而 **WSAGetLastError** 傳回 [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)的錯誤，則表示未啟用 IPv4。 在此情況下，  \_ 應用程式可以忽略嘗試設定 IP PKTINFO 通訊端選項時的 setsockopt 函式失敗。 否則，嘗試設定 IP \_ PKTINFO 通訊端選項時，應該將失敗視為未預期的錯誤。

若為使用 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 函式傳送資料包時的雙重堆疊通訊端，而應用程式想要指定要使用的特定本機 IP 來源位址，處理此情況的方法取決於目的地 IP 位址。 傳送至 IPv4 目的地位址或 IPv4 對應的 IPv6 目的地位址時， *lpMsg* 參數所指向的 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)結構中所傳遞的其中一個控制資料物件應該包含包含要用於傳送之本機 IPv4 來源位址的 [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)結構。 傳送至不是 IPv4 對應 IPv6 位址的 IPv6 目的地位址時， *lpMsg* 參數所指向的 **WSAMSG** 結構中所傳遞的其中一個控制資料物件應包含 [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)結構，其中包含要用於傳送的本機 IPv6 來源位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[變更 IPv6 Winsock Html5 應用程式的資料結構](changing-data-structures-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的函式呼叫](function-calls-2.md)
</dt> <dt>

[使用硬式編碼的 IPv4 位址](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的消費者介面問題](user-interface-issues-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**在 \_ pktinfo 中**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 

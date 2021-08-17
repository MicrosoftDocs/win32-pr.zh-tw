---
description: 下表說明適用于為 \_ IPv4 位址系列建立之通訊端 (AF INET) 的 IPPROTO IP 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 getsockopt 和 setsockopt 函數參考頁面。
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: IPPROTO_IP 通訊端選項
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 4ce469ab9989bc1cd3ec261e3d3a1b3b819c30443225fee24ae06c92efb6bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927708"
---
# <a name="ipproto_ip-socket-options"></a>IPPROTO \_ IP 通訊端選項

下表說明適用于為 IPv4 位址系列建立之通訊端的 **IPPROTO_IP** 通訊端選項 (AF \_ INET) 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

有些通訊端選項需要比這些資料表可以傳達的更多說明;這類選項包含其他頁面的連結。

## <a name="options"></a>選項。

| 選項 | Get | 集合 | Optval 類型 | 描述 |
|-|-|-|-|-|
| IP_ADD_IFLIST | | 是 | DWORD (IF_INDEX)  | 將介面索引加入與 **IP_IFLIST** 選項相關聯的 IFLIST。 |
| IP_ADD_MEMBERSHIP | | 是 | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | 將通訊端聯結至指定介面上提供的多播群組。 |
| IP_ADD_SOURCE_MEMBERSHIP | | 是 | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | 在指定的介面上加入所提供的多播群組，並接受源自所提供來源位址的資料。 |
| IP \_ 區塊 \_ 來源 | | 是 | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | 將指定的來源以傳送者的形式移除至提供的多播群組和介面。 |
| IP_DEL_IFLIST | | 是 | DWORD (IF_INDEX)  | 從與 **IP_IFLIST** 選項相關聯的 IFLIST 中移除介面索引。 只有應用程式才能移除專案，因此請注意，移除介面之後，專案可能會過時。 |
| IP \_ DONTFRAGMENT | 是 | 是 | DWORD (布林值)  | 指出不論本機 MTU 為何，都不應該分割資料。 僅適用于訊息導向的通訊協定。 Microsoft TCP/IP 提供者尊重 UDP 和 ICMP 的這個選項。 |
| IP \_ 捨棄 \_ 成員資格 | | 是 | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | 從指定的介面離開指定的多播群組。 當支援多播時，服務提供者必須支援此選項。 使用下列方法，在 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)函式呼叫所傳回的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中指出支援： XPI \_ 支援 \_ MULTIPOINT = 1，XP1 \_ MULTIPOINT \_ 控制項 \_ 平面 = 0，XP1 \_ multipoint \_ 資料 \_ 平面 = 0。 |
| IP \_ DROP \_ SOURCE \_ 成員資格 | | 是 | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | 卸載指定多播群組、介面和來源位址的成員資格。 |
| IP_GET_IFLIST | 是 | | DWORD [] (IF_INDEX [] )  | 取得與 **IP_IFLIST** 選項相關聯的目前 IFLIST。 如果未啟用 **IP_IFLIST** ，則會傳回錯誤。 |
| IP \_ HDRINCL | 是 | 是 | DWORD (布林值)  | 設定為 **TRUE** 時，表示應用程式會提供 IP 標頭。 只適用于 SOCK 的 \_ 原始通訊端。 如果應用程式所提供的值為零，TCP/IP 服務提供者可能會設定識別碼欄位。  [IP \_ HDRINCL] 選項只會套用至 SOCK \_ 原始通訊協定類型。 支援 SOCK RAW 的 TCP/IP 服務提供者 \_ 也應支援 IP \_ HDRINCL。  |
| IP_IFLIST | 是 | 是 | DWORD (布林值)  | 取得或設定通訊端的 **IP_IFLIST** 狀態。 當此選項設定為 true 時，資料包接收會限制為 IFLIST 中的介面。 系統會忽略在任何其他介面上接收的資料包。 IFLIST 會開始空白。 使用 **IP_ADD_IFLIST** 和 **IP_DEL_IFLIST** 來編輯 IFLIST。 |
| IP \_ MTU | 是 | | DWORD | 取得系統對路徑 MTU 的估計值。 必須連接通訊端。 |
| IP \_ MTU \_ 探索 | 是 | 是 | DWORD (**PMTUD \_ 狀態**)  | 取得或設定通訊端的路徑 MTU 探索狀態。 預設值為 [ **\_ \_ 未 \_ 設定 IP PMTUDISC**]。 針對串流通訊端 **， \_ \_ 未 \_ 設定 Ip PMTUDISC** ，且 **IP \_ PMTUDISC \_ 確實** 會執行路徑 MTU 探索。 **IP \_PMTUDISC \_** 不會和 **IP \_ PMTUDISC \_ 探查** 將會關閉路徑 MTU 探索。 針對資料包通訊端， **IP \_ PMTUDISC \_** 會強制所有傳出封包都設定 DF 位，而且嘗試傳送大於路徑 MTU 的封包會導致錯誤。 **IP \_PMTUDISC \_** 不會強制所有傳出的封包都未設定 DF 位，而且會根據介面 MTU 來分割封包。 **IP \_PMTUDISC \_ 探查** 會強制所有傳出封包都設定 DF 位，而且嘗試傳送大於介面 MTU 的封包會導致錯誤。 |
| IP \_ 多播 \_ IF | 是 | 是 | DWORD | 取得或設定用於傳送 IPv4 多播流量的輸出介面。 此選項不會變更接收 IPv4 多播流量的預設介面。  設定此選項的輸入值是以網路位元組順序表示的4位元組 IPv4 位址。 這個 DWORD 參數也可以是網路位元組順序的介面索引。 在 0. x. x. x 區塊中的任何 IP 位址 (第一個八位) 的 IP 位址，除非 IPv4 位址0.0.0.0 被視為介面索引。 介面索引是24位數位，且不會使用 0.0.0.0/8 IPv4 位址區塊 (此範圍是保留) 。 介面索引可以用來指定 IPv4 的多播流量預設介面。 如果 *optval* 為零，則會指定接收多播的預設介面來傳送多播流量。  取得此選項時， *optval* 會傳回目前的預設介面索引，以依主機位元組順序傳送多播 IPv4 流量。 |
| IP \_ 多播 \_ 迴圈 | 是 | 是 | DWORD (布林值)  | 控制應用程式在本機電腦上傳送的資料 (不一定是在多播會話中的相同通訊端) ，將會由聯結至回送介面上多播目的地群組的通訊端接收。 **TRUE** 值會導致本機電腦上的應用程式傳送的多播資料，傳遞給回送介面上的接聽通訊端。 值為 **FALSE** 可防止本機電腦上的應用程式傳送的多播資料，將其傳遞至回送介面上的接聽通訊端。 預設會啟用 **IP \_ 多播 \_ 回送** 。 |
| IP \_ 多播 \_ TTL | 是 | 是 | DWORD | 設定/取得與通訊端上 IP 多播流量相關聯的 TTL 值。 |
| IP \_ 選項 | 是 | 是 | 字元 \[\] | 指定要插入傳出封包中的 IP 選項。 設定新選項會覆寫所有先前指定的選項。 將 optval 設定為零會移除所有先前指定的選項。 \_不需要 ip 選項支援; 若要檢查是否 \_ 支援 ip 選項，請使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)來取得目前的選項。 如果 **getsockopt** 失敗， \_ 則不支援 IP 選項。 |
| IP \_ 原始 \_ 抵達（ \_ 如果 | 是 | 是 | DWORD (布林值)  | 指出 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式是否應該傳回選擇性的控制項資料，其中包含針對資料包通訊端接收封包的抵達介面。 此選項可讓接收封包的 IPv4 介面，在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回。  此選項只適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| [IP \_ PKTINFO](ip-pktinfo.md) | 是 | 是 | DWORD | 指出 **WSARecvMsg** 函數應該傳回封包資訊。 |
| IP \_ 接收 \_ 廣播 | 是 | 是 | DWORD (布林值)  | 允許或封鎖廣播接收。 |
| IP \_ RECVIF | 是 | 是 | DWORD (布林值)  | 指出 IP 堆疊是否應在控制項緩衝區中填入有關使用資料包通訊端接收封包的介面詳細資料。 當此值為 true 時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式會傳回選擇性的控制項資料，其中包含針對資料包通訊端接收封包的介面。 此選項可讓接收封包的 IPv4 介面，在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回。  此選項只適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IP \_ RECVTOS | 是 | 是 | DWORD (布林值)  | 指出 IP 堆疊是否應該在收到的資料包上，使用包含服務類型 (TOS) IPv4 標頭欄位的訊息來擴展控制項緩衝區。 當此值為 true 時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式會傳回選擇性的控制項資料，其中包含所接收資料包的 TOS IPv4 標頭域值。  此選項允許在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回所接收資料包的 [TOS IPv4 標頭] 欄位。 傳回的訊息類型將是 IP \_ TOS。 將會傳回 TOS 欄位的所有 DSCP 和 ECN 位。  此選項只適用于資料包通訊端， (通訊端類型必須是 SOCK \_ DGRAM) 。  |
| IP \_ RECVTTL | 是 | 是 | DWORD (布林值)  | 表示應該在 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式中傳回躍點 (TTL) 資訊。 如果在呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)時， *optval* 設定為 **1** ，則會啟用此選項。 如果設定為 **0**，則會停用此選項。  此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IP \_ TOS | 是 | 是 | DWORD (布林值)  | 請勿使用。 服務類型 (TOS) 設定只能使用服務 API 的品質來設定。 如需詳細資訊，請參閱 Platform SDK 的服務品質一節中的 [差異服務](/previous-versions/windows/desktop/qos/differentiated-services) 。 |
| IP \_ TTL | 是 | 是 | DWORD (布林值)  | 在傳出資料包的 IP 標頭的 TTL 欄位中，變更 TCP/IP 服務提供者所設定的預設值。 \_不需要 ip ttl 支援; 若要檢查 ip \_ ttl 是否受支援，請使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)來取得目前的選項。 如果 **getsockopt** 失敗， \_ 則不支援 IP TTL。 |
| IP \_ 解除封鎖 \_ 來源 | | 是 | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | 將指定來源以傳送者的形式新增至提供的多播群組和介面。 |
| IP \_ 單播（ \_ 如果 | 是 | 是 | 如果索引) ，則為 DWORD (\_ | 取得或設定用於傳送 IPv4 流量的輸出介面。 此選項不會變更接收 IPv4 流量的預設介面。 此選項對於多重主目錄電腦而言很重要。  設定此選項的輸入值是以網路位元組順序表示的4位元組 IPv4 位址。 這個 DWORD 參數必須是以網路位元組順序排列的介面索引。 在 0. x. x. x 區塊中的任何 IP 位址 (第一個八位) 的 IP 位址，除非 IPv4 位址0.0.0.0 被視為介面索引。 介面索引是24位數位，且不會使用 0.0.0.0/8 IPv4 位址區塊 (此範圍是保留) 。 介面索引可以用來指定傳送 IPv4 流量的預設介面。 [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)函數可以用來取得介面索引資訊。 如果 *optval* 為零，則傳送流量的預設介面會設定為 [未指定]。  取得這個選項時， *optval* 會傳回目前的預設介面索引，以依主機位元組順序傳送 IPv4 流量。 |
| IP_USER_MTU | 是 | 是 | DWORD | 取得或設定指定之通訊端的 IP 層 MTU (（位元組) ）上限。 如果值高於系統對路徑 MTU 的估計 (您可以藉由查詢 **IP_MTU** 通訊端選項) 在連接的通訊端上抓取，則選項不會有任何作用。 如果值較低，則大於此值的輸出封包將會被分割，或者將無法傳送，視 **IP_DONTFRAGMENT** 的值而定。 預設值為 **IP_UNSPECIFIED_USER_MTU** (MAXULONG) 。 針對型別安全，您應該使用 [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) 和 [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) 函式，而不是直接使用通訊端選項。 |
| IP \_ WFP 重新 \_ 導向 \_ 內容 | 是 | 是 | 具有控制資料的 WSACMSGHDR | 資料包通訊端附屬資料類型 (cmsg \_ 類型) 指出使用者模式所使用 UDP 通訊端的重新導向內容 Windows 篩選平台 (WFP) 重新導向服務。 |
| IP \_ WFP 重新 \_ 導向 \_ 記錄 | 是 | 是 | 具有控制資料的 WSACMSGHDR | 資料包通訊端附屬資料類型 (cmsg \_ 類型) 指出使用者模式所使用 UDP 通訊端的重新導向記錄 Windows 篩選平台 (WFP) 重新導向服務。 |

## <a name="windows-support-for-ip_proto-options"></a>IP PROTO 選項的 Windows 支援 \_

| 選項 | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IP \_ 新增 \_ 成員資格 | x | x | x | x | x | x |
| IP \_ 新增 \_ 來源 \_ 成員資格 | x | x | x | x | x | x |
| IP \_ 區塊 \_ 來源 | x | x | x | x | x | x |
| IP_DEL_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IP \_ DONTFRAGMENT | x | x | x | x | x | x |
| IP \_ 捨棄 \_ 成員資格 | x | x | x | x | x | x |
| IP \_ DROP \_ SOURCE \_ 成員資格 | x | x | x | x | x | x |
| IP_GET_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IP \_ HDRINCL | x | x | x | x | x | x |
| IP_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IP \_ 多播 \_ IF | x | x | x | x | x | x |
| IP \_ 多播 \_ 迴圈 | x | x | x | x | x | x |
| IP \_ 多播 \_ TTL | x | x | x | x | x | x |
| IP \_ 選項 | x | x | x | x | x | x |
| IP \_ 原始 \_ 抵達（ \_ 如果 | x | x | x | x | | |
| IP \_ PKTINFO | x | x | x | x | x | x |
| IP \_ 接收 \_ 廣播 | x | x | x | x | x | x |
| IP \_ RECVIF | 從 Windows 10 開始，版本1703 | x | x | x | x | x |
| IP \_ RECVTTL | x | | | | | |
| IP \_ TOS | x | x | x | | | |
| IP \_ TTL | x | x | x | x | x | x |
| IP \_ 解除封鎖 \_ 來源 | x | x | x | x | x | x |
| IP \_ 單播（ \_ 如果 | x | x | x | x | x | x |
| IP \_ WFP 重新 \_ 導向 \_ 內容 | x | x | x | | | |
| IP \_ WFP 重新 \_ 導向 \_ 記錄 | x | x | x | | | |

<br/>

| 選項 | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| IP \_ 新增 \_ 成員資格 | x | x |
| IP \_ 新增 \_ 來源 \_ 成員資格 | x | x |
| IP \_ 區塊 \_ 來源 | x | x |
| IP_DEL_IFLIST | | |
| IP \_ DONTFRAGMENT | x | x |
| IP \_ 捨棄 \_ 成員資格 | x | x |
| IP \_ DROP \_ SOURCE \_ 成員資格 | x | x |
| IP_GET_IFLIST | | |
| IP \_ HDRINCL | x | x |
| IP_IFLIST | | |
| IP \_ 多播 \_ IF | x | x |
| IP \_ 多播 \_ 迴圈 | x | x |
| IP \_ 多播 \_ TTL | x | x |
| IP \_ 選項 | x | x |
| IP \_ 原始 \_ 抵達（ \_ 如果 | | |
| IP \_ PKTINFO | x | x |
| IP \_ 接收 \_ 廣播 | x | x |
| IP \_ RECVIF | | |
| IP \_ RECVTTL | | |
| IP \_ TOS | | |
| IP \_ TTL | x | x |
| IP \_ 解除封鎖 \_ 來源 | x | x |
| IP \_ 單播（ \_ 如果 | | |
| IP \_ WFP 重新 \_ 導向 \_ 內容 | | |
| IP \_ WFP 重新 \_ 導向 \_ 記錄 | | |

## <a name="remarks"></a>備註

在 Windows Vista 和更新版本中發行的 Microsoft Windows 軟體開發套件 (SDK) 中，標頭檔的組織已變更，且 **IPPROTO \_ IP** 層級定義于 *Ws2def .h* 標頭檔中，該檔案會自動包含在 *Winsock2* 標頭檔中。 某些 **IPPROTO \_ IP** 通訊端選項定義于 *Ws2ipdef .h* 標頭檔中，該檔案會自動包含在 *Ws2tcpip .h* 標頭檔中。 其餘的 **IPPROTO \_ IP** 通訊端選項是在 *Wsipv6ok .h* 標頭檔中定義，此檔案會自動包含在 *Winsock2* 標頭檔中。 絕不能直接使用 *Ws2def .h*、 *Ws2ipdef .h* 和 *Wsipv6ok .h* 標頭檔。

在針對 Windows Server 2003 和 Windows XP 發行的 Platform SDK 中， **IPPROTO \_ IP** 層級會定義于 *Winsock2* 標頭檔中。 某些 **IPPROTO \_ IP** 通訊端選項定義于 *Ws2tcpip .h* 標頭檔中。 其餘的 **IPPROTO \_ IP** 通訊端選項是在 *Wsipv6ok .h* 標頭檔中定義，此檔案會自動包含在 *Winsock2* 標頭檔中。 不應直接使用 *Wsipv6ok* 標頭檔。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | <dl> <dt>Ws2def (包含 Winsock2. h) ;</dt><dt>Ws2ipdef (包括 Ws2tcpip .h) ;</dt><dt>Wsipv6ok (包含 Winsock2) </dt> </dl> |

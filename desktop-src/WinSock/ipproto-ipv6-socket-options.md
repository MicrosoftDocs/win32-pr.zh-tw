---
description: 下表說明適用于為 \_ ipv6 位址系列建立之通訊端 (AF INET6) 的 IPPROTO IPV6 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 getsockopt 和 setsockopt 函數參考頁面。
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: IPPROTO_IPV6 通訊端選項
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 1ceaf08c2a59a24b9ff694ac9ff42b28fbf18480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994042"
---
# <a name="ipproto_ipv6-socket-options"></a>IPPROTO \_ IPV6 通訊端選項

下表說明適用于為 IPv6 位址系列建立之通訊端 (AF INET6) 的 **IPPROTO \_ IPV6** 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

有些通訊端選項需要比這些資料表可以傳達的更多說明;這類選項包含其他資訊的連結。

## <a name="options"></a>選項。

| 選項 | get | set | Optval 類型 | Description |
|-|-|-|-|-|
| IP \_ 原始 \_ 抵達（ \_ 如果 | 是 | 是 | DWORD (布林值)  | 指出 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式是否應該傳回選擇性的控制項資料，其中包含針對資料包通訊端接收封包的原始抵達介面。 此選項適用于 IPv6 轉換技術 (6to4、ISATAP 和 Teredo 通道，例如，當 IPv6 主機必須將 IP4 網路移到其他 IPv6 網路時，為單播 IPv6 流量提供位址指派和主機對主機自動通道的) 。 IPv6 封包是以通道方式傳送為 IPv4 封包。 此選項可讓已接收封包的原始 IPv4 介面，在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回。  |
| IPV6_ADD_IFLIST | | 是 | DWORD (IF_INDEX)  | 將介面索引加入與 **IP_IFLIST** 選項相關聯的 IFLIST。 |
| IPV6 \_ 新增 \_ 成員資格 | | 是 | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | 將通訊端聯結至指定介面上提供的多播群組。  此選項只適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IPV6_DEL_IFLIST | | 是 | DWORD (IF_INDEX)  | 從與 **IP_IFLIST** 選項相關聯的 IFLIST 中移除介面索引。 只有應用程式才能移除專案，因此請注意，移除介面之後，專案可能會過時。 |
| IPV6 \_ 捨棄 \_ 成員資格 | | 是 | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | 將提供的多播群組保留在指定的介面中。  此選項只適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IPV6_GET_IFLIST | 是 | | DWORD [] (IF_INDEX [] )  | 取得與 **IP_IFLIST** 選項相關聯的目前 IFLIST。 如果未啟用 **IP_IFLIST** ，則會傳回錯誤。 |
| IPV6 \_ HDRINCL | 是 | 是 | DWORD (布林值)  | 表示應用程式會在所有傳出資料上提供 IPv6 標頭。 如果在呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)時， *optval* 參數設定為 **1** ，則會啟用此選項。 如果 *optval* 設定為 **0**，則會停用此選項。 預設值為已停用。 此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 支援 SOCK RAW 的 TCP/IP 服務提供者 \_ 也應支援 IPV6 \_ HDRINCL。 |
| IPV6 \_ HOPLIMIT | 是 | 是 | DWORD (布林值)  | 表示應該在 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式中傳回躍點 (TTL) 資訊。 如果在呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)時， *optval* 設定為 **1** ，則會啟用此選項。 如果設定為 **0**，則會停用此選項。  此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IPV6_IFLIST | 是 | 是 | DWORD (布林值)  | 取得或設定通訊端的 **IP_IFLIST** 狀態。 當此選項設定為 true 時，資料包接收會限制為 IFLIST 中的介面。 系統會忽略在任何其他介面上接收的資料包。 IFLIST 會開始空白。 使用 **IP_ADD_IFLIST** 和 **IP_DEL_IFLIST** 來編輯 IFLIST。 |
| IPV6 \_ 聯結 \_ 群組 | | 是 | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | 與 IPV6 \_ 新增 \_ 成員資格相同 |
| IPV6 \_ 離開 \_ 群組 | | 是 | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | 與 IPV6 \_ DROP \_ 成員資格相同 |
| IPV6 \_ MTU | 是 | | DWORD | 取得系統對路徑 MTU 的估計值。 必須連接通訊端。 |
| IPV6 \_ MTU \_ 探索 | 是 | 是 | DWORD (**PMTUD \_ 狀態**)  | 取得或設定通訊端的路徑 MTU 探索狀態。 預設值為 [ **\_ \_ 未 \_ 設定 IP PMTUDISC**]。 針對串流通訊端 **， \_ \_ 未 \_ 設定 Ip PMTUDISC** ，且 **IP \_ PMTUDISC \_ 確實** 會執行路徑 MTU 探索。 **IP \_PMTUDISC \_** 不會和 **IP \_ PMTUDISC \_ 探查** 將會關閉路徑 MTU 探索。 針對資料包通訊端，如果設定為 [ **IP \_ PMTUDISC \_** ]，則嘗試傳送大於路徑 MTU 的封包將會導致錯誤。 如果設定為 **[ \_ IP \_ PMTUDISC**]，封包將會根據介面 MTU 進行分割。 如果設定為 **IP \_ PMTUDISC \_ 探查**，則嘗試傳送大於介面 MTU 的封包會導致錯誤。  |
| IPV6 \_ 多播 \_ 躍點 | 是 | 是 | DWORD | 取得或設定與通訊端上 IPv6 多播流量相關聯的 TTL 值。 將 TTL 設定為大於255的值是不合法的。  此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IPV6 \_ 多播 \_ IF | 是 | 是 | DWORD | 取得或設定傳送 IPv6 多播流量的輸出介面。 此選項不會變更接收 IPv6 多播流量的預設介面。 此選項對於多重主目錄電腦而言很重要。  設定此選項的輸入值是以主機位元組順序表示之所需輸出介面的4位元組介面索引。 [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)函數可以用來取得介面索引資訊。 如果在呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)時， *Optval* 設定為 **Null** ，則會使用預設 IPv6 介面。 如果 *optval* 為零，則會指定接收多播的預設介面來傳送多播流量。  取得此選項時， *optval* 會傳回目前的預設介面索引，以依主機位元組順序傳送多播 IPv6 流量。 |
| IPV6 \_ 多播 \_ 迴圈 | 是 | 是 | DWORD (布林值)  | 指出在通訊端上傳送的多播資料，如果它也聯結到目的地多播群組，則會將它送至通訊端接收緩衝區。 如果在呼叫 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)時， *optval* 設定為 **1** ，則會啟用此選項。 如果設定為 **0**，則會停用此選項。  此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| [IPV6 \_ PKTINFO](ipv6-pktinfo.md) | 是 | 是 | DWORD (布林值)  | 指出 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函數應該傳回封包資訊。 |
| [IPV6 \_ 保護 \_ 層級](ipv6-protection-level.md) | 是 | 是 | INT | 啟用通訊端至指定範圍的限制，例如具有相同連結本機或網站本機前置詞的位址。 提供各種限制層級和預設設定。 如需詳細資訊，請參閱 [IPV6 \_ 保護 \_ 層級](ipv6-protection-level.md) 。 |
| IPV6 \_ RECVIF | 是 | 是 | DWORD (布林值)  | 指出 IP 堆疊是否應在控制項緩衝區中填入有關使用資料包通訊端接收封包的介面詳細資料。 當此值為 true 時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式會傳回選擇性的控制項資料，其中包含針對資料包通訊端接收封包的介面。 此選項可讓接收封包的 IPv6 介面，在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回。  此選項僅適用于資料包和原始通訊端， (通訊端類型必須是 SOCK \_ DGRAM 或 SOCK \_ 原始) 。 |
| IPV6 \_ RECVTCLASS | 是 | 是 | DWORD (布林值)  | 指出 IP 堆疊是否應該在收到的資料包中，以包含流量類別 IPv6 標頭欄位的訊息填入控制項緩衝區。 當此值為 true 時， [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) 函式會傳回選擇性的控制項資料，其中包含所接收資料包的流量類別 IPv6 標頭域值。  此選項可讓接收資料包的流量類別 IPv6 標頭欄位在 [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) 結構中傳回。 傳回的訊息類型會是 IPV6 \_ TCLASS。 將會傳回 [流量類別] 欄位的所有 DSCP 和 ECN 位。  此選項只適用于資料包通訊端， (通訊端類型必須是 SOCK \_ DGRAM) 。  |
| IPV6 \_ 單播 \_ 躍點 | 是 | 是 | DWORD | 取得或設定與 IPv6 通訊端相關聯的目前 TTL 值（用於單播流量）。 將 TTL 設定為大於255的值是不合法的。 |
| IPV6 \_ 單播 \_ IF | 是 | 是 | 如果索引) ，則為 DWORD (\_ | 取得或設定用來傳送 IPv6 流量的輸出介面。 此選項不會變更接收 IPv6 流量的預設介面。 此選項對於多重主目錄電腦而言很重要。  設定此選項的輸入值是以主機位元組順序表示之所需輸出介面的4位元組介面索引。 [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)函數可以用來取得介面索引資訊。 如果 *optval* 為零，則傳送 IPv6 流量的預設介面會設定為 [未指定]。  取得此選項時， *optval* 會傳回目前的預設介面索引，以依主機位元組順序傳送 IPv6 流量。 |
| IPV6_USER_MTU | 是 | 是 | DWORD | 取得或設定指定之通訊端的 IP 層 MTU (（位元組) ）上限。 如果值高於系統對路徑 MTU 的估計 (您可以藉由查詢 **IPV6_MTU** 通訊端選項) 在連接的通訊端上抓取，則選項不會有任何作用。 如果值較低，則大於此值的輸出封包將會被分割，或者將無法傳送，視 **IPV6_DONTFRAG** 的值而定。 預設值為 **IP_UNSPECIFIED_USER_MTU** (MAXULONG) 。 針對型別安全，您應該使用 [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) 和 [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) 函式，而不是直接使用通訊端選項。 |
| IPV6 \_ V6ONLY | 是 | 是 | DWORD (布林值)  | 指出為 AF INET6 位址系列建立的通訊端 \_ 是否僅限於 IPv6 通訊。 為 AF INET6 位址系列建立的通訊端可 \_ 用於 IPv6 和 IPv4 通訊。 某些應用程式可能會想要將為 AF INET6 位址系列建立的通訊端限制 \_ 為僅限 IPv6 通訊。 當此值為非零 (Windows) 上的預設值時，為 AF INET6 位址系列建立的通訊端只能 \_ 用來傳送和接收 IPv6 封包。 當此值為零時，為 AF INET6 位址系列建立的通訊端 \_ 可以用來在 IPv6 位址或 IPv4 位址之間傳送和接收封包。 請注意，必須使用 IPv4 對應位址，才能發揮與 IPv4 位址互動的能力。 Windows Vista (含) 以後版本支援這個通訊端選項。 |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>IPPROTO \_ IPV6 通訊端選項的 Windows 支援

| 選項 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP \_ 原始 \_ 抵達（ \_ 如果 | x | x | x | | |
| IPV6_ADD_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IPV6 \_ 新增 \_ 成員資格 | x | x | x | x | x |
| IPV6_DEL_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IPV6 \_ 捨棄 \_ 成員資格 | x | x | x | x | x |
| IPV6_GET_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IPV6 \_ HDRINCL | x | x | x | x | x |
| IPV6 \_ HOPLIMIT | x | x | x | x | x |
| IPV6_IFLIST | 從 Windows 10 開始，版本1803 | | | | | |
| IPV6 \_ 聯結 \_ 群組 | x | x | x | x | x |
| IPV6 \_ 離開 \_ 群組 | x | x | x | x | x |
| IPV6 \_ 多播 \_ 躍點 | x | x | x | x | x |
| IPV6 \_ 多播 \_ IF | x | x | x | x | x |
| IPV6 \_ 多播 \_ 迴圈 | x | x | x | x | x |
| IPV6 \_ PKTINFO | x | x | x | x | x |
| [IPV6 \_ 保護 \_ 層級](ipv6-protection-level.md) | x | x | x | x | x |
| IPV6 \_ RECVIF | x | x | x | x | x |
| IPV6 \_ 單播 \_ 躍點 | x | x | x | x | x |
| IPV6 \_ 單播 \_ IF | x | x | x | x | x |
| IPV6 \_ V6ONLY | x | x | x | x | x |

<br/>

| 選項 | Windows Server 2003 | Windows XP |
|-|-|-|
| IP \_ 原始 \_ 抵達（ \_ 如果 | | |
| IPV6_ADD_IFLIST | | |
| IPV6 \_ 新增 \_ 成員資格 | x | x |
| IPV6_DEL_IFLIST | | |
| IPV6 \_ 捨棄 \_ 成員資格 | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| IPV6 \_ 聯結 \_ 群組 | x | x |
| IPV6 \_ 離開 \_ 群組 | x | x |
| IPV6 \_ 多播 \_ 躍點 | x | x |
| IPV6 \_ 多播 \_ IF | x | x |
| IPV6 \_ 多播 \_ 迴圈 | x | x |
| IPV6 \_ PKTINFO | x | x |
| [IPV6 \_ 保護 \_ 層級](ipv6-protection-level.md) | x | x |
| IPV6 \_ RECVIF | | |
| IPV6 \_ 單播 \_ 躍點 | x | x |
| IPV6 \_ 單播 \_ IF | | |
| IPV6 \_ V6ONLY | | |

## <a name="remarks"></a>備註

在 Windows Vista （含）以後版本的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已變更，且 **IPPROTO \_ IPV6** 層級定義于 *Ws2def .h* 標頭檔中，該檔案會自動包含在 *Winsock2* 標頭檔中。 **IPPROTO \_ IPV6** 通訊端選項定義于 *Ws2ipdef .h* 標頭檔中，該檔案會自動包含在 *Ws2tcpip .h* 標頭檔中。 不應直接使用 *Ws2def .h* 和 *Ws2ipdef* 標頭檔。

\_ \_ \_ 當 Windows Server 2008 R2 和 windows 7 上支援「通訊端」選項時，IP 原始抵達。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | <dl> <dt>Ws2def (包含 Winsock2. h) ;</dt><dt>Windows Server 2003 和 WINDOWS XP 上的 Winsock2</dt> </dl> |

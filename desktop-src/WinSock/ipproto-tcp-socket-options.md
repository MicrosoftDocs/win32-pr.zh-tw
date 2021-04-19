---
description: 下表說明適用于 \_ IPv4 和 IPv6 位址系列所建立之通訊端的 IPPROTO TCP 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ protocol 參數指定為 tcp (IPPROTO \_ tcp) 。
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: IPPROTO_TCP 通訊端選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994251"
---
# <a name="ipproto_tcp-socket-options"></a>IPPROTO \_ TCP 通訊端選項

下表說明適用于 IPv4 和 IPv6 位址系列所建立之通訊端的 **IPPROTO \_ TCP** 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ *PROTOCOL* 參數 [](/windows/desktop/api/Winsock2/nf-winsock2-socket)指定為 tcp (IPPROTO \_ tcp) 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

## <a name="options"></a>選項。

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>Get</th>
<th>設定</th>
<th>Optval 類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>若 <strong>為 TRUE</strong>，則服務提供者會將 Berkeley 軟體散發 (BSD) 樣式 (預設) 來處理快速資料。 此選項是 TCP_EXPEDITED_1122 選項的反向。 此選項只能在連接上設定一次。 一旦將此選項設為 on，就無法關閉這個選項。 服務提供者不需要執行這個選項。 預設會啟用此選項 (設定為 <strong>TRUE</strong>) 。</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>若 <strong>為 TRUE</strong>，則服務提供者會依照 RFC-1222 中指定的方式來執行快速資料。 否則，會使用 Berkeley 軟體散發 (BSD) 樣式 (預設) 。 此選項只能在連接上設定一次。 一旦將此選項設為 on，就無法關閉這個選項。 服務提供者不需要執行這個選項。</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>若 <strong>為 TRUE</strong>，connect API 呼叫將會在接收到具有值 WSAEHOSTUNREACH 的 ICMP 錯誤時傳回。 錯誤的來源位址接著會透過 TCP_ICMP_ERROR_INFO 通訊端選項提供。 如果 <strong>為 FALSE</strong>，則通訊端會正常運作。 預設為停用 (設定為 <strong>FALSE</strong>) 。 針對型別安全，您應該使用 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> 和 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> 函式，而不是直接使用通訊端選項。</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>是</td>
<td>不可以</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>抓取 TCP 通訊端在失敗的連接呼叫期間收到的 ICMP 錯誤資訊。 只有在先前已啟用 TCP_FAIL_CONNECT_ON_ICMP_ERROR 的 TCP 通訊端上有效，且 <strong>CONNECT</strong> 已傳回 WSAEHOSTUNREACH。 查詢未封鎖。 如果查詢成功，且傳回的 optlen 值為0，則自上次連接呼叫後，就不會收到任何 ICMP 錯誤。 如果收到 ICMP 錯誤，則其資訊將可供使用，直到再次呼叫 <strong>connect</strong> 為止。 這項資訊會以 <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> 結構的形式傳回。 針對型別安全，您應該使用 <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> 函式，而不是直接使用通訊端選項。</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>是</td>
<td>是</td>
<td>DWORD</td>
<td>取得或設定要在連接結束之前傳送的 TCP 保持運作探查數目。 將 TCP_KEEPCNT 設定為大於255的值是不合法的。</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>是</td>
<td>是</td>
<td>DWORD</td>
<td>如果此值為非負數，表示所需的連接逾時（以秒為單位）。 如果是-1，則表示停用連接逾時的要求 (亦即，連接將永遠重新傳輸) 。 如果已停用連接逾時，則每次重新傳輸的重新傳輸超時會以指數方式增加到最大值60sec，然後保持在該處。</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>啟用或停用 TCP 通訊端的 Nagle 演算法。 預設會停用此選項 (設定為 FALSE) 。</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>啟用或停用 RFC 1323 時間戳記。 請注意，也有時間戳記的全域設定 (預設值為 off) &quot; 、 &quot; (set/get) -nettcpsetting 中的時間戳記。 設定此通訊端選項會覆寫全域設定設定。</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>是</td>
<td>是</td>
<td>DWORD (布林值) </td>
<td>啟用或停用「 <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP 快速開啟」，這可讓您在開啟連線的三向交握階段期間開始傳送資料。 請注意，若要使用快速開啟，您應該使用 <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> 進行初始連線，並指定該函式之 <em>lpSendBuffer</em> 參數中的資料，以便在交握程式期間傳送。 <em>LpSendBuffer</em>中的某些資料將會以 Fast Open 通訊協定來傳送。</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>是</td>
<td>是</td>
<td>DWORD</td>
<td>取得或設定在將 keepalive 探查傳送至遠端之前，TCP 連線將維持閒置的秒數。
<blockquote>
[!Note]<br />
從 Windows 10 1709 版開始，可以使用此選項。
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>是</td>
<td>是</td>
<td>DWORD</td>
<td>取得或設定 TCP 連線在傳送另一個 keepalive 探查之前，會等候 keepalive 回應的秒數。
<blockquote>
[!Note]<br />
從 Windows 10 1709 版開始，可以使用此選項。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>IPPROTO TCP 選項的 Windows 支援 \_

| 選項 | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| TCP \_ BSDURGENT | x | x | x | x |
| TCP \_ 加速 \_ 1122 | x | x | x | x |
| TCP \_ KEEPCNT | 從 Windows 10 開始，版本1703 | | | |
| TCP \_ MAXRT | x | x | x | x |
| TCP \_ NODELAY | x | x | x | x |
| TCP \_ 時間戳記 | x | x | x | x |
| TCP \_ FASTOPEN | 從 Windows 10 開始，版本1607 | | | |

<br/>

 | 選項 | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/我 |
|-|-|-|-|-|-|
| TCP \_ BSDURGENT | x | x | x | x | |
| TCP \_ 加速 \_ 1122 | x | x | x | | |
| TCP \_ KEEPCNT | | | | | |
| TCP \_ MAXRT | | | | | |
| TCP \_ NODELAY | x | x | x | x | |
| TCP \_ 時間戳記 | | | | | |
| TCP \_ FASTOPEN | | | | | |

## <a name="remarks"></a>備註

在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中，標頭檔的組織已變更，且 **IPPROTO \_ TCP** 層級定義于 *Ws2def .h* 標頭檔中，該檔案會自動包含在 *Winsock2* 標頭檔中。 **IPPROTO \_ tcp** 通訊端選項（ **tcp \_ BSDURGENT** 除外）定義于 *Ws2ipdef .h* 標頭檔中，該檔案會自動包含于 *Ws2tcpip .h* 標頭檔中。 適用于歷史原因的 **TCP \_ BSDURGENT** 選項定義于 *Mswsock .h* 標頭檔中。 不應直接使用 *Ws2def .h* 和 *Ws2ipdef* 標頭檔。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | <dl> <dt>Ws2def (包含 Winsock2. h) ;</dt><dt>Windows Server 2003、WINDOWS XP 和 windows 2000 上的 Winsock2</dt> </dl> |

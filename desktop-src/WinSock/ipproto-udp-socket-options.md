---
description: 下表描述適用于為 \_ IPv4 和 IPv6 位址系列建立之通訊端的 IPPROTO UDP 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ protocol 參數提供給指定為 udp (IPPROTO \_ udp) 的 socket 函數。
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: IPPROTO_UDP 通訊端選項
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051476"
---
# <a name="ipproto_udp-socket-options"></a>IPPROTO \_ UDP 通訊端選項

下表描述適用于為 IPv4 和 IPv6 位址系列建立之通訊端的 **IPPROTO \_ UDP** 通訊端選項 (AF \_ INET 和 AF INET6) ，並將 \_ *PROTOCOL* 參數提供給指定為 udp (IPPROTO udp) 的 [**socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) 函數 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

## <a name="options"></a>選項。

| 選項 | Get | 集合 | Optval 類型 | 描述 |
|-|-|-|-|-|
| UDP 總和 \_ 檢查碼 \_ 涵蓋範圍 (ws2tcpip .h)  | 是 | 是 | DWORD (布林值)  | 若 **為 TRUE**，則會使用總和檢查碼傳送 UDP 資料包。 |
| UDP \_ NOCHECKSUM (ws2tcpip .h)  | 是 | 是 | DWORD (布林值)  | 若 **為 TRUE**，則會傳送 UDP 資料包，且總和檢查碼為零。 服務提供者所需。 如果服務提供者沒有可停用 UDP 總和檢查碼計算的機制，則可以直接儲存此選項，而不需要採取任何動作。 IPv6 不支援此選項。 |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef .h;包含 ws2tcpip .h)  | 是 | 是 | DWORD | 當設定為非零值時，多個接收的資料包可能會在向您的應用程式表示之前，合併成單一訊息緩衝區。 選項值代表可對您的應用程式表示的合併訊息之訊息大小上限（以位元組為單位）。 可能仍會指出大於選項值的未合併訊息。 預設值為 0 (沒有聯合) 。 只有當資料包源自相同的來源位址和埠時，才會合並。 所有結合的資料包都會具有相同的大小 &mdash; ，但最後一個資料包可能較小。 如果您的應用程式想要抓取資料包大小 (除了最後一個資料包（可能不同) ）之外，您必須使用支援控制資訊的接收 API (例如 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)) 。 除了最後一則訊息的大小，可以在 **UDP_COALESCED_INFO** control 訊息中找到，其類型為 DWORD。 針對型別安全，您的應用程式應該使用 [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) 和 [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) 函式，而不是直接使用通訊端選項。 |
| UDP_SEND_MSG_SIZE (ws2ipdef .h;包含 ws2tcpip .h)  | 是 | 是 | DWORD | 當設定為非零值時，網路堆疊會將您的應用程式傳送的緩衝區細分為多個訊息。 選項值代表每個細分訊息的大小。 選項值以位元組表示。 最後一個區段的大小可能小於選項的值。 預設值為 0 (沒有分割) 。 您的應用程式應該將值設定為低於目的地 () s 的路徑的 MTU，以避免 IP 片段。 針對型別安全，您的應用程式應該使用 [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) 和 [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) 函式，而不是直接使用通訊端選項。 |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>IPPROTO UDP 選項的舊版 Windows 支援 \_

**UDP \_Windows \_** 2000 和 Windows NT4 上無法使用總和檢查碼涵蓋範圍。 **UDP \_Windows \_** 9x/Me 無法使用總和檢查碼涵蓋範圍和 **UDP \_ NOCHECKSUM** 。 

## <a name="remarks"></a>備註

在 Windows Vista 和更新版本所發行的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已變更，且 **IPPROTO \_ UDP** 層級定義于 *Ws2def .h* 標頭檔中，該檔案會自動包含在 *Winsock2* 標頭檔中。 **IPPROTO \_ UDP** 通訊端選項定義于 *Ws2tcpip .h* 標頭檔中。 不應直接使用 *Ws2def* 標頭檔。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭<br/> | <dl> ws2ipdef (包含<dt>Windows Server 2003、Windows XP 和 Windows 2000 上的</dt> <dt>ws2tcpip .h) 和 ws2tcpip .h</dt> </dl> |

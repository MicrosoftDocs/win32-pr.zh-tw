---
description: 下表摘要說明一些適用于 Windows 通訊端2的通訊端選項。
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: 通訊端選項和 IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979956"
---
# <a name="socket-options-and-ioctls"></a>通訊端選項和 IOCTLs

下表摘要說明一些適用于 Windows 通訊端2的通訊端選項。 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))和/或 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))的第4節提供更詳細的資訊。 您可以在 Protocol-Specific 附錄中找到其他新的通訊協定特定通訊端選項。 Winsock 參考中提供適用于 Windows 通訊端的 [**通訊端選項**](socket-options.md) 完整清單。

如需部分 Winsock Ioctls 的摘要，請參閱 [通訊端 Ioctl opcode 的摘要](summary-of-socket-ioctl-opcodes-2.md)。 Winsock 參考中提供完整的 [**Winsock IOCTLs**](winsock-ioctls.md) 清單。

## <a name="summary-of-common-socket-options"></a>一般通訊端選項的摘要

Winsock 服務提供者必須辨識所有這些選項，而 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) 的 () 會傳回每個選項的合理值。 下表顯示每個選項的預設值。

值

類型

意義

預設

注意

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN

BOOL

通訊端正在接聽。

如果已執行 [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) ，則為 FALSE。

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_廣播

BOOL

通訊端已設定為傳輸和接收廣播訊息。

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>\_DEBUG

BOOL

已啟用偵錯工具。

FALSE

 (我) 

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER

BOOL

若為 true，則 \_ 會停用 [關閉] 選項。

true

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE

BOOL

路由已停用。 成功，但在 AF INET 通訊端上會忽略， \_ 在 \_ 具有 [WSAENOPROTOOPT](windows-sockets-error-codes-2.md)的 af INET6 通訊端上失敗。 在 ATM 通訊端上不受支援 (會導致錯誤) 。

FALSE

 (我) 

<span id="SO_ERROR"></span><span id="so_error"></span>\_錯誤

int

捕獲錯誤狀態並清除。

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_群組 \_ 識別碼

GROUP

保留的。

NULL

僅取得

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_群組 \_ 優先順序

int

保留的。

0

[**所以 \_ KEEPALIVE**](so-keepalive.md)

BOOL

正在傳送 keepalive。 在 ATM 通訊端上不受支援 (會導致錯誤) 。

FALSE

 (我) 

<span id="SO_LINGER"></span><span id="so_linger"></span>\_延遲

結構延遲

傳回目前的延遲選項。

l \_ onoff 是0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_最大 \_ 訊息 \_ 大小

int

訊息通訊端類型訊息的最大輸出大小。 沒有可決定輸入訊息大小上限的布建。 對資料流程導向通訊端沒有任何意義。

執行相依

僅取得

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE

BOOL

正在正常資料流程中接收 OOB 資料。

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO \_ PROTOCOL \_ INFOW

結構 [ **WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

系結至此通訊端之通訊協定的通訊協定資訊描述。

通訊協定相依

僅取得

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF

int

保留給接收的每個通訊端緩衝區空間總數。 這與「 \_ 最大訊息 \_ 大小」無關 \_ ，而且不一定會對應到 TCP 接收視窗的大小。

執行相依

 (我) 

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR

BOOL

此通訊端所系結的位址可供其他人使用。 不適用於 ATM 通訊端。

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF

int

保留給傳送的每個通訊端緩衝區空間總數。 這與「 \_ 最大訊息 \_ 大小」無關 \_ ，而且不一定會對應至 TCP 傳送視窗的大小。

執行相依

 (我) 

<span id="SO_TYPE"></span><span id="so_type"></span>\_請輸入

int

通訊端 (的類型，例如 SOCK \_ STREAM) 。

透過通訊端建立。

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD \_ 設定

字元遠 \*

不透明的資料結構物件，其中包含服務提供者的設定資訊。

執行相依

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NODELAY

BOOL

停用用於傳送聯合的 Nagle 演算法。

執行相依

 (我) 服務提供者可能會在 [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) 上以無訊息方式忽略此選項，並傳回 [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))的常數值，或可能接受 **WSPSetSockOpt** 的值，並傳回 **WSPGetSockOpt** 中的對應值，而不需以任何方式使用此值。



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**通訊端選項**](socket-options.md)
</dt> <dt>

[**SOL \_ 通訊端通訊端選項**](sol-socket-socket-options.md)
</dt> <dt>

[**IPPROTO \_ TCP 通訊端選項**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**IPPROTO \_ UDP 通訊端選項**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> </dl>

 

 

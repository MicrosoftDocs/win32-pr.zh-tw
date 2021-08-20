---
title: 遠端桌面服務 API 結構
description: 列出與遠端桌面服務 API 搭配使用的結構。
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000098"
---
# <a name="remote-desktop-services-api-structures"></a>遠端桌面服務 API 結構

下列結構會與遠端桌面服務 API 搭配使用。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**通道 \_ 定義**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

包含遠端桌面服務虛擬通道的名稱和選項。

</dd> <dt>

[**通道 \_ 進入 \_ 點**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

包含用戶端 DLL 呼叫之函式的指標，以存取虛擬通道。

</dd> <dt>

[**通道 \_ PDU \_ 標頭**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

包含由虛擬通道的伺服器端所接收之資料區塊的相關資訊。

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

包含特定遠端桌面服務授權金鑰套件的相關資訊。

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

包含特定遠端桌面服務授權的相關資訊。

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

包含遠端桌面連線 (RDC) 用戶端的相關資訊。

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

包含遠端桌面服務會話的相關資訊。

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

包含遠端桌面服務會話的相關資訊。

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

包含 [**WTSINFOEX \_ 層級**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) 聯集，其中包含遠端桌面服務會話的延伸資訊。

</dd> <dt>

[**WTSINFOEX \_ 級1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

包含遠端桌面服務會話的延伸資訊。

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

包含遠端桌面服務接聽程式的相關資訊。

</dd> <dt>

[**WTSSBX \_ IP \_ 位址**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

包含網路資源 IP 位址的相關資訊。

</dd> <dt>

[**WTSSBX \_ 電腦 \_ 連接 \_ 資訊**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

包含正在接受遠端連線之電腦的相關資訊。

</dd> <dt>

[**WTSSBX \_ 機器 \_ 資訊**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

包含電腦及其目前狀態的相關資訊。

</dd> <dt>

[**WTSSBX \_ 會話 \_ 資訊**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

包含遠端桌面連線代理人 (RD 連線代理人) 可用之會話的相關資訊。

</dd> <dt>

[**WTSSESSION \_ 通知**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

提供會話變更通知的相關資訊。 服務會在其 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) 函式中接收此結構，以回應會話變更事件。

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

包含網域控制站或遠端桌面工作階段主機 (RD 工作階段主機) server 上使用者的設定資訊。

</dd> <dt>

[**WTS \_用戶端 \_ 位址**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

包含遠端桌面服務會話的用戶端網路位址。

</dd> <dt>

[**WTS \_用戶端 \_ 顯示**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

包含遠端桌面連線 (RDC) 用戶端顯示的相關資訊。

</dd> <dt>

[**WTS \_進程 \_ 資訊**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

包含在 RD 工作階段主機伺服器上執行之進程的相關資訊。

</dd> <dt>

[**WTS \_進程 \_ 資訊， \_ 例如**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

包含在 RD 工作階段主機伺服器上執行之進程的擴充資訊。

</dd> <dt>

[**WTS \_產品 \_ 資訊**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

連接到終端機伺服器所需的產品授權詳細資料。

</dd> <dt>

[**WTS \_伺服器 \_ 資訊**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

包含特定遠端桌面服務伺服器的相關資訊。

</dd> <dt>

[**WTS \_會話 \_ 位址**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

包含指派給會話的虛擬 IP 位址。

</dd> <dt>

[**WTS \_會話 \_ 資訊**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

包含 RD 工作階段主機伺服器上用戶端會話的相關資訊。

</dd> <dt>

[**WTS \_會話 \_ 資訊 \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

包含 RD 工作階段主機伺服器或遠端桌面虛擬化主機 (RD 虛擬化主機) 伺服器上用戶端會話的延伸資訊。

</dd> </dl>

 

 
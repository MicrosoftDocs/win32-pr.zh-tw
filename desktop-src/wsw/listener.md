---
title: 接聽程式
description: 用戶端會使用接聽程式來接受來自服務的傳入通道。
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- 適用于 Windows 的接聽程式 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383325"
---
# <a name="listener"></a>接聽程式

用戶端會使用接聽程式來接受來自服務的傳入 [通道](channel.md) 。

若要建立接聽程式缺少，您必須將通道類型指定為 [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 列舉值、系 [結資訊，](binding.md) 以及要接聽的 [URL](url.md) 。


若要開始在 URL 上接聽，請呼叫 [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) 函數。

若要接受連入通訊，請呼叫 [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)。

若要取消接聽程式的暫止 IO，請呼叫 [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)。

如需有關接聽程式之狀態轉換的詳細資訊，請參閱 WS 接聽程式 [**\_ \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) 列舉。

下列回呼是接聽程式的一部分：

-   [**WS \_ 中止接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ 接受 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ 關閉接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**接聽 \_ \_ \_ 程式回呼的 \_ WS CREATE 通道 \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ 建立接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS \_ 免費接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET 接聽程式 \_ \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ 開啟接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ 重設接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ SET 接聽程式 \_ \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

下列列舉是接聽程式的一部分：

-   [**WS \_ IP \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**WS 接聽程式 \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**WS 接聽程式 \_ \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

下列函數是接聽程式的一部分：

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

下列控制碼是接聽程式的一部分：

-   [WS \_ 接聽程式](ws-listener.md)

下列結構是接聽程式的一部分：

-   [**WS \_ 自訂接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**WS 不 \_ 允許的 \_ 使用者 \_ 代理程式 \_ 子字串**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**WS \_ 主機 \_ 名**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**WS 接聽程式 \_ \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**WS 接聽程式 \_ \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 





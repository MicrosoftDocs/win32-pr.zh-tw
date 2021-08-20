---
title: '內建的標注識別碼 (Fwpmu .h) '
description: 內建于 Windows 篩選平台 (WFP) 的注標函式識別碼，分別以 GUID 表示。 這些識別碼的定義如下。
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151424"
---
# <a name="built-in-callout-identifiers"></a>內建的標注識別碼

內建于 Windows 篩選平台 (WFP) 的注標函式識別碼，分別以 GUID 表示。 這些識別碼的定義如下。

注標識別碼結尾的 V4 和 V6 尾碼會指出標注是針對 IPv4 網路堆疊或 IPv6 網路堆疊。

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 傳輸 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 傳輸 \_ V6** 
</dt> <dd> <dl> <dt>



確認每個接收到的封包都應安全地抵達傳輸模式安全性關聯。

此標注適用于傳輸層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 傳輸 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 傳輸 \_ V6** 
</dt> <dd> <dl> <dt>



指出 IPsec 必須透過傳輸模式安全性關聯保護的輸出流量。

此標注適用于傳輸層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ V6** 
</dt> <dd> <dl> <dt>



確認每個接收到的封包都會安全地抵達通道模式安全性關聯。

此標注適用于傳輸層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸出 \_ 通道 \_ V6** 
</dt> <dd> <dl> <dt>



表示 IPsec 必須透過通道模式安全性關聯保護的輸出流量。

此標注適用于傳輸層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸入 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸入 \_ 通道 \_ V6**
</dt> <dd> <dl> <dt>



確認每個接收到的封包都會安全地抵達通道模式安全性關聯。

此標注適用于轉送層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸出 \_ 通道 \_ V4/FWPM \_ 標注 \_ ipsec \_ 轉寄 \_ 輸出 \_ 通道 \_ V6**
</dt> <dd> <dl> <dt>



表示 IPsec 必須透過通道模式安全性關聯保護的輸出流量。

此標注適用于轉送層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 起始 \_ 安全 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 起始 \_ 安全 \_ V6** 
</dt> <dd> <dl> <dt>



確認每個應該送達安全的連入連線都安全地送達。

此標注適用于 ALE 接受層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ ale \_ 接受 \_ V4/FWPM \_ 標注 \_ ipsec \_ 輸入 \_ 通道 \_ ale \_ 接受 \_ V6**
</dt> <dd> <dl> <dt>



允許 IPsec 通道模式的 IP 傳入 ip 封包在 ALE 接受層級進行分類。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ 標注 \_ ipsec \_ ale \_ connect \_ V4/FWPM \_ CALLOUT \_ ipsec \_ ale \_ connect \_ V6**
</dt> <dd> <dl> <dt>



將 IPsec 原則修飾詞套用至用戶端應用程式。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ 標注 \_ ipsec \_ DOSP \_ 轉寄 \_ V4/FWPM \_ CALLOUT \_ ipsec \_ DOSP \_ 轉寄 \_ V6**
</dt> <dd> <dl> <dt>



發出 IPsec DoS 保護的信號，指出需要驗證流量是否有潛在的 DoS，而且可能需要受到速率限制。

> [!Note]  
> 僅適用于 Windows 7 和 Windows Server 2008 R2。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ 標注 \_ wfp \_ 傳輸 \_ 層 \_ V4 \_ 無訊息卸載 \_ /FWPM \_ 標注 \_ wfp \_ 傳輸 \_ 層 \_ V6 \_ 無 \_ 訊息卸載**
</dt> <dd> <dl> <dt>



以無訊息方式卸載所有 TCP 沒有接聽端點的傳入封包，以執行隱形模式篩選。

此標注適用于輸入傳輸捨棄層。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ 標注 \_ tcp \_ 煙囪 \_ 連接 \_ 層 \_ V4/FWPM \_ 注 \_ tcp \_ 煙囪 \_ 連接 \_ 層 \_ V6**
</dt> <dd> <dl> <dt>



啟用或停用每個連出連線的 TCP 煙囪卸載。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ 標注 \_ tcp \_ 煙囪 \_ 接受 \_ 層 \_ V4/FWPM \_ 注 \_ tcp \_ 煙囪 \_ 接受 \_ 層 \_ V6**
</dt> <dd> <dl> <dt>



針對每個連入連線啟用或停用 TCP 煙囪卸載。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ 標注 \_ set \_ options \_ auth \_ connect \_ layer \_ V4/FWPM \_ CALLOUT \_ set \_ options \_ auth \_ connect \_ layer \_ V6**
</dt> <dd> <dl> <dt>



設定輸出流程的分類選項。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM 注標 \_ \_ 設定 \_ 選項 \_ 驗證 \_ 接收 \_ 接受 \_ 層 \_ V4/FWPM 注標 \_ \_ set \_ 選項 \_ 驗證 \_ 接收 \_ 接受 \_ 層 \_ V6**
</dt> <dd> <dl> <dt>



設定輸入流程的分類選項。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM 注標 \_ \_ 保留 \_ auth \_ CONNECT \_ layer \_ V4/FWPM \_ CALLOUT \_ reserved \_ auth \_ connect \_ layer \_ V6**
</dt> <dd> <dl> <dt>



此識別碼已保留供內部使用。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ v6/FWPM \_ 注 \_ TEREDO \_ ale \_ 接聽 \_ v6**
</dt> <dd> <dl> <dt>



向 Teredo 服務發出通知，表示應用程式需要 Teredo 位址。

> [!Note]  
> 針對 Windows 7 和更新版本，請使用 **FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ V6**。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ale \_ 資源 \_ 指派 \_ v6/FWPM \_ 標注 \_ TEREDO \_ ale \_ 資源 \_ 指派 \_ v6**
</dt> <dd> <dl> <dt>



向 Teredo 服務發出通知，表示應用程式需要 Teredo 位址。

> [!Note]  
> 針對 Windows 7 和更新版本，請使用 **FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 資源 \_ 指派 \_ V6**。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 資源 \_ 指派 \_ V4** 
</dt> <dd> <dl> <dt>



此識別碼保留供日後使用。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ 標注 \_ EDGE \_ 遍歷 \_ ALE \_ 接聽 \_ V4**
</dt> <dd> <dl> <dt>



此識別碼保留供日後使用。


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM 注標 \_ \_ tcp \_ 範本 \_ 連接 \_ 層 \_ V4/FWPM 注標 \_ \_ tcp \_ 範本 \_ 連接 \_ 層 \_ V6**
</dt> <dd> <dl> <dt>



針對相符的傳出連接套用 TCP 範本設定。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM 注標 \_ \_ tcp \_ 範本 \_ 接受 \_ 層 \_ V4/FWPM 注標 \_ \_ tcp \_ 範本 \_ 接受 \_ 圖層 \_ V6**
</dt> <dd> <dl> <dt>



套用 TCP 範本設定以進行相符的連入連線。

> [!Note]  
> 僅適用于 Windows 8 和 Windows Server 2012。

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



 

 






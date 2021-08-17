---
title: " (Fwpmu 的篩選內容識別碼) "
description: 內建于 Windows 篩選平台之篩選內容的識別碼。
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc7d9914a9b6089ace87e7e9b942499d8e65dc7705bf524f74cddf96ee419d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951267"
---
# <a name="filter-context-identifiers"></a>篩選內容識別碼

內建至 Windows 篩選平台之篩選內容的識別碼定義如下。

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ PASSTHRU、FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保存 \_ 連接 \_ 安全性、FWPM \_ 內容 \_ IPSEC \_ 輸入 \_ 保留**
</dt> <dd> <dl> <dt>



輸入層中的 IPsec 傳輸篩選內容。


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 協商 \_ 探索，FWPM \_ 內容 \_ IPSEC \_ 輸出 \_ 隱藏的 \_ 協商**
</dt> <dd> <dl> <dt>



輸出層中的 IPsec 傳輸篩選內容。

> [!Note]  
> 針對 Windows 7，請使用 **FWPM \_ 內容 \_ IPSEC \_ 輸出隱藏的 \_ \_ 協商**。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 安全性，FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 延遲 \_ SD \_ 評估**
</dt> <dd> <dl> <dt>



用於 ALE 連接層的篩選內容。


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ 內容 \_ ALE \_ 設定 \_ 連接 \_ 需要 \_ IPSEC \_ 加密，FWPM \_ 內容 \_ ALE \_ 設定 \_ 連線 \_ 允許 \_ 第 \_ 一個 \_ 輸入 \_ 的 PKT 未加密，FWPM \_ 內容 \_ ALE \_ 允許 \_ 驗證 \_ FW**
</dt> <dd> <dl> <dt>



用於 ALE 連接或接受層的篩選內容。

> [!Note]  
> 針對 Windows 7，請使用 **FWPM \_ 內容 \_ ale 設定連線 \_ \_ \_ 允許 \_ 第一個 \_ 輸入的 \_ PKT \_ 未加密，** 或 **FWPM \_ 內容 \_ ale \_ 允許 \_ 驗證 \_ FW**。

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM \_ 內容 \_ TCP \_ 煙囪 \_ 卸載 \_ 啟用，FWPM \_ 內容 \_ TCP \_ 煙囪 \_ 卸載 \_ 停用**
</dt> <dd> <dl> <dt>



TCP 煙囪卸載標注所使用的內容。


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_已啟用 FWPM 內容 \_ RPC \_ AUDIT \_**
</dt> <dd> <dl> <dt>



RPC audit 子層中使用的內容。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Fwpmu。h</dt> </dl> |



 

 






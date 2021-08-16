---
title: 驗證等級
description: 驗證層級會控制用戶端或伺服器希望其 SSP 有多少安全性。
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c468408a22f1ea0c0fae67d7ce3d5f5b40f8a6342538614c1619acd40574ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311148"
---
# <a name="authentication-level"></a>驗證等級

驗證層級會控制用戶端或伺服器希望其 SSP 有多少安全性。 驗證層級是透過 DwAuthnLevel 參數傳遞適當的 \_ RPC \_ C 驗證 \_ level \_ xxx 值給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 所設定。 用戶端和伺服器的驗證層級會在交握期間進行比較，並使用較高層級的安全性保護設定來進行連接。

不同的驗證等級如下所述，從最低層級安全性保護到最高：

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>無 (RPC \_ C \_ 驗證 \_ 層級 \_ 無) 
</dt> <dd>

在用戶端與伺服器之間進行通訊時，不會執行任何驗證。 系統會忽略所有安全性設定。 只有在 [驗證服務層級](com-authentication-service-constants.md) 為 [RPC \_ C \_ 驗證無] 時，才可以設定此驗證等級 \_ 。

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>預設 (RPC \_ C \_ 驗證 \_ LEVEL \_ default) 
</dt> <dd>

COM 會使用其一般安全性整體協商來選擇驗證等級。 它永遠不會選擇 [無] 的驗證層級。

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>連線 (RPC \_ C \_ 驗證 \_ LEVEL \_ Connect) 
</dt> <dd>

一般驗證交握會在用戶端與伺服器之間進行，並建立工作階段金鑰，但永遠不會將該金鑰用於用戶端與伺服器之間的通訊。 交握之後的所有通訊都不是安全的。

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>呼叫 (RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫) 
</dt> <dd>

只有每個呼叫開頭的標頭會經過簽署。 用戶端與伺服器之間交換的其餘資料都不會進行簽署或加密。 大部分的 Ssp 都不支援此驗證層級，並以無訊息方式將它升級為封包。

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>封包 (RPC \_ C \_ 驗證 \_ 層級 \_ PKT) 
</dt> <dd>

每個封包的標頭都已簽署但未加密。 封包本身不會進行簽署或加密。

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>封包完整性 (RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 完整性) 
</dt> <dd>

每個資料封包都會完整登入，但不會加密。 由於所有資料都是由傳送者簽署，因此收件者可以確定在傳輸期間沒有任何資料遭到篡改。

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>封包隱私權 (RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權) 
</dt> <dd>

每個資料封包都會經過簽署和加密。 這有助於保護用戶端與伺服器之間的整個通訊。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 





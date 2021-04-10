---
title: '驗證服務常數 (RpcDce .h) '
description: 藉由識別提供服務的安全性封裝（例如 NTLMSSP、Kerberos 或 Schannel）來定義驗證服務。
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106319"
---
# <a name="authentication-service-constants"></a>驗證服務常數

藉由識別提供服務的安全性封裝（例如 NTLMSSP、Kerberos 或 Schannel）來定義驗證服務。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 無**</dt> <dt>0</dt> </dl>                              | 不需要驗證。<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DCE \_ 私**</dt>用 <dt>1</dt> </dl>        | DCE 私密金鑰驗證。<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | DCE 公開金鑰驗證。<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DEC \_ 公用**</dt> <dt>4</dt> </dl>           | DEC 公開金鑰驗證。 保留供未來使用。<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ 協商**</dt> <dt>9</dt> </dl>  | Snego 安全性支援提供者。<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_C \_ 驗證 \_ WINNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ SCHANNEL**</dt>安全通道 <dt>14</dt> </dl>    | Schannel 安全性支援提供者。 此驗證服務支援 SSL 2.0、SSL 3.0、TLS 和 PCT。<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | Kerberos 安全性支援提供者。<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DPA**</dt> <dt>17</dt> </dl>                                | DPA 安全性支援提供者。<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_C \_ 驗證 \_ MSN**</dt> <dt>18</dt> </dl>                                | MSN 安全性支援提供者。<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 核心**</dt> <dt>20</dt> </dl>                       | 核心安全性支援提供者。<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 摘要**</dt> <dt>21</dt> </dl>                       | 摘要式安全性支援提供者。<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_C \_ 驗證 \_ NEGO \_**</dt>擴充項 <dt>30</dt> </dl> | NEGO 擴充項安全性支援提供者。<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_C \_ 驗證 \_ PKU2U**</dt> <dt>31</dt> </dl>                          | PKU2U 安全性支援提供者。<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_C \_ 驗證 \_ MQ**</dt> <dt>100</dt> </dl>                                  | MQ 安全性支援提供者。<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 預設**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | 系統預設驗證服務。 指定此值時，COM 會使用其一般安全性全面協商演算法來挑選驗證服務。 如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。 <br/> |



## <a name="remarks"></a>備註

這些常數會用於唯一的 [**\_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) 和唯一的 [**\_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 結構中。 **唯一的 \_ 驗證 \_ 服務** 結構會由伺服器傳遞至 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)函式，而且可以由 [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)函數抓取。 用戶端會將 **唯一 \_ 驗證 \_ 資訊** 結構的指標傳遞至 **CoInitializeSecurity**。 如需這些值（例如 NTLMSSP 和 Kerberos）所識別之安全性封裝的詳細資訊，請參閱 [COM 和安全性封裝](com-and-security-packages.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>RpcDce。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**唯一 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 


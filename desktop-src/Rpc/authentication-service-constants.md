---
title: 'Authentication-Service 常數 (Rpcdce) '
description: 驗證服務常數代表傳遞給各種執行時間函數的驗證服務。
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509207"
---
# <a name="authentication-service-constants"></a>Authentication-Service 常數

驗證服務常數代表傳遞給各種執行時間函數的驗證服務。

下列常數是 *AuthnSvc* 參數的有效值。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 無**</dt> <dt>0</dt> </dl>                              | 不需要驗證。<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DCE \_ 私**</dt>用 <dt>1</dt> </dl>        | 使用分散式運算環境 (DCE) 私密金鑰驗證。<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | 「DCE 公開金鑰驗證」 (保留供日後使用) 。<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DEC \_ 公用**</dt> <dt>4</dt> </dl>           | DEC 公開金鑰驗證 (保留供日後使用) 。<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ 協商**</dt> <dt>9</dt> </dl>  | 使用 [Microsoft NEGOTIATE SSP](/windows/desktop/SecAuthN/microsoft-negotiate)。 此 SSP 會在使用 NTLM 和 Kerberos 通訊協定安全性支援提供者 (SSP) 之間進行協調。<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_C \_ 驗證 \_ WINNT**</dt> <dt>10</dt> </dl>                          | 使用 [MICROSOFT NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm)。<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ SCHANNEL**</dt>安全通道 <dt>14</dt> </dl>    | 使用 [SCHANNEL SSP](/windows/desktop/SecAuthN/secure-channel)。 此 SSP 支援安全通訊端層 (SSL) 、私用通訊技術 (PCT) ，以及傳輸層級安全性 (TLS) 。<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_C \_ 驗證 \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | 使用 [Microsoft KERBEROS SSP](/windows/desktop/SecAuthN/microsoft-kerberos)。<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_C \_ 驗證 \_ DPA**</dt> <dt>17</dt> </dl>                                | 使用 (DPA) 的分散式密碼驗證。<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_C \_ 驗證 \_ MSN**</dt> <dt>18</dt> </dl>                                | 用於 Microsoft Network (MSN) 的驗證通訊協定 SSP。<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 摘要**</dt> <dt>21</dt> </dl>                       | Windows XP 或更新版本：使用 [MICROSOFT DIGEST SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_C \_ 驗證 \_ NEGO \_**</dt>擴充項 <dt>30</dt> </dl> | Windows 7 或更新版本：已保留。 請勿使用<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_C \_ 驗證 \_ MQ**</dt> <dt>100</dt> </dl>                                  | 這個 SSP 會為 Microsoft 訊息佇列提供 SSPI 相容的包裝函式， (MSMQ) 傳輸層級的通訊協定。<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_C \_ 驗證 \_ 預設**</dt>為 <dt>0xffffffff</dt> </dl>            | 使用預設驗證服務。<br/>                                                                                                                                   |



## <a name="remarks"></a>備註

針對透過系結 \_ \_ \_ 控制碼發出的遠端程序呼叫，指定 RPC C 驗證 NONE 來關閉驗證。 當您指定 RPC \_ c \_ 驗證 \_ 預設值時，rpc 執行時間程式庫會使用 rpc \_ c \_ 驗證 \_ WINNT 驗證服務來進行使用系結控制碼進行的遠端程序呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 


---
title: 'Authentication-Level 常數 (Rpcdce) '
description: 驗證層級常數代表傳遞給各種執行時間函數的驗證層級。
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509208"
---
# <a name="authentication-level-constants"></a>驗證層級常數

驗證層級常數代表傳遞給各種執行時間函數的驗證層級。 這些層級會依提高驗證順序列出。 每個新層級都會加入至上一個層級所提供的驗證。 如果 RPC 執行時間程式庫不支援指定的層級，則會自動升級至下一個較高的支援層級。



| 常數                                                                                                                                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 預設值**</dt> </dl>                    | 使用指定驗證服務的預設驗證層級。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 無**</dt> </dl>                             | 不執行任何驗證。<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT**</dt> </dl>                    | 只有在用戶端與伺服器建立關聯性時才會驗證。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫**</dt> </dl>                             | 當伺服器收到要求時，只會在每個遠端程序呼叫的開頭進行驗證。 不會套用至使用以連線為基礎的通訊協定順序所建立的遠端程序呼叫， (開頭為 "ncacn" 前置詞的 ) 。 如果系結控制碼中的通訊協定順序是以連線為基礎的通訊協定順序，而您指定此層級，則此常式會改為使用 RPC \_ C \_ 驗證 \_ 層級的 \_ PKT 常數。<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ 層級 \_ PKT**</dt> </dl>                                | 只會驗證收到的所有資料來自預期的用戶端。 不會驗證資料本身。<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性**</dt> </dl> | 驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**</dt> </dl>       | 包含所有先前的層級，並確保只有寄件者和接收者可以看到純文字資料。 在本機案例中，這牽涉到使用安全通道。 在遠端案例中，這牽涉到加密每個遠端程序呼叫的引數值。<br/>                                                                                                                                                                 |



## <a name="remarks"></a>備註

無論常數所指定的值為何， **ncalrpc** 一律會使用 RPC \_ C \_ 驗證 \_ 層 \_ 級 \_ 的 PKT 隱私權。

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

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 






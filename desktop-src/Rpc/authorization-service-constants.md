---
title: 'Authorization-Service 常數 (Rpcdce) '
description: 授權服務常數代表傳遞給各種執行時間函數的授權服務。
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027b32acb8b38ac1359cee96f68542da94f48d3bdf7d454d631bf0a8eff1092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023428"
---
# <a name="authorization-service-constants"></a>Authorization-Service 常數

授權服務常數代表傳遞給各種執行時間函數的授權服務。

下列常數是 *AuthzSvc* 參數的有效值。 大部分的應用程式都發現 RPC \_ C \_ AUTHZ \_ 沒有足夠的許可權。



| 常數/值                                                                                                                                                                                                                                    | 描述                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ 無**</dt> <dt>0</dt> </dl>                   | 伺服器不會執行任何授權。<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ 名稱**</dt> <dt>1</dt> </dl>                   | 伺服器會根據用戶端的主體名稱執行授權。<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | 伺服器會使用用戶端的 DCE 許可權屬性憑證來執行授權檢查 (PAC) 資訊，此資訊會透過使用系結控制碼的每個遠端程序呼叫傳送至伺服器。 一般而言，會根據 ([acl](/windows/desktop/api/winnt/ns-winnt-acl)) 的 DCE 存取控制清單來檢查存取權。<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_C \_ 授權 \_ 預設**</dt>為 <dt>0xffffffff</dt> </dl> | 伺服器使用目前 SSP 的預設授權服務。<br/>                                                                                                                                                                                                                                |



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
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 


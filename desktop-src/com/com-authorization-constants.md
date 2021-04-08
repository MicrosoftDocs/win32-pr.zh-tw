---
title: " (RpcDce 的授權常數) "
description: 定義伺服器授權的內容。
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686532"
---
# <a name="authorization-constants"></a>授權常數

定義伺服器授權的內容。



| 常數/值                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ 無**</dt> <dt>0</dt> </dl>                   | 伺服器不會執行任何授權。 目前，RPC \_ c \_ 驗證 \_ WINNT、rpc \_ c \_ 驗證 \_ gss \_ SCHANNEL 和 rpc \_ c \_ 驗證 \_ GSS \_ KERBEROS 全都只使用 rpc \_ c \_ 授權 \_ 無。<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ 名稱**</dt> <dt>1</dt> </dl>                   | 伺服器會根據用戶端的主體名稱執行授權。 <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | 伺服器會使用用戶端的 DCE 許可權屬性憑證來執行授權檢查 (PAC) 資訊，此資訊會透過使用系結控制碼的每個遠端程序呼叫傳送至伺服器。 一般而言，會根據 (Acl) 的 DCE 存取控制清單來檢查存取權。 <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_C \_ 授權 \_ 預設**</dt>為 <dt>0xffffffff</dt> </dl> | DCOM 可以選擇使用其一般安全性整體協商演算法的授權層級。 如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。<br/>                                                                                           |



## <a name="remarks"></a>備註

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)介面的方法會使用這些常數。 它們是在 [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)函式所取出的 [**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)結構中使用。 它們也會用在 [**唯一的 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 結構中，而後者又是 [**唯一 \_ 驗證 \_ 清單**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) 結構的成員。 此結構是驗證服務的清單、他們執行的授權服務，以及每個服務的驗證資訊，都會傳遞至 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式和 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 方法。

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

 


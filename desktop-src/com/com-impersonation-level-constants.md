---
title: '模擬層級常數 (RpcDce .h) '
description: 指定模擬等級，指出當伺服器模擬用戶端時，提供給伺服器的授權數量。
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048486"
---
# <a name="impersonation-level-constants"></a>模擬層級常數

指定模擬等級，指出當伺服器模擬用戶端時，提供給伺服器的授權數量。



| 常數/值                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_C \_ IMP \_ 層級 \_ 預設值**</dt> <dt>0</dt> </dl>             | DCOM 可以選擇使用其一般安全性整體協商演算法的模擬等級。 如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_C \_ IMP \_ 層級 \_ 匿名**</dt> <dt>1</dt> </dl>       | 用戶端對伺服器而言是匿名。 伺服器進程可以模擬用戶端，但模擬權杖將不會包含任何資訊，也無法使用。<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_C \_ IMP \_ 層級 \_ 識別**</dt> <dt>2</dt> </dl>          | 伺服器可以取得用戶端的身分識別。 伺服器可以模擬用戶端進行 ACL 檢查，但是無法存取系統物件做為用戶端。 <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_C \_ IMP \_ 層 \_ 級**</dt>模擬 <dt>3</dt> </dl> | 伺服器進程可在代表用戶端時模擬用戶端的安全性內容。 此層級的模擬可用來存取本機資源，例如檔案。 模擬此層級時，模擬權杖只能跨一個電腦界限傳遞。 [Schannel](schannel.md)驗證服務只支援此層級的模擬。 <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_C \_ IMP \_ 層級 \_ 委派**</dt> <dt>4</dt> </dl>          | 伺服器進程可在代表用戶端時模擬用戶端的安全性內容。 伺服器進程也可以在代表用戶端的情況下，使用掩蓋來撥打電話給其他伺服器。 伺服器可能會在其他電腦上使用用戶端的安全性內容，以用戶端的形式存取本機和遠端資源。 當模擬此層級時，模擬權杖可以跨任意數目的電腦界限傳遞。<br/> |



## <a name="remarks"></a>備註

在識別層級進行模擬時， [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)將會失敗。 解決方法是模擬、呼叫 [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)、還原、呼叫 [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)，最後呼叫 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)。 使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)，用戶端會設定模擬等級

用戶端會使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)來設定模擬等級和 proxy 身分識別，以便在伺服器呼叫 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)時使用。 在進行模擬時，伺服器將會看到的身分識別會在 [掩蓋](cloaking.md)中描述。 請注意，在模擬時進行呼叫時，被呼叫端通常會接收呼叫端的進程權杖，而不是呼叫端的模擬權杖。 若要接收呼叫端的模擬權杖，呼叫端必須啟用遮蓋。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>RpcDce。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[隱形](cloaking.md)
</dt> </dl>

 


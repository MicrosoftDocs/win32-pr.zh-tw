---
description: 帳戶許可權會決定使用者帳戶可以執行的登入類型。 系統管理員會將帳戶許可權指派給使用者和群組帳戶。 每個使用者帳戶許可權包含授與使用者的許可權，以及使用者所屬的群組。
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: '帳戶許可權常數 (Ntsecapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4285561761908308f67585544bef6c87d2f0ebbaa25de9989f53fcab051b79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785364"
---
# <a name="account-rights-constants"></a>帳戶許可權常數

帳戶許可權會決定使用者帳戶可以執行的登入類型。 系統管理員會將帳戶許可權指派給使用者和群組帳戶。 每個使用者的帳戶許可權包含授與使用者的許可權，以及使用者所屬的群組。

系統管理員可以使用「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」 (LSA) 功能來處理帳戶許可權。 [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)和 [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights)函數會從帳戶新增或移除帳戶許可權。 [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)函式會列舉指定帳戶所持有的帳戶許可權。 [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)函式會列舉持有指定帳戶許可權的帳戶。

下列帳戶正確常數可用來控制帳戶的登入能力。 如果登入的帳戶沒有所要執行之登入類型所需的帳戶許可權，則 [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) 或 [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) 函式會失敗。



| 常數/值                                                                                                                                                                                                                                                                                                                           | 描述                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**SE \_BATCH \_ 登入 \_ 名稱**</dt><dt>文字 ( "登入 sebatchlogonright" )</dt> </dl>                                                                         | 需要帳戶才能使用 batch 登入類型登入。<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**SE \_拒絕 \_ 批次 \_ 登入 \_ 名稱**</dt><dt>文字 ( "SeDenyBatchLogonRight" )</dt> </dl>                                                     | 使用批次登入類型，明確地拒絕帳戶登入的許可權。<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**SE \_拒絕 \_ 互動式 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeDenyInteractiveLogonRight" )</dt> </dl>                             | 明確拒絕帳戶使用互動式登入類型登入的許可權。<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**SE \_拒絕 \_ 網路 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeDenyNetworkLogonRight" )</dt> </dl>                                             | 明確拒絕帳戶使用網路登入類型登入的許可權。<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**SE \_拒絕 \_ 遠端 \_ 互動式 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeDenyRemoteInteractiveLogonRight" )</dt> </dl> | 明確拒絕帳戶使用互動式登入類型從遠端登入的許可權。<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**SE \_拒絕 \_ 服務 \_ 登入 \_ 名稱**</dt><dt>文字 ( "SeDenyServiceLogonRight" )</dt> </dl>                                             | 明確拒絕帳戶使用服務登入類型登入的許可權。<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**SE \_互動式 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeInteractiveLogonRight" )</dt> </dl>                                                 | 需要帳戶才能使用互動式登入類型登入。<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**SE \_網路 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeNetworkLogonRight" )</dt> </dl>                                                                 | 需要帳戶才能使用網路登入類型登入。<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**SE \_遠端 \_ 互動式 \_ 登錄 \_ 名稱**</dt><dt>文字 ( "SeRemoteInteractiveLogonRight" )</dt> </dl>                     | 帳戶需要使用互動式登入類型從遠端登入。<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**SE \_服務 \_ 登入 \_ 名稱**</dt><dt>文字 ( "SeServiceLogonRight" )</dt> </dl>                                                                 | 需要帳戶才能使用服務登入類型登入。<br/>                             |



## <a name="remarks"></a>備註

SE \_ 拒絕許可權會覆寫對應的帳戶許可權。 系統管理員可以將 SE \_ 拒絕許可權指派給帳戶，以覆寫帳戶可能因為群組成員資格而產生的任何登入許可權。 例如，您可以為 \_ 所有人指派 SE 網路 \_ 登入名稱， \_ 但將 SE \_ 拒絕網路登入名稱指派給系統 \_ \_ \_ 管理員，以防止電腦的遠端系統管理。

上述簡介中提及的所有 LSA 函數都支援帳戶權利和 [許可權](privilege-constants.md)。 但不同于許可權， [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 和 [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) 函數不支援帳戶許可權。 如果 TokenGroups （而非 TokenPrivileges）指定為 *TokenInformationClass* 參數的值，則 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)函式會取得帳戶許可權的資訊。

先前的帳戶右常數會定義為 Ntsecapi 中的字串。 例如，SE 的 \_ 互動式 \_ 登錄 \_ 名稱常數會定義為 "SeInteractiveLogonRight"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntsecapi。h</dt> </dl> |



 


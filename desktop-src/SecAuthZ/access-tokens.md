---
description: 存取權杖是描述進程或執行緒之安全性內容的物件。
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: 存取權杖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849887"
---
# <a name="access-tokens"></a>存取權杖

[*存取權杖*](/windows/desktop/SecGloss/a-gly)是描述 [*進程*](/windows/desktop/SecGloss/p-gly)或執行緒之 [*安全性內容*](/windows/desktop/SecGloss/s-gly)的物件。 權杖中的資訊包括與進程或執行緒相關聯之使用者帳戶的身分識別和許可權。 當使用者登入時，系統會將使用者的密碼與儲存在安全性資料庫中的資訊進行比較，以驗證該使用者的密碼。 如果密碼 [*經過驗證*](/windows/desktop/SecGloss/a-gly)，系統會產生存取權杖。 代表此使用者執行的每個處理常式都有此存取權杖的複本。

當執行緒與 [安全物件](securable-objects.md) 互動，或嘗試執行需要許可權的系統工作時，系統會使用存取權杖來識別使用者。 存取權杖包含下列資訊：

-   使用者帳戶 (SID) 的[安全識別碼](security-identifiers.md)
-   使用者為其成員之群組的 Sid
-   識別目前 [*登入會話*](/windows/desktop/SecGloss/l-gly)的 [*登入 SID*](/windows/desktop/SecGloss/l-gly)
-   使用者或使用者群組所持有的 [許可權](privileges.md) 清單
-   擁有者 SID
-   主要群組的 SID
-   當使用者建立安全物件但未指定 [*安全描述項*](/windows/desktop/SecGloss/s-gly)時，系統所使用的預設 [DACL](access-control-lists.md)
-   存取權杖的來源
-   權杖是否為 [*主要*](/windows/desktop/SecGloss/p-gly)[或模擬](client-impersonation.md)權杖
-   [限制 sid](restricted-tokens.md)的選擇性清單
-   目前的模擬層級
-   其他統計資料

每個處理常式都有一個 [*主要權杖*](/windows/desktop/SecGloss/p-gly) ，可描述與處理常式相關聯之使用者帳戶的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 。 根據預設，當進程的執行緒與安全物件互動時，系統會使用主要權杖。 此外，執行緒也可以模擬用戶端帳戶。 模擬可讓執行緒使用用戶端的安全性內容，與安全物件互動。 模仿用戶端的執行緒同時具有主要權杖和模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。

您可以使用 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 函式來抓取進程主要 token 的控制碼。 您可以使用 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函式來抓取執行緒模擬權杖的控制碼。 如需詳細資訊， [請參閱模擬](client-impersonation.md)。

您可以使用下列函數來操作存取權杖。



| 函式                                               | 描述                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | 變更存取權杖中的群組資訊。                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | 啟用或停用存取權杖中的許可權。 它不會授與新的許可權或撤銷現有的許可權。                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | 判斷指定的存取權杖中是否已啟用指定的 SID。                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | 建立新的權杖，此權杖是現有權杖的受限制版本。 受限的權杖可以停用 Sid、已刪除的許可權，以及受限 Sid 的清單。 |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | 建立新的模擬權杖，以複製現有的權杖。                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | 建立新的主要權杖或模擬權杖，以複製現有的權杖。                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | 抓取權杖的相關資訊。                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | 判斷權杖是否有限制 Sid 的清單。                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | 抓取進程的主要存取權杖控制碼。                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | 抓取執行緒之模擬存取權杖的控制碼。                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | 指派或移除執行緒的模擬權杖。                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | 變更權杖的擁有者、主要群組或預設的 DACL。                                                                                                               |



 

存取權杖函數會使用下列結構來描述存取權杖的部分。



| 結構                                            | Description                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**TOKEN \_ 控制項**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | 識別存取權杖的資訊。                                                          |
| [**TOKEN \_ 預設 \_ DACL**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | 系統線上程所建立之新物件的安全描述項中使用的預設 DACL。 |
| [**權杖 \_ 群組**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | 指定存取權杖中群組 Sid 的 Sid 和屬性。                               |
| [**權杖 \_ 擁有者**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | 新物件之安全描述項的預設擁有者 SID。                                    |
| [**權杖 \_ 主要 \_ 群組**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | 新物件之安全描述項的預設主要群組 SID。                            |
| [**權杖 \_ 許可權**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | 與存取權杖相關聯的許可權。 也可決定是否啟用許可權。   |
| [**權杖 \_ 來源**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | 存取權杖的來源。                                                                        |
| [**權杖 \_ 統計資料**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | 與存取權杖相關聯的統計資料。                                                           |
| [**權杖 \_ 使用者**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | 與存取權杖相關聯之使用者的 SID。                                                  |



 

存取權杖函數會使用下列列舉類型。



| 列舉類型                                             | 指定                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**TOKEN \_ 資訊 \_ 類別**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | 識別要設定或從存取權杖中取出的資訊類型。 |
| [**TOKEN \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | 將存取權杖識別為主要或模擬權杖。                 |



 

 

 

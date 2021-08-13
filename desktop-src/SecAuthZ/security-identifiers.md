---
description: " (SID) 的安全識別碼是用來識別信任者之可變長度的唯一值。"
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: 安全性識別元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6acaaeacfbc77b2dc814062c4254c5f08e58869e0b6d8b2fbb64e8511dc31e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413488"
---
# <a name="security-identifiers"></a>安全性識別元

 (SID) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) 是用來識別 [信任者](trustees.md)之可變長度的唯一值。 每個帳戶都有授權單位所發行的唯一 SID，例如 Windows 網域控制站，並儲存在安全性資料庫中。 每次使用者登入時，系統會從資料庫抓取該使用者的 SID，並將其放在該使用者的 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中。 系統會在存取權杖中使用 SID，以在後續與 Windows 安全性的互動中識別使用者。 使用 SID 做為使用者或群組的唯一識別碼時，不能再次用來識別另一個使用者或群組。

Windows 安全性會在下列安全性元素中使用 sid：

-   在 [安全描述項](security-descriptors.md) 中識別物件和主要群組的擁有者
-   在 [存取控制專案](access-control-entries.md)中，識別允許、拒絕或審核存取權的信任者
-   在 [存取權杖](access-tokens.md)中，用來識別使用者和使用者所屬的群組

除了指派給特定使用者和群組的唯一建立的特定網域 Sid 之外，也有已知的 [sid](well-known-sids.md) 可識別一般群組和一般使用者。 例如，已知的 Sid （Everyone 和 World）會識別包含所有使用者的群組。

大部分的應用程式永遠都不需要使用 Sid。 由於 [已知 sid](well-known-sids.md) 的名稱可能會不同，因此您應該使用函式從預先定義的常數建立 SID，而不是使用已知 SID 的名稱。 例如，美國英文版的 Windows 作業系統都有一個名為「內建 \\ 系統管理員」的已知 SID，在國際版的系統上可能會有不同的名稱。 如需建立已知 SID 的範例，請參閱 [在 c + + 中搜尋存取權杖中的 sid](searching-for-a-sid-in-an-access-token-in-c--.md)。

如果您需要使用 Sid，請勿直接操作它們。 相反地，請使用下列函數。



| 函式                                                       | 描述                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | 配置並初始化具有指定之 subauthorities 數目的 SID。                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | 將 SID 轉換成適合顯示、儲存或傳輸的字串格式。                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | 將字串格式 SID 轉換成有效的功能 SID。                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | 將來源 SID 複製到緩衝區。                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | 測試兩個 SID 首碼值是否相等。 除了最後一個 subauthority 值以外，SID 首碼是整個 SID。                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | 測試兩個 Sid 是否相等。 它們必須完全相符才能視為相等。                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | 使用 [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) 函數釋放先前配置的 SID。                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | 抓取 SID 的長度。                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | 抓取 SID 的識別碼授權單位指標。                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | 抓取儲存具有指定 subauthorities 數目之 SID 所需的緩衝區大小。                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | 抓取 SID 中指定之 subauthority 的指標。                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | 捕獲 SID 中的 subauthorities 數目。                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | 初始化 [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) 結構。                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | 藉由確認修訂編號在已知範圍內，且 subauthorities 數目小於最大值，來測試 SID 的有效性。 |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | 抓取對應至指定之帳戶名稱的 SID。                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | 抓取對應至指定之 SID 的帳戶名稱。                                                                                           |



 

 

 

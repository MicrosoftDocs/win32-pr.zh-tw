---
description: 許可權是帳戶（例如使用者或群組帳戶）的許可權，可在本機電腦上執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: 權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cccedffdf5786da07dd2cfd77c3de428ee15ba94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943563"
---
# <a name="privileges"></a>權限

[*許可權*](/windows/desktop/SecGloss/p-gly)是帳戶（例如使用者或群組帳戶）的許可權，可在本機電腦上執行各種系統相關作業，例如關閉系統、載入設備磁碟機，或變更系統時間。 許可權與存取權限有兩種不同之處：

-   許可權可控制對系統資源和系統相關工作的存取，而存取權限則會控制 [安全物件](securable-objects.md)的存取權。
-   系統管理員會將許可權指派給使用者和群組帳戶，而系統會根據在物件 DACL 中的 Ace 授與的存取權限，來授與或拒絕對安全物件的存取權。

每個系統都有一個帳戶資料庫，用來儲存使用者和群組帳戶所持有的許可權。 當使用者登入時，系統會產生一個 [存取權杖](access-tokens.md) ，其中包含使用者許可權的清單，包括授與使用者的許可權，或使用者所屬的群組。 請注意，這些許可權只適用于本機電腦。網域帳戶在不同的電腦上可以有不同的許可權。

當使用者嘗試執行具有特殊許可權的作業時，系統會檢查使用者的存取權杖，以判斷使用者是否擁有必要的許可權，如果是，則會檢查是否已啟用許可權。 如果使用者未通過這些測試，系統就不會執行此操作。

若要判斷存取權杖中所持有的許可權，請呼叫 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 函式，這也表示已啟用哪些許可權。 預設會停用大部分許可權。

Windows API 會定義一組字串常數（例如 SE \_ ASSIGNPRIMARYTOKEN \_ 名稱），以識別各種許可權。 這些常數在所有系統上都相同，並定義于 Winnt. h 中。 如需 Windows 所定義之許可權的表格，請參閱 [許可權常數](authorization-constants.md)。 不過，取得和調整存取權杖中之許可權的函式會使用 [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) 類型來識別許可權。 許可權的 **LUID** 值可能會與另一部電腦不同，以及在同一部電腦上的另一部開機。 若要取得對應至其中一個字串常數的目前 **LUID** ，請使用 [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 函數。 您可以使用 [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) 函式，將 **LUID** 轉換為其對應的字串常數。

系統會提供一組描述每個許可權的顯示名稱。 當您需要對使用者顯示許可權的描述時，這些功能就很有用。 您可以使用 [**LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) 函式，來取得對應至許可權之字串常數的描述字串。 例如，在使用美式英文的系統上，SE \_ SYSTEMTIME 名稱許可權的顯示名稱 \_ 為「變更系統時間」。

您可以使用 [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) 函式來判斷存取權杖是否持有指定的許可權集。 這主要是用來模擬用戶端的伺服器應用程式。

系統管理員可以使用系統管理工具（例如「使用者管理員」）來新增或移除使用者和群組帳戶的許可權。 系統管理員可以透過程式設計的方式，使用 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 函數來處理許可權。 [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)和 [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights)函式會新增或移除帳戶中的許可權。 [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)函式會列舉指定的帳號所持有的許可權。 [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)函式會列舉擁有指定之許可權的帳戶。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[授權常數](authorization-constants.md)
</dt> <dt>

[在 c + + 中啟用和停用許可權](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 

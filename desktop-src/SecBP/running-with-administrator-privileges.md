---
description: 若要協助防止惡意攻擊，請判斷您的應用程式是否需要系統管理員許可權。 對於需要系統管理員許可權的函式，請建立個別的應用程式，並使用 Windows RunAs 命令列命令。
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: 以系統管理員許可權執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622718"
---
# <a name="running-with-administrator-privileges"></a>以系統管理員許可權執行

建立應用程式所需執行的帳戶類型的第一個步驟，就是檢查應用程式將使用的資源，以及它所要呼叫的特殊許可權 Api。 您可能會發現應用程式或其中的大型元件不需要系統管理員許可權。 *撰寫安全* 的程式碼時，Michael Howard 和 David LeBlanc 提供如何執行這項評量的絕佳描述，而且強烈建議您這樣做。  (此資源可能無法在某些語言及國家/地區使用。 ) 

您可以使用下列其中一種方法，提供應用程式所需的許可權，減少暴露于惡意攻擊的風險：

-   以較少許可權的帳戶執行。 執行這項作業的其中一種方式是使用 [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) 來判斷在權杖中啟用的許可權。 如果可用的許可權不適合目前的作業，您可以停用該程式碼，並要求使用者登入具有系統管理員許可權的帳戶。
-   中斷需要系統管理員許可權的個別應用程式功能。 您可以為使用者提供執行 RunAs 命令的快捷方式。 如需有關如何設定快捷方式的詳細指示，請在 [說明] 中搜尋「runas」。 您可以用程式設計的方式，在應用程式的[AppId 金鑰](/windows/desktop/com/appid-key)登錄機碼下設定[RunAs](/windows/desktop/com/runas)命令。
-   藉由呼叫 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) 或 [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (命令列) 來取得使用者名稱和密碼，來驗證使用者。 如需範例，請參閱 [要求使用者提供認證](asking-the-user-for-credentials.md)。
-   模擬使用者。 以高許可權帳戶（例如系統）啟動的進程，可以藉由呼叫 [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) 或類似的模擬函式來模擬使用者帳戶，進而減少許可權層級。 但是，如果對 [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) 的呼叫插入執行緒中，則進程會回到原始系統許可權。

如果您已判斷出應用程式必須在具有系統管理員許可權的帳戶下執行，而且系統管理員密碼必須儲存在軟體系統中，請參閱為安全地執行此操作的方法 [處理密碼](handling-passwords.md) 。

 

 

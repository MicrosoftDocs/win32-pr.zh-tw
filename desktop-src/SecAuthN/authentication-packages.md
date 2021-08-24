---
description: 驗證套件包含在動態連結程式庫中。
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: 驗證套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141361"
---
# <a name="authentication-packages"></a>驗證套件

[*驗證套件*](/windows/desktop/SecGloss/a-gly) 包含在動態連結程式庫中。 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 使用儲存在登錄中的設定資訊來載入驗證套件。 載入多個驗證套件可允許 LSA 支援多個登入程式和多個 [*安全性通訊協定*](/windows/desktop/SecGloss/s-gly)。

登入程式會使用驗證套件來分析登入資料。 藉由新增 [*GINA*](/windows/desktop/SecGloss/g-gly) 來收集所需的登入資料，並視需要新增驗證套件來分析資料，以將新的登入程式新增至系統。

安全性通訊協定是由驗證套件所執行。 驗證套件會遵循安全性通訊協定中所設定的規則和程式，來分析登入資料。

驗證套件負責下列工作：

-   分析登入資料，以判斷是否允許 [*安全性主體*](/windows/desktop/SecGloss/s-gly) 登入系統。
-   建立新的 [*登入會話*](/windows/desktop/SecGloss/l-gly) ，並建立成功驗證主體的唯一 [*登入識別碼*](/windows/desktop/SecGloss/l-gly) 。
-   將安全性資訊傳遞給主體安全性權杖的 LSA。

當使用者嘗試互動式登入時，LSA 會呼叫驗證套件來判斷是否允許使用者登入。 \_例如，MSV1 0 是與 Microsoft Windows 作業系統一起安裝的驗證套件。 MSV1 \_ 0 封裝接受使用者名稱和 [*雜湊*](/windows/desktop/SecGloss/h-gly) 密碼。 它會查閱安全性帳戶管理員 (SAM) 資料庫中的使用者名稱和雜湊密碼組合。 如果登入資料 [*符合儲存的認證，*](/windows/desktop/SecGloss/c-gly)驗證套件會允許登入成功。

成功驗證 [*安全性主體的*](/windows/desktop/SecGloss/s-gly) 認證之後，驗證套件會負責為主體建立新的 LSA 登入會話，並配置可唯一識別登入會話的 [*登入識別碼*](/windows/desktop/SecGloss/l-gly) 。 驗證套件可能會將認證資訊與登入會話產生關聯，以進行後續的驗證要求。 例如，Microsoft 所提供的 MSV1 \_ 0 authentication package () 會將使用者帳戶名稱和使用者密碼的雜湊與每個登入會話產生關聯。

驗證套件也會提供一組 [*安全性識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 和其他適用于 LSA 所建立之安全性權杖的資訊。 此權杖會代表主體的安全性 [*內容*](/windows/desktop/SecGloss/c-gly)，以存取 Windows 作業。

在建立登入會話並與主體產生關聯之後，會以不同于初始登入的方式來處理要求主體所提出的後續驗證要求。 驗證套件不會建立新的登入會話，也不會傳回用來建立權杖的資訊。 不過，驗證套件可以將後續驗證期間所取得的 [*補充*](/windows/desktop/SecGloss/s-gly) 認證與主體的現有登入會話產生關聯。 存取要求的資源時，會取得補充認證，需要的資訊超出初始登入所建立的認證。 例如，當登入的使用者要求 Novell 網路登入時，可以呼叫 Novell 專屬的驗證套件，而且可以驗證 Novell 特定的認證，並與登入會話相關聯。 Novell 重新導向程式可在使用者存取 Novell 網路時，透過 Novell authentication 套件) 參考這些認證 (。

下列主題將討論各種類型的 [*驗證套件*](/windows/desktop/SecGloss/a-gly)：

-   [Windows驗證套件](windows-authentication-packages.md)
-   [安全性支援提供者/驗證套件](security-support-provider-authentication-packages.md)
-   [Microsoft 提供的驗證套件](authentication-packages-provided-by-microsoft.md)
-   [子驗證套件](subauthentication-packages.md)

 

 

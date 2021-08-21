---
description: 由於 COM + 程式庫應用程式是由另一個進程（可能有自己的安全性設定）所裝載，因此程式庫應用程式的安全性需要特別考慮。
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: 程式庫應用程式安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9fa2d03f21707af42fa108cb9c4ecbce6d2a352ea03714961a0eef4f028119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813517"
---
# <a name="library-application-security"></a>程式庫應用程式安全性

由於 COM + 程式庫應用程式是由另一個進程（可能有自己的安全性設定）所裝載，因此程式庫應用程式的安全性需要特別考慮。

下列條件約束適用于程式庫應用程式安全性：

-   程式庫應用程式會在用戶端進程安全性權杖下執行，而不是在自己的使用者身分識別下執行。 他們擁有的許可權與用戶端的許可權一樣多。
-   程式庫應用程式不會控制進程層級安全性。 系統不會將角色中的任何使用者新增至程式的安全描述項。 程式庫應用程式執行自己的存取檢查的唯一方法是使用元件層級安全性。  (查看 [安全性界限](security-boundaries.md)。 ) 
-   您可以啟用或停用驗證，將程式庫應用程式設定為參與或不參與主機進程驗證。  (參閱 [啟用程式庫應用程式的驗證](enabling-authentication-for-a-library-application.md)。 ) 
-   程式庫應用程式無法設定模擬等級;它們會使用主機進程的。

## <a name="using-library-applications-to-limit-application-privilege"></a>使用程式庫應用程式來限制應用程式許可權

在某些情況下，您可能會想要將應用程式明確設定為程式庫應用程式，使其在裝載進程的身分識別下執行。 這麼做基本上會限制應用程式，使其只能存取其用戶端、主機進程可以存取的資源。 程式庫應用程式元件在其上執行的執行緒預設會使用進程 token，因此當它們在應用程式外部呼叫或存取資源（例如，以安全描述項保護的檔案）時，它們就會顯示為用戶端。 對於執行敏感性工作的應用程式而言，這可能是控制其動作範圍的簡易方式。

## <a name="effectively-securing-library-applications"></a>有效保護程式庫應用程式的安全

針對程式庫應用程式設定以角色為基礎的安全性和驗證時，有一些特殊的考慮，讓它們能如預期般執行。 如需詳細資訊，請參閱設定連結 [庫應用程式的安全性](configuring-security-for-library-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




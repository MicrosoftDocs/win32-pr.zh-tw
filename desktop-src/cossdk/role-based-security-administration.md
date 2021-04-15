---
description: Role-Based 安全性管理
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based 安全性管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510671"
---
# <a name="role-based-security-administration"></a>Role-Based 安全性管理

以角色為基礎的安全性是由 COM + 提供的自動服務，可讓您對 COM + 應用程式進行系統管理和強制執行存取控制原則。 使用彈性且可擴充的安全性設定模型，以角色為基礎的安全性可提供更大的優勢，而不會在您的元件內強制執行所有安全性，並提供下列優點：

-   您可以使用 [元件服務] 系統管理工具或系統管理功能，以系統管理的方式設定安全性。
-   當方法層級的角色保護提供足夠的存取控制時，您不需要在元件中撰寫安全性相關的邏輯。
-   您不需要將安全性納入介面或元件設計中。 相反地，您可以依方法逐一設定安全性。
-   您可以將焦點放在您想要強制執行的安全性原則結構，而透過角色，該原則可以明確地表示給部署您應用程式的系統管理員。
-   您可以輕鬆地修改安全性原則，以適應不斷演進的應用程式安全性需求。
-   如果需要，您可以使用以角色為基礎的安全性做為支援平臺，以程式設計方式建立更細微的安全性原則。
-   您可以利用以角色為基礎的安全性來進行詳細的審核，因為您可以取得整個上游呼叫鏈的呼叫端安全性資訊。

> [!Note]  
> 系統應用程式之系統管理員角色中的使用者必須是本機系統管理員群組的成員。 此外，從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。 此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。 將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。

 

請參閱本節中的下列主題，以取得以角色為基礎的安全性如何運作的相關資訊，以及使用它來為應用程式建立安全性原則時應考慮的問題：

-   [使用角色進行用戶端授權](using-roles-for-client-authorization.md)
-   [有效設計角色](designing-roles-effectively.md)
-   [安全性界限](security-boundaries.md)
-   [安全性呼叫內容資訊](security-call-context-information.md)
-   [資訊安全內容屬性](security-context-property.md)

如需有關為應用程式設定以角色為基礎的安全性所需步驟的詳細說明，請參閱設定 [Role-Based 安全性](configuring-role-based-security.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 

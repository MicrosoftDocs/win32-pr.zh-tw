---
description: 當您在包含元件的 COM + 應用程式中使用以角色為基礎的安全性時，您可以從元件記憶體取程式設計的安全性功能。
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: 程式設計元件安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971961"
---
# <a name="programmatic-component-security"></a>程式設計元件安全性

當您在包含元件的 COM + 應用程式中使用以角色為基礎的安全性時，您可以從元件記憶體取程式設計的安全性功能。 您可以檢查角色成員資格，判斷是否已執行特定的程式碼區段，您可以使用安全性呼叫內容物件來存取安全性資訊，也可以判斷是否已啟用目前呼叫的安全性。 您可以使用適用于 Microsoft Visual Basic 應用程式 ([**SecurityCallCoNtext**](securitycallcontext.md) 物件的參考來執行上述所有工作) 或針對 C 和 Microsoft Visual C++ 應用程式) 的 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面 (指標。

如需有關以程式設計的角色為基礎之安全性的詳細資訊，請參閱本節中的下列主題：

-   [檢查角色成員資格](checking-role-membership.md)
-   [判斷是否已啟用 Role-Based 安全性](determining-whether-role-based-security-is-enabled.md)
-   [存取安全性呼叫內容資訊](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a>模擬和 COM 安全性功能

如果您的元件是在不使用角色型安全性的 COM + 應用程式中使用，則無法使用程式設計的角色檢查和安全性呼叫內容資訊。 不過，您可以使用 COM 所提供的程式設計安全性功能。 如需詳細資訊，請參閱 [COM 中的安全性](/windows/desktop/com/security-in-com)。

雖然您可以使用 COM 提供的大部分安全性功能，但您無法從屬於 COM + 應用程式一部分的元件呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，因為 **CoInitializeSecurity** 是由 com + 應用程式執行所在的代理程式所呼叫。 不過，您可以呼叫其他安全性功能，例如 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)，以抓取用戶端的相關資訊。

尤其是當您需要使用用戶端的身分識別來存取某些資源時（例如，存取受安全描述項保護的檔案，或將用戶端的身分識別傳播至資料庫），您可以用程式設計的方式執行模擬。 如需有關何時及如何進行此作業的詳細資訊，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。

## <a name="testing-security-functionality"></a>測試安全性功能

如果您在元件中使用 COM + 程式設計安全性，當您準備好測試元件的安全性功能時，就必須將元件整合至 COM + 應用程式。 如果在未整合至 COM + 應用程式的情況下執行使用 COM + 程式設計安全性的元件，則會擲回例外狀況。 因此，如果您想要確保這類元件也可以成功整合至不屬於 COM + 環境的應用程式，您必須確定這些例外狀況會適當地處理。

## <a name="documenting-security-requirements"></a>記錄安全性需求

如果您要為使用以角色為基礎之安全性的 COM + 應用程式撰寫獨立元件，則需要記載元件，以便在元件整合至 COM + 應用程式時適當地設定安全性。 例如，您應該識別必須新增的角色，並說明每個角色應指派給哪些方法和介面。 此外，如果呼叫如 IsCallerInRole ( "取款" ) 的方法，您應該描述只有 Tellers 可以存取的功能。 您也應該指定是否需要角色，以協助保護整個元件的存取權。

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

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 

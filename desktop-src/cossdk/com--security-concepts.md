---
description: COM + 提供數種安全性功能，可用來協助保護您的 COM + 應用程式，範圍從您設定的服務，到您可以在程式碼中呼叫的 Api。
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: COM + 安全性概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025996"
---
# <a name="com-security-concepts"></a>COM + 安全性概念

COM + 提供數種安全性功能，可用來協助保護您的 COM + 應用程式，範圍從您設定的服務，到您可以在程式碼中呼叫的 Api。

可能的話，針對 COM + 應用程式，最好使用自動安全性，例如宣告式角色型安全性和驗證，而不是在元件內設定安全性。 使用自動安全性可讓您更輕鬆地撰寫和維護元件、更輕鬆地設計整個應用程式的安全性，而且因為它是以系統管理員的方式設定，所以更容易修改應用程式的安全性原則。 這些自動安全性服務可讓您將所有與安全性相關的功能留給您的元件。 當您可以開啟並適當地設定服務時，COM + 將會處理強制執行您所指定安全性原則的詳細資料。

不過，當 COM + 中的自動安全性服務未精確地達成您需要的功能時，您可以擴充這些服務，並在 COM + 所提供的自動安全性平臺上進行擴充。 如果您選擇不使用自動安全性，或您想要使用它，但需要根據您的應用程式的安全性需求來建立它，您可以透過程式設計方式設定安全性的下列選項：

-   以程式設計的角色為基礎的安全性，例如，當您的應用程式啟用以角色為基礎的安全性時，可使用的角色檢查。
-   模擬—適用于當您想要使用用戶端的身分識別來存取受保護的資源時。
-   以安全性呼叫內容資訊為基礎的審核功能，也可在啟用角色安全性時使用。

您使用哪些機制來協助保護指定的應用程式，將取決於該應用程式的特定需求。 某些安全性選擇可能會影響您撰寫元件的方式，有些則會大幅影響應用程式的設計。 在您決定如何為應用程式實施安全性策略之前，您應該先考慮其整體設計內容中的安全性需求，包括效能需求、資料存取、實體設計，以及選擇最適合的安全性功能組合。 如需有關如何執行程式設計安全性的詳細資訊，請參閱程式 [設計元件安全性](programmatic-component-security.md)。

您可以在這裡提供 COM + 安全性類別、功能和問題的簡短說明，以及本節中的主題連結，提供每個重要領域的詳細討論。

> [!Note]  
> 雖然本節未討論過，但是佇列元件也會有特定的問題，這些問題與它們可用的安全性功能有關。 如需詳細資訊，請參閱已 [排入佇列的元件安全性](queued-components-security.md) 和 [開發佇列元件](developing-queued-components.md)。

 

## <a name="role-based-security"></a>以角色為基礎的安全性

以角色為基礎的安全性是 COM + 應用程式安全性的核心功能。 您可以使用角色來管理應用程式的授權原則，如有必要，請選擇向下 (到方法層級，) 哪些使用者可以存取哪些資源。 此外，如果您的應用程式需要更細微的存取控制，角色就會提供在程式碼中強制執行安全性檢查的架構。

以角色為基礎的安全性建基於一般機制，可讓您在對您的元件發出呼叫的鏈中，取得有關所有上游呼叫端的安全性資訊。 如果您想要進行詳細的審核和記錄，這項功能特別有用。 如需 COM + 所提供之審核功能的描述，請參閱 [存取安全性呼叫內容資訊](accessing-security-call-context-information.md)。

如需使用時應考慮以角色為基礎的安全性和管理問題的說明，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。

## <a name="client-authentication"></a>用戶端驗證

在授權用戶端能夠存取資源之前，您必須先確信它們是誰。 為了啟用此身分識別驗證，COM + 會提供驗證服務。 雖然這些服務實際上是由 COM 和 Microsoft Windows 提供更基本的層級，但 COM + 應用程式可讓您以系統管理的方式開啟驗證服務，使其在應用程式的透明範圍中運作。 如需驗證服務的描述，請參閱 [用戶端驗證](client-authentication.md)。

## <a name="client-impersonation-and-delegation"></a>用戶端模擬和委派

在某些情況下，您的應用程式需要使用用戶端的身分識別來代表用戶端執行工作，例如，存取即將驗證原始用戶端的資料庫時。 這需要您的應用程式模擬用戶端。 COM + 提供的工具可啟用各種層級的模擬。 模擬是以系統管理員的方式設定，但您也必須使用應用程式元件的程式碼來提供模擬支援。 如需模擬和其使用相關問題的說明，請參閱 [用戶端模擬和委派](client-impersonation-and-delegation.md)。

## <a name="using-the-software-restriction-policy-in-com"></a>在 COM + 中使用軟體限制原則

軟體限制原則可讓您在受限的環境中執行不受信任的程式碼，因此可能會造成有害的程式碼，使其無法誤用使用者的許可權。 這樣做的方法是將信任層級指派給使用者可以執行的檔案。 例如，某些系統檔案可以是完全受信任的，且不受限制地存取使用者的許可權，而從網際網路下載的檔案可能完全不受信任，因此只允許在受限制的環境中執行，而不允許使用任何安全性敏感的使用者權限。

全系統軟體限制原則是透過「本機安全性原則」系統管理工具來控制，讓系統管理員可以設定個別檔案的信任層級。 但是，所有 COM + 伺服器應用程式都是在 dllhost.exe 檔案中執行。 因此，COM + 會提供一種方法來指定每個伺服器應用程式的軟體限制原則，讓它們不需要相依于 dllhost.exe 檔案的限制原則。 如需有關如何在 COM + 中使用軟體限制原則的討論，請參閱 [在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)。

## <a name="library-application-security"></a>程式庫應用程式安全性

程式庫應用程式具有特殊的安全性考慮。 因為這些應用程式是在用戶端的進程中執行，所以會受到裝載進程強制執行的安全性影響，同時無法控制進程層級安全性。 如需針對程式庫應用程式考慮因素的說明，請參閱連結 [庫應用程式安全性](library-application-security.md)。

## <a name="multi-tier-application-security"></a>多層式應用程式安全性

COM + 應用程式通常是中介層應用程式;也就是說，它們會在用戶端與後端資源（例如資料庫）之間移動資訊。 難以決定應如何強制執行安全性以及什麼程度。 安全性本質上牽涉到效能取捨。 當您必須在資料層和仲介層強制執行安全性檢查時，其中一些最嚴重的情況會發生。 如需考慮問題的討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[用戶端模擬和委派](client-impersonation-and-delegation.md)
</dt> <dt>

[COM + 安全性工作](com--security-tasks.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




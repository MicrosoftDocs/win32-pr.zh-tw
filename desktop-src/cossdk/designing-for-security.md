---
description: 安全性設計
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: 安全性設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977006"
---
# <a name="designing-for-security"></a>安全性設計

您的安全性的端對端策略顯然取決於您所開發的分散式應用程式類型。 以下是針對仲介層應用程式邏輯定址安全性的幾個建議：

-   為了提高效率和效能，請盡可能接近使用者進行驗證。 如果您的應用程式牽涉到瀏覽器對企業邏輯到資料庫的架構，請考慮將瀏覽器用戶端對應到網域身分識別、在每個應用程式專屬的身分識別下執行 COM + 應用程式，以及將資料層中的資料表設定為只能由特定的應用程式識別碼存取。 此信任的伺服器案例比使用 DBMS 進行驗證更具擴充性和較低的問題。
-   如果您要設計的元件會使用以角色為基礎的安全性在分散式應用程式中使用，您可以使用 [Com + 安全性](com--security.md) 功能。 這項功能可讓您呼叫方法（例如 [**IObjectCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) 和 [**IObjectCoNtext：： IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) ），以協助保護程式碼區塊免于遭到未經授權的存取。 您也可以使用安全性呼叫內容來取得物件呼叫端的相關資訊。
-   如果您要設計的元件將在分散式應用程式中使用，而不使用以角色為基礎的安全性，則只會在進程層級自動檢查安全性。 流程存取權限會決定誰會獲得應用程式的存取權。 如果您需要更細微的控制安全性設定，或是在介面層級，請使用 COM 提供的程式設計安全性功能。
-   如果在未整合至 COM + 應用程式的情況下執行使用 COM + 程式設計安全性的元件，則會擲回例外狀況。 因此，如果您想要將這類元件成功整合至不屬於 COM + 環境的應用程式，您必須適當地處理所有例外狀況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[可用性設計](designing-for-availability.md)
</dt> <dt>

[設計部署](designing-for-deployment.md)
</dt> <dt>

[擴充性設計](designing-for-scalability.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> </dl>

 

 




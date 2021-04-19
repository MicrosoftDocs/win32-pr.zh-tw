---
description: 本主題提供幾個構成區塊的案例，其中說明決定要如何強制執行安全性的準則。
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: 在多層式應用程式中保護資料的基本案例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972563"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>在多層式應用程式中保護資料的基本案例

本主題提供幾個構成區塊的案例， [其中說明決定要如何強制執行安全性](deciding-where-to-enforce-security.md)的準則。

## <a name="trusted-server-scenario"></a>信任的伺服器案例

-   資料庫會完全信任 COM + 應用程式，以驗證和授權終端使用者存取資料庫中的資料。
-   最好的情況是，資料庫會受到保護，除非透過應用程式存取。
-   COM + 應用程式會使用以角色為基礎的安全性來授權使用者。
-   連接會以 COM + 應用程式的身分識別來開啟，並完全共用。
-   您可以透過 COM + 應用程式來完成審核和記錄，也可以由應用程式將這項資訊傳遞到資料庫中。

此案例最適用于可透過可預測的使用者類別（可在角色中封裝）存取的資料。 例如，只有「管理員」、「Tellers」和「會計」具有存取帳戶的許可權。 在中介層強制執行每個精確的商務邏輯。

## <a name="impersonation-scenario"></a>模擬案例

-   資料庫會自行驗證及授權使用者，以協助限制資料庫中資料的存取權。
-   COM + 應用程式會在每次存取資料庫時模擬用戶端。
-   連接是以每次呼叫為基礎進行，無法重複使用。

此案例最適用于緊密系結至極小使用者類別的資料。 例如，每個員工只能存取自己的人員檔案，而且每個經理只能存取其報表的人員檔案。

## <a name="hybrid-scenario"></a> 混合式案例

上述兩個案例的組合，其中只會在需要時使用模擬。

在您有混合式使用者資料關聯性的情況下，此案例的效果最佳。 例如，您有「經理」、「Tellers」、「會計」和數千個個別的 Web 用戶端，他們只可以存取自己的帳戶。 您可以透過應用程式來分隔邏輯路徑（可能使用個別的元件）來處理後者的使用者類別，特別是在這些使用者的效能假設不同的情況下。

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>使用 Microsoft SQL Server 角色的信任案例

-   Microsoft SQL Server 7.0 和更新版本可以使用角色來授與特定資料列的存取權，但信任 COM + 應用程式來驗證和授權使用者，以及將它們對應到資料庫中的正確角色。
-   COM + 應用程式會使用以角色為基礎的安全性來授與使用者，而且應用程式角色也適合資料庫角色。
-   您可以開啟特定資料庫角色的特定連接。 如果在 COM + 應用程式中的集區物件持有這些連線，就可以重複使用這些連接。 如需如何進行此作業的詳細資訊，請參閱 [Com + 物件](com--object-pooling.md)共用。
-   您可以透過 COM + 應用程式來完成審核和記錄，也可以由應用程式將這項資訊傳遞給資料庫。

此案例最適合一般與第一個受信任的伺服器案例中相同類型的使用者和資料，因為 COM + 應用程式仍然會受到信任，以正確地處理授權。 不過，它可協助保護資料庫免于遭受未經授權的存取，同時允許來自 COM + 應用程式外部多個來源的存取，而不會導致模擬案例的調整和效能受到影響。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[決定要在哪裡強制執行安全性](deciding-where-to-enforce-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> </dl>

 

 




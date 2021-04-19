---
description: 說明 LSA 驗證模型。
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: LSA 驗證模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f5a44a20284a7285eb7fcffe1d1f8f6bf1f286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975823"
---
# <a name="lsa-authentication-model"></a>LSA 驗證模型

[*本地安全機構*](../secgloss/l-gly.md) (LSA) 驗證模型具有下列功能：

-   LSA 驗證支援自訂 [驗證套件](authentication-packages.md)。 這可讓 (Isv 的終端客戶和獨立軟體廠商) 自訂或取代驗證常式，以符合標準 Microsoft 驗證套件所提供的需求。 雖然 Microsoft 提供的驗證套件需要使用者名稱和密碼登入資料，但是自訂驗證套件可採用其他形式的登入資料，例如 ATM 卡資訊和個人識別碼 (PIN) 。 自訂驗證套件也可以用來執行新的 [*安全性通訊協定*](../secgloss/s-gly.md)。
-   LSA 支援自訂安全性封裝，可做為分散式應用程式的安全性支援提供者，以及做為需要驗證服務的應用程式之驗證套件。 驗證功能可使用與獨立驗證封裝相同的介面來存取，而安全性支援提供者功能則是使用 [安全性支援提供者介面](sspi.md) (SSPI) 來存取。 自訂安全性套件可用的 LSA 支援函式集合，可讓他們提供最先進的安全性功能，例如權杖建立和 [*補充認證*](../secgloss/s-gly.md) 管理。
-   LSA 支援與非 Microsoft 產品（例如網路和資料庫）互動的異類認證管理。 因為這類產品通常會有自己的安全性認證，所以 LSA 提供的函式可讓驗證套件用來將非 Microsoft 認證與 Windows 進程產生關聯。 自訂驗證套件可以在需要時提供查詢這些認證的服務，例如當網路重新導向程式嘗試建立與遠端系統的連接時。
-   系統上安裝的每個登入裝置類別都可以有自己的登入程式。 裝置類別通常包含像是智慧卡讀卡機的裝置;不過，為了方便進行 [*LSA*](../secgloss/l-gly.md) 驗證，已連線的網路也會被視為裝置。 根據預設，Windows 作業系統提供的登入程式可支援使用鍵盤的使用者名稱和密碼登入。 開發人員可以新增其他裝置的支援，例如 [*智慧卡*](../secgloss/s-gly.md)[*讀卡機*](../secgloss/r-gly.md)。 如需智慧卡的詳細資訊，請參閱 [智慧卡驗證](smart-card-authentication.md)。 如需有關登入裝置支援的詳細資訊，請參閱 [Winlogon 和 GINA](winlogon-and-gina.md)。

 

 

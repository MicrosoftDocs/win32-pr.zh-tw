---
description: 當 SSP/AP 安全性封裝作為驗證套件運作時，它會載入到本地安全機構 (LSA) 的進程空間中，並被視為在 LSA 模式中。
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: LSA 模式與使用者模式的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa965cd66f43548243c1e62329e6d9d337a2a0123344a8cb9f10915846a765f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922077"
---
# <a name="lsa-mode-vs-user-mode"></a>LSA 模式與使用者模式的比較

當 SSP/AP [*安全性封裝*](../secgloss/s-gly.md) 作為 [*驗證套件*](../secgloss/a-gly.md)運作時，它會載入到 [*本地安全機構*](../secgloss/l-gly.md) (lsa) 的進程空間中，並被視為在 lsa 模式中。 使用 [LSA 登入功能](authentication-functions.md)的登入應用程式存取驗證套件功能。 開發人員可以使用 LSA 支援函式，僅適用于 LSA 模式安全性封裝，以執行比先前支援更複雜的驗證套件。

當 [*安全性封裝*](../secgloss/s-gly.md) 提供安全性服務給用戶端/伺服器應用程式時，它會載入至用戶端和伺服器進程，而且會被視為使用者模式。 用戶端/伺服器應用程式會使用 Microsoft [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 來存取安全性套件的安全性支援服務。

SSP/Ap 的 LSA 支援包含可讓安全性封裝的 LSA 模式和使用者模式實例用來進行通訊的功能。 此外，安全性封裝的使用者模式實例可以將所選要求的資訊委派給該封裝的 LSA 模式實例。

如需有關如何針對每個模式初始化安全性封裝的詳細資訊，請參閱 [LSA 模式初始化](lsa-mode-initialization.md) 和 [使用者模式初始化](user-mode-initialization.md)。

 

 

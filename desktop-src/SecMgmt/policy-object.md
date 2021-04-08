---
description: 原則物件是用來控制對本地安全機構 (LSA) 資料庫的存取，並且包含適用于整個系統或為系統建立預設值的資訊。
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: 原則物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847883"
---
# <a name="policy-object"></a>原則物件

**原則** 物件是用來控制對 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) (LSA) 資料庫的存取，並且包含適用于整個系統或為系統建立預設值的資訊。 每個系統只有一個 **原則** 物件。 當系統啟動時，LSA 會建立這個 **原則** 物件，而且應用程式無法建立或終結它。

**原則** 物件中儲存的資訊包括：

-   系統預設記憶體配額。 除非另有指定，否則登入系統的每個使用者都會被指派此記憶體配額。 您可以透過 [**Account**](account-object.md) 物件，將特殊的記憶體配額指派給個人或群組或本機群組的成員。
-   全系統安全性審核需求。
-   這個系統帳戶網域的名稱和 SID。
-   此系統主域的相關資訊。 這項資訊包括主域的名稱和 SID、要用於驗證要求的主要網域內的帳戶名稱、名稱和 SID 轉譯，以及取得網域內網域控制站的名稱。 這些名稱可能已過期，且應只做為提示。 這份清單的順序是很重要的，而且會維持不變。 例如，這可讓清單中的第一個名稱代表最後已知的主域控制站。
-   LSA 是否持有原則資訊或複本的主要複本的相關資訊。 只會複寫部分原則資訊;其餘部分則是以每個系統為基礎建立。

**原則** 物件的 **AccountDomain** 和 **PrimaryDomain** 欄位會基於不同的用途而使用，視系統和信任關係的類型而定：

-   在沒有主域的系統上，[ **AccountDomain** ] 欄位包含系統本機帳戶網域的名稱和 SID，與電腦名稱稱相同。 **PrimaryDomain** 欄位包含這部電腦所屬工作組的名稱。 [**TrustedDomain**](trusteddomain-object.md) 物件會被忽略，但有一個例外狀況，不能有與工作組同名的 **TrustedDomain** 物件，因為它會顯示為電腦的主要網域。
-   在具有主域的系統上， **AccountDomain** 欄位會識別本機帳戶網域的名稱和 SID （如同之前一樣）。 不過， **PrimaryDomain** 欄位包含系統主域的名稱和 SID。 此外，您應該會有一個 [**TrustedDomain**](trusteddomain-object.md) 物件，其中包含 **PrimaryDomain** 欄位中所識別的名稱和 SID。 這個 **TrustedDomain** 物件包含為網域主控站建立安全通道所需的帳戶和伺服器資訊。 系統會忽略任何其他 **TrustedDomain** 物件。
-   在網域控制站上，[ **AccountDomain** ] 欄位會識別系統的本機帳戶網域。不過，系統會將帳戶名稱指派給使用者，而不是已知的名稱。 因為主要網域與帳戶網域相同，所以 **PrimaryDomain** 欄位必須包含與 **AccountDomain** 欄位相同的值。 此外，所有的 [**TrustedDomain**](trusteddomain-object.md) 物件都必須有效，且代表與其他網域的信任關係。 如果系統不信任任何其他網域，則應該不會有任何 **TrustedDomain** 物件。

 

 

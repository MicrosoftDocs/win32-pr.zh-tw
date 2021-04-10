---
description: 列出並說明 GINA 的責任。
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: GINA 的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026708"
---
# <a name="responsibilities-of-the-gina"></a>GINA 的責任

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 

[*GINA*](../secgloss/g-gly.md) DLL 具有下列責任：

-   SAS 監視

    GINA 負責辨識 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) 、監視 sas 事件，以及在發生 sas 時通知 Winlogon。 請注意，您可以定義一個以上的 SAS，而定義的 SASs 集合可能會隨著時間而變更。 例如，當 [*Winlogon*](../secgloss/w-gly.md) 處於已登入的狀態時，可能會有一組 SASs，另一組則處於登入狀態。

    Winlogon 提供使用 CTRL + ALT + DEL SAS 來協助 GINA 的服務。

-   SAS 處理

    讓 GINA 可取代的原因之一，就是提供替代的識別和驗證機制。 若要這樣做，GINA 必須顯示所有由 SAS 辨識所產生的使用者介面。 當使用者未登入時，GINA 會負責呈現身分識別和驗證選項，以及任何其他未經過驗證的允許選項。 當使用者登入時，GINA 會負責向使用者呈現相關的選項，以及採取適當的動作。 例如，在包含 [*智慧卡*](../secgloss/s-gly.md)的系統中，如果使用者移除智慧卡，可能會自動鎖定工作站。

-   Shell 啟用

    當使用者登入時，GINA 會負責為該使用者建立一或多個初始進程。  (在本檔中，假設這些初始進程會向使用者呈現介面。 不過，處理常式實際上可以是任何程式，且不一定需要與使用者互動。 ) 這些進程稱為 *使用者 shell* 或只是 *shell*。 在 shell 啟用的過程中，GINA 必須將新登入的使用者權杖指派給處理常式。 Winlogon 提供可協助 GINA 指派權杖的服務。

 

 

---
description: 當執行緒嘗試存取安全物件時，系統會授與或拒絕存取權。
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: AccessCheck 的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566335"
---
# <a name="how-accesscheck-works"></a>AccessCheck 的運作方式

當執行緒嘗試存取安全物件時，系統會授與或拒絕存取權。 如果物件沒有 [*任意的存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，系統會授與存取權;否則，系統會在應用於執行緒的物件 DACL 中尋找 (Ace) 的 [存取控制專案](access-control-entries.md) 。 物件 DACL 中的每個 ACE 都會指定允許或拒絕 [信任者](trustees.md)的存取權限，這可以是使用者帳戶、群組帳戶或 [*登入會話*](/windows/desktop/SecGloss/l-gly)。

## <a name="dacls"></a>DACL

系統會將每個 ACE 中的信任者與線上程 [存取權杖](access-tokens.md)中識別的受信任者進行比較。 存取權杖包含 (Sid) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) ，可識別使用者以及使用者所屬的群組帳戶。 權杖也包含識別目前登入會話的 [*登入 SID*](/windows/desktop/SecGloss/l-gly) 。 在存取檢查期間，系統會忽略未啟用的群組 Sid。 如需啟用、停用和僅限拒絕 Sid 的詳細資訊，請參閱 [存取權杖中的 Sid 屬性](sid-attributes-in-an-access-token.md)。

一般而言，系統會使用要求存取之執行緒的 [*主要存取權杖*](/windows/desktop/SecGloss/p-gly) 。 但是，如果執行緒正在模擬另一個使用者，系統就會使用執行緒的模擬 [*token*](/windows/desktop/SecGloss/i-gly)。

系統會依序檢查每個 ACE，直到發生下列其中一個事件為止：

-   拒絕存取時的 ACE 會明確拒絕對執行緒存取權杖中所列其中一個受攻擊者所要求的任何 [存取權限](access-rights-and-access-masks.md) 。
-   執行緒存取權杖中所列的一個或多個存取允許 Ace 明確授與所有要求的存取權限。
-   所有 Ace 都已核取，而且至少有一個要求的存取權限未明確允許，在這種情況下，會隱含拒絕存取。

下圖顯示物件的 DACL 如何允許存取某個執行緒，同時拒絕另一個執行緒的存取。

![將不同存取權限授與不同執行緒的 dacl](images/accctrl1.png)

針對執行緒 A，系統會讀取 ACE 1，並立即拒絕存取，因為存取拒絕的 ACE 會套用至使用者線上程的存取權杖中。 在此情況下，系統不會檢查 Ace 2 和3。 針對執行緒 B，ACE 1 不適用，因此系統會繼續進行 ACE 2，以允許寫入權限，以及允許讀取和執行存取的 ACE 3。

由於系統在明確授與或拒絕要求的存取權時，系統會停止檢查 Ace，因此 DACL 中的 Ace 順序很重要。 請注意，如果此範例中的 ACE 順序不同，則系統可能已授與執行緒 A 的存取權。若為系統物件，作業系統會 [在 DACL 中定義慣用的 ace 順序](order-of-aces-in-a-dacl.md)。

 

 

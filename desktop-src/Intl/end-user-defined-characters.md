---
description: 使用者自訂字元 (在雙位元組字元集中的 EUDC)  (Dbcs) 和私用區域 (PUA) Unicode 字元是自訂字元。
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: 終端使用者定義和私用區域字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320232"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>終端使用者定義和私用區域字元

使用者自訂字元 (在 [雙位元組字元集](double-byte-character-sets.md) 中的 EUDC)  (dbcs) 和私用區域 (PUA) [Unicode](unicode.md) 字元是自訂字元。 您可以由使用者或其他合作物件（例如設備製造商、使用者群組、政府機構或字型設計公司）來定義和執行這些用戶端。 其用途可讓使用者使用標準螢幕和印表機字型中未提供的字元來形成名稱和其他文字。

您可以在不同的電腦上，以不同的方式指派 EUDC 和 PUA 字元。 某些字碼頁有可重複使用 EUDC 範圍的延伸模組，而這些延伸模組可能會彼此衝突。 在其他情況下，製造商可能會在其中一個範圍內提供一組自訂字元。 此外，使用者群組也可以嘗試在 PUA 中提供額外的字元。 這些案例的不同組合可能會造成衝突。 建立依賴 EUDC 或 PUA 字元的應用程式時，您應該記住個別程式碼點的衝突解釋。

下列主題討論支援 EUDCs 的字型，以及這些字元的存取和管理：

-   [字元集和字型](character-sets-and-fonts.md)
-   [EUDC 登錄專案](eudc-registry-entries.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Unicode 和字元集](about-unicode-and-character-sets.md)
</dt> </dl>

 

 




---
title: 停用現有的類別和屬性
description: 新增架構是永久性的。
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671343"
---
# <a name="disabling-existing-classes-and-attributes"></a>停用現有的類別和屬性

新增架構是永久性的。 您無法刪除 **attributeSchema** 和 **classSchema** 物件。 在分散式系統中，很難保證指定類別或屬性沒有任何實例。 移除類別或屬性的定義會損害該類別或屬性的現有實例。

您可以藉由將現有的類別或屬性標示為「無用」來停用它。 這並不會影響類別或屬性的現有實例來標記，但會防止建立新的實例。

停用架構類別和屬性時，適用下列限制：

-   您無法停用類別目錄1類別或屬性。
-   您無法停用不是也停用之類別成員的屬性。 這是因為 (未停用) 類別的屬性可能是必要的，而停用屬性則會防止建立類別的新實例。

若要停用屬性，請將其 **attributeSchema** 物件的 **isDefunct** 屬性設定為 **TRUE**。 當屬性停用時，就無法建立屬性的新實例。 若要重新啟用屬性，請將 **isDefunct** 屬性設定為 **FALSE**。

若要停用類別，請將其 **classSchema** 物件的 **isDefunct** 屬性設定為 **TRUE**。 當某個類別停用時，就無法建立類別的新實例。 若要重新啟用類別，請將 **isDefunct** 屬性設定為 **FALSE**。

將架構物件設定為無用，在實際執行環境中會很有用。 當不再需要架構延伸模組的測試版本時，請將它標示為無用。 您可以藉由移除 **isDefunct** 屬性或將屬性值設定為 **FALSE** 來還原。 這也可防止非預期的架構物件移除，因為它會將它設定為「無用」，因為可以輕鬆地反向操作。

請注意，當您讓架構物件無用時，Active Directory 伺服器不會清除屬性或類別的現有實例。 如果您移除 **isDefunct** 屬性，任何實例會再次變成有效的一般物件。

下列清單包含其他將 **attributeSchema** 或 **classSchema** 物件標示為無用的後果：

-   新增或修改實例失敗。
-   錯誤碼的行為就像是無用的類別永遠不存在一樣。
-   搜尋和刪除的行為就像尚未讓任何架構物件成為無用一樣。
-   只允許從物件刪除整個屬性。

下列清單包含生產環境中的其他選項，以減少無用架構延伸的影響：

-   從無用的類別中移除所有 **mayHave** 屬性值。
-   從無用的類別中，減少所有 **mustHave** 屬性值的大小。
-   從通用類別目錄中移除無用的屬性。
-   從任何索引中移除無用的屬性。

在實際執行環境中移除不必要架構變更的其他選項，是讓開發人員使用私用網域控制站進行測試。 在此情況下，您可以：

-   使用 Dcpromo.exe 將 DC 降級，以「重設」 Active Directory 的伺服器。 降級完成之後，請再次使用 Dcpromo.exe 將伺服器升級回 DC。 然後，開發人員可以使用 LDIF 腳本來重載任何必要的類別、屬性和物件實例。
-   使用 Ntbackup.exe 對可用的磁碟分割執行系統狀態備份。 重新開機至安全/目錄服務還原模式以進行還原。

若為 Windows Server 2003 作業系統，當您將類別或屬性設定為 [無用] 時，當您建立新的類別或屬性來取代它時，可以立即重複使用無用架構專案的 **ldapDisplayName**、 **schemaIdGuid**、 **OID** 和 **mapiID** 值。 類別或屬性的無用版本會保留在架構容器中，但會在 MMC 嵌入式管理單元中隱藏。 若要重新啟用舊的 schema 元素，請將 **isDefunct** 設定為 **FALSE**。

下列 LDIF 程式碼範例顯示如何修改 **isDefunct** 屬性並變更 RDN，使其不會與您建立用來取代它的新類別混淆。

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

使用下列命令，針對在 Windows Server 2003 作業系統上執行的電腦，對樹系執行 LDIF 程式碼範例。

**ldifde/i/f rdn .ldf。 .ldf/c "DC = X" "dc = mydomain，DC = com"**

 (，其中 "DC = X" 是常數) 

 

 





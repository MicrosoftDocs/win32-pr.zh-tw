---
title: 架構延伸的限制
description: 為了減少某個應用程式中斷其他應用程式的架構變更的可能性，以及維持架構一致性，Active Directory Domain Services 對允許應用程式或使用者進行的架構變更類型強制執行限制。
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671244"
---
# <a name="restrictions-on-schema-extension"></a>架構延伸的限制

為了減少某個應用程式中斷其他應用程式的架構變更的可能性，以及維持架構一致性，Active Directory Domain Services 對允許應用程式或使用者進行的架構變更類型強制執行限制。

只有在修改現有的架構物件時，才會加諸限制。 架構分為兩個類別。 基底架構中 Windows 2000 隨附的架構物件屬於類別1。 其他應用程式或使用者稍後透過動態架構延伸新增的任何架構物件都屬於類別2。 架構物件的類別可以由 **classSchema** 物件上 **systemFlags** 屬性中所設定的0x10 位來決定。 這個位只會在類別1物件上設定，且無法變更，也不能在任何類別2物件上設定。

**SystemFlags** 屬性是由 Active Directory Domain Services 在內部使用，以識別基底架構中「基礎結構」物件的特殊特性。 除了識別類別1物件之外， **systemFlags** 還會控制是否可以移動、刪除或重新命名物件。 Windows 2000 相依的物件無法執行這些作業。

在任何架構物件（類別1或2）上，Active Directory Domain Services 會強制執行下列限制：

-   您無法將新的 **mustContain** 加入至類別 (直接或透過繼承加入) 的輔助類別。
-   您無法直接或透過繼承) 來刪除類別 (的任何 **mustContain** 。

此外，還會在類別1架構物件上加上下列額外的限制：

-   您無法變更類別1屬性的下列屬性：

    -   **rangeLower** 和 **rangeUpper** (值範圍) 。
    -   如果有任何) ， **attributeSecurityGuid** (會決定屬性所屬的屬性集。

-   您無法變更類別1類別的 **defaultObjectCategory** 。
-   您無法變更類別1類別的任何實例的 **objectCategory** 。
-   您無法讓類別目錄1類別或屬性無用。
-   您無法變更類別1類別或屬性的 **lDAPDisplayName** 。
-   您無法重新命名類別1類別或屬性。

 

 





---
title: 關於 Active Directory Domain Services 的使用者介面
description: 系統管理員和使用者必須能夠從使用者介面查看和修改 Microsoft Active Directory Domain Services 中的目錄服務物件。
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c451a44660aaadbf0021ff57e675736b797d8f3e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023207"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>關於 Active Directory Domain Services 的使用者介面

系統管理員和使用者必須能夠從使用者介面查看和修改 Microsoft Active Directory Domain Services 中的目錄服務物件。 系統管理員會使用不同的 Microsoft Management Console (MMC) 嵌入式管理單元來管理 Active Directory 伺服器，具體來說，Active Directory Domain Services 的使用者和電腦、Active Directory Domain Services 的網站和服務、Active Directory Domain Services 的網域和信任，以及 Active Directory Domain Services 的架構管理員嵌入式管理單元。如果授與適當許可權，使用者也可以使用 Active Directory MMC 嵌入式管理單元來查看目錄物件。 Windows shell 也可以用來查看目錄物件。 Windows shell 可讓使用者從 [我的網路位置] 中的目錄專案，或透過 [開始] 功能表中提供的 [搜尋] 對話方塊，流覽儲存在目錄中的物件。

Active Directory Domain Services 支援可適應的使用者介面，以符合系統管理員和終端使用者的需求。 Active Directory Domain Services 可讓您擴充代表現有物件類別的使用者介面，以及新增至架構的新類別。 下列元素可以用來控制或擴充架構中所定義之每個類別的 UI：

-   [搭配顯示規範使用的屬性頁](property-pages-for-use-with-display-specifiers.md)
-   [用於顯示規範的內容功能表](context-menus-for-use-with-display-specifiers.md)
-   [類別和屬性顯示名稱](class-and-attribute-display-names.md)
-   [物件建立的嚮導](object-creation-wizards.md)
-   [類別圖示](class-icons.md)
-   [以分葉節點形式來查看容器](viewing-containers-as-leaf-nodes.md)

從 Windows 2000 開始，系統會提供 COM 物件，以執行使用目錄物件的通用對話方塊。 這些對話方塊會提供通用 UI，而不需要重新產生這些對話方塊。

-   [目錄物件選擇器](directory-object-picker.md)
-   [網域瀏覽器](domain-browser.md)
-   [容器瀏覽器](container-browser.md)

您可以使用 MMC 延伸嵌入式管理單元擴充 Active Directory 的系統管理嵌入式管理單元、內容功能表和屬性頁。其他 MMC 延伸模組（例如，任務板、命名空間專案、控制列和工具列）也可以執行。 如需詳細資訊，請參閱 [擴充 Active Directory 系統管理嵌入式管理單元](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins)。

 

 
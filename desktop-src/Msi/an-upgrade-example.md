---
description: 下列各節會針對安裝範例中所述的應用程式撰寫升級套件的範例。
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: 升級範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a148c8d66c09ae2ce033d3ad2440040734a2b1301b2e9e1b9bb1b79e44beb06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066348"
---
# <a name="an-upgrade-example"></a>升級範例

下列各節會針對 [安裝範例](an-installation-example.md)中所述的應用程式撰寫升級套件的範例。 此範例的最基本使用者介面範例，會在[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供，做為檔 Uisample.msi。 如果您有 SDK，就可以存取重現範例安裝套件、使用者介面和範例升級套件所需的所有工具和資料。

此範例說明如何建立 Windows Installer 套件，以將假想產品 MNP2000 升級為稱為 MNP2001 的新產品。 範例升級套件會將主要升級套用至需要變更產品代碼的產品。 如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)一節中的[重大升級](major-upgrades.md)主題。

範例升級套件具有下列規格：

-   若要符合接收此升級至 MNP2001 的資格，使用者必須先前已使用 Windows Installer，將1.0 到 1.4 (內含) 版本的英文語言。
-   當使用者嘗試安裝升級套件時，Windows Installer 的升級功能會在使用者電腦上搜尋任何符合升級資格的產品。
-   Windows安裝程式會將所有原始產品的功能設定遷移到升級的產品。
-   安裝程式會從使用者的電腦移除所有已淘汰的功能。
-   安裝程式會安裝屬於升級的所有新功能。
-   卸載升級套件會將產品從使用者的電腦中移除，而不會還原舊版產品。
-   範例升級會更新新檔案和功能的快捷方式。

    [規劃主要升級](planning-a-major-upgrade.md)

    [匯入原始安裝資料庫](importing-original-installation-database.md)

    [更新升級的目錄結構](updating-directory-structure-for-an-upgrade.md)

    [更新升級的檔案和檔案屬性](updating-files-and-file-attributes-for-an-upgrade.md)

    [更新升級的元件](updating-components-for-an-upgrade.md)

    [更新升級的功能](updating-features-for-an-upgrade.md)

    [更新升級的快捷方式](updating-shortcuts-for-an-upgrade.md)

    [更新升級的升級資料表](updating-upgrade-table-for-an-upgrade.md)

    [更新升級的屬性](updating-properties-for-an-upgrade.md)

    [更新升級的順序資料表](updating-sequence-tables-for-an-upgrade.md)

    [更新升級的摘要資訊](updating-summary-information-for-an-upgrade.md)

    [驗證安裝升級](validating-an-installation-upgrade.md)

 

 




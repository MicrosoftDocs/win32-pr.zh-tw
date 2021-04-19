---
description: 本檔是 Windows Installer 的參考資料的主要來源。
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Windows Installer 檔的藍圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324d626eb5dd201a47c16613c5de598fcd13052d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969261"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Windows Installer 檔的藍圖

本檔是 Windows Installer 的參考資料的主要來源。 它會提供安裝套件和安裝程式服務的相關資訊。 它也會提供應用程式開發介面的完整描述 (API) 和安裝程式資料庫的元素。 本檔也包含 [Windows Installer 範例](windows-installer-examples.md)中安裝和更新套件的基本範例討論。

[Windows Installer 檔的以角色為基礎的指南](role-based-guide-to-windows-installer-documentation.md)是一種提供者指南的替代方案，可讓讀者更容易看到依專業角色和一般工作案例所組織的主題連結。

如需 Windows Installer 新聞群組的詳細資訊，請參閱主題： [Windows Installer 資訊的其他來源](other-sources-of-windows-installer-information.md)。

如需使用 Windows Installer 的秘訣清單，請參閱 [Windows Installer 最佳做法](windows-installer-best-practices.md)。

下列清單說明安裝程式檔的每一節。

-   [關於 Windows Installer](about-windows-installer.md) 提供安裝程式功能和優點的總覽，例如廣告、隨選安裝、復原、自訂及元件管理。 本節介紹安裝程式元件和功能的概念，這些概念對於瞭解安裝程式如何組織安裝而言是不可或缺的。 它也會討論有關安裝的數個高階主題，例如系統原則、檔案版本控制規則和復原安裝。
-   [使用 Windows Installer](using-windows-installer.md) 討論各種主題，例如將應用程式組織成元件的標準方法，安裝程式可從使用者的電腦安裝或移除這些元件;如何從 World Wide Web 下載安裝套件;以及使用壓縮的來源映射。
-   Windows Installer 區段的 [新](what-s-new-in-windows-installer.md) 功能中的資訊可以用來識別舊版 Windows Installer 不支援的新功能。
-   [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md) 描述如何搭配套件、轉換、修補程式、合併模組和外部封包檔來使用數位簽章。
-   [元件](assemblies.md) 說明如何使用 Windows Installer 來安裝和管理 common language run Time 和 Win32 元件。
-   [消費者介面](user-interface.md) 提供安裝程式使用者介面功能的相關資訊。 雖然安裝程式不提供使用者介面，但封裝作者可以保留在安裝資料庫中執行完全互動式內部或外部使用者介面所需的所有資料和邏輯。 參考區段描述資料庫資料表中 specifiable 的使用者介面元素，包括對話方塊、控制項和控制項事件。
-   [標準動作](standard-actions.md) 討論順序表中的安裝程式用來執行安裝的標準動作。 這項資訊主要適用于封裝開發人員。
-   [自訂動作](custom-actions.md) 說明如何在安裝程式中建立額外的功能。 自訂動作可讓安裝套件的作者藉由包含可執行檔、動態連結程式庫和腳本，來擴充標準動作的功能。 這項資訊適用于需要執行安裝程式的套件開發人員，而不在安裝程式中的其他位置。
-   [屬性](properties.md) 提供安裝期間安裝程式所使用之屬性的相關資訊。 [關於] 和 [使用] 區段提供這些全域變數的總覽，而且每個屬性都會在 [參考] 區段中描述。
-   [摘要資訊串流](summary-information-stream.md) 記錄安裝程式所使用的摘要資訊屬性。 這項資訊是所有開發人員的相關資訊。
-   [修補與升級](patching-and-upgrades.md) 會討論如何使用安裝程式來執行檔案更新、qfe、次要更新、產品升級和修補。
-   [轉換](transforms.md) 說明如何使用資料庫轉換來改變或自訂安裝資料庫，以及如何產生、保護和套用轉換。
-   [套件驗證](package-validation.md) 會討論使用內部一致性評估工具 (的) ，測試開發中安裝套件的內部一致性。
-   [合併模組](merge-modules.md) 提供合併模組設計的標準。 這項標準應該遵循建立自己的合併模組的開發人員，以及計畫使用安裝程式將共用程式碼傳遞至其應用程式的開發人員。
-   [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md) 會討論如何使用 Windows Installer 來安裝和管理專為在64位作業系統上執行而設計的安裝程式元件。
-   [Windows Installer 範例](windows-installer-examples.md) 包含在 [安裝範例](an-installation-example.md)中使用內部使用者介面建立安裝套件的逐步範例。 如需撰寫現有套件之主要升級的範例，請參閱 [升級範例](an-upgrade-example.md)。 若要瞭解自訂轉換如何停用功能並新增新的資源，請參閱 [自訂轉換範例](a-customization-transform-example.md)。 如需建立修補程式套件以將小型更新套用至現有安裝套件的範例，請參閱 [小型更新修補範例](a-small-update-patching-example.md)。 若要瞭解如何當地語系化現有的安裝程式套件，請參閱 [當地語系化範例](a-localization-example.md)。
-   [Automation 介面](automation-interface.md) 為想要使用 Windows Installer 自動化介面的開發人員提供資訊。
-   [安裝程式](installer-functions.md) 函式描述對安裝程式 API 的函式呼叫。 這些是其他應用程式呼叫以存取安裝程式服務，以安裝、維護或移除應用程式的功能。 使用章節包括有關如何要求功能、起始安裝，以及以程式設計方式重新安裝遺漏元件的討論。 參考區段是安裝程式服務功能的主要參考資料。
-   安裝[程式資料庫](installer-database.md)會討論安裝資料庫。 安裝程式會將安裝所需的所有邏輯和資料保留在位於 .msi 檔案中的關係資料庫。 [關於] 區段提供資料庫之主要功能群組的架構圖表總覽。 使用章節討論使用這些資料表中最重要的部分。 這些章節包含撰寫安裝套件或撰寫套件建立工具之開發人員不可或缺的資訊。 參考區段包含每個資料庫資料表的完整參考資料。 本節也包含每個資料庫函數的主要參考。 資料庫函式是由安裝程式在內部用來存取資料庫，而且主要是安裝程式套件建立工具的開發人員感興趣。

 

 




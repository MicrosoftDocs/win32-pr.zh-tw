---
description: 此範例說明如何建立可安裝應用程式的簡單 Windows Installer 套件。
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: 安裝範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848978"
---
# <a name="an-installation-example"></a>安裝範例

此範例說明如何建立可安裝應用程式的簡單 Windows Installer 套件。 此範例會安裝「記事本」、Windows 隨附的文字編輯器，以及數個描述事件和招生的文字檔（在紅色公園的假想）。

此範例具有下列規格：

-   應用程式會以自行安裝的 Windows Installer 套件的形式提供給使用者，以安裝所有必要的檔案、快捷方式和登錄資訊。
-   安裝套件可能會在安裝期間對使用者顯示 UI wizard，以收集使用者資訊。
-   在安裝期間，使用者可以選擇要安裝的個別功能，以在本機執行、從來源執行，或不安裝。
-   您可以將其中一項功能提供給使用者，作為隨選安裝功能。
-   相同的套件會卸載應用程式，並從使用者的電腦移除所有應用程式檔和登錄資訊。
-   封裝已準備好接收包含變更其產品代碼的主要升級。

若要重現範例，您需要能夠建立和編輯空白 Windows Installer 資料庫的軟體工具。 獨立軟體廠商提供數種套件建立工具。 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供稱為 Orca 的 Windows Installer 資料庫編輯器。

若要完成此範例，請遵循下列步驟：

[規劃安裝](planning-the-installation.md)

[匯入空白資料庫](importing-a-blank-database.md)

[指定目錄結構](specifying-directory-structure.md)

[指定元件](specifying-components.md)

[指定檔案和檔案屬性](specifying-files-and-file-attributes.md)

[指定來源媒體](specifying-source-media.md)

[指定功能](specifying-features.md)

[指定 Feature-Component 關聯性](specifying-feature-component-relationships.md)

[新增登錄資訊](adding-registry-information.md)

[指定快速鍵](specifying-shortcuts.md)

[指定屬性](specifying-properties.md)

[匯入 InstallExecuteSequence](importing-the-installexecutesequence.md)

[匯入 InstallUISequence](importing-the-installuisequence.md)

[匯入 AdminExecuteSequence](importing-the-adminexecutesequence.md)

[匯入 AdminUISequence](importing-the-adminuisequence.md)

[匯入 AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[新增摘要資訊](adding-summary-information.md)

[匯入消費者介面](importing-the-user-interface.md)

[驗證安裝資料庫](validating-an-installation-database.md)

 

 




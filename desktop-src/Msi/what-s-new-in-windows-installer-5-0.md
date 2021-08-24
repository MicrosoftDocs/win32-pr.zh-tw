---
description: 本主題中的資訊會識別 Windows Installer&160; 5.0 中提供的新增和變更 \# 。
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: Windows Installer 5.0 的新功能
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: 82c6ae3bf5c6781ba84d18b366998c74deedd4ca0fa4c61ac452b1d0ec409850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145221"
---
# <a name="whats-new-in-windows-installer-50"></a>Windows Installer 5.0 的新功能

本主題中的資訊會識別 Windows Installer 5.0 中可用的新增和變更。

Windows安裝程式5.0 隨附于下列版本的 Windows：

* 用戶端： Windows 7 和所有更新版本。
* 伺服器： Windows server 2008 R2 和所有更新版本。

> [!NOTE]
> Windows Installer 5.0 沒有可轉散發套件。 如需舊版 Windows Installer 可用可轉散發套件的清單，請參閱[Windows Installer](windows-installer-redistributables.md)可轉散發套件。 如需 Windows Installer 版本的完整清單，請參閱[Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

本頁面是以檔的指南的形式提供。 您應參閱主要參考頁面上的需求一節，以判斷實際的作業系統需求。 從這個頁面未連結的部分 Windows Installer，可能會在另一個版本的 Windows Installer 中提供。 如需其他 Windows Installer 版本的詳細資訊，請參閱[Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

[標準動作](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[安裝程式函數](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[資料行資料類型](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[屬性](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[摘要資訊屬性](summary-information-stream-reference.md)

-   [**範本摘要**](template-summary.md)有新的值，指出資料庫與 Windows RT 或 Arm64 平臺相容。

[資料庫資料表](database-tables.md)

-   [MsiServiceConfig 資料表](msiserviceconfig-table.md)
-   [MsiServiceConfigFailureActions 資料表](msiserviceconfigfailureactions-table.md)
-   [MsiShortcutProperty 資料表](msishortcutproperty-table.md)
-   [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)

[事件](control-events.md)

-   [MsiPrint ControlEvent](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent](msilaunchapp-controlevent.md)

[控制項](controls.md)

-   [超連結控制項](hyperlink-control.md)

[內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Automation 介面](automation-interface.md)

-   [**安裝程式物件** 的屬性](installer-object.md)

    -   [**ClientsEx**](installer-clientsex.md)
    -   [**ComponentsEx**](installer-componentsex.md)
    -   [**ComponentPathEx**](installer-componentpathex.md)

-   [**元件物件** 的屬性](components.md)

    -   [**ComponentCode**](component-componentcode.md)
    -   [**UserSID**](component-usersid.md)
    -   [**元件。內容**](component-context.md)

-   [**用戶端物件** 的屬性](client.md)

    -   [**用戶端. ProductCode**](client-productcode.md)
    -   [**ComponentCode**](client-componentcode.md)
    -   [**UserSID**](client-usersid.md)
    -   [**用戶端。內容**](client-context.md)

-   [**ComponentInfo**](componentinfo.md)物件的屬性

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo 路徑**](componentinfo-path.md)
    -   [**ComponentInfo。州**](componentinfo-state.md)

## <a name="notes"></a>備註

安裝程式開發人員可以使用 Windows Installer 5.0 來撰寫單一安裝套件，以支援每一電腦安裝或應用程式的每個使用者安裝。 如需詳細資訊，請參閱 [單一封裝撰寫](single-package-authoring.md)。 內部一致性評估工具 [ICE105](ice-105.md) 會檢查封裝是否已撰寫成要安裝在每個使用者的內容中。 不具特權的標準使用者可以安裝、更新、執行和移除的應用程式，也稱為 Per-User 應用程式 (PUA。 ) PUA 可以提供較佳的使用者體驗、將系統和其他電腦使用者的影響降到最低，以及將 UAC 提示保留在實際需要提高使用者權限的情況下。 Windows Installer 5.0 的單一套件撰寫功能可協助開發 Per-User 的應用程式。

服務設定選項可讓 Windows Installer 套件自訂電腦上的[服務](../services/services.md)。 如需詳細資訊，請參閱 [使用服務](using-services-configuration.md)設定。

從 Windows Installer 5.0 開始，Windows Installer 套件能夠保護新的帳戶、Windows[服務](../services/services.md)、檔案、資料夾和登錄機碼。 [MsiLockPermissionsEx](msilockpermissionsex-table.md)資料表可以指定拒絕許可權的安全描述項、指定父資源的許可權繼承，或指定新帳戶的許可權。 如需詳細資訊，請參閱 [保護資源](securing-resources-.md)。

Windows安裝程式5.0 可以列舉電腦上安裝的所有元件，並取得元件的金鑰路徑。 如需詳細資訊，請參閱 [列舉元件](enumerating-components-.md)。

WindowsWindows Server 2012 或 Windows 8 上執行的安裝程式5.0 支援在 Windows RT 上安裝已核准的應用程式。 未由 Microsoft 簽署的 Windows Installer 套件、修補程式或轉換，無法安裝在 Windows RT 上。 [[**範本摘要**](template-summary.md)] 屬性會指出與安裝資料庫相容的平臺，而且應該包含 Windows RT 的值。

Windows在 Arm64 處理器上 Windows 10 上執行的安裝程式5.0 支援安裝專門針對 Arm64 平臺編譯的應用程式。  這些套件的 [ [**範本摘要**](template-summary.md) ] 屬性必須包含值 Arm64。 

 

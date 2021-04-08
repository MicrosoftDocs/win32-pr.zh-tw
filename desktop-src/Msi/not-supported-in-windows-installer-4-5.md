---
description: Windows Installer&\# 160、4.5 和較早的版本不支援此頁面上列出的 Windows Installer 函數、資料表和屬性。
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Windows Installer 4.5 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691787"
---
# <a name="not-supported-in-windows-installer-45"></a>Windows Installer 4.5 中不支援

Windows Installer 4.5 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。 這份清單缺少某項功能，並不保證支援此功能。 請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。 如需其他 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

Windows Installer 4.5 可作為 Windows Server 2008、Windows Vista （含 Service Pack 1） (SP1) 、Windows XP （含 Service Pack 2） (SP2) 和更新版本，以及 Windows Server 2003 （含 Service Pack 1 (SP1) 和更新版本）的可轉散發套件。 如需所有 Windows Installer 版本和可轉散發套件的完整清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

Windows Installer 4.5 及更舊版本中不支援下列功能。

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
-   WIC 影像檔案格式的[點陣圖控制項](bitmap-control.md)支援

[內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)

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
    -   [**Component**](component-context.md)

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

Windows Installer 4.5 不支援某些功能，可讓單一安裝套件安裝在每部電腦或每一使用者的安裝內容中。 如需詳細資訊，請參閱 [單一封裝撰寫](single-package-authoring.md)。

Windows Installer 4.5 不支援某些服務設定選項，這些選項可以讓封裝自訂電腦上的 [服務](../services/services.md) 。 如需詳細資訊，請參閱 [使用服務](using-services-configuration.md)設定。

Windows Installer 4.5 不支援某些功能，可讓 Windows Installer 保護新的帳戶、Windows [服務](../services/services.md)、檔案、資料夾和登錄機碼。 如需詳細資訊，請參閱 [保護資源](securing-resources-.md)。

Windows Installer 4.5 不支援某些功能，可讓安裝程式列舉電腦上所安裝的所有元件，並取得元件的金鑰路徑。 如需詳細資訊，請參閱 [列舉元件](enumerating-components-.md)。

 

 

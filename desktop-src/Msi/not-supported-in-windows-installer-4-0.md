---
description: Windows Installer&\# 160、4.0 和更早版本不支援此頁面上列出的 Windows Installer 函數、資料表和屬性。
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Windows Installer 4.0 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558798"
---
# <a name="not-supported-in-windows-installer-40"></a>Windows Installer 4.0 中不支援

Windows Installer 4.0 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。 這份清單缺少某項功能，並不保證支援此功能。 請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。 如需其他 Windows Installer 版本的詳細資訊，請參閱[Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

Windows安裝程式4.0 適用于 Microsoft Windows Server 2008 和 Windows Vista。 如需所有 Windows Installer 版本和可轉散發套件的完整清單，請參閱[Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

Windows Installer 4.0 及更舊版本中不支援下列功能。

[安裝程式函數](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[屬性](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[資料庫資料表](database-tables.md)

-   [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md)
-   [MsiEmbeddedUI 資料表](msiembeddedui-table.md)
-   [MsiPackageCertificate 資料表](msipackagecertificate-table.md)
-   [元件資料表](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) ExtendedType 資料行  
    

[自訂動作修補卸載選項](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[系統原則](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

回呼函數原型

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) 會確認任何元件都沒有 **msidbComponentAttributesPermanent** 和 **msidbComponentAttributesUninstallOnSupersedence** 屬性。

## <a name="notes"></a>備註

Windows安裝程式4.0 無法使用 [*交易處理*](t-gly.md)執行 [多個封裝安裝](multiple-package-installations.md)。

使用 Windows Installer 4.0 或舊版的安裝程式時，當使用 [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)原則或 [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)屬性時，小更新和次要升級可能會失敗，因為更新會移除元件。

自訂使用者介面無法使用[內嵌 UI](using-an-embedded-ui.md)中所述的方法，內嵌在 Windows Installer 套件內。

 

 




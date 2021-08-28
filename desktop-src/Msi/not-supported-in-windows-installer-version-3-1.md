---
description: 在此頁面上列出的 Windows Installer 函式、資料表和屬性，Windows Installer&160、 \# 3.1 和較早的版本不支援此功能。
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: Windows Installer 3.1 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33334133fafa5e37f8bd7dfe4edfd30962c4e605bf2a675661e9d57aca4184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145581"
---
# <a name="not-supported-in-windows-installer-31"></a>Windows Installer 3.1 中不支援

Windows Installer 3.1 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。 這份清單缺少某項功能，並不保證支援此功能。 請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。 如需其他 Windows Installer 版本的詳細資訊，請參閱[Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

Windows安裝程式3.1 適用于 Windows Server 2003、Windows XP 或 Windows 2000。 如需所有 Windows Installer 版本和可轉散發套件的清單，請參閱[Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

Windows Installer 3.1 及更舊版本中不支援下列功能。

[安裝程式函數](installer-functions.md)

-   [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[屬性](properties.md)

-   [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)
-   [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md)
-   [**MSIDISABLERMRESTART**](msidisablermrestart.md)
-   [**MsiLogFileLocation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)
-   [**MSIRMSHUTDOWN**](msirmshutdown.md)
-   [**MsiRunningElevated**](msirunningelevated-.md)
-   [**MsiSystemRebootPending**](msisystemrebootpending.md)
-   [**MsiTabletPC**](msitabletpc.md)
-   [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)

[摘要資訊屬性](summary-information-stream-reference.md)

-   [ [**字數統計摘要] 屬性**](word-count-summary.md) 具有新的旗標位，可指定封裝的安裝是否需要較高的許可權。

[系統原則](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[資料庫資料表](database-tables.md)

-   [快速鍵資料表](shortcut-table.md)

    新資料行： DisplayResourceDLL、DisplayResourceId、DescriptionResourceDLL 和 DescriptionResourceId

[對話方塊](dialog-boxes.md)

-   [MsiRMFilesInUse 對話方塊](msirmfilesinuse-dialog.md)

[控制項屬性](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[事件](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[外部 UI 訊息類型](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   INSTALLLOGMODE \_ RMFILESINUSE

[Windows64位作業系統上的安裝程式](windows-installer-on-64-bit-operating-systems.md)

-   [元件資料表](component-table.md)中的 **msidbComponentAttributesDisableRegistryReflection** 屬性

[Automation 介面](automation-interface.md)

-   [**安裝程式物件** 的方法](installer-object.md)

    -   [**AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**AdvertiseScript**](installer-advertisescript.md)
    -   [**CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**ProvideAssembly**](installer-provideassembly.md)

-   [**安裝程式物件** 的屬性](installer-object.md)

    -   [**PatchFiles**](installer-patchfiles.md)
    -   [**ProductElevated**](installer-productelevated.md)
    -   [**ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>備註

Windows Installer 服務必須在 Windows Vista 上執行，才能使用 [[重新開機管理員](../rstmgr/restart-manager-portal.md)]、[[*使用者帳戶控制*](u-gly.md)] 和 [[使用者帳戶控制] (UAC) 修補](user-account-control--uac--patching.md)。 如需詳細資訊，請參閱搭配[使用 Windows Installer 與重新開機管理員](using-windows-installer-with-restart-manager.md)，以及[使用 Windows Installer 搭配 uac](using-windows-installer-with-uac.md)和[使用者帳戶控制 (uac) 修補](user-account-control--uac--patching.md)。

Windows安裝程式3.1 支援 Windows 檔案保護 (WFP) ，且不支援 Windows 資源保護 (WRP) 。 Windows server 2008 和 Windows Vista 中的 WRP 取代 Windows Server 2003、Windows XP 和 Windows 2000 中的 WFP。 如需 Windows Installer 和 WFP 的詳細資訊，請參閱[使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。

 

 

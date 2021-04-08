---
description: Windows Installer&\# 160、2.0 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Windows Installer 2.0 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852524"
---
# <a name="not-supported-in-windows-installer-20"></a>Windows Installer 2.0 中不支援

Windows Installer 2.0 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。 這份清單缺少某項功能，並不保證支援此功能。 請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。 如需其他 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

Windows Installer 2.0 可在 Microsoft Windows 2000、Microsoft Windows XP 或 Windows Server 2003 上執行。 如需所有 Windows Installer 版本的清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

Windows Installer 2.0 及更舊版本中不支援下列功能。

[安裝程式函數](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Installer 結構](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[資料庫資料表](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[屬性](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[系統原則](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[錯誤碼](error-codes.md)

-   \_ \_ 不支援移除錯誤修補程式 \_
-   錯誤 \_ 不明的 \_ 修補程式
-   錯誤 \_ 修補程式 \_ 沒有 \_ 順序
-   不 \_ \_ 允許移除錯誤修補程式 \_
-   錯誤 \_ 不正確 \_ PATCH \_ XML
-   錯誤 \_ 修補 \_ 受管理的 \_ 公告 \_ 產品

記錄模式

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Automation 介面](automation-interface.md)

-   [ **Product 物件** 的屬性](product-object.md)

    -   [**UserSid**](product-usersid.md)
    -   [**產品。來源**](product-sources.md)
    -   [**MediaDisks**](product-mediadisks.md)
    -   [**FeatureState**](product-featurestate.md)
    -   [**Product. CoNtext**](product-context.md)
    -   [**InstallProperty**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**ComponentState**](product-componentstate.md)
    -   [**產品。州**](product-state.md)
    -   [**SourceListInfo**](product-sourcelistinfo.md)

-   [ **Product 物件** 的方法](product-object.md)

    -   [**SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**SourceListClearAll**](product-sourcelistclearall.md)
    -   [**SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   [ **Patch 物件** 的屬性](patch-object.md)

    -   [**Patch. UserSid**](patch-usersid.md)
    -   [**修補程式。狀態**](patch-state.md)
    -   [**Patch。來源**](patch-sources.md)
    -   [**Patch. SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch。 ProductCode**](patch-productcode.md)
    -   [**Patch. PatchProperty**](patch-patchproperty.md)
    -   [**Patch. PatchCode**](patch-patchcode.md)
    -   [**Patch. MediaDisks**](patch-mediadisks.md)
    -   [**Patch。 CoNtext**](patch-context.md)

-   [ **Patch 物件** 的方法](patch-object.md)

    -   [**Patch. SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch. SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch. SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch. SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   [**安裝程式物件** 的屬性](installer-object.md)

    -   [**ProductsEx**](installer-productsex.md)
    -   [**ProductInfo**](installer-productinfo.md)
    -   [**PatchesEx**](installer-patchesex.md)

-   [**安裝程式物件** 的方法](installer-object.md)

    -   [**ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**ApplyPatch**](installer-applypatch.md)
    -   [**RemovePatches**](installer-removepatches.md)
    -   [**ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Windows Installer 版本2.0.2600 中也不支援下列功能。 Windows Installer 版本2.0.2600 已與 Windows XP 和 Windows 2000 伺服器一起發行。 從使用 Windows Server 2003 發行的 Windows Installer 版本2.0.3790 開始，可以使用這些功能。 如需所有 Windows Installer 版本的清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

[安裝程式函數](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   MSIADVERTISEOPTIONS \_ 實例
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Automation 介面](automation-interface.md)

-   [**安裝程式物件** 的方法](installer-object.md)

    -   [**ApplyPatch**](installer-applypatch.md)
    -   [**ProductInfo**](installer-productinfo.md)

[屬性](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[錯誤碼](error-codes.md)

-   [\_禁止安裝 \_ 遠端的錯誤 \_](error-codes.md)

[電腦原則](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [TransformsSecure 原則](transformssecure-policy.md)

[命令列選項](command-line-options.md)

-   [/c](command-line-options.md)
-   [n](command-line-options.md)
-   [/Lx](command-line-options.md)

[控制項屬性](control-attributes.md)

-   **ImageHandle** 已移除

## <a name="notes"></a>備註

Windows Installer 2.0 不支援 [標準安裝程式 Command-Line 選項](standard-installer-command-line-options.md) 。 請改用 Windows Installer [命令列選項](command-line-options.md)。

當 Windows Installer 2.0 安裝 patch 封裝時，它會忽略 [MsiPatchSequence](msipatchsequence-table.md) 或 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中的資訊。 較新版本的 Windows Installer 可以使用這些資料表中的資訊，來改善修補程式的排序、移除和優化。 如需 Windows Installer 中改進修補功能的相關資訊，請參閱 [修補](patching.md)。

Windows Installer 2.0 不支援 [可卸載修補](uninstallable-patches.md) 程式，以及從應用程式移除特定修補程式的唯一方法，就是卸載整個修補後的應用程式，然後重新安裝，而不需要重新套用任何即將移除的修補程式。

Windows Installer 2.0 不支援修補程式順序，並且會依照在 [安裝多個修補程式](installing-multiple-patches.md)時提供給系統的順序來安裝修補程式。

Windows Installer 2.0 不支援使用 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md) ，以啟用可由非系統管理員使用者套用的數位簽章修補程式。

Windows Installer 2.0 不支援 [修補程式優化](patch-optimization.md)。 相較于稍後 Windows Installer 只會更新受修補程式所影響之檔案的版本，修補可能需要更多時間。

Windows Installer 2.0 不支援 [使用 Windows Installer 來清查產品和修補程式](inventory-products-and-patches-.md)。

Windows Installer 2.0 不支援對所有使用者在系統上安裝的 Windows Installer 應用程式和修補程式的來源清單資訊進行提取和修改。 Windows Installer 的較新版本可讓系統管理員管理網路、URL 和媒體來源的來源清單和來源清單屬性。 較新的版本可讓系統管理員管理外部進程的來源清單。 如需詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。

Windows Installer 2.0 不支援安裝多個產品或修補程式的實例，而且每個實例都沒有個別的安裝套件。 之後 Windows Installer 版本可以使用產品程式碼轉換和一個 .msi 封裝或一個修補程式，安裝多個產品的實例。 如需詳細資訊，請參閱 [安裝產品和修補程式的多個實例](installing-multiple-instances-of-products-and-patches.md)。

從 Windows XP Service Pack 2 開始 (SP2) ，Windows Installer 可以使用 HTTP、HTTPS 和檔案通訊協定。 安裝程式不支援 FTP 和 GOPHER 通訊協定。

 

 




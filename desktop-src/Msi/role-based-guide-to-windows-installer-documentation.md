---
description: Windows安裝程式是在 Windows 上安裝和設定應用程式的建議解決方案。
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Windows Installer 檔的以角色為基礎的指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625860"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Windows Installer 檔的以角色為基礎的指南

Windows安裝程式是在 Windows 上安裝和設定應用程式的建議解決方案。 因此，此 SDK 中包含的部分資訊會對各式各樣的軟體發展和 IT 專業人員感興趣。 這一節是以讀者的指南來提供，想要看到依專業角色和一般工作案例組織的主題連結。 因為組織之間的角色可能會有極大的差異，所以必須將下列群組視為要開始搜尋所需資訊的位置指南。

-   [應用程式開發人員](#application-developers)
-   [設定作者](#setup-authors)
-   [IT 專業人員](#it-professionals)
-   [基礎結構開發人員](#infrastructure-developers)

本檔適用于想要讓應用程式使用 Windows Installer 的軟體發展人員。 SDK 是安裝程式參考資料的主要來源，提供安裝套件和安裝程式服務的相關資訊。 它包含應用程式開發介面的完整描述 (API) 和安裝程式資料庫的元素。

如需詳細資訊，請參閱[Windows Installer 資訊的其他來源](other-sources-of-windows-installer-information.md)。

## <a name="application-developers"></a>應用程式開發人員

應用程式開發人員建立的應用程式會呼叫 Windows Installer 應用程式開發介面，並在執行時間安裝 Windows 安裝程式套件。 Windows Installer 可以在應用程式中工作，例如自行修復和隨選安裝。 一般來說，應用程式開發人員會執行下列動作：

-   在執行時間從另一個應用程式中啟用應用程式的隨選安裝。

    如需詳細資訊，請參閱下列：

    -   [使用安裝程式函數](using-installer-functions.md)
    -   [安裝程式函數參考](installer-function-reference.md)
    -   [隨選安裝](installation-on-demand.md)
    -   [元件管理](component-management.md)
    -   [編輯安裝程式快捷方式](editing-installer-shortcuts.md)
    -   [**OLEAdvtSupport 屬性**](oleadvtsupport.md)
    -   [廣告的平臺支援](platform-support-of-advertisement.md)

-   在執行時間視需要重新安裝元件，以啟用應用程式的自我修復。

    如需詳細資訊，請參閱下列：

    -   [使用安裝程式函數](using-installer-functions.md)
    -   [安裝程式函數參考](installer-function-reference.md)
    -   [復原](resiliency.md)
    -   [來源復原](source-resiliency.md)
    -   [搜尋中斷的功能或元件](searching-for-a-broken-feature-or-component.md)
    -   [取代現有的檔案](replacing-existing-files.md)

-   顯示使用者介面，以便在第一次安裝或執行應用程式時，收集使用者資訊和設定喜好設定。 使用者介面必須由 Windows Installer 套件的安裝程式作者加入。

    如需詳細資訊，請參閱下列：

    -   [使用安裝程式函數](using-installer-functions.md)
    -   [初始化應用程式](initializing-an-application.md)
    -   [Firstrun.cmd 對話方塊](firstrun-dialog.md)
    -   [關於消費者介面](about-the-user-interface.md)

-   建立應用程式，使用間接模型來參考具有平行功能的元件。 Windows Installer 套件的安裝程式作者必須加入限定的元件類別。

    如需詳細資訊，請參閱下列：

    -   [合格元件](qualified-components.md)
    -   [使用限定元件](using-qualified-components.md)

-   使用私用和並存元件來隔離應用程式並減少 DLL 衝突。

    如需詳細資訊，請參閱下列：

    -   [組件](assemblies.md)
    -   [Windows Installer 所寫入的元件登錄機碼](assembly-registry-keys-written-by-windows-installer-.md)
    -   [在 Windows XP 上安裝適用于並存共用的 Win32 元件](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [在 Windows XP 上安裝 Win32 元件以私用應用程式](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [MsiAssembly 資料表](msiassembly-table.md)
    -   [MsiAssemblyName 資料表](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**MsiWin32AssemblySupport 屬性**](msiwin32assemblysupport.md)
    -   [**MsiNetAssemblySupport 屬性**](msinetassemblysupport.md)
    -   [**隔離的元件**](isolated-components.md)

-   準備應用程式來安裝自己的完整主要升級。

    如需詳細資訊，請參閱下列：

    -   [修補和升級](patching-and-upgrades.md)
    -   [主要升級](major-upgrades.md)
    -   [**UpgradeCode 屬性**](upgradecode.md)
    -   [**使用 UpgradeCode**](using-an-upgradecode.md)
    -   [防止舊套件安裝在較新的版本上](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   準備應用程式以安裝自己的次要升級、小型更新或修正。

    如需詳細資訊，請參閱下列：

    -   [修補和升級](patching-and-upgrades.md)
    -   [小型更新](small-updates.md)
    -   [次要升級](minor-upgrades.md)

-   將應用程式資源組織成可搭配 Windows Installer 使用的元件。

    如需詳細資訊，請參閱下列：

    -   [Windows安裝程式元件](windows-installer-components.md)
    -   [使用功能和元件](working-with-features-and-components.md)
    -   [使用可轉移的元件](using-transitive-components.md)
    -   [如果元件規則中斷，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)
    -   [將應用程式組織成元件](organizing-applications-into-components.md)
    -   [隔離的元件](isolated-components.md)
    -   [合格元件](qualified-components.md)

## <a name="setup-authors"></a>設定作者

安裝程式作者會建立 Windows Installer 套件 (.msi 檔案) ，其中包含安裝程式邏輯以及安裝應用程式所需的資訊。 它們通常會使用撰寫工具（例如[Orca.exe](orca-exe.md) ），以安裝程式邏輯和資訊填入 Windows Installer 資料庫。 一般而言，安裝程式作者會執行下列動作：

-   判斷不同 Windows Installer 版本所提供的功能。

    如需詳細資訊，請參閱下列：

    -   [判斷 Windows Installer 版本](determining-the-windows-installer-version.md)
    -   [Windows Installer 的發行版本](released-versions-of-windows-installer.md)
    -   [Windows Installer 的新功能](what-s-new-in-windows-installer.md)

-   將應用程式資源組織成 Windows Installer 元件。

    如需詳細資訊，請參閱下列：

    -   [Windows安裝程式元件](windows-installer-components.md)
    -   [將應用程式組織成元件](organizing-applications-into-components.md)
    -   [變更元件程式碼](changing-the-component-code.md)
    -   [如果元件規則中斷，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   使用協力廠商 Windows Installer 套件撰寫工具或 SDK 工具（例如[Orca.exe](orca-exe.md) ）來填入安裝資料庫，並建立 Windows Installer 套件。

    如需詳細資訊，請參閱下列：

    -   [Windows安裝程式開發工具](windows-installer-development-tools.md)
    -   [安裝套件，關於安裝程式資料庫](installation-package.md)
    -   [Windows安裝程式副檔名](windows-installer-file-extensions.md)
    -   [資料庫資料表](database-tables.md)
    -   [封裝碼](package-codes.md)
    -   [撰寫大型封裝](authoring-a-large-package.md)
    -   [Windows64位作業系統上的安裝程式](windows-installer-on-64-bit-operating-systems.md)
    -   [命名自訂資料表、屬性和動作](naming-custom-tables-properties-and-actions.md)
    -   [資料流程的 OLE 限制](ole-limitations-on-streams.md)
    -   [資料行定義格式](column-definition-format.md)
    -   [減少 .msi 檔案的大小](reducing-the-size-of-an--msi-file.md)

-   撰寫 Windows Installer 資料庫以安裝檔案。

    如需詳細資訊，請參閱下列：

    -   [核心資料表群組](core-tables-group.md)
    -   [檔案資料表群組](file-tables-group.md)
    -   [FileTable](file-table.md)
    -   [檔案搜尋](file-searching.md)
    -   [檔案成本](file-costing.md)
    -   [檔案安裝](file-installation.md)
    -   [隨附檔案](companion-files.md)
    -   [檔案版本控制規則](file-versioning-rules.md)
    -   [預設檔案版本控制](default-file-versioning.md)
    -   [取代現有的檔案](replacing-existing-files.md)
    -   [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)
    -   [移除擱置的檔案](removing-stranded-files.md)
    -   [安裝永久元件、檔案、字型、登錄機碼](installing-permanent-components-files-fonts-registry-keys.md)
    -   [FileSFPCatalog 資料表](filesfpcatalog-table.md)
    -   [搜尋檔案並建立保存檔案路徑的屬性](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [搜尋目錄和目錄中的檔案](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   撰寫安裝目錄結構和資料夾的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [核心資料表群組](core-tables-group.md)
    -   [檔案資料表群組](file-tables-group.md)
    -   [元件資料表](component-table.md)
    -   [目錄資料表](directory-table.md)
    -   [使用目錄資料表](using-the-directory-table.md)
    -   [使用路徑中的目錄屬性](using-a-directory-property-in-a-path.md)
    -   [系統資料夾屬性](property-reference.md)
    -   [CreateFolder 資料表](createfolder-table.md)
    -   [LockPermissions 資料表](lockpermissions-table.md)
    -   [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)
    -   [變更目錄的目標位置](changing-the-target-location-for-a-directory.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   撰寫會安裝登錄機碼的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [核心資料表群組](core-tables-group.md)
    -   [登錄資料表群組](registry-tables-group.md)
    -   [登錄資料表](registry-table.md)
    -   [修改登錄](modifying-the-registry.md)
    -   [在安裝或移除元件時新增或移除登錄機碼](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [新增和移除應用程式，而不在登錄中保留任何追蹤](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [安裝永久元件、檔案、字型、登錄機碼](installing-permanent-components-files-fonts-registry-keys.md)
    -   [搜尋現有的應用程式、檔案、登錄專案或 .ini 的檔案專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [搜尋登錄專案，並建立保存登錄值的屬性](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Windows Installer 所寫入的元件登錄機碼](assembly-registry-keys-written-by-windows-installer-.md)
    -   [卸載登錄機碼](uninstall-registry-key.md)
    -   [SelfReg 資料表](selfreg-table.md)
    -   [指定自我註冊的順序](specifying-the-order-of-self-registration.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   撰寫安裝服務的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [ServiceInstall 資料表](serviceinstall-table.md)
    -   [ServiceControl 資料表](servicecontrol-table.md)
    -   [元件資料表](component-table.md)

-   撰寫可安裝隔離元件或 COM 元件的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [登錄資料表群組](registry-tables-group.md)
    -   [類別資料表](class-table.md)
    -   [Complus 資料表](complus-table.md)
    -   [隔離的元件](isolated-components.md)
    -   [使用隔離的元件](using-isolated-components.md)
    -   [獨立元件的安裝](installation-of-isolated-components.md)
    -   [重新安裝隔離的元件](reinstallation-of-isolated-components.md)
    -   [移除隔離的元件](removal-of-isolated-components.md)
    -   [將 COM 元件安裝至私用位置](installing-a-com-component-to-a-private-location.md)
    -   [使現有封裝中的 COM 元件成為私用](make-a-com-component-in-an-existing-package-private.md)
    -   [安裝具有 Windows Installer 的 com + 應用程式](installing-a-com--application-with-the-windows-installer.md)
    -   [將非 COM 元件安裝至私用位置](installing-a-non-com-component-to-a-private-location.md)
    -   [將現有封裝中的非 COM 元件設為私用](make-a-non-com-component-in-an-existing-package-private.md)

-   撰寫安裝元件的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [MsiAssembly 資料表](msiassembly-table.md)
    -   [MsiAssemblyName 資料表](msiassemblyname-table.md)
    -   [組件](assemblies.md)
    -   [Windows Installer 所寫入的元件登錄機碼](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Win32 元件的安裝](installation-of-win32-assemblies.md)

-   撰寫安裝 ODBC 驅動程式和轉譯程式的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [ODBCAttribute 資料表](odbcattribute-table.md)
    -   [ODBCDriver 資料表](odbcdriver-table.md)
    -   [ODBCTranslator 資料表](odbctranslator-table.md)
    -   [ODBCDataSource 資料表](odbcdatasource-table.md)
    -   [ODBCSourceAttribute 資料表](odbcsourceattribute-table.md)

-   撰寫可安裝 MIME 的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [MIME 資料表](mime-table.md)
    -   [延伸模組資料表](extension-table.md)
    -   [修改登錄](modifying-the-registry.md)

-   撰寫會安裝環境變數的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [環境資料表](environment-table.md)

-   撰寫可安裝快速鍵的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [快速鍵資料表](shortcut-table.md)
    -   [MsiShortcutProperty 資料表](msishortcutproperty-table.md)
    -   [編輯安裝程式快捷方式](editing-installer-shortcuts.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   撰寫安裝多個應用程式實例的 Windows Installer 資料庫。

    如需詳細資訊，請參閱下列：

    -   [安裝多個產品和修補程式實例](installing-multiple-instances-of-products-and-patches.md)
    -   [使用實例轉換撰寫多個實例](authoring-multiple-instances-with-instance-transforms.md)
    -   [使用實例轉換安裝多個實例](installing-multiple-instances-with-instance-transforms.md)

-   指定預設功能選取狀態和選項。

    如需詳細資訊，請參閱下列：

    -   [核心資料表群組](core-tables-group.md)
    -   [元件資料表](component-table.md)
    -   [功能資料表](feature-table.md)
    -   [FeatureComponents 資料表](featurecomponents-table.md)
    -   [控制特徵選取狀態](controlling-feature-selection-states.md)
    -   [功能安裝選項屬性](property-reference.md)

-   指定必須符合才能安裝應用程式或選定元件的條件。

    如需詳細資訊，請參閱下列：

    -   [條件資料表](condition-table.md)
    -   [LaunchCondition 資料表](launchcondition-table.md)
    -   [元件資料表](component-table.md)
    -   [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)
    -   [條件陳述式語法](conditional-statement-syntax.md)
    -   [要在移除期間執行的調節動作](conditioning-actions-to-run-during-removal.md)
    -   [條件陳述式語法的範例](examples-of-conditional-statement-syntax.md)

-   撰寫用來安裝應用程式的動作順序。

    如需詳細資訊，請參閱下列：

    -   [使用順序資料表](using-a-sequence-table.md)
    -   [安裝程式資料表群組](installation-procedure-tables-group.md)
    -   [順序資料表詳細範例](sequence-table-detailed-example.md)
    -   [具有排序限制的動作](actions-with-sequencing-restrictions.md)
    -   [沒有排序限制的動作](actions-without-sequencing-restrictions.md)
    -   [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)
    -   [條件陳述式語法](conditional-statement-syntax.md)
    -   [條件陳述式語法的範例](examples-of-conditional-statement-syntax.md)
    -   [要在移除期間執行的調節動作](conditioning-actions-to-run-during-removal.md)
    -   [標準動作](standard-actions.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   準備應用程式的安裝套件，以便日後 Windows Installer 服務升級應用程式。

    如需詳細資訊，請參閱下列：

    -   [修補和升級](patching-and-upgrades.md)
    -   [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)
    -   [使用 UpgradeCode](using-an-upgradecode.md)
    -   [升級資料表](upgrade-table.md)
    -   [**UpgradeCode 屬性**](upgradecode.md)
    -   [防止舊套件安裝在較新的版本上](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [變更產品代碼](changing-the-product-code.md)
    -   [更新組件](updating-assemblies.md)
    -   [Windows安裝程式範例](windows-installer-examples.md)

-   針對開發中的 Windows Installer 套件進行疑難排解。

    如需詳細資訊，請參閱下列：

    -   [套件驗證](package-validation.md)
    -   [內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)
    -   [Windows安裝程式記錄](windows-installer-logging.md)
    -   [檢查功能、元件、檔案的安裝](checking-the-installation-of-features-components-files.md)
    -   [撰寫大型封裝](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows安裝程式開發工具](windows-installer-development-tools.md)
    -   [驗證合併模組](validating-merge-modules.md)
    -   [驗證安裝資料庫](validating-an-installation-database.md)
    -   [驗證安裝升級](validating-an-installation-upgrade.md)
    -   [搜尋中斷的功能或元件](searching-for-a-broken-feature-or-component.md)
    -   [Windows安裝程式錯誤訊息](windows-installer-error-messages.md)
    -   [重新開機要求的記錄](logging-of-reboot-requests.md)

-   確保應用程式的安全安裝和安裝。

    如需詳細資訊，請參閱下列：

    -   [撰寫安全安裝的指導方針](guidelines-for-authoring-secure-installations.md)
    -   [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)
    -   [自訂動作安全性](custom-action-security.md)
    -   [在鎖定的電腦上保護套件安全的指導方針](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [以 URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)
    -   [撰寫密碼輸入的消費者介面](authoring-the-user-interface-for-password-input.md)
    -   [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)
    -   [搭配使用 Windows Installer 與 UAC](using-windows-installer-with-uac.md)
    -   [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser 屬性**](adminuser.md)
    -   [**具有特殊許可權的屬性**](privileged.md)
    -   [**SecureCustomProperties 屬性**](securecustomproperties.md)

-   建立使用者介面，以顯示設定安裝的選項，並向使用者取得擱置安裝程式的相關資訊。

    如需詳細資訊，請參閱下列：

    -   [關於消費者介面](about-the-user-interface.md)
    -   [加入控制項和文字](adding-controls-and-text.md)
    -   [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)
    -   [撰寫磁片提示訊息](authoring-disk-prompt-messages.md)
    -   [撰寫條件式「請稍候 ...」訊息方塊](authoring-a-conditional-please-wait-------message-box.md)
    -   [預覽消費者介面](previewing-the-user-interface.md)
    -   [加入儲存在屬性中的文字](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   建立外部使用者介面來呈現自訂使用者介面，以設定安裝並從使用者取得有關擱置安裝程式的資訊。

    如需詳細資訊，請參閱下列：

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [使用 MsiSetExternalUIRecord 監視安裝](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [剖析 Windows Installer 訊息](parsing-windows-installer-messages.md)
    -   [從外部消費者介面處理常式傳回值](returning-values-from-an-external-user-interface-handler.md)
    -   [INSTALLUI \_ 處理常式](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [使用 MsiSetExternalUI 處理進度訊息](handling-progress-messages-using-msisetexternalui.md)
    -   [使用 MsiSetExternalUI 監視安裝](monitoring-an-installation-using-msisetexternalui.md)

-   在 [ **新增/移除程式** ] (ARP 中設定應用程式的資訊 ) 

    如需詳細資訊，請參閱下列：

    -   [使用 Windows Installer 設定新增/移除程式](configuring-add-remove-programs-with-windows-installer.md)
    -   [新增和移除應用程式，而不在登錄中保留任何追蹤](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [卸載登錄機碼](uninstall-registry-key.md)

-   撰寫自訂動作來處理 Windows Installer 原本就不支援的安裝邏輯。

    如需詳細資訊，請參閱下列：

    -   [自訂動作](custom-actions.md)
    -   [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)
    -   [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)
    -   [自訂動作參考](custom-action-reference.md)
    -   [使用自訂動作在本機電腦上建立使用者帳戶](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [使用自訂動作在安裝結束時啟動已安裝的檔案](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [從自訂動作內部存取資料庫或會話](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [從自訂動作內部存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [使用自訂動作變更系統狀態](changing-the-system-state-using-a-custom-action.md)

-   在使用者的電腦上啟動 Windows Installer。

    如需詳細資訊，請參閱下列：

    -   [啟動](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [網際網路下載啟動載入](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [以 URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)
    -   [設定 Setup.exe 資源](configuring-the-setup-exe-resources.md)
    -   [從網際網路下載安裝](downloading-an-installation-from-the-internet.md)

-   撰寫 Windows Installer 封裝時，請遵循 Active Accessibility 的指導方針。

    如需詳細資訊，請參閱下列：

    -   [協助工具](accessibility.md)

-   為應用程式設定的國際化做好準備。

    如需詳細資訊，請參閱下列：

    -   [準備 Windows Installer 套件進行當地語系化](preparing-a-windows-installer-package-for-localization.md)，
    -   [當地語系化 Windows Installer 套件](localizing-a-windows-installer-package.md)
    -   [程式字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)
    -   [新增當地語系化的資源](adding-localized-resources.md)
    -   [當地語系化範例](a-localization-example.md)
    -   [將錯誤和 ActionText 表當地語系化](localizing-the-error-and-actiontext-tables.md)
    -   [當地語系化資料庫資料行](localizing-database-columns.md)
    -   [使用中性字碼頁建立資料庫](creating-a-database-with-a-neutral-code-page.md)
    -   [匯入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)
    -   [將對話方塊所顯示的語言當地語系化](localizing-the-language-displayed-by-dialogs.md)
    -   [匯入當地語系化的錯誤和 ActionText 資料表](importing-localized-error-and-actiontext-tables.md)
    -   [更新 ProductLanguage 和 ProductCode 屬性](updating-productlanguage-and-productcode-properties.md)
    -   [更新摘要資訊資料流程](updating-a-summary-information-stream.md)
    -   [合格元件](qualified-components.md)
    -   [UIText 資料表](uitext-table.md)
    -   [管理語言和字碼頁](manage-language-and-codepage.md)
    -   [檢查安裝資料庫字碼頁](checking-the-installation-database-code-page.md)

-   建立32位和64位平臺 Windows Installer 套件。

    如需詳細資訊，請參閱下列：

    -   [Windows64位作業系統上的安裝程式](windows-installer-on-64-bit-operating-systems.md)
    -   [64位自訂動作](64-bit-custom-actions.md)
    -   [使用64位自訂動作](using-64-bit-custom-actions.md)
    -   [使用64位合併模組](using-64-bit-merge-modules.md)

-   將共用的 Windows Installer 元件和設定邏輯轉散發為合併模組。

    如需詳細資訊，請參閱下列：

    -   [合併模組](merge-modules.md)
    -   [撰寫多個語言合併模組的語言轉換](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [套用可設定的合併模組與自訂](applying-a-configurable-merge-module-with-customizations.md)

-   排程或隱藏 Windows Installer 安裝期間的重新開機。

    如需詳細資訊，請參閱下列：

    -   [系統重新開機](system-reboots.md)
    -   [重新開機要求的記錄](logging-of-reboot-requests.md)

-   藉由建立修補程式來為現有的應用程式建立更新或修正。

    如需詳細資訊，請參閱下列：

    -   [建立小型更新修補程式](creating-a-small-update-patch.md)
    -   [小型更新修補範例](a-small-update-patching-example.md)

-   撰寫一個可針對目前使用者或電腦的所有使用者安裝應用程式的雙重用途套件。

    如需詳細資訊，請參閱下列：

    -   [安裝內容](installation-context.md)
    -   [單一套件撰寫](single-package-authoring.md)
    -   [單一套件撰寫範例](single-package-authoring-example.md)

-   使用 Windows Installer 自訂電腦上的服務。

    如需詳細資訊，請參閱下列：

    -   [使用服務設定](using-services-configuration.md)

-   使用 Windows Installer 保護電腦上的資源。

    如需詳細資訊，請參閱下列：

    -   [撰寫安全安裝的指導方針](guidelines-for-authoring-secure-installations.md)
    -   [保護資源](securing-resources-.md)

-   列舉電腦上安裝的所有元件，並取得元件的金鑰路徑。

    如需詳細資訊，請參閱下列：

    -   [列舉元件](enumerating-components-.md)

-   使用 [*交易處理*](t-gly.md)來安裝多個封裝。

    如需詳細資訊，請參閱下列：

    -   [多套件安裝](multiple-package-installations.md)

-   在 Windows Installer 套件中內嵌自訂使用者介面。

    如需詳細資訊，請參閱下列：

    -   [使用使用者介面](using-the-user-interface.md)
    -   [使用內嵌 UI](using-an-embedded-ui.md)

## <a name="it-professionals"></a>IT 專業人員

IT 專業人員和系統管理員會自訂及部署現有的 Windows Installer 套件。 這些使用者會將現有應用程式的安裝程式重新封裝成 Windows Installer 安裝套件，並安裝和維護網路上 Windows Installer 安裝的系統管理映射。

-   藉由產生和套用 Windows Installer 轉換來自訂應用程式和設定

    如需詳細資訊，請參閱下列：

    -   [自訂](customization.md)
    -   [資料庫轉換](database-transforms.md)
    -   [自訂轉換範例](a-customization-transform-example.md)
    -   [合併和轉換](merges-and-transforms.md)
    -   [使用轉換來新增資源](using-transforms-to-add-resources.md)
    -   [產生轉換](generate-a-transform.md)
    -   [命令列選項](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [套用轉換](apply-a-transform.md)
    -   [查看轉換](view-a-transform.md)
    -   [查看兩個資料庫之間的差異](view-differences-between-two-databases.md)
    -   [修補自訂應用程式](patching-customized-applications.md)

-   部署 Windows Installer 安裝套件、更新或修補程式。

    如需詳細資訊，請參閱下列：

    -   [安裝應用程式](installing-an-application.md)
    -   [修補和升級](patching-and-upgrades.md)
    -   [轉換](transforms.md)
    -   [以較高的許可權安裝非系統管理員的封裝](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [藉由修補產品的本機安裝來套用主要升級](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [藉由安裝產品來套用主要升級](applying-major-upgrades-by-installing-the-product.md)
    -   [藉由修補產品的本機安裝來套用小型更新](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [重新安裝產品以套用小型更新](applying-small-updates-by-reinstalling-the-product.md)
    -   [藉由修補系統管理映射來套用小型更新](applying-small-updates-by-patching-an-administrative-image.md)
    -   [修補初始安裝](patching-initial-installations.md)
    -   [命令列選項](command-line-options.md)

-   針對 Windows Installer 套件進行疑難排解。

    如需詳細資訊，請參閱下列：

    -   [Windows安裝程式記錄](windows-installer-logging.md)
    -   [檢查功能、元件、檔案的安裝](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [搜尋中斷的功能或元件](searching-for-a-broken-feature-or-component.md)
    -   [Windows安裝程式錯誤訊息](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   使用腳本來查詢 Windows Installer 套件，以取得產品的相關資訊並修改安裝。

    如需詳細資訊，請參閱下列：

    -   [Automation 介面](automation-interface.md)
    -   [Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
    -   [搭配使用 Windows Installer 與 WMI](using-windows-installer-with-wmi.md)

-   建立和維護系統管理安裝。

    如需詳細資訊，請參閱下列：

    -   [系統管理安裝](administrative-installation.md)
    -   [命令列選項](command-line-options.md)
    -   [**AdminProperties 屬性**](adminproperties.md)
    -   [藉由修補系統管理映射來套用小型更新](applying-small-updates-by-patching-an-administrative-image.md)
    -   [將修補套件套用至系統管理安裝](applying-a-patch-package-to-an-administrative-installation.md)
    -   [動作執行順序](action-execution-order.md)
    -   [**IsAdminPackage 屬性**](isadminpackage.md)
    -   [屬性優先順序的順序](order-of-property-precedence.md)
    -   [**AdminProperties 屬性**](adminproperties.md)

-   將應用程式提供給電腦的所有使用者或僅供指定的使用者使用。

    如需詳細資訊，請參閱下列：

    -   [安裝內容](installation-context.md)
    -   [**ALLUSERS 屬性**](allusers.md)

-   使用命令列來解讀套件、安裝產品和設定功能選項。

    如需詳細資訊，請參閱下列：

    -   [命令列選項](command-line-options.md)
    -   [在命令列上設定公用屬性值](setting-public-property-values-on-the-command-line.md)
    -   [取得和設定屬性](getting-and-setting-properties.md)
    -   [重新安裝功能或應用程式](reinstalling-a-feature-or-application.md)
    -   [藉由修補產品的本機安裝來套用小型更新](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [重新安裝產品以套用小型更新](applying-small-updates-by-reinstalling-the-product.md)
    -   [變更目錄的目標位置](changing-the-target-location-for-a-directory.md)
    -   [藉由修補系統管理映射來套用小型更新](applying-small-updates-by-patching-an-administrative-image.md)
    -   [藉由安裝產品來套用主要升級](applying-major-upgrades-by-installing-the-product.md)
    -   [設定屬性](property-reference.md)
    -   [功能安裝選項屬性](property-reference.md)

-   使用原則來管理存取權和許可權。

    如需詳細資訊，請參閱下列：

    -   [電腦原則](machine-policies.md)
    -   [使用者原則](user-policies.md)
    -   [以較高的許可權安裝非系統管理員的封裝](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [廣告以較高的許可權安裝的 Per-User 應用程式](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [使用自訂動作在本機電腦上建立使用者帳戶](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser 屬性**](adminuser.md)
    -   [**具有特殊許可權的屬性**](privileged.md)
    -   [**EnableUserControl 屬性**](enableusercontrol.md)
    -   [**UserSID 屬性**](usersid.md)
    -   [**SecureCustomProperties 屬性**](securecustomproperties.md)

-   使用 [*交易處理*](t-gly.md)來安裝多個封裝。

    如需詳細資訊，請參閱下列：

    -   [多套件安裝](multiple-package-installations.md)

-   在 Windows Installer 套件中內嵌自訂使用者介面。

    如需詳細資訊，請參閱下列：

    -   [使用使用者介面](using-the-user-interface.md)
    -   [使用內嵌 UI](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>基礎結構開發人員

基礎結構開發人員可以建立統一的平臺，以部署和管理使用 Windows Installer 服務的軟體。 他們可以使用 Windows Installer 程式設計介面來查詢、管理及散發系統上的應用程式、修補程式和來源。

-   找出、清查和查詢元件的狀態、資訊和用戶端。

    如需詳細資訊，請參閱下列：

    -   [元件特定函式](installer-function-reference.md)
    -   [系統狀態函數](installer-function-reference.md)
    -   [安裝程式物件](installer-object.md)
    -   [Product 物件](product-object.md)
    -   [Patch 物件](patch-object.md)

-   清查和查詢資訊以及產品和功能的狀態。

    如需詳細資訊，請參閱下列：

    -   [清查產品和修補程式](inventory-products-and-patches-.md)
    -   [系統狀態函數](installer-function-reference.md)
    -   [產品查詢函數](installer-function-reference.md)
    -   [安裝程式物件](installer-object.md)
    -   [Product 物件](product-object.md)
    -   [Patch 物件](patch-object.md)

-   使用 Windows Installer 清查、查詢和修改應用程式、升級和修補程式的來源清單，以改善來源復原。

    如需詳細資訊，請參閱下列：

    -   [**SOURCELIST 屬性**](sourcelist.md)
    -   [**來源復原**](source-resiliency.md)
    -   [安裝和設定功能](installer-function-reference.md)
    -   [安裝程式物件](installer-object.md)
    -   [Product 物件](product-object.md)
    -   [Patch 物件](patch-object.md)

-   使用 Windows Installer 清查、查詢和修改媒體來源，改善來源復原。

    如需詳細資訊，請參閱下列：

    -   [**SOURCELIST 屬性**](sourcelist.md)
    -   [來源復原](source-resiliency.md)
    -   [安裝和設定功能](installer-function-reference.md)
    -   [Product 物件](product-object.md)
    -   [Patch 物件](patch-object.md)

-   清查和查詢資訊和修補程式的狀態。

    如需詳細資訊，請參閱下列：

    -   [清查產品和修補程式](inventory-products-and-patches-.md)
    -   [安裝程式函數參考](installer-function-reference.md)
    -   [Patch 物件](patch-object.md)

-   使用原則來管理存取權和許可權。

    如需詳細資訊，請參閱下列：

    -   [電腦原則](machine-policies.md)
    -   [使用者原則](user-policies.md)
    -   [以較高的許可權安裝非系統管理員的封裝](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [廣告以較高的許可權安裝的 Per-User 應用程式](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [使用自訂動作在本機電腦上建立使用者帳戶](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser 屬性**](adminuser.md)
    -   [**具有特殊許可權的屬性**](privileged.md)
    -   [**EnableUserControl 屬性**](enableusercontrol.md)
    -   [**UserSID 屬性**](usersid.md)
    -   [**SecureCustomProperties 屬性**](securecustomproperties.md)

 

 




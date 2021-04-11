---
description: 本節列舉連結至主要 Windows Installer SDK 檔的秘訣清單，以協助應用程式開發人員、設定作者、IT 專業人員和基礎結構開發人員探索使用 Windows Installer 的最佳作法：
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Installer 最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027019"
---
# <a name="windows-installer-best-practices"></a>Windows Installer 最佳作法

本節列舉連結至主要 Windows Installer SDK 檔的秘訣清單，以協助應用程式開發人員、設定作者、IT 專業人員和基礎結構開發人員探索使用 Windows Installer 的最佳作法：

-   [更新 Windows Installer 版本。](#update-the-windows-installer-version)
-   [符合 Windows 標誌認證需求。](#meet-the-windows-logo-certification-requirements)
-   [準備套件以進行當地語系化。](#prepare-the-package-for-localization)
-   [更新您的 Windows Installer 開發工具和檔。](#update-your-windows-installer-development-tools-and-documentation)
-   [如果您決定重新封裝舊版安裝應用程式，請遵循妥善的重新封裝做法。](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [請勿嘗試取代受保護的資源。](#do-not-try-to-replace-protected-resources)
-   [請勿依賴非關鍵性的資源。](#do-not-depend-upon-non-critical-resources)
-   [使用 API 來取出 Windows Installer 設定資訊。](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [在元件周圍組織應用程式的安裝。](#organize-the-installation-of-your-application-around-components)
-   [減少大型 Windows Installer 套件的大小。](#reduce-the-size-of-large-windows-installer-packages)
-   [如果您使用自訂動作，請遵循良好的自訂動作實務。](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [如果您使用元件，請遵循良好的元件實務](#if-you-use-assemblies-follow-good-assembly-practices)
-   [請勿運送並行安裝。](#do-not-ship-concurrent-installations)
-   [讓套件名稱和套件碼保持一致。](#keep-package-names-and-package-codes-consistent)
-   [請勿使用 SelfReg 和 TypeLib 資料表。](#do-not-use-the-selfreg-and-typelib-tables)
-   [提供在沒有使用者介面的情況下安裝的選項。](#provide-the-option-to-install-without-a-user-interface)
-   [避免使用 AlwaysInstallElevated 原則。](#avoid-using-the-alwaysinstallelevated-policy)
-   [啟用 DisableMedia 原則以限制未經授權的安裝。](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [將原始套件來源檔案保持安全並可供使用者使用。](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [針對部署進行疑難排解時，請在使用者的電腦上啟用詳細資訊記錄。](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [卸載會將使用者的電腦保持在乾淨的狀態。](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [針對每位使用者和每部電腦的安裝部署測試套件。](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [先規劃及測試服務策略，再寄送應用程式。](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [在原始來源上減少更新的相依性。](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [請勿散發 unserviceable 合併模組。](#do-not-distribute-unserviceable-merge-modules)
-   [避免修補系統管理安裝。](#avoid-patching-administrative-installations)
-   [以較高的許可權註冊更新以執行。](#register-updates-to-run-with-elevated-privilege)
-   [使用 MsiPatchSequence 資料表來排列修補程式的順序。](#use-the-msipatchsequence-table-to-sequence-patches)
-   [徹底測試安裝套件。](#test-the-installation-package-thoroughly)
-   [請先修正所有驗證錯誤，再部署新的或修改過的安裝套件。](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [撰寫安全的安裝。](#author-a-secure-installation)
-   [使用 PMSIHANDLE 而非控制碼](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>更新 Windows Installer 版本。

-   在 Windows Server 2008 R2 和 Windows 7 上使用 Windows Installer 5.0。 這是作業系統隨附的 Windows Installer 版本。
-   在 Windows Server 2008、Windows Server 2003 Service Pack 1 (SP1) 、Windows Vista （含 Service Pack 1） (SP1) 或 Windows XP Service Pack 2 (SP2) 中使用 Windows Installer 4.5。 如需取得最新 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer](windows-installer-redistributables.md)可轉散發套件。
-   在 Windows 2000 Service Pack 3 (SP3) 上使用 Windows Installer 3.1。 Windows Installer 3.1 版具有可加速應用程式服務和 [修補](patching.md)的功能。
-   版本3.0 引進了許多重要的功能，並且列在 [Windows Installer 版本2.0 中不支援](not-supported-in-windows-installer-version-2-0.md)的章節。 您可以使用 Windows Installer 3.0 和更新版本，安裝針對 Windows Installer 2.0 建立的安裝套件和更新。 如果修補封裝包含 Windows Installer 3.0 所使用的新資料表，仍然可以使用舊版 Windows Installer，但不含 Windows Installer 3.0 修補功能。 您也可以撰寫明確需要 Windows Installer 3.0 的修補程式，而這些修補程式無法由舊版 Windows Installer 套用。 如果使用者無法更新安裝程式版本，請確定您的應用程式或更新將與未來的 Windows Installer 更新相容。
-   如需舊版 Windows Installer 不支援的 Windows Installer 功能清單，請參閱 [Windows Installer 中的新](what-s-new-in-windows-installer.md)功能。

## <a name="meet-the-windows-logo-certification-requirements"></a>符合 Windows 標誌認證需求。

-   即使您不打算將您的應用程式提交到標誌計畫，遵循標誌認證指導方針可協助讓您的 Windows Installer 套件更好。 如需標誌需求的總覽，以及特定標誌認證計畫的連結，請參閱 [Windows Installer 和標誌需求](windows-installer-and-logo-requirements.md)。

## <a name="prepare-the-package-for-localization"></a>準備套件以進行當地語系化。

-   撰寫原始安裝套件時，最好先準備好未來的當地語系化。 您可以依照建議的封裝當地語系化程式來 [當地語系化 Windows Installer 套件](localizing-a-windows-installer-package.md)。

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>更新您的 Windows Installer 開發工具和檔。

-   [Windows Installer 的開發工具](windows-installer-development-tools.md)不是可轉散發套件，您應該只使用 Microsoft 提供的這些工具版本。 這些都可在 Microsoft Windows 軟體開發套件 (SDK) 中 [Windows Installer 開發人員的 Windows SDK 元件中取得](platform-sdk-components-for-windows-installer-developers.md) 。
-   許多獨立軟體廠商提供建立或修改 Windows Installer 套件的工具。 這些工具可以提供封裝撰寫環境，比 Windows Installer SDK 中提供的工具更容易使用。 您可以從 [Windows Installer 資訊的其他來源](other-sources-of-windows-installer-information.md)中所討論的資訊資源，深入瞭解這些工具。
-   對某些開發人員而言，從文字檔建立封裝的功能可能更直覺化。 [Sourceforge.net](https://sourceforge.net/projects/wix)上提供的 Windows Installer Xml (WiX) 工具組會從 XML 原始程式碼建立 Windows 安裝套件。
-   MSDN 線上程式庫中所發行 [WINDOWS INSTALLER SDK](./windows-installer-portal.md) 的檔最常更新。
-   使用適用于 Windows Vista 或更新版本的[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供的[Msizap.exe](msizap-exe.md) (版本3.1.4000.2726 或更高版本) 。 較低版本的 Msizap.exe 可以移除已套用至使用者電腦上其他應用程式之所有更新的相關資訊。 如果移除此資訊，可能需要移除並重新安裝這些其他應用程式才能接收其他更新。
-   資料庫資料表編輯器 [Orca.exe](orca-exe.md) 是用來建立和編輯 Windows Installer 封裝和合併模組的資料庫資料表編輯器。 它有基本的 GUI 介面，但支援 Windows Installer 資料庫的 advanced 編輯。 即使您使用其他應用程式作為主要開發工具，但您可能會發現使用 Orca.exe 在對封裝進行疑難排解和測試時，會很方便。
-   如需最新的 Windows Installer 資訊，請參閱 [Windows Installer 資訊的其他來源](other-sources-of-windows-installer-information.md) ，這些資訊可在 blog、技術聊天室、新聞群組、技術文章和網站中取得。

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>如果您決定重新封裝舊版安裝應用程式，請遵循妥善的重新封裝做法。

許多應用程式廠商都提供安裝或其產品的原生 Windows Installer 套件。 將現有舊版安裝應用程式轉換成 Windows Installer 套件的軟體稱為「重新封裝」工具。 [針對 Windows Installer 建立 Windows Installer 套件和重新封裝軟體的白皮書逐步指南](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx)，描述商用的可重新封裝工具。 重新封裝現有的安裝應用程式並不是最佳的開發作法。 從開始設計的應用程式會利用 Windows Installer 功能，可讓使用者更輕鬆地安裝及服務。 如果您決定使用重新封裝軟體，下列做法可協助您產生更好的 Windows Installer 套件。

-   重新封裝工具會將舊版安裝轉換成 Windows Installer 套件，方法是在安裝前後拍攝預備系統的圖片。 在執行捕獲程式期間發生的任何登錄變更、檔案變更或系統設定，都會包含在安裝中。 將用來重新封裝安裝的電腦硬體和軟體設定為盡可能接近預期的使用者系統。 為每個不同的硬體設定建立個別的套件。 使用乾淨的預備電腦重新封裝。 移除任何不必要的應用程式。 停止所有不必要的進程。 關閉所有非基本的系統服務。
-   請一律建立原始安裝的複本，然後開始處理它。 一律使用複製。 在完成封裝的建立之前，絕對不要停止重新封裝器。 如果重新封裝器損毀封裝，您仍然會有原始的。
-   請勿將 Microsoft 軟體更新重新封裝成 Windows Installer 套件。 Microsoft 會將軟體更新（例如 service pack）發行為自動執行安裝的自動解壓縮檔案。 這些更新會使用不同于 Windows Installer 的安裝程式來取代受保護的 Windows 資源，且無法轉換成 Windows Installer 套件。 如需有關如何部署 Windows service pack 的詳細資訊，請參閱 [Microsoft TechNet](https://technet.microsoft.com/)上的 service pack 部署指南。
-   請勿使用重新封裝工具將 Windows Installer 封裝轉換成新的套件。 Windows Installer 會將設定資訊新增至系統以及應用程式資源。 當重新封裝工具在安裝前後比較系統時，重新封裝器會誤譯設定資訊作為應用程式的一部分。 這通常會損害重新封裝的應用程式。 改為使用 [自訂轉換](a-customization-transform-example.md) 來修改現有的 Windows Installer 封裝，或建立新的封裝。 您可以使用 [Msitran.exe](msitran-exe.md) 工具來建立自訂轉換。
-   請勿使用重新封裝工具，將數個 Windows Installer 套件合併成單一套件。 您可以改為使用 [Msistuff.exe](msistuff-exe.md) 工具來設定 Setup.exe 啟動程式可執行檔，以逐一安裝套件。
-   製作您的 Windows Installer 套件，讓客戶可以輕鬆地自訂。 在安裝期間，Windows Installer 所使用的全域變數可以使用公用 [屬性](properties.md) 或 [自訂轉換](a-customization-transform-example.md)來設定。 提供檔，說明如何使用這些屬性以及所有可自訂值的實際預設值。 如需取得和設定屬性的詳細資訊，請參閱 [使用屬性](using-properties.md)。 如需自訂轉換的範例，請參閱 [自訂轉換範例](a-customization-transform-example.md)。

## <a name="do-not-try-to-replace-protected-resources"></a>請勿嘗試取代受保護的資源。

在安裝或更新期間，Windows Installer 套件不應嘗試取代受保護的資源。 Windows Installer 不會移除或取代這些資源，因為 Windows 會防止取代必要的系統檔案、資料夾和登錄機碼。 保護這些資源可防止應用程式和作業系統失敗。

-   在 Windows Server 2008 或 Windows Vista 上執行時，Windows Installer 會略過 [Windows 資源保護](../wfp/windows-resource-protection-portal.md) (WRP) 所保護的任何檔案或登錄機碼的安裝，安裝程式會在記錄檔中輸入警告，並繼續安裝的其餘部分，而不會發生錯誤。 如需詳細資訊，請參閱 [使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。
-   WRP 是 Windows 檔案保護 (WFP) 的新名稱。 WRP 可保護登錄機碼和資料夾，以及基本的系統檔案。 在 Windows Server 2003、Windows XP 及 Windows 2000 中，當 Windows Installer 遇到受 WFP 保護的檔案時，安裝程式會要求 WFP 安裝檔案。 如需詳細資訊，請參閱 [使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。

## <a name="do-not-depend-upon-non-critical-resources"></a>請勿依賴非關鍵性的資源。

基於下列原因，您的安裝或更新不應該相依于非關鍵性資源的安裝。

-   如果自訂動作相依于某個元件，而該元件屬於使用者所通告的功能，而不是安裝，則可能會失敗。
-   如果自訂動作相依于包含所安裝元件的元件，則在 [InstallFinalize](installfinalize-action.md) 動作之前排序的自訂動作可能會失敗。 Windows Installer 在 InstallFinalize 動作完成之前，不會將元件認可至全域組件快取 (GAC) 。

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>使用 API 來取出 Windows Installer 設定資訊。

安裝您的應用程式或更新時，不應該相依于您電腦上所儲存 Windows Installer 設定資訊的直接存取。 改為使用 Windows Installer 應用程式開發介面來取得設定資訊。 設定資訊的位置和格式是由 Windows Installer 服務所管理，而且可以變更。

-   Windows Installer API 的安裝和設定功能將在 [安裝程式函數參考](installer-function-reference.md)中說明。
-   設定 [屬性](property-reference.md) 會在屬性參考中描述。
-   Automation [介面參考](automation-interface-reference.md)中說明了自動化方法和屬性。 範例腳本 WiLstPrd.vbs 連接到安裝程式物件，並列舉已註冊的產品和產品資訊。 如需詳細資訊，請參閱 [列出產品、屬性、功能和元件](list-products-properties-features-and-components.md)。

## <a name="organize-the-installation-of-your-application-around-components"></a>在元件周圍組織應用程式的安裝。

Windows Installer 服務會安裝或移除稱為 [元件](windows-installer-components.md)的資源集合。 因為通常會共用元件，所以安裝套件的作者在指定功能或應用程式的元件時，必須遵循規則。

-   將 [應用程式組織成元件](organizing-applications-into-components.md) 時，請遵循元件規則，以確保可以安裝和移除新元件或新版本的元件，而不會破壞其他應用程式。 您可以依照 [定義安裝程式元件](defining-installer-components.md)中所述的程式進行操作。
-   安裝程式會依 [元件表格](component-table.md)中所指定的個別元件識別碼 GUID 來追蹤每個元件。 這對 Windows Installer 的參考計數機制而言很重要，因為元件識別碼 GUID 是正確的。 遵循 [變更元件程式碼](changing-the-component-code.md)的指導方針。
-   如果您的套件必須中斷元件規則，請留意可能的結果，並確定您的安裝絕不會安裝這些元件，而這些元件可能會損毀使用者系統上的元件。 如需詳細資訊，請參閱 [元件規則中斷時，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)。
-   [取代現有](replacing-existing-files.md)的檔案時，請注意 Windows Installer 如何套用檔案[版本控制規則](file-versioning-rules.md)。 Windows Installer 先決定是否已安裝元件的金鑰檔，然後再嘗試安裝元件的任何檔案。 如果安裝程式找到的檔案與安裝在目標位置中的元件金鑰檔名稱相同，則會比較兩個金鑰檔的版本、日期和語言，並使用檔案版本控制規則來判斷是否要安裝封裝所提供的元件。 如果安裝程式判斷需要在金鑰檔上取代元件基底，則會在每個已安裝的檔案上使用檔案版本控制規則，以判斷是否要取代檔案。

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>減少大型 Windows Installer 套件的大小。

非常大型的 Windows 套件採用系統資源，而且可能很難安裝使用者。 最好的作法是使用下列方法來縮減超大型 Windows Installer 套件的大小。

-   壓縮安裝中的檔案，並將它們儲存在封包 ( .cab) 檔案中。 安裝程式允許將 .cab 檔儲存為個別的外部檔案，或儲存為 MSI 封裝本身的資料流程。 如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。
-   使用 [減少 .msi 檔案大小](reducing-the-size-of-an--msi-file.md)所討論的其中一個選項，移除 .msi 檔案中浪費的儲存空間。
-   如果您的 Windows Installer 封裝包含32767以上的檔案，您必須變更資料庫的架構。 如需詳細資訊，請參閱 [撰寫大型封裝](authoring-a-large-package.md)。

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>如果您使用自訂動作，請遵循良好的自訂動作實務。

Windows Installer 在安裝和維護應用程式時，有許多內建的 [標準動作](standard-actions-reference.md) 。 開發人員應該儘量依賴標準動作，而不是建立自己的 [自訂動作](custom-actions.md)。 不過，在某些情況下，安裝套件的開發人員會發現需要撰寫自訂動作。

-   遵循 [使用自訂動作](using-custom-actions.md)的指導方針。
-   遵循 [指導方針來保護自訂動作](guidelines-for-securing-custom-actions.md)。 使用敏感性資訊的自訂動作不應將此資訊寫入記錄檔中。 如需詳細資訊，請參閱 [自訂動作安全性](custom-action-security.md)。
-   自訂動作不能嘗試設定自訂動作內的系統還原進入點。 如需詳細資訊，請參閱 [設定自訂動作的還原點](setting-a-restore-point-from-a-custom-action.md)。
-   從自訂動作傳回錯誤訊息，並將它們寫入記錄檔，以協助疑難排解自訂動作。 如需詳細資訊，請參閱 [錯誤訊息自訂動作](error-message-custom-actions.md) 和 [從自訂動作傳回錯誤訊息](returning-error-messages-from-custom-actions.md)。
-   請勿變更來自立即自訂動作的系統狀態。 直接變更系統或呼叫另一個系統服務的自訂動作，必須延後至執行安裝腳本的時間。 變更系統狀態的每個 [順延強制自訂動作](deferred-execution-custom-actions.md) 之前都必須加上 [rollback 自訂動作](rollback-custom-actions.md) ，以復原安裝復原上的系統狀態變更。 如需詳細資訊，請參閱 [使用自訂動作變更系統狀態](changing-the-system-state-using-a-custom-action.md)。
-   執行複雜安裝作業的自訂動作應該是 [可執行檔](executable-files.md) 或 [動態連結程式庫](dynamic-link-libraries.md)。 根據 [腳本](scripts.md) ，將自訂動作的使用限制為簡單的安裝作業。
-   將您的自訂動作的詳細資料提供給系統管理員，方便探索到系統管理員。 將自訂動作所使用的登錄專案和檔案的詳細資料，放入自訂的資料表，並從這個資料表讀取自訂動作。 這是 [使用自訂動作在本機電腦上建立使用者帳戶](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)的範例所示範。 如需將自訂資料表加入至資料庫的詳細資訊，請參閱[使用 SQL 和腳本](examples-of-database-queries-using-sql-and-script.md)[處理查詢](working-with-queries.md)和資料庫查詢範例。
-   自訂動作不應顯示對話方塊。 需要使用者介面的自訂動作可以改用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 函數。 請參閱 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。
-   自訂動作不得使用頁面上所列的任何函式： [非自訂動作中使用](functions-not-for-use-in-custom-actions.md)的函式。
-   如果安裝是要在終端機伺服器上執行，請測試所有自訂動作都能在終端機伺服器上執行。 如需詳細資訊，請參閱 [**TerminalServer**](terminalserver.md) 屬性。
-   若要在卸載特定的修補程式時執行自訂動作，自訂動作必須存在於原始應用程式中，或者必須在永遠套用之產品的修補程式中。 如需詳細資訊，請參閱 [修補卸載自訂動作](patch-uninstall-custom-actions.md)。
-   自訂動作不應使用 UI 層級做為將錯誤訊息傳送至安裝程式的條件，因為這可能會干擾記錄和外部訊息。 如需詳細資訊，請參閱 [從自訂動作判斷 UI 層級](determining-ui-level-from-a-custom-action.md)。
-   使用條件陳述式和 [條件陳述式語法](conditional-statement-syntax.md) ，以確保您的封裝會正確執行自訂動作、不執行自訂動作，或在卸載套件時執行替代自訂動作。 測試套件在 [卸載自訂動作](uninstalling-custom-actions.md)時是否如預期般運作。 如需詳細資訊，請參閱 [移除時要執行的調節動作](conditioning-actions-to-run-during-removal.md)
-   如果安裝必須能夠由沒有系統管理員許可權的使用者執行，請進行測試以確保所有自訂動作都能以非系統管理員許可權執行。 自訂動作需要較高的許可權，才能修改系統中非特定使用者的部分。 如果正在安裝受管理的應用程式，或已針對較高的許可權指定系統原則，則安裝程式可能會以更高的許可權執行自訂動作。 需要提高許可權的任何自訂動作都必須在自訂動作類型中包含 msidbCustomActionTypeInScript 和 msidbCustomActionTypeNoImpersonate [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md) 。 這是 [使用自訂動作在本機電腦上建立使用者帳戶](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)的範例所示範。

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>如果您使用元件，請遵循良好的元件實務

如果您的套件使用軟體 [元件](assemblies.md)，請遵循將 [元件新增至套件](adding-assemblies-to-a-package.md)、 [更新元件](updating-assemblies.md)，以及 [安裝和移除元件](installing-and-removing-assemblies.md)的指導方針。

## <a name="do-not-ship-concurrent-installations"></a>請勿運送並行安裝。

[並行安裝](concurrent-installations.md)（也稱為嵌套安裝）會在目前執行的安裝期間安裝另一個 Windows Installer 套件。 使用並行安裝不是很好的作法，因為它們對客戶而言很難服務。 修補和升級可能無法搭配並行安裝使用。 使用並行安裝的建議替代方式是改為使用安裝應用程式和外部 UI 處理常式，依序安裝數個 Windows Installer 套件。

如需使用外部 UI 處理常式的詳細資訊，請參閱 [使用 MsiSetExternalUI 監視安裝](monitoring-an-installation-using-msisetexternalui.md)。 如需使用以記錄為基礎的外部處理常式的詳細資訊，請參閱 [使用 MsiSetExternalUIRecord 監視安裝](monitoring-an-installation-using-msisetexternaluirecord.md)。

在受控制的公司環境中，有時會使用並行安裝來安裝不適合公用的應用程式。 如果您決定要使用並行安裝，請遵循這些指導方針。

-   請勿使用並行安裝來安裝或更新出貨產品。
-   並行安裝不應共用元件。
-   系統管理安裝不應包含並行安裝。
-   整合式 ProgressBars 不應搭配並行安裝使用。
-   同時安裝不應安裝要通告的資源。
-   執行應用程式並行安裝的封裝，也應該在父產品卸載時卸載並行應用程式。 在主控台的 [新增/移除程式] 中，父產品的內容下會有嵌套的安裝。

## <a name="keep-package-names-and-package-codes-consistent"></a>讓套件名稱和套件碼保持一致。

.Msi 檔案可以提供任何有助於使用者識別封裝的名稱，但不應該變更該名稱，也不需要變更產品代碼。

-   為您的 .msi 檔案提供可讓使用者識別 Windows Installer 套件內容的易記名稱。
-   [產品代碼](product-codes.md)是應用程式的主體識別，且必須在應用程式的完整更新時變更。 如需詳細資訊，請參閱 [ [**ProductCode**](productcode.md) ] 和 [[變更產品代碼](changing-the-product-code.md)]。 變更應用程式 .msi 檔案的名稱會被視為完整的變更，而且一律需要對產品程式碼進行對應的變更，才能維持一致性。
-   [封裝程式碼](package-codes.md)是安裝程式用來搜尋並驗證指定安裝之正確封裝的主要識別碼。 沒有兩個 nonidentical .msi 檔案應該要有相同的套件程式碼。 如果在未變更套件程式碼的情況下變更套件，安裝程式仍可存取安裝程式時，安裝程式可能不會使用較新的套件。 封裝程式碼會儲存在 [摘要資訊資料流程](summary-information-stream.md)的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中。
-   請注意，產品代碼和套件程式碼 [guid](guid.md) 中的字母都必須全部都是大寫。

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>請勿使用 SelfReg 和 TypeLib 資料表。

-   強烈建議您不要使用自我註冊和 [SelfReg](selfreg-table.md) 資料表的安裝套件作者。 相反地，他們應該藉由在登錄 [資料表群組](registry-tables-group.md)中撰寫一或多個資料表來註冊模組。 由於自我註冊常式通常會隱藏重要的設定資訊，因此 Windows Installer 的許多優點會因為自我註冊而遺失。 如需避免自行註冊的原因清單，請參閱 [SelfReg 資料表](selfreg-table.md)。
-   使用 [TypeLib](typelib-table.md) 資料表時，強烈建議使用安裝套件作者。 使用登錄資料表來註冊類型程式庫，而不是 [使用 TypeLib](registry-table.md) 資料表。 如果使用 TypeLib 資料表的安裝失敗，而且必須回復，則回復可能不會將電腦還原到復原之前存在的相同狀態。

## <a name="provide-the-option-to-install-without-a-user-interface"></a>提供在沒有使用者介面的情況下安裝的選項。

系統管理員通常偏好在公司內部部署應用程式，而不需要使用者互動。 最好的作法是讓您的應用程式提供選項，讓 [使用者介面層級](user-interface-levels.md) 為 [無]。

-   使用 [公用屬性](public-properties.md) 來取得設定資訊。 系統管理員可以在命令列上提供此資訊。
-   不需要安裝取決於使用者與對話方塊的互動所搜集的資訊。 無訊息安裝期間無法使用這項資訊。
-   請勿在無訊息安裝期間自動重新開機使用者的電腦。
-   系統管理員可以使用[命令列選項](command-line-options.md)"/q"，在安裝時設定[使用者介面層級](user-interface-levels.md)。 您也可以使用呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)，以程式設計方式設定使用者介面層級。

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>避免使用 AlwaysInstallElevated 原則。

如果未設定 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則，系統會使用使用者的許可權來安裝未由系統管理員散發的應用程式，而且只有受管理的應用程式才會取得較高的許可權。 設定此原則會指示 Windows Installer 在系統上安裝應用程式時使用系統許可權。 這種方法可以開啟電腦的安全性風險，因為當設定此原則時，非系統管理員的使用者可以使用較 [*高*](e-gly.md) 的許可權執行安裝，並存取電腦上的安全位置。 以 [較高的許可權安裝具有非系統管理員](installing-a-package-with-elevated-privileges-for-a-non-admin.md) 或 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)的套件時，最好使用其他方法，而不是 AlwaysInstallElevated 原則。

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>啟用 DisableMedia 原則以限制未經授權的安裝。

[DisableMedia](disablemedia.md)原則可防止未經授權的應用程式安裝。 啟用此原則時，執行一項產品維護安裝的使用者和系統管理員，將無法使用 [流覽] 對話方塊來流覽媒體來源（例如 CD-ROM），以取得其他可安裝產品的來源。 無論是否以較高的許可權進行安裝，都會防止流覽其他產品。 如果使用者已正確標示媒體來源，則使用者仍然可以從媒體重新安裝產品。

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>將原始套件來源檔案保持安全並可供使用者使用。

在某些情況下，可能需要 Windows Installer 套件的原始來源，才能視需要安裝、修復或更新應用程式。 如果安裝程式找不到可用的來源，系統會要求使用者提供媒體或移至包含所需來源的網路位置。 確定安裝程式具有所需的來源，而不需要提示使用者，是很好的作法。

-   使用 [數位簽章和外部封包](digital-signatures-and-external-cabinet-files.md) 檔，以確保安裝程式所使用的 origial 來源是安全的。 儲存在公用位置的未壓縮來源映射不安全。
-   在 [**SOURCELIST**](sourcelist.md) 屬性中包含應用程式安裝套件之網路或 URL 來源路徑的完整清單。
-   針對來源路徑使用分散式檔案系統 (DFS) 共用。
-   使用 Windows Installer API 來取得和修改 Windows Installer 應用程式和修補程式的來源清單資訊。 如需詳細資訊，請參閱 [管理安裝來源](managing-installation-sources.md)。
-   您可以使用 [**安裝程式物件**](installer-object.md)、 [**Product 物件**](product-object.md)和 [**Patch 物件**](patch-object.md) 的方法和屬性，來取得和修改 Windows Installer 應用程式和修補程式的來源清單資訊。
-   遵循所列的， [防止修補程式要求存取原始安裝來源](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) 點，以將修補程式需要存取原始來源的可能性降至最低。
-   將套件來源檔案儲存在非系統暫存資料夾的位置。 儲存在暫存資料夾中的 Windows Installer 原始檔可能會變成無法供使用者使用。

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>針對部署進行疑難排解時，請在使用者的電腦上啟用詳細資訊記錄。

[Windows Installer 記錄](windows-installer-logging.md) 包含可在使用者電腦上啟用的詳細資訊記錄選項。 當您嘗試針對 Windows Installer 套件部署進行疑難排解時，詳細資訊記錄檔中的資訊可能很有説明。

-   您可以使用 [命令列選項](command-line-options.md)、 [**MsiLogging**](msilogging.md) 屬性、 [記錄原則](logging.md)、 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)和 [**EnableLog**](installer-enablelog.md) 方法，在使用者的電腦上啟用詳細資訊記錄。
-   有一項非常實用的資源可解讀 Windows Installer 的記錄檔 [Wilogutl.exe](wilogutl-exe.md)。 這項工具可協助分析記錄檔，並顯示在記錄檔中找到之錯誤的建議解決方案。
-   如需有關解讀 Windows Installer 記錄檔的詳細資訊，請參閱 TechNet 網站上提供的白皮書： [Windows Installer：系統管理員的權益和實行](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx)。
-   詳細資訊記錄選項應該僅用於疑難排解用途，不應該保持開啟，因為它可能會對系統效能和磁碟空間造成負面影響。 每次您使用主控台中的 [新增/移除程式] 工具時，都會建立新的檔案。

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>卸載會將使用者的電腦保持在乾淨的狀態。

應用程式的移除就像安裝一樣重要。 卸載 Windows Installer 套件時，不會在使用者的電腦上留下任何無用的部分。

-   如果在執行卸載之後，必須從使用者的電腦中移除的檔案仍已安裝，則安裝程式可能不會移除包含檔案的元件，原因是 [移除擱置](removing-stranded-files.md)的檔案中所述的一或多個原因。
-   如果必須註冊應用程式，請在卸載應用程式時撰寫套件以移除登錄資訊。 如需相關資訊，請參閱在 [安裝或移除元件時新增或移除登錄機碼](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)。 如果未註冊應用程式，則應用程式不會列在主控台的 [新增或移除程式] 功能中，也無法使用 Windows Installer 來管理。
-   若要從主控台中的 [新增或移除程式] 功能隱藏應用程式，且仍然能夠使用 Windows Installer 來管理應用程式，請遵循新增和移除應用程式中所述的指導方針， [並在登錄中保留沒有追蹤](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)。
-   自訂動作應受條件地執行，而不需要在卸載時執行。 安裝和卸載時，可能需要執行不同的自訂動作。
-   使用者特定的自訂資訊可以儲存在電腦的文字檔中。 這樣做的優點是，當應用程式卸載時可以移除檔案，即使這個自訂的使用者目前未登入也一樣。

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>針對每位使用者和每部電腦的安裝部署測試套件。

最好的作法是讓客戶決定是否要在每部電腦或每一使用者的 [安裝內容](installation-context.md)中部署套件以進行安裝。

-   請考慮應用程式是否應該僅供特定使用者或電腦的所有使用者使用，在開發過程中。
-   測試套件是否可針對每個使用者安裝和個別電腦的安裝內容正確運作。
-   使套件易於自訂，並讓客戶決定是否要將它部署為每位使用者或每部電腦。

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>先規劃及測試服務策略，再寄送應用程式。

第一次部署應用程式之前，您應該先決定要如何為應用程式提供服務。

-   請考慮未來您預期用來服務應用程式的更新類型。 Windows Installer 提供三種類型的更新： [小型更新](small-updates.md)、 [次要升級](minor-upgrades.md)和 [主要升級](major-upgrades.md)。 [修補和升級](patching-and-upgrades.md)主題將說明這些差異。
-   在交付您的應用程式之前，請先測試它在使用每個更新類型進行服務之後是否能正常運作。

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>在原始來源上減少更新的相依性。

如果需要原始來源檔案來更新您的應用程式，這可能會讓應用程式的服務變得更困難。 下列方法可協助減少原始來源的更新相依性。

-   使用 [*差異修補*](d-gly.md) 程式來更新應用程式的基準版本，例如 RTM 版本和 service pack 版本。 遵循主題： [減少修補程式大小](reducing-patch-size.md)中所述之差異修補程式的使用指導方針。
-   遵循主題中所列的建議： [防止 Patch 要求存取原始安裝來源](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)。

## <a name="do-not-distribute-unserviceable-merge-modules"></a>請勿散發 unserviceable 合併模組。

如果合併模組的擁有者和應用程式的擁有者不同，則應用程式不應該相依于安裝元件的 [合併模組](merge-modules.md) 。 這可能會讓應用程式變得很困難，因為這兩個擁有者都需要協調以更新應用程式或模組。 如果不知道已使用合併模組的所有應用程式，應用程式的擁有者就無法更新合併模組，而且不會有風險，因為更新可能與其他應用程式不相容。 合併模組的擁有者沒有直接的方法可更新已安裝合併模組的 Windows Installer 封裝。

-   請考慮為使用者提供所需的元件，因為另一個 Windows Installer 安裝。

## <a name="avoid-patching-administrative-installations"></a>避免修補系統管理安裝。

在網路上提供應用程式原始 Windows Installer 套件的 [系統管理安裝](administrative-installation.md) ，讓工作組的成員可以安裝應用程式。 然後，這個系統管理映射的使用者應該將更新套用到位於其電腦上的應用程式的本機實例。 這樣可讓使用者與系統管理映射保持同步。 基於下列原因，不建議將更新套用至管理安裝。

-   相較于下載修補程式，使用者取得更新所需的下載大小和延遲會增加。 整個更新後的 Windows Installer 套件和來源檔案必須下載、recached 和重新安裝。
-   使用者在重新緩存並重新安裝應用程式之前，無法 [視需要安裝](installation-on-demand.md) 和修復更新的系統管理安裝中的應用程式。
-   將修補程式套用至系統管理安裝時，會從套件中移除數位簽章。 系統管理員必須重新簽署封裝。 如需有關使用數位簽章的詳細資訊，請參閱 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)。
-   許多二進位修補程式都是以應用程式的 RTM 映射為目標，而且需要先前的檔案版本。 從更新的系統管理安裝所安裝之應用程式的本機實例可能不適用於其他更新。 許多二進位修補程式應用程式可能會失敗。
-   將修補程式套用至系統管理安裝會更新來源檔案和 .msi 檔案，但不會使用更新的相關資訊來戳記網路映射。 使用者無法判斷他們從系統管理安裝所收到的更新。 如此一來，在使用者端套用的更新順序將會套用至已套用於系統管理映射端的更新。
-   套用至系統管理安裝的修補程式不是 [可卸載修補程式](uninstallable-patches.md)。 這可防止使用者電腦上快取的套件程式碼與系統管理安裝上的套件程式碼不同。 如果使用者電腦上快取的套件程式碼與系統管理安裝上的不同，請從系統管理安裝重新安裝該應用程式，然後再修補用戶端電腦。
-   如果您決定透過修補系統管理映射來套用小型更新，請依照主題中所述的指導方針： [修補系統管理映射以套用 Small update](applying-small-updates-by-patching-an-administrative-image.md)。

## <a name="register-updates-to-run-with-elevated-privilege"></a>以較高的許可權註冊更新以執行。

從 Windows Installer 3.0 開始，在修補程式註冊為具有更高的許可權之後，就可以將修補程式套用至每個使用者管理內容中已安裝的應用程式。 您無法使用3.0 版之前的 Windows Installer 版本，將修補程式套用至每個使用者管理內容中安裝的應用程式。

-   使用 [**SourceListAddSource**](patch-sourcelistaddsource.md) 方法或 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) 函式，以較高的許可權註冊 patch 套件。 遵循在 [修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)中所提供的指導方針與範例。
-   在 Windows Vista 上執行 Windows Installer 4.0 版時，您也可以使用 [ [使用者帳戶控制] (UAC) 修補](user-account-control--uac--patching.md) 程式，讓 Windows Installer 安裝的作者找出可由非系統管理員使用者未來套用的數位簽章修補程式。 這僅適用于在個別電腦 [安裝內容](installation-context.md) 中安裝套件 (ALLUSERS = 1) 。
-   藉由設定 [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) 屬性或 [DisableLUAPatching](disableluapatching.md) 原則，確保未停用最低許可權修補。

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>使用 MsiPatchSequence 資料表來排列修補程式的順序。

在您的封裝中包含 [MsiPatchSequence 資料表](msipatchsequence-table.md) ，並新增修補程式排序資訊。 從 Windows Installer 版本3.0 開始，安裝程式可以在 [安裝多個修補](installing-multiple-patches.md) 程式時使用 MsiPatchSequence 資料表，以判斷最佳的修補程式應用程式順序。 使用 [Windows Installer 3.0 版白皮書中的修補程式順序中](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) 所述的指導方針來定義修補程式系列。

-   如果可行的話，請將所有修補程式指定為屬於單一修補程式系列。 在許多情況下，單一修補程式系列提供足夠的彈性來排列修補程式。 使用多個修補程式系列時，撰寫的複雜度會增加。 為修補程式系列指派有意義的名稱，並在該修補程式系列中指派隨時間增加的順序值。 遵循 [多重修補範例](multiple-patching-example.md) ，依照發行修補程式的順序套用修補程式。
-   使用[Patchwiz.dll](patchwiz-dll.md)中的[PatchSequence 資料表](patchsequence-table--patchwiz-dll-.md)來產生[MsiPatchSequence 資料表](msipatchsequence-table.md)中的資訊。 使用 Windows Installer 3.0 發行的 PATCHWIZ.DLL 版本可以自動產生修補程式排序資訊。 如需有關如何新增修補程式的詳細資訊，請參閱 [產生修補程式順序資訊](generating-patch-sequence-information---patchwiz-dll-.md)。 如需修補程式排序案例的詳細資訊，請參閱白皮書： [Windows Installer 版本3.0 中的修補程式順序](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3)。

## <a name="test-the-installation-package-thoroughly"></a>徹底測試安裝套件。

測試您的 Windows Installer 套件是否正確安裝、修復和移除。 您可以將測試程式分成下列部分。

-   安裝測試-使用所有可能的應用程式功能組合來測試安裝。 測試所有類型的安裝，包括系統 [管理安裝](administrative-installation.md)、 [復原安裝](rollback-installation.md)和 [隨選安裝](installation-on-demand.md)。 嘗試安裝的所有可能方法，包括按一下 .msi 檔案、 [命令列選項](command-line-options.md)，以及從 [控制台] 進行安裝。 測試封裝是否可由使用者在所有可能的許可權內容中進行安裝。 在所有可能的方法部署套件之後，請嘗試安裝該套件。 啟用每個測試的 [Windows Installer 記錄](windows-installer-logging.md) ，並解決安裝程式記錄檔和事件記錄檔中找到的所有錯誤。
-   消費者介面測試-以所有可能的 [使用者介面層級](user-interface-levels.md)安裝時測試封裝。 測試安裝的套件不含使用者介面，以及透過使用者介面提供的所有資訊。 確定使用者介面的 [存取](accessibility.md) 範圍，以及使用者介面如預期般針對不同的螢幕解析度和字型大小運作。
-   服務和修復測試-測試封裝是否可以處理[小型更新](small-updates.md)、[次要升級](minor-upgrades.md)和[主要升級](major-upgrades.md)所提供的[修補和升級](patching-and-upgrades.md)。 在部署套件之前，請先撰寫每個類型的試用更新，並嘗試將它套用至原始套件。
-   卸載測試-確認移除套件時，不會在使用者的電腦上留下無用的部分，而且只會移除屬於封裝的資訊。 卸載封裝之後，請重新開機測試電腦，並確認通用系統工具和其他標準應用程式的完整性。 測試封裝是否可由使用者在所有可能的許可權內容中移除。 測試所有方法以移除封裝，按一下 .msi 檔案，嘗試 [命令列選項](command-line-options.md)，然後嘗試從 [控制台] 移除套件。 啟用每個測試的 [Windows Installer 記錄](windows-installer-logging.md) ，並解決安裝程式記錄檔和事件記錄檔中找到的所有錯誤。
-   產品功能測試-確保應用程式在安裝、修復或移除套件之後如預期般運作。

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>請先修正所有驗證錯誤，再部署新的或修改過的安裝套件。

先在新的或修改過的 Windows Installer 封裝上執行 [套件驗證](package-validation.md) ，再嘗試第一次安裝。 驗證會檢查 Windows Installer 資料庫是否有撰寫錯誤。 嘗試安裝未通過驗證的封裝可能會損毀使用者的系統。

-   您可以使用 [Orca.exe](orca-exe.md) 或 [Msival2.exe](msival2-exe.md)來驗證您的封裝。 這兩種工具都隨附于 Windows SDK。 協力廠商也可以將 ICE 驗證系統納入其撰寫環境中。
-   您可以使用 SDK 隨附的 .cub 檔中所包含的一組標準 [內部一致性評估](internal-consistency-evaluators-ices.md) 工具，或藉由 [建立 ICE](building-an-ice.md) 並將其新增至 .cub 檔案來自訂驗證。
-   您可以使用 Evalcom2.dll 來執行安裝封裝和合併模組的 [驗證自動化](validation-automation.md) 。

## <a name="author-a-secure-installation"></a>撰寫安全的安裝。

開發封裝時，請遵循這些指導方針，以協助在安裝期間維護安全的環境。

-   [撰寫安全安裝的指導方針](guidelines-for-authoring-secure-installations.md)
-   [在鎖定的電腦上保護套件安全的指導方針](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>使用 PMSIHANDLE 而非控制碼

**PMSIHANDLE** 類型變數是在 msi 中定義。 建議您的應用程式使用 **PMSIHANDLE** 類型，因為安裝程式會在超出範圍時關閉 **PMSIHANDLE** 物件，而您的應用程式必須藉由呼叫 [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)來關閉 **MSIHANDLE** 物件。

例如，如果您使用如下所示的程式碼：

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

將它變更為：

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 

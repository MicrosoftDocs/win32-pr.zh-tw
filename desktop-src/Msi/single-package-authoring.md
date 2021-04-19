---
description: 雙用途套件是一種 Windows Installer 5.0 套件，其撰寫目的是要能夠在每位使用者或每部電腦的安裝內容中安裝應用程式。
ms.assetid: b2da9fba-8fdf-48fa-a662-6b3eee1bfe87
title: 單一套件撰寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c22b9be930be2d2178ea4efb7ba1538320823a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000147"
---
# <a name="single-package-authoring"></a>單一套件撰寫

雙用途套件是一種 Windows Installer 5.0 套件，其撰寫目的是要能夠在每位使用者或每部電腦的 [安裝內容](installation-context.md)中安裝應用程式。 針對其應用程式使用雙重用途套件的設定開發人員，可以在安裝期間提供使用者選擇安裝內容，並可從 Windows 7 或 Windows Server 2008 R2 上的個別使用者安裝移除 UAC 認證提示。 在 Windows 7 和 Windows Server 2008 R2 上進行安裝的雙用途 Windows Installer 5.0 套件開發，稱為單一套件撰寫。

您可以開始開發 Windows 7 和 Windows Server 2008 R2 的雙重用途套件，方法是使用 Windows Installer 5.0、 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性、 [**ALLUSERS**](allusers.md) 屬性，以及適用于 [windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85))的每個使用者已知資料夾和註冊。 當 Windows Installer 5.0 將雙用途套件安裝在 Windows 7 或 Windows Server 2008 R2 上的每個使用者內容時，安裝程式會將檔案和登錄專案導向至每個使用者的位置，而不會顯示 UAC 提示以取得認證。 當 Windows Installer 5.0 將雙用途套件安裝在每部電腦的內容中時，安裝程式會將檔案和登錄專案導向至各電腦的位置，並提示您輸入 UAC 認證，以確認使用者有足夠的許可權可以為電腦的所有使用者安裝軟體。 一旦 Windows Installer 5.0 安裝應用程式，它就會針對應用程式的所有後續更新、修復或移除，使用相同的安裝內容。

**[Windows Installer 4.5 或更早](not-supported-in-windows-installer-4-5.md)版本：** 不支援 [**ProgramFilesFolder**](programfilesfolder.md)、 [**CommonFilesFolder**](commonfilesfolder.md)、 [**ProgramFiles64Folder**](programfiles64folder.md)和 [**CommonFiles64Folder**](commonfiles64folder.md)屬性所參考的 [**MSIINSTALLPERUSER**](msiinstallperuser.md)屬性和每個使用者版本的資料夾。 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用 **FOLDERID \_ UserProgramFiles** 和 **FOLDERID \_ UserProgramFilesCommon** 資料夾。 這表示針對 Windows Installer 4.5 或舊版的直接檔案和登錄專案所開發的安裝，可 FOLDERID \_ ProgramFiles、FOLDERID \_ PROGRAMFILESCOMMON、FOLDERID \_ ProgramFilesX64 和 FOLDERID \_ ProgramFilesCommonX64。 因為這些是電腦的其他使用者可存取的位置，所以 Windows Vista 和更新版本的系統需要顯示 UAC 提示以取得認證。

當使用者安裝針對 Windows Installer 5.0 （使用 Windows Installer 4.5 或更早版本）撰寫的雙重用途套件時，安裝程式會忽略 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性。 在此情況下，安裝可以將檔案和登錄專案導向可供其他使用者存取的位置，並要求系統顯示 UAC 提示以取得認證。 Windows Installer 5.0 可以安裝為 Windows Installer 4.5 或更早版本所開發的封裝，但安裝會將檔案和登錄專案導向其他使用者可存取的位置，並且要求系統顯示 UAC 提示以取得認證。

## <a name="development-guidelines"></a>開發指導方針

遵循下列單一套件撰寫指導方針，以確保封裝可以安裝在每個使用者或每一電腦的內容中。 遵循這些指導方針，讓使用者在安裝時可以選擇每位使用者或每部電腦的安裝，並從每個使用者的安裝中移除 UAC 提示。

-   在 Windows 7 或 Windows Server 2008 R2 上，每位使用者的安裝需要 Windows Installer 5.0。 您應通知使用者套件支援在舊版系統上安裝應用程式的每一電腦。
-   在您的雙重用途封裝的 [屬性工作表](property-table.md)中，初始化 [**ALLUSERS**](allusers.md)和 [**MSIINSTALLPERUSER**](msiinstallperuser.md)屬性的值。 將 **ALLUSERS** 值2和 **MSIINSTALLPERUSER** 值1作為初始值。 這會將每個使用者安裝指定為雙用途套件的預設值。
-   請考慮為您的雙重用途封裝的 [使用者介面](user-interface.md) 撰寫一個對話方塊，讓使用者在安裝時選擇內容。 撰寫這個自訂對話方塊上的控制項，以設定 [**ALLUSERS**](allusers.md) 和 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值。 如果 **ALLUSERS** 值為2，請將 **MSIINSTALLPERUSER** 設定為1的值以指定每位使用者安裝，並將 **MSIINSTALLPERUSER** 設為空字串 ( "" ) 來指定每部電腦安裝。 如果使用者從命令列安裝封裝，也可以在命令列上設定 **ALLUSERS** 和 **MSIINSTALLPERUSER** 。
-   使用 [內部一致性評估](internal-consistency-evaluators-ices.md)工具驗證套件-ices-003 封裝必須能夠透過 [ICE105](ice-105.md) 傳遞驗證，才能成為有效的雙重用途套件。
-   使用登錄 [資料表](registry-table.md) 和 [RemoveRegistry 資料表](removeregistry-table.md) ，將登錄專案重新導向至每個使用者安裝期間的登錄個別使用者部分。 在每一使用者安裝中，會將根欄位中具有-1 的登錄專案重新導向至 **HKEY \_ 目前的 \_ 使用者**，而在個別電腦安裝中，這些專案會導向至 **HKEY \_ 本機 \_ 電腦**。 在每一使用者安裝中，會將根資料行中具有 msidbRegistryRootClassesRoot (0) 的登錄專案重新導向至 **HKCU** \\ **software** \\ **類別**，而在個別電腦安裝中，這些專案會導向至 **HKLM** \\ **軟體** \\ **類別**。
-   使用 [32 位 Windows Installer 套件](32-bit-windows-installer-packages.md)的 [目錄資料表](directory-table.md)中的 [ [**ProgramFilesFolder**](programfilesfolder.md) ] 屬性，指定包含32位元件的目錄位置，而不是跨應用程式共用。 當使用者使用每部電腦內容安裝雙重用途套件時，這些元件會儲存在32位版 Windows 的 Program Files 資料夾中，以及在64位版系統上的 Program Files (x86) 資料夾中。 所有使用者都可以存取這些目錄中的元件。 當使用者使用每一使用者內容在 Windows 7 或 Windows Server 2008 R2 上安裝雙重用途套件時，這些元件會儲存在目前使用者的 [程式] 資料夾中 (例如，在% LocalAppData% \\ 程式) ，而且只能由該使用者存取。
-   使用 [32 位 Windows Installer 套件](32-bit-windows-installer-packages.md)的 [目錄資料表](directory-table.md)中的 [ [**CommonFilesFolder**](commonfilesfolder.md) ] 屬性，指定包含跨應用程式共用之32位元件的目錄位置。 當使用者使用每部電腦的內容安裝雙重用途套件時，這些元件會儲存在 [一般檔案] 資料夾中，而且可供所有使用者存取。 當使用者使用每一使用者內容在 Windows 7 或 Windows Server 2008 R2 上安裝雙重用途套件時，這些元件會儲存在目前使用者的通用資料夾 (例如，在% LocalAppData% \\ 程式 \\ 一般) ，而且只能由該使用者存取。
-   使用 [64 位 Windows Installer 套件](64-bit-windows-installer-packages.md)的 [目錄資料表](directory-table.md)中的 [ [**ProgramFiles64Folder**](programfiles64folder.md) ] 屬性，指定包含64位元件的目錄位置，而不是跨應用程式共用。 當使用者使用每部電腦的內容安裝雙重用途套件時，這些元件會儲存在 [Program Files] 資料夾中。 所有使用者都可以存取這些目錄中的元件。 當使用者使用每一使用者內容在 Windows 7 或 Windows Server 2008 R2 上安裝雙重用途套件時，這些元件會儲存在目前使用者的 [程式] 資料夾中 (例如，在% LocalAppData% \\ 程式) ，而且只能由該使用者存取。 如需有關撰寫套件以在64位作業系統上安裝應用程式的詳細資訊，請參閱 [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)。
-   使用 [64 位 Windows Installer 套件](64-bit-windows-installer-packages.md)的 [目錄資料表](directory-table.md)中的 [ [**CommonFiles64Folder**](commonfiles64folder.md) ] 屬性，指定包含跨應用程式共用之64位元件的目錄位置。 當使用者使用每部電腦的內容安裝雙重用途套件時，這些元件會儲存在 [一般檔案] 資料夾中，而且可供所有使用者存取。 當使用者使用每一使用者內容在 Windows 7 或 Windows Server 2008 R2 上安裝雙重用途套件時，這些元件會儲存在目前使用者的通用資料夾 (例如，在% LocalAppData% \\ 程式 \\ 一般) ，而且只能由該使用者存取。
-   使用 [64 位 Windows Installer 封裝](64-bit-windows-installer-packages.md)的 [目錄資料表](directory-table.md)中的 [**ProgramFilesFolder**](programfilesfolder.md)和 [**CommonFilesFolder**](commonfilesfolder.md)屬性來指定包含32位元件的目錄位置。 針對使用相同名稱提供之任何元件的32位和64位版本，請使用不同的名稱，或者將版本儲存在不同的資料夾中。 例如，將資訊新增至目錄資料表，以將包含32位版本的目錄位置指定為 \[ ProgramFilesFolder \] \\ *isv name* \\ *application name* \\ x86，以及包含64位版本的目錄位置（ \[ Program64FilesFolder \] \\ *ISV name* \\ *application name* \\ x64）。 每一部電腦的安裝，接著會將32位版本儲存在 program files (x86) \\ *ISV name* \\ *application name* \\ x86，然後將64位版本儲存在 program files \\ *isv 名稱* \\ *應用程式名稱* \\ x64 中。 每一使用者的安裝會將32位版本儲存在% LocalAppData% \\ 程式 \\ *isv name* \\ *應用程式名稱* \\ x86 中，並在% LocalAppData% \\ 程式 \\ *isv 名稱* \\ *應用程式名稱* x64 中安裝64位版本 \\ 。
-   在 \\ 使用者使用者 \\ *名稱* AppData 下，儲存應用程式的每位使用者設定資料 \\ 。
-   將應用程式所產生的範本和檔案儲存在 [ \\ 使用者 \\ *名稱*] 底下的子資料夾中。
-   如果您的應用程式使用 shell 擴充功能，您應該使用從 Windows 7 或 Windows Server 2008 R2 開始提供的每一使用者的 [shell](https://msdn.microsoft.com/library/bb762762.aspx) 擴充點。
-   請勿在需要提高許可權的封裝中使用自訂動作來執行。 [CustomAction](customaction-table.md)資料表不應該包含已標示為以較高許可權執行的自訂動作。 如需更高的自訂動作的詳細資訊，請參閱 [自訂動作安全性](custom-action-security.md)。
-   請勿寫入任何全域系統資料夾中。 [目錄](directory-table.md)資料表不應包含下列任何系統資料夾屬性的參考。

    <dl>

[**AdminToolsFolder**](admintoolsfolder.md)  
    [**CommonAppDataFolder**](commonappdatafolder.md)  
    [**FontsFolder**](fontsfolder.md)  
    [**System16Folder**](system16folder.md)  
    [**System64Folder**](system64folder.md)  
    [**SystemFolder**](systemfolder.md)  
    [**TempFolder**](tempfolder.md)  
    [**WindowsFolder**](windowsfolder.md)  
    [**WindowsVolume**](windowsvolume.md)  
    </dl>

-   請勿將通用語言執行平臺元件安裝到全域組件快取 (GAC 中 ) 。如需有關將元件安裝到全域組件快取的詳細資訊，請參閱 [將元件加入封裝](adding-assemblies-to-a-package.md) 和 [安裝 Common language runtime 元件](installation-of-common-language-runtime-assemblies.md)。
-   請勿安裝任何 ODBC 資料來源。 請勿使用 [ODBCDataSource](odbcdatasource-table.md) 資料表來安裝資料來源。
-   請勿安裝任何服務。 請勿使用 [ServiceInstall](serviceinstall-table.md) 資料表來安裝服務。

## <a name="example"></a>範例

[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了雙用途封裝的範例，做為檔 PUASample1.msi。 如果您有最新的 SDK，則可以存取重現範例安裝套件所需的所有工具和資料。 如需此範例的詳細資訊，請參閱 [單一套件撰寫範例](single-package-authoring-example.md)。

 

 

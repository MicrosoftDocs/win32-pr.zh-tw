---
description: 範例 PUASample.msi 是可安裝在 Windows Server 2008 R2 和 Windows 7 上個別使用者或每部電腦安裝內容中的雙重用途 Windows Installer 5.0 封裝的範例。
ms.assetid: be018e8a-ca5f-4135-a019-970ec4173f23
title: 單一套件撰寫範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0ed56b8d7aaf8793416ba3ecab24c1f2a48ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000148"
---
# <a name="single-package-authoring-example"></a>單一套件撰寫範例

範例 PUASample.msi 是可安裝在 Windows Server 2008 R2 和 Windows 7 上個別使用者或每部電腦 [安裝內容](installation-context.md) 中的雙重用途 Windows Installer 5.0 封裝的範例。 此範例套件遵循 [單一封裝撰寫](single-package-authoring.md)中所述的開發指導方針。

## <a name="obtaining-a-copy-of-the-sample"></a>取得範例的複本

此範例的複本和 Windows Installer 資料庫資料表編輯器（Orca.exe）都在 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中。 範例和資料表編輯器隨附于 Windows Server 2008 R2 和 Windows 7 的 Windows 軟體開發套件，作為 Windows Installer 安裝檔案 PUASample1.msi 和 Orca.msi。

## <a name="system-requirements"></a>系統需求

資料庫編輯器（ [Orca.exe](orca-exe.md)）需要 Windows Server 2008 R2 和更早版本以及 windows 7 及更早版本。 雙用途封裝（PUASample1.msi）可以安裝在 Windows Server 2008 R2 和 Windows 7 上的每部電腦或每一使用者的 [安裝內容](installation-context.md) 中。 PUASample1.msi 只能安裝在 Windows Server 2008 及更早版本以及 Windows Vista 及更早版本的個別電腦內容中。 您可以安裝資料庫編輯器來檢查 PUASample1.msi 的內容，而不需要安裝範例。 若要安裝範例或編輯器套件，請確定 [DisableMSI](disablemsi.md) 原則未設定為封鎖應用程式安裝的值。

## <a name="identifying-a-dual-purpose-package"></a>識別 Dual-Purpose 套件

雙用途封裝應該將 [**MSIINSTALLPERUSER**](msiinstallperuser.md) 屬性的值初始化為1。 這會將套件識別為可安裝在 Windows Server 2008 R2 和 Windows 7 上的每部電腦或每一使用者內容中。 只有在撰寫 [單一套件](single-package-authoring.md)時所述的開發指導方針，以及您想要為使用者提供可選擇在每個使用者或每一電腦的內容中安裝封裝的選項時，才在封裝中設定 **MSIINSTALLPERUSER** 屬性。 雙用途封裝也應該將 [**ALLUSERS**](allusers.md) 屬性的值初始化為2。 這會將每位使用者指定為應用程式的預設安裝內容。 如果 **ALLUSERS** 屬性的值是2以外的任何值，Windows Installer 會忽略 **MSIINSTALLPERUSER** 屬性。

使用 Windows Installer 資料庫編輯器（例如 [Orca.exe](orca-exe.md)）來檢查 PUASample1.msi 的內容。 範例封裝中的 [屬性](property-table.md) 表包含下列兩個專案。

[屬性](property-table.md) 資料表 (部分) 

| 屬性          | 值 |
|-------------------|-------|
| ALLUSERS          | 2     |
| MSIINSTALLPERUSER | 1     |



 

## <a name="custom-dialog-box-for-installation-context"></a>安裝內容的自訂對話方塊

範例套件的 [使用者介面](user-interface.md) 包含自訂對話方塊 VerifyReadyDialog 的範例，可讓使用者在安裝時選取每位使用者或每部電腦的安裝內容。 [對話方塊](dialog-table.md)資料表包含描述 VerifyReadyDialog 對話方塊的記錄。 在 [屬性] 欄位中輸入的值為39，因為此對話方塊使用 msidbDialogAttributesVisible (1) 、msidbDialogAttributesModal (2) 、msidbDialogAttributesMinimize (4) 和 msidbDialogAttributesTrackDiskSpace (32) [對話方塊樣式位](dialog-style-bits.md)。 對話方塊的標題列會顯示 [ [**ProductName**](productname.md) ] 屬性值所提供的標題。

[對話方塊](dialog-table.md) 資料表 (部分)  

| 對話            | HCentering | VCentering | 寬度 | 高度 | 屬性 | 標題           | \_先控制項 | 控制項 \_ 預設值 | 控制 \_ 取消 |
|-------------------|------------|------------|-------|--------|------------|-----------------|----------------|------------------|-----------------|
| VerifyReadyDialog | 50         | 50         | 480   | 280    | 39         | \[ProductName\] | InstallPerUser | 下一個             | 取消          |



 

[控制](control-table.md)表格包含 [VerifyReadyDialog] 對話方塊所顯示的[控制項](controls.md)專案。 對話方塊會顯示 [按鈕](pushbutton-control.md) 控制項和 [文字](text-control.md) 控制項。 所有控制項都使用 msidbControlAttributesEnabled (2) ，而 msidbControlAttributesVisible (1) [控制項屬性](control-attributes.md)。 InstallPerMachine 控制項也會使用 [ElevationShield](elevationshield-attribute.md) 控制項屬性 msidbControlAttributesElevationShield (8388608。 ) 此控制項屬性會將 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 提高許可權圖示 (至 InstallPerMachine 控制項，並通知使用者必須要有 uac 認證，才能將應用程式安裝在每部電腦的內容中。 控制資料表文字欄位中的值是控制項所顯示的文字樣式和文字。 如需使用預先定義樣式將文字新增至控制項的詳細資訊，請參閱控制資料表主題中文字欄位的描述。

[控制項](control-table.md) 資料表 (部分) 

| 對話\_          | 控制           | 類型       | 屬性 | Text                                                   | 控制 \_ 下一步     |
|-------------------|-------------------|------------|-----------|--------------------------------------------------------|-------------------|
| VerifyReadyDialog | 取消            | 按鈕 | 3         | { \\ Tahoma10} &取消                                    | 下一個              |
| VerifyReadyDialog | 上一個          | 按鈕 | 3         | { \\ Tahoma10} <<&上一個                          | 取消            |
| VerifyReadyDialog | 下一個              | 按鈕 | 3         | { \\ Tahoma10} &下一個 >>                             | InstallPerUser    |
| VerifyReadyDialog | Text2             | Text       | 3         | 您是否準備好完成暫停的安裝？ |                   |
| VerifyReadyDialog | InstallPerUser    | 按鈕 | 3         | { \\ Tahoma10} 僅針對 &我安裝                       | InstallPerMachine |
| VerifyReadyDialog | InstallPerMachine | 按鈕 | 8388611   | { \\ Tahoma10} 為每個人 &安裝                      | 上一個          |
| VerifyReadyDialog | 取消            | 按鈕 | 3         | { \\ Tahoma10} &取消                                    | 下一個              |



 

[ControlEvent](controlevent-table.md)資料表會指定使用者與控制項互動時，安裝程式所執行的[事件](control-events.md)（或動作）。 當使用者啟動 InstallPerUser 按鈕時，如果 [**OutOfDiskSpace**](outofdiskspace.md) 屬性為1，使用者介面會顯示 [OutOfDisk] 對話方塊，將 [ [**MSIINSTALLPERUSER**](msiinstallperuser.md) ] 屬性的值設定為1，將 [**ALLUSERS**](allusers.md) 屬性的值設定為 [2]，將 [ [**MSIFASTINSTALL**](msifastinstall.md) ] 屬性設定為1，然後傳回。 因為已設定 **MSIFASTINSTALL** 屬性，所以不會針對安裝產生任何系統還原點。 當使用者啟動 InstallPerMachine 按鈕時，如果 **OutOfDiskSpace** 屬性為1，使用者介面會顯示 [OutOfDisk] 對話方塊，將 **ALLUSERS** 屬性的值設定為1，然後傳回。

[ControlEvent](controlevent-table.md) 資料表 (部分)  

| 對話\_          | 控制項\_         | 事件                 | 引數  | 條件                 | 單 |
|-------------------|-------------------|-----------------------|-----------|---------------------------|-------|
| VerifyReadyDialog | InstallPerUser    | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerUser    | EndDialog             | 傳回    | OutOfDiskSpace <> 1 | 5     |
| VerifyReadyDialog | InstallPerUser    | \[MSIINSTALLPERUSER\] | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[ALLUSERS\]          | 2         | 1                         | 3     |
| VerifyReadyDialog | InstallPerMachine | SpawnDialog           | OutOfDisk | OutOfDiskSpace = 1        | 1     |
| VerifyReadyDialog | InstallPerMachine | EndDialog             | 傳回    | OutOfDiskSpace <> 1 | 3     |
| VerifyReadyDialog | InstallPerMachine | \[ALLUSERS\]          | 1         | 1                         | 2     |
| VerifyReadyDialog | InstallPerUser    | \[MSIFASTINSTALL\]    | 1         | 1                         | 4     |



 

InstallPerUser 控制項應從任何安裝的使用者介面中移除，其使用早于 Windows Installer Windows Installer 5.0 的 Windows Installer 版本。 範例封裝中的 [ControlCondition](controlcondition-table.md) 資料表包含四個專案，如果目前的版本小於 Windows Installer 5.0，則會停用並隱藏 InstallPerUser 控制項。 資料表會使用 [**VersionMsi**](versionmsi.md) 屬性的值和 [條件陳述式語法](conditional-statement-syntax.md) 來定義此條件。 只有當條件欄位中的語句為 true 時，才會執行 [動作] 欄位中指定的動作。

[ControlCondition](controlcondition-table.md) 資料表 (部分) 

| 對話\_          | 控制項\_      | 動作  | 條件               |
|-------------------|----------------|---------|-------------------------|
| VerifyReadyDialog | InstallPerUser | 啟用  | VersionMsi >= "5.00" |
| VerifyReadyDialog | InstallPerUser | 停用 | VersionMsi < "5.00"  |
| VerifyReadyDialog | InstallPerUser | 顯示    | VersionMsi >= "5.00" |
| VerifyReadyDialog | InstallPerUser | 隱藏    | VersionMsi < "5.00"  |



 

## <a name="specifying-directory-structure"></a>指定目錄結構

使用資料庫編輯器來檢查 PUASample1.msi 的 [目錄](directory-table.md) 資料表。 目錄資料表的目錄（在其目錄父欄位中具有空字串）， \_ 代表來源和目標目錄樹狀目錄的根目錄。 如果未定義 [**TARGETDIR**](targetdir.md) 屬性，安裝程式會在安裝時將其值設定為 [**ROOTDRIVE**](rootdrive.md) 屬性的值。 如果未定義 [**SourceDir**](sourcedir.md) 屬性，安裝程式會將其值設定為包含 Windows Installer 封裝 ( .msi 檔案的目錄位置。 ) 目錄名稱是使用簡短的 \| long 格式來指定。

[目錄](directory-table.md) 資料表 (部分) 

| 目錄          | 目錄 \_ 父系  | DefaultDir               |
|--------------------|--------------------|--------------------------|
| TARGETDIR          |                    | SourceDir                |
| ProgramFilesFolder | TARGETDIR          | .                        |
| ProgramMenuFolder  | TARGETDIR          | .                        |
| INSTALLLOCATION    | MyVendor           | Sample1 \| MSDN-PUASample1 |
| MyVendor           | ProgramFilesFolder | Msft \| Microsoft          |



 

在來源，此 [目錄](directory-table.md) 資料表會解析為下列目錄路徑。

<dl> \[SourceDir \] \\ Msft \\ Sample1  
\[SourceDir\]  
</dl>

在目標上， [目錄](directory-table.md) 資料表會解析為下表中的路徑。 安裝程式會將 [**ProgramFilesFolder**](programfilesfolder.md) 和 [**ProgramMenuFolder**](programmenufolder.md) 屬性的值設定為相依于 [安裝內容](installation-context.md) 的位置，以及系統是否為 Windows Server 2008 R2 和 windows 7 的32位或64位版本。 目的檔案夾的路徑取決於使用者選取的是個別使用者或每部電腦的安裝。

| 安裝內容 | 系統                                                                              | 範例路徑                                                                                                                    |
|----------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 與 Windows 7<br/> 32位版本<br/>           | % ProgramFiles% \\ Msft \\ Sample1<br/> % ALLUSERSPROFILE% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式<br/>                  |
| Per-Machine          | Windows Server 2008 R2 與 Windows 7<br/> 64位版本<br/>           | % ProgramFiles (x86) % \\ Msft \\ Sample1<br/> % ALLUSERSPROFILE% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式<br/>             |
| Per-User             | Windows Server 2008 R2 與 Windows 7<br/> 32位或64位版本<br/> | % USERPROFILE% \\ AppData \\ 本機 \\ 程式 \\ Msft \\ Sample1<br/> % APPDATA% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式<br/> |



 

每個使用者的應用程式應該儲存在 [**ProgramFilesFolder**](programfilesfolder.md) 屬性值所指定的 [程式] 資料夾下的子資料夾中。 一般而言，應用程式的路徑會採用下列格式。

% LOCALAPPDATA% \\ 程式 \\ *ISV 名稱* \\ *AppName*。

每個使用者的設定資料應儲存在 [**ProgramMenuFolder**](programmenufolder.md) 屬性值所指定的 [程式] 資料夾中。 此資料夾通常位於下列路徑。

% APPDATA% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式

如果安裝 [32 位 Windows Installer 封裝](32-bit-windows-installer-packages.md)元件，請使用 [目錄](directory-table.md)資料表中的 [**ProgramFilesFolder**](programfilesfolder.md)和 [**CommonFilesFolder**](commonfilesfolder.md)屬性。 如果要安裝 [64 位 Windows Installer 套件](64-bit-windows-installer-packages.md) 元件，請使用 [**ProgramFiles64Folder**](programfiles64folder.md) 和 [**CommonFiles64Folder**](commonfiles64folder.md) 屬性。 如果您的應用程式包含具有相同名稱之相同元件的32位和64位版本，請確定這些版本儲存在不同的目錄中，或提供不同的名稱。

下表提供與封裝相容 [的目錄配置](directory-table.md) 範例，其中包含32位和64位元件，並且包含一些跨應用程式共用的元件。

| 目錄            | 目錄 \_ 父系    | DefaultDir                        |
|----------------------|----------------------|-----------------------------------|
| TARGETDIR            |                      | SourceDir                         |
| ProgramFilesFolder   | TARGETDIR            | .:P rog32                          |
| ProgramFiles64Folder | TARGETDIR            | .:P rog64                          |
| CommonFilesFolder    | TARGETDIR            | .:Share32                         |
| CommonFiles64Folder  | TARGETDIR            | .:Share64                         |
| ProgramMenuFolder    | TARGETDIR            | .： Sample1 \| MSDN-PUASample1        |
| INSTALLLOCATION      | MyVendor             | Sample1 \| MSDN-PUASample1          |
| INSTALLLOCATIONX64   | Vendorx64            | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATION       | ShVendor             | Sample1 \| MSDN-PUASample1          |
| SHAREDLOCATIONX64    | ShVendorx64          | Sample1 \| MSDN-PUASample1          |
| MyVendor             | ProgramFilesFolder   | Msft \| Microsoft                   |
| Vendorx64            | ProgramFiles64Folder | Msft \| Microsoft                   |
| ShVendor             | CommonFilesFolder    | Msft \| Microsoft                   |
| ShVendorx64          | CommonFiles64Folder  | Msft \| Microsoft                   |
| Shrx86               | SHAREDLOCATION       | x32 \| 32-bit 元件            |
| Shrx64               | SHAREDLOCATIONX64    | x64 \| 64 位元件            |
| Binx86               | INSTALLLOCATION      | x32 \| 32-bit 元件            |
| Binx64               | INSTALLLOCATIONX64   | x64 \| 64 位元件            |
| App32                | Binx86               | myapp 未 \| 共用的32位元件 |
| App64                | Binx64               | myapp 未 \| 共用的64位元件 |
| Share32              | Shrx86               | 共用 \| 共用的32位元件  |
| Share64              | Shrx64               | 共用 \| 共用的64位元件  |



 

在來源，此 [目錄](directory-table.md) 資料表會解析為下列目錄路徑。

<dl> \[SourceDir \] Prog32 \\ Msft \\ Sample1 \\ x32 \\ myapp  
\[SourceDir \] Share32 \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared  
\[SourceDir \] Prog64 \\ Msft \\ Sample1 \\ x64 \\ myapp  
\[SourceDir \] Share64 \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared  
\[SourceDir \] Sample1  
</dl>

在目標上，此 [目錄](directory-table.md) 資料表會解析為下列目錄路徑。 目標路徑取決於 [安裝內容](installation-context.md) 和系統。

| 安裝內容 | 系統                                                                              | 範例路徑                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Per-Machine          | Windows Server 2008 R2 與 Windows 7<br/> 32位版本<br/>           | % ProgramFiles% \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> % ProgramFiles% \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared<br/> % ProgramFiles (x86) % \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> % ProgramFiles (x86) % \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared<br/> % ProgramData% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式 \\ Sample1<br/>               |
| Per-Machine          | Windows Server 2008 R2 與 Windows 7<br/> 64位版本<br/>           | % ProgramFiles (x86) % \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> % ProgramFiles (x86) % \\ Common Files \\ Msft \\ Sample1 \\ x32 \\ shared<br/> % ProgramFiles% \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> % ProgramFiles% \\ Common Files \\ Msft \\ Sample1 \\ x64 \\ shared<br/> % ProgramData% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式 \\ Sample1<br/>               |
| Per-User             | Windows Server 2008 R2 與 Windows 7<br/> 32位或64位版本<br/> | % LOCALAPPDATA% \\ 程式 \\ Msft \\ Sample1 \\ x32 \\ myapp<br/> % LOCALAPPDATA% \\ 程式 \\ 常見的 \\ Msft \\ Sample1 \\ x32 \\ 共用<br/> % LOCALAPPDATA% \\ 程式 \\ Msft \\ Sample1 \\ x64 \\ myapp<br/> % LOCALAPPDATA% \\ 程式 \\ 常見的 \\ Msft \\ Sample1 \\ x64 \\ 共用<br/> % APPDATA% \\ Microsoft \\ Windows [ \\ 開始] 功能表 \\ 程式 \\ Sample1<br/> |



 

## <a name="application-registration"></a>應用程式註冊

PUASample.msi 會將子機碼加入至應用程式的應用程式路徑登錄機碼，並執行註冊，讓應用程式資訊儲存在登錄中的此機碼下。 如需應用程式路徑和應用程式註冊的詳細資訊，請參閱[Shell 開發人員指南](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))的[shell](https://msdn.microsoft.com/library/bb762762.aspx)擴充性一節中的[PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。 在安裝時，使用者會決定是否要在每個使用者或每部電腦的安裝內容中安裝應用程式。 撰寫雙重用途套件時，套件開發人員無法得知是否應在 HKEY 本機電腦下執行註冊， \_ \_ 或 HKEY \_ 目前的 \_ 使用者金鑰。

封裝開發人員會在 [file](file-table.md) 資料表的 file 欄位中，定義應用程式可執行檔的檔案識別碼。

[](file-table.md)檔案資料表 (部分)  

| 檔案      | 元件\_      | FileName                     | FileSize | 版本 | 語言 | 屬性 | 順序 |
|-----------|------------------|------------------------------|----------|---------|----------|------------|----------|
| MyAppFile | ProductComponent | PUASAMP1.EXE\|PUASample1.exe | 81920    |         |          | 0          | 1        |



 

要儲存在登錄中的值可以在 [登錄資料表的](registry-table.md) [值] 欄位中指定為 [格式化](formatted.md) 字串。 使用[檔案資料表的](file-table.md)[檔案] 欄位中定義的檔案識別碼，以及 \[ \#  \] 格式化類型的 filekey 慣例，以指定應用程式路徑登錄機碼的預設值。 最上層 [安裝](install-action.md) 動作會在 [InstallExecuteSequence](installexecutesequence-table.md) 資料表中執行動作。 在此資料表中的[CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和[InstallFinalize](installfinalize-action.md)動作完成之後，Windows Installer 會以 \[ \# \] 應用程式檔的完整路徑取代登錄資料表中格式化的子字串 MyAppFile。

此範例會定義自訂屬性 RegRoot，以包含根機碼的位置，並使用自訂動作來重設屬性值（如果使用者選擇個別電腦安裝）。 使用自訂屬性 RegRoot，在任何格式的字串值中參考根位置。 在 [屬性](property-table.md) 表中，PUASample.msi 套件會定義自訂屬性，並將 RegRoot 的值設定為 HKCU。 這會初始化每個使用者安裝內容的屬性值，也就是雙用途封裝的建議預設內容。

[屬性](property-table.md) 資料表 (部分) 

| 屬性 | 值 |
|----------|-------|
| RegRoot  | HKCU  |



 

在 [CustomAction](customaction-table.md) 資料表中，封裝會定義名為 Set RegRoot HKLM 的自訂動作 \_ \_ 。 [類型] 欄位中的值會將這個值識別為 [自訂動作類型 51](custom-action-type-51.md) 標準自訂動作。 CustomAction 資料表中的來源和目標欄位的意義取決於自訂動作類型。 如需有關標準自訂動作類型的詳細資訊，請參閱 [自訂動作類型](summary-list-of-all-custom-action-types.md)。 Set \_ RegRoot HKLM 自訂動作的 [來源] 欄位 \_ 會指定 RegRoot 屬性的值。 如果安裝程式執行 Set \_ RegRoot \_ HKLM 自訂動作，這會將 RegRoot 屬性的值重設為 hklm。

[CustomAction](customaction-table.md) 資料表 (部分) 

| 動作             | 類型 | 來源      | 目標 |
|--------------------|------|-------------|--------|
| 設定 \_ RegRoot \_ HKLM | 51   | \[RegRoot\] | HKLM   |



 

最上層 [安裝](install-action.md) 動作會以該資料表之 [順序] 欄位中指定的順序，執行 [InstallExecuteSequence](installexecutesequence-table.md) 資料表中的動作。 在 Set RegRoot HKLM 自訂動作 (1501) 的 [順序] 欄位中所撰寫的值 \_ \_ 會指定此自訂動作是在 [InstallInitialize](installinitialize-action.md) 動作 (1500) 之前，以及 [ProcessComponents](processcomponents-action.md) 動作 (1600 之前執行。 ) 此順序可確保 \_ \_ 在安裝時評估 Set RegRoot HKLM 自訂動作的記錄。 如需 InstallExecuteSequence 資料表中建議的動作順序的詳細資訊，請參閱 [建議的 InstallExecuteSequence](suggested-installexecutesequence.md) 主題。 在 [條件] 欄位中撰寫的 [條件陳述式語法](conditional-statement-syntax.md) ，指定 \_ \_ 只有當 [**ALLUSERS**](allusers.md) 屬性的值在安裝時評估為1時，才會執行 Set RegRoot HKLM 動作。 **ALLUSERS** 屬性值1指定每部電腦安裝。

[InstallExecuteSequence](installexecutesequence-table.md) 資料表 (部分) 

| 動作             | 條件  | 順序 |
|--------------------|------------|----------|
| 設定 \_ RegRoot \_ HKLM | ALLUSERS = 1 | 1501     |



 

如果已安裝 ProductComponent 元件 [，則登錄資料表中](registry-table.md) 的下列記錄會執行註冊。 根欄位中的值-1 是在 HKEY 本機電腦上執行註冊所需的值-1 \_ \_ ，適用于每位使用者安裝，以及在 HKEY 目前使用者下，可 \_ 進行個別 \_ 使用者安裝。 登錄欄位中含有空白字串的記錄會在 AppPaths 登錄機碼下新增應用程式的子機碼，並將 " (預設) " 值設定為應用程式可執行檔的完整路徑。 MyAppPathAlias 註冊會將可執行檔對應到應用程式別名，並在使用者于命令列提示字元中輸入別名 "puapct" 時，讓應用程式啟動。 MyAppPathRegistration 註冊會將可執行檔的名稱對應至檔案的完整路徑。



| 登錄              | Root | 按鍵                                                                     | 名稱 | 值                                                                            | 元件        |
|-----------------------|------|-------------------------------------------------------------------------|------|----------------------------------------------------------------------------------|------------------|
|                       | -1   | 軟體 \\ Microsoft \\ MyAppPathRegistrationLocation                      |      | \[RegRoot \] \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ App Paths \\PUAPCT.exe | ProductComponent |
| MyAppPathAlias        | -1   | 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 應用程式路徑 \\PUAPCT.exe     |      | \[\#MyAppFile\]                                                                  | ProductComponent |
| MyAppPathRegistration | -1   | 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 應用程式路徑 \\PUASample1.exe |      | \[\#MyAppFile\]                                                                  | ProductComponent |



 

## <a name="autoplay-cancel-registration"></a>自動播放取消註冊

PUASample.msi 會執行註冊，讓應用程式使用者防止 [硬體自動](/previous-versions/windows/desktop/legacy/cc144210(v=vs.85)) 啟動選取的裝置。 如需有關註冊處理常式以取消自動播放以回應事件的詳細資訊，請參閱[Shell 開發人員指南](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))的[shell](https://msdn.microsoft.com/library/bb762762.aspx)擴充性一節中的[準備硬體和軟體以供使用自動播放](/previous-versions//cc144208(v=vs.85))主題。 下列記錄會在安裝 ProductComponent 元件時，註冊 [名稱] 欄位中指定的處理常式。 根欄位中的值-1 必須指定給 Windows Installer，才能將註冊重新導向至相依于安裝內容的位置。

[](registry-table.md)登錄表 

| 登錄                     | Root | 按鍵                                                                                             | 名稱                                 | 值 | 元件        |
|------------------------------|------|-------------------------------------------------------------------------------------------------|--------------------------------------|-------|------------------|
| MyAutoplayCancelRegistration | -1   | 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ CancelAutoplay \\ CLSID | 66A32FE6-229D-427b-A608-D273F40C034C |       | ProductComponent |



 

## <a name="preview-handler-registration"></a>預覽處理常式註冊

PUASample.msi 執行安裝 [預覽處理常式](../shell/preview-handlers.md) 所需的註冊，此處理程式會啟用 pua 檔案的唯讀預覽，而不啟動應用程式。 如需註冊預覽處理常式的詳細資訊，請參閱[Shell 開發人員指南](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85))的[shell](https://msdn.microsoft.com/library/bb762762.aspx)擴充性一節中的[註冊預覽處理常式](../shell/how-to-register-a-preview-handler.md)主題。 安裝 ProductComponent 元件 [時，登錄表中](registry-table.md) 的下列記錄會註冊處理常式。 根欄位中的值-1 必須指定給 Windows Installer，才能將註冊重新導向至相依于安裝內容的位置。

[](registry-table.md)登錄表

| 登錄                       | Root | 按鍵                                                                              | 名稱                                   | 值                                        | 元件        |
|--------------------------------|------|----------------------------------------------------------------------------------|----------------------------------------|----------------------------------------------|------------------|
| MyPreviewHandlerRegistration1  | -1   | 軟體 \\ 類別 \\ 。 pua                                                          |                                        | puafile                                      | ProductComponent |
| MyPreviewHandlerRegistration2  | -1   | Software \\ Microsoft \\ Windows \\ CurrentVersion \\ PreviewHandlers                    | {1531d583-8375-4d3f-b5fb-d23bbd169f22} | Microsoft Windows PUA TEST Preview 處理常式   | ProductComponent |
| MyPreviewHandlerRegistration3  | -1   | 軟體 \\ 類別 \\ puafile \\ ShellEx \\ {8895b1c6-b41f-4c1c-a562-0d564250836f}      |                                        | {1531d583-8375-4d3f-b5fb-d23bbd169f22}       | ProductComponent |
| MyPreviewHandlerRegistration4  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 |                                        | Per-User 應用程式範例1預覽處理常式 | ProductComponent |
| MyPreviewHandlerRegistration5  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | AppID                                  | {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}       | ProductComponent |
| MyPreviewHandlerRegistration6  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | DisplayName                            | @shell32、-38242                              | ProductComponent |
| MyPreviewHandlerRegistration7  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22}                 | 圖示                                   | notepad.exe，2                                | ProductComponent |
| MyPreviewHandlerRegistration8  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ThreadingModel                         | 公寓                                    | ProductComponent |
| MyPreviewHandlerRegistration9  | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 |                                        | \#%% SystemRoot% \\ system32 \\shell32.dll       | ProductComponent |
| MyPreviewHandlerRegistration10 | -1   | 軟體 \\ 類別 \\ CLSID \\ {1531d583-8375-4d3f-b5fb-d23bbd169f22} \\ InProcServer32 | ProgID                                 | puafile                                      | ProductComponent |



 

 

 

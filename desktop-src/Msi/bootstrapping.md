---
description: 目前每次嘗試使用 Windows Installer 的安裝都會先檢查安裝程式是否出現在使用者的電腦上，如果不存在，是否已準備好安裝 Windows Installer 的使用者和電腦。
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: 引導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982379"
---
# <a name="bootstrapping"></a>引導

目前每次嘗試使用 Windows Installer 的安裝都會先檢查安裝程式是否出現在使用者的電腦上，如果不存在，是否已準備好安裝 Windows Installer 的使用者和電腦。 Windows Installer SDK 提供安裝應用程式 [Instmsi.exe](instmsi-exe.md) ，其中包含安裝 Windows Installer 的所有邏輯和功能。 不過，啟動載入應用程式必須管理此安裝。

啟動載入應用程式必須先檢查目前是否已安裝 Windows Installer。 應用程式可以使用 [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)取得目前安裝的 Windows Installer 版本。 如果目前未安裝 Windows Installer，啟動載入器應用程式必須查詢作業系統，以判斷所需的 Instmsi.exe 版本。 開始安裝 Windows Installer 之後，啟動載入應用程式必須處理來自 Instmsi.exe 應用程式的傳回碼，並處理 Windows Installer 安裝期間所產生的任何重新開機。 如需詳細資訊，請參閱 [判斷 Windows Installer 版本](determining-the-windows-installer-version.md)

下列範例會示範安裝 Microsoft Office 2000 的安裝應用程式如何檢查使用者的系統，並設定 Windows Installer 安裝。 此範例是專為安裝 Office 2000 所撰寫，且僅供一般參考使用。

當使用者將 Office 2000 CD-ROM 插入電腦時，Setup.exe 會根據使用者的需求，嘗試啟動維護模式、安裝應用程式，或完全不執行任何動作。 下一節描述 Office 2000 安裝應用程式（名為 Setup.exe）如何限定使用者和其電腦、如何建立命令列，並使用 Msiexec.exe 應用程式安裝 Windows Installer。

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a>Setup.exe 如何在安裝 Office 2000 時啟動 Windows Installer

1.  使用者將 Office 2000 CD-ROM 插入他們的電腦。 Windows 作業系統會使用/autorun 參數和自動播放 .inf 檔案起始 Setup.exe。 您可以在 Office 2000 CD-ROM 的根目錄找到自動執行 .inf 檔案，其中包含下列各節：

    \[自動執行\]

     

    \[Office 功能\]

     

    \[產品資訊\]

     

    \[ServicePack \] 。

    [ \[ 自動 \] 執行] 區段包含執行 Setup.exe 應用程式的命令列、執行用來顯示光碟的圖示，以及包含將 [安裝] 選項和 [設定] 選項新增至 cd-rom 內容功能表的資訊。

    [ \[ Office 功能] \] 區段包含功能和功能名稱組的清單。

    [ \[ 產品資訊] \] 區段會指定應用程式的名稱和版本。

    [ \[ ServicePack] \] 區段可讓網路系統管理員設定所需的最低 service pack 層級。 網路系統管理員可以使用此區段來撰寫當本機作業系統沒有必要的 service pack 時，所顯示的警示訊息文字。

    以下是範例自動執行 .inf。

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  Setup.exe 的應用程式會檢查 \_ MsiPromptForCD mutex。 Windows Installer 會在提示使用者插入 CD-ROM 時建立此 mutex。 Mutex 是否存在指出 Windows Installer 正在執行已要求 Office 2000 CD-ROM 的安裝。 在此情況下，Setup.exe 的應用程式會立即結束，並允許 Office 2000 安裝繼續進行。 如果沒有 mutex，Setup.exe 的應用程式會繼續進行評估登錄機碼以判斷是否已安裝 Office 2000 的步驟3。
3.  Setup.exe 的應用程式會檢查 Office9 登錄機碼是否存在：

    **HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**

    如果這個登錄機碼不存在，Setup.exe 的應用程式會在檢查作業系統的步驟6繼續進行，以判斷它是否符合安裝 Office 2000 的資格。

4.  如果 Office 2000 登錄機碼存在，Setup.exe 的應用程式會藉由呼叫 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)來檢查目前的安裝狀態。 InstallState 預設值的傳回狀態 \_ 表示已安裝 office 2000，而 Setup.exe 應用程式會繼續執行步驟5，並在其中檢查 office 2000 以從來源執行。

    如果未安裝 Office 2000，Setup.exe 應用程式會在檢查作業系統的步驟6繼續進行，以判斷它是否符合安裝 Office 2000 的資格。

5.  Setup.exe 的應用程式會針對每個 **\[ \] OfficeFeatures** 區段中的每一項功能呼叫 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) ，以進行每個自動播放 .inf 檔案的功能。 如果其中任何一項功能傳回 INSTALLSTATE \_ 來源，這表示該功能正在從來源執行，而且 Setup.exe 應用程式會立即結束。

    如果沒有任何功能傳回 INSTALLSTATE \_ 來源，Setup.exe 應用程式會啟動安裝程式應用程式、Msiexec.exe，並在結束之前提供 Windows Installer 維護模式。

6.  Setup.exe 的應用程式會判斷作業系統是否符合安裝 Office 2000 的資格。 需要 Windows XP 才能安裝 Office 2000。 如果作業系統需要 service pack 更新才能符合 Office 2000 的資格，Setup.exe 應用程式會顯示在 [自動播放] 檔案中指定的文字。 如果作業系統不符合 Office 2000 或 Office 2000 升級的資格，Setup.exe 的應用程式會顯示一則訊息，讓使用者無法繼續。

    如果作業系統符合 Office 2000 的資格，Setup.exe 的應用程式會繼續進行步驟7，判斷是否已在使用者的電腦上安裝 Windows Installer。

7.  如果使用者的電腦上有 Windows Installer，Setup.exe 應用程式就會啟動 Msiexec.exe 應用程式，並將 Office 2000 .msi 檔案傳遞給它。

    如果本機電腦上未安裝 Windows Installer，Setup.exe 應用程式會繼續執行步驟8，判斷作業系統是否符合安裝 Windows Installer 的資格。

8.  如果本機電腦有資格安裝 Windows Installer，Setup.exe 應用程式會針對該平臺執行 Instmsi.exe 安裝程式應用程式的正確版本。 Setup.exe 可以傳遞 "/q" 命令列參數來隱藏使用者介面，並防止使用者變更任何安裝設定選項。
9.  Setup.exe 的應用程式會載入新安裝的 Msi.dll 檔案，並執行 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 函式的呼叫，以安裝使用者的應用程式。

## <a name="setupexe-command-line-parameters"></a>Setup.exe 命令列參數

Setup.exe 的應用程式可讓系統管理員和使用者將命令列選項傳遞至 Msiexec.exe 應用程式。 如需詳細資訊，請參閱 [命令列選項](command-line-options.md)。 下表列出可搭配 Setup.exe 使用的命令選項。



| 選項                       | 使用方式                                                                                                                                        | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /autorun                     | setup.exe/autorun                                                                                                                           | 執行上面所述的執行 .inf。                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| /a                           | setup.exe /a                                                                                                                                 | 起始系統管理安裝。                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| /j                           | \[u \| m \] *套件* 或 <br/> \[u \| m \] *封裝*/t *轉換清單*<br/> 或 <br/> \[u \| m \] *套件*/g *LanguageID*<br/> | 通告產品。 此選項會忽略在命令列上輸入的任何屬性值。 u 向目前的使用者通告。<br/> m 通告給電腦的所有使用者。<br/> g 語言識別項<br/> t 會將轉換套用至已公告的封裝。<br/>                                                                                                                                                                                                                        |
| /I                           | setup.exe/I Office9.msi/t ProgramMgmt .mst                                                                                                  | 指定要安裝 Setup.exe 的 .msi 檔案。 如果未包含/I 選項，Setup.exe 會使用 Office9.msi 檔。                                                                                                                                                                                                                                                                                                                                                                                 |
| /o<*屬性* = *值*> | setup.exe/o CDKEY = 111111-1111                                                                                                               | 設定 .msi 檔案中的屬性。 Setup.exe 將其傳遞至 msiexec （如撰寫）。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| /q                           | setup.exe/q                                                                                                                                 | 設定安裝的 UI 層級。 /q 沒有適用于 msiexec 的 UI (/qn。 ) /qb 基本 UI<br/> /qr 縮減的 UI。<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| 一樣\#                         | setup.exe/m4                                                                                                                                | 根據選取的協定支援多個授權。 授權驗證自訂動作會使用這個屬性來寫入 LV 憑證。 /M 選項後面必須接著允許的解除鎖定數目。 /M 選項指定的值應該設定為 Office9.msi 檔中的 "M" 屬性。 如果未指定任何值，但使用/m 選項與安裝程式，則應該設定0的值。 需要有/m 選項，才能支援使用 CD 或網路的選取客戶。 |
| /settings                    | setup.exe/settings mysettings.ini                                                                                                           | 可讓系統管理員指定 .ini 檔案，其中包含要在 Office 2000 安裝期間傳遞的所有自訂設定。 請參閱以下 .ini 檔案的描述。                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a>使用 .ini 檔案

建立初始化檔可能比建立長命令列更容易。 使用/settings 選項，Setup.exe 應用程式會讀取指定的 .ini 檔，並建立命令列以傳遞至 Msiexec.exe 應用程式。 .Ini 檔只支援命令列支援的屬性。 如果在 .ini 檔和命令列中都找到屬性或值，則命令列設定會覆寫 .ini 檔案設定。

.Ini 檔案的格式為：

\[微星\]

 

\[Mst\]

 

\[options\]

 

\[顯示\]

.Ini 檔案的 \[ msi \] 區段會指定安裝安裝套件的路徑。 這會對應至命令列上的/I 選項。

.Ini 檔案的 \[ mst \] 區段會指定此安裝所使用的轉換路徑。 這會對應至命令列上的/j 選項。 使用 MST1 MST (N) ，在不同的行上指出多個轉換。 當剖析為命令列時，.ini 檔案中的清單會從左至右轉換。 請注意，與 MST (N) 標題相關聯的數位只存在於維護唯一識別碼，而且沒有任何程式設計意義。

\[選項 \] 區段可讓網路系統管理員設定及覆寫 .msi 或 .mst 檔案中的屬性。 在 .ini 檔案中設定的選項會使用/o 選項新增至命令列。 選項區段中的每個選項都必須有屬性名稱和值。

[ \[ 顯示] \] 區段是用來設定安裝期間使用的使用者介面層級。 這會對應至命令列上的/q 選項。 有效值為 [無]、[基本]、[已縮減] 和 [完整]。

範例 .ini 檔案

\[MSI\]

 

MSI = \\ \\ sourceshare \\ Office2000 \\Office2000.msi

 

\[Mst\]

 

MST1 = \\ \\ sourceshare \\ Office2000 \\ trns1 .mst

 

MST2 = \\ \\ sourceshare \\ Office2000 \\ trns2 .mst

 

\[選項\]

 

PUBLICPROPERTY = 您的值

\[顯示\]

 

顯示 = 無

 


---
description: Instmsi.exe 是安裝 Windows Installer 的可轉散發套件&\# 160、2.0 和舊版的 Windows Installer。 請參閱可轉散發套件的 Windows Installer 可轉散發套件，適用于 Windows Installer&\# 160、3.0 和更新版本。
ms.assetid: 74ea4530-3a73-4169-b0b7-f0272229192d
title: Instmsi.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2177fbb145dbfe2817dba2207cff95e5d80b801cc2f442085ba396f461870f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946116"
---
# <a name="instmsiexe"></a>Instmsi.exe

Instmsi.exe 是安裝 Windows Installer 2.0 和舊版 Windows Installer 的可轉散發套件。 請參閱 Windows Installer 3.0 和更新版本的可轉散發套件[Windows Installer](windows-installer-redistributables.md)可轉散發套件。

如需作業系統隨附的 Windows Installer 版本的詳細資訊，請參閱[Windows Installer 的發行](released-versions-of-windows-installer.md)版。

某些可轉散發套件不應在特定版本的作業系統上執行。 下表說明哪些 Instmsi 與哪些作業系統相容。



| 如果 Instmsi.exe 安裝這個版本的 Windows Installer | Instmsi.exe 可以在這些作業系統上執行                    | Instmsi.exe 不得在這些作業系統上執行                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Windows安裝程式版本1。0                                 | Windows 95、Windows 98、Windows NT 4.0 + SP3                           | Windows我、Windows 2000、Windows XP、Windows Server 2003、Windows Vista Windows Server 2008 |
| Windows安裝程式版本1。1                                 | Windows 95、Windows 98、Windows NT 4.0 + SP3                           | Windows我、Windows 2000、Windows XP、Windows Server 2003、Windows Vista Windows Server 2008 |
| Windows安裝程式版本1。2                                 | Windows 95、Windows 98、Windows Me、Windows NT 4.0 + SP3               | Windows 2000、Windows XP、Windows Server 2003、Windows Vista、Windows Server 2008             |
| Windows安裝程式版本2。0                                 | Windows 95、Windows 98、Windows Me、Windows NT 4.0 + SP6、Windows 2000 | WindowsXP、Windows server 2003、Windows Vista Windows Server 2008                           |



 

例如，在執行可轉散發套件之前，重新散發 Windows Installer 版本1.1 的應用程式應該檢查作業系統是否 Windows NT 4.0 SP3 或 Windows 98/95。 使用可轉散發套件的應用程式也應該確保 Windows Installer 的 ANSI 版本是安裝在 Windows 98/95 上，而且 Unicode 版本是安裝在 Windows NT 或 Windows 2000 上。 請注意，有些應用程式會將 Unicode 版本重新命名為 InstMsiW。

## <a name="syntax"></a>Syntax

**instmsi** *選項*

## <a name="command-line-options"></a>命令列選項

命令列選項不區分大小寫。



| 選項                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /q                         | 供應用程式使用，以在啟動載入器應用程式中重新發佈 Windows Installer。 不會向使用者顯示任何 UI。 啟動載入應用程式應該會檢查傳回碼，以判斷是否需要重新開機才能完成 Windows Installer 安裝。                                                                                                                                                                                                                          |
| /t                         | 僅供用於偵錯工具用途。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /c： "msiinst/delayreboot"  | 延遲的重新開機選項。 防止 Instmsi 提示使用者重新開機，即使它必須取代安裝期間所使用的檔案。 如果使用此選項叫用 Instmsi， \_ \_ \_ 如果必須取代使用中的檔案，則會傳回錯誤成功重新開機。 如果不需要取代使用中的檔案，則會傳回錯誤 \_ 成功。 適用于 Windows Installer 2.0 或更新版本的 Instmsi。 如需延遲重新開機的詳細資訊，請參閱「備註」一節。<br/> |
| /c： "msiinst/delayrebootq" | 延遲重新開機選項的安靜版本。 它不會向使用者顯示任何 UI。 否則行為會與先前的選項相同。 適用于 Windows Installer 2.0 或更新版本的 Instmsi。 如需延遲重新開機的詳細資訊，請參閱「備註」一節。<br/>                                                                                                                                                                                                                           |
| /?                         | 顯示說明。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>備註

啟動使用 Instmsi.exe 安裝 Windows Installer 與另一個[應用程式的應用程式](bootstrapping.md)，可能需要額外的系統重新開機。 這可能是在安裝應用程式所需的任何重新開機以外的額外重新開機。

延遲的重新開機選項只適用于想要消除額外重新開機所造成的額外重新開機的安裝程式開發人員，其安裝應用程式會 Instmsi.exe 使用安裝程式來安裝使用中的檔案。

開發人員應在其安裝應用程式中執行下列動作，以使用延遲的重新開機選項。 安裝2.0 版之前的 Windows Installer 版本的 Instmsi.exe 版本，無法使用此選項：

**使用延遲的重新開機選項**

1.  使用其中一個延遲的重新開機命令列選項來呼叫 Instmsi.exe。
2.  請將錯誤 \_ 成功或錯誤 \_ 成功重新開機的傳回視為 \_ \_ 成功。
3.  從以下的 InstallerLocation 值取得包含新安裝 Windows Installer 二進位檔之資料夾的路徑：

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **安裝程式**

    此值的型別為 **REG \_ SZ**。

4.  將目前目錄設定為在步驟3中取得的路徑。
5.  在應用程式的封裝上叫用 Msiexec，並執行應用程式特定的其他安裝程式程式碼。 如果安裝應用程式使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)，則應用程式必須從步驟3取得的位置載入 MSI.DLL。
    > [!Note]  
    > 在步驟3中取得之位置的新 MSI.DLL 上呼叫 **LoadLibrary** 的應用程式，必須確保進程內尚未載入較舊版本的 MSI.DLL。 如果已在進程中載入舊版 MSI.DLL，則必須在新 MSI.DLL 的 **LoadLibrary** 呼叫之前，從進程位址空間中卸載它。

     

6.  如果步驟 (5) 不需要重新開機，且 Instmsi.exe \_ \_ \_ 在步驟 (1) 中傳回錯誤成功重新開機，請提示使用者重新開機，以完成系統上 Windows Installer 二進位檔的設定。 但是，如果在步驟 (5) 中發生重新開機，則不需要執行任何其他步驟。

Instmsi.exe 適用于[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟動](bootstrapping.md)
</dt> <dt>

[網際網路下載啟動載入](internet-download-bootstrapping.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> </dl>

 

 





---
description: 此區段會列出 Windows Installer 所定義的屬性：
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: 屬性參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38f952632609090c69b85786c6aef64243d420b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481564"
---
# <a name="property-reference"></a>屬性參考

此區段會列出 Windows Installer 所定義的屬性：

-   [元件位置屬性](#component-location-properties)
-   [設定屬性](#configuration-properties)
-   [日期、時間屬性](#date-time-properties)
-   [功能安裝選項屬性](#feature-installation-options-properties)
-   [硬體屬性](#hardware-properties)
-   [安裝狀態屬性](#installation-status-properties)
-   [作業系統屬性](#operating-system-properties)
-   [產品資訊屬性](#product-information-properties)
-   [摘要資訊更新屬性](#summary-information-update-properties)
-   [系統資料夾屬性](#system-folder-properties)
-   [使用者資訊屬性](#user-information-properties)

您可以透過撰寫的資料或自訂動作來指定其他屬性。 名稱不含小寫字母的屬性是公用屬性，可以在命令列上指定。

如需安裝程式屬性所提供之 [ **卸載** ] 登錄機碼值的詳細資訊，請參閱卸載登錄機 [碼](uninstall-registry-key.md)。

## <a name="component-location-properties"></a>元件位置屬性

下列清單提供元件位置屬性的詳細資訊連結。



| 屬性                                                            | 描述                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | 安裝程式會將這個屬性設定為啟動的資料庫、來源上的資料庫，或快取的資料庫。<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | 安裝程式會針對 [並行安裝](concurrent-installations.md) 動作所執行的安裝，設定此屬性。<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | 包含原始程式檔的根目錄。<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | 指定安裝的根目的地目錄。 在 [系統管理安裝](administrative-installation.md) 期間，此屬性是要複製安裝套件的位置。<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

下列清單提供其他可設定屬性的詳細資訊連結。



| 屬性                                                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**行動**](action.md)<br/>                                                     | 初始化安裝程式之後所呼叫的初始動作。<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | 決定儲存設定資訊的位置。<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | 應用程式更新通道的 URL。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | 提供 **主控台** 中的 [**新增或移除程式**] 的批註。<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | 提供 **主控台** 中的 [**新增或移除程式**] 的連絡人。<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | 應用程式主要資料夾的完整路徑。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | 停用修改產品的功能。<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | 停用移除產品的功能。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | 停用 [程式] wizard 中的 [ **修復** ] 按鈕。<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | 指定安裝套件的主要圖示。<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | 提供 **主控台** 中的 [**新增或移除程式**] 的 **讀我檔案**。<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | 應用程式的估計大小（以 kb 為單位）。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | 防止在 [ **新增或移除程式** ] 清單中顯示應用程式。<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | 應用程式首頁的 URL。<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | 應用程式更新資訊的 URL。<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | 應用程式所需的登錄空間 (以 kb) 。 由 [AllocateRegistrySpace 動作](allocateregistryspace-action.md)使用。<br/>                                                                                                                                                                                                                                              |
| [**CCP \_ 磁片磁碟機**](ccp-drive.md)<br/>                                              | 適用于 CCP 的合格產品的根路徑。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | 用於控制項的預設字型樣式。<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | 設定以停用產生支援 [隨選安裝](installation-on-demand.md)的特定快速鍵。<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | 防止安裝程式將媒體來源（例如 CD-ROM）註冊為產品的有效來源。<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | 停用目前設定的復原。<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | ExecuteAction 起始的最上層動作。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | 安裝程式執行的執行模式。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | 改善特定 OEM 案例下的安裝效能。<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | 安裝功能的初始層級。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | UI 層級上限為基本。<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | 要記錄的動作名稱清單。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | 如果安裝套件不在 CD-ROM 的根目錄，則必須將此屬性設定為相對路徑。<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | 此選用屬性包含以分號分隔的登錄位置清單，應用程式會在其中儲存使用者的設定和喜好設定。 適用于 Windows Installer 4.0。<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | 停用安裝的內嵌使用者介面。<br/> **[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | 縮短安裝大型 Windows Installer 套件所需的時間。<br/> **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | 要求 Windows Installer 只為目前的使用者安裝套件。<br/> **[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | 設定此屬性，以防止安裝程式設定 [**DISABLEMEDIA**](-disablemedia.md) 屬性。<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | 將此屬性設定為 1 (命令列上的一個) 或在 [屬性工作表](property-table.md) 中，將升級元件規則套用至特定產品的 [小型更新](small-updates.md) 和 [次要升級](minor-upgrades.md) 。 從 Windows Installer 3.0 開始提供。<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | 當這個屬性設定為1時，安裝程式可以取消註冊並卸載多餘的元件，以防止在電腦上留下孤立的元件。<br/> **[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | 允許作者指定主要資料夾以進行安裝。 用來判斷 [**PrimaryVolumePath**](primaryvolumepath.md)、 [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)、 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)和 [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) 屬性的值。<br/> |
| [**特權**](privileged.md)<br/>                                             | 以較高的許可權執行安裝。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | 如果沒有足夠的磁碟空間可供安裝，則為動作。<br/>                                                                                                                                                                                                                                                                                                                   |
| [**重新 啟動**](reboot.md)<br/>                                                     | 強制或隱藏重新開機。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | 抑制重新開機使用者的提示顯示。 任何需要的重新開機都會自動發生。<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | 安裝的預設磁片磁碟機。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | 具有順序資料表架構的資料表。<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | 會使用短檔案名。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**變換**](transforms.md)<br/>                                             | 要套用至資料庫的轉換清單。<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | 通知安裝程式，產品的轉換位於來源。<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | 將 [**TRANSFORMSECURE**](transformssecure.md) 屬性設定為 1 (一個) 會通知安裝程式在使用者電腦上的本機快取轉換，而使用者沒有寫入存取權。<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | 當啟用記錄功能時，安裝程式會將這個屬性的值設定為記錄檔的完整路徑。 從 Windows Installer 4.0 開始，可以使用此屬性。<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | 設定 Windows Installer 封裝的預設記錄模式。 從 Windows Installer 4.0 開始，可以使用此屬性。<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | 將此屬性設定為1，以要求安裝程式在設定 [**AdminUser**](adminuser.md) 屬性時，使用實際的使用者資訊。 從 Windows Installer 4.0 開始，可以使用此屬性。<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>日期、時間屬性

[**日期**](date.md)和 [**時間**](time.md)屬性是安裝程式在資料解壓縮時所設定的即時屬性。



| 屬性                        | 描述                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | 目前的日期。<br/> |
| [**時間**](time.md)<br/> | 目前的時間。<br/> |



 

## <a name="feature-installation-options-properties"></a>功能安裝選項屬性

下列清單提供有關功能安裝選項屬性的詳細資訊連結。



| 屬性                                                                | 描述                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | 要安裝在預設設定中的功能清單。<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | 要在本機安裝的功能清單。<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | 要從來源執行的功能清單。<br/>                                                                                                                                |
| [**做廣告**](advertise.md)<br/>                               | 要公告的功能清單。<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | 要安裝在預設設定中的元件清單。<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | 要在本機安裝的元件識別碼清單。<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | 要從來源媒體執行的元件識別碼清單。<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | 要安裝在預設設定中之檔案的檔案索引鍵清單。<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | 要在本機執行之檔案的檔案索引鍵清單。<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | 要從來源媒體執行的檔案索引鍵清單。<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | 設定此屬性可防止最低許可權使用者 (LUA) 修補應用程式。<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | 要在安裝期間移除的修補程式清單。<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | 指定封裝是否使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 或 [FilesInUse](filesinuse-dialog.md) 功能。<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | 指定如何關閉和重新開機目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | 指定如何關閉目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | 設定這個屬性會移除修補程式。<br/>                                                                                                                                 |
| [**補丁**](patch.md)<br/>                                       | 設定此屬性會套用修補程式。<br/>                                                                                                                                 |
| [**REINSTALL**](reinstall.md)<br/>                               | 要重新安裝的功能清單。<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | 字串，其中包含指定要執行之重新安裝類型的字母。<br/>                                                                                          |
| [**刪除**](remove.md)<br/>                                     | 要移除之功能的清單。<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>硬體屬性

下列清單會識別 Windows Installer 在啟動時設定的硬體屬性。




| 屬性 | 描述 | 
|----------|-------------|
| <a href="alpha.md"><strong>Alpha</strong></a><br /> | 在 Alpha 處理器上執行時的數值處理器等級。<br /><blockquote>[!Note]<br />這個屬性已過時，Windows Installer 不支援 Alpha 平臺。</blockquote><br /> | 
| <a href="borderside.md"><strong>BorderSide</strong></a><br /> | 視窗框線的寬度（以圖元為單位）。<br /> | 
| <a href="bordertop.md"><strong>BorderTop</strong></a><br /> | 視窗框線的高度（以圖元為單位）。<br /> | 
| <a href="captionheight.md"><strong>CaptionHeight</strong></a><br /> | 一般字幕區域的高度（以圖元為單位）。<br /> | 
| <a href="colorbits.md"><strong>ColorBits</strong></a><br /> | 每個圖元的相鄰色彩位數目。<br /> | 
| <a href="intel.md"><strong>英特爾</strong></a><br /> | 在 Intel 處理器上執行時的數值處理器等級。<br /> | 
| <a href="intel64.md"><strong>Intel64</strong></a><br /> | 在 Itanium 處理器上執行時的數值處理器等級。<br /> | 
| <a href="msix64.md"><strong>Msix64</strong></a><br /> | 在 x64 處理器上執行時的數值處理器等級。<br /> | 
| <a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br /> | 已安裝 RAM 的大小（以 mb 為單位）。<br /> | 
| <a href="screenx.md"><strong>ScreenX</strong></a><br /> | 畫面的寬度（以圖元為單位）。<br /> | 
| <a href="screeny.md"><strong>ScreenY</strong></a><br /> | 螢幕的高度（以圖元為單位）。<br /> | 
| <a href="textheight.md"><strong>TextHeight</strong></a><br /> | 字元的高度（以邏輯單位表示）。<br /> | 
| <a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br /> | 可用的分頁檔空間量（以 mb 為單位）。<br /> | 




 

## <a name="installation-status-properties"></a>安裝狀態屬性

下列清單提供安裝期間，安裝程式所更新之狀態屬性的詳細資訊連結。



| 屬性                                                                      | 描述                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | 指出目前的安裝會遵循 [ForceReboot 動作](forcereboot-action.md) 叫用的重新開機。<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | 指出是否已完成磁碟空間的成本。<br/>                                                                                                                                                                                                             |
| [**安裝**](installed.md)<br/>                                     | 表示已安裝產品。<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | 只有在設定 [**MSICHECKCRCS**](msicheckcrcs.md) 屬性時，安裝程式才會對檔案執行 CRC。<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | 安裝程式會將這個屬性設定為 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話的工作階段金鑰。<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | 當安裝程式以較 [*高*](e-gly.md) 的許可權執行時，安裝程式會將這個屬性的值設定為1。<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | 如果作業系統重新開機目前暫止，則安裝程式會將這個屬性設定為1。<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | 當內部安裝層級包含 **INSTALLUILEVEL \_ HIDECANCEL** 時，安裝程式會將 [**MsiUIHideCancel**](msiuihidecancel.md)設定為1。<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | 當內部安裝層級包含 **INSTALLUILEVEL \_ PROGRESSONLY** 時，安裝程式會將 [**MsiUIProgressOnly**](msiuiprogressonly.md)設定為1。<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | 當內部安裝層級包含 **INSTALLUILEVEL \_ SOURCERESONLY** 時， [**MsiUISourceResOnly**](msiuisourceresonly.md)為 1 (一) 。<br/>                                                                                                                       |
| [**NOCOMPANYNAME**](nocompanyname.md)<br/>                             | 抑制 [ [**公司名稱**](companyname.md) ] 屬性的自動設定。<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | 隱藏 [**USERNAME**](username.md) 屬性的自動設定。<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | 磁碟空間不足，無法容納安裝。<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | 磁碟空間不足，復原已關閉。<br/>                                                                                                                                                                                                             |
| [**預選**](preselected.md)<br/>                                 | 已選取功能。<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | 安裝程式會將這個屬性的值設定為 [**PRIMARYFOLDER**](primaryfolder.md) 屬性所指定之磁片區的路徑。<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | 安裝程式會將這個屬性的值設定為字串，表示 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上可用的位元組總數。<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | 安裝程式會將這個屬性的值設定為字串，此字串代表 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考的磁片區上的剩餘位元組總數（如果已安裝所有目前選取的功能的話）。<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | 安裝程式會將這個屬性的值設定為字串，表示 [**PrimaryVolumePath**](primaryvolumepath.md) 屬性所參考之磁片區上所有目前選取之功能所需的總位元組數。<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | LANGID 資料庫的數值語言識別項 () 。 需要 () <br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | 設定安裝程式是否要在使用中的檔案上安裝。<br/>                                                                                                                                                                                          |
| [**恢復**](resume.md)<br/>                                           | 繼續安裝。<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | 停用回復時，安裝程式會設定這個屬性。<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | 指出使用者介面層級。<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | 當系統的變更開始進行此安裝時設定。<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | 當升級移除應用程式時，由安裝程式設定。<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | 安裝程式會將這個屬性設定為安裝期間執行的 Windows Installer 版本。<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>作業系統屬性

下列清單提供有關安裝程式在啟動時所設定之作業系統屬性的詳細資訊連結。



| 屬性名稱                                                                             | 簡短描述                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | 如果使用者具有系統管理員許可權，則設定為 Windows 2000。<br/>                                                                                                                                                                                                                        |
| [**名稱**](computername.md)<br/>                                           | 目前系統的電腦名稱稱。<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | 在支援通用語言執行時間元件的系統上，安裝程式會將這個屬性的值設定為 fusion.dll 的檔案版本。 如果作業系統不支援 common language runtime 元件，安裝程式就不會設定這個屬性。<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | 指出 Windows 的產品類型。<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | 在 Windows 2000 和更新版本的作業系統上，安裝程式只會在安裝 Microsoft BackOffice 元件時，將這個屬性設定為 1 (一個) 。<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | 在 Windows 2000 和更新版本的作業系統上，安裝程式只會在安裝 Windows 2000 Datacenter Server 時，將此屬性設定為 1 (一個) 。<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | 在 Windows 2000 和更新版本的作業系統上，安裝程式只會在安裝 Windows 2000 Advanced Server 時，將此屬性設定為 1 (一個) 。<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | 在 Windows XP 及更新版本的作業系統上，安裝程式會將這個屬性設定為 1 (只有在作業系統為 Home (不 Professional) 時才會) 。<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | 在 Windows 2000 和更新版本的作業系統上，安裝程式只會在安裝 Microsoft Small Business Server 時，將這個屬性設定為 1 (一個) 。<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | 在 Windows 2000 和更新版本的作業系統上，安裝程式會將這個屬性設定為 1)  (只有在使用嚴格的用戶端授權安裝 Microsoft Small Business Server 時，才會將此屬性設定為1。<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows Server 2003 的 web 版本，安裝程式會將 [**MsiNTSuiteWebServer**](msintsuitewebserver.md)屬性設定為 1 (一個) 。 僅適用于 Windows Installer 的 Windows Server 2003 版本。<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | 如果目前的作業系統 Windows XP Tablet PC Edition，則安裝程式會將這個屬性設定為非零值。<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | 在支援 Win32 元件的系統上，安裝程式會將這個屬性的值設定為 sxs.dll 的檔案版本。 如果作業系統不支援 Win32 元件，安裝程式就不會設定這個屬性。<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | 如果 OLE 支援 Windows Installer，則設定。<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | 如果執行安裝的系統支援 [隔離的元件](isolated-components.md)，安裝程式會設定 [**RedirectedDllSupport**](redirecteddllsupport.md)屬性。<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | 當系統是執行終端機伺服器角色服務的遠端管理伺服器時，安裝程式會設定 [**RemoteAdminTS**](remoteadmints.md) 屬性。<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | 作業系統 service pack 的版本號碼。<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | 作業系統 service pack 的次要版本號碼。<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | 當系統作為共用 Windows 運作時設定。<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | 如果 shell 支援功能廣告，請設定。<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | 系統的預設語言識別項。<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | 當系統是執行終端機伺服器角色服務的伺服器時設定。<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | 指出作業系統是否支援使用. simsun18030.ttc (true 型別字型集合) 檔。<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | Windows 作業系統的版本號碼。<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | 目前安裝的數值資料庫版本。<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | 作業系統的版本號碼。<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | 如果系統正在64位的電腦上執行，則為作業系統的版本號碼。<br/>                                                                                                                                                                                               |
| [**Windows 組建**](windowsbuild.md)<br/>                                          | 作業系統的組建編號。<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>產品資訊屬性

下列清單提供有關在 [屬性工作表](property-table.md)中指定之產品特定屬性的詳細資訊連結。



| 屬性名稱                                                  | 簡短描述                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | 技術支援的網際網路位址或 URL。<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | 技術支援電話號碼。<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | 由訊息方塊顯示的字串，會提示您輸入磁片。<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | 如果目前的安裝是從透過系統管理安裝所建立的封裝執行，則設定為 1 (一) 。<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | 將單位放在數位的左邊。<br/>                                                                                        |
| [**製造商**](manufacturer.md)<br/>                | 應用程式製造商的名稱。 (必要)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | 安裝程式會在安裝使用媒體來源（例如 CD-ROM）時，將此屬性設定為 1 (一) 。<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | 這個屬性的存在表示產品程式碼變更轉換已註冊至產品。<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | 這個屬性工作表示安裝具有實例轉換之產品的新實例。<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | 安裝程式會針對 [並行安裝](concurrent-installations.md) 動作執行的安裝設定這個屬性。<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | 用來作為 [**PIDKEY**](pidkey.md) 屬性之範本的字串。<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | 特定產品版本的唯一識別碼。 (必要)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | 人們看得懂的應用程式名稱。 (必要)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | 設定為產品的已安裝狀態。<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | 產品版本的字串格式，做為數值。 (必要)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | 表示一組相關產品的 GUID。<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>摘要資訊更新屬性

下列屬性只能透過 .msp 檔中的轉換來設定，這些檔案是用來更新系統管理映射的摘要資訊串流。



| 屬性                                                              | 描述                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | 這個屬性的值會寫入至 [**修訂編號摘要**](revision-number-summary.md) 屬性。<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | 這個屬性的值會寫入 [ [**批註摘要**](comments-summary.md) ] 屬性中。<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | 這個屬性的值會寫入至 [ [**主體摘要**](subject-summary.md) ] 屬性。<br/>                 |



 

## <a name="system-folder-properties"></a>系統資料夾屬性

下列清單提供有關安裝程式在安裝時所設定之系統資料夾的詳細資訊連結。



| 屬性                                                        | 描述                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | 包含系統管理工具之目錄的完整路徑。<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | 目前使用者之 **漫遊** 資料夾的完整路徑。<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | 所有使用者之應用程式資料的完整路徑。<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | 預先定義的 **64 位通用** 檔案資料夾的完整路徑。<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | 目前使用者之 **一般** 檔案資料夾的完整路徑。<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | **桌面** 資料夾的完整路徑。<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | 目前使用者的 [我的最愛 **]** 資料夾的完整路徑。<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | [字型 **] 資料夾的** 完整路徑。<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | 資料夾的完整路徑，其中包含本機 (nonroaming) 應用程式。<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | [ **圖片** ] 資料夾的完整路徑。<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | **NetHood** 資料夾的完整路徑。<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | 目前使用者的 [ **檔** ] 資料夾的完整路徑。<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | **PrintHood** 資料夾的完整路徑。<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | 預先定義的 **64 位 Program Files** 資料夾的完整路徑。<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | 預先定義的 **32 位 Program Files** 資料夾的完整路徑。<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | **程式功能表** 資料夾的完整路徑。<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | **最近** 資料夾的完整路徑。<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | 目前使用者之 **SendTo** 資料夾的完整路徑。<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | **[開始] 功能表** 資料夾的完整路徑。<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | **啟動** 資料夾的完整路徑。<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | 16位系統 Dll 之資料夾的完整路徑。<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | 預先定義之 **System64** 資料夾的完整路徑。<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | 目前使用者之 **系統** 資料夾的完整路徑。<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | **暫存** 資料夾的完整路徑。<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | 目前使用者之 **範本** 資料夾的完整路徑。<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | **Windows** 資料夾的完整路徑。<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | **Windows** 資料夾的磁片區。<br/>                                      |



 

## <a name="user-information-properties"></a>使用者資訊屬性

下列清單提供使用者提供資訊的詳細資訊連結。



| 屬性                                                      | 描述                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | 管理安裝期間所設定的屬性清單。<br/>       |
| [**名稱**](companyname.md)<br/>                 | 執行安裝之使用者的組織名稱。<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | 目前登入之使用者的使用者名稱。<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | 防止寫入記錄檔的屬性清單。<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | 使用者輸入的產品識別碼部分。<br/>                                 |
| [**ProductID**](productid.md)<br/>                     | 成功驗證之後的完整產品識別碼。<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | 目前使用者的預設語言識別項。<br/>                             |
| [**使用者**](username.md)<br/>                       | 執行安裝的使用者。<br/>                                     |
| [**UserSID 屬性**](usersid.md)<br/>                | 根據使用者的安全識別碼 (SID) 來設定安裝程式。<br/> |



 

 

 

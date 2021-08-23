---
description: 作業系統類別會群組代表作業系統相關物件的類別。
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: 作業系統類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5cbb168b2a322b5ceae8a2bd73985d14a74b4f1df227fd3e6cce384c554742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588288"
---
# <a name="operating-system-classes"></a>作業系統類別

作業系統類別會群組代表作業系統相關物件的類別。 它們代表定義計算環境的各種設定和設定。 範例包括：開機設定、元件物件模型 (COM) 設定、桌面環境設定、驅動程式、安全性設定、使用者設定和登錄設定。

作業系統分類會分組為下列子類別：

-   [COM](#com)
-   [桌上型電腦](#desktop)
-   [驅動程式](#drivers)
-   [事件記錄檔](#windows-event-log)
-   [檔案系統](#file-system)
-   [工作物件](#job-objects)
-   [記憶體和分頁檔案](#memory-and-page-files)
-   [多媒體音訊或視覺效果](#multimedia-audio-or-visual)
-   [網路](#networking)
-   [作業系統事件](#operating-system-events)
-   [作業系統設定](#operating-system-settings)
-   [處理序](#processes)
-   [登錄](#registry)
-   [排程器工作](#scheduler-jobs)
-   [安全性](#security)
-   [服務](#services)
-   [共用](#shares)
-   [[開始] 功能表](#start-menu)
-   [儲存體](#storage)
-   [使用者](#users)
-   [Windows 產品啟用](#windows-product-activation)

## <a name="com"></a>COM

COM 子類別目錄群組類別，這些類別表示 COM 和 DCOM 設定、類別和用戶端應用程式設定。



| 類別                                                                                           | 描述                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ClassicCOMApplicationClasses**](win32-classiccomapplicationclasses.md)               | Association 類別<br/> 關聯 DCOM 應用程式和其下分組的 COM 元件。<br/>                                                                             |
| [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md)                                         | Instance 類別<br/> 表示 COM 元件的屬性。<br/>                                                                                                   |
| [**Win32 \_ ClassicCOMClassSettings**](win32-classiccomclasssettings.md)                         | Association 類別<br/> 將 COM 類別和用來設定 COM 類別實例的設定產生關聯。<br/>                                                           |
| [**Win32 \_ ClientApplicationSetting**](win32-clientapplicationsetting.md)                       | Association 類別<br/> 建立可執行檔和包含可執行檔之 DCOM 設定選項的 DCOM 應用程式的關聯。<br/>                           |
| [**Win32 \_ COMApplication**](win32-comapplication.md)                                           | Instance 類別<br/> 表示 COM 應用程式。<br/>                                                                                                                   |
| [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md)                             | Association 類別<br/> 將 COM 元件與其所在的 COM 應用程式產生關聯。<br/>                                                                            |
| [**Win32 \_ COMApplicationSettings**](win32-comapplicationsettings.md)                           | Association 類別<br/> 關聯 DCOM 應用程式及其設定。<br/>                                                                                   |
| [**Win32 \_ comclass.zip**](win32-comclass.md)                                                       | Instance 類別<br/> 表示 COM 元件的屬性。<br/>                                                                                                   |
| [**Win32 \_ ComClassAutoEmulator**](win32-comclassautoemulator.md)                               | Association 類別<br/> 使 COM 類別和它會自動模擬的另一個 COM 類別產生關聯。<br/>                                                                    |
| [**Win32 \_ ComClassEmulator**](win32-comclassemulator.md)                                       | Association 類別<br/> 建立 COM 類別的兩個版本之間的關聯。<br/>                                                                                                         |
| [**Win32 \_ ComponentCategory**](win32-componentcategory.md)                                     | Instance 類別<br/> 表示元件類別。<br/>                                                                                                                |
| [**Win32 \_ COMSetting**](win32-comsetting.md)                                                   | Instance 類別<br/> 表示與 COM 元件或 COM 應用程式相關聯的設定。<br/>                                                                     |
| [**Win32 \_ DCOMApplication**](win32-dcomapplication.md)                                         | Instance 類別<br/> 表示 DCOM 應用程式的屬性。<br/>                                                                                                |
| [**Win32 \_ DCOMApplicationAccessAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Association 類別<br/> 將 [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) 實例和使用者安全性標識，與可存取的 (SID) 產生關聯。<br/> |
| [**Win32 \_ DCOMApplicationLaunchAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Association 類別<br/> 使 [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) 實例與可啟動它的使用者 sid 產生關聯。<br/>                           |
| [**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)                           | Instance 類別<br/> 表示 DCOM 應用程式的設定。<br/>                                                                                                  |
| [**Win32 \_ ImplementedCategory**](win32-implementedcategory.md)                                 | Association 類別<br/> 使用元件的介面來建立元件類別和 COM 類別的關聯。<br/>                                                                         |



 

## <a name="desktop"></a>桌面

桌面子類別目錄會群組類別，這些類別代表定義特定桌面設定的物件。



| 類別                                           | 描述                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 桌面**](win32-desktop.md)         | Instance 類別<br/> 代表使用者桌面的一般特性。<br/>                                    |
| [**Win32 \_ 環境**](win32-environment.md) | Instance 類別<br/> 代表執行 Windows 之電腦系統上的環境或系統內容設定。<br/> |
| [**Win32 \_ 時區**](win32-timezone.md)       | Instance 類別<br/> 代表執行 Windows 之電腦系統的時區資訊。<br/>                   |
| [**Win32 \_ UserDesktop**](win32-userdesktop.md) | Association 類別<br/> 將使用者帳戶與其專屬的桌面設定產生關聯。<br/>                   |



 

## <a name="drivers"></a>驅動程式

驅動程式子類別會將代表基礎服務之虛擬裝置磁碟機和系統驅動程式的類別分組。



| 類別                                             | 描述                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32 \_ >systemdriver**](win32-systemdriver.md) | Instance 類別<br/> 代表基底服務的系統驅動程式。<br/> |



 

## <a name="file-system"></a>檔案系統

檔案系統子類別目錄會將代表硬碟以邏輯方式相片順序的類別組成群組。 這包括使用的檔案系統類型、目錄結構，以及磁片分割的方式。



| 類別                                                                               | 描述                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CIMLogicalDeviceCIMDataFile**](win32-cimlogicaldevicecimdatafile.md)     | Association 類別<br/> 關聯邏輯裝置和資料檔案，指出裝置所使用的驅動程式檔案。<br/>                                                      |
| [**Win32 \_ 目錄**](win32-directory.md)                                         | Instance 類別<br/> 代表執行 Windows 之電腦系統上的目錄專案。<br/>                                                                              |
| [**Win32 \_ DirectorySpecification**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Instance 類別<br/> 表示產品的目錄版面配置。<br/>                                                                                                |
| [**Win32 \_ DiskDriveToDiskPartition**](win32-diskdrivetodiskpartition.md)           | Association 類別<br/> 將磁片磁碟機和現有磁碟分割相關聯。<br/>                                                                                         |
| [**Win32 \_ DiskPartition**](win32-diskpartition.md)                                 | Instance 類別<br/> 表示執行 Windows 之電腦系統上的實體磁片之分割區的功能和管理功能。<br/>              |
| [**Win32 \_ DiskQuota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Association 類別<br/> 追蹤 NTFS 檔案系統磁片區的磁碟空間使用量。<br/>                                                                                        |
| [**Win32 \_ LogicalDisk**](win32-logicaldisk.md)                                     | 表示在執行 Windows 的電腦系統上，解析為實際本機儲存裝置的資料來源。<br/>                                                            |
| [**Win32 \_ LogicalDiskRootDirectory**](win32-logicaldiskrootdirectory.md)           | Association 類別<br/> 建立邏輯磁片與其目錄結構的關聯。<br/>                                                                                          |
| [**Win32 \_ LogicalDiskToPartition**](win32-logicaldisktopartition.md)               | Association 類別<br/> 關聯邏輯磁片磁碟機和其所在的磁碟分割。<br/>                                                                           |
| [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md)                         | 代表網路儲存裝置，這些裝置會在執行 Windows 的電腦系統上對應為邏輯磁片。<br/>                                                               |
| [**Win32 \_ OperatingSystemAutochkSetting**](/previous-versions//aa394240(v=vs.85)) | Association 類別<br/> 代表 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 實例與其定義之設定之間的關聯。<br/> |
| [**Win32 \_ QuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Instance 類別<br/> 包含磁片區上磁片配額的設定資訊。<br/>                                                                                       |
| [**Win32 \_ ShortcutFile**](win32-shortcutfile.md)                                   | Instance 類別<br/> 代表做為其他檔案、目錄和命令之快捷方式的檔案。<br/>                                                                  |
| [**Win32 \_ 子目錄**](win32-subdirectory.md)                                   | Association 類別<br/> 將目錄 (資料夾) 和其中一個子目錄 (子資料夾) 建立關聯。<br/>                                                                     |
| [**Win32 \_ SystemPartitions**](win32-systempartitions.md)                           | Association 類別<br/> 將電腦系統和該系統上的磁碟分割相關聯。<br/>                                                                               |
| [**Win32 \_ 磁片區**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Instance 類別<br/> 代表硬碟上的儲存區。<br/>                                                                                                   |
| [**Win32 \_ VolumeQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Association 類別<br/> 將磁片區與每個磁片區配額設定產生關聯。<br/>                                                                                           |
| [**Win32 \_ VolumeQuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Association 類別<br/> 將磁片配額設定與特定磁片區相關聯。<br/>                                                                                     |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Association 類別<br/> 將每個使用者配額與啟用配額的磁片區相關聯。<br/>                                                                                            |



 

## <a name="job-objects"></a>工作物件

工作物件子類別會將代表類別的類別分組，這些類別會提供檢測命名的工作物件。 無法檢測未命名的工作物件。



| 類別                                                                               | 描述                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CollectionStatistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Association 類別<br/> 建立 managed 系統專案集合和類別的關聯，代表有關集合的統計資訊。<br/>                               |
| [**Win32 \_ LUID**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Instance 類別<br/> 代表 (LUID 的本機唯一識別碼) <br/>                                                                                                         |
| [**Win32 \_ LUIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Instance 類別<br/> 表示 LUID 和其屬性。<br/>                                                                                                                 |
| [**Win32 \_ NamedJobObject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Instance 類別<br/> 代表核心物件，該物件可用來將進程分組，以控制工作物件內進程的存留期和資源。<br/> |
| [**Win32 \_ NamedJobObjectActgInfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Instance 類別<br/> 表示工作物件的 i/o 帳戶處理資訊。<br/>                                                                                           |
| [**Win32 \_ NamedJobObjectLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Instance 類別<br/> 表示工作物件與工作物件限制設定之間的關聯。<br/>                                                                     |
| [**Win32 \_ NamedJobObjectLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Instance 類別<br/> 表示工作物件的限制設定。<br/>                                                                                                       |
| [**Win32 \_ NamedJobObjectProcess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Instance 類別<br/> 關聯工作物件和工作物件中包含的進程。<br/>                                                                                     |
| [**Win32 \_ NamedJobObjectSecLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Instance 類別<br/> 建立工作物件和工作物件安全性限制設定的關聯。<br/>                                                                                      |
| [**Win32 \_ NamedJobObjectSecLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Instance 類別<br/> 表示工作物件的安全性限制設定。<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Instance 類別<br/> 表示工作物件與工作物件 i/o 帳戶處理資訊類別之間的關聯。<br/>                                                   |
| [**Win32 \_ SIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Instance 類別<br/> 代表 (SID) 及其屬性的安全識別碼。<br/>                                                                                            |
| [**Win32 \_ TokenGroups**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | 事件類別<br/> 代表存取權杖中群組 Sid 的相關資訊。<br/>                                                                                          |
| [**Win32 \_ TokenPrivileges**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | 事件類別<br/> 表示存取權杖之許可權集的相關資訊。<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>記憶體和分頁檔案

記憶體和分頁檔子類別會將代表分頁檔案設定的類別分組。



| 類別                                                                 | 描述                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 分頁檔**](win32-pagefile.md)                             | Instance 類別<br/> 表示用來處理 Windows 系統上的虛擬記憶體檔案交換的檔案。<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Association 類別<br/> 在正常使用期間，將分頁檔案的初始設定與這些設定的狀態產生關聯。<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Instance 類別<br/> 表示分頁檔的設定。<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Instance 類別<br/> 代表用來處理執行 Windows 之電腦系統上的虛擬記憶體檔案交換的檔案。<br/> |



 

## <a name="multimedia-audio-or-visual"></a>多媒體音訊或視覺效果

多媒體音訊或視覺子類別中的類別代表電腦系統上所安裝之音訊或影片編解碼器的屬性。



| 類別                                       | 描述                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CodecFile**](win32-codecfile.md) | Instance 類別<br/> 代表電腦系統上所安裝的音訊或影片編解碼器。<br/> |



 

## <a name="networking"></a>網路

網路子類別會將代表網路連線、網路用戶端和網路連線設定的類別分組，例如使用的通訊協定。



| 類別                                                                            | 描述                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Association 類別<br/> 將目前的 IP4 路由與保存的 IP 路由表產生關聯。<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Instance 類別<br/> 表示保存的 IP 路由。<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Instance 類別<br/> 表示控制網路資料封包路由的資訊。<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | 事件類別<br/> 表示 IP 路由變更事件。<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Instance 類別<br/> 代表執行 Windows 之電腦系統上的網路用戶端。<br/>                           |
| [**Win32 \_ NetworkConnection**](win32-networkconnection.md)                      | Instance 類別<br/> 代表 Windows 環境中的使用中網路連接。<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Instance 類別<br/> 代表執行 Windows 之電腦系統上的通訊協定和其網路特性。<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Instance 類別<br/> 代表 Windows NT 網域。<br/>                                                             |
| [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Instance 類別<br/> 代表標準 **ping** 命令所傳回的值。<br/>                            |
| [**Win32 \_ ProtocolBinding**](win32-protocolbinding.md)                          | Association 類別<br/> 將系統層級的驅動程式、網路通訊協定和網路介面卡相關聯。<br/>                    |



 

## <a name="operating-system-events"></a>作業系統事件

作業系統事件子類別目錄會將代表作業系統中與進程、執行緒和系統關機相關之事件的類別分組。



| 類別                                                                                 | 描述                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | 事件類別<br/> 代表電腦關機事件。<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | 事件類別<br/> 代表與電腦系統相關的事件。<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | 事件類別<br/> 表示在電腦系統上新增、移除或修改裝置所產生的裝置變更事件。<br/>               |
| [**Win32 \_ ModuleLoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | 事件類別<br/> 表示進程已載入新的模組。<br/>                                                                                      |
| [**Win32 \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | 事件類別<br/> 模組事件的基底事件。<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | 事件類別<br/> 表示已開始新的進程。<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | 事件類別<br/> 表示進程已結束。<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | 事件類別<br/> 進程事件的基底事件。<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | 事件類別<br/> 指出已重新整理系統上的裝置清單 (已新增或移除裝置，或設定) 變更。<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | 事件類別<br/> 所有系統追蹤事件的基類，包括模組、進程和執行緒追蹤。<br/>                                                  |
| [**Win32 \_ ThreadStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | 事件類別<br/> 表示已開始新的執行緒。<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | 事件類別<br/> 表示執行緒已停止。<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | 事件類別<br/> 執行緒事件的基底事件類別。<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | 事件類別<br/> 代表在電腦系統上新增網路磁碟機號或掛接的磁片磁碟機時，所產生的網路對應磁碟機事件。<br/> |



 

## <a name="operating-system-settings"></a>作業系統設定

作業系統設定子類別目錄會群組代表作業系統及其設定的類別。



| 類別                                                                                       | 描述                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BootConfiguration**](win32-bootconfiguration.md)                                 | Instance 類別<br/> 代表執行 Windows 之電腦系統的開機設定。<br/>                                                                       |
| [**Win32 \_ 未進行**](win32-computersystem.md)                                       | Instance 類別<br/> 代表在 Windows 環境中操作的電腦系統。<br/>                                                                              |
| [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md)                     | Association 類別<br/> 將電腦系統和在該系統上執行的處理器建立關聯。<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Instance 類別<br/> 代表產品。<br/>                                                                                                                         |
| [**Win32 \_ DependentService**](win32-dependentservice.md)                                   | Association 類別<br/> 將兩個相依的基底服務相互關聯。<br/>                                                                                                  |
| [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Instance 類別<br/> 代表定義執行相依性的系統服務群組。<br/>                                                                     |
| [**Win32 \_ LoadOrderGroupServiceDependencies**](win32-loadordergroupservicedependencies.md) | Instance 類別<br/> 表示基底服務和載入順序群組之間的關聯，此服務會相依于該群組以開始執行。<br/>                         |
| [**Win32 \_ LoadOrderGroupServiceMembers**](win32-loadordergroupservicemembers.md)           | Association 類別<br/> 使載入順序群組和基底服務產生關聯。<br/>                                                                                             |
| [**Win32 \_ 作業系統**](win32-operatingsystem.md)                                     | Instance 類別<br/> 代表安裝在執行 Windows 之電腦系統上的作業系統。<br/>                                                                |
| [**Win32 \_ OperatingSystemQFE**](win32-operatingsystemqfe.md)                               | Association 類別<br/> 將套用的作業系統和產品更新與 [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)中所表示的相關聯。<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Instance 類別<br/> 表示當作業系統失敗時，將會從記憶體收集的資訊類型。<br/>                                        |
| [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)                             | Instance 類別<br/> 代表整個系統的快速修正程式設計 (QFE) 或已套用至目前作業系統的更新。<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Instance 類別<br/> 代表當使用者登入電腦系統時自動執行的命令。<br/>                                                       |
| [**Win32 \_ SystemBootConfiguration**](win32-systembootconfiguration.md)                     | Association 類別<br/> 使電腦系統與其開機設定產生關聯。<br/>                                                                                      |
| [**Win32 \_ SystemDesktop**](win32-systemdesktop.md)                                         | Association 類別<br/> 使電腦系統與其桌面設定產生關聯。<br/>                                                                                   |
| [**Win32 \_ SystemDevices**](win32-systemdevices.md)                                         | Association 類別<br/> 將電腦系統和安裝在該系統上的邏輯裝置建立關聯。<br/>                                                                   |
| [**Win32 \_ SystemLoadOrderGroups**](win32-systemloadordergroups.md)                         | Association 類別<br/> 建立電腦系統和載入順序群組的關聯。<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Association 類別<br/> 使網路連接與其所在的電腦系統產生關聯。<br/>                                                                  |
| [**Win32 \_ SystemOperatingSystem**](win32-systemoperatingsystem.md)                         | Association 類別<br/> 將電腦系統與其作業系統相關聯。<br/>                                                                                        |
| [**Win32 \_ SystemProcesses**](win32-systemprocesses.md)                                     | Association 類別 <br/> 使電腦系統和在該系統上執行的進程產生關聯。<br/>                                                                           |
| [**Win32 \_ SystemProgramGroups**](win32-systemprogramgroups.md)                             | Association 類別<br/> 建立電腦系統和邏輯程式群組的關聯。<br/>                                                                                     |
| [**Win32 \_ SystemResources**](win32-systemresources.md)                                     | Association 類別<br/> 使系統資源與其所在的電腦系統產生關聯。<br/>                                                                           |
| [**Win32 \_ SystemServices**](win32-systemservices.md)                                       | Association 類別<br/> 將電腦系統和存在於系統上的服務程式產生關聯。<br/>                                                                 |
| [**Win32 \_ SystemSetting**](win32-systemsetting.md)                                         | Association 類別<br/> 將電腦系統與一般設定關聯在該系統上。<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Association 類別<br/> 將電腦系統和在該電腦系統上執行的系統驅動程式相關聯。<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Association 類別<br/> 將電腦系統和時區相關聯。<br/>                                                                                                 |
| [**Win32 \_ 系統使用者**](win32-systemusers.md)                                             | Association 類別<br/> 將電腦系統和該系統上的使用者帳戶相關聯。<br/>                                                                               |



 

## <a name="processes"></a>處理序

處理子類別會將代表系統進程和執行緒的類別分組。



| 類別                                                 | 描述                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 進程**](win32-process.md)               | Instance 類別<br/> 代表執行 Windows 之電腦系統上的事件順序。<br/>      |
| [**Win32 \_ ProcessStartup**](win32-processstartup.md) | Instance 類別<br/> 代表執行 Windows 之電腦系統的啟動設定。<br/> |
| [**Win32 \_ 執行緒**](win32-thread.md)                 | Instance 類別<br/> 表示執行的執行緒。<br/>                                          |



 

## <a name="registry"></a>登錄

登錄子類別中的類別代表 Windows 登錄的內容。



| 類別                                     | 描述                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 登錄**](win32-registry.md) | Instance 類別<br/> 代表執行 Windows 之電腦系統上的系統登錄。<br/> |



 

## <a name="scheduler-jobs"></a>排程器作業

排程器工作子類別目錄會將代表排程工作設定的類別分組。



| 類別                                                | 描述                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | 抽象類別<br/> 代表時間的實例，以時間為單位秒、分鐘、周中的日等等。<br/>                                                                                                                                        |
| [**Win32 \_ register-scheduledjob**](win32-scheduledjob.md)    | Instance 類別<br/> 表示使用 Windows 排程服務排程的作業。<br/>                                                                                                                                                                   |
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Instance 類別<br/> 表示以查詢所產生的 [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 物件形式傳回的時間點。 以24小時制的本機時間傳回 **Hour** 屬性。<br/>                                |
| [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Instance 類別<br/> 表示以查詢所產生的 [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) 物件形式傳回的時間點。 以24小時制的國際標準時間 (UTC) 時間傳回 **Hour** 屬性。<br/> |



 

## <a name="security"></a>安全性

安全性子類別目錄會群組代表系統安全性設定的類別。



| 類別                                                                               | 描述                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ AccountSID**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Association 類別<br/> 建立安全性帳戶實例與安全描述項實例的關聯。<br/>                                             |
| [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Instance 類別<br/> 表示存取控制項目 (ACE)。<br/>                                                                               |
| [**Win32 \_ LogicalFileAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Association 類別<br/> 將檔案或目錄的安全性設定，以及其任意存取控制清單的一個成員， (DACL) 的相關聯。<br/> |
| [**Win32 \_ LogicalFileAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Association 類別<br/> 將檔案或目錄的安全性設定與系統存取控制清單中的一個成員產生關聯 (SACL) 。<br/>            |
| [**Win32 \_ LogicalFileGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Association 類別<br/> 將檔案或目錄及其群組的安全性設定產生關聯。<br/>                                                  |
| [**Win32 \_ LogicalFileOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Association 類別<br/> 將檔案或目錄及其擁有者的安全性設定產生關聯。<br/>                                                  |
| [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Instance 類別<br/> 代表邏輯檔案的安全性設定。<br/>                                                                        |
| [**Win32 \_ LogicalShareAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Association 類別<br/> 關聯共用的安全性設定，以及其 DACL 的其中一個成員。<br/>                                                 |
| [**Win32 \_ LogicalShareAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Association 類別<br/> 將共用的安全性設定和其 SACL 的一個成員產生關聯。<br/>                                                 |
| [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Instance 類別<br/> 代表邏輯檔案的安全性設定。<br/>                                                                        |
| [**Win32 \_ PrivilegesStatus**](win32-privilegesstatus.md)                           | Instance 類別<br/> 表示完成操作所需許可權的相關資訊。<br/>                                          |
| [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Instance 類別<br/> 表示 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)的結構化標記法。<br/>                   |
| [**Win32 \_ SecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Instance 類別<br/> 表示 managed 元素的安全性設定。<br/>                                                                     |
| [**Win32 \_ SecuritySettingAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Instance 類別<br/> 表示授與和拒絕指定物件之信任者的許可權。<br/>                                               |
| [**Win32 \_ SecuritySettingAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Instance 類別<br/> 表示指定物件上指定之信任者的審核。<br/>                                                          |
| [**Win32 \_ SecuritySettingGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Association 類別<br/> 將物件及其群組的安全性相關聯。<br/>                                                                     |
| [**Win32 \_ SecuritySettingOfLogicalFile**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Instance 類別<br/> 表示檔案或目錄物件的安全性設定。<br/>                                                             |
| [**Win32 \_ SecuritySettingOfLogicalShare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Instance 類別<br/> 表示共用物件的安全性設定。<br/>                                                                        |
| [**Win32 \_ SecuritySettingOfObject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Association 類別<br/> 將物件與安全性設定產生關聯。<br/>                                                                          |
| [**Win32 \_ SecuritySettingOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Association 類別<br/> 關聯物件的安全性設定及其擁有者。<br/>                                                            |
| [**Win32 \_ SID**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Instance 類別<br/> 代表任意的 SID。<br/>                                                                                            |
| [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Instance 類別<br/> 表示信任者。<br/>                                                                                                   |



 

## <a name="services"></a>服務

服務子類別會將代表服務和基底服務的類別分組。



| 類別                                           | 描述                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BaseService**](win32-baseservice.md) | Instance 類別<br/> 代表安裝在服務控制管理員所維護之登錄資料庫中的可執行物件。<br/> |
| [**Win32 \_ 服務**](win32-service.md)         | Instance 類別<br/> 代表執行 Windows 之電腦系統上的服務。<br/>                                                         |



 

## <a name="shares"></a>共用

共用子類別會將代表共用資源詳細資料的類別（例如印表機和資料夾）組成群組。



| 類別                                                       | 描述                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DFSNode**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Association 類別<br/> 代表以網域為基礎或獨立分散式檔案系統 (DFS) 的根或連接節點。<br/>                                                           |
| [**Win32 \_ DFSNodeTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Association 類別<br/> 代表 DFS 節點與其中一個目標的關聯性。<br/>                                                                                             |
| [**Win32 \_ DFSTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Association 類別<br/> 代表 DFS 節點的目標。<br/>                                                                                                                         |
| [**Win32 \_ ServerConnection**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Instance 類別<br/> 代表從遠端電腦連接到本機電腦上共用資源的連線。<br/>                                                              |
| [**Win32 \_ ServerSession**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Instance 類別<br/> 代表遠端電腦上的使用者在本機電腦上所建立的會話。<br/>                                                             |
| [**Win32 \_ ConnectionShare**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Association 類別<br/> 將電腦上的共用資源與共用資源的連接產生關聯。<br/>                                                                    |
| [**Win32 \_ PrinterShare**](win32-printershare.md)           | Association 類別<br/> 在透過網路查看本機印表機和代表它的共用時，建立其關聯。<br/>                                                                     |
| [**Win32 \_ SessionConnection**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Association 類別<br/> 代表遠端電腦上的使用者與本機伺服器建立的會話之間的關聯，以及相依于會話的連接。<br/> |
| [**Win32 \_ SessionProcess**](win32-sessionprocess.md)       | Association 類別<br/> 表示登入會話與與該會話相關聯之進程之間的關聯。<br/>                                                            |
| [**Win32 \_ ShareToDirectory**](win32-sharetodirectory.md)   | Association 類別<br/> 將電腦系統上的共用資源與其對應的目錄相關聯。<br/>                                                                    |
| [**Win32 \_ 共用**](win32-share.md)                         | Instance 類別<br/> 代表執行 Windows 之電腦系統上的共用資源。<br/>                                                                                              |



 

## <a name="start-menu"></a>開始功能表

[開始] 功能表子類別目錄會群組代表程式群組的類別。



| 類別                                                                                   | 描述                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LogicalProgramGroup**](win32-logicalprogramgroup.md)                         | Instance 類別<br/> 代表執行 Windows 之電腦系統中的程式群組。<br/>                                                                    |
| [**Win32 \_ LogicalProgramGroupDirectory**](win32-logicalprogramgroupdirectory.md)       | Association 類別<br/> 將邏輯程式群組關聯至 [開始] 功能表) 中的 (群組，以及儲存它們的檔案目錄。<br/>                 |
| [**Win32 \_ LogicalProgramGroupItem**](win32-logicalprogramgroupitem.md)                 | Instance 類別<br/> 代表 **Win32 \_ ProgramGroup** 實例所包含的專案，它本身不是另一個 **win32 \_ ProgramGroup** 實例。<br/> |
| [**Win32 \_ LogicalProgramGroupItemDataFile**](win32-logicalprogramgroupitemdatafile.md) | Association 類別<br/> 使 [開始] 功能表的程式群組專案和儲存這些專案的檔案產生關聯。<br/>                                       |
| [**Win32 \_ ProgramGroupContents**](win32-programgroupcontents.md)                       | Association 類別<br/> 使程式群組順序和其中包含的個別程式群組或專案產生關聯。<br/>                                           |
| [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)                           | Instance 類別<br/> 代表使用者的 [**啟動** \| **程式**] 功能表上程式的邏輯群組。<br/>                                               |



 

## <a name="storage"></a>儲存體

Users 子類別會將代表儲存體資訊的類別分組。



| 類別                                                                   | 描述                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ShadowBy**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Association 類別<br/> 代表陰影複製和建立陰影複製的提供者之間的關聯。<br/>      |
| [**Win32 \_ ShadowCoNtext**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Association 類別<br/> 指定如何建立、查詢或刪除陰影複製。<br/>                                   |
| [**Win32 \_ 陰影**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Instance 類別<br/> 表示先前的原始磁片區複本。<br/>                                  |
| [**Win32 \_ ShadowDiffVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Association 類別<br/> 代表陰影複製提供者與儲存磁片區之間的關聯。<br/>                       |
| [**Win32 \_ ShadowFor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Association 類別<br/> 代表陰影複製和建立陰影複製的磁片區之間的關聯。<br/> |
| [**Win32 \_ ShadowOn**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Association 類別<br/> 代表陰影複製和寫入差異資料的位置之間的關聯。<br/>          |
| [**Win32 \_ ShadowProvider**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Association 類別<br/> 表示建立和表示磁片區陰影複製的元件。<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Association 類別<br/> 代表陰影複製和寫入差異資料的位置之間的關聯。<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Association 類別<br/> 表示陰影複製提供者與支援的磁片區之間的關聯。<br/>                    |
| [**Win32 \_ 磁片區**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Instance 類別<br/> 代表硬碟上的儲存區。<br/>                                                           |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Association 類別<br/> 代表每個磁片區配額設定的磁片區。<br/>                                                |



 

## <a name="users"></a>使用者

Users 子類別會將代表使用者帳戶資訊的類別分組，例如群組成員資格詳細資料。



| 類別                                                                 | 描述                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 帳戶**](win32-account.md)                               | Instance 類別<br/> 表示執行 Windows 之電腦系統已知的使用者帳戶和群組帳戶的相關資訊。<br/> |
| [**Win32 \_ 群組**](win32-group.md)                                   | Instance 類別<br/> 代表群組帳戶的相關資料。<br/>                                                                      |
| [**Win32 \_ GroupInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Association 類別<br/> 識別與 Windows NT 網域相關聯的群組帳戶。<br/>                                       |
| [**Win32 \_ GroupUser**](win32-groupuser.md)                           | Association 類別<br/> 讓群組和屬於該群組成員的帳戶產生關聯。<br/>                                           |
| [**Win32 \_ LogonSession**](win32-logonsession.md)                     | Instance 類別<br/> 描述與登入 Windows 的使用者相關聯的登入會話或會話。<br/>                        |
| [**Win32 \_ LogonSessionMappedDisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Instance 類別<br/> 表示與會話相關聯的對應邏輯磁片。<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Instance 類別<br/> 代表執行 Windows 之電腦系統上特定使用者的網路登入資訊。<br/>           |
| [**Win32 \_ SystemAccount**](win32-systemaccount.md)                   | Instance 類別<br/> 表示系統帳戶。<br/>                                                                                |
| [**Win32 \_ UserAccount**](win32-useraccount.md)                       | Instance 類別<br/> 代表執行 Windows 之電腦系統上使用者帳戶的相關資訊。<br/>                           |
| [**Win32 \_ UserInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Association 類別<br/> 建立使用者帳戶和 Windows NT 網域的關聯。<br/>                                                          |



 

## <a name="windows-event-log"></a>Windows 事件記錄檔

Windows 事件記錄子類別目錄會將代表事件、事件記錄檔專案、事件記錄檔設定等的類別分組。



| 類別                                                         | 描述                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Instance 類別<br/> 表示儲存在 Windows 事件記錄檔中的資料。<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Instance 類別<br/> 表示 Windows 事件。<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Association 類別<br/> 使 [**win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 和 win32 的 [**實例 \_**](win32-computersystem.md)產生關聯。<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Association 類別<br/> 將 [**win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 和 [**win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) 類別的實例產生關聯。<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Association 類別<br/> 將 [**win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 和 [**win32 \_ UserAccount**](win32-useraccount.md)的實例產生關聯。<br/>               |



 

## <a name="windows-product-activation"></a>Windows產品啟用

Windows (WPA) 的產品啟用是一種 antipiracy 技術，可減少軟體的偶爾複製。



| 類別                                                                                                               | 描述                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerSystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Association 類別<br/> 將 Win32 的 [**實例 \_**](win32-computersystem.md) 和 [**win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))相關聯。<br/> |
| [**Win32 \_ Proxy**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Instance 類別<br/> 包含屬性和方法，以查詢及設定與 WPA 相關的網際網路連線。<br/>                                                                |
| [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Instance 類別<br/> 包含與 WPA 相關的屬性和方法。<br/>                                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Win32 類別](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 


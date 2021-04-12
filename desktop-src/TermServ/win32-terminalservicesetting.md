---
title: Win32_TerminalServiceSetting 類別
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting 類別遠端桌面服務
- Win32_TerminalServiceSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317423"
---
# <a name="win32_terminalservicesetting-class"></a>Win32 \_ TerminalServiceSetting 類別

**Win32 \_ TerminalServiceSetting** WMI 類別代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。 設定包括 RD 工作階段主機伺服器模式、授權、Active Desktop、許可權、刪除暫存資料夾，以及會話的臨時目錄等功能。

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。 如需方法的參考資訊，請參閱本主題稍後的方法表格。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a>成員

**Win32 \_ TerminalServiceSetting** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TerminalServiceSetting** 類別具有這些方法。



| 方法                                                                                                                | 描述                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | 在企業中設定新的授權伺服器。<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | 將指定的授權伺服器新增至指定授權伺服器清單的結尾。<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | 判斷 RD 工作階段主機伺服器是否允許從遠端桌面授權伺服器 (RDS Cal) 要求遠端桌面服務用戶端存取授權。<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | 設定遠端桌面授權伺服器的授權類型。<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | 根據接聽程式名稱和 NIC 的唯一組合，建立新的接聽程式堆疊。<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | 從企業刪除指定的授權伺服器。<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | 從指定的授權伺服器清單中移除所有授權伺服器。<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | 列舉所有的遠端桌面授權伺服器和探索方法。<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | 抓取 RD 工作階段主機伺服器為其成員之網域的名稱。<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | 抓取 RD 工作階段主機伺服器 RD 授權寬限期內剩餘的天數。<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | 取得已註冊授權伺服器的清單。<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | 抓取指定授權伺服器的清單。<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | 取得遠端桌面服務網路介面卡的識別碼和描述。<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | 判斷遠端桌面服務與授權伺服器之間的連接狀態。<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | 抓取 Winstation 驅動程式名稱的清單。<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Ping 授權伺服器以判斷它是否為有效的授權伺服器。<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | 從指定的授權伺服器清單中移除指定的授權伺服器。<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | 設定 **AllowTSConnections** 屬性。<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | 設定 **DisableForcibleLogoff** 屬性。<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | 設定 **FallbackPrintDriverType** 屬性。<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | 設定 **HomeDirectory** 屬性。<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | 設定下列其中一個屬性： **DeleteTempFolders** 或 **UseTempFolders**。<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | 將指定的授權伺服器設定為指定授權伺服器清單中的第一個專案。<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | 設定 **ProfilePath** 屬性。<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | 設定 **SingleSession** 屬性。<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | 更新指定授權伺服器的清單，並取代任何現有的指定授權伺服器。<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | 設定 **TimeZoneRedirection** 屬性。<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | 更新探索授權伺服器的清單。<br/>                                                                                                                      |



 

### <a name="properties"></a>屬性

**Win32 \_ TerminalServiceSetting** 類別具有這些屬性。

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定每個使用者會話中是否允許 Active Desktop。

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (0) 


</dt> <dd>

每個使用者會話中都不允許 Active Desktop。

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (1) 


</dt> <dd>

每個使用者會話中都允許 Active Desktop。

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許新的遠端桌面服務連接。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

不允許新的連接。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

允許新的連接。

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

簡短描述 (物件的單行字串) 。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否要在結束時刪除臨時目錄。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

停用臨時目錄的刪除。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

已啟用刪除臨時目錄。

</dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

無法使用這個屬性。

**Windows Server 2008：** 列舉授權伺服器的清單。

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

判斷登入主控台的系統管理員是否可以強制登出。

<dt>

0
</dt> <dd>

系統管理員可以強制登出。

</dd> <dt>

1
</dt> <dd>

系統管理員無法強制登出。

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否要允許遠端桌面連線用戶端在網路連結暫時遺失時，自動重新連線到 RD 工作階段主機伺服器上的會話。

<dt>

0 (0x0) 
</dt> <dd>

自動重新連接已停用。

</dd> <dt>

1 (0x1) 
</dt> <dd>

已啟用自動重新連接。

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否已啟用或停用 (DFSS) 動態公平共用排程。 這可以是下列其中一個值。

**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。

<dt>

0
</dt> <dd>

DFSS 已停用。

</dd> <dt>

1
</dt> <dd>

DFSS 已啟用。

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否啟用磁片公平共用排程。

<dt>

0 (0x0) 
</dt> <dd>

已停用磁片公平共用排程。

</dd> <dt>

1 (0x1) 
</dt> <dd>

已啟用磁片公平共用排程。

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否啟用網路公平共用排程。

<dt>

0 (0x0) 
</dt> <dd>

網路公平共用排程已停用。

</dd> <dt>

1 (0x1) 
</dt> <dd>

已啟用網路公平共用排程。

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否啟用或停用遠端桌面 MSI。

<dt>

0 (0x0) 
</dt> <dd>

Disabled

</dd> <dt>

1 (0x1) 
</dt> <dd>

已啟用

</dd> </dl>

**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定要退回的印表機驅動程式。

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**沒有 fallback dirvers = 0** (0) 


</dt> <dd>

無備用驅動程式。

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**最佳猜測 = 1** (1) 


</dt> <dd>

最佳猜測。

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**最佳猜測，如果找不到符合的結果，則會回復至 PCL = 2** (2) 


</dt> <dd>

最佳猜測。 如果找不到相符項，則會切換回 Hewlett-Packard 印表機控制語言 (PCL) 。

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**最佳猜測，如果找不到相符的結果，請回到 PS = 3** (3) 


</dt> <dd>

最佳猜測。 如果找不到相符的結果，則會改回 Postscript (PS) 。

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**最佳猜測，如果找不到相符項，則會顯示 PCL 和 PS 驅動程式 = 4** (4) 


</dt> <dd>

最佳猜測。 如果找不到相符的，則會顯示 PS 和 PCL 驅動程式。

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供者的功能識別碼。

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦的根目錄。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") 
</dt> </dl>

物件的安裝日期。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權模式的簡短描述。

</dd> <dt>

**LicensingName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

授權模式的名稱。

</dd> <dt>

**LicensingType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定伺服器模式的授權類型。

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**個人終端機伺服器** (0) 


</dt> <dd>

個人 RD 工作階段主機 server。

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>管理 (1) **的遠端桌面**


</dt> <dd>

用於系統管理的遠端桌面。

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**每一裝置** (2) 


</dt> <dd>

每一裝置。 適用于應用程式伺服器。

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (3) 


</dt> <dd>

每個使用者。 適用于應用程式伺服器。

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (4) 


</dt> <dd>

未設定。

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否已啟用 RD 工作階段主機伺服器上允許的作用中和非作用中會話的數目限制的功能。 例如，您可能想要設定 **LimitedUserSessions** ，以保證 RD 工作階段主機伺服器上所安裝特定應用程式的授權合規性。 或者，您可能會想要在負載平衡的伺服器陣列中限制 RD 工作階段主機伺服器上的最大會話數目，如此一來，如果伺服器陣列中的另一部伺服器失敗，伺服器將不會超載。

> [!Note]
>
> 用來連線到伺服器以進行系統管理的會話不會受到 **LimitedUserSessions** 的影響。
>
> 在 RD 工作階段主機伺服器陣列中，如果使用者超過會話限制，則會 RD 連線代理人負載平衡，將會話導向至另一部伺服器。 如果伺服器是獨立伺服器，使用者將無法連接。
>
> 由於基於系統管理目的而用來連線到伺服器的會話，以及在登入週期強制執行會話數目的時間，建議您將 **LimitedUserSessions** 設定為小於伺服器上會話數目的實體限制的值，以稍微低一點。
>
> 只有在安裝 RD 工作階段主機角色服務時， **LimitedUserSessions** 屬性才有效。

 

<dt>

0
</dt> <dd>

這項功能已停用。

</dd> <dt>

1或更大
</dt> <dd>

一個或多個值代表 RD 工作階段主機伺服器上允許的作用中和非作用中)  (會話的最大數目。

</dd> </dl>

</dd> <dt>

**登錄**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否允許新的會話。 此設定不會影響現有的設定。

<dt>

0
</dt> <dd>

允許新的會話。

</dd> <dt>

1
</dt> <dd>

不允許新的會話。

</dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定全部攔截網路流量的預設網路公平共用權數。 有效的值為1到9。

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定本機系統進程的預設網路公平共用權數。 有效的值為1到9。

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定使用者會話的預設網路公平共用權數。 有效的值為1到9。

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **AllowTSConnections** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) 方法所傳回的授權伺服器是否由伺服器或群組原則設定。

**Windows Server 2008：** 無法使用這個屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **DeleteTempFolders** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

無法使用這個屬性。

**Windows Server 2008：** 指出 **DirectConnectLicenseServers** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

不支援這個屬性。

**Windows Server 2008：** 判斷 **DisableForcibleLogoff** 屬性是否由伺服器或群組原則設定。

<dt>

0
</dt> <dd>

伺服器

</dd> <dt>

1
</dt> <dd>

群組原則。

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **EnableAutomaticReconnection** 屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**PolicySourceEnableDFSS**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **EnableDFSS** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **EnableRemoteDesktopMSI** 屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **FallbackPrintDriverType** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **HomeDirectory** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **LicensingType** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **ProfilePath** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **RedirectSmartCards** 屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出屬性 **SingleSession** 是否由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出屬性 **TimeZoneRedirection** 是否由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PolicySourceUseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否由伺服器或群組原則設定 **UseRDEasyPrintDriver** 屬性。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **UseTempFolders** 屬性是由伺服器或群組原則設定。

<dt>

0 (0x0) 
</dt> <dd>

伺服器

</dd> <dt>

1 (0x1) 
</dt> <dd>

群組原則

</dd> </dl>

</dd> <dt>

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ( "0"、"1"、"2"、"4"、"5" ) 、 [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「個人終端機伺服器」、「系統管理遠端桌面」、「個別裝置」、「每位使用者」、「未設定」 ) 
</dt> </dl>

指定可用授權類型的位元遮罩。 這可以是下列一或多個值的組合。

<dt>

1 (0x1) 
</dt> <dd>

支援個人 RD 工作階段主機 server 授權。

</dd> <dt>

2 (0x2) 
</dt> <dd>

支援遠端桌面授權。

</dd> <dt>

4 (0x4) 
</dt> <dd>

支援每一裝置的授權。

</dd> <dt>

8 (0x8) 
</dt> <dd>

支援每個使用者授權。

</dd> </dl>

</dd> <dt>

**ProfilePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

電腦的設定檔路徑。

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否允許在遠端會話中使用智慧卡裝置的重新導向。

<dt>

0 (0x0) 
</dt> <dd>

不允許智慧卡裝置重新導向。

</dd> <dt>

1 (0x1) 
</dt> <dd>

允許智慧卡裝置重新導向。

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

有興趣其屬性的 RD 工作階段主機伺服器名稱。

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

RD 連線代理人的使用者登入模式。

<dt>

0
</dt> <dd>

允許所有連接。

</dd> <dt>

1
</dt> <dd>

允許重新開機，但在重新開機伺服器之前防止新的登入。

</dd> <dt>

2
</dt> <dd>

允許重新登錄，但防止新的登入。

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否允許每位使用者使用一或多個遠端桌面服務會話。

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0) 


</dt> <dd>

每位使用者可以有一個以上的會話。

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1) 


</dt> <dd>

每位使用者只允許一個會話。

</dd> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

<dt>



  ( [確定] ) 


</dt> <dd></dd> <dt>



  ( 「錯誤」 ) 


</dt> <dd></dd> <dt>



  ( 「降級」 ) 


</dt> <dd></dd> <dt>



  ( 「未知」 ) 


</dt> <dd></dd> <dt>



  ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>



  ( 「開始」 ) 


</dt> <dd></dd> <dt>



  ( 「正在停止」 ) 


</dt> <dd></dd> <dt>



  ( "Service" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遠端桌面服務服務的 RD 工作階段主機 server 操作模式。 此模式會控制適用的授權原則，以及是否啟用應用程式相容性功能。

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**>appserver** (1) 


</dt> <dd>

伺服器會以應用程式伺服器的形式運作。

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0) 


</dt> <dd>

會話是從遠端系統管理。

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定用戶端電腦是否可以將其時區設定重新導向至遠端桌面服務會話。

<dt>

0
</dt> <dd>

重新導向已停用。

</dd> <dt>

1
</dt> <dd>

重新導向已啟用。

</dd> </dl>

</dd> <dt>

**UseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否先使用遠端桌面輕鬆列印印表機驅動程式來安裝所有用戶端印表機。

<dt>

0
</dt> <dd>

RD 工作階段主機伺服器會嘗試找出合適的印表機驅動程式來安裝用戶端印表機。 如果 RD 工作階段主機伺服器沒有符合用戶端印表機的印表機驅動程式，伺服器會嘗試使用遠端桌面輕鬆列印驅動程式來安裝用戶端印表機。

</dd> <dt>

1
</dt> <dd>

RD 工作階段主機伺服器會先嘗試使用遠端桌面輕鬆列印印表機驅動程式來安裝所有用戶端印表機。 如果基於任何原因而無法使用遠端桌面輕鬆列印印表機驅動程式，則會使用 RD 工作階段主機伺服器上符合用戶端印表機的印表機驅動程式。

</dd> </dl>

**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。

</dd> <dt>

**UserPermission**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定每個使用者會話是否具有嚴格或寬鬆的安全性。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

安全性是嚴格的。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

安全性被放寬。

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否在每個會話中建立和刪除臨時目錄。

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0) 


</dt> <dd>

系統不會針對每個會話建立和刪除臨時目錄。 第一個會話會建立一個，而且永遠不會刪除。

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1) 


</dt> <dd>

系統會為每個會話建立和刪除臨時目錄。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_TerminalServiceSetting** 會與 [**win32 \_ TerminalService**](win32-terminalservice.md)相關聯，作為 [**win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **設定** 屬性。

[**Win32 \_TerminalSetting**](win32-terminalsetting.md)會與 [**win32 \_ 終端**](win32-terminal.md)機相關聯，作為 [**win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)關聯的 **設定** 屬性。

若要連接到根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。

下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[**Win32 \_ 終端機**](win32-terminal.md)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dt>

[**CIM \_ 設定**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 


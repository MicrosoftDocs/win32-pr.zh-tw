---
title: Win32_TerminalService 類別
description: Win32 服務類別的子類別 \_ 。 Win32 \_ TerminalService 代表 win32 TerminalServiceToSetting 關聯的 Element 屬性 \_ 。
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService 類別遠端桌面服務
- Win32_TerminalService 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867848"
---
# <a name="win32_terminalservice-class"></a>Win32 \_ TerminalService 類別

**Win32 \_ TerminalService** WMI 類別是 [**win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的子類別。 **Win32 \_TerminalService** 代表 [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **Element** 屬性。

下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>成員

**Win32 \_ TerminalService** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TerminalService** 類別具有這些方法。



| 方法                                                                       | 描述                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**改變**](win32-terminalservice-change.md)                               | 修改服務。<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | 修改服務的啟動模式。<br/>                                                     |
| [**建立**](win32-terminalservice-create.md)                               | 建立新的服務。<br/>                                                                    |
| [**刪除**](win32-terminalservice-delete.md)                               | 刪除現有的服務。<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | 傳回控制服務存取的安全描述項。<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | 要求服務將其狀態更新至 service manager。<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | 嘗試將服務置於暫停狀態。<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | 嘗試將服務放在恢復狀態。<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | 寫入安全描述項的更新版本，以控制服務的存取權。<br/> |
| [**StartService**](win32-terminalservice-startservice.md)                   | 嘗試將服務置於啟動狀態。<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | 將服務置於已停止狀態。<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | 嘗試將使用者定義的控制項程式碼傳送至服務。<br/>                                |



 

### <a name="properties"></a>屬性

**Win32 \_ TerminalService** 類別具有這些屬性。

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「服務接受暫停」 ) 
</dt> </dl>

指出是否可以暫停服務。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "服務接受停止" ) 
</dt> </dl>

指出是否可以停止服務。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

服務的簡短描述（單行字串）。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**檢查站**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**service \_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Check Point Count" ) 
</dt> </dl>

此值會在長時間啟動、停止、暫停或繼續作業期間，定期遞增以報告其進度。 例如，服務會在啟動時完成其初始化的每個步驟，以遞增此值。 在服務上叫用作業的使用者介面程式會使用這個值，在冗長的作業期間追蹤服務的進度。 此值無效，而且當服務沒有暫止的啟動、停止、暫停或繼續作業時，應該為零。

這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) 
</dt> </dl>

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 延遲 \_ 自動 \_ 啟動 \_ 資訊**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| FDelayedAutostart" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「延遲的自動啟動」 ) 
</dt> </dl>

若 **為 True**，則服務會在其他自動啟動服務啟動後加上短暫延遲之後啟動。

**Windows Server 2012 R2、Windows 8.1、Windows Server 2012、Windows 8、Windows server 2008 R2、Windows 7、Windows server 2008 和 Windows Vista：** 在 Windows Server 2016 和 Windows 10 之前，不支援這個屬性。

這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( [與桌面互動] ) 
</dt> </dl>

指出服務是否可以在桌面上建立或與 windows 通訊，進而以某種方式與使用者互動。 互動式服務必須在本機系統帳戶下執行。 大部分的服務都不是互動式的;也就是說，它們不會以任何方式與使用者通訊。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前伺服器上已中斷連線的會話數目。 這些會話可能仍會主動耗用伺服器資源，但目前沒有與用戶端的網路連線。

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Display Name" ) 
</dt> </dl>

在 [服務] 嵌入式管理單元中所看到的服務名稱。 這個字串的最大長度為 256 個字元。 請注意，儲存在登錄) 中的顯示名稱和服務名稱 (不一定相同。 例如，DHCP 用戶端服務的服務名稱是 Dhcp，而是顯示名稱 DHCP 用戶端。 服務控制管理員中的名稱會保留大小寫。 不過， [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) 比較一律不區分大小寫。

Constraint：接受與 [**Name**](/windows/desktop/CIMWin32Prov/win32-service) 屬性相同的值。

範例： "Atdisk"

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動失敗的嚴重性」 ) 
</dt> </dl>

當此服務在啟動期間無法啟動時的錯誤嚴重性。 值指出如果發生失敗，啟動程式所採取的動作。 電腦系統會記錄所有錯誤。

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) 


</dt> <dd>

不通知使用者。

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) 


</dt> <dd>

通知使用者。 通常這會是顯示通知使用者問題的訊息方塊。

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) 


</dt> <dd>

使用上次的正確組態重新啟動系統。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) 


</dt> <dd>

系統嘗試以正確的組態重新啟動。 如果服務無法第二次啟動，則啟動會失敗。

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) 


</dt> <dd>

錯誤的嚴重性未知。

</dd> </dl>

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "結束代碼" ) 
</dt> </dl>

Windows 錯誤碼，此錯誤碼會定義啟動或停止服務時所遇到的錯誤。 這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 [**可見於 servicespecificexitcode**](/windows/desktop/CIMWin32Prov/win32-service) 屬性中取得。 服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

已安裝日期物件。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

提供受管理功能指示的服務的唯一識別碼。 這項功能會在物件的 [**Description**](/windows/desktop/CIMWin32Prov/win32-service) 屬性中說明。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "File Path Name" ) 
</dt> </dl>

執行服務之服務二進位檔案的完整路徑。

範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**進程**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態 \_ 進程**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "處理序識別碼" ) 
</dt> </dl>

服務的處理序識別碼。

範例：324

這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。

</dd> <dt>

**可見於 servicespecificexitcode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Server 特定結束代碼" ) 
</dt> </dl>

服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。 結束代碼是由這個類別所代表的服務所定義。 只有當 [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) 屬性值為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Service Type" ) 
</dt> </dl>

為呼叫處理序所提供的服務類型。

值如下：

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**核心驅動程式** ( 「核心驅動程式」 ) 


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**檔案系統驅動程式** ( 「檔案系統驅動程式」 ) 


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**介面卡** ( 「介面卡」 ) 


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

辨識 **器驅動程式** ( 「辨識器驅動程式」 ) 


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**自己的進程** ( 「自己的進程」 ) 


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**共用進程** ( 「共用進程」 ) 


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**互動式進程** ( 「互動式進程」 ) 


</dt> <dd></dd> </dl>

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已啟動」 ) 
</dt> </dl>

指出服務是否已啟動。

這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「啟動模式」 ) 
</dt> </dl>

Windows 基礎服務的啟動模式。

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**開機** ( 「開機」 ) 


</dt> <dd>

作業系統載入器啟動的設備磁碟機 (只對驅動程式服務) 有效。

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) 


</dt> <dd>

由作業系統初始化程式啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**自動** ( 「自動」 ) 


</dt> <dd>

要由服務控制管理員在系統啟動期間自動啟動的服務。 即使使用者沒有登入，也會啟動自動服務。

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) 


</dt> <dd>

當進程呼叫 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) 方法時，服務控制管理員要啟動的服務。 除非使用者登入並啟動這些服務，否則這些服務將不會啟動。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) 


</dt> <dd>

在 StartMode 變更為 Auto 或 Manual 之前無法啟動的服務。

</dd> </dl>

這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "起始帳戶名稱" ) 
</dt> </dl>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username" 或 UPN 格式 ( " *Username@DomainName* " ) 。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為 "。 \\您可以指定使用者名稱」。 若為核心或系統層級的驅動程式， [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) 會包含驅動程式物件名稱 (也就是「 \\ FileSystem \\ Rdr」或「 \\ 驅動程式 Xns」，這是 \\ i/o 系統用來載入設備磁碟機的 ) 。 此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。

範例： "DWDOM \\ Admin"

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "State" ) 
</dt> </dl>

基底服務的目前狀態。

值如下：

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**停止** ( 「已停止」 ) 


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**開始暫** 止 ( 「開始暫止」 ) 


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**停止暫** 止 ( 「停止暫止」 ) 


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**正在** 執行 ( 「正在執行」 ) 


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**繼續暫** 止 ( 「繼續暫止」 ) 


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**暫停暫** 止 ( 「暫停暫止」 ) 


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**暫停** ( 「已暫停」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> </dl>

**Windows Server 2008 和 Windows Vista：** 在 Windows 7 和 Windows Server 2008 R2 之前，此屬性是唯讀的。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

值如下：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)」。CreationClassName ") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ") 
</dt> </dl>

裝載這項服務的系統類型名稱。

這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)」。Name ") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ") 
</dt> </dl>

裝載此服務的系統名稱。

這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "標記識別項" ) 
</dt> </dl>

群組中此服務的唯一標記值。 值為 0 (零) 表示服務沒有標記。 標記可以用來排序載入順序群組內的服務啟動，方法是在位於下列位置的登錄中指定標記順序向量：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **GroupOrderList**    

標記只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務進行評估。

這個屬性繼承自 [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)。

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前伺服器上的會話總數。 這包括已連線和已中斷連線的會話。

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint" ) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「估計的等候時間」 ) 
</dt> </dl>

暫止的啟動、停止、暫停或繼續作業所需的預估時間（以毫秒為單位）。 經過指定的時間之後，服務會使用遞增的 [**檢查點**](/windows/desktop/CIMWin32Prov/win32-service)值或 **CurrentState** 中的變更，對 **>setservicestatus** 方法進行下一個呼叫。 如果 **WaitHint** 所指定的時間量，且 **檢查點** 尚未遞增，或 **CurrentState** 尚未變更，服務控制管理員或服務控制程式會假設發生錯誤。

這個屬性繼承自 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)。

</dd> </dl>

## <a name="remarks"></a>備註

由於 **win32 \_ TerminalService** 類別是 [**win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別的子類別，因此類別會繼承 **win32 \_ 服務** 的所有屬性和方法。

[**Win32 \_TerminalServiceSetting**](win32-terminalservicesetting.md)會與 **win32 \_ TerminalService** 相關聯，作為 [**win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **設定** 屬性。

[**Win32 \_TSSessionDirectory**](win32-tssessiondirectory.md)會與 **win32 \_ TerminalService** 相關聯，作為 [**win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)關聯的 **設定** 屬性。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 


---
description: 代表基底服務的系統驅動程式。
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7533e5d1e842e6794a9f9c386103b781afa0404ee181354c420770358f7e8a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751218"
---
# <a name="win32_systemdriver-class"></a>Win32 \_ >systemdriver 類別

**Win32 \_ >systemdriver** [WMI 類別](../wmisdk/retrieving-a-class.md)代表基底服務的系統驅動程式。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>成員

**Win32 \_ >systemdriver** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ >systemdriver** 類別具有這些方法。



| 方法                                                                              | 描述                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**改變**](change-method-in-class-win32-systemdriver.md)                         | 修改服務的類別方法。<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-systemdriver.md)       | 修改服務啟動模式的類別方法。<br/>                              |
| [**建立**](create-method-in-class-win32-systemdriver.md)                         | 建立新服務的類別方法。<br/>                                             |
| [**刪除**](delete-method-in-class-win32-systemdriver.md)                         | 刪除現有服務的類別方法。<br/>                                       |
| [**InterrogateService**](interrogateservice-method-in-class-win32-systemdriver.md) | 要求服務將其狀態更新為 service manager 的類別方法。<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)             | 嘗試將服務置於暫停狀態的類別方法。<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-systemdriver.md)           | 嘗試將服務置於繼續狀態的類別方法。<br/>                |
| [**StartService**](startservice-method-in-class-win32-systemdriver.md)             | 嘗試將服務置於啟動狀態的類別方法。<br/>              |
| [**StopService**](stopservice-method-in-class-win32-systemdriver.md)               | 將服務置於已停止狀態的類別方法。<br/>                           |
| [**UserControlService**](usercontrolservice-method-in-class-win32-systemdriver.md) | 嘗試傳送使用者定義控制項程式碼至服務的類別方法。<br/>         |



 

### <a name="properties"></a>屬性

**Win32 \_ >systemdriver** 類別具有這些屬性。

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 暫停」 \_ ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「服務接受暫停」 ) 
</dt> </dl>

服務可以暫停。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| 服務 \_ 接受 \_ 停止" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "服務接受停止" ) 
</dt> </dl>

可以停止服務。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) 
</dt> </dl>

第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。 搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| dwServiceType \| 服務 \_ 互動式 \_ 進程" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( [與桌面互動] ) 
</dt> </dl>

這種服務可以在桌面上建立 windows 或與 windows 通訊。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Display Name" ) 
</dt> </dl>

服務的顯示名稱。 這個字串的最大長度為 256 個字元。 服務控制管理員中的名稱會保留大小寫。 **DisplayName** 比較一律不區分大小寫。

條件約束：接受與 **Name** 屬性相同的值。

範例： "Atdisk"

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 服務結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| DwErrorControl」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動失敗的嚴重性」 ) 
</dt> </dl>

當此服務在啟動期間無法啟動時的錯誤嚴重性。 此值表示如果發生失敗，啟動程式所採取的動作。 電腦系統會記錄所有錯誤。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** ( "ignore" ) 


</dt> <dd>

不通知使用者。

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** ( 「正常」 ) 


</dt> <dd>

通知使用者。

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** ( 「嚴重」 ) 


</dt> <dd>

使用上次的正確組態重新啟動系統。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** ( 「重大」 ) 


</dt> <dd>

系統嘗試以正確的組態重新啟動。

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 ( 「未知」 ) 


</dt> <dd>

失敗的原因不明。

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "結束代碼" ) 
</dt> </dl>

Windows 錯誤碼，以定義啟動或停止服務時所遇到的任何問題。 這個屬性會設定為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 當此類別所代表之服務的唯一錯誤，以及錯誤的相關資訊可在 **可見於 servicespecificexitcode** 屬性中取得。 服務會將此值設定為在執行時，以及在正常終止時， **不會 \_ 發生錯誤** 。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

已安裝物件。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)
</dt> </dl>

提供受管理功能指示的服務的唯一識別碼。 這項功能在 [物件 **描述** ] 屬性中有更詳細的說明。

這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "File Path Name" ) 
</dt> </dl>

執行服務之服務二進位檔案的完整路徑。

範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**可見於 servicespecificexitcode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwServiceSpecificExitCode" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Server 特定結束代碼" ) 
</dt> </dl>

服務特定的錯誤碼，表示服務正在啟動或停止時所發生的錯誤。 結束代碼是由這個類別所代表的服務所定義。 只有當 **ExitCode** 屬性值為 **錯誤 \_ 服務 \_ 特定 \_ 錯誤** (1066) 時，才會設定這個值。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Service Type" ) 
</dt> </dl>

為呼叫處理序所提供的服務類型。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

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

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「已啟動」 ) 
</dt> </dl>

服務已啟動。

這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「啟動模式」 ) 
</dt> </dl>

系統驅動程式的啟動模式。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

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

服務控制管理員在系統啟動期間自動啟動的服務。

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動** ( 「手動」 ) 


</dt> <dd>

當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) 


</dt> <dd>

無法再啟動的服務。

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**查詢 \_ 服務 \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)設定 \| LpServiceStartName" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "起始帳戶名稱" ) 
</dt> </dl>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱的格式可能是 DomainName \\ Username。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。 如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。 若是核心或系統層級的驅動程式， **StartName** 會包含驅動程式物件名稱 (也就是 \\ FileSystem \\ Rdr 或 \\ 驅動程式 \\ Xns) ，) 系統會使用這些輸入和 (輸出來載入設備磁碟機。 此外，如果指定了 **Null** ，驅動程式就會根據服務名稱，以 i/o 系統建立的預設物件名稱執行。

範例： "DWDOM \\ Admin"

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| service 結構 \| [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "State" ) 
</dt> </dl>

基底服務的目前狀態。

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

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

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ") 
</dt> </dl>

裝載這項服務的系統類型名稱。

這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ") 
</dt> </dl>

裝載此服務的系統名稱。

這個屬性繼承自 [**CIM \_ 服務**](cim-service.md)。

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Service 結構 \| [**QUERY \_ Service \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "標記識別項" ) 
</dt> </dl>

群組中此服務的唯一標記值。 值為 0 (零) 表示尚未指派標記給服務。 標記可以用來排序載入順序群組內的服務啟動，方法是在位於下列位置的登錄中指定標記順序向量：

這個屬性繼承自 [**Win32 \_ BaseService**](win32-baseservice.md)。

**HKEY \_本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項 \\ GroupOrderList**。

系統只會針對具有開機或系統啟動模式的核心驅動程式和檔案系統驅動程式啟動類型服務來評估標記。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ >systemdriver** 類別衍生自 [**win32 \_ BaseService**](win32-baseservice.md)。

## <a name="examples"></a>範例

[列出系統驅動程式](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141)VBScript 範例會在 HTML 檔案中顯示已安裝的系統驅動程式。

下列 PowerShell 範例會從電腦上的執行中系統驅動程式抓取許多屬性。


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 

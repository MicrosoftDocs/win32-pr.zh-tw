---
description: 執行查詢以接收事件。 呼叫會立即傳回。
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecNotificationQuery 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979191"
---
# <a name="swbemservicesexecnotificationquery-method"></a>SWbemServices.ExecNotificationQuery 方法

[**SWbemServices**](swbemservices.md)物件的 **ExecNotificationQuery** 方法會執行查詢來接收事件。 呼叫會立即傳回。 當事件到達時，使用者可以輪詢傳回的列舉值。

方法會在半同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strQuery* 
</dt> <dd>

必要。 包含事件相關查詢之文字的字串。 此參數不可以是空白。 如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。

</dd> <dt>

*strQueryLanguage* \[選\]
</dt> <dd>

字串，包含要使用的查詢語言。 如果有指定，此值必須是 "WQL"。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

這是決定查詢行為的整數。 預設值為 **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**。 如果您指定這個參數，此參數必須設定為 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** ，否則呼叫會失敗。 此參數可接受下列值。

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * (32 (0x20) ) 


</dt> <dd>

使順向列舉值傳回。 順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果沒有發生錯誤，這個方法會傳回 [**SWbemEventSource**](swbemeventsource.md) 物件。 您可以呼叫 [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) 方法，在事件抵達時取出它們。

## <a name="error-codes"></a>錯誤碼

**ExecNotificationQuery** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者未獲授權可查看結果集。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017) 
</dt> <dd>

查詢語法無效。

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018) 
</dt> <dd>

所要求的查詢語言不支援。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

不同于 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) 方法， **ExecNotificationQuery** 會傳回未來事件所產生的事件種類物件，而不是現有的物件。 **ExecNotificationQuery** 要求的事件物件可以是內建的 (例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) 或外建 (（例如， [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)或 SNMP 事件) 之類的登錄提供者事件）。 如需詳細資訊，請參閱 [判斷要接收](determining-the-type-of-event-to-receive.md) 和 [接收事件通知](receiving-event-notifications.md)的事件種類。

WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。 複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。 WQL 關鍵字的限制取決於查詢的複雜程度。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會監視本機電腦上的磁片區變更。 請注意， [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) 是由提供者定義的外建事件，而不是內建的 WMI 定義事件。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



下列 VBScript 程式碼範例會監視進程刪除。 如果您在工作管理員中刪除進程或關閉應用程式，則腳本會顯示一則訊息。 請注意，此腳本會查詢由 WMI [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)定義的內部事件。


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> <dt>

[使用 WQL 查詢](querying-with-wql.md)
</dt> <dt>

[WQL (適用於 WMI 的 SQL)](wql-sql-for-wmi.md)
</dt> <dt>

[判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 


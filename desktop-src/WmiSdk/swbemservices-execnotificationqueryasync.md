---
description: 執行查詢以接收事件。
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecNotificationQueryAsync 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996655"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.ExecNotificationQueryAsync 方法

[**SWbemServices**](swbemservices.md)物件的 **ExecNotificationQueryAsync** 方法會執行查詢來接收事件。 這個呼叫會立即傳回，而結果和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫端。

查詢中指定的事件可以是內建的 Windows Management Instrumentation (WMI) 事件（例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)）或內建事件（例如 [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)或 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)）。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

在非同步模式中呼叫方法。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemSink* 
</dt> <dd>

必要。 接收非同步事件通知的物件接收。 建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。

</dd> <dt>

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

判斷查詢行為的整數。 這個參數可以設定為下列值。

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80) ) 


</dt> <dd>

導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * (0 (0x0) ) 


</dt> <dd>

防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> <dt>

*objWbemAsyncCoNtext* \[選\]
</dt> <dd>

這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。 使用這個參數可使用相同的物件接收進行多個非同步呼叫。 若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md)方法進行解壓縮。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。 在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。

## <a name="error-codes"></a>錯誤碼

**ExecNotificationQueryAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中所識別的其中一個錯誤碼。

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

不支援要求的查詢語言。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

**ExecNotificationQueryAsync** 方法會傳回未來事件所產生的事件種類物件。 **ExecNotificationQueryAsync** 要求的事件物件可以是內建的 (例如， [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) 或外部 (例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)或 SNMP 事件) 。 如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。

對 **ExecNotificationQueryAsync** 的呼叫會立即傳回。 要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。 若要在每個物件傳回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。 傳回所有物件之後，請執行最後的處理，以執行 *objWbemSink*。[**OnCompleted**](swbemsink-oncompleted.md) 事件。

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。 複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 傳回 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼 asan **HRESULT** 值。 WQL 關鍵字的限制取決於查詢的複雜程度。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例示範一個腳本，該腳本會等候表示進程已結束的 WMI 事件通知。 它正在等候 WMI 內建事件，事件類別的實例 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)。 **\_ \_ InstanceDeletionEvent** 必須代表刪除 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的實例。 如需 WMI 內建事件的詳細資訊，請參閱 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)。

下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。 若要手動停止腳本，請使用工作管理員停止進程。 若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
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

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[註冊系統登錄事件](registering-for-system-registry-events.md)
</dt> <dt>

[判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> <dt>

[在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 


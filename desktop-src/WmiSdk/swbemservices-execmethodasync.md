---
description: SWbemServices.ExecMethodAsync 方法-執行方法提供者所匯出的方法。
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecMethodAsync 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105586"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.ExecMethodAsync 方法

[**SWbemServices**](swbemservices.md)物件的 **ExecMethodAsync** 方法會執行方法提供者所匯出的方法。 呼叫會立即傳回至用戶端，而輸入參數會轉送至方法執行所在的適當提供者。 資訊和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫者。 提供者（而不是 Windows Management Instrumentation (WMI) ）會執行方法。

在非同步模式中呼叫方法。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的詳細資訊與說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemSink* 
</dt> <dd>

必要。 建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。 接收方法呼叫結果的物件接收。 輸出參數會傳送到所提供之物件接收的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件。 呼叫機制的結果會傳送到所提供之物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件。 請注意， **SWbemSink OnCompleted** 不會收到 WMI 方法的傳回碼。 但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證呼叫是否發生，或是基於機械原因而失敗。 從 WMI 方法傳回的結果碼會在提供給 **SWbemSink** 的輸出參數物件中傳回。 如果傳回任何錯誤碼，則不會使用提供的 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。 如果呼叫成功，則會呼叫使用者的 **IWbemObjectSink** 執行以指出作業的結果。

</dd> <dt>

*strObjectPath* 
</dt> <dd>

必要。 字串，包含執行方法之物件的物件路徑。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

</dd> <dt>

*strMethodName* 
</dt> <dd>

必要。 要執行的方法名稱。

</dd> <dt>

*objWbemInParams* \[選\]
</dt> <dd>

[**SWbemObject**](swbemobject.md)物件，其中包含所執行之方法的輸入參數。 根據預設，這個參數是未定義的。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

判斷呼叫行為的整數。 此參數可接受下列值。

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

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> <dt>

*objWbemAsyncCoNtext* \[選\]
</dt> <dd>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會返回物件接收以識別原始非同步呼叫的來源。 如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。 若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。 這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。 如需詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 如果呼叫成功，則會將 [**OutParameters**](swbemmethod-outparameters.md) 物件（也就是 [**SWbemObject**](swbemobject.md) ）提供給 *objWbemSink* 中指定的接收。 傳回的 **OutParameters** 物件包含所執行之方法的輸出參數和傳回值。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

## <a name="error-codes"></a>錯誤碼

**ExecMethodAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單所列的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010) 
</dt> <dd>

指定的類別無效。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E) 
</dt> <dd>

要求的方法無法使用。

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者未獲授權執行此方法。

</dd> </dl>

## <a name="remarks"></a>備註

如果執行的方法具有輸入參數，則 *objWbemInParam* 參數中的 [**InParameters**](swbemmethod-inparameters.md)物件必須與「[建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)」主題中的描述相同。

當您無法直接執行方法時，請使用 **SWbemServices.ExecMethodAsync** 做為直接存取來執行 [*提供者方法*](gloss-p.md) 的替代方法。 例如，將它用於不支援輸出參數的指令碼語言，也就是您的方法有 OUT 參數。 否則，建議您使用直接存取來叫用方法。 如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

**SWbemServices.Exe的 cMethodAsync** 方法需要物件路徑。 如果腳本已經包含 [**SWbemObject**](swbemobject.md) 物件，您可以呼叫 [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md)。

此呼叫會立即傳回。 狀態資訊會透過傳回到呼叫的呼叫，傳回到呼叫端（在 *objWbemSink* 中指定的接收）。 若要在呼叫完成時繼續處理，請執行 *objWbemSink* 的副程式。[**OnCompleted**](swbemsink-oncompleted.md) 事件。

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 如需如何消除風險的詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

使用 *objWbemAsyncCoNtext* 參數來驗證呼叫的來源。

## <a name="examples"></a>範例

下列程式碼範例顯示 **ExecMethodAsync** 方法。 腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。 它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。 如需顯示同步執行相同作業的腳本，請參閱 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)。 如需使用直接存取的範例，請參閱 [在 Class Win32 \_ 進程中建立方法](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。 如需使用 [**SWbemObject**](swbemobject.md)進行相同操作的範例，請參閱 [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md)。


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[呼叫提供者方法](calling-a-provider-method.md)
</dt> <dt>

[操作類別和實例資訊](manipulating-class-and-instance-information.md)
</dt> </dl>

 


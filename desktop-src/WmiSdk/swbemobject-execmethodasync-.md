---
description: SWbemObject 的 ExecMethodAsync \_ 方法會以非同步方式執行方法提供者所匯出的方法。
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: 'SWbemObject.ExecMethodAsync_ 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194913"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.ExecMethodAsync \_ 方法

[**SWbemObject**](swbemobject.md)的 **ExecMethodAsync \_** 方法會以非同步方式執行方法提供者所匯出的方法。 這個方法類似于 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)，但會直接在要執行之方法的物件上運作。 Windows Management Instrumentation (WMI) 不會執行此方法。 提供者會執行此方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemSink* \[在\]
</dt> <dd>

必要。 這是接收方法呼叫結果的物件接收。 輸出參數會傳送到所提供之物件接收的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件。 呼叫機制的結果會傳送到所提供之物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件。 請注意， **SWbemSink OnCompleted** 不會收到方法的傳回碼。 但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證發生的呼叫，或是基於機械原因而失敗。 從方法傳回的結果碼會在提供給 **SWbemSink** 的輸出參數物件中傳回。 如果有任何錯誤碼傳回，則不會使用提供的 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。 如果呼叫成功，則會呼叫使用者的 **IWbemObjectSink** 執行以指出作業的結果。

</dd> <dt>

*strMethodName* \[在\]
</dt> <dd>

必要。 這是物件的方法名稱。

</dd> <dt>

*objwbemInParams* \[在中，選擇性\]
</dt> <dd>

這是 [**SWbemObject**](swbemobject.md) 物件，其中包含所執行之方法的輸入參數。 根據預設，這個參數是未定義的。 如需詳細資訊，請參閱 [建立 InParameters 物件](constructing-inparameters-objects.md) 和 [剖析 OutParameters 物件](parsing-outparameters-objects.md)。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

判斷呼叫行為的整數。 此參數可接受下列值。

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80) ) 


</dt> <dd>

導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * (0 (0x0) ) 


</dt> <dd>

防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，它是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> <dt>

*objWbemAsyncCoNtext* \[在中，選擇性\]
</dt> <dd>

這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。 如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。 若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。 這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法沒有傳回值。 如果呼叫成功，則會將 [**OutParameters**](swbemmethod-outparameters.md) 物件（也是 [**SWbemObject**](swbemobject.md) 物件）提供給 *objWbemSink* 中指定的接收。 傳回的 **OutParameters** 物件包含所執行之方法的輸出參數和傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **ExecMethodAsync \_** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。

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

當您無法直接執行方法時，請使用 **SWbemObject.ExecMethodAsync \_** 方法做為直接存取執行 [*提供者方法*](gloss-p.md)的替代方法。 例如，如果您的方法有 out 參數，請使用 **SWbemObject.ExecMethodAsync \_** 方法搭配不支援輸出參數的指令碼語言。 否則，建議您使用直接存取來叫用方法。 如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

此呼叫會立即傳回。 要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。 若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。 傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用兩個同步通訊或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如果正在執行的方法具有輸入參數，則 [**InParameters**](swbemmethod-inparameters.md) 物件和 *objWbemInParam* 參數必須依照 [建立 InParameters 物件](constructing-inparameters-objects.md) 和 [剖析 OutParameters 物件](parsing-outparameters-objects.md)中所述的方式來進行結構化。

**SWbemObject.ExecMethodAsync \_** 方法會假設 [**SWbemObject**](swbemobject.md)所代表的物件包含要執行的方法。 [**SWbemServices.Exe的 cMethodAsync**](swbemservices-execmethodasync.md)方法需要物件路徑。

## <a name="examples"></a>範例

下列範例顯示 [**ExecMethodAsync**](swbemservices-execmethodasync.md) 方法。 腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。 它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。

如需顯示同步執行相同作業的腳本，請參閱 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。 如需使用直接存取的範例，請參閱 [**在 Class Win32 \_ 進程中建立方法**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。 如需使用 [**SWbemServices**](swbemservices.md) 物件進行相同操作的範例，請參閱 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)。


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
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
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 


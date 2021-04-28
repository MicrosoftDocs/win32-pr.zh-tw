---
description: SWbemServices.ExecMethod 方法-執行方法提供者所匯出的方法。
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecMethod 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 452c42c37e8dcb9f2b37b660b1f8899e587b5579
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103636"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.ExecMethod 方法

[**SWbemServices**](swbemservices.md)物件的 **ExecMethod** 方法會執行方法提供者所匯出的方法。 當轉送至適當提供者的方法執行時，這個方法會封鎖。 然後會傳回信息和狀態。 提供者（而非 WMI）會執行方法。

這個方法是在同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strObjectPath* 
</dt> <dd>

必要。 字串，包含執行方法之物件的物件路徑。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

</dd> <dt>

*strMethodName* 
</dt> <dd>

必要。 物件之方法的名稱。

</dd> <dt>

*objWbemInParams* \[選\]
</dt> <dd>

[**SWbemObject**](swbemobject.md)物件，其中包含所要執行之方法的輸入參數。 根據預設，這個參數是未定義的。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

保留的。 這個值必須為零。

</dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 [**SWbemObject**](swbemobject.md) 物件。 傳回的物件包含要執行之方法的 out 參數和傳回值。

## <a name="error-codes"></a>錯誤碼

**ExecMethod** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

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

在無法直接執行方法的情況下，使用 **SWbemServices.ExecMethod** 作為直接存取來執行 [*提供者方法*](gloss-p.md) 的替代方法。 **ExecMethod** 方法可讓您取得輸出參數（如果提供者提供的話），以及不支援輸出參數的指令碼語言。 否則，叫用方法的建議方法是使用直接存取。 如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

例如，下列程式碼範例會呼叫 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)中的 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)提供者方法，以使用直接存取。


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



這個範例會呼叫 **SWbemServices.ExecMethod** 來執行 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) 方法。 請注意，物件路徑是必要的，因為 **SWbemServices.ExecMethod** 不會在物件上運作，不同于 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



**SWbemServices.Exe的 cMethod** 方法需要物件路徑。 如果腳本已保存 [**SWbemObject**](swbemobject.md) 物件，請使用 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) 方法。

## <a name="examples"></a>範例

下列範例顯示 **ExecMethod** 方法。 腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，該物件代表正在執行 [記事本] 的進程。 它會顯示 [**InParameters**](swbemmethod-inparameters.md) 物件的設定，以及如何從 [**OutParameters**](swbemmethod-outparameters.md) 物件取得結果。 如需顯示以非同步方式執行相同作業的腳本，請參閱 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)。 如需使用直接存取的範例，請參閱 [在 Class Win32 \_ 進程中建立方法](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)。 如需使用 [**SWbemObject**](swbemobject.md)進行相同操作的範例，請參閱 [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)。


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[呼叫提供者方法](calling-a-provider-method.md)
</dt> <dt>

[操作類別和實例資訊](manipulating-class-and-instance-information.md)
</dt> </dl>

 


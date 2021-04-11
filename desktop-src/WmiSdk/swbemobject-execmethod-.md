---
description: '\_SWbemObject 物件的 ExecMethod 方法會執行方法提供者所匯出的方法。'
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: 'SWbemObject.ExecMethod_ 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114868"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.ExecMethod \_ 方法

[**SWbemObject**](swbemobject.md)物件的 **ExecMethod \_** 方法會執行方法提供者所匯出的方法。

當轉送至適當提供者的方法執行時，這個方法會暫停。 然後會傳回信息和狀態。 提供者（而非 WMI）會執行方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strMethodName* \[在\]
</dt> <dd>

必要。 物件之方法的名稱。

</dd> <dt>

*objwbemInParams* \[在中，選擇性\]
</dt> <dd>

這是 [**SWbemObject**](swbemobject.md) 物件，其中包含所執行之方法的輸入參數。 根據預設，這個參數是未定義的。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

如果已指定，則會保留，且必須設定為 0 (零) 。

</dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，它是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功， [**SWbemObject**](swbemobject.md) 物件會傳回。 傳回的物件包含要執行之方法的 out 參數和傳回值。

## <a name="error-codes"></a>錯誤碼

**ExecMethod \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

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

這個方法類似于 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)，但是它會直接在要執行其方法的物件上運作。 例如，下列程式碼範例會呼叫 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)中的 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)提供者方法，並使用 [直接存取](manipulating-class-and-instance-information.md)。


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



此版本會呼叫 **SWbemObject.Exe\_ cMethod** 來執行 [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service)方法。


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



在無法直接執行方法的情況下，使用 **SWbemObject.ExecMethod \_** 作為直接存取來執行 [*提供者方法*](gloss-p.md)的替代方法。 例如，如果您的方法有 out 參數，則您會使用 **SWbemObject.ExecMethod \_** 搭配不支援輸出參數的指令碼語言。 否則，叫用方法的建議方法是使用直接存取。

-   **SWbemObject.ExecMethod \_** 方法會假設 [**SWbemObject**](swbemobject.md)所代表的物件包含要執行的方法。 相較之下， [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 需要物件路徑。 如果您已經取得要執行其方法的物件，請使用 **SWbemObject.ExecMethod \_** 。

## <a name="examples"></a>範例

下列範例顯示 [**ExecMethod**](swbemservices-execmethod.md) 方法。腳本會建立 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 物件，代表執行 [記事本] 的進程。 如需有關如何以非同步方式執行相同作業的腳本詳細資訊，請參閱 [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md)。 如需使用直接存取的範例，請參閱 [**在 Class Win32 \_ 進程中建立方法**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) 。 如需使用 [**SWbemServices**](swbemservices.md) 物件進行相同操作的範例，請參閱 **SWbemServices.ExecMethod**。


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 


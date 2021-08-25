---
description: '\_SWbemObject 物件的 Delete 方法會刪除目前的類別或目前的實例。'
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: 'SWbemObject.Delete_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: db8df81e56db9967db46b88c0587af9b82a6281e7e732b8647059e8bf4f5457a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857378"
---
# <a name="swbemobjectdelete_-method"></a>SWbemObject \_ 方法

[**SWbemObject**](swbemobject.md)物件的 **Delete \_** 方法會刪除目前的類別或目前的實例。 如果動態提供者提供了類別或實例，除非提供者支援類別或實例的刪除，否則有時候無法刪除此物件。 如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

如果有指定，就會保留，且必須為 0 (零) 。

</dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

此參數通常是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **刪除 \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的內容沒有足夠的安全性許可權可刪除物件。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010) 
</dt> <dd>

指定的類別不存在。

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016) 
</dt> <dd>

無法刪除物件。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

物件不存在。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

如果建立了 [**SWbemObject**](swbemobject.md)的新實例，但未提供索引鍵屬性的值， **Delete \_** 方法會失敗。 WindowsManagement Instrumentation (WMI) 會自動產生全域唯一識別碼 (GUID) 值，但 **SWbemObject \_** 不接受 guid 值。 在此情況下， [**SWbemServices**](swbemservices-delete.md)會使用物件路徑運作。 請注意，在將物件認可至 WMI 之後， [**SWbemObject \_ . Put**](swbemobject-put-.md)方法會傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件。

## <a name="examples"></a>範例

下列範例會建立新的類別。加入索引鍵屬性;將新類別寫入至存放庫;並顯示新類別物件的路徑。 腳本接著會產生新類別的實例;寫入它;並顯示路徑。 請注意，腳本只會刪除類別，從儲存機制刪除類別及其實例。


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 





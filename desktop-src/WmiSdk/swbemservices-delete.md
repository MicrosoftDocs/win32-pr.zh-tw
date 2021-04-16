---
description: 刪除物件路徑中指定的類別或實例。 您只能刪除目前命名空間中的物件。
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: 'SWbemServices 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469308"
---
# <a name="swbemservicesdelete-method"></a>SWbemServices 方法

[**SWbemServices**](swbemservices.md)物件的 **Delete** 方法會刪除物件路徑中指定的類別或實例。 您只能刪除目前命名空間中的物件。

如果動態提供者提供類別或實例，除非提供者支援類別或實例的刪除，否則您無法刪除此物件。

這個方法是在同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strObjectPath* 
</dt> <dd>

必要。 字串，包含您要刪除之物件的物件路徑。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

保留的。 這個值必須為零。

</dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **刪除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

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

當物件的索引鍵屬性未指定值時，就可以使用 **SWbemServices** 方法，因為這個方法只需要物件路徑做為輸入。 如果缺少索引鍵值， [**SWbemObject \_**](swbemobject-delete-.md)會失敗的情況下可以使用這個方法。 如果透過 [**SWbemObject \_**](swbemobject-put-.md)將物件認可至 WMI，則會透過呼叫取得 [**SWbemObjectPath**](swbemobjectpath.md)物件。

## <a name="examples"></a>範例

下列範例會建立新的類別、加入非索引鍵的屬性、將新類別寫入存放庫，並顯示新類別物件的路徑。 腳本接著會產生新類別的實例、寫入實例，並顯示路徑。 請注意，腳本會藉由刪除類別，從存放庫中刪除類別和其實例。 如需 WMI 類別和實例的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md) 和 [通用訊息模型](common-information-model.md)。


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
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
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

 





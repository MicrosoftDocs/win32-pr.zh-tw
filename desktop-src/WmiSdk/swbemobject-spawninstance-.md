---
description: 使用 \_ SWbemObject 物件的 SpawnInstance 方法，建立類別的新實例。
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: 'SWbemObject.SpawnInstance_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b465bb53fd031dff397ef0ddf39db39d5d9987f03e037becebcd8dd41a65b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640038"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject. SpawnInstance \_ 方法

使用 [**SWbemObject**](swbemobject.md)物件的 **SpawnInstance \_** 方法，建立類別的新實例。 目前的物件必須是透過 SWbemServices 取得的 WMI 所取得的類別定義，例如 [**Get**](swbemservices-get.md) 或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)。 然後，使用此類別定義來建立新的實例。 在進程內的本機建立每個新的實例，然後呼叫 [**SWbemObject \_**](swbemobject-put-.md) ，以實際在 WMI 內建立實例。

> [!Note]  
> 支援從實例產生實例，但傳回的實例是空的。

 

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

如果已指定，則必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，此呼叫會傳回 [**SWbemObject**](swbemobject.md) 物件，其中包含類別的新實例。

## <a name="error-codes"></a>錯誤碼

**SpawnInstance \_** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020) 
</dt> <dd>

目前的物件不是有效的類別定義，而且無法產生新的實例。 可能是未完成，或尚未使用 [**SWbemObject \_**](swbemobject-put-.md)向 WMI 註冊。

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E) 
</dt> <dd>

如果在實例上使用這個方法，而不是在類別上，則傳回。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject。 Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices。 Get**](swbemservices-get.md)
</dt> </dl>

 

 





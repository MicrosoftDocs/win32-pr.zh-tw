---
description: SWbemObject 物件的子類別方法會傳回 \_ swbemobjectset 搭配使用物件。
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: 'SWbemObject.Subclasses_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979061"
---
# <a name="swbemobjectsubclasses_-method"></a>SWbemObject 類別 \_ 方法

[**SWbemObject**](swbemobject.md)物件的子 **類別 \_** 方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件。 此物件是目前物件的子類別集合，必須是類別。 傳回之集合中的專案可以使用標準的收集方法來取得。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

判斷呼叫列舉詳細程度的整數。 此參數可接受下列值。

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep * * * (0 (0x0) ) 


</dt> <dd>

強制遞迴列舉至所有衍生自指定父類別的子類別。 父類別本身不會在列舉中傳回。

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow * * * (1 (0x1) ) 


</dt> <dd>

此參數的預設值。 它會強制列舉只包含指定之父類別的直屬子類別。

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到呼叫完成為止。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

導致 WMI 傳回類別修訂資料以及基類定義。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。

## <a name="error-codes"></a>錯誤碼

在完成子 **類別 \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010) 
</dt> <dd>

指定的類別不存在。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

如果沒有目前物件的子類別，則傳回的集合不會有零個元素的錯誤。 子 **類別 \_** 方法只適用于類別物件。

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

[**Swbemobjectset 搭配使用**](swbemobjectset.md)
</dt> </dl>

 

 





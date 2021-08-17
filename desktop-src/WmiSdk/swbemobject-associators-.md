---
description: '\_SWbemObject 物件的 associators of 方法會傳回與目前物件相關聯)  (類別或實例的集合。'
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: 'SWbemObject.Associators_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 87458cec77a6b003a6dd35d0fc0f1a39fb785522401b46fa50a515f869760889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857428"
---
# <a name="swbemobjectassociators_-method"></a>SWbemObject. Associators of \_ 方法

[**SWbemObject**](swbemobject.md)物件的 **associators of \_** 方法會傳回與目前物件相關聯)  (類別或實例的集合。 這些傳回的物件稱為端點。 這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strAssocClass* \[在中，選擇性\]
</dt> <dd>

包含關聯類別的字串。 如果有指定，這個參數會指出傳回的端點必須透過指定的關聯類別或衍生自這個關聯類別的類別，與來源產生關聯。

</dd> <dt>

*strResultClass* \[在中，選擇性\]
</dt> <dd>

包含類別名稱的字串。 如果有指定，這個參數會指出傳回的端點必須屬於或衍生自此參數中指定的類別。

</dd> <dt>

*strResultRole* \[在中，選擇性\]
</dt> <dd>

包含屬性名稱的字串。 如果有指定，這個參數表示傳回的端點必須在其與來源物件的關聯中扮演特定的角色。 角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。

</dd> <dt>

*strRole* \[在中，選擇性\]
</dt> <dd>

包含屬性名稱的字串。 如果有指定，這個參數會指出傳回的端點必須參與來源物件的關聯，其中來源物件會扮演特定的角色。 角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。

</dd> <dt>

*bClassesOnly* \[在中，選擇性\]
</dt> <dd>

布林值，指出是否應該傳回類別名稱的清單，而不是類別的實際實例。 這些是端點實例所屬的類別。 此參數的預設值為 **FALSE**。

</dd> <dt>

*bSchemaOnly* \[在中，選擇性\]
</dt> <dd>

這是布林值，指出查詢是否適用于架構，而不是資料。 此參數的預設值為 **FALSE**。 如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。 當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。

</dd> <dt>

*strRequiredAssocQualifier* \[在中，選擇性\]
</dt> <dd>

包含辨識符號名稱的字串。 如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。

</dd> <dt>

*strRequiredQualifier* \[在中，選擇性\]
</dt> <dd>

包含辨識符號名稱的字串。 如果有指定，這個參數表示傳回的端點必須包含指定的限定詞。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

指定作業其他旗標的整數。 這個參數的預設值是 **wbemFlagReturnImmediately**，它會指示立即傳回呼叫，而不是等到查詢完成為止。 此參數可接受下列值。

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * (32 (0x20) ) 


</dt> <dd>

使順向列舉值傳回。 順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * (0 (0x0) ) 


</dt> <dd>

讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到查詢完成為止。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

讓 WMI 以基類定義傳回類別修訂資料。 包含這個旗標可讓當地語系化的描述辨識符號文字可供類別、屬性和方法使用。 如需修改過的限定詞的詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。

## <a name="error-codes"></a>錯誤碼

完成 **associators of \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

如需有關 ASSOCIATORS OF 相關 WQL 查詢、來源實例和端點的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。

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

[**SWbemObject 參考\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 





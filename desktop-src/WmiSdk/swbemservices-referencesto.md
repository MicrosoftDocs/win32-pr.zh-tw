---
description: 傳回參考特定來源類別或實例的所有關聯類別或實例的集合。
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: 'SWbemServices. ReferencesTo 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b703ab1384286ecfc3a797f88ec18cafe8b6142acf586c7f96e4ae9b4085f7cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312497"
---
# <a name="swbemservicesreferencesto-method"></a>SWbemServices. ReferencesTo 方法

[**SWbemServices**](swbemservices.md)物件的 **ReferencesTo** 方法會傳回參考特定來源類別或實例之所有關聯類別或實例的集合。 這個方法會執行 WQL 查詢 [參考](references-of-statement.md) 所執行的相同函數。

這個方法會在半同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strObjectPath* 
</dt> <dd>

必要。 字串，包含此方法之來源的物件路徑。 如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。

</dd> <dt>

*strResultClass* \[選\]
</dt> <dd>

包含類別名稱的字串。 如果有指定，這個參數會指出傳回的關聯物件必須屬於或衍生自此參數中指定的類別。

</dd> <dt>

*strRole* \[選\]
</dt> <dd>

包含屬性名稱的字串。 如果有指定，這個參數表示所傳回的關聯物件必須限制為來源物件扮演特定角色的物件。 角色是由指定之屬性的名稱所定義 (必須是關聯) 的參考屬性。

</dd> <dt>

*bClassesOnly* \[選\]
</dt> <dd>

布林值，指出是否應該傳回類別名稱清單，而不是類別的實際實例。 這些是關聯物件所屬的類別。 此參數的預設值為 **FALSE**。

</dd> <dt>

*bSchemaOnly* \[選\]
</dt> <dd>

指出查詢是否適用于架構而非資料的布林值。 此參數的預設值為 **FALSE**。 如果 *strObjectPath* 參數指定類別的物件路徑，它只能設定為 **TRUE** 。 當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。

</dd> <dt>

*strRequiredQualifier* \[選\]
</dt> <dd>

包含辨識符號名稱的字串。 如果有指定，這個參數會指出傳回的關聯物件必須包含指定的限定詞。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

指定運算其他旗標的整數。 這個參數的預設值是 **wbemFlagReturnImmediately**，它會指示立即傳回呼叫，而不是等到查詢完成為止。 此參數可接受下列值。

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * (32 (0x20) ) 


</dt> <dd>

使順向列舉值傳回。 順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * (0 (0x0) ) 


</dt> <dd>

造成 Windows Management Instrumentation (WMI) 保留列舉物件的指標，直到用戶端釋放列舉值為止。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到查詢完成為止。 此旗標會在同步模式中呼叫方法。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

導致 WMI 傳回類別修訂資料以及基類定義。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。

## <a name="error-codes"></a>錯誤碼

**ReferencesTo** 方法完成後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

> [!Note]  
> 具有零個元素的傳回集合不是錯誤。

 

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

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemFlagUseAmendedQualifiers** -131072 (0x20000) 
</dt> <dd>

讓 WMI 以基類定義傳回類別修訂資料。

</dd> </dl>

## <a name="remarks"></a>備註

如需相關 WQL 查詢、來源實例和關聯物件之參考的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。

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

[**SWbemObject. Associators of\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject 參考\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 





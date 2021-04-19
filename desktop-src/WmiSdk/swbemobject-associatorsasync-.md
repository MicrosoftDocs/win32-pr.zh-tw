---
description: SWbemObject 的 AssociatorsAsync \_ 方法會取得與目前物件相關聯 (類別或實例) 的物件。 這些物件稱為端點。 這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: 'SWbemObject.AssociatorsAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974189"
---
# <a name="swbemobjectassociatorsasync_-method"></a>SWbemObject. AssociatorsAsync \_ 方法

[**SWbemObject**](swbemobject.md)的 **AssociatorsAsync \_** 方法會取得與目前物件相關聯 (類別或實例) 的物件。 這些物件稱為端點。 這個方法會執行 WQL 查詢 ASSOCIATORS OF 所執行的相同功能。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemSink* \[在\]
</dt> <dd>

必要。 以非同步方式接收物件作為回呼的物件接收。

</dd> <dt>

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

指出查詢是否適用于架構而非資料的布林值。 此參數的預設值為 **FALSE**。 如果叫用此方法的物件為類別，則只能設定為 **TRUE** 。 當設為 **TRUE** 時，傳回的端點集會代表與架構中的來源類別適當相關聯的類別。

</dd> <dt>

*strRequiredAssocQualifier* \[在中，選擇性\]
</dt> <dd>

包含辨識符號名稱的字串。 如果有指定，這個參數會指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。

</dd> <dt>

*strRequiredQualifier* \[在中，選擇性\]
</dt> <dd>

包含辨識符號名稱的字串。 如果有指定，這個參數會指出傳回的端點必須包含指定的限定詞。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

指定作業其他旗標的整數。 此參數可接受下列值。

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * (131072 (0x20000) ) 


</dt> <dd>

導致 WMI 傳回當地語系化的類別和屬性描述。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[在中，選擇性\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> <dt>

*objWbemAsyncCoNtext* \[在中，選擇性\]
</dt> <dd>

這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。 如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。 若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。 這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。 在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。

## <a name="error-codes"></a>錯誤碼

完成 **AssociatorsAsync \_** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。

</dd> <dt>

**wbemErrFailed** -2147449889 (0x7FFF7C21) 
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

</dd> </dl>

## <a name="remarks"></a>備註

此呼叫會立即傳回。 要求的物件和狀態會透過傳送至 *objWbemSink* 中指定之接收的呼叫傳回給呼叫端。 若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。 傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用兩個同步通訊或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需有關 ASSOCIATORS OF 相關 WQL 查詢、來源實例和端點的詳細資訊，請參閱 [語句 associators of](associators-of-statement.md)。

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

[**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject 參考\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 


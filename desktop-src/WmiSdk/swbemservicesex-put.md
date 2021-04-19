---
description: 傳回 SWbemObjectPath 物件，其中包含寫入資料的物件路徑。
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: 'SWbemServicesEx： Put 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974597"
---
# <a name="swbemservicesexput-method"></a>SWbemServicesEx Put 方法

[**SWbemServicesEx**](swbemservicesex.md)物件的 **Put** 方法會將物件儲存至系結至物件的命名空間，並傳回 [**SWbemObjectPath**](swbemobjectpath.md)物件，其中包含寫入資料的物件路徑。

這個方法會在半同步模式中呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemObject* 
</dt> <dd>

必要。 要放入命名空間中的新物件。 這可以是新建立的物件或修改過的物件。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

此參數會判斷呼叫是否建立或更新物件，以及呼叫是否立即傳回。 此參數可接受下列值。

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0) ) 


</dt> <dd>

如果沒有衍生類別且沒有該類別的實例，則允許更新類別。 如果變更僅限於不 (重要的辨識符號（例如， **描述** 辨識符號) ），也可以在所有情況下進行更新。 這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。 如果類別有實例，則更新會失敗。

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20) ) 


</dt> <dd>

即使在有子類別時，也允許更新類別，但變更不會造成與子類別的任何衝突。 將新屬性加入至先前未在任何子類別中提及的基類時，您可以使用此旗標。 如果類別有實例，則更新會失敗。

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40) ) 


</dt> <dd>

當有衝突的子類別存在時，此旗標會強制更新類別。 例如，此旗標會在子類別中定義類別限定詞時強制進行更新，而且基類會嘗試在與現有限定詞衝突的情況下加入相同的限定詞。 在強制模式中，在子類別中刪除衝突的辨識符號，即可解決此衝突。 如果類別有實例，則更新會失敗。

使用強制模式來更新靜態類別，會導致刪除該類別的所有實例。 提供者類別的強制更新不會刪除類別的實例。

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0) ) 


</dt> <dd>

如果類別或實例不存在，則會加以建立，如果已經存在，則會予以覆寫。

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2) ) 


</dt> <dd>

僅用於建立。 如果類別或實例已經存在，呼叫就會失敗。

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1) ) 


</dt> <dd>

導致此呼叫只進行更新。 類別或實例必須存在，呼叫才能成功。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到作業完成為止。 此旗標會在同步模式中呼叫方法。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000) ) 


</dt> <dd>

導致 WMI 撰寫類別修訂資料和基類定義。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功，則會傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件。 此物件包含已成功認可至 WMI 之實例或類別的物件路徑。

## <a name="error-codes"></a>錯誤碼

完成 **Put** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有操作的許可權。

</dd> <dt>

**wbemErrAlreadyExists** -2147749913 (0x80041019) 
</dt> <dd>

指定了 **wbemChangeFlagCreateOnly** 旗標，但該實例已經存在。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrIllegalNull** -2147749898 (0x8004100A) 
</dt> <dd>

針對不能為 **null** 的屬性，指定了 **null** 值。 這類屬性的範例之一，是由 **索引**[**鍵**](standard-qualifiers.md)、索引或 **非 \_ Null** 的辨識符號標記。

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014) 
</dt> <dd>

指定的物件無效。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

指定了 **wbemChangeFlagUpdateOnly** 旗標，但實例或類別不存在。

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020) 
</dt> <dd>

尚未設定類別的必要屬性。

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
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



 

 





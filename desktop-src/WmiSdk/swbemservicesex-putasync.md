---
description: 以非同步方式將物件儲存到命名空間。 成功時，這個方法會將 OnCompleted 事件傳送至指定為輸入參數的 SWbemSink 物件。
ms.assetid: 27da0c60-6dae-482d-a9bf-1aab016d3ae8
ms.tgt_platform: multiple
title: 'SWbemServicesEx. PutAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
- ISWbemServicesEx.PutAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 06f470ed6f8cbd497ba3d3a3a77c5a8b4e5748c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027072"
---
# <a name="swbemservicesexputasync-method"></a>SWbemServicesEx. PutAsync 方法

[**SWbemServicesEx**](swbemservicesex.md)物件的 **PutAsync** 方法會以非同步方式將物件儲存到命名空間。 成功時，這個方法會將 [**OnCompleted**](swbemsink-oncompleted.md) 事件傳送至指定為輸入參數的 [**SWbemSink**](swbemsink.md) 物件。

在非同步模式中呼叫這個方法。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemServicesEx.PutAsync( _
  ByVal objWbemSink, _
  ByVal ojbWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemSink* 
</dt> <dd>

必要。 以非同步方式接收物件的物件接收。 建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。

</dd> <dt>

*ojbWbemObject* 
</dt> <dd>

必要。 要放入命名空間中的新物件。 這可能是新建立的物件或修改過的物件。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

此參數會決定呼叫是建立或更新物件，以及呼叫是否立即傳回。 此參數可接受下列值。

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0) ) 


</dt> <dd>

允許在沒有衍生類別且沒有類別的實例時，更新類別。 當變更僅限於不重要的辨識符號（例如， **描述** 辨識符號）時，它也可讓您在所有情況下進行更新。 這是此呼叫的預設行為，而且會用於與舊版 WMI 的相容性。 如果類別有實例，則更新會失敗。

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20) ) 


</dt> <dd>

即使有子類別且變更不會導致與子類別發生衝突，還是允許更新類別。 將新屬性加入至先前未在任何子類別中提及的基類時，請使用此旗標。 如果類別有實例，則更新會失敗。

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40) ) 


</dt> <dd>

當有衝突的子類別存在時，此旗標會強制更新類別。 例如，當類別限定詞在子類別中定義時，此旗標會強制進行更新，而且基類會嘗試在與現有的限定詞衝突時，加入相同的限定詞。 在強制模式中，在子類別中刪除衝突的辨識符號，即可解決此衝突。 如果類別有實例，則更新會失敗。

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

導致此呼叫更新。 類別或實例必須存在，呼叫才能成功。

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10) ) 


</dt> <dd>

導致呼叫立即返回。

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0) ) 


</dt> <dd>

導致此呼叫封鎖，直到查詢完成為止。 此旗標會在同步模式中呼叫方法。

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000) ) 


</dt> <dd>

導致 WMI 撰寫類別修訂資料和基類定義。 如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> <dt>

*objWbemAsyncCoNtext* \[選\]
</dt> <dd>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。 使用這個參數可使用相同的物件接收進行多個非同步呼叫。 若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。 這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 如果呼叫成功，所提供之物件接收的 [**OnObjectPut**](swbemsink-onobjectput.md) 事件會接收 [**SWbemObjectPath**](swbemobjectpath.md) 物件，其中包含已成功認可至 WMI 之實例或類別的物件路徑。

## <a name="error-codes"></a>錯誤碼

**PutAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003) 
</dt> <dd>

目前的使用者沒有更新指定類別之實例的許可權。

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

針對不能為 Null 的屬性，指定了 Null 值。 這類屬性的範例之一，是由 **索引****鍵**、索引或 **非 \_ Null** 的辨識符號標記。

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014) 
</dt> <dd>

所指定的執行個體無效。

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

## <a name="remarks"></a>備註

這個呼叫會立即傳回，而結果和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫端。 若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。 在所有物件抵達之後完成的任何處理，都是在 *objWbemSink* 的副程式中完成。[**OnCompleted**](swbemsink-oncompleted.md) 事件。

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。

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



 


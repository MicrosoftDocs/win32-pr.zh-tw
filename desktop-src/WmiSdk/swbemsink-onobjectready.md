---
description: 當非同步作業傳回物件時，會觸發 SWbemSink 物件的 OnObjectReady 事件。
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnObjectReady 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114845"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>ISWbemSinkEvents：： OnObjectReady 事件

當非同步作業傳回物件時，會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnObjectReady** 事件。 您可以使用此事件來處理非同步呼叫的物件，例如 [**SWbemObject \_ . InstancesAsync**](swbemobject-instancesasync-.md)或 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)。 **OnObjectReady** 會每次都傳回一個 [**SWbemObject**](swbemobject.md) ，直到列舉完成為止。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemObject* 
</dt> <dd>

[**SWbemObject**](swbemobject.md)物件。 這與觸發這個事件之非同步呼叫的同步對等專案所傳回的內容類別似。 例如，對 [**SWbemServices. GetAsync**](swbemservices-getasync.md)方法的呼叫會在 [**OnObjectReady**](swbemsink.md)物件之 **SWbemSink** 事件 *的 objWbemObject* 參數中傳回 **SWbemObject** ，該物件會以原始呼叫的 *objWbemObject* 參數形式傳遞。 您可以使用對 [**SWbemServices**](swbemservices-get.md)的對等同步呼叫來取得相同的 **SWbemObject** 物件。

</dd> <dt>

*objWbemAsyncCoNtext* 
</dt> <dd>

傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。 使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="error-codes"></a>錯誤碼

**OnObjectReady** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015) 
</dt> <dd>

發生網路錯誤，導致無法正常運作。

</dd> </dl>

## <a name="remarks"></a>備註

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用半同步通訊或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>wbemdisp.tlb .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 


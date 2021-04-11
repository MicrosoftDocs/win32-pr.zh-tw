---
description: 非同步呼叫完成時，會觸發 SWbemSink 物件的 OnCompleted 事件。 此事件表示用戶端應用程式、非同步作業的結果，並提供非同步呼叫失敗時的錯誤資訊。
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnCompleted 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114849"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>ISWbemSinkEvents：： OnCompleted 事件

非同步呼叫完成時，會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnCompleted** 事件。 此事件表示用戶端應用程式、非同步作業的結果，並提供非同步呼叫失敗時的錯誤資訊。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iHResult* 
</dt> <dd>

已完成之非同步方法的 HRESULT。 HRESULT 與針對 WMI 方法呼叫的對等 [COM API](com-api-for-wmi.md) 所傳回的值相同。 檢查此值以判斷非同步呼叫是否成功。 如果非同步呼叫成功，則此參數會包含 WBEM \_ S \_ ， \_ (0) 不會發生錯誤。 如果非同步呼叫失敗，此參數會包含錯誤碼。

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

當非同步方法失敗時，包含 [**SWbemLastError**](swbemlasterror.md) 物件。

</dd> <dt>

*objWbemAsyncCoNtext* 
</dt> <dd>

這是傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。 使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **OnCompleted** 事件之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列其中一個錯誤碼。

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

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用最半同步或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

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



 


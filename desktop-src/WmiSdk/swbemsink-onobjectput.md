---
description: 當非同步 Put 作業完成時，就會觸發 SWbemSink 物件的 OnObjectPut 事件。 此事件會傳回實例或已儲存類別的物件路徑。
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'ISWbemSinkEvents：： OnObjectPut 事件 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 81f012d6156e6ec17c609bec5be2bc355a0bd9bf197b139a7da2a494285a1c87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030398"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>ISWbemSinkEvents：： OnObjectPut 事件

當非同步 Put 作業完成時，就會觸發 [**SWbemSink**](swbemsink.md)物件的 **OnObjectPut** 事件。 此事件會傳回實例或已儲存類別的物件路徑。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemObjectPath* 
</dt> <dd>

[**SWbemObjectPath**](swbemobjectpath.md)物件，其中包含 put 作業寫入至 WMI 之實例或類別的物件路徑。

</dd> <dt>

*objWbemAsyncCoNtext* 
</dt> <dd>

傳遞至原始非同步呼叫的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。 使用這個參數來識別非同步呼叫的來源，此呼叫會在使用這個物件接收進行多個非同步呼叫時觸發這個事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="error-codes"></a>錯誤碼

**OnObjectPut** 事件完成之後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列其中一個錯誤碼。

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

> [!Note]  
> 非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用半同步通訊或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>Wbemdisp.tlb .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 


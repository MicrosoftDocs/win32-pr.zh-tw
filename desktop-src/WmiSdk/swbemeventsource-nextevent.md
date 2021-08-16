---
description: 如果有可用的事件，SWbemEventSource 物件的 NextEvent 方法就會從事件查詢中抓取事件。
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: 'SWbemEventSource. NextEvent 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6ce39d442b48f32c2aafcd6e24c1c214dce82a19435b6b36bce65d5426161859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050066"
---
# <a name="swbemeventsourcenextevent-method"></a>SWbemEventSource. NextEvent 方法

如果有可用的事件， [**SWbemEventSource**](swbemeventsource.md)物件的 **NextEvent** 方法就會從事件查詢中抓取事件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iTimeoutMs* \[在中，選擇性\]
</dt> <dd>

在傳回逾時錯誤之前，呼叫等候事件的毫秒數。 這個參數的預設值是 **wbemTimeoutInfinite** (-1) ，它會將呼叫指示無限期等候。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **NextEvent** 方法成功，它會傳回 [**SWbemObject**](swbemobject.md) 物件，其中包含所要求的事件。 如果呼叫超時，傳回的物件會是 **Null** ，並引發錯誤。

## <a name="error-codes"></a>錯誤碼

**NextEvent** 方法完成後， **Err** 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

要求的事件未在 ITimeoutMs 中指定的時間量內到達 *。*

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 





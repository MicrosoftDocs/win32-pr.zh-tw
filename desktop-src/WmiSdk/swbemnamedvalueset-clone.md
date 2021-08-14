---
description: SWbemNamedValueSet 物件的 Clone 方法會傳回新的物件，這個物件是目前集合的複製。
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 複製方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9158901a39fa80e49404912ee5458c416069bbe354e19059ef4622ae4257fda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314189"
---
# <a name="swbemnamedvaluesetclone-method"></a>SWbemNamedValueSet 複製方法

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **clone** 方法會傳回新的物件，這個物件是目前集合的複製。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則會傳回新的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。

## <a name="error-codes"></a>錯誤碼

**複製** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法複製物件。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用這個方法來複製 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 





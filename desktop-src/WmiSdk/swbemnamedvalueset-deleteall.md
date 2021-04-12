---
description: SWbemNamedValueSet 物件的 DeleteAll 方法會從集合中移除所有命名值，因此請將它清空。
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet. DeleteAll 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193260"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a>SWbemNamedValueSet. DeleteAll 方法

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **DeleteAll** 方法會從集合中移除所有命名值，因此請將它清空。

## <a name="syntax"></a>語法


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

**DeleteAll** 方法完成後， **Err** 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> <dt>

[**SWbemNamedValueSet。移除**](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 





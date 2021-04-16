---
description: SWbemNamedValueSet 物件的 Item 方法會從集合取得 SWbemNamedValue 物件。
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512980"
---
# <a name="swbemnamedvaluesetitem-method"></a>SWbemNamedValueSet 專案方法

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Item** 方法會從集合取得 [**SWbemNamedValue**](swbemnamedvalue.md)物件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 要取出的值名稱。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 如果有指定，此值必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回要求的 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。

## <a name="error-codes"></a>錯誤碼

當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效，或無法剖析命名空間。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的項目。

</dd> </dl>

## <a name="remarks"></a>備註

如需新增和取出命名值的範例，請參閱 [**SWbemNamedValue。**](swbemnamedvalue-value.md)

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
</dt> </dl>

 

 





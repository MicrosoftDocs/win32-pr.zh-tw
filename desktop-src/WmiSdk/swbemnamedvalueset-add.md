---
description: SWbemNamedValueSet 物件的 Add 方法會將 SWbemNamedValue 物件加入至集合。 如果專案已經存在相同名稱的集合中，則新的元素會取代它。
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512981"
---
# <a name="swbemnamedvaluesetadd-method"></a>SWbemNamedValueSet 新增方法

[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Add** 方法會將 [**SWbemNamedValue**](swbemnamedvalue.md)物件加入至集合。 如果專案已經存在相同名稱的集合中，則新的元素會取代它。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 新值的名稱。

</dd> <dt>

*varVal* \[在\]
</dt> <dd>

必要。 表示新值的 Variant。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

如果有指定，則必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回新修改或新建立的 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。

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

 

 





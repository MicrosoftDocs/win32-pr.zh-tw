---
description: 內含物件的 Remove 方法會刪除內含集合中的屬性。
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: '內含： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114864"
---
# <a name="swbempropertysetremove-method"></a>內含方法

[**內含**](swbempropertyset.md)物件的 **Remove** 方法會刪除 **內含** 集合中的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 要移除之專案的名稱。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 如果有指定，此值必須為 0 (零) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **移除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的失敗。

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016) 
</dt> <dd>

使用者嘗試刪除無法刪除的屬性。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

指定的屬性不存在。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法執行此方法。

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380) 
</dt> <dd>

使用者嘗試刪除未擁有的屬性。 屬性繼承自父代 (Parent) 類別。

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002) 
</dt> <dd>

使用者已刪除目前類別的覆寫預設值。 父類別中這個屬性的預設值已重新開機。

</dd> </dl>

## <a name="remarks"></a>備註

無法從類別實例或具有繼承屬性的衍生類別移除屬性。 這類刪除嘗試會引發錯誤，而且不會移除屬性;屬性會重設為其預設值。

您無法在移除專案時逐一查看集合，因為當您從集合中移除專案時，集合指標會移至下一個元素。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

## <a name="examples"></a>範例

如需使用此方法的程式碼範例，請參閱 [**內含**](swbempropertyset.md) 主題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ 內含<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**內含**](swbempropertyset.md)
</dt> <dt>

[**內含新增**](swbempropertyset-add.md)
</dt> </dl>

 

 





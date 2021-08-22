---
description: SWbemQualifierSet 物件的 Remove 方法會從集合中刪除已命名的辨識符號。
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: 'SWbemQualifierSet： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f4ca62276e39822964d33b58345b4718354bfd63039ec42ab30ac5daf95f6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463608"
---
# <a name="swbemqualifiersetremove-method"></a>SWbemQualifierSet 方法

[**SWbemQualifierSet**](swbemqualifierset.md)物件的 **Remove** 方法會從集合中刪除已命名的辨識符號。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 要移除的辨識符號名稱。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 預設值為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="error-codes"></a>錯誤碼

完成 **移除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

*IFlags* 參數無效。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

指定的限定詞不存在。

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016) 
</dt> <dd>

移除此辨識符號不合法。

</dd> </dl>

## <a name="remarks"></a>備註

您無法在移除專案時逐一查看集合，因為當您從集合中移除專案時，集合指標會移至下一個元素。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet 新增**](swbemqualifierset-add.md)
</dt> </dl>

 

 





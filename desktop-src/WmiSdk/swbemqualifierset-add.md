---
description: SWbemQualifierSet 物件的 Add 方法會將 SWbemQualifier 物件加入至 SWbemQualifierSet 集合。 如果集合中已經存在具有相同名稱的辨識符號，則會予以取代。
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: 'SWbemQualifierSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320656"
---
# <a name="swbemqualifiersetadd-method"></a>SWbemQualifierSet 新增方法

[**SWbemQualifierSet**](swbemqualifierset.md)物件的 **Add** 方法會將 [**SWbemQualifier**](swbemqualifier.md)物件加入至 **SWbemQualifierSet** 集合。 如果集合中已經存在具有相同名稱的辨識符號，則會予以取代。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 新限定詞的名稱。

</dd> <dt>

*varVal* \[在\]
</dt> <dd>

必要。 新限定詞的變異值。

</dd> <dt>

*bPropagatesToSubclasses* \[在中，選擇性\]
</dt> <dd>

布林值，指出這個新的辨識符號是否會傳播至子類別。 預設值為 **TRUE**。

</dd> <dt>

*bPropagatesToInstances* \[在中，選擇性\]
</dt> <dd>

布林值，指出這個新的辨識符號是否會傳播至實例。 預設值為 **TRUE**。

</dd> <dt>

*bOverridable* \[在中，選擇性\]
</dt> <dd>

指出是否可以在傳播時覆寫此限定詞的布林值。 預設值為 **TRUE**。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 預設值為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回代表新辨識符號的 [**SWbemQualifier**](swbemqualifier.md) 物件。 否則，會傳回 **null** 物件。

## <a name="error-codes"></a>錯誤碼

完成 **Add** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

*IFlags* 參數無效。

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrCannotBeKey** -2147749919 (0x8004101F) 
</dt> <dd>

在不能是索引鍵的屬性上，指定索引 **鍵** 限定詞的嘗試不合法。 索引鍵會在物件的類別定義中指定，並且不能對每個執行個體進行變更。

</dd> <dt>

**wbemErrInvalidQualifierType** -2147749929 (0x80041029) 
</dt> <dd>

*VarVal* 參數不是合法的辨識符號類型。

</dd> <dt>

**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A) 
</dt> <dd>

因為擁有物件不允許覆寫，所以無法對此限定詞執行 **SWbemQualifierSet。**

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet。移除**](swbemqualifierset-remove.md)
</dt> </dl>

 

 





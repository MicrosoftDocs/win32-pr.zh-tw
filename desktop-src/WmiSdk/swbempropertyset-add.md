---
description: 內含物件的 Add 方法會將 Swbempropertyset 物件加入至內含集合。 如果集合中已經有相同名稱的屬性，則會將其內容取代為新的定義。
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: '內含： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975488"
---
# <a name="swbempropertysetadd-method"></a>內含新增方法

[**內含**](swbempropertyset.md)物件的 **Add** 方法會將 [**swbempropertyset**](swbemproperty.md)物件加入至 **內含** 集合。 如果集合中已經有相同名稱的屬性，則會將其內容取代為新的定義。

> [!Note]  
> 在這項作業之後，已加入的屬性值為 **Null** (未指派) 。 若要設定或變更 WMI 屬性的值，您必須設定所傳回之 [**swbempropertyset**](swbemproperty.md)物件的 [**value**](swbemdatetime-value.md)屬性。

 

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 新屬性的名稱。

</dd> <dt>

*iCIMType* \[在\]
</dt> <dd>

必要。 整數，表示新屬性的 **CIMType** 限定詞。 如需 **CIMType** 辨識符號及其值的清單，請參閱 [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) 。

</dd> <dt>

*bIsArray* \[在中，選擇性\]
</dt> <dd>

指定屬性是否為數組類型。 此參數的預設值為 **FALSE**。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

如果已指定，則必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回代表新屬性的 [**swbempropertyset**](swbemproperty.md) 物件。 否則，會傳回 **null** 物件。

## <a name="error-codes"></a>錯誤碼

完成 **Add** 方法之後， **Err** 物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的失敗。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法執行此方法。

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

無法辨識 **CIMType** 限定詞。

</dd> </dl>

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

[**內含。移除**](swbempropertyset-remove.md)
</dt> <dt>

[**Swbempropertyset。值**](swbemproperty-value.md)
</dt> </dl>

 

 





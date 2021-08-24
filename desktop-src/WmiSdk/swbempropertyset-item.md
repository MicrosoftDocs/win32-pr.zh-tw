---
description: 內含物件的 Item 方法會從集合取得名為 Swbempropertyset。 這是這個物件的預設方法。
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: '內含專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: afd0aede44effb14005f111429e365e6831df0d2cae8d1d0685539620c696723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897958"
---
# <a name="swbempropertysetitem-method"></a>內含專案方法

[**內含**](swbempropertyset.md)物件的 **Item** 方法會從集合取得名為 [**swbempropertyset**](swbemproperty.md) 。 這是這個物件的預設方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 要取得之屬性的名稱。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 如果有指定，此值必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回要求的 [**swbempropertyset**](swbemproperty.md) 物件。

## <a name="error-codes"></a>錯誤碼

完成 **專案** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的失敗。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749896
</dt> <dd>

記憶體不足，無法執行此方法。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ 內含<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



 

 





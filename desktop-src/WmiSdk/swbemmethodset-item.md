---
description: SWbemMethodSet 物件的 Item 方法會從集合傳回名為 SWbemMethod 的物件。
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: 'SWbemMethodSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986837"
---
# <a name="swbemmethodsetitem-method"></a>SWbemMethodSet 專案方法

[**SWbemMethodSet**](swbemmethodset.md)物件的 **Item** 方法會從集合傳回名為 [**SWbemMethod**](swbemmethod.md)的物件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strName* \[在\]
</dt> <dd>

必要。 要取出之方法的名稱。

</dd> <dt>

*iFlags* \[在中，選擇性\]
</dt> <dd>

保留的。 預設值為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，要求的 [**SWbemMethod**](swbemmethod.md) 物件就會傳回。

## <a name="error-codes"></a>錯誤碼

當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

*IFlags* 參數無效。

</dd> <dt>

**wbemErrFailed** -2147749894
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

指定的方法不存在。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 





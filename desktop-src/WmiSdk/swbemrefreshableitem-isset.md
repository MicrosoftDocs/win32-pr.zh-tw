---
description: SWbemRefreshableItem. IsSet 屬性是布林值，指出 SWbemRefreshableItem 物件是否代表單一物件或物件集。SWbemRefreshableItem 物件代表單一物件或物件集。
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem. IsSet 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312917"
---
# <a name="swbemrefreshableitemisset-property"></a>SWbemRefreshableItem. IsSet 屬性

**SWbemRefreshableItem. IsSet** 屬性是布林值，指出 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件是否代表單一物件或物件集。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果 **SWbemRefreshableItem** 為 **TRUE**，則專案代表 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件，且 [**物件**](swbemrefreshableitem-object.md) 屬性將會是 **Null**。 如果 **為 FALSE**，則表示專案代表 [**SWbemObject**](swbemobject.md) 物件，而 **物件** 屬性為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 





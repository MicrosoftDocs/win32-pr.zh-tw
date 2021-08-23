---
description: Swbempropertyset 物件的 CIMType 屬性是一個整數，可用來判斷這個屬性的 CIM 型別。 這是唯讀的屬性。
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: 'Swbempropertyset. CIMType 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f3b92cca8d17af8814a7891d0d4f97c7e003b1a999a42c63b6abe59d50e8ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991928"
---
# <a name="swbempropertycimtype-property"></a>Swbempropertyset. CIMType 屬性

[**Swbempropertyset**](swbemproperty.md)物件的 **CIMType** 屬性是一個整數，可用來判斷這個屬性的 CIM 型別。 這是唯讀的屬性。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如需這個屬性之有效類型的詳細資訊，請參閱 [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)。

内嵌物件的實例會儲存在綜合物件中，做為 **CIM \_ 物件** 類型的屬性。 若要在複合類別的實例中判斷内嵌物件的類別，您必須檢查 **CIM \_ 物件** 類型屬性的 **CIMType** 限定詞。

關聯類別中的物件參考會儲存在 **CIM \_ 參考** 類型的屬性中。 若要判斷實際的物件路徑，您必須檢查 **CIM \_ 參考** 型別屬性的 **CIMType** 限定詞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbempropertyset<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 





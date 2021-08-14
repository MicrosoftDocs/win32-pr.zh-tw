---
title: 'EM_INSERTTABLE 訊息 (Richedit .h) '
description: 插入一或多個具有空白資料格的相同資料表資料列。
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a015ae2b9a886ddfa24591944f3f70eca8cb192af771c821df9e4a403c837d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413056"
---
# <a name="em_inserttable-message"></a>EM \_ INSERTTABLE 訊息

插入一或多個具有空白資料格的相同資料表資料列。


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)結構的指標。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果插入資料表，則傳回，否則傳回錯誤碼。

## <a name="remarks"></a>備註

如果 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)的 **cpStartRow** 成員是1，則此訊息會刪除選取的文字 (如果有任何) ，然後使用 *wParam* 和 *lParam* 所指定的資料列和資料格參數插入空的資料表資料列。 它會將選取範圍指向第一個資料列中第一個資料格的開頭。 然後，用戶端可以將選取範圍 (或 [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) 指向各種資料格結束記號，然後插入並格式化所需的文字，以填入資料表單元格。 這類文字可以包含內嵌的資料表資料列。 或者，如果 **TABLEROWPARMS** 的 **cpStartRow** 成員為0或更大，則會在 **cpStartRow** 指定的字元位置插入資料表資料列。 只有在選取的文字中插入資料表時，才會變更目前的選取範圍。

Microsoft Rich Edit 資料表是由一連串的資料表資料列所組成，而這些資料列會由段落順序組成。 資料表資料列會以特殊的雙字元分隔符號（U + FFF9 U + 000D）開頭，並以兩個字元的分隔符號段落 U + FFFB U + 000D 做為結尾。 每個資料格都會以儲存格標記 U + 0007 來結束，如同 U + 000D (CR) 為。 資料表資料列和資料格參數會被視為資料表資料列分隔符號的特殊段落格式。 格式包含 [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) 結構中的資訊。 [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)結構所指定的資料格參數會儲存在擴充版的索引標籤陣列中。 此格式可讓資料表嵌套在其他資料表中，最多可達十五個層級。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 






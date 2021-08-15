---
title: 編輯方塊. editStyle
description: EditStyle 屬性會指定或抓取編輯方塊控制項的樣式。
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- 編輯方塊. editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d40d1933c68c4e34707f01a4d425045c773297e8567ba8ea13a88c6fbc57c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749459"
---
# <a name="editboxeditstyle"></a>編輯方塊. editStyle

**EditStyle** 屬性會指定或抓取編輯方塊控制項的樣式。

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>可能的值

這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。



| 值     | 描述                                                                     |
|-----------|---------------------------------------------------------------------------------|
| 正常    | 預設值。 在單一行上顯示一般文字。                                 |
| 密碼  |  () 顯示星號 \* 來取代文字。 只能在設計階段指定。 |
| 小寫 | 將文字顯示為全部大寫。                                                 |
| 小寫 | 將文字顯示為全部小寫。                                                 |
| number    | 只會顯示數位。                                                          |
| 適用 | 顯示多行文字。 只能在設計階段指定。          |



 

## <a name="remarks"></a>備註

這個屬性只能在設計階段設定為 "password" 或 "多行"。 如果設定為 "多行"，就無法在執行時間變更該值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> </dl>

 

 






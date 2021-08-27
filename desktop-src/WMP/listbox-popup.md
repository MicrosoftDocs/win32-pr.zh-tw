---
title: LISTBOX. popUp
description: PopUp 屬性指定一個值，指出專案是否代表 popUp 或清單方塊控制項。
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996438"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

**PopUp** 屬性指定一個值，指出專案是否代表 popUp 或清單方塊控制項。

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>可能的值

這個屬性是在設計階段指定的 **布林值** 。



| 值 | 描述                                |
|-------|--------------------------------------------|
| true  | 元素代表 popup 控制項。    |
| false | 元素代表清單方塊控制項。 |



 

## <a name="remarks"></a>備註

**POPUP** 元素表示只有在需要時才會顯示的清單方塊控制項。 它與 **LISTBOX** 元素相同，但這個屬性的預設值除外，後者會變更顯示行為。 若為 **LISTBOX** 元素，預設值為 false。 針對 **POPUP** 元素，預設值為 true。 **LISTBOX** 或 **POPUP** 元素應該根據所需的行為來使用，而不是指定此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> <dt>

[**POPUP 元素**](popup-element.md)
</dt> </dl>

 

 






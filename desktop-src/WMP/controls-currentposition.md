---
title: CurrentPosition
description: CurrentPosition 屬性會指定或抓取媒體專案中的目前位置（以秒為單位）。
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- CurrentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993225"
---
# <a name="controlscurrentposition"></a>CurrentPosition

**CurrentPosition** 屬性會指定或抓取媒體專案中的目前位置（以秒為單位）。

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**雙**) 的讀/寫 **號碼**。

## <a name="examples"></a>範例

下列範例會使用 **currentPosition** 來搜尋使用者提供的位置。 系統會建立 HTML 按鈕元素來執行 JScript 程式碼。 系統會建立名為 setPosition 的 HTML 文字輸入元素，以從使用者接受值（以秒為單位）。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> </dl>

 

 






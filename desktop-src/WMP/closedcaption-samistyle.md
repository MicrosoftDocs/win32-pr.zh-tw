---
title: ClosedCaption.SAMIStyle
description: SAMIStyle 屬性會指定或抓取隱藏式輔助字幕樣式。
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIStyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990589"
---
# <a name="closedcaptionsamistyle"></a>ClosedCaption.SAMIStyle

**SAMIStyle** 屬性會指定或抓取隱藏式輔助字幕樣式。

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

薩米文檔案可以包含數個格式樣式定義。 薩米文的樣式定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。 樣式的定義是以文字字串前面加上 \# 字元。 例如：


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



這會指定產生特定字型的樣式。

如果未指定薩米體樣式，預設會使用薩米文檔案中所定義的第一個樣式。

**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。

## <a name="examples"></a>範例

下列 JScript 範例會建立使用 *closedCaption* 的 HTML SELECT 元素。**SAMIStyle** ，以變更隱藏式輔助字幕文字的外觀。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> </dl>

 

 






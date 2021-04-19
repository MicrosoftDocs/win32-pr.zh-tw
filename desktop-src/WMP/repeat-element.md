---
title: REPEAT 元素
description: REPEAT 元素會定義 Windows Media Player 重複一或多個 ENTRY 或 ENTRYREF 元素的次數。
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- 重複元素 Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978460"
---
# <a name="repeat-element"></a>REPEAT 元素

**REPEAT** 元素會定義 Windows Media Player 重複一或多個 **ENTRY** 或 **ENTRYREF** 元素的次數。

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>屬性

**COUNT**

整數，代表 Windows Media Player 重複此專案範圍內的 **專案** 與 **ENTRYREF** 元素的次數。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                |
|-----------------|-------------------------|
| 父元素 | **.ASX**                 |
| 子元素  | **ENTRY**、 **ENTRYREF** |



 

## <a name="remarks"></a>備註

這個元素會定義 Windows Media Player 重複或迴圈的次數，以及此專案範圍內的 **ENTRY** 和 **ENTRYREF** 元素所定義的剪輯。 只有中繼檔中的第一個 **重複** 元素是有效的;後續的 **重複** 元素會被忽略。

如果未定義 **COUNT** 屬性，相關聯的專案和 ENTRYREF **專案** 中的內容就會重複一次無限的次數。 值為零會導致 Windows Media Player 忽略 **重複** 專案並播放一次內容。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 






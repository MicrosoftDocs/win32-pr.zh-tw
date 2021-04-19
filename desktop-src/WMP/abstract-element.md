---
title: ABSTRACT 元素
description: ABSTRACT 元素包含描述相關聯的 ASX、橫幅或 ENTRY 元素的文字。
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- ABSTRACT 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999440"
---
# <a name="abstract-element"></a>ABSTRACT 元素

**ABSTRACT** 元素包含描述相關聯的 **ASX**、**橫幅** 或 **ENTRY** 元素的文字。

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                       |
|-----------|--------------------------------|
| 父代    | **ASX**、 **ENTRY**、 **橫幅** |
| 子系     | 無                           |



 

## <a name="remarks"></a>備註

如果這個專案出現在 **ASX** 元素內，當滑鼠停留在顯示標題上時，文字會顯示為工具提示。

如果這個元素出現在 **ENTRY 專案** 中，當滑鼠停留在剪輯標題上時，文字會顯示為工具提示。

如果這個元素出現在 **橫幅** 專案中，則文字會顯示為橫幅圖形的工具提示。

每個範圍只使用一個 **抽象** 元素。 只有在處理中繼檔檔案時，才會使用另一個元素範圍內的第一個 **抽象** 元素。 該範圍中的任何後續 **抽象** 元素都會被忽略。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
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

 

 






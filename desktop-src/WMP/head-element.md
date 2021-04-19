---
title: head 元素
description: Head 元素包含適用于整個播放清單的中繼資料。
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- head 元素 Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976105"
---
# <a name="head-element"></a>head 元素

**Head** 元素包含適用于整個播放清單的中繼資料。

``` syntax
<head>
</head>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                                  |
|-----------|-----------------------------------------------------------|
| 父代    | [Smil](smil-element.md)                                  |
| 子系     | [標題](title-element--wpl.md)、 [中繼](meta-element.md) |



 

## <a name="remarks"></a>備註

**標頭** 專案通常包含 **標題** 專案，以及一個或多個定義播放清單全域特性的 **中繼** 元素。

## <a name="examples"></a>範例


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**中繼元素**](meta-element.md)
</dt> <dt>

[**.WPL) 的 title 元素 (**](title-element--wpl.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






---
title: STARTTIME 元素
description: STARTTIME 元素會定義時間索引，Windows Media Player 將從該索引開始轉譯資料流程。
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME 元素 Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981340"
---
# <a name="starttime-element"></a>STARTTIME 元素

**STARTTIME** 元素會定義時間索引，Windows Media Player 將從該索引開始轉譯資料流程。

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>屬性

**值** (必要) 

時間索引 (時、分、秒和百分之一秒的) ，Windows Media Player 開始播放相關元素中定義的資料流程。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ENTRY**、 **REF** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

這個元素會在內容中定義一個時間索引，Windows Media Player 開始呈現資料流程。 此元素只可用於已編制索引的預存、隨選內容。

## <a name="examples"></a>範例


```XML
<STARTTIME VALUE="1:30.0" />
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

 

 






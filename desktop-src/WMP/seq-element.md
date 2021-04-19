---
title: seq 元素
description: Seq 元素包含定義靜態播放清單的元素，或定義智慧播放清單的元素。
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- seq 元素 Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999143"
---
# <a name="seq-element"></a>seq 元素

**Seq** 元素包含定義靜態播放清單的元素，或定義智慧播放清單的元素。

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                                               |
|-----------|------------------------------------------------------------------------|
| 父代    | [body](body-element.md)                                               |
| 子系     | [media](media-element.md)、 [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>備註

當 **seq** 元素只包含參考特定媒體專案的 **媒體** 專案時，播放清單會被視為靜態。 當 **seq** 元素包含 **smartPlaylist** 元素時，它會被視為動態的「智慧型」播放清單。

## <a name="examples"></a>範例


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**body 元素**](body-element.md)
</dt> <dt>

[**媒體元件**](media-element.md)
</dt> <dt>

[**smartPlaylist 元素**](smartplaylist-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






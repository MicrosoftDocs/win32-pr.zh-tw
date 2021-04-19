---
title: body 元素
description: Body 元素包含定義播放清單內容的元素。
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- body 元素 Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995994"
---
# <a name="body-element"></a>body 元素

**Body** 元素包含定義播放清單內容的元素。

``` syntax
<body>
</body>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                 |
|-----------|--------------------------|
| 父代    | [Smil](smil-element.md) |
| 子系     | [序列](seq-element.md)   |



 

## <a name="remarks"></a>備註

播放清單的內容會組織在包含于 **body** 專案內的 **seq** 元素中。 一般來說，有一個 seq 元素定義了一組靜態的媒體專案，其中包含 **媒體** 專案，或是有一個定義一組動態媒體專案，並且包含 **smartPlaylist** 專案的 **seq** 專案。

## <a name="examples"></a>範例


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體元件**](media-element.md)
</dt> <dt>

[**seq 元素**](seq-element.md)
</dt> <dt>

[**smartPlaylist 元素**](smartplaylist-element.md)
</dt> <dt>

[**smil 元素**](smil-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






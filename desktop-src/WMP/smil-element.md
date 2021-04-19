---
title: smil 元素
description: Smil 元素一律是 Windows Media 播放清單中的最上層元素， (.WPL) 檔。 它會指定檔案使用 SMIL (同步處理的多媒體整合語言) 語法和文法。
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil 元素 Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996021"
---
# <a name="smil-element"></a>smil 元素

**Smil** 元素一律是 Windows Media 播放清單中的最上層元素， (.wpl) 檔。 它會指定檔案使用 SMIL (同步處理的多媒體整合語言) 語法和文法。

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                           |
|-----------|----------------------------------------------------|
| 父代    | 無                                               |
| 子系     | [head](head-element.md)、 [body](body-element.md) |



 

## <a name="remarks"></a>備註

每個 Windows Media 播放清單的根目錄都必須有 **smil** 元素。

## <a name="examples"></a>範例


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**body 元素**](body-element.md)
</dt> <dt>

[**head 元素**](head-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






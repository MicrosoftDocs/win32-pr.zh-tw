---
title: smartPlaylist 元素
description: SmartPlaylist 元素包含動態定義的播放清單部分。
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- smartPlaylist 元素 Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983169"
---
# <a name="smartplaylist-element"></a>smartPlaylist 元素

**SmartPlaylist** 元素包含動態定義的播放清單部分。

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>屬性



| 詞彙                                                                                                                                   | 描述                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>需要 (**版本**)  <br/> | 十進位數，代表智慧播放清單架構的版本號碼。 設定為1.0.0.0。<br/> |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                                       |
|-----------|----------------------------------------------------------------|
| 父代    | [序列](seq-element.md)                                         |
| 子系     | [querySet](queryset-element.md)， [篩選](filter-element.md) |



 

## <a name="remarks"></a>備註

**SmartPlaylist** 元素通常包含 **querySet** 專案，而且也可以包含 **篩選** 元素。

## <a name="examples"></a>範例


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**引數元素**](argument-element.md)
</dt> <dt>

[**filter 元素**](filter-element.md)
</dt> <dt>

[**片段元素**](fragment-element.md)
</dt> <dt>

[**querySet 元素**](queryset-element.md)
</dt> <dt>

[**seq 元素**](seq-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






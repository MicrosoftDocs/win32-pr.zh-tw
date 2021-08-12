---
title: querySet 元素
description: QuerySet 元素包含定義將從程式庫選取哪些媒體專案的元素。
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- querySet 元素 Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb157bb30c2e728b7840fe7021a2a4fcacc317b10eb6778b5702d7d2277c4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570611"
---
# <a name="queryset-element"></a>querySet 元素

**QuerySet** 元素包含定義將從程式庫選取哪些媒體專案的元素。

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                   |
|-----------|--------------------------------------------|
| 父代    | [smartPlaylist](smartplaylist-element.md) |
| 子系     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>備註

**QuerySet** 元素會指定應該從程式庫中選取哪些媒體專案，而不考慮結果集的大小。 另一方面， **filter** 元素會限制結果集的大小。

## <a name="examples"></a>範例


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
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

[**smartPlaylist 元素**](smartplaylist-element.md)
</dt> <dt>

[**sourceFilter 元素**](sourcefilter-element.md)
</dt> <dt>

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






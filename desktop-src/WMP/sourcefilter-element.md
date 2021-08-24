---
title: sourceFilter 元素
description: SourceFilter 元素包含可從程式庫中選取專案的元素。
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- sourceFilter 元素 Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14294f227e5ebe29e422d60a95734f7b93207880ea82ef9fb70ed3f7cf6dac4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763268"
---
# <a name="sourcefilter-element"></a>sourceFilter 元素

**SourceFilter** 元素包含可從程式庫中選取專案的元素。

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**類型**
</dt> <dd>

篩選物件的型別。 這個屬性沒有預先定義的值。

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>需要 (**識別碼**)  
</dt> <dd>

可唯一識別來源篩選物件的 GUID。 系統會叫用來源篩選物件的方法，以解讀 **sourceFilter** 元素中包含的 **片段** 元素。



| 值                                  | 描述                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | 「我的媒體櫃中的音樂」來源篩選的 GUID。    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | 「我的媒體櫃中的影片」來源篩選的 GUID。    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | 「我的媒體櫃中的圖片」來源篩選的 GUID。 |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | 「我的媒體櫃中的電視節目」來源篩選的 GUID。 |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>需要 (**名稱**)  
</dt> <dd>

篩選物件的名稱。



| 值                  | 描述                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| 媒體櫃中的音樂    | 篩選物件，可從使用者程式庫中的一組音樂專案選取指定的專案。 |
| 媒體櫃中的影片    | 篩選物件，它會從使用者程式庫中的一組影片專案選取指定的專案。 |
| 媒體櫃中的圖片 | 篩選物件，可從使用者程式庫中的一組相片專案選取指定的專案。 |
| 媒體櫃中的電視節目 | 篩選物件，可從使用者程式庫中的電視專案集合中選取指定的專案。    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                         |
|-----------|----------------------------------|
| 父代    | [querySet](queryset-element.md) |
| 子系     | [片段](fragment-element.md) |



 

## <a name="remarks"></a>備註

**SourceFilter** 元素會從程式庫中選取專案，而不考慮結果集的大小。 另一方面， **filter** 元素會限制結果集的大小。

## <a name="examples"></a>範例


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**filter 元素**](filter-element.md)
</dt> <dt>

[**片段元素**](fragment-element.md)
</dt> <dt>

[**querySet 元素**](queryset-element.md)
</dt> <dt>

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






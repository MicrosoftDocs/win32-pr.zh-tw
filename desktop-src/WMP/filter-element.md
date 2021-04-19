---
title: filter 元素
description: 篩選元素包含的元素會限制播放清單的大小、播放清單的持續時間，或播放清單中的媒體專案數。
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- 篩選元素 Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984011"
---
# <a name="filter-element"></a>filter 元素

**篩選** 元素包含的元素會限制播放清單的大小、播放清單的持續時間，或播放清單中的媒體專案數。

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**類型**
</dt> <dd>

篩選物件的型別。 這個屬性沒有預先定義的值。

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>需要 (**識別碼**)  
</dt> <dd>

可唯一識別篩選物件的 GUID。 系統會叫用篩選物件的方法，以解讀 **篩選** 元素中包含的 **片段** 專案。



| 值                                  | 描述                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | 「Microsoft 自動播放清單篩選--依計數、大小或持續時間限制自動播放清單」篩選器的識別碼。 |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>需要 (**名稱**)  
</dt> <dd>

篩選物件的名稱。



| 值                                                                              | 描述                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Microsoft 自動播放清單篩選--依計數、大小或持續時間限制自動播放清單 | 依計數、大小或持續時間限制自動播放清單。 |



 

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                                   |
|-----------|--------------------------------------------|
| 父代    | [smartPlaylist](smartplaylist-element.md) |
| 子系     | [片段](fragment-element.md)           |



 

## <a name="remarks"></a>備註

**篩選** 元素不會將任何媒體元件新增至播放清單;它只會移除或篩選 **sourceFilter** 元素所選取的內容。

## <a name="examples"></a>範例


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**引數元素**](argument-element.md)
</dt> <dt>

[**片段元素**](fragment-element.md)
</dt> <dt>

[**smartPlaylist 元素**](smartplaylist-element.md)
</dt> <dt>

[**sourceFilter 元素**](sourcefilter-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 






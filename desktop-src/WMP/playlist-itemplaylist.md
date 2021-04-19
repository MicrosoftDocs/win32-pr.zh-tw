---
title: 播放清單。 itemPlaylist
description: ItemPlaylist 屬性會抓取播放清單元素中指定索引處所顯示媒體專案的播放清單。
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- 播放清單. itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999501"
---
# <a name="playlistitemplaylist"></a>播放清單。 itemPlaylist

**ItemPlaylist** 屬性會抓取 **播放清單** 元素中指定索引處所顯示媒體專案的播放清單。

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **播放清單** 物件。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

包含播放清單專案索引的 (**長**) **數目**。

</dd> </dl>

## <a name="remarks"></a>備註

**ItemPlaylist** 屬性會傳回播放 **清單** 元素中展開的播放清單物件。 例如，如果有兩個未在 **播放清單** 元素中展開的嵌套播放清單，且其中包含三個媒體剪輯， **itemPlaylist** (1) 將會傳回包含兩個嵌套播放清單的父播放清單。 如果展開第二個播放清單， **itemPlaylist** (1) 將會傳回第二個播放清單。 如果這兩個播放清單都已展開， **itemPlaylist** (1) 將會傳回第一個播放清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> </dl>

 

 






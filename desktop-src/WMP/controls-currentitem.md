---
title: CurrentItem
description: CurrentItem 屬性會指定或抓取目前的媒體專案。
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- CurrentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997548"
---
# <a name="controlscurrentitem"></a>CurrentItem

**CurrentItem** 屬性會指定或抓取目前的媒體專案。

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **媒體** 物件。

## <a name="remarks"></a>備註

此方法僅適用于 *Player* 中的專案。**currentPlaylist**。 不支援使用已儲存媒體專案的參考來呼叫 **currentItem** 。

## <a name="examples"></a>範例

下列 JScript 範例會使用 **currentItem** ，將播放程式控制項目前的媒體專案設定為 HTML SELECT 專案中所選取的值。 目前的播放清單是使用 *PlaylistCollection* 來指定。**getByName**。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 






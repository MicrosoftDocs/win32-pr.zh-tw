---
title: CurrentPlaylistChange 事件
description: 當目前播放清單中的某個專案發生變更時，就會發生 CurrentPlaylistChange 事件。 |CurrentPlaylistChange 事件
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- CurrentPlaylistChange 事件 Windows Media Player
- CurrentPlaylistChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentPlaylistChange 事件
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977168"
---
# <a name="playercurrentplaylistchange-event"></a>CurrentPlaylistChange 事件

當目前播放清單中的某個專案發生變更時，就會發生 **CurrentPlaylistChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*change* 
</dt> <dd>

**Number** (**long**) 指出播放清單所發生的變更類型。 查看 *播放機*。可能值資料表的 **PlaylistChange** 事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當不同的播放清單變成目前的播放清單時，就不會發生此事件。 只有在目前的播放清單中發生變更時才會發生，例如將媒體專案附加至播放清單。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="examples"></a>範例

下列 JScript 範例會更新名為 PlItems 之 HTML DIV 元素中的文字，以顯示目前播放清單中的媒體專案名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**CurrentPlaylist**](player-currentplaylist.md)
</dt> <dt>

[**PlaylistChange**](player-player-playlistchange.md)
</dt> </dl>

 

 






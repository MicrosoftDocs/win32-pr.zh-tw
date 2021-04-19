---
title: CurrentPlaylist
description: CurrentPlaylist 屬性會指定或抓取目前的播放清單物件。
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- CurrentPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980154"
---
# <a name="playercurrentplaylist"></a>CurrentPlaylist

CurrentPlaylist 屬性會指定或抓取目前的 **播放清單** 物件。

## <a name="syntax"></a>Syntax

*玩家* 。**currentPlaylist**

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **播放清單** 物件。

## <a name="remarks"></a>備註

如果 *設定*，則為。**autoStart** 屬性為 true，每當您設定 **currentPlaylist** 時，就會自動開始播放。

這個屬性會採用播放清單物件，可以透過數種方式取得，例如藉由呼叫 *PlaylistArray*。**專案** 或 *PlaylistCollection*。**[]**。 若要使用檔案名載入 **播放清單** 專案，請設定 URL 屬性或使用 *播放* 清單。**[]**。

## <a name="examples"></a>範例

下列 JScript 範例會抓取媒體櫃中的第一個播放清單。 然後，它會使用 **currentPlaylist** 讓抓取的播放清單成為目前的播放清單，然後顯示目前播放清單的名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
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

[**[]**](player-newplaylist.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**PlaylistArray 專案**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection. []**](playlistcollection-newplaylist.md)
</dt> <dt>

[**設定。 autoStart**](settings-autostart.md)
</dt> </dl>

 

 






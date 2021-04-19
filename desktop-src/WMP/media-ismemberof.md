---
title: IsMemberOf 方法
description: IsMemberOf 方法會傳回值，指出媒體專案是否為指定播放清單的成員。
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- isMemberOf 方法 Windows Media Player
- isMemberOf 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isMemberOf 方法
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990037"
---
# <a name="mediaismemberof-method"></a>IsMemberOf 方法

**IsMemberOf** 方法會傳回值，指出媒體專案是否為指定播放清單的成員。

## <a name="syntax"></a>語法


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*播放清單* \[在\]
</dt> <dd>

可能包含媒體專案的 **播放清單** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="remarks"></a>備註

這個方法無法檢查透過 **MediaCollection** 物件取出的播放清單。 若要測試媒體專案是否為特定命名播放清單的成員，請使用 *播放* 程式取出播放清單。*playlistCollection*。**getByName** (*名稱*) 。**專案** (0) 。 此方法也可以搭配 CD 播放清單和中繼檔播放清單使用。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**isMemberOf** ，測試目前的媒體專案是否為名為範例播放清單的播放清單成員。 如果不是，則會將目前的媒體專案附加至範例播放清單。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






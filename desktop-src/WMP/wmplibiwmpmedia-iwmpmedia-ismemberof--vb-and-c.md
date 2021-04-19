---
title: IWMPMedia isMemberOf 方法
description: IsMemberOf 方法會傳回值，指出指定的媒體專案是否為指定播放清單的成員。
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- isMemberOf 方法 Windows Media Player
- isMemberOf 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，isMemberOf 方法
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000967"
---
# <a name="iwmpmediaismemberof-method"></a>IWMPMedia：： isMemberOf 方法

**IsMemberOf** 方法會傳回值，指出指定的媒體專案是否為指定播放清單的成員。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a>參數

<dl> <dt>

*pPlaylist* \[在\]
</dt> <dd>

**WMPLib IWMPPlaylist** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

System.string **值，** 指出媒體專案是否為播放清單的成員。

## <a name="remarks"></a>備註

這個方法無法檢查透過 **IWMPMediaCollection** 介面取出的播放清單。 若要測試媒體專案是否為特定命名播放清單的成員，請使用 **AxWindowsMediaPlayer. playlistCollection** 屬性取出播放清單集合。 一旦您取得集合，請呼叫 **IWMPPlaylistCollection. getByName** 方法來取出個別播放清單。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **isMemberOf** 來測試目前的媒體專案是否為名為所有音樂的播放清單的成員。 如果不是，則會將目前的媒體專案附加至播放清單。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. playlistCollection (VB 和 c # )**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 






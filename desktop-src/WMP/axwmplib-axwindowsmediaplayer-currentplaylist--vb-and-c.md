---
title: AxWindowsMediaPlayer. currentPlaylist 屬性
description: CurrentPlaylist 屬性會取得或設定目前的 IWMPPlaylist 介面，以提供簡單的方式來組織和動作清單中的媒體專案。
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- currentPlaylist 屬性 Windows Media Player
- currentPlaylist 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，currentPlaylist 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999297"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a>AxWindowsMediaPlayer. currentPlaylist 屬性

CurrentPlaylist 屬性會取得或設定目前的 **IWMPPlaylist** 介面，以提供簡單的方式來組織和動作清單中的媒體專案。

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>屬性值

提供目前播放清單存取權的 WMPLib. IWMPPlaylist 介面。

## <a name="remarks"></a>備註

如果 IWMPSettings 的屬性 (也可透過 AxWindowsMediaPlayer 存取。**autoStart**) 為 true，每當您設定 **currentPlaylist** 時，就會自動開始播放。

這個屬性會採用 IWMPPlaylist 介面，這可以透過數種方式取得，例如從 *IWMPPlaylistArray* 取得值。**專案** 或 *IWMPPlaylistCollection*。**[]** 屬性。 若要使用檔案名載入 **播放清單** 專案，請設定 URL 屬性，或使用 AxWindowsMediaPlayer。**[]**。

## <a name="examples"></a>範例

下列範例會抓取媒體櫃中的第一個播放清單，並使用 currentPlaylist 屬性將取出的播放清單設定為目前的播放清單，並顯示其名稱。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. [] (VB 和 c # )**](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[**AxWindowsMediaPlayer VB 和 c # 的 (設定 )**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray (VB 和 c # )**](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






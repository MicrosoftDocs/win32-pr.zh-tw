---
title: IWMPControls playItem 方法
description: PlayItem 方法會播放指定的媒體專案。 |IWMPControls playItem 方法
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- playItem 方法 Windows Media Player
- playItem 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，playItem 方法
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996466"
---
# <a name="iwmpcontrolsplayitem-method"></a>IWMPControls：:p layItem 方法

**PlayItem** 方法會播放指定的媒體專案。

## <a name="syntax"></a>語法


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a>參數

<dl> <dt>

*pIWMPMedia* \[在\]
</dt> <dd>

媒體專案的 **WMPLib IWMPMedia** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

不論 **IWMPSettings** 的值為何，媒體專案都會自動載入並播放。 若要載入專案而不自動播放，請將 **IWMPSettings** 設定為 **false** ，並將值指派給 **AxWindowsMediaPlayer**，之後可以呼叫 **IWMPControls** 來開始播放專案。

注意

**playItem** 僅適用于 **AxWindowsMediaPlayer. currentPlaylist** 中的專案。 不支援使用已儲存媒體專案的參考來呼叫 **playItem** 。

## <a name="examples"></a>範例

下列範例會使用 **playItem** 來播放目前播放清單中的媒體專案。 您可以根據播放清單中的位置，選擇要播放的專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist (VB 和 c # )**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






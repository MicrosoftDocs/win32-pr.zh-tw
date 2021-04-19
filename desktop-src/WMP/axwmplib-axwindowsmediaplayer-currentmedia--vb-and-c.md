---
title: AxWindowsMediaPlayer. currentMedia 屬性
description: CurrentMedia 屬性會取得或設定對應至目前媒體專案的 IWMPMedia 介面。
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- currentMedia 屬性 Windows Media Player
- currentMedia 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，currentMedia 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983158"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a>AxWindowsMediaPlayer. currentMedia 屬性

CurrentMedia 屬性會取得或設定對應至目前媒體專案的 IWMPMedia 介面。

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a>屬性值

WMPLib. IWMPMedia 介面，可提供目前媒體專案的存取權。

## <a name="remarks"></a>備註

如果設定為 AxWindowsMediaPlayer，則為。**autoStart** 屬性為 true，每當您設定 **currentMedia** 時，就會自動開始播放。

您可以 \_ 在 c # ) 中，透過 IWMPPlaylist (IWMPPlaylist. get item 方法取得指定媒體專案的 IWMPMedia 介面。 若要使用檔案名載入媒體專案，請設定 URL 屬性，或使用 newMedia。

## <a name="examples"></a>範例

下列範例會抓取媒體櫃中的第一個媒體專案，並使用 currentMedia 屬性將取出的媒體專案設定為目前的媒體專案，並顯示其名稱。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
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

[**AxWindowsMediaPlayer. newMedia (VB 和 c # )**](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist (VB 和 c # )**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 






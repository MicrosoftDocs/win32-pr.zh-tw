---
title: IWMPCdrom 播放清單屬性
description: 播放清單屬性會取得 IWMPPlaylist 介面，此介面代表 cd 光碟機或 DVD 的根層級標題專案中的曲目。
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- 播放清單屬性 Windows Media Player
- 播放清單屬性 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player、播放清單屬性
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985575"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPCdrom：:P laylist 屬性

**播放清單** 屬性會取得 **IWMPPlaylist** 介面，此介面代表 cd 光碟機或 DVD 的根層級標題專案中的曲目。

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>屬性值

**WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

通常，以 DVD 為基礎的內容會組織成標題。 每個標題都包含一或多個章節。 每個 DVD 的撰寫方式都不同，因此使用標題和章節的方式是由內容作者決定。

若是 DVD，這個屬性會取得播放清單，其中包含做為 **IWMPMedia** 介面（名為 "DVD"）的第一個專案。 此介面代表 DVD 媒體。 如果播放專案是在插入新 DVD 之後第一次播放，播放該專案會導致 DVD 播放，或在 DVD 與最後一張 DVD 相同時繼續播放。 在播放期間將這個專案設定為目前的專案，會從一開始就播放 DVD。

播放清單中) **IWMPMedia** 介面所代表的其他 (專案，是以嵌套播放清單表示的 DVD 標題。 當您將 **IWMPControls** 設定為等於這些嵌套播放清單專案的其中一個時，Windows Media Player 會在首次播放開始之後，自動將嵌套播放清單設定為目前的播放清單。 然後，您可以使用 **IWMPPlaylist** 介面屬性、方法和相關事件來處理 DVD 章節，也就是播放清單專案。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **播放** 清單來填滿名為 myText 的多行文字方塊，以及目前位於第一個 CD 光碟機的音訊 CD 的曲目清單。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdrom 介面 (VB 和 c # )**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






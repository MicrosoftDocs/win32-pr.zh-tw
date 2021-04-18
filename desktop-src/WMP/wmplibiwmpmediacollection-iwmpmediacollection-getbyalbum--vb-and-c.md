---
title: IWMPMediaCollection getByAlbum 方法
description: GetByAlbum 方法會傳回 IWMPPlaylist 介面，此介面可讓您從指定的專輯存取媒體專案。
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- getByAlbum 方法 Windows Media Player
- getByAlbum 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAlbum 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996321"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>IWMPMediaCollection：： getByAlbum 方法

**GetByAlbum** 方法會傳回 **IWMPPlaylist** 介面，此介面可讓您從指定的專輯存取媒體專案。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAlbum* \[在\]
</dt> <dd>

表示專輯標題的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

您有兩種方式可以取出 **IWMPMediaCollection** 介面，而 **getByAlbum** 方法的行為取決於您所使用的兩種方式。 如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則 **getByAlbum** 方法會傳回媒體櫃中的所有媒體專案。 但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則 **getByAlbum** 方法只會傳回程式庫中屬於指定之專輯的音訊專案。

## <a name="examples"></a>範例

下列範例會使用 **getByAlbum** ，在使用者按一下按鈕時，建立媒體專案的播放清單。 播放清單中包含使用者在文字方塊中指定之專輯的專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 






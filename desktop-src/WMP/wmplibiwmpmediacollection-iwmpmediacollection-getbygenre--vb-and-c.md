---
title: IWMPMediaCollection getByGenre 方法
description: GetByGenre 方法會傳回 IWMPPlaylist 介面，以提供指定之內容類型的媒體專案存取權。
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- getByGenre 方法 Windows Media Player
- getByGenre 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByGenre 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976246"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>IWMPMediaCollection：： getByGenre 方法

`getByGenre`方法會傳回 **IWMPPlaylist** 介面，以提供指定之內容類型的媒體專案存取權。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrGenre* \[在\]
</dt> <dd>

**System.string** ，此為類型的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

您有兩種方式可以取出 **IWMPMediaCollection** 介面，而方法的行為 `getByGenre` 取決於您所使用的兩種方法。 如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則方法會傳回 `getByGenre` 媒體櫃中的所有媒體專案。 但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則方法只會傳回連結 `getByGenre` 庫中具有指定之屬性和值的音訊專案。

## <a name="examples"></a>範例

下列範例會在 `getByGenre` 使用者按一下按鈕時，使用來取得媒體專案的播放清單。 播放清單中包含使用者在文字方塊中指定之類型的專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

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

 

 






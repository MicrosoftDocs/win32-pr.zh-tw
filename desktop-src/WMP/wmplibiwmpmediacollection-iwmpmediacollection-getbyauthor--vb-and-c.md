---
title: IWMPMediaCollection getByAuthor 方法
description: GetByAuthor 方法會傳回 IWMPPlaylist 介面，以提供指定作者存取媒體專案的許可權。
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- getByAuthor 方法 Windows Media Player
- getByAuthor 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getByAuthor 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829232e6cd9fb64fec1d209991c3734ad435b4b69d0d7b66b135ab9cca1fe4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053606"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a>IWMPMediaCollection：： getByAuthor 方法

`getByAuthor`方法會傳回 **IWMPPlaylist** 介面，以提供指定作者存取媒體專案的許可權。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAuthor* \[在\]
</dt> <dd>

**System.string** ，也就是作者的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

抓取之媒體專案的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

您有兩種方式可以取出 **IWMPMediaCollection** 介面，而方法的行為 `getByAuthor` 取決於您所使用的兩種方法。 如果您藉由呼叫 [AxWindowsMediaPlayer](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)來取出介面，則方法會傳回 `getByAuthor` 媒體櫃中的所有媒體專案。 但是，如果您藉由呼叫 [IWMPLibrary](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)來取出介面，則方法只會傳回連結 `getByAuthor` 庫中具有指定之屬性和值的音訊專案。

## <a name="examples"></a>範例

下列範例會在 `getByAuthor` 使用者按一下按鈕時，使用來建立媒體專案的播放清單。 播放清單包含符合使用者在文字方塊中指定之作者名稱的專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

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

 

 






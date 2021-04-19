---
title: AxWindowsMediaPlayer 物件的 CurrentPlaylistChange 事件
description: 當目前播放清單中的某個專案發生變更時，就會發生 CurrentPlaylistChange 事件。 |AxWindowsMediaPlayer 物件的 CurrentPlaylistChange 事件
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- AxWindowsMediaPlayer 物件的 CurrentPlaylistChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981262"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CurrentPlaylistChange 事件

當目前播放清單中的某個專案發生變更時，就會發生 CurrentPlaylistChange 事件。

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CurrentPlaylistChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CurrentPlaylistChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| 變更   | WMPLib. WMPPlaylistChangeEventTypeAn 列舉值，指出播放清單所發生的變更類型。<br/> |



 

## <a name="remarks"></a>備註

當不同的播放清單變成目前的播放清單時，就不會發生此事件。 只有在目前的播放清單中發生變更時才會發生，例如將媒體專案附加至播放清單。

## <a name="examples"></a>範例

下列範例會顯示目前播放清單中所有媒體專案的名稱，以回應 CurrentPlaylistChange 事件。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
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

[**AxWindowsMediaPlayer. currentPlaylist (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer PlaylistChange 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[**WMPPlaylistChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 






---
title: AxWindowsMediaPlayer-全螢幕屬性
description: 全螢幕屬性會取得或設定值，指出是否以全螢幕模式播放影片內容。
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- 全螢幕屬性 Windows Media Player
- 全螢幕屬性 Windows Media Player、AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，全螢幕屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992378"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a>AxWindowsMediaPlayer-全螢幕屬性

全螢幕屬性會取得或設定值，指出是否以全螢幕模式播放影片內容。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a>屬性值

指出內容是否以全螢幕模式播放的布林值。 預設值為 false。

## <a name="remarks"></a>備註

若要在內嵌 Windows Media Player 控制項時讓全螢幕模式正常運作，影片顯示區域必須具有至少一個圖元的高度和寬度。 如果 **uiMode** 設定為「迷你」或「完整」，則控制項本身的高度必須是65或更大，才能容納除了使用者介面之外的影片顯示區域。

如果 **uiMode** 設為「隱藏」，則將這個屬性設定為 true 會引發錯誤，而且不會影響控制項的行為。

在全螢幕播放期間，Windows Media Player 會在 [enableCoNtextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

如果 **uiMode** 設為「完整」或「迷你」，Windows Media Player 在滑鼠游標移動時，以全螢幕模式顯示傳輸控制項。 在不移動滑鼠的短暫間隔之後，就會隱藏傳輸控制項。 如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。

> [!Note]  
> 以全螢幕模式顯示傳輸控制項需要 Windows XP 作業系統。

 

如果傳輸控制項未以全螢幕模式顯示，則 Windows Media Player 會在播放停止時自動離開全螢幕模式。

## <a name="examples"></a>範例

下列範例會建立一個按鈕，使用 [全螢幕] 屬性將內嵌的播放機物件切換至全螢幕模式。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                  |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                            |
| 組件<br/>  | <dl> <dt>AxInterop. WMPLib (AxInterop.WMPLib.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. uiMode (VB 和 c # )**](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 






---
title: IWMPNetwork encodedFrameRate 屬性
description: EncodedFrameRate 屬性會取得內容作者所指定的影片畫面播放速率。
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- encodedFrameRate 屬性 Windows Media Player
- encodedFrameRate 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，encodedFrameRate 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977396"
---
# <a name="iwmpnetworkencodedframerate-property"></a>IWMPNetwork：： encodedFrameRate 屬性

**EncodedFrameRate** 屬性會取得內容作者所指定的影片畫面播放速率。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a>屬性值

以每秒畫面格的編碼畫面播放速率 (fps) 的 **Int32。**

> [!Note]  
> 雖然 **encodedFrameRate** 屬性會測量每秒畫面格的編碼畫面播放速率，但 [ **幀** 速率] 屬性會測量目前的畫面播放速率（以每一百秒為單位）。

 

## <a name="examples"></a>範例

下列程式碼範例會使用 **encodedFrameRate** 來顯示編碼檔案時所指定的畫面播放速率。 這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

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

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**(VB 和 c # 的 IWMPNetwork 幀 )**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 






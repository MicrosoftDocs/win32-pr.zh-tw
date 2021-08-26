---
title: IWMPNetwork 畫面播放速率屬性
description: '[畫面播放速率] 屬性會取得目前的影片畫面播放速率。'
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- 速率屬性 Windows Media Player
- IWMPNetwork 介面的畫面播放速率屬性 Windows Media Player
- IWMPNetwork 介面 Windows Media Player、畫面播放速率屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3169cc21eee2317da45db3cb3ca9ceffffa01c85479312defe63cda1fa09796f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956158"
---
# <a name="iwmpnetworkframerate-property"></a>IWMPNetwork：：幀屬性

[ **幀** 速率] 屬性會取得目前的影片畫面播放速率。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a>屬性值

在每一百秒框架中的目前畫面播放速率的 **system.object** 。

> [!Note]  
> 雖然 **encodedFrameRate** 屬性會測量每秒畫面格的編碼畫面播放速率，但 [ **幀** 速率] 屬性會測量目前的畫面播放速率（以每一百秒為單位）。 請參閱＜備註＞。

 

## <a name="remarks"></a>備註

目前的畫面播放速率值會以每一百秒的框架傳回。 例如，值2998表示每秒29.98 個畫面 (fps) 。

## <a name="examples"></a>範例

下列程式碼範例會使用 **幀** 速率來顯示編碼檔案時所指定的畫面播放速率。 這項資訊會顯示在標籤中，以回應 **PlayStateChange** 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

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

[**IWMPNetwork. encodedFrameRate (VB 和 c # )**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 






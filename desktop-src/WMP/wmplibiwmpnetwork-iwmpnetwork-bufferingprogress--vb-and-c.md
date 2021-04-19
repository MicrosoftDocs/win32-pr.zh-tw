---
title: IWMPNetwork bufferingProgress 屬性
description: BufferingProgress 屬性會取得緩衝處理已完成的百分比。
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- bufferingProgress 屬性 Windows Media Player
- bufferingProgress 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，bufferingProgress 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998851"
---
# <a name="iwmpnetworkbufferingprogress-property"></a>IWMPNetwork：： bufferingProgress 屬性

**BufferingProgress** 屬性會取得緩衝處理已完成的百分比。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a>屬性值

表示以百分比表示之緩衝進度的 **system.object。**

## <a name="remarks"></a>備註

每次播放都會停止並重新啟動，這個屬性會重設為零。 如果播放暫停，則不會重設。

緩衝處理只適用于串流內容。 這個屬性只會在執行時間期間取得有效的資訊。當播放的 URL 是使用 **AxWindowsMediaPlayer** 屬性設定時。

使用 **AxWindowsMediaPlayer。 \_WMPOCXEvents \_ BufferingEvent** ，以判斷何時啟動或停止緩衝。

## <a name="examples"></a>範例

下列範例會使用 **bufferingProgress** 來顯示在標籤中完成的緩衝百分比，以回應緩衝事件。 此範例使用具有1秒間隔的計時器來更新顯示。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

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

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # ) 的緩衝事件**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






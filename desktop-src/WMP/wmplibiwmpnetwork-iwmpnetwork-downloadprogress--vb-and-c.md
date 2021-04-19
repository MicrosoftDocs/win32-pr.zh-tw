---
title: IWMPNetwork downloadProgress 屬性
description: DownloadProgress 屬性會取得下載已完成的百分比。
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- downloadProgress 屬性 Windows Media Player
- downloadProgress 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，downloadProgress 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997665"
---
# <a name="iwmpnetworkdownloadprogress-property"></a>IWMPNetwork：:d ownloadProgress 屬性

**DownloadProgress** 屬性會取得下載已完成的百分比。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a>屬性值

以百分比表示的下載進度的 **system.object** 。

## <a name="remarks"></a>備註

當 Windows Media Player 控制項連接到可同時播放和下載的數位媒體檔案時， **downloadProgress** 屬性會取得已下載的檔案總數百分比。 這項功能目前僅支援從 web 伺服器下載的數位媒體檔案。 您可以同時下載並播放下列任何格式的檔案：

-   進階系統格式 (ASF)
-   Windows Media 音訊 (WMA)
-   Windows Media 視訊 (WMV)
-   MP3
-   MPEG
-   WAV

此外，也可以同時下載並播放某些 AVI 檔案。

使用 **AxWindowsMediaPlayer。 \_WMPOCXEvents \_ BufferingEvent** ，以判斷何時啟動或停止緩衝。

## <a name="examples"></a>範例

下列程式碼範例會使用 **downloadProgress** 來顯示已完成下載的百分比。 這項資訊會顯示在標籤中，以回應 **緩衝** 事件。 此範例使用具有1秒間隔的計時器來更新顯示。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

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

[**AxWindowsMediaPlayer (VB 和 c # ) 的緩衝事件**](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 






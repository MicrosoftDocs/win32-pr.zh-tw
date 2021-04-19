---
title: IWMPMedia duration 屬性
description: Duration 屬性會取得目前媒體專案的持續時間（以秒為單位）。
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- duration 屬性 Windows Media Player
- duration 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，duration 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996269"
---
# <a name="iwmpmediaduration-property"></a>IWMPMedia：:d uration 屬性

**Duration** 屬性會取得目前媒體專案的持續時間（以秒為單位）。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>屬性值

以秒為間隔的 **Double** 。

## <a name="remarks"></a>備註

如果這個屬性與 AxWindowsMediaPlayer. currentMedia 中所指定的媒體專案不同，它可能不包含有效的值。

若要取得不在使用者程式庫中的檔案持續時間，您必須等候 Windows Media Player 開啟檔案;亦即，目前的 **OpenState** 必須等於 **MediaOpen**。 您可以藉由處理 AxWindowsMediaPlayer 來確認這一點 **。 \_WMPOCXEvents \_ OpenStateChange** 事件，或定期檢查 **AxWindowsMediaPlayer. openState** 的值。

若為播放清單，當個別媒體專案開啟時，可以抓取每個媒體專案的持續時間，而不是開啟播放清單時的。

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **持續時間** ，在標籤中顯示目前媒體專案的剩餘時間。 計時器會每秒更新標籤中的文字。


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. openState (VB 和 c # )**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer OpenStateChange 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. durationString (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 






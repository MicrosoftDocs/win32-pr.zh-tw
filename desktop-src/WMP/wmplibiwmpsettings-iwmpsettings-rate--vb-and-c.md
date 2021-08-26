---
title: IWMPSettings rate 屬性
description: Rate 屬性可取得或設定影片目前的播放速率。
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- rate 屬性 Windows Media Player
- rate 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，速率屬性
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999698"
---
# <a name="iwmpsettingsrate-property"></a>IWMPSettings：： rate 屬性

**Rate** 屬性可取得或設定影片目前的播放速率。

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>屬性值

這是播放速率的 **雙精度浮點數** ，預設值為1.0。

## <a name="remarks"></a>備註

這個屬性所抓取的值會作為乘數值，讓您以更快或較慢的速率播放媒體專案。 預設值1.0 表示撰寫的速度。

請注意，在低於0.5 或高於1.5 的速率中，音訊播放軌會變得很難理解。 播放速率2表示正常播放速度的兩倍。

Windows Media Player 將嘗試使用下列四種不同播放模式的最有效方式

-   維持音訊音調的流暢播放影片
-   不維持音訊音調的流暢播放影片
-   無音訊的流暢播放影片
-   沒有音訊的主要畫面格影片播放

Windows Media Player 選擇的模式取決於許多因素，包括檔案類型和位置、作業系統、網路和伺服器。

其他考慮也適用，視用來建立內容的數位媒體格式而定：

-   **Windows媒體影片 (WMV) 和 ASF。** **速率** 屬性的最佳值是從1到10，或從1到10以進行反向播放。 從0.5 到1.0 或從-0.5 到-1.0 的值可能也適用于可以維持音訊音調的情況，例如播放位於本機電腦上的檔案時。 允許絕對值大於10的值，但沒有什麼意義。
-   **其他影片格式。** **Rate** 屬性的範圍可以從0到9。 不允許負數值。 小於1的值表示緩慢的移動。 允許超過9個值，但沒有什麼意義。

**IWMPControls. fastForward** 方法會將 **速率** 的值變更為5.0，而 **IWMPControls. fastReverse** 方法會將 **速率** 的值變更為5.0。

某些數位媒體格式的播放速率無法改變。 使用 c # 中的 **IWMPSettings. isAvailable** 屬性 (**IWMPSettings. get \_ isAvailable** 方法) 來找出是否可以針對特定媒體專案指定這個屬性。

## <a name="examples"></a>範例

下列範例使用數值上下按鈕控制項，可讓使用者變更目前媒體的播放速度。 當使用者按一下控制項的向上或向下箭號時，[ **速率** ] 屬性會設定為新的值。 控制項中的可能值範圍為 0.5 (半高速) 至 2.0 (雙速度) 。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

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

[**IWMPControls. fastForward (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastReverse (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. isAvailable (VB 和 c # )**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # ) 的靜音**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 






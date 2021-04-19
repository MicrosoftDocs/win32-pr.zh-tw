---
title: IWMPControls fastReverse 方法
description: FastReverse 方法會以反向方向啟動媒體專案的快速播放。
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- fastReverse 方法 Windows Media Player
- fastReverse 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，fastReverse 方法
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998676"
---
# <a name="iwmpcontrolsfastreverse-method"></a>IWMPControls：： fastReverse 方法

**FastReverse** 方法會以反向方向啟動媒體專案的快速播放。

## <a name="syntax"></a>語法


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**FastReverse** 方法會以正常速度的五倍反向掃描剪輯，如果是影片檔案，則只會顯示主要畫面格。 呼叫 **fastReverse** 相當於藉由設定 **IWMPSettings 的速率** 屬性，為速率指定-5.0。 如果後續的速率有所變更，或呼叫 **IWMPControls** 或 **IWMPControls** ，Windows Media Player 將會停止快速反轉。

如果專案是播放清單的一部分， **fastReverse** 就會在目前的播放軌開始時停止。比方說，如果 track 3 是在 **fastReverse** 中，當到達 track 3 的開頭時，Windows Media Player 將不會移至「追蹤2」。 呼叫 **fastReverse** 時，播放次數不會遞增。

如果您在 **fastReverse** 執行時呼叫 **IWMPControls fastForward** ， **fastReverse** 將會停止，而且 **IWMPControls** 將會開始。

這個方法不適用於即時廣播和某些數位媒體類型。 若要判斷您是否可以在剪輯中使用快速反轉，請將 **system.string** 值 "FastReverse" 傳遞給 **IWMPControls. isAvailable** 屬性， (**IWMPControls. Get \_ isAvailable** 方法（c # ) ）。

## <a name="examples"></a>範例

下列範例會使用 **fastReverse** 來反轉目前的媒體專案，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

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

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastForward (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. isAvailable (VB 和 c # )**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls。停止 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # 的速率 )**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 






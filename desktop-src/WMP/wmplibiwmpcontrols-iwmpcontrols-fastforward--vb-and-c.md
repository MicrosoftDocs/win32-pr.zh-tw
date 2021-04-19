---
title: IWMPControls fastForward 方法
description: FastForward 方法會以正向方向啟動媒體專案的快速播放。 |IWMPControls fastForward 方法
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- fastForward 方法 Windows Media Player
- fastForward 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，fastForward 方法
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978484"
---
# <a name="iwmpcontrolsfastforward-method"></a>IWMPControls：： fastForward 方法

**FastForward** 方法會以正向方向啟動媒體專案的快速播放。

## <a name="syntax"></a>語法


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**FastForward** 方法會以正常速度的五倍來播放剪輯。 呼叫 **fastForward** 相當於藉由設定 **IWMPSettings 的速率** 屬性來指定5.0 的速率。 如果後續的速率有所變更，或呼叫 **IWMPControls** 或 **IWMPControls** ，Windows Media Player 將會停止快速轉送。

**FastForward** 方法不適用於即時廣播和特定媒體類型。 若要判斷您是否可以在剪輯中向前快轉，請將 **system.string** 值 "FastForward" 傳遞給 **IWMPControls. isAvailable** 屬性， (**IWMPControls. Get \_ isAvailable** 方法 in c # ) 。

## <a name="examples"></a>範例

下列範例會使用 **fastForward** 來向前快轉目前的媒體專案，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

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

[**IWMPControls. isAvailable (VB 和 c # )**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls。停止 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # 的速率 )**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 






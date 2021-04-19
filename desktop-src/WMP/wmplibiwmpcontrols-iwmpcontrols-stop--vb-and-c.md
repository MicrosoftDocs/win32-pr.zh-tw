---
title: IWMPControls stop 方法
description: Stop 方法會停止播放媒體專案。 |IWMPControls stop 方法
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- stop 方法 Windows Media Player
- stop 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，stop 方法
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999388"
---
# <a name="iwmpcontrolsstop-method"></a>IWMPControls：： stop 方法

**Stop** 方法會停止播放媒體專案。

## <a name="syntax"></a>語法


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使 Windows Media Player 釋出它所使用的任何系統資源，例如音訊裝置。 但目前的媒體專案則不會釋出。

當 Windows Media Player 停止時，媒體專案中目前的播放位置會重設為專案的開頭。 接著呼叫 **IWMPControls** ，就會開始從媒體專案的開頭播放。 若要停止播放作業而不變更目前的位置，請使用 **IWMPControls** 方法。

## <a name="examples"></a>範例

下列範例會使用 [ **停止** ] 來停止目前的媒體專案，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

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

[**IWMPControls：接下來 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls： pause (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls 之前 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 






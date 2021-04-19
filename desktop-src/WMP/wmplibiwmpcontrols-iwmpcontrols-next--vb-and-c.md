---
title: IWMPControls next 方法
description: 下一個方法會將播放清單中的下一個專案設定為目前的專案。
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- next 方法 Windows Media Player
- next 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player、next 方法
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984842"
---
# <a name="iwmpcontrolsnext-method"></a>IWMPControls：： next 方法

**下一個** 方法會將播放清單中的下一個專案設定為目前的專案。

## <a name="syntax"></a>語法


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果叫用 [ **下一步]** 時，播放清單是最後一個專案，播放清單中的第一個專案就會成為目前的專案。

針對伺服器端播放清單，這個方法會跳至伺服器端播放清單中的下一個專案，而不是用戶端播放清單。

播放 DVD 時，此方法會跳到播放順序中的下一個邏輯章節，這可能不是播放清單中的下一章。 播放 DVD 的靜止影像時，此方法會跳到下一個影像。

## <a name="examples"></a>範例

下列範例會使用 **[下一步]** 移至目前播放清單中的下一個專案，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**IWMPControls 之前 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**IWMPControls。停止 (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 






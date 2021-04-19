---
title: IWMPControls pause 方法
description: Pause 方法會暫停播放媒體專案。 |IWMPControls pause 方法
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- pause 方法 Windows Media Player
- pause 方法 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，pause 方法
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998640"
---
# <a name="iwmpcontrolspause-method"></a>IWMPControls：:p ause 方法

**Pause** 方法會暫停播放媒體專案。

## <a name="syntax"></a>語法


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當檔案暫停時，Windows Media Player 不會提供任何系統資源，例如音訊裝置。

若要判斷特定媒體類型是否可以暫停，請將 **system.string** 值 "pause" 傳遞給 **IWMPControls. isAvailable** 屬性， (c # ) 中的 **IWMPControls. get \_ isAvailable** 方法。

## <a name="examples"></a>範例

下列範例會使用 **pause** 來暫停播放目前媒體專案，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

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
</dt> </dl>

 

 






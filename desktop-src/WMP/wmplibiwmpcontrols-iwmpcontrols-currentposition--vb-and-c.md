---
title: IWMPControls currentPosition 屬性
description: CurrentPosition 屬性會從開頭取得或設定媒體專案中的目前位置（以秒為單位）。
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- currentPosition 屬性 Windows Media Player
- currentPosition 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentPosition 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053666"
---
# <a name="iwmpcontrolscurrentposition-property"></a>IWMPControls：： currentPosition 屬性

**CurrentPosition** 屬性會從開頭取得或設定媒體專案中的目前位置（以秒為單位）。

## <a name="syntax"></a>Syntax


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>屬性值

目前位置的 **雙精度浮點數** 。

## <a name="examples"></a>範例

下列範例會使用 **currentPosition** 來搜尋使用者提供的位置。 為了回應按鈕的點擊， **currentPosition** 會設為在名為 newPosition 的文字方塊中輸入的值。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**IWMPControls. currentPositionString (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 






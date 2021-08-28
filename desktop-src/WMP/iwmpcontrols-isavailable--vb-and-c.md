---
title: 'IWMPControls. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054846"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls. isAvailable (VB 和 c # ) 

**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>參數

*bstrItem*

System.string，這是下列其中一個值。



| 值           | 描述                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | 探索使用者是否可以設定 **IWMPControls currentItem** 屬性。                                                                                     |
| currentMarker   | 探索使用者是否可以搜尋特定標記。                                                                                                         |
| currentPosition | 探索使用者是否可以搜尋檔案中的特定位置。 有些檔案不支援搜尋。                                                        |
| fastForward     | 探索檔案是否支援快速轉送以及是否可叫用該功能。 許多檔案類型 (和即時資料流) 不支援 fastForward。 |
| fastReverse     | 探索檔案是否支援 fastReverse，以及是否可叫用該功能。 許多檔案類型 (和即時資料流) 不支援 fastReverse。     |
| 下一步            | 探索使用者是否可以搜尋播放清單中的下一個專案。                                                                                              |
| pause           | 探索 **IWMPControls** 方法是否可用。                                                                                                 |
| 玩遊戲            | 探索 IWMPControls 的 **播放** 方法是否可用。                                                                                                  |
| previous        | 探索使用者是否可以搜尋播放清單中的上一個專案。                                                                                          |
| 步驟            | 探索是否可在播放期間使用 **IWMPControls2** 方法。                                                                                 |
| stop            | 探索 **IWMPControls. stop** 方法是否可用。                                                                                                  |



 

## <a name="property-value"></a>屬性值

**System.Boolean**

**布林值**，指出指定的資訊類型是否可用，或是否可以執行指定的動作。

## <a name="remarks"></a>備註

**IWMPControls. isAvailable** 是 Visual Basic 中接受參數的屬性。 在 c # 中，它稱為 **IWMPControls. get \_ isAvailable** 方法。

## <a name="examples"></a>範例

下列範例會使用 **isAvailable** 屬性 (c # ) 中的 **get \_ isAvailable** 方法，以確認目前的媒體專案支援 **currentPosition** 屬性。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
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

[**IWMPControls. currentItem (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls： pause (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2 VB 和 c # ) 的步驟 (**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 






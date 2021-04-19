---
title: 'IWMPControls (VB 和 C ) 介面 (h.264. h) '
description: 提供一種方式，藉由代表 Windows Media Player 的傳輸控制項（例如播放、停止和暫停）來操作媒體專案的播放。 IWMPControls 介面會公開下列屬性。
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls (VB 和 C ) 介面 Windows Media Player
- IWMPControls (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994091"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>IWMPControls (VB 和 c # ) 介面

提供一種方式，藉由代表 Windows Media Player 的傳輸控制項（例如播放、停止和暫停）來操作媒體專案的播放。

**IWMPControls** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPControls (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPControls (VB 和 c # )** 介面都有這些方法。



| 方法                                                                       | 描述                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**fastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | 以正向方向啟動媒體專案的快速播放。<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | 以相反方向啟動媒體專案的快速播放。<br/>                     |
| [**下**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | 將播放清單中的下一個專案設定為目前的專案。<br/>                          |
| [**暫停**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | 暫停媒體專案的播放。<br/>                                               |
| [**玩**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | 開始播放目前的媒體專案，或繼續播放暫停的專案。<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | 播放指定的媒體專案。<br/>                                                  |
| [**以前**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | 將播放清單中的上一個專案設定為目前的專案。<br/>                      |
| [**停止**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | 停止播放媒體專案。<br/>                                                |



 

### <a name="properties"></a>屬性

**IWMPControls (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                                    | 存取類型           | Description                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**currentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | 讀取/寫入<br/> | 取得或設定播放清單中目前的媒體專案。<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | 讀取/寫入<br/> | 取得或設定目前的標記編號。<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | 讀取/寫入<br/> | 從開頭取得或設定媒體專案中的目前位置（以秒為單位）。<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | 唯讀<br/>  | 取得媒體專案中做為 **system.string** 的目前位置。<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | 唯讀<br/>  | 取得值，這個值表示指定的資訊類型是否可用，或是否可以執行指定的動作。 在 c # 中，這是 **get \_ isAvailable** 方法。<br/> |



 

使用下列屬性來取得 **IWMPControls** 介面。



| Object                                                                   | 屬性                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls2 介面 (VB 和 c # )**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**IWMPControls3 介面 (VB 和 c # )**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 






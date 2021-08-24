---
title: AxWindowsMediaPlayer 物件的 PositionChange 事件
description: 當媒體專案中目前的播放位置變更時，就會發生 PositionChange 事件。
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- AxWindowsMediaPlayer 物件的 PositionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269d83c92687b5debda8b70fb4d6710b55eebd5476153759ebad36e5d17657d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764678"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 PositionChange 事件

當媒體專案中目前的播放位置變更時，就會發生 PositionChange 事件。

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ PositionChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ PositionChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性    | 描述                                         |
|-------------|-----------------------------------------------------|
| oldPosition | DoubleSpecifies 舊的位置。<br/> |
| newPosition | DoubleSpecifies 新的位置。<br/> |



 

## <a name="remarks"></a>備註

此事件不會在播放期間定期引發。 只有在主動變更播放媒體專案的目前位置時（例如當使用者移動搜尋控制碼，或執行程式碼以指定 IWMPControls 的值）時，才會發生此問題。**currentPosition**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentPosition (VB 和 c # )**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 






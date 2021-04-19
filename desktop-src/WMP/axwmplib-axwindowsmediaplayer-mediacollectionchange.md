---
title: AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件
description: 當媒體集合變更時，就會發生 MediaCollectionChange 事件。 |AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000944"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 MediaCollectionChange 事件

當媒體集合變更時，就會發生 MediaCollectionChange 事件。

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a>事件資料

此事件不包含資料。

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

[**AxWindowsMediaPlayer. mediaCollection (VB 和 c # )**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






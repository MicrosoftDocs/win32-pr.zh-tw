---
title: AxWindowsMediaPlayer 物件的 CdromMediaChange 事件
description: 從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 CdromMediaChange 事件。 |AxWindowsMediaPlayer 物件的 CdromMediaChange 事件
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- AxWindowsMediaPlayer 物件的 CdromMediaChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dac05b3ca8a8675bfae431d3f2e8ffbb38db8701a2501fa80d282cd3c976ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054999"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromMediaChange 事件

從 CD 或 DVD 光碟機插入或退出 CD 或 DVD 時，就會發生 **CdromMediaChange** 事件。

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromMediaChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromMediaChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                        |
|----------|--------------------------------------------------------------------|
| CdromNum | Int32Specifies CD 或 DVD 光碟機的索引。<br/> |



 

## <a name="remarks"></a>備註

CD 光碟機的索引會對應到可透過 IWMPCdromCollection 介面存取之 IWMPCdrom 介面的索引。

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

[**IWMPCdrom 介面 (VB 和 c # )**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection 介面 (VB 和 c # )**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 






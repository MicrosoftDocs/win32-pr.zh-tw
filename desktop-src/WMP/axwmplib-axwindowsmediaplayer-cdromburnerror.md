---
title: AxWindowsMediaPlayer 物件的 CdromBurnError 事件
description: 在 CD 燒錄操作期間發生一般錯誤時，就會發生 CdromBurnError 事件。
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864738"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromBurnError 事件

在 CD 燒錄操作期間發生一般錯誤時，就會發生 CdromBurnError 事件。

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnErrorEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnErrorEvent**，其中包含與這個事件相關的下列屬性。



| 屬性   | 描述                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System.object** 引發事件的錯誤。<br/>                                               |
| pCdromBurn | 代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。<br/> |



 

## <a name="remarks"></a>備註

若要捕獲媒體特定的錯誤，請處理 AxWMPLib。 \_WMPOCXEvents \_ CdromBurnMediaError 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11<br/>                                                                                         |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. CdromBurnMediaError 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 






---
title: AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件
description: 將個別媒體專案燒錄至 CD 時，發生錯誤時，就會發生 CdromBurnMediaError 事件。
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765267"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromBurnMediaError 事件

將個別媒體專案燒錄至 CD 時，發生錯誤時，就會發生 CdromBurnMediaError 事件。

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnMediaErrorEvent**，其中包含與這個事件相關的下列屬性。



| 屬性   | 描述                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdromBurn | 代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。<br/>               |
| pMedia     | 引發錯誤的 ObjectThe 媒體專案。 您可以將此轉換成 IWMPMedia 介面來存取它。<br/> |



 

## <a name="remarks"></a>備註

若要捕獲一般錯誤，請處理 AxWMPLib。 \_WMPOCXEvents \_ CdromBurnError 事件。

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

[**AxWindowsMediaPlayer. CdromBurnError 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






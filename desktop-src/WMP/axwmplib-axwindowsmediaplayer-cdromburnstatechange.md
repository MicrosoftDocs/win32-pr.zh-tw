---
title: AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件
description: 當 CD 燒錄操作變更狀態時，就會發生 CdromBurnStateChange 事件。
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28a8dfad6e5d9bc7bb603632e2eb08ceb5810f9bf02f395d825fc2d7ac64c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055036"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 CdromBurnStateChange 事件

當 CD 燒錄操作變更狀態時，就會發生 CdromBurnStateChange 事件。

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ CdromBurnStateChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ CdromBurnStateChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性   | 描述                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromBurn | 代表引發錯誤之燒錄作業的 WMPLib IWMPCdromBurnThe 介面。<br/> |
| wmpbs      | WMPLib，表示新狀態的 WMPBurnStateThe 列舉值。<br/>                         |



 

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

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 






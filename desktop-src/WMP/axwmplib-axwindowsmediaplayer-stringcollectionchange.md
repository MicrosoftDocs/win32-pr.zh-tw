---
title: AxWindowsMediaPlayer 物件的 StringCollectionChange 事件
description: 當字串集合變更時，就會發生 StringCollectionChange 事件。 |AxWindowsMediaPlayer 物件的 StringCollectionChange 事件
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- AxWindowsMediaPlayer 物件的 StringCollectionChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986568"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 StringCollectionChange 事件

當字串集合變更時，就會發生 StringCollectionChange 事件。

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ StringCollectionChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ StringCollectionChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性              | 描述                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| pdispStringCollection | 已變更的 ObjectThe 字串集合專案。 您可以將此轉換成 IWMPStringCollection 介面來存取它。<br/> |
| lCollectionIndex      | 已變更之字串收集項目的 Int32The 索引。<br/>                                                          |
| 變更                | WMPLib. WMPStringCollectionChangeEventTypeAn 列舉值，表示發生的變更類型。<br/>                 |



 

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

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**WMPStringCollectionChangeEventType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 






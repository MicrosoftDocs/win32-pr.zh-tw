---
title: AxWindowsMediaPlayer 物件的 DomainChange 事件
description: 當 DVD 網域變更時，就會發生 DomainChange 事件。 |AxWindowsMediaPlayer 物件的 DomainChange 事件
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- AxWindowsMediaPlayer 物件的 DomainChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000917"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 DomainChange 事件

當 DVD 網域變更時，就會發生 DomainChange 事件。

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DomainChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DomainChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性  | 描述                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| strDomain | StringIndicates 新網域。 如需了解可能的值，請參閱＜備註＞一節。<br/> |



 

## <a name="remarks"></a>備註

下表顯示 strDomain 屬性的可能值。



| String            | Description                                                          |
|-------------------|----------------------------------------------------------------------|
| firstPlay         | 執行 DVD 光碟的預設初始化。                     |
| videoManagerMenu  | 顯示整個光碟的功能表。也稱為根功能表或 topMenu。 |
| videoTitleSetMenu | 顯示目前標題集的功能表。 也稱為 titleMenu。     |
| title             | 顯示目前的標題。                                        |
| stop              | DVD 導覽器位於 DVD 停止網域中。                         |



 

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

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 






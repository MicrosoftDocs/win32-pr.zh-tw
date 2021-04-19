---
title: AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件
description: 當資料夾監控操作變更狀態時，就會發生 FolderScanStateChange 事件。
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989252"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 FolderScanStateChange 事件

當資料夾監控操作變更狀態時，就會發生 FolderScanStateChange 事件。

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ FolderScanStateChangeEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ FolderScanStateChangeEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| wmpfss   | WMPLib，表示新狀態的 WMPFolderScanStateThe 列舉值。<br/> |



 

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

[**WMPFolderScanState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 






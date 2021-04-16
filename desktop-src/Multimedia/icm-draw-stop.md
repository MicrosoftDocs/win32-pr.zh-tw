---
title: 'ICM_DRAW_STOP 訊息 (Vfw .h) '
description: ICM \_ 繪製 \_ 停止訊息會通知轉譯驅動程式，以在繪製框架的時機停止其內部時鐘。 您可以使用 ICDrawStop 宏明確地傳送此訊息。
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464993"
---
# <a name="icm_draw_stop-message"></a>ICM \_ 繪圖 \_ 停止訊息

**ICM \_ 繪製 \_ 停止** 訊息會通知轉譯驅動程式，以在繪製框架的時機停止其內部時鐘。 您可以使用 [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) 宏明確地傳送此訊息。


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






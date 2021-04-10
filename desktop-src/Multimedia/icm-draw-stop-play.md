---
title: 'ICM_DRAW_STOP_PLAY 訊息 (Vfw .h) '
description: '\_ \_ 當播放作業完成時，ICM DRAW 停止 \_ 播放訊息會通知轉譯驅動程式。 您可以使用 ICDrawStopPlay 宏明確地傳送此訊息。'
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106553"
---
# <a name="icm_draw_stop_play-message"></a>ICM \_ 繪圖 \_ 停止 \_ 播放訊息

當播放作業完成時， **ICM \_ DRAW \_ 停止 \_ 播放** 訊息會通知轉譯驅動程式。 您可以使用 [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) 宏明確地傳送此訊息。


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

當播放作業完成時，請使用此訊息。 使用 [**ICM \_ 繪製 \_ 停止**](icm-draw-stop.md) 訊息來結束計時。

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

 

 






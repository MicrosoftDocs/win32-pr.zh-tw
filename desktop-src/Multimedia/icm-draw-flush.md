---
title: 'ICM_DRAW_FLUSH 訊息 (Vfw .h) '
description: ICM 繪圖排清 \_ \_ 訊息會通知轉譯驅動程式，以轉譯任何等候繪製之影像緩衝區的內容。 您可以使用 ICDrawFlush 宏明確地傳送此訊息。
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966121"
---
# <a name="icm_draw_flush-message"></a>ICM \_ 繪製 \_ 清除訊息

**ICM \_ 繪圖 \_** 排清訊息會通知轉譯驅動程式，以轉譯任何等候繪製之影像緩衝區的內容。 您可以使用 [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) 宏明確地傳送此訊息。


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

這則訊息只會由執行自己的非同步解壓縮、時間和繪圖的硬體使用。

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

 

 






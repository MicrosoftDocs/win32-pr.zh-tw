---
title: 'ICM_DRAW_RENDERBUFFER 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ RENDERBUFFER 訊息會通知轉譯驅動程式，以繪製已傳遞給它的框架。 您可以使用 ICDrawRenderBuffer 宏明確地傳送此訊息。
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934843"
---
# <a name="icm_draw_renderbuffer-message"></a>ICM \_ 繪圖 \_ RENDERBUFFER 訊息

**ICM \_ DRAW \_ RENDERBUFFER** 訊息會通知轉譯驅動程式，以繪製已傳遞給它的框架。 您可以使用 [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) 宏明確地傳送此訊息。


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

使用此訊息搭配執行自己的非同步解壓縮、計時和繪製的硬體。

此訊息通常用來執行搜尋作業，而必須特別指示驅動程式顯示每個傳遞給它的影片畫面，而不是播放一連串的影片畫面。

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

 

 






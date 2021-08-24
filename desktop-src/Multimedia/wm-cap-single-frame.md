---
title: 'WM_CAP_SINGLE_FRAME 訊息 (Vfw .h) '
description: WM \_ cap \_ 單一 \_ 框架訊息會將單一畫面附加至使用 WM \_ cap \_ 單一 \_ 框架 \_ 開啟訊息開啟的捕獲檔案。 您可以使用 capCaptureSingleFrame 宏明確地傳送此訊息。
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891788"
---
# <a name="wm_cap_single_frame-message"></a>WM \_ CAP \_ 單一 \_ 畫面格訊息

**WM \_ cap \_ 單一 \_ 框架** 訊息會將單一畫面附加至使用 [**WM \_ cap \_ 單一 \_ 框架 \_ 開啟**](wm-cap-single-frame-open.md)訊息開啟的捕獲檔案。 您可以使用 [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) 宏明確地傳送此訊息。


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 






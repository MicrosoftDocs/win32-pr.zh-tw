---
title: 'WM_CAP_GRAB_FRAME_NOSTOP 訊息 (Vfw .h) '
description: '[WM \_ 端點 \_ 抓取 \_ 框架] \_ NOSTOP 訊息會以單一未壓縮的框架（取自捕獲裝置）填滿框架緩衝區，並加以顯示。'
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622597"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>WM \_ CAP \_ 抓取 \_ 框架 \_ NOSTOP 訊息

[ **WM \_ 端點 \_ 抓取 \_ 框架] \_ NOSTOP** 訊息會以單一未壓縮的框架（取自捕獲裝置）填滿框架緩衝區，並加以顯示。 不同于 [**WM \_ CAP \_ 抓取 \_ 框架**](wm-cap-grab-frame.md) 訊息，此訊息不會改變重迭或預覽的狀態。 您可以使用 [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) 宏明確地傳送此訊息。


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如需安裝回呼函式的詳細資訊，請參閱 [**wm \_ cap \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 和 [**wm \_ \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md) 訊息。

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

 

 






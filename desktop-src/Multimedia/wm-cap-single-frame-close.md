---
title: 'WM_CAP_SINGLE_FRAME_CLOSE 訊息 (Vfw .h) '
description: WM \_ cap \_ 單一 \_ 框架 \_ 關閉訊息會關閉由 wm \_ cap \_ 單一 \_ 框架開啟的 \_ 訊息開啟的捕獲檔案。 您可以使用 capCaptureSingleFrameClose 宏明確地傳送此訊息。
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686451"
---
# <a name="wm_cap_single_frame_close-message"></a>WM \_ CAP \_ 單一 \_ 框架 \_ 關閉訊息

**Wm \_ cap \_ 單一 \_ 框架 \_ 關閉** 訊息會關閉由 [**wm \_ cap \_ 單一 \_ 框架 \_ 開啟**](wm-cap-single-frame-open.md)的訊息開啟的捕獲檔案。 您可以使用 [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) 宏明確地傳送此訊息。


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
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

 

 






---
title: 'WM_CAP_SINGLE_FRAME_OPEN 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 單一 \_ 畫面格 \_ 開啟訊息] 會開啟單一畫面格捕獲的捕獲檔案。 捕捉檔案中的任何先前資訊都會遭到覆寫。 您可以使用 capCaptureSingleFrameOpen 宏明確地傳送此訊息。'
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134833"
---
# <a name="wm_cap_single_frame_open-message"></a>WM \_ CAP \_ 單一 \_ 框架 \_ 開啟訊息

[ **WM \_ CAP \_ 單一 \_ 畫面格 \_ 開啟** 訊息] 會開啟單一畫面格捕獲的捕獲檔案。 捕捉檔案中的任何先前資訊都會遭到覆寫。 您可以使用 [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) 宏明確地傳送此訊息。


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 






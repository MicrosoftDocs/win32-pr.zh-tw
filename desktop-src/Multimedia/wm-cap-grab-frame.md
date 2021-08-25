---
title: 'WM_CAP_GRAB_FRAME 訊息 (Vfw .h) '
description: WM \_ CAP \_ 抓取 \_ 框架訊息會從 capture 驅動程式取出並顯示單一畫面格。 在 capture 之後，會停用覆迭和預覽。 您可以使用 capGrabFrame 宏明確地傳送此訊息。
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdccfc9df0f3abac7febfa78029b4ecb351ec3044c618dc4c811e91b433f0f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892038"
---
# <a name="wm_cap_grab_frame-message"></a>WM \_ 上限 \_ 抓取 \_ 框架訊息

**WM \_ CAP \_ 抓取 \_ 框架** 訊息會從 capture 驅動程式取出並顯示單一畫面格。 在 capture 之後，會停用覆迭和預覽。 您可以使用 [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) 宏明確地傳送此訊息。


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
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

 

 






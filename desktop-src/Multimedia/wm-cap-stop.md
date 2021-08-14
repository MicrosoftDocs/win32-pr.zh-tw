---
title: 'WM_CAP_STOP 訊息 (Vfw .h) '
description: WM \_ CAP \_ 停止訊息會停止捕獲操作。 您可以使用 capCaptureStop 宏明確地傳送此訊息。
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369327"
---
# <a name="wm_cap_stop-message"></a>WM \_ CAP \_ 停止訊息

**WM \_ CAP \_ 停止** 訊息會停止捕獲操作。 您可以使用 [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) 宏明確地傳送此訊息。

在步驟框架捕獲中，傳送此訊息之前所收集的影像資料會保留在 capture 檔案中。 如果啟用音訊捕捉，則相同的音訊資料持續時間也會保留在 capture 檔案中。


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

捕捉作業必須採用此訊息。 使用 [**WM \_ CAP \_ ABORT**](wm-cap-abort.md) 訊息放棄目前的捕獲作業。

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

 

 






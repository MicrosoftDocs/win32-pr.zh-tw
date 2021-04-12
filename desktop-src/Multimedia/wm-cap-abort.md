---
title: 'WM_CAP_ABORT 訊息 (Vfw .h) '
description: WM \_ CAP \_ ABORT 訊息會停止捕捉作業。
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508539"
---
# <a name="wm_cap_abort-message"></a>WM \_ CAP \_ 中止訊息

**WM \_ CAP \_ ABORT** 訊息會停止捕捉作業。 在步驟捕捉的案例中，會將收集到 **WM \_ CAP \_ 中止** 訊息點的影像資料保留在 capture 檔案中，但不會捕獲音訊。 您可以使用 [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) 宏明確地傳送此訊息。


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

捕捉作業必須採用此訊息。

使用 [**WM \_ CAP \_ 停止**](wm-cap-stop.md) 訊息，在目前的位置停止步驟捕捉，然後捕獲音訊。

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

 

 






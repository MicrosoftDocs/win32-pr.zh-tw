---
title: 'WM_CAP_EDIT_COPY 訊息 (Vfw .h) '
description: WM \_ CAP \_ 編輯 \_ 複製訊息會將影片框架緩衝區和相關聯的調色板內容複寫到剪貼簿。 您可以使用 capEditCopy 宏明確地傳送此訊息。
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104700"
---
# <a name="wm_cap_edit_copy-message"></a>WM \_ CAP \_ 編輯 \_ 複製訊息

**WM \_ CAP \_ 編輯 \_ 複製** 訊息會將影片框架緩衝區和相關聯的調色板內容複寫到剪貼簿。 您可以使用 [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) 宏明確地傳送此訊息。


```C++
WM_CAP_EDIT_COPY 
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

 

 






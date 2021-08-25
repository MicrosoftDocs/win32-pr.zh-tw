---
title: 'WM_CAP_GET_USER_DATA 訊息 (Vfw .h) '
description: WM \_ CAP \_ 取得 \_ 使用者 \_ 資料訊息會 \_ 抓取與捕捉視窗相關聯的長 PTR 資料值。 您可以使用 capGetUserData 宏明確地傳送此訊息。
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a79a513d415d166ab2715a181a6d8fc366b60480caf2982f6bbc53eadf90d96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892028"
---
# <a name="wm_cap_get_user_data-message"></a>WM \_ CAP \_ 取得 \_ 使用者 \_ 資料訊息

**WM \_ CAP \_ 取得 \_ 使用者 \_ 資料** 訊息會抓取與捕捉視窗相關聯的 **長 \_ PTR** 資料值。 您可以使用 [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

傳回先前使用 [**WM \_ CAP \_ SET \_ 使用者 \_ 資料**](wm-cap-set-user-data.md) 訊息儲存的值。

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

 

 






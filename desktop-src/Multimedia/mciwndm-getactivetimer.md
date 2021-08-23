---
title: 'MCIWNDM_GETACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ GETACTIVETIMER 訊息會抓取 MCIWnd 視窗為使用中視窗時所使用的更新期間。 您可以使用 MCIWndGetActiveTimer 宏明確地傳送此訊息。
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc542e5a4b43b974eb7f28bc59d8e2fab7547834f28b5bccb6ea46f978e2158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525518"
---
# <a name="mciwndm_getactivetimer-message"></a>MCIWNDM \_ GETACTIVETIMER 訊息

**MCIWNDM \_ GETACTIVETIMER** 訊息會抓取 MCIWnd 視窗為使用中視窗時所使用的更新期間。 您可以使用 [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

傳回更新期間（以毫秒為單位）。 預設值為500毫秒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 






---
title: 'MCIWNDM_GETINACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ GETINACTIVETIMER 訊息會抓取 MCIWnd 視窗為非作用中視窗時所使用的更新期間。 您可以使用 MCIWndGetInactiveTimer 宏明確地傳送此訊息。
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969140"
---
# <a name="mciwndm_getinactivetimer-message"></a>MCIWNDM \_ GETINACTIVETIMER 訊息

**MCIWNDM \_ GETINACTIVETIMER** 訊息會抓取 MCIWnd 視窗為非作用中視窗時所使用的更新期間。 您可以使用 [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回更新期間（以毫秒為單位）。 預設值為2000毫秒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 






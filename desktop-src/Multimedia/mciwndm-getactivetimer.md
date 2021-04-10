---
title: 'MCIWNDM_GETACTIVETIMER 訊息 (Vfw .h) '
description: MCIWNDM \_ GETACTIVETIMER 訊息會抓取 MCIWnd 視窗為使用中視窗時所使用的更新期間。 您可以使用 MCIWndGetActiveTimer 宏明確地傳送此訊息。
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER message Windows 多媒體
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
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106530"
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

 

 






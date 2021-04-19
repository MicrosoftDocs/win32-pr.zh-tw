---
title: 'MCIWNDM_GETSTYLES 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSTYLES 訊息會抓取指定視窗所使用之目前 MCIWnd 視窗樣式的旗標。 您可以使用 MCIWndGetStyles 宏明確地傳送此訊息。
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966953"
---
# <a name="mciwndm_getstyles-message"></a>MCIWNDM \_ GETSTYLES 訊息

**MCIWNDM \_ GETSTYLES** 訊息會抓取指定視窗所使用之目前 MCIWnd 視窗樣式的旗標。 您可以使用 [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

傳回值，表示 MCIWnd 視窗目前的樣式。 傳回值是 MCIWnd 視窗樣式的位 OR 運算子， (MCIWNDF 旗標) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 






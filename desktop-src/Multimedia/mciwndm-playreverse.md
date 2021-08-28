---
title: 'MCIWNDM_PLAYREVERSE 訊息 (Vfw .h) '
description: MCIWNDM \_ PLAYREVERSE 訊息會以反向方向播放目前的內容，從目前位置開始，結束于內容的開頭，或直到另一個命令停止播放為止。
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5664ea53f73745648e668a78a6dc5f6da28a9cb27d54b96fced09523f655ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037968"
---
# <a name="mciwndm_playreverse-message"></a>MCIWNDM \_ PLAYREVERSE 訊息

**MCIWNDM \_ PLAYREVERSE** 訊息會以反向方向播放目前的內容，從目前位置開始，結束于內容的開頭，或直到另一個命令停止播放為止。 您可以使用 [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) 宏明確地傳送此訊息。


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 






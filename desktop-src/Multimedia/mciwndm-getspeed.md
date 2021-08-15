---
title: 'MCIWNDM_GETSPEED 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSPEED 訊息會捕獲 MCI 裝置的播放速度。 您可以使用 MCIWndGetSpeed 宏明確地傳送此訊息。
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42749fb2f99c446dbd45bc6e2497287ab3b0ce987c9343ed4580735c760cc892
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429248"
---
# <a name="mciwndm_getspeed-message"></a>MCIWNDM \_ GETSPEED 訊息

**MCIWNDM \_ GETSPEED** 訊息會捕獲 MCI 裝置的播放速度。 您可以使用 [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果成功，則傳回播放速度。 正常速度的值是1000。 較大的值表示速度更快，較小的值表示速度較慢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 






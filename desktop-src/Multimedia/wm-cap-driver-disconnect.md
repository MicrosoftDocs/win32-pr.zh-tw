---
title: 'WM_CAP_DRIVER_DISCONNECT 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 驅動程式 \_ 中斷連線] 訊息會中斷捕捉驅動程式與捕捉視窗的連線。 您可以使用 capDriverDisconnect 宏明確地傳送此訊息。'
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803858"
---
# <a name="wm_cap_driver_disconnect-message"></a>WM \_ CAP \_ 驅動程式 \_ 中斷連線訊息

[ **WM \_ CAP \_ 驅動程式 \_ 中斷連線]** 訊息會中斷捕捉驅動程式與捕捉視窗的連線。 您可以使用 [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) 宏明確地傳送此訊息。


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ，如果捕捉視窗未連接到 capture 驅動程式，則傳回 **FALSE** 。

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

 

 






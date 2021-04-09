---
title: 'WM_CAP_PAL_PASTE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ 貼上訊息會從剪貼簿複製元件，並將它傳遞至 capture 驅動程式。 您可以使用 capPalettePaste 宏明確地傳送此訊息。
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934175"
---
# <a name="wm_cap_pal_paste-message"></a>WM \_ CAP \_ PAL \_ 貼上訊息

**WM \_ CAP \_ PAL \_ 貼** 上訊息會從剪貼簿複製元件，並將它傳遞至 capture 驅動程式。 您可以使用 [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) 宏明確地傳送此訊息。


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

捕捉驅動程式會在指定的數位化影片格式需要時使用調色板。

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

 

 






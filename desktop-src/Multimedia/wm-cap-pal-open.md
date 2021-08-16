---
title: 'WM_CAP_PAL_OPEN 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL 開啟的 \_ 訊息會從調色板檔案載入新的元件，並將它傳遞至 capture 驅動程式。
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb831ca0128b0562d6ee53b8e66309d2e1dbd91803dab13202dc4a6723bfa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800577"
---
# <a name="wm_cap_pal_open-message"></a>WM \_ CAP \_ PAL \_ 開啟訊息

**WM \_ CAP \_ PAL \_ 開啟** 的訊息會從調色板檔案載入新的元件，並將它傳遞至 capture 驅動程式。 調色板檔案通常會使用副檔名。朋友。 捕捉驅動程式會在指定的數位化影像格式需要時使用調色板。 您可以使用 [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) 宏明確地傳送此訊息。


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

包含調色板檔案名之以 null 結尾的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

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

 

 






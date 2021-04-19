---
title: 'WM_CAP_PAL_AUTOCREATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ 會自動建立訊息要求 capture 驅動程式範例影片框架，並自動建立新的調色板。 您可以使用 capPaletteAuto 宏明確地傳送此訊息。
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969575"
---
# <a name="wm_cap_pal_autocreate-message"></a>WM \_ CAP \_ PAL 自動顯示 \_ 訊息

**WM \_ CAP \_ PAL \_** 會自動建立訊息要求 capture 驅動程式範例影片框架，並自動建立新的調色板。 您可以使用 [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) 宏明確地傳送此訊息。


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframe*
</dt> <dd>

要取樣的框架數目。

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

調色板中的色彩數目。 此參數的最大值為256。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

取樣的影片順序應該包含您在 [調色板] 中所需的所有色彩。 若要取得最佳的調色板，您可能必須取樣整個序列，而不是它的一部分。

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

 

 






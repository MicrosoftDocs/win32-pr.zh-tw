---
title: 'MCIWNDM_REALIZE 訊息 (Vfw .h) '
description: MCIWNDM \_ 實現訊息會在 MCIWnd 視窗中瞭解 MCI 裝置目前所使用的調色板。 這個宏是使用 MCIWNDM 的實現訊息來定義的 \_ 。 您可以使用 MCIWndRealize 宏明確地傳送此訊息。
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fdbee3757e1fd3aada5292b86cc37577ccb718315c5b81140ceb14278c37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012616"
---
# <a name="mciwndm_realize-message"></a>MCIWNDM \_ 實現訊息

**MCIWNDM \_ 實現** 訊息會在 MCIWnd 視窗中瞭解 MCI 裝置目前所使用的調色板。 這個宏是使用 MCIWNDM 的 **\_ 實現** 訊息來定義的。 您可以使用 [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) 宏明確地傳送此訊息。


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

背景旗標。 如果視窗是背景應用程式，請為此參數指定 **TRUE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

**MCIWNDM \_**「請注意」會使用 MCI 裝置的選擇區，並呼叫 [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)函式。 如果您的應用程式明確處理 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 訊息，您應該在應用程式中使用此訊息，而不是使用 **RealizePalette**。 如果其中一個訊息處理常式的主體只包含 **RealizePalette**，則會將訊息轉寄至 MCIWnd 視窗，這將會自動實現調色板。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 


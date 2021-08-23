---
title: 'WM_CAP_PAL_MANUALCREATE 訊息 (Vfw .h) '
description: WM \_ CAP \_ PAL \_ MANUALCREATE 訊息要求 capture 驅動程式手動取樣影片畫面，並建立新的調色板。 您可以使用 capPaletteManual 宏明確地傳送此訊息。
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8cc313cb6eae8e757d0777642bbc0ab72fe07fcfbf5b530a6479675c8ab3c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781289"
---
# <a name="wm_cap_pal_manualcreate-message"></a>WM \_ CAP \_ PAL \_ MANUALCREATE 訊息

**WM \_ CAP \_ PAL \_ MANUALCREATE** 訊息要求 capture 驅動程式手動取樣影片畫面，並建立新的調色板。 您可以使用 [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) 宏明確地傳送此訊息。


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

選用區長條圖旗標。 針對建立最佳調色板中包含的每個畫面格，將此參數設定為 **TRUE** 。 在收集最後一個畫面格之後，請將此參數設定為 **FALSE** ，以計算最佳的選擇區，並將它傳送至 capture 驅動程式。

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

調色板中的色彩數目。 此參數的最大值為256。 只有在序列中的第一個框架收集期間，才會使用這個值。

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

 

 






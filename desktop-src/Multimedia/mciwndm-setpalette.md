---
title: 'MCIWNDM_SETPALETTE 訊息 (Vfw .h) '
description: MCIWNDM \_ SETPALETTE 訊息會將調色板控制碼傳送至與 MCIWnd 視窗相關聯的 MCI 裝置。 您可以使用 MCIWndSetPalette 宏明確地傳送此訊息。
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525228"
---
# <a name="mciwndm_setpalette-message"></a>MCIWNDM \_ SETPALETTE 訊息

**MCIWNDM \_ SETPALETTE** 訊息會將調色板控制碼傳送至與 MCIWnd 視窗相關聯的 MCI 裝置。 您可以使用 [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

調色板控制碼。

</dd> </dl>

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

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 






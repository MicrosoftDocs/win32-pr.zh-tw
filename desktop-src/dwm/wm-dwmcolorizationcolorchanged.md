---
title: 'WM_DWMCOLORIZATIONCOLORCHANGED 訊息 (Winuser .h) '
description: 通知所有最上層視窗的顏色標示色彩已變更。
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdbb854821f2a25565241700d28964b2d32319bccb8226c3d7d789c0e457fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094588"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>WM \_ DWMCOLORIZATIONCOLORCHANGED 訊息

通知所有最上層視窗的顏色標示色彩已變更。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定新的顏色標示色彩。 色彩格式為0xAARRGGBB。

</dd> <dt>

*lParam* 
</dt> <dd>

指定新的色彩是否與不透明度混合。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) 用來判斷目前的色彩值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 


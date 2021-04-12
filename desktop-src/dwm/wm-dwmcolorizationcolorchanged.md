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
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103943"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 


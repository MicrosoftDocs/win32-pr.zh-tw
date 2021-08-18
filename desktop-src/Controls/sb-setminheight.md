---
title: 'SB_SETMINHEIGHT 訊息 (Commctrl .h) '
description: 設定狀態視窗之繪圖區域的最小高度。
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b644067e48312b265d132f7d06d53343c4612b879c3a09b638ebd0a98a7c88a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293728"
---
# <a name="sb_setminheight-message"></a>SB \_ SETMINHEIGHT 訊息

設定狀態視窗之繪圖區域的最小高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

視窗的最小高度（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

最小高度是 *wParam* 和狀態視窗垂直框線寬度（以圖元為單位）的總和。 應用程式必須將 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息傳送至狀態視窗，以重繪視窗。 **WM \_ 大小** 訊息的 *wParam* 和 *lParam* 參數應設為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


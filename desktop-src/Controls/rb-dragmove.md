---
title: 'RB_DRAGMOVE 訊息 (Commctrl .h) '
description: 更新在上一個 RB BEGINDRAG 訊息之後，Rebar 控制項中的拖曳位置 \_ 。
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409720"
---
# <a name="rb_dragmove-message"></a>RB \_ DRAGMOVE 訊息

更新在上一個 [**RB \_ BEGINDRAG**](rb-begindrag.md) 訊息之後，Rebar 控制項中的拖曳位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

包含新滑鼠座標的 **DWORD** 值。 水準座標是包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而垂直座標則是包含在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。 如果您傳遞 (DWORD) -1，Rebar 控制項將會使用滑鼠的位置，這是上一次控制項的執行緒，稱為 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage)。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 


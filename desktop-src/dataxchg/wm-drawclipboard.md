---
title: 'WM_DRAWCLIPBOARD 訊息 (Winuser .h) '
description: 當剪貼簿的內容變更時，傳送至剪貼簿檢視器鏈中的第一個視窗。 這可讓剪貼簿檢視器視窗顯示剪貼簿的新內容。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967536"
---
# <a name="wm_drawclipboard-message"></a>WM \_ DRAWCLIPBOARD 訊息

當剪貼簿的內容變更時，傳送至剪貼簿檢視器鏈中的第一個視窗。 這可讓剪貼簿檢視器視窗顯示剪貼簿的新內容。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="remarks"></a>備註

只有 [剪貼簿檢視器] 視窗會收到此訊息。 這些是使用 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函式新增至剪貼簿檢視器鏈的 windows。

每個接收 **WM \_ DRAWCLIPBOARD** 訊息的視窗都必須呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，以將訊息傳遞至剪貼簿檢視器鏈中的下一個視窗。 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)會傳回鏈中下一個視窗的控制碼，而且可能會變更以回應 [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 


---
title: 'WM_CHANGECBCHAIN 訊息 (Winuser .h) '
description: 從鏈中移除視窗時，傳送至剪貼簿檢視器鏈中的第一個視窗。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25dac74784a214f77f8b2912e2fd643624ae767027121e2262d81989d54d3831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736312"
---
# <a name="wm_changecbchain-message"></a>WM \_ CHANGECBCHAIN 訊息

從鏈中移除視窗時，傳送至剪貼簿檢視器鏈中的第一個視窗。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

從剪貼簿檢視器鏈中移除的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

在要移除的視窗後面的鏈中，下一個視窗的控制碼。 如果要移除的視窗是鏈中的最後一個視窗，則此參數為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

每個剪貼簿檢視器視窗都會將控制碼儲存至剪貼簿檢視器鏈中的下一個視窗。 一開始，這個控制碼是 [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) 函數的傳回值。

當剪貼簿檢視器視窗收到 **WM \_ CHANGECBCHAIN** 訊息時，它應該呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，將訊息傳遞至鏈中的下一個視窗，除非下一個視窗是要移除的視窗。 在此情況下，剪貼簿檢視器應該將 *lParam* 參數所指定的控制碼儲存為鏈中的下一個視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 


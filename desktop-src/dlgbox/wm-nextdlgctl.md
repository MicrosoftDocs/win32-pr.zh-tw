---
title: 'WM_NEXTDLGCTL 訊息 (Winuser .h) '
description: 傳送至對話方塊程式，將鍵盤焦點設定至對話方塊中的不同控制項。
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL 訊息對話方塊
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508952"
---
# <a name="wm_nextdlgctl-message"></a>WM \_ NEXTDLGCTL 訊息

傳送至對話方塊程式，將鍵盤焦點設定至對話方塊中的不同控制項。


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

如果 *lParam* 為 **TRUE**，則此參數會識別接收焦點的控制項。 如果 *lParam* 為 **FALSE**，則此參數會指出具有 **WS \_ TABSTOP** 樣式的下一個或上一個控制項是否會收到焦點。 如果 *wParam* 為零，則下一個控制項會接收焦點;否則，具有 **WS \_ TABSTOP** 樣式的先前控制項就會收到焦點。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字表示系統使用 *wParam* 的方式。 如果低序位字是 **TRUE**，則 *wParam* 是與接收焦點的控制項相關聯的控制碼;否則， *wParam* 是一個旗標，指出下一個或前一個具有 **WS \_ TABSTOP** 樣式的控制項是否會收到焦點。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

這則訊息會執行其他對話方塊管理作業，而非 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函式 **WM \_ NEXTDLGCTL** 會更新預設的按鍵框線、設定預設的控制項識別碼，並自動選取編輯控制項的文字 (如果目標視窗是編輯控制項) 。

如果您的應用程式將會同時處理設定焦點的其他訊息，請不要使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式來傳送 **WM \_ NEXTDLGCTL** 訊息。 請改用 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**概念**
</dt> <dt>

[對話方塊](dialog-boxes.md)
</dt> </dl>

 


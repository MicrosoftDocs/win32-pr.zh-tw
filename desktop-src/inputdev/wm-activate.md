---
title: 'WM_ACTI加值稅E 訊息 (Winuser .h) '
description: 傳送至正在啟動的視窗和停用的視窗。
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTI加值稅E 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094356"
---
# <a name="wm_activate-message"></a>WM \_ 啟用訊息

傳送至正在啟動的視窗和停用的視窗。 如果 windows 使用相同的輸入佇列，則會以同步方式將訊息傳送至即將停用之最上層視窗的視窗程式，然後再傳送至即將啟動之最上層視窗的視窗程式。 如果 windows 使用不同的輸入佇列，則會以非同步方式傳送訊息，因此會立即啟用視窗。


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位字組可指定視窗是否正在啟用或停用。 此參數可以是下列其中一個值。 高序位單字指定要啟動或停用視窗的最小化狀態。 非零值表示視窗最小化。



| 值                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**WA \_主動**</dt> <dt>1</dt> </dl>                | 由滑鼠點以外的某個方法啟用 (例如，透過呼叫 [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) 函式，或使用鍵盤介面選取視窗) 。<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**WA \_CLICKACTIVE**</dt> <dt>2</dt> </dl> | 由滑鼠按一下來啟用。<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**WA \_非**</dt>作用中 <dt>0</dt> </dl>          | 關閉。<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要啟用或停用的視窗控制碼（視 *wParam* 參數的值而定）。 如果 *wParam* 的低序位字是 **WA \_ 非** 使用中，則 *lParam* 是正在啟動之視窗的控制碼。 如果 *wParam* 的低序位字是 **Wa \_ ACTIVE** 或 **wa \_ CLICKACTIVE**， *lParam* 就是停用視窗的控制碼。 這個控制碼可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

如果視窗正在啟動且未最小化， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將鍵盤焦點設定為視窗。 如果視窗是由滑鼠按一下來啟動，它也會收到 [**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md) 訊息。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md)
</dt> <dt>

[**WM \_ NCACTI加值稅E**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


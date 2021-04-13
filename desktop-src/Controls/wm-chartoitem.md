---
title: 'WM_CHARTOITEM 訊息 (Winuser .h) '
description: 由具有磅 WANTKEYBOARDINPUT 樣式的清單方塊傳送 \_ 給其擁有者，以回應 WM \_ 字元訊息。
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322543"
---
# <a name="wm_chartoitem-message"></a>WM \_ CHARTOITEM 訊息

由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息。


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定使用者所按下之按鍵的字元碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))指定插入號的目前位置。

</dd> <dt>

*lParam* 
</dt> <dd>

清單方塊的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會指定應用程式在回應訊息時所執行的動作。 傳回值-1 或-2 表示應用程式已處理選取專案的所有層面，而不需要在清單方塊中採取進一步的動作。 傳回值0或以上會指定清單方塊中專案的以零為基底的索引，並指出清單方塊應該針對指定的專案執行擊鍵的預設動作。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回-1。

只有擁有者繪製的清單方塊沒有 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式可以接收此訊息。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 *DWL \_ MSGRESULT* 值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ 字元**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 


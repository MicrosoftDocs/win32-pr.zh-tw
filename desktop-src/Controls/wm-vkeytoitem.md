---
title: 'WM_VKEYTOITEM 訊息 (Winuser .h) '
description: 由具有磅 WANTKEYBOARDINPUT 樣式的清單方塊傳送 \_ 給其擁有者，以回應 WM \_ KEYDOWN 訊息。
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47c054952c74b8e66bb109b925cfbdc353ec97f7bebfb5b5cafaedf8857ccb5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957467"
---
# <a name="wm_vkeytoitem-message"></a>WM \_ VKEYTOITEM 訊息

由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息。


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定使用者所按下之金鑰的虛擬金鑰碼。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))指定插入號的目前位置。

</dd> <dt>

*lParam* 
</dt> <dd>

清單方塊的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會指定應用程式在回應訊息時所執行的動作。 傳回值-2 表示應用程式已處理選取專案的所有層面，且清單方塊不需要採取進一步的動作。  (請參閱 [備註]。 ) 傳回值-1 表示清單方塊應該執行預設動作來回應擊鍵。 傳回值0或以上會指定清單方塊中專案的索引，並指出清單方塊應該針對指定的專案執行擊鍵的預設動作。

## <a name="remarks"></a>備註

只有當清單方塊控制項未轉譯為字元的索引鍵時，才會傳回-2 的傳回值。 如果 [**wm 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息轉譯成 [**wm \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息，而應用程式處理由按鍵結果所產生的 **wm \_ VKEYTOITEM** 訊息，則清單方塊會忽略傳回值，並對該字元進行預設處理) 。 **WM \_** 由索引鍵產生的 KEYDOWN 訊息（例如 VK \_ UP、VK \_ DOWN、VK \_ NEXT 和 VK \_ PREVIOUS）不會轉譯為 **WM \_ 字元** 訊息。 在這種情況下，會捕捉 **WM \_ VKEYTOITEM** 訊息並傳回-2，以防止清單方塊執行該金鑰的預設處理。

若要對產生 char 訊息並進行特殊處理的索引鍵進行陷阱，應用程式必須將清單方塊設為子類別、將 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 和 [**wm \_ char**](/windows/desktop/inputdev/wm-char) 訊息設為子類別，並在子類別程式中適當地處理訊息。

上述備註適用于以 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式建立的一般清單方塊。 如果清單方塊是主控描繪的，應用程式必須處理 [**WM \_ CHARTOITEM**](wm-chartoitem.md) 訊息。

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函數會傳回-1。

如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **布林** 值，並直接傳回值。 \_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ CHARTOITEM**](wm-chartoitem.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 


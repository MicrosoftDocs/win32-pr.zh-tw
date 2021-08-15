---
title: 'WM_KEYUP 訊息 (Winuser .h) '
description: 當系統釋放非系統機碼時，以鍵盤焦點張貼至視窗。 非系統索引鍵是未按下 ALT 鍵時所按下的按鍵，或是當視窗具有鍵盤焦點時按下的鍵盤按鍵。
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc23b941f232007a781ca160538f28d864f818639df47a180de472f54cd89a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247820"
---
# <a name="wm_keyup-message"></a>WM \_ KEYUP 訊息

當系統釋放非系統機碼時，以鍵盤焦點張貼至視窗。 非系統索引鍵是 *未* 按下 ALT 鍵時所按下的按鍵，或是當視窗具有鍵盤焦點時按下的鍵盤按鍵。


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

非系統索引鍵的虛擬機器碼程式碼。 請參閱 [虛擬金鑰代碼](virtual-key-codes.md)。

</dd> <dt>

*lParam* 
</dt> <dd>

[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。



| Bits  | 意義                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | 目前訊息的重複計數。 值是當使用者按住按鍵時，按鍵 autorepeated 的次數。 針對 **WM \_ KEYUP** 訊息，重複計數一律為1。 |
| 16-23 | 掃描程式碼。 此值取決於 OEM。                                                                                                                                                                     |
| 24    | 指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。 如果它是擴充索引鍵，則此值為 1;否則，它是0。         |
| 25-28 | 保護請勿使用。                                                                                                                                                                                            |
| 29    | 內容程式碼。 **WM 的 \_ KEYUP** 訊息的值一律為0。                                                                                                                                             |
| 30    | 先前的金鑰狀態。 若為 **WM 的 \_ KEYUP** 訊息，此值一律為1。                                                                                                                                       |
| 31    | 轉換狀態。 若為 **WM 的 \_ KEYUP** 訊息，此值一律為1。                                                                                                                                         |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。
 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

如果放開了 F10 鍵或 ALT 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。 訊息的 *wParam* 參數設定為 SC \_ KEYMENU。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。

應用程式必須將 *wParam* 傳遞至 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ，而不需要加以變更。

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


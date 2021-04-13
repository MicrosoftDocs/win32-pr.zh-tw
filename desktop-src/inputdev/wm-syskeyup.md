---
title: 'WM_SYSKEYUP 訊息 (Winuser .h) '
description: 當使用者放開按住 ALT 鍵時所按下的按鍵時，以鍵盤焦點張貼至視窗。
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321799"
---
# <a name="wm_syskeyup-message"></a>WM \_ SYSKEYUP 訊息

當使用者放開按住 ALT 鍵時所按下的按鍵時，以鍵盤焦點張貼至視窗。 當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 **WM \_ SYSKEYUP** 訊息傳送至使用中視窗。 接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要釋放之金鑰的虛擬金鑰碼。 請參閱 [**虛擬金鑰代碼**](virtual-key-codes.md)。

</dd> <dt>

*lParam* 
</dt> <dd>

[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。



| Bits  | 意義                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | 目前訊息的重複計數。 值是當使用者按住按鍵時，按鍵 autorepeated 的次數。 針對 **WM \_ SYSKEYUP** 訊息，重複計數一律是一個。         |
| 16-23 | 掃描程式碼。 此值取決於 OEM。                                                                                                                                                                                  |
| 24    | 指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。 如果它是擴充索引鍵，則此值為 1;否則，它是零。                   |
| 25-28 | 保護請勿使用。                                                                                                                                                                                                         |
| 29    | 內容程式碼。 如果在釋放金鑰時，ALT 鍵已關閉，則此值為 1;如果將 **WM \_ SYSKEYUP** 訊息張貼至使用中視窗，因為沒有視窗具有鍵盤焦點，則為零。 |
| 30    | 先前的金鑰狀態。 **WM \_ SYSKEYUP** 訊息的值一律為1。                                                                                                                                                 |
| 31    | 轉換狀態。 **WM \_ SYSKEYUP** 訊息的值一律為1。                                                                                                                                                   |

如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

如果放開了 F10 鍵或 ALT 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。 訊息的 *wParam* 參數設定為 **SC \_ KEYMENU**。

當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式，它會處理它，就像是一般的索引鍵訊息，而非字元索引鍵訊息一樣。 這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。

針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。

適用于非 U. S。增強的 102-按鍵鍵盤，右邊的 ALT 鍵會以 CTRL + ALT 鍵的形式處理。 下表顯示當使用者按下並釋放此索引鍵時，所產生的訊息順序。



| 訊息                           | 虛擬金鑰碼 |
|-----------------------------------|------------------|
| [**WM \_ KEYDOWN**](wm-keydown.md) | **VK \_ 控制項**  |
| [**WM \_ KEYDOWN**](wm-keydown.md) | **VK \_ 功能表**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **VK \_ 控制項**  |
| **WM \_ SYSKEYUP**                  | **VK \_ 功能表**     |



 

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 


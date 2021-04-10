---
title: 回應滑鼠點擊
description: 回應滑鼠點擊
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092721"
---
# <a name="responding-to-mouse-clicks"></a>回應滑鼠點擊

當游標位於視窗的工作區時，如果使用者按下滑鼠按鍵，該視窗就會收到下列其中一則訊息。



| 訊息                                        | 意義                   |
|------------------------------------------------|---------------------------|
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | 向下鍵向下按鈕          |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | 左方按鈕向上鍵            |
| [**WM \_ MBUTTONDOWN**](/windows/desktop/inputdev/wm-mbuttondown) | 中間按鈕下移        |
| [**WM \_ MBUTTONUP**](/windows/desktop/inputdev/wm-mbuttonup)     | 中間按鈕向上鍵          |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown) | 向下鍵向下按鈕         |
| [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)     | 向右鍵向上鍵           |
| [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 或 XBUTTON2 向下 |
| [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 或 XBUTTON2 up   |



 

回想一下，工作區是排除框架的視窗部分。 如需有關用戶端區域的詳細資訊，請參閱 [什麼是視窗？](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>滑鼠座標

在所有這些訊息中， *lParam* 參數都包含滑鼠指標的 x 和 y 座標。 *LParam* 的最低16位包含 x 座標，後面的16個位包含 y 座標。 使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，將座標從 *LPARAM* 解壓縮。


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



這些宏會定義在標頭檔 WindowsX 中。

在64位的 Windows 上， *lParam* 是64位值。 不使用 *lParam* 的上方32位。 MSDN 檔提及 *lParam* 的「低序位單字」和「高序位單字」。 在64位的情況下，這表示較低的32位的低和高序位字組。 宏會將正確的值解壓縮，因此，如果您使用這些值，就會是安全的。

滑鼠座標以圖元為單位，而不是與裝置無關的圖元 (Dip) ，而且會相對於視窗的工作區進行測量。 座標為帶正負號的值。 在工作區左邊和左邊的位置具有負座標，如果您在視窗外追蹤滑鼠位置，這就很重要。 在稍後的主題中，我們將瞭解如何在 [視窗外捕捉滑鼠移動](mouse-movement.md)。

### <a name="additional-flags"></a>其他旗標

*WParam* 參數包含位 **or** of 旗標，表示另一個滑鼠按鍵的狀態以及 SHIFT 和 CTRL 鍵。



| 旗標             | 意義                          |
|------------------|----------------------------------|
| **MK \_ 控制項**  | CTRL 鍵已關閉。            |
| **MK \_ LBUTTON**  | 左邊的滑鼠按鍵已關閉。   |
| **MK \_ MBUTTON**  | 中間的滑鼠按鍵已關閉。 |
| **MK \_ RBUTTON**  | 滑鼠右鍵已關閉。  |
| **MK \_ 移位**    | SHIFT 鍵已關閉。           |
| **MK \_ XBUTTON1** | [XBUTTON1] 按鈕已關閉。     |
| **MK \_ XBUTTON2** | [XBUTTON2] 按鈕已關閉。     |



 

沒有旗標表示未按下對應的按鈕或按鍵。 例如，若要測試 CTRL 鍵是否已關閉：


```C++
if (wParam & MK_CONTROL) { ...
```



如果您需要尋找 CTRL 和 SHIFT 以外的其他按鍵狀態，請使用 [[鍵盤輸入](keyboard-input.md)] 中所述的 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)函數。

[**Wm \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown)和 [**wm \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)視窗訊息同時適用于 XBUTTON1 和 XBUTTON2。 *WParam* 參數指出按一下的按鈕。


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>按兩下

根據預設，視窗不會收到按兩下的通知。 若要接收按兩下，請在註冊視窗類別時，在 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構中設定 **CS \_ DBLCLKS** 旗標。


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



如果您設定 **CS \_ DBLCLKS** 旗標（如所示），此視窗將會收到按兩下通知。 按兩下會以名稱中有 "DBLCLK" 的視窗訊息表示。 例如，按兩下滑鼠左鍵會產生下列一連串的訊息：

<dl>

[**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
[**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

實際上，通常會產生的第二個 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息會變成 [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) 訊息。 對等的訊息會定義為 right、中間和 XBUTTON 按鈕。

在您看到按兩下訊息之前，無法分辨一下第一次按下滑鼠，就是按兩下開始。 因此，按兩下動作應該會繼續執行以第一次按一下滑鼠的動作。 例如，在 Windows Shell 中，只要按一下，就會選取資料夾，然後按兩下以開啟資料夾。

## <a name="non-client-mouse-messages"></a>非用戶端滑鼠訊息

系統會為視窗的非工作區中所發生的滑鼠事件定義一組個別的訊息。 這些訊息的名稱中會有字母 "NC"。 例如， [**wm \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) 與 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)的非用戶端相等。 一般的應用程式不會攔截這些訊息，因為 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會正確處理這些訊息。 不過，它們對某些 advanced 函式很有用。 例如，您可以使用這些訊息在標題列中執行自訂行為。 如果您處理這些訊息，您通常應該在之後將它們傳遞給 **DefWindowProc** 。 否則，您的應用程式將會中斷標準功能，例如拖曳或最小化視窗。

## <a name="next"></a>下一個

[滑鼠移動](mouse-movement.md)

 

 
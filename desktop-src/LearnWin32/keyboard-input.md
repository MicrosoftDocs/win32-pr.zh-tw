---
title: 使用 Win32 和 c + +) 開始的鍵盤輸入 (
description: 鍵盤輸入
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106986002"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>使用 Win32 和 c + +) 開始的鍵盤輸入 (

鍵盤用於數種不同類型的輸入，包括：

-   字元輸入。 使用者在檔或編輯方塊中輸入的文字。
-   鍵盤快速鍵。 叫用應用程式函式的按鍵筆觸;例如，CTRL + O 表示開啟檔案。
-   系統命令。 叫用系統函數的按鍵筆觸;例如，ALT + TAB 可以切換視窗。

考慮鍵盤輸入時，請務必記住，按鍵筆劃與字元不同。 例如，按下按鍵可能會產生下列任何字元。

-   a
-   A
-   × (鍵盤是否支援合併字元符號) 

此外，如果按住 ALT 鍵，則按下鍵會產生 ALT + A，而系統完全不會將它視為一個字元，而是系統命令。

## <a name="key-codes"></a>金鑰碼

當您按下按鍵時，硬體會產生 *掃描程式碼*。 掃描程式碼會依下一個鍵盤而有所不同，而且有個別的掃描碼可用於按鍵和關鍵事件。 您幾乎不會在意掃描代碼。 鍵盤驅動程式會將掃描碼轉譯為 *虛擬金鑰代碼*。 虛擬金鑰碼與裝置無關。 在任何鍵盤上按下按鍵會產生相同的虛擬按鍵程式碼。

一般而言，虛擬機器碼不會對應到 ASCII 碼或任何其他字元編碼標準。 如果您想要的話，這是很明顯的，因為相同的索引鍵可以產生不同的字元 (a、×) ，而某些按鍵（例如函式索引鍵）不會對應到任何字元。

也就是說，下列虛擬機器碼會對應到 ASCII 對等專案：

-   0到9個索引鍵 = ASCII ' 0 ' – ' 9 ' (0x30< – 0x39) 
-   A 到 Z 的按鍵 = ASCII ' A ' – ' Z ' (0x41 向– 0x5A) 

在某些方面，這個對應很不幸，因為您絕對不應該將虛擬金鑰碼視為字元，因為這是討論的原因。

標頭檔 WinUser 會定義大部分虛擬金鑰程式碼的常數。 例如，向左箭號鍵的虛擬按鍵程式碼會 **VK \_ left** (0x25) 。 如需完整的虛擬金鑰程式代碼清單，請參閱虛擬機器碼 [**程式碼**](/windows/desktop/inputdev/virtual-key-codes)。 不會針對符合 ASCII 值的虛擬金鑰碼定義常數。 例如，索引鍵的虛擬金鑰程式碼為0x41 向，但沒有名為 **VK \_ 的** 常數。 相反地，只使用數值。

## <a name="key-down-and-key-up-messages"></a>Key-Down 和 Key-Up 訊息

當您按下按鍵時，具有鍵盤焦點的視窗就會收到下列其中一則訊息。

-   [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)

[**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)訊息表示 *系統金鑰*，也就是叫用系統命令的按鍵筆觸。 系統金鑰有兩種類型：

-   ALT + 任何按鍵
-   F10

F10 鍵會啟用視窗的功能表列。 不同的 ALT 鍵組合會叫用系統命令。 例如，ALT + TAB 會切換至新的視窗。 此外，如果視窗有功能表，則可以使用 ALT 鍵來啟動功能表項目。 某些 ALT 按鍵組合不會進行任何動作。

所有其他的按鍵筆劃會被視為非系統金鑰，並產生 [**WM 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息。 這包括 F10 以外的函式索引鍵。

當您釋放金鑰時，系統會傳送對應的索引鍵訊息：

-   [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)

如果您將按鍵的時間夠長，以啟動鍵盤的重複功能，系統會傳送多個關鍵的訊息，後面接著單一的按鍵訊息。

在截至目前為止所討論的四個鍵盤訊息中， *wParam* 參數包含金鑰的虛擬按鍵碼。 *LParam* 參數包含封裝成32位的一些其他資訊。 您通常不需要 *lParam* 中的資訊。 有一個可能有用的旗標是 bit 30，也就是「先前的金鑰狀態」旗標，它會設定為1，以重複的索引鍵關閉訊息。

顧名思義，系統金鑰筆劃主要是供作業系統使用。 如果您攔截了 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) 訊息，請在之後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 。 否則，您將會封鎖作業系統來處理命令。

## <a name="character-messages"></a>字元訊息

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式會將按鍵筆劃轉換成字元，我們會先在 [課程模組 1](your-first-windows-program.md)中看到此功能。 此函式會檢查索引鍵下的訊息，並將其轉譯為字元。 **TranslateMessage** 函式會針對每個產生的字元，將 [**Wm \_ CHAR**](/windows/desktop/inputdev/wm-char)或 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)訊息放在視窗的訊息佇列上。 訊息的 *wParam* 參數包含 utf-16 字元。

您可能會猜到，wm 的 [**\_ CHAR**](/windows/desktop/inputdev/wm-char) 訊息是從 [**wm 的 \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息產生，而 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) 訊息是從 [**wm \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) 訊息產生的。 例如，假設使用者按下 SHIFT 鍵，然後按下鍵。 假設有標準鍵盤佈局，您會收到下列一連串的訊息：

**WM \_KEYDOWN**： SHIFT  
**WM \_KEYDOWN**： A  
**WM \_CHAR**： ' A '  


另一方面，ALT + P 的組合會產生：

 **WM \_SYSKEYDOWN**： VK \_ 功能表  
**WM \_SYSKEYDOWN**：0x50  
**WM \_SYSCHAR**： ' p '  
**WM \_SYSKEYUP**：0x50  
**WM \_KEYUP**： VK \_ 功能表  


基於歷史原因， (ALT 鍵的虛擬按鍵程式碼名稱為 VK \_ 功能表。 ) 

[**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)訊息表示系統字元。 如同使用 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)，您通常應該將此訊息直接傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。 否則，您可能會干擾標準系統命令。 尤其是，請勿將 **WM \_ SYSCHAR** 視為使用者所輸入的文字。

您通常會將 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息視為字元輸入。 字元的資料類型為 **wchar \_ t**，代表 utf-16 Unicode 字元。 字元輸入可以包含 ASCII 範圍以外的字元，尤其是在美國以外的鍵盤配置。 您可以使用 [螢幕小鍵盤] 功能來安裝區域鍵盤，以嘗試不同的鍵盤配置。

使用者也可以使用標準鍵盤， (IME) 輸入複雜的腳本（例如日文字元），以安裝輸入方法編輯器。 例如，使用日文 IME 輸入片假名字元カ (ka) ，您可能會收到下列訊息：

**WM \_KEYDOWN**： VK \_ PROCESSKEY (IME 處理按鍵)   
**WM \_KEYUP**：0x4B  
**WM \_KEYDOWN**： VK \_ PROCESSKEY  
**WM \_KEYUP**：0x41 向  
**WM \_KEYDOWN**： VK \_ PROCESSKEY  
**WM \_CHAR**：カ  
**WM \_KEYUP**： VK \_ RETURN  


有些 CTRL 按鍵組合會轉譯成 ASCII 控制字元。 例如，CTRL + A 會轉譯成 ASCII CTRL-A (SOH) 字元 (ASCII 值 0x01) 。 針對文字輸入，您通常應該篩選出控制字元。 此外，請避免使用 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 來執行鍵盤快速鍵。 Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table. 快速鍵對應表將在下一個主題（ [快速鍵對應表](accelerator-tables.md)）中描述。

下列程式碼會在偵錯工具中顯示主要鍵盤訊息。 請嘗試使用不同的按鍵組合來播放，並查看所產生的訊息。


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a>其他鍵盤訊息

大部分的應用程式都可以安全地忽略一些其他的鍵盤訊息。

-   會針對組合索引鍵傳送 [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) 訊息，例如「變音符號」。 例如，在西班牙文語言鍵盤上，輸入輔符號 ( ' ) 後面接著 E 會產生日字元。 會為輔色字元傳送 **WM \_ DEADCHAR** 。
-   [**WM \_ 則 unichar 會**](/windows/desktop/inputdev/wm-unichar)訊息已過時。 它可讓 ANSI 程式接收 Unicode 字元輸入。
-   當 IME 將按鍵順序轉譯為字元時，會傳送 [**WM \_ ime \_**](/windows/desktop/Intl/wm-ime-char) 字元字元。 除了一般的 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息之外，還會傳送此訊息。

## <a name="keyboard-state"></a>鍵盤狀態

鍵盤訊息是由事件驅動。 也就是說，當發生有趣的問題（例如按鍵）時，您會收到訊息，而訊息會告訴您發生什麼事。 但是，您也可以藉由呼叫 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 函式，隨時測試索引鍵的狀態。

例如，請考慮您要如何偵測滑鼠左鍵按一下 + ALT 鍵的組合。 您可以藉由接聽按鍵筆劃訊息和儲存旗標來追蹤 ALT 鍵的狀態，但 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 可節省您的麻煩。 當您收到 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息時，只要呼叫 **GetKeyState** ，如下所示：


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



[**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)訊息會採用虛擬金鑰程式碼作為輸入，並傳回一組位旗標， (實際上只有兩個旗標) 。 0x8000 值包含位旗標，可測試是否目前已按下金鑰。

大部分鍵盤都有兩個 ALT 鍵：左邊和右邊。 上述範例會測試是否已按下其中一個。 您也可以使用 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 來區分 ALT、SHIFT 或 CTRL 鍵的左和右實例。 例如，下列程式碼會測試是否按下右邊的 ALT 鍵。


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



[**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)函數很有趣，因為它會報告 *虛擬* 鍵盤狀態。 此虛擬狀態是以訊息佇列的內容為基礎，當您從佇列中移除訊息時就會更新。 當您的程式處理視窗訊息時， **GetKeyState** 會在每個訊息排入佇列時，提供鍵盤的快照。 例如，如果佇列上的最後一個訊息是 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)， **GetKeyState** 就會在使用者按下滑鼠按鍵時報告鍵盤狀態。

因為 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) 是以您的訊息佇列為基礎，所以它也會忽略傳送至另一個程式的鍵盤輸入。 如果使用者切換到其他程式， **GetKeyState** 會忽略傳送至該程式的任何按鍵動作。 如果您真的想要知道鍵盤的立即實體狀態，有一個函式可用於： [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)。 但是針對大部分的 UI 程式碼，正確的函式是 **GetKeyState**。

## <a name="next"></a>下一個

[快速鍵對應表](accelerator-tables.md)

 

 

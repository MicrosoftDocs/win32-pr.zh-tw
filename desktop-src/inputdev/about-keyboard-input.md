---
title: 關於鍵盤輸入
description: 本主題討論鍵盤輸入。
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- 使用者輸入，鍵盤輸入
- 捕獲使用者輸入，鍵盤輸入
- 鍵盤輸入
- 鍵盤焦點
- 按鍵訊息
- 字元訊息
- 系統按鍵
- 非系統按鍵
- 非系統字元訊息
- 死金鑰
- 死字元訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de85794901be3fef37156bde29520039f85702b
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373196"
---
# <a name="about-keyboard-input"></a>關於鍵盤輸入

應用程式應該接受來自鍵盤以及滑鼠的使用者輸入。 應用程式會以張貼至其 windows 的訊息形式接收鍵盤輸入。

本節包含下列主題：

-   [鍵盤輸入模型](#keyboard-input-model)
-   [鍵盤焦點和啟用](#keyboard-focus-and-activation)
-   [按鍵訊息](#keystroke-messages)
    -   [系統和非系統的按鍵](#system-and-nonsystem-keystrokes)
    -   [描述的虛擬金鑰碼](#virtual-key-codes-described)
    -   [按鍵訊息旗標](#keystroke-message-flags)
-   [字元訊息](#character-messages)
    -   [非系統字元訊息](#nonsystem-character-messages)
    -   [死字元訊息](#dead-character-messages)
-   [金鑰狀態](#key-status)
-   [按鍵和字元翻譯](#keystroke-and-character-translations)
-   [支援熱鍵](#hot-key-support)
-   [流覽和其他功能的鍵盤按鍵](#keyboard-keys-for-browsing-and-other-functions)
-   [模擬輸入](#simulating-input)
-   [語言、地區設定和鍵盤配置](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>鍵盤輸入模型

系統會安裝適用于目前鍵盤的鍵盤設備磁碟機，為應用程式提供與裝置無關的鍵盤支援。 系統會使用使用者或應用程式目前選取的語言特定鍵盤配置，來提供與語言無關的鍵盤支援。 鍵盤設備磁碟機會從鍵盤接收掃描碼，並將其傳送至鍵盤配置，並將其轉譯成電子郵件，並在您的應用程式中張貼至適當的視窗。

指派給鍵盤上的每個索引鍵都是唯一值，稱為「 *掃描碼*」（鍵盤上的按鍵裝置相依識別碼）。 當使用者輸入金鑰時，鍵盤會產生兩個掃描代碼—一個是在使用者按下按鍵時，另一個是在使用者釋放金鑰時使用。

鍵盤設備磁碟機會轉譯掃描程式碼，並將 (對應) 它轉譯為 *虛擬按鍵程式碼*，這是由系統定義的裝置獨立值，用以識別金鑰的用途。 轉譯掃描碼之後，鍵盤配置會建立一則訊息，其中包含掃描碼、虛擬機器碼和其他有關按鍵的資訊，然後將訊息放在系統訊息佇列中。 系統會從系統訊息佇列中移除訊息，並將它張貼到適當執行緒的訊息佇列。 最後，執行緒的訊息迴圈會移除訊息，並將訊息傳遞至適當的視窗程式進行處理。 下圖說明鍵盤輸入模型。

![鍵盤輸入處理模型](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>鍵盤焦點和啟用

系統會將鍵盤訊息張貼至使用鍵盤焦點建立視窗之前景執行緒的訊息佇列。 *鍵盤焦點* 是視窗的暫時屬性。 系統會將鍵盤焦點（以使用者的方向）移至另一個視窗，以在顯示的所有視窗之間共用鍵盤。 具有鍵盤焦點的視窗會從建立它) 所有鍵盤訊息的執行緒訊息佇列接收 (，直到焦點變更為不同的視窗為止。

如果任何) 目前有鍵盤焦點，執行緒可以呼叫 [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) 函式來判斷哪個視窗 (。 執行緒可以呼叫 [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) 函式，將鍵盤焦點提供給其中一個視窗。 當鍵盤焦點從某個視窗變更為另一個視窗時，系統會將 [**wm \_ KILLFOCUS**](wm-killfocus.md) 訊息傳送至已失去焦點的視窗，然後將 [**wm \_ SETFOCUS**](wm-setfocus.md) 訊息傳送至已取得焦點的視窗。

鍵盤焦點的概念與使用中視窗的概念有關。 *使用中視窗* 是使用者目前正在處理的最上層視窗。 具有鍵盤焦點的視窗是使用中視窗，或是使用中視窗的子視窗。 為了協助使用者識別使用中視窗，系統會將它放在 Z 順序的頂端，並反白顯示其標題列 (如果有一個) 和框線。

使用者可以藉由按一下來啟動最上層視窗，並使用 ALT + TAB 或 ALT + ESC 鍵組合來選取它，或從工作清單中選取它。 執行緒可以使用 [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) 函數來啟動最上層視窗。 它可以使用 [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) 函式來判斷它所建立的最上層視窗是否作用中。

當停用某個視窗並啟用另一個視窗時，系統會傳送 [**WM \_ 啟動**](wm-activate.md) 訊息。 如果停用視窗， *wParam* 參數的低序位字組為零，如果正在啟用，則為非零。 當預設視窗程式收到 **WM \_ 啟動** 訊息時，它會將鍵盤焦點設定為使用中視窗。

若要防止鍵盤和滑鼠輸入事件到達應用程式，請使用 [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput)。 請注意， **BlockInput** 函數不會干擾非同步鍵盤輸入狀態資料表。 這表示在封鎖輸入時呼叫 [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) 函式，將會變更非同步鍵盤輸入狀態資料表。

## <a name="keystroke-messages"></a>按鍵訊息

按下按鍵會將 [**wm 的 \_ KEYDOWN**](wm-keydown.md) 或 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息放置在附加至具有鍵盤焦點之視窗的執行緒訊息佇列中。 釋放金鑰會導致將 [**wm 的 \_ KEYUP**](wm-keyup.md) 或 [**wm \_ SYSKEYUP**](wm-syskeyup.md) 訊息放置在佇列中。

索引鍵和索引鍵的訊息通常會成對出現，但如果使用者的金鑰夠長而無法啟動鍵盤的自動重複功能，則系統會在資料列中產生數個 [**WM 的 \_ KEYDOWN**](wm-keydown.md) 或 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息。 然後，它會在使用者釋放金鑰時產生單一 [**wm \_ KEYUP**](wm-keyup.md) 或 [**WM \_ SYSKEYUP**](wm-syskeyup.md) 訊息。

本節包含下列主題：

-   [系統和非系統的按鍵](#system-and-nonsystem-keystrokes)
-   [描述的虛擬金鑰碼](#virtual-key-codes-described)
-   [按鍵訊息旗標](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>系統和非系統的按鍵

系統會區分系統擊鍵和非系統按鍵。 系統擊鍵會產生系統擊鍵訊息、 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md) 和 [**wm \_ SYSKEYUP**](wm-syskeyup.md)。 非系統擊鍵會產生非系統的按鍵訊息、 [**wm 的 \_ KEYDOWN**](wm-keydown.md) 和 [**wm \_ KEYUP**](wm-keyup.md)。

如果您的視窗程式必須處理系統擊鍵訊息，請確定在處理訊息之後，程式會將它傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。 否則，每當視窗具有鍵盤焦點時，就會停用所有涉及 ALT 鍵的系統作業。 也就是說，使用者將無法存取視窗的功能表或系統功能表，也無法使用 ALT + ESC 或 ALT + TAB 鍵組合來啟用不同的視窗。

系統擊鍵訊息主要是供系統使用，而不是應用程式使用。 系統會使用它們來提供內建的鍵盤介面給功能表，並允許使用者控制作用中的視窗。 當使用者以 ALT 鍵組合輸入按鍵，或是當使用者輸入和沒有視窗具有鍵盤 (焦點時，例如當使用中應用程式的最小化) 時，就會產生系統擊鍵訊息。 在此情況下，訊息會張貼至附加至使用中視窗的訊息佇列。

應用程式視窗使用非系統的擊鍵訊息; [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數不會執行任何動作。 視窗程式可能會捨棄不需要的任何非系統擊鍵訊息。

### <a name="virtual-key-codes-described"></a>描述的 Virtual-Key 碼

擊鍵訊息的 **wParam** 參數包含已按下或已釋放之金鑰的虛擬機器碼。 視窗程式會根據虛擬機器碼的值來處理或忽略按鍵訊息。

一般的視窗程式只會處理它所接收之按鍵訊息的一小部分，並忽略其餘的部分。 例如，視窗程式可能只會處理 [**WM 的 \_ KEYDOWN**](wm-keydown.md) 按鍵訊息，而且只會處理包含資料指標移動索引鍵的虛擬機器碼、shift 鍵 (也稱為控制項索引鍵) 和功能鍵。 一般的視窗程式不會處理來自字元鍵的按鍵訊息。 相反地，它會使用 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 函數將訊息轉換成字元訊息。 如需 **TranslateMessage** 和字元訊息的詳細資訊，請參閱 [字元訊息](#character-messages)。

### <a name="keystroke-message-flags"></a>按鍵訊息旗標

擊鍵訊息的 **lParam** 參數包含產生訊息之按鍵的其他相關資訊。 這項資訊包括重複計數、掃描碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標，以及轉換狀態旗標。 下圖顯示這些旗標和值在 **lParam** 參數中的位置。

![按鍵訊息的 lparam 參數中，旗標和值的位置](images/csinp-02.png)

應用程式可以使用下列值來操作按鍵旗標。



| 值            | 描述                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **KF \_ ALTDOWN**  | 操作 ALT 鍵旗標，指出是否按下 ALT 鍵。     |
| **KF \_ DLGMODE**  | 操作對話方塊模式旗標，這個旗標會指出對話方塊是否為使用中狀態。 |
| **KF \_ 擴充** | 操控擴充按鍵旗標。                                                |
| **KF \_ MENUMODE** | 操作功能表模式旗標，指出功能表是否為作用中。         |
| **KF \_ 重複**   | 操作先前的金鑰狀態旗標。                                          |
| **\_向上 KF**       | 操縱轉換狀態旗標。                                            |

程式碼範例：

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>重複計數

您可以檢查 [重複計數] 來判斷擊鍵訊息是否代表一個以上的按鍵。 系統會在鍵盤產生 [**wm 的 \_ KEYDOWN**](wm-keydown.md) 或 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息時，以比應用程式可以處理它們更快的速度來遞增計數。 這種情況通常發生在使用者所需的時間夠長，以啟動鍵盤的自動重複功能時。 系統不會使用產生的索引鍵關閉訊息來填滿系統訊息佇列，而是將訊息合併成單一金鑰的下一則訊息，並遞增重複計數。 釋出金鑰無法啟動自動重複功能，因此， [**wm \_ KEYUP**](wm-keyup.md) 和 [**wm \_ SYSKEYUP**](wm-syskeyup.md) 訊息的重複計數一律設定為1。

### <a name="scan-code"></a>掃描程式碼

掃描碼是當使用者按下按鍵時，鍵盤硬體所產生的值。 它是裝置相依的值，用來識別已按下的按鍵，而不是索引鍵所代表的字元。 應用程式通常會忽略掃描程式碼。 相反地，它會使用裝置獨立的虛擬金鑰碼來解讀按鍵訊息。

### <a name="extended-key-flag"></a>Extended-Key 旗標

擴充按鍵旗標會指出擊鍵訊息是否源自增強型鍵盤上的其中一個額外的按鍵。 擴充的按鍵包含鍵盤右手邊的 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;NUM LOCK 鍵;中斷 (CTRL + PAUSE) 鍵;PRINT SCRN 鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。 如果金鑰是擴充索引鍵，則會設定擴充按鍵旗標。

如果指定，則掃描程式碼前面會加上值為 0xE0 (224) 的前置位元組。

### <a name="context-code"></a>內容程式碼

內容程式碼指出當產生按鍵訊息時，ALT 鍵是否已關閉。 如果 ALT 鍵已關閉，則程式碼為1，如果已啟動則為0。

### <a name="previous-key-state-flag"></a>上一個 Key-State 旗標

先前的索引鍵狀態旗標會指出產生按鍵訊息的索引鍵先前是否已啟動或關閉。 如果索引鍵之前已關閉，則為1，如果索引鍵先前已啟動，則為0。 您可以使用此旗標來識別鍵盤自動重複功能所產生的按鍵訊息。 此旗標會設定為1，代表自動重複功能所產生的 [**wm \_ KEYDOWN**](wm-keydown.md) 和 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md) 擊鍵訊息。 對於 [**wm 的 \_ KEYUP**](wm-keyup.md) 和 [**wm \_ SYSKEYUP**](wm-syskeyup.md) 訊息，一律會設定為1。

### <a name="transition-state-flag"></a>Transition-State 旗標

轉換狀態旗標會指出按下按鍵或釋放金鑰是否產生按鍵訊息。 針對 [**wm \_ KEYDOWN**](wm-keydown.md) 和 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息，此旗標一律設為 0; 對於 [**wm \_ KEYUP**](wm-keyup.md) 和 [**wm \_ SYSKEYUP**](wm-syskeyup.md) 訊息，此旗標一律設定為1。

## <a name="character-messages"></a>字元訊息

擊鍵訊息提供許多關於按鍵的資訊，但不提供字元碼來進行字元按鍵。 若要取出字元碼，應用程式必須在其執行緒訊息迴圈中包含 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 函數。 **TranslateMessage** 會將 [**Wm \_ KEYDOWN**](wm-keydown.md) 或 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息傳遞至鍵盤配置。 配置會檢查訊息的虛擬機器碼，如果它對應至字元索引鍵，則會提供對等的字元碼 (將 SHIFT 和 CAPS LOCK 索引鍵) 的狀態納入考慮。 然後，它會產生包含字元碼的字元訊息，並將訊息放在訊息佇列的最上方。 訊息迴圈的下一個反復專案會從佇列中移除字元訊息，然後將訊息分派至適當的視窗程式。

本節包含下列主題：

-   [非系統字元訊息](#nonsystem-character-messages)
-   [死字元訊息](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>非系統字元訊息

視窗程式可以接收下列字元訊息： [**WM \_ CHAR**](wm-char.md)、 [**WM \_ DEADCHAR**](wm-deadchar.md)、 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)、 [**wm \_ SYSDEADCHAR**](wm-sysdeadchar.md)和 [**wm \_ 則 unichar 會**](wm-unichar.md)。 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式會在處理 [**wm \_ KEYDOWN**](wm-keydown.md)訊息時產生 **wm \_ CHAR** 或 **wm \_ DEADCHAR** 訊息。 同樣地，它會在處理 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md)訊息時產生 **wm \_ SYSCHAR** 或 **WM \_ SYSDEADCHAR** 訊息。

處理鍵盤輸入的應用程式通常會忽略所有的 [**wm \_ CHAR**](wm-char.md) 和 [**WM \_ 則 unichar 會**](wm-unichar.md) 訊息，而將任何其他訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。 請注意，當 **wm \_ 則 unichar 會** 使用 32 Utf-16 時， **wm \_ CHAR** 會使用16位 Unicode 轉換格式 (utf-16) 。 系統會使用 [**wm \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) 和 [**wm \_ SYSDEADCHAR**](wm-sysdeadchar.md) 訊息來執行功能表的助憶鍵。

所有字元訊息的 **wParam** 參數都包含已按下之字元碼的字元碼。 字元碼的值取決於接收訊息之視窗的視窗類別。 如果使用 Unicode 版本的 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 函式來註冊視窗類別，系統就會提供 unicode 字元給該類別的所有視窗。 否則，系統會提供 ASCII 字元碼。 如需詳細資訊，請參閱 [Unicode 和字元集](/windows/desktop/Intl/unicode-and-character-sets)。

字元訊息的 **lParam** 參數內容，與已轉譯為產生字元訊息的索引鍵的 **lParam** 參數內容相同。 如需詳細資訊，請參閱 [按鍵訊息旗標](#keystroke-message-flags)。

### <a name="dead-character-messages"></a>Dead-Character 訊息

某些非英文鍵盤會包含不需要自行產生字元的字元索引鍵。 相反地，它們是用來將文字元號新增到後續按鍵產生的字元。 這些機碼稱為「 *死索引鍵*」。 德文鍵盤上的揚抑符號鍵是死索引鍵的範例。 若要輸入包含 "o" 的字元加上揚揚碼，德文使用者會輸入以抑揚的字元，並在後面加上 "o" 鍵。 具有鍵盤焦點的視窗會收到下列一連串的訊息：

1.  [**WM \_ KEYDOWN**](wm-keydown.md)
2.  [**WM \_ DEADCHAR**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM \_ KEYDOWN**](wm-keydown.md)
5.  [**WM \_ 字元**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)會在處理來自無作用金鑰的 [**wm \_ KEYDOWN**](wm-keydown.md)訊息時產生 [**wm \_ DEADCHAR**](wm-deadchar.md)訊息。 雖然 **WM \_ DEADCHAR** 訊息的 *wParam* 參數包含死碼之變音符號的字元碼，但應用程式通常會忽略該訊息。 相反地，它會處理後續擊鍵所產生的 [**WM \_ 字元**](wm-char.md) 訊息。 **WM \_ 字元** 訊息的 *wParam* 參數包含字母的字元碼加上變音符號。 如果後續的按鍵產生的字元無法與文字元號結合，系統就會產生兩個 **WM \_ 字元** 訊息。 第一個的 *wParam* 參數包含變音符號的字元碼;第二個的 *wParam* 參數包含後續字元索引鍵的字元碼。

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式會在處理來自系統失效金鑰的 [**wm \_ SYSKEYDOWN**](wm-syskeydown.md)訊息時產生 [**wm \_ SYSDEADCHAR**](wm-sysdeadchar.md)訊息 (與 ALT 鍵) 組合的無作用索引鍵。 應用程式通常會忽略 **WM \_ SYSDEADCHAR** 訊息。

## <a name="key-status"></a>金鑰狀態

處理鍵盤訊息時，應用程式可能需要判斷另一個索引鍵的狀態（除了產生目前訊息的金鑰以外）。 例如，可讓使用者按下 SHIFT + END 鍵來選取一段文字的文字處理應用程式，必須在每次從結尾按鍵收到按鍵訊息時，檢查 SHIFT 鍵的狀態。 應用程式可以使用 [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) 函式，在產生目前的訊息時，判斷虛擬機器碼的狀態。它可以使用 [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) 函式來取得虛擬機器碼的目前狀態。

鍵盤配置會維護名稱清單。 產生單一字元的索引鍵名稱與金鑰所產生的字元相同。 非字元索引鍵（例如 TAB 和 ENTER）的名稱會儲存為字元字串。 應用程式可以藉由呼叫 [**GetKeyNameText**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) 函式，從設備磁碟機取出任何索引鍵的名稱。

## <a name="keystroke-and-character-translations"></a>按鍵和字元翻譯

系統包含數個特殊用途的函式，這些函式會轉譯各種擊鍵訊息所提供的掃描碼、字元碼和虛擬金鑰代碼。 這些函數包括 [**MapVirtualKey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)、 [**ToAscii**](/windows/win32/api/winuser/nf-winuser-toascii)、 [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)和 [**VkKeyScan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)。

此外，Microsoft Rich Edit 3.0 支援 [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime)，可讓使用者使用快速鍵在十六進位和 Unicode 字元之間進行轉換。 這表示當 Microsoft Rich Edit 3.0 併入應用程式時，應用程式會繼承 HexToUnicode IME 的功能。

## <a name="hot-key-support"></a>Hot-Key 支援

快速鍵是產生 [**WM \_ 熱鍵**](wm-hotkey.md)訊息的按鍵組合，*系統會將* 訊息放線上程訊息佇列的頂端，略過佇列中的任何現有訊息。 應用程式會使用快速鍵來取得使用者的高優先順序鍵盤輸入。 例如，藉由定義包含 CTRL + C 按鍵組合的熱鍵，應用程式可以讓使用者取消冗長的作業。

若要定義快速鍵，應用程式會呼叫 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函式，並指定產生 [**WM \_ 熱鍵**](wm-hotkey.md) 訊息的按鍵組合、接收訊息的視窗控制碼，以及快速鍵的識別碼。 當使用者按下快速鍵時，會在建立視窗之執行緒的訊息佇列中放置一個 **WM 的 \_ 熱鍵** 訊息。 訊息的 *wParam* 參數包含快速鍵的識別碼。 應用程式可以定義執行緒的多個快速鍵，但是執行緒中的每個快速鍵都必須有唯一的識別碼。 應用程式終止之前，應該使用 [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) 函式來終結快速鍵。

應用程式可以使用快速鍵控制項，讓使用者可以輕鬆地選擇快速鍵。 快速鍵控制項通常是用來定義可啟動視窗的快速鍵;它們不會使用 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 和 [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) 函數。 相反地，使用快速鍵控制項的應用程式通常會傳送 [**WM \_ SETHOTKEY**](wm-sethotkey.md) 訊息來設定快速鍵。 當使用者按下快速鍵時，系統會傳送指定 SC 熱鍵的 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息 \_ 。 如需快速鍵控制項的詳細資訊，請 [參閱快速鍵控制項中的](../controls/hot-key-controls.md)「使用快速鍵控制項」。

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>流覽和其他功能的鍵盤按鍵

Windows 針對瀏覽器函式、媒體功能、應用程式啟動和電源管理的特殊按鍵，提供鍵盤的支援。 [**WM \_ APPCOMMAND**](wm-appcommand.md)支援額外的鍵盤按鍵。 此外， [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) 函式會經過修改，以支援額外的鍵盤按鍵。

元件應用程式中的子視窗不太可能會直接針對這些額外的鍵盤按鍵來執行命令。 因此，當按下其中一個索引鍵時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會將 [**WM \_ APPCOMMAND**](wm-appcommand.md) 訊息傳送至視窗。 **DefWindowProc** 也會將 **WM \_ APPCOMMAND** 訊息反升至其父視窗。 這與使用滑鼠右鍵叫用快顯功能表的方式類似，也就是 **DefWindowProc** 會在按一下滑鼠右鍵時傳送 [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) 訊息，然後將它反升到其父系。 此外，如果 **DefWindowProc** 收到最上層視窗的 **WM \_ APPCOMMAND** 訊息，它就會使用程式碼 **HSHELL \_ APPCOMMAND** 來呼叫 shell 勾點。

Windows 也支援 Microsoft 的「智慧按鈕瀏覽器」，這是具有五個按鈕的滑鼠。 這兩個額外的按鈕支援向前及向後瀏覽器導覽。 如需詳細資訊，請參閱 [XBUTTONs](about-mouse-input.md)。

## <a name="simulating-input"></a>模擬輸入

若要模擬一系列不連續的使用者輸入事件，請使用 [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) 函數。 函數會接受三個參數。 第一個參數 *cInputs*，表示將模擬的輸入事件數目。 第二個參數 *rgInputs* 是 [**輸入**](/windows/win32/api/winuser/ns-winuser-input) 結構的陣列，每個都描述輸入事件的類型以及該事件的其他資訊。 最後一個參數 *cbSize* 接受 **輸入** 結構的大小（以位元組為單位）。

[**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput)函式的運作方式是將一連串的模擬輸入事件插入裝置的輸入資料流程。 這種效果類似于重複呼叫 [**keybd \_ 事件**](/windows/win32/api/winuser/nf-winuser-keybd_event) 或 [**滑鼠 \_ 事件**](/windows/win32/api/winuser/nf-winuser-mouse_event) 函式，不同之處在于系統可確保沒有其他輸入事件與模擬的事件 intermingle。 當呼叫完成時，傳回值會指出成功播放的輸入事件數目。 如果此值為零，則會封鎖輸入。

[**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput)函數不會重設鍵盤的目前狀態。 因此，當您呼叫此函式時，如果使用者已按下任何按鍵，則可能會干擾此函式所產生的事件。 如果您擔心可能的干擾，請使用 [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) 函式檢查鍵盤的狀態，並視需要進行更正。

## <a name="languages-locales-and-keyboard-layouts"></a>語言、地區設定和鍵盤配置

*語言* 是一種自然語言，例如英文、法文和日文。 子 *語言是一* 種自然語言的變異，在特定地理區域中說出，例如英國和美國所說的英文 sublanguages。 應用程式會使用稱為 [語言識別項](/windows/desktop/Intl/language-identifiers)的值，來唯一識別語言和 sublanguages。

應用程式通常會使用 *地區* 設定來設定用來處理輸入和輸出的語言。 例如，設定鍵盤的地區設定會影響鍵盤產生的字元值。 設定顯示器或印表機的地區設定會影響顯示或列印的圖像。 應用程式會藉由載入和使用鍵盤配置來設定鍵盤的地區設定。 他們會選取支援指定地區設定的字型，來設定顯示或印表機的地區設定。

鍵盤配置不僅會指定鍵盤上按鍵的實體位置，也會決定按下這些按鍵產生的字元值。 每個版面配置都會識別目前的輸入語言，並決定哪些字元值是由哪些索引鍵和按鍵組合所產生。

每個鍵盤配置都有一個對應的控點，可識別版面配置和語言。 控制碼的低字組是語言識別項。 最大的單字是裝置控制碼，指定實體配置，或為零，表示預設實體版面配置。 使用者可以將任何輸入語言與實體版面配置建立關聯。 比方說，在法文中非常簡單的英文使用者可以將鍵盤的輸入語言設定為法文，而不需要變更鍵盤的實體配置。 這表示使用者可以使用熟悉的英文版面配置來輸入法文格式的文字。

應用程式通常不需要直接操作輸入語言。 相反地，使用者會設定語言和版面配置組合，然後在它們之間切換。 當使用者按一下標記為不同語言的文字時，應用程式會呼叫 [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) 函式，以啟動該語言的使用者預設版面配置。 如果使用者使用不在作用中清單中的語言來編輯文字，應用程式可以使用語言呼叫 [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) 函式，以取得以該語言為基礎的版面配置。

[**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout)函式會設定目前工作的輸入語言。 *Hkl* 參數可以是鍵盤配置的控制碼，也可以是零擴充的語言識別項。 您可以從 [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) 或 [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) 函數取得鍵盤配置控制碼。 **\_ 接下來的 HKL** 和 **HKL \_ 前** 幾個值也可以用來選取下一個或上一個鍵盤。

[**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)函式會抓取呼叫執行緒的作用中鍵盤配置的名稱。 如果應用程式使用 [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) 函式建立作用中配置， **GetKeyboardLayoutName** 會抓取用來建立配置的相同字串。 否則，字串就是對應至使用中配置之地區設定的主要語言識別項。 這表示函式不一定會區分具有相同主要語言的不同版面配置，因此無法傳回輸入語言的特定資訊。 不過， [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) 函式可以用來判斷輸入語言。

[**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)函式會載入鍵盤配置，並讓使用者可以使用版面配置。 應用程式可以使用 **KLF \_ 啟動** 值，讓目前線程的版面配置立即處於作用中狀態。 應用程式可以使用 **KLF \_ 重新排序** 值來重新排序版面配置，而不同時指定 **KLF \_ 啟動** 值。 在載入鍵盤配置時，應用程式應該一律使用 **KLF \_ 替代 \_ [確定]** 值，以確保選取使用者的喜好設定（如果有的話）。

若為多語系支援， [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) 函數會提供 **KLF \_ REPLACELANG** 和 **KLF \_ NOTELLSHELL** 旗標。 **KLF \_ REPLACELANG** 旗標會指示函式取代現有的鍵盤配置，而不需要變更語言。 嘗試使用相同的語言識別項來取代現有的版面配置，但未指定 **KLF \_ REPLACELANG** 是一項錯誤。 **KLF \_ NOTELLSHELL** 旗標可防止函式在新增或取代鍵盤配置時通知 shell。 這適用于將多個配置新增至連續一連串呼叫的應用程式。 此旗標應用於除了最後一個呼叫以外的所有。

[**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)函式會受到限制，因為它無法卸載系統預設的輸入語言。 這可確保使用者一律有一個配置，可使用 shell 和檔案系統所使用的相同字元集來輸入文字。

 

 

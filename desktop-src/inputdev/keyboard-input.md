---
title: '鍵盤輸入 (鍵盤和滑鼠輸入) '
description: 本節將討論系統產生鍵盤輸入的方式，以及應用程式接收和處理該輸入的方式。
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardinput.htm
keywords:
- 使用者輸入，鍵盤輸入
- 捕獲使用者輸入，鍵盤輸入
- 鍵盤輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249e42a97c0848a9935fe700a0408989cbab90abc53c9ac2da6c7ef56fbc31da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757587"
---
# <a name="keyboard-input-keyboard-and-mouse-input"></a>鍵盤輸入 (鍵盤和滑鼠輸入) 

本節說明系統如何產生鍵盤輸入，以及應用程式如何接收和處理該輸入。

### <a name="in-this-section"></a>本節內容



| 名稱                                                     | 描述                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [關於鍵盤輸入](about-keyboard-input.md)         | 討論鍵盤輸入。<br/>                              |
| [使用鍵盤輸入](using-keyboard-input.md)         | 涵蓋與鍵盤輸入相關聯的工作。 <br/> |
| [鍵盤輸入參考](keyboard-input-reference.md) | 包含 API 參考。<br/>                            |



 

### <a name="functions"></a>函式



| 名稱                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) | 將輸入地區設定識別碼 (先前稱為呼叫執行緒或目前進程的鍵盤配置控點) 。 輸入地區設定識別碼會指定地區設定以及鍵盤的實體配置。<br/>                                                                                                                                                                |
| [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput)                         | 封鎖鍵盤和滑鼠輸入事件，使其無法到達應用程式。 <br/>                                                                                                                                                                                                                                                                                                                        |
| [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)                     | 啟用或停用滑鼠和鍵盤輸入至指定的視窗或控制項。 當輸入停用時，視窗不會收到輸入，例如按下滑鼠，然後按鍵。 當輸入啟用時，視窗會接收所有輸入。<br/>                                                                                                                                                     |
| [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow)               | 抓取連接至呼叫執行緒訊息佇列之使用中視窗的視窗控制碼。 <br/>                                                                                                                                                                                                                                                                                          |
| [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate)             | 判斷在呼叫函式時，金鑰是否為啟動或關閉，以及是否在前一次呼叫 [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate)之後按下金鑰。 <br/>                                                                                                                                                                                                         |
| [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus)                             | 如果視窗附加至呼叫執行緒的訊息佇列，則抓取具有鍵盤焦點的視窗控制碼。 <br/>                                                                                                                                                                                                                                                          |
| [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)           | 抓取現用輸入地區設定識別碼 (先前稱為指定執行緒的鍵盤配置) 。 如果 *idThread* 參數為零，則會傳回作用中線程的輸入地區設定識別碼。<br/>                                                                                                                                                                           |
| [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist)   | 抓取 (先前稱為鍵盤配置控點的輸入地區設定識別碼，) 對應至系統中的一組目前的輸入地區設定。 函數會將識別碼複製到指定的緩衝區。<br/>                                                                                                                                                                             |
| [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)   | 抓取使用中輸入地區設定識別碼 (先前稱為鍵盤配置) 的名稱。 <br/>                                                                                                                                                                                                                                                                                           |
| [**GetKeyboardState**](/windows/win32/api/winuser/nf-winuser-getkeyboardstate)             | 將256虛擬機器碼的狀態複製到指定的緩衝區。 <br/>                                                                                                                                                                                                                                                                                                                        |
| [**GetKeyNameText**](/windows/win32/api/winuser/nf-winuser-getkeynametexta)                 | 抓取代表索引鍵名稱的字串。 <br/>                                                                                                                                                                                                                                                                                                                                     |
| [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate)                       | 捕獲指定虛擬機器碼的狀態。 狀態會指定在每次按下按鍵時，索引鍵是開啟、關閉或切換 () 。 <br/>                                                                                                                                                                                                                       |
| [**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)             | 捕獲最後輸入事件的時間。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled)               | 判斷指定的視窗是否啟用滑鼠和鍵盤輸入。 <br/>                                                                                                                                                                                                                                                                                                          |
| [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)         | 載入新的輸入地區設定識別碼 (先前稱為鍵盤配置) 至系統中。 一次可以載入數個輸入地區設定識別碼，但一次只能有一個使用中的處理常式。 載入多個輸入地區設定識別碼，可讓您快速切換它們。<br/>                                                                                             |
| [**MapVirtualKey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)                   | 將虛擬金鑰程式碼) 的 (對應轉譯成掃描碼或字元值，或將掃描程式碼轉譯為虛擬金鑰程式碼。 <br/> 若要指定用來轉譯指定程式碼之鍵盤配置的控制碼，請使用 [**MapVirtualKeyEx**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa) 函數。<br/>                                                                                                |
| [**MapVirtualKeyEx**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa)               | 將虛擬金鑰程式碼地圖為掃描碼或字元值，或將掃描程式碼轉譯為虛擬金鑰程式碼。 函數會使用輸入語言和輸入地區設定識別碼來轉譯程式碼。<br/>                                                                                                                                                                                 |
| [**OemKeyScan**](/windows/win32/api/winuser/nf-winuser-oemkeyscan)                         | 地圖OEMASCII 代碼0至0x0FF 進入 OEM 掃描碼和移位狀態。 此函式提供的資訊可讓程式透過模擬鍵盤輸入，將 OEM 文字傳送到另一個程式。 <br/>                                                                                                                                                                                   |
| [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)                 | 定義整個系統的快速鍵。<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput)                           | 會合成按鍵、滑鼠動作，以及按鈕的點擊。<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)               | 啟用視窗。 視窗必須附加至呼叫執行緒的訊息佇列。 <br/>                                                                                                                                                                                                                                                                                                    |
| [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)                             | 將鍵盤焦點設定至指定的視窗。 視窗必須附加至呼叫執行緒的訊息佇列。 <br/>                                                                                                                                                                                                                                                                       |
| [**SetKeyboardState**](/windows/win32/api/winuser/nf-winuser-setkeyboardstate)             | 將鍵盤按鍵狀態的256位元組陣列複製到呼叫執行緒的鍵盤輸入狀態資料表中。 這是 [**GetKeyboardState**](/windows/win32/api/winuser/nf-winuser-getkeyboardstate) 和 [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) 函數所存取的相同資料表。 對此資料表所做的變更不會影響鍵盤輸入至任何其他執行緒。 <br/>                                                                   |
| [**ToAscii**](/windows/win32/api/winuser/nf-winuser-toascii)                               | 將指定的虛擬按鍵程式碼和鍵盤狀態轉譯為對應的字元或字元。 函式會使用鍵盤配置控點所識別的輸入語言和實體鍵盤配置來轉譯程式碼。<br/> 若要指定鍵盤配置的控制碼以用來轉譯指定的程式碼，請使用 [**ToAsciiEx**](/windows/win32/api/winuser/nf-winuser-toasciiex) 函數。<br/> |
| [**ToAsciiEx**](/windows/win32/api/winuser/nf-winuser-toasciiex)                           | 將指定的虛擬按鍵程式碼和鍵盤狀態轉譯為對應的字元或字元。 函式會使用輸入地區設定識別碼所識別的輸入語言和實體鍵盤配置來轉譯程式碼。<br/>                                                                                                                                               |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)                           | 將指定的虛擬按鍵程式碼和鍵盤狀態轉譯為對應的 Unicode 字元。 <br/> 若要指定鍵盤配置的控制碼以用來轉譯指定的程式碼，請使用 [**ToUnicodeEx**](/windows/win32/api/winuser/nf-winuser-tounicodeex) 函數。<br/>                                                                                                                     |
| [**ToUnicodeEx**](/windows/win32/api/winuser/nf-winuser-tounicodeex)                       | 將指定的虛擬按鍵程式碼和鍵盤狀態轉譯為對應的 Unicode 字元。<br/>                                                                                                                                                                                                                                                                         |
| [**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)     | 卸載輸入地區設定識別碼 (先前稱為鍵盤配置) 。 <br/>                                                                                                                                                                                                                                                                                                                   |
| [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey)             | 釋放先前由呼叫執行緒註冊的熱鍵。 <br/>                                                                                                                                                                                                                                                                                                                              |
| [**VkKeyScanEx**](/windows/win32/api/winuser/nf-winuser-vkkeyscanexa)                       | 將字元轉譯成對應的虛擬按鍵程式碼和移位狀態。 函式會使用輸入地區設定識別碼所識別的輸入語言和實體鍵盤配置來轉譯字元。 <br/>                                                                                                                                                                      |



 

下列函式已過時。



| 函式                               | 描述                                                                                                                                                                                                                                                                   |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKBCodePage**](/windows/win32/api/winuser/nf-winuser-getkbcodepage) | 擷取目前的字碼頁。<br/>                                                                                                                                                                                                                                   |
| [**keybd \_ 事件**](/windows/win32/api/winuser/nf-winuser-keybd_event)    | 會合成按鍵。 系統可以使用這種合成擊鍵來產生 Wm 的 [**\_ KEYUP**](wm-keyup.md) 或 [**WM 的 \_ KEYDOWN**](wm-keydown.md) 訊息。 鍵盤驅動程式的中斷處理常式會呼叫 [**keybd \_ 事件**](/windows/win32/api/winuser/nf-winuser-keybd_event) 函數。<br/> |
| [**VkKeyScan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)         | 將字元轉譯成對應的虛擬按鍵程式碼，以及目前鍵盤的移位狀態。<br/>                                                                                                                                                             |



 

### <a name="messages"></a>訊息



| 名稱                                  | 描述                                                                                                           |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETHOTKEY**](wm-gethotkey.md) | 決定與視窗相關聯的快速鍵。 <br/>                                                          |
| [**WM \_ SETHOTKEY**](wm-sethotkey.md) | 使快速鍵與視窗產生關聯。 當使用者按下快速鍵時，系統會啟動視窗。 <br/> |



 

### <a name="notifications"></a>通知



| 名稱                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 啟用**](wm-activate.md)       | 傳送至正在啟動的視窗和停用的視窗。 如果 windows 使用相同的輸入佇列，則會以同步方式將訊息傳送至即將停用之最上層視窗的視窗程式，然後再傳送至即將啟動之最上層視窗的視窗程式。 如果 windows 使用不同的輸入佇列，則會以非同步方式傳送訊息，因此會立即啟用視窗。 <br/>                                                                                                                               |
| [**WM \_ APPCOMMAND**](wm-appcommand.md)   | 通知視窗使用者所產生的應用程式命令事件，例如，按一下 [應用程式命令] 按鈕，或在鍵盤上輸入應用程式命令鍵。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ 字元**](wm-char.md)               | 在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYDOWN**](wm-keydown.md)訊息時，以鍵盤焦點張貼至視窗。 [**WM \_ 字元**](wm-char.md)訊息包含已按下之按鍵的字元碼。 <br/>                                                                                                                                                                                                                                                                             |
| [**WM \_ DEADCHAR**](wm-deadchar.md)       | 在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYUP**](wm-keyup.md)訊息時，以鍵盤焦點張貼至視窗。 [**WM \_DEADCHAR**](wm-deadchar.md) 指定由死索引鍵產生的字元碼。 無作用索引鍵是產生字元的索引鍵，例如，與另一個字元結合以形成複合字元的母音 (雙點) 。 例如，藉由為母音字元輸入死索引鍵，然後輸入 O 鍵來產生 ( ) 的母音字元。 <br/> |
| [**WM \_ 熱鍵**](wm-hotkey.md)           | 當使用者按下 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函式所註冊的快速鍵時張貼。 訊息會放在與註冊快速鍵之執行緒相關聯的訊息佇列頂端。 <br/>                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ KEYDOWN**](wm-keydown.md)         | 當按下非系統鍵時，將鍵盤焦點張貼至視窗。 非系統機碼是未按下 ALT 鍵時所按下的按鍵。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ KEYUP**](wm-keyup.md)             | 當系統釋放非系統機碼時，以鍵盤焦點張貼至視窗。 非系統索引鍵是未按下 ALT 鍵時所按下的按鍵，或是當視窗具有鍵盤焦點時按下的鍵盤按鍵。 <br/>                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ KILLFOCUS**](wm-killfocus.md)     | 在失去鍵盤焦點之前，立即傳送至視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ SETFOCUS**](wm-setfocus.md)       | 在取得鍵盤焦點之後傳送至視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) | 當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數轉譯了 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)訊息時，會使用鍵盤焦點將其傳送至視窗。 [**WM \_SYSDEADCHAR**](wm-sysdeadchar.md) 指定系統失效金鑰的字元碼，也就是按住 ALT 鍵時按下的無作用索引鍵。 <br/>                                                                                                                                                                                                        |
| [**WM \_ SYSKEYDOWN**](wm-syskeydown.md)   | 當使用者按下 F10 (鍵時，以鍵盤焦點張貼至視窗) 或按住 ALT 鍵，然後按下另一個按鍵。 當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) 訊息傳送至使用中視窗。 接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。 <br/>                                                                             |
| [**WM \_ SYSKEYUP**](wm-syskeyup.md)       | 當使用者放開按住 ALT 鍵時所按下的按鍵時，以鍵盤焦點張貼至視窗。 當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 [**WM \_ SYSKEYUP**](wm-syskeyup.md) 訊息傳送至使用中視窗。 接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。 <br/>                                                                                                                           |
| [**WM \_ 則 UNICHAR 會**](wm-unichar.md)         | 在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYDOWN**](wm-keydown.md)訊息時，以鍵盤焦點張貼至視窗。 [**WM \_ 則 unichar 會**](wm-unichar.md)訊息包含已按下之按鍵的字元碼。<br/>                                                                                                                                                                                                                                                                        |



 

### <a name="structures"></a>結構



| 名稱                                   | 描述                                                                                                              |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**HARDWAREINPUT**](/windows/win32/api/winuser/ns-winuser-hardwareinput) | 包含鍵盤或滑鼠以外輸入裝置所產生之模擬訊息的相關資訊。 <br/>  |
| [**輸入**](/windows/win32/api/winuser/ns-winuser-input)                 | 包含用來合成輸入事件的資訊，例如擊鍵、滑鼠移動和滑鼠點擊。<br/> |
| [**KEYBDINPUT**](/windows/win32/api/winuser/ns-winuser-keybdinput)       | 包含模擬鍵盤事件的相關資訊。 <br/>                                                       |
| [**LASTINPUTINFO**](/windows/win32/api/winuser/ns-winuser-lastinputinfo) | 包含最後輸入的時間。<br/>                                                                          |
| [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)       | 包含模擬滑鼠事件的相關資訊。<br/>                                                           |



 

### <a name="constants"></a>常數



| 名稱                                           | 描述                                                                                                                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**虛擬金鑰碼**](virtual-key-codes.md) | 系統所使用的虛擬金鑰碼的符號常數名稱、十六進位值，以及滑鼠或鍵盤對應專案。 這些代碼會依數位順序列出。 <br/> |



 

 


---
title: 對話方塊程式設計考量
description: 本總覽討論一些有關對話方塊的程式設計考慮。
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows 消費者介面、視窗化
- Windows 消費者介面，對話方塊
- 視窗化，對話方塊
- 對話方塊，關於
- 對話方塊程式
- 對話方塊、程式
- WM_INITDIALOG 訊息
- WM_COMMAND 訊息
- WM_PARENTNOTIFY 訊息
- 控制項色彩訊息
- 對話方塊，訊息處理
- 對話方塊、鍵盤介面
- 對話方塊、助憶鍵
- 對話方塊，自訂
- 自訂對話方塊
- 對話方塊，設定
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 790abe7c76cdb99f86b2a90a133b15faae721e0e
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2020
ms.locfileid: "106969543"
---
# <a name="dialog-box-programming-considerations"></a>對話方塊程式設計考量

本總覽討論一些有關對話方塊的程式設計考慮。

此總覽包含下列主題。

-   [對話方塊程式](#dialog-box-procedures)
    -   [WM \_ INITDIALOG 訊息](wm-initdialog.md)
    -   [WM \_ 命令訊息](/windows/desktop/menurc/wm-command)
    -   [WM \_ PARENTNOTIFY 訊息](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [控制項色彩訊息](#control-color-messages)
    -   [對話方塊預設訊息處理](#dialog-box-default-message-processing)
-   [對話方塊鍵盤介面](#dialog-box-keyboard-interface)
    -   [WS \_ TABSTOP 樣式](/windows/desktop/winmsg/window-styles)
    -   [WS \_ 群組樣式](/windows/desktop/winmsg/window-styles)
    -   [符號](#mnemonics)
-   [對話方塊設定](#dialog-box-settings)
    -   [選項按鈕和核取方塊](#radio-buttons-and-check-boxes)
    -   [對話方塊編輯控制項](#dialog-box-edit-controls)
    -   [清單方塊、下拉式方塊和目錄清單](#list-boxes-combo-boxes-and-directory-listings)
    -   [對話方塊控制項訊息](#dialog-box-control-messages)
-   [自訂對話方塊](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>對話方塊程式

對話方塊程式類似于中的視窗程式，系統會將訊息傳送至程式，以提供要執行的資訊或執行工作。與視窗程式不同的是，對話方塊程式永遠不會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 相反地，如果處理訊息，則會傳回 **TRUE** ; 否則會傳回 **FALSE** 。

每個對話方塊程式都有下列形式：

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

程式參數的作用與視窗程式相同，且 *hwndDlg* 參數會接收對話方塊的視窗控制碼。

大部分的對話方塊程式都會處理該控制項所傳送的 [**wm \_ INITDIALOG**](wm-initdialog.md) 訊息和 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，但如果有任何其他訊息，則會進行一些處理。 如果對話方塊程式未處理訊息，則必須傳回 **FALSE** ，指示系統在內部處理訊息。 這項規則的唯一例外狀況是 **WM \_ INITDIALOG** 訊息。 對話方塊程式必須傳回 **TRUE** ，指示系統進一步處理 **WM \_ INITDIALOG** 訊息。 在任何情況下，程式都不能呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

- [WM \_ INITDIALOG 訊息](#the-wm_initdialog-message)
- [WM \_ 命令訊息](#the-wm_command-message)
- [WM \_ PARENTNOTIFY 訊息](#the-wm_parentnotify-message)
- [控制項色彩訊息](#control-color-messages)
- [對話方塊預設訊息處理](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>WM \_ INITDIALOG 訊息

系統不會將 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息傳送至對話方塊程式。 相反地，它會在建立對話方塊及其所有控制項時，但在顯示對話方塊之前，傳送 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息。 程式應該執行任何必要的初始化，以確保對話方塊顯示與工作相關聯的目前設定。 例如，當對話方塊包含可顯示目前磁片磁碟機和目錄的控制項時，此程式必須判斷目前的磁片磁碟機和目錄，並將控制項設定為該值。

此程式可以使用 [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) 和 [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)等函數來初始化控制項。 由於控制項是 windows，因此程式也可以使用視窗管理函數（例如 [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) 和 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)）來操作它們。 此程式可以使用 [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) 函式來抓取控制項的視窗控制碼。

對話方塊程式可以視需要變更任何控制項的內容、狀態和位置。 例如，在包含檔案名清單方塊和 [ **開啟** ] 按鈕的對話方塊中，程式可以停用 [ **開啟** ] 按鈕，直到使用者從清單中選取檔案為止。 在此範例中，對話方塊範本會指定 [**開啟**] 按鈕的 [**WS \_ DISABLED**](/windows/desktop/winmsg/window-styles)樣式，而且系統會在建立時自動停用按鈕。 當對話方塊程式從清單方塊收到通知訊息，指出使用者已選取檔案時，此程式會呼叫 [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) 函式來啟用 [ **開啟** ] 按鈕。

若要在對話方塊的標題列上顯示自訂圖示，您的 [**wm \_ INITDIALOG**](wm-initdialog.md) 處理常式可以將 [**WM \_ SETICON**](/windows/desktop/winmsg/wm-seticon) 訊息傳送至對話方塊。

如果應用程式使用其中一個函式 [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)、 [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)、 [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)或 [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)來建立對話方塊，則 [**WM \_ lParam**](wm-initdialog.md)訊息的 *INITDIALOG* 參數會包含傳遞至函數的額外參數。 應用程式通常會使用這個額外的參數將其他初始化資訊的指標傳遞至對話方塊程式，但對話方塊程式必須判斷參數的意義。 如果應用程式使用另一個函式來建立對話方塊，則系統會將 *lParam* 參數設定為 **Null**。

從 [**WM \_ INITDIALOG**](wm-initdialog.md) 訊息傳回之前，程式應判斷是否應該將輸入焦點設定為指定的控制項。 如果對話方塊程式傳回 **TRUE**，系統就會自動將輸入焦點設定至控制項，而控制項的視窗控制碼位於 *wParam* 參數中。 如果接收預設焦點的控制項不適當，則可以使用 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數將焦點設定為適當的控制項。 如果程式設定了輸入焦點，則必須傳回 **FALSE** ，以防止系統設定預設焦點。 接收預設輸入焦點的控制項一律是範本中所指定的第一個控制項，而該控制項是可見、未停用的，而且具有 [WS \_ TABSTOP](/windows/desktop/winmsg/window-styles) 樣式。 如果沒有這類控制項存在，系統會將預設的輸入焦點設定為範本中的第一個控制項。

### <a name="the-wm_command-message"></a>WM \_ 命令訊息

當使用者在控制項中執行動作時，控制項可以傳送 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息至對話方塊程式。 這些訊息稱為通知訊息，會通知使用者輸入，並允許它執行適當的回應。

所有預先定義的控制項（靜態控制項除外）都會針對選取的使用者動作傳送通知訊息。 例如，每當使用者按下按鈕時，按下按鈕就會傳送 [**BN \_ 點擊**](../controls/bn-clicked.md) 通知訊息。 在所有情況下， *wParam* 參數的低序位字包含控制項識別碼、 *wParam* 的高序位字包含通知碼，而 *lParam* 參數則包含控制視窗控制碼。

對話方塊程式應該會監視及處理通知訊息。 尤其是，此程式必須處理具有 IDOK 或 IDCANCEL 識別碼的訊息;這些訊息代表使用者要求關閉對話方塊。 此程式應該會使用強制回應對話方塊的 [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) 函數和非強制回應對話方塊的 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函式，來關閉對話方塊。

如果對話方塊具有功能表（例如 [**視窗]** 功能表），而且使用者按一下功能表項目，則系統也會將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息傳送至對話方塊程式。 尤其是，只要使用者在對話方塊的 [視窗] 功能表中按一下 [**關閉**]，系統就會傳送包含 *WParam* 參數的 **WM \_ 命令** 訊息，並將其設定為 **IDCANCEL** 。 此訊息與 [ **取消** ] 按鈕所傳送的通知訊息幾乎完全相同，而且應該以完全相同的方式處理。

### <a name="the-wm_parentnotify-message"></a>WM \_ PARENTNOTIFY 訊息

當使用者在指向控制項時按下滑鼠按鍵時，控制項會傳送 [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 訊息。 有些應用程式會將此訊息解讀為指示，以執行與控制項相關的動作，例如，顯示描述控制項用途的文字行。

系統也會在建立和終結視窗時傳送 [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 訊息，但不會傳送自對話方塊範本所建立的控制項。 系統會在建立控制項時指定 **WS \_ EX \_ NOPARENTNOTIFY** 樣式，以防止這些訊息。 應用程式無法覆寫這個預設行為，除非它為對話方塊建立自己的控制項。

### <a name="control-color-messages"></a>Control-Color 訊息

控制項和系統可以在希望對話方塊程式使用特定筆刷和色彩繪製控制項或其他視窗的背景時，傳送控制項色彩訊息。 當應用程式覆寫對話方塊及其控制項中使用的預設色彩時，這會很有用。 以下是已取代了 **WM \_ CTLCOLOR** 訊息的控制項色彩訊息。

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

控制項只會在繪製其本身的背景之前，將控制項色彩訊息傳送至對話方塊程式。 此訊息可讓程式指定要使用的筆刷，以及設定背景和前景色彩。 此程式會藉由傳回筆刷控點來指定筆刷。 若要設定背景和前景色彩，程式會使用 [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) 和 [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) 函式與控制項的顯示裝置內容。 控制項色彩訊息會將顯示裝置內容的控制碼傳遞給訊息的 *wParam* 參數中的程式。

如果程式未處理 [**wm \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)訊息，系統會將 [**wm \_ CTLCOLORDLG**](wm-ctlcolordlg.md)訊息傳送至對話方塊程式。 預先定義的對話方塊類別沒有類別背景筆刷，因此此訊息可讓程式定義自己的背景，而不需要包含程式碼來執行工作。

在任何情況下，當對話方塊程式未處理控制項色彩訊息時，系統會使用具有預設視窗色彩的筆刷來繪製所有控制項和視窗的背景（捲軸除外）。 應用程式可以藉由將 **色彩 \_ 視窗** 值傳遞至 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 函式，來取出預設的視窗色彩。 繪製背景時，顯示裝置內容的前景色彩會設定為預設的文字色彩 (**色彩 \_ WINDOWTEXT**) 。 如果是捲軸，系統會使用具有預設捲軸色彩 (**色彩 \_ 滾動** 條) 的筆刷。 在此情況下，顯示裝置內容的背景和前景色彩會分別設定為白色和黑色。

### <a name="dialog-box-default-message-processing"></a>對話方塊預設訊息處理

預先定義之對話方塊類別的視窗程式會執行對話方塊程式未處理之所有訊息的預設處理。 當對話方塊程式針對任何訊息傳回 **FALSE** 時，預先定義的視窗程式會檢查訊息，並執行下列預設動作：



| 訊息                                            | 預設動作                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | 您可以將此訊息傳送至對話方塊。 如果對話方塊有一個，對話方塊會傳回預設推播按鈕的控制項識別碼。否則，它會傳回零。                                                                                                                                                                                                                                                                                                                      |
| [**DM 重新 \_ 定位**](dm-reposition.md)            | 您可以將此訊息傳送至最上層對話方塊。 對話方塊會自行重新置放，使其符合桌面區域。                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | 您可以將此訊息傳送至對話方塊。 對話方塊會將預設的 [推送] 按鈕設定為 *wParam* 參數中控制項識別碼所指定的控制項。                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ 啟用**](/windows/desktop/inputdev/wm-activate)           | 將輸入焦點還原至先前儲存之控制碼所識別的控制項（如果已啟用此對話方塊）。 否則，程式會將控制碼儲存至具有輸入焦點的控制項。                                                                                                                                                                                                                                                                                               |
| [**WM \_ CHARTOITEM**](../controls/wm-chartoitem.md)         | 傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)                   | 將 [**BN \_ 按一下**](../controls/bn-clicked.md) 的通知訊息張貼至對話方塊，並將 **IDCANCEL** 指定為控制項識別碼。 如果對話方塊具有 IDCANCEL 控制項識別碼，且控制項目前已停用，則程式會產生警告，且不會張貼訊息。                                                                                                                                                                                              |
| [**WM \_ COMPAREITEM**](../controls/wm-compareitem.md)       | 傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | 使用從 [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) 訊息傳回的筆刷或預設的視窗色彩，填滿對話方塊工作區。                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | 傳回應用程式定義之對話方塊字型的控制碼。                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ INITDIALOG**](wm-initdialog.md)            | 傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | 將 [**CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) 訊息傳送至具有輸入焦點的下拉式方塊，導向控制項以隱藏其下拉式清單方塊。 此程式會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 以完成預設動作。                                                                                                                                                                                                                                      |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | 釋放配置給對話方塊中編輯控制項的全域記憶體 (適用于指定 [**ds \_ LOCALEDIT**](dialog-box-styles.md) 樣式的對話方塊) 並釋出任何應用程式定義的字型 (適用于指定 [**ds \_ SETFONT**](dialog-box-styles.md) 或 [**ds \_ SHELLFONT**](dialog-box-styles.md) 樣式) 的對話方塊。 此程式會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數來完成預設動作。 |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) | 將 [**CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) 訊息傳送至具有輸入焦點的下拉式方塊，導向控制項以隱藏其下拉式清單方塊。 此程式會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 以完成預設動作。                                                                                                                                                                                                                                      |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)            | 將輸入焦點設定至對話方塊中的下一個或上一個控制項、由 *wParam* 參數中的控制碼所識別的控制項，或設定為可見、未停用之對話方塊中的第一個控制項，而且具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式。 如果具有輸入焦點的目前視窗不是控制項，則程式會忽略此訊息。                                                                                                                  |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | 將輸入焦點設定為先前儲存的控制項視窗控制碼所識別的控制項。 如果沒有這樣的控制碼存在，程式就會將輸入焦點設定為對話方塊範本中可見、未停用的第一個控制項，而且具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式。 如果沒有這類控制項存在，程式會將輸入焦點設定為範本中的第一個控制項。                                                                                          |
| [**WM \_ SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | 如果對話方塊已隱藏，則將控制碼儲存至具有輸入焦點的控制項，然後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 以完成預設動作。                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)         | 如果對話方塊已最小化，則將控制碼儲存至具有輸入焦點的控制項，然後呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 以完成預設動作。                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ VKEYTOITEM**](../controls/wm-vkeytoitem.md)         | 傳回零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

預先定義的視窗程式會將所有其他訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，以進行預設處理。

## <a name="dialog-box-keyboard-interface"></a>對話方塊鍵盤介面

系統會為對話方塊提供特殊的鍵盤介面，以執行數個索引鍵的特殊處理。 介面會產生對應至對話方塊中特定按鈕的訊息，或將輸入焦點從一個控制項變更為另一個控制項。 以下是在此介面中使用的金鑰及其各自的動作。


| Key            | 動作                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT +*助憶鍵* | 將輸入焦點移至第一個控制項 (具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式) 在包含指定助憶鍵的靜態控制項之後。        |
| DOWN           | 將輸入焦點移至群組中的下一個控制項。                                                                                                                   |
| ENTER          | 將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息傳送至對話方塊程式。 *WParam* 參數會設定為 IDOK 或預設 push 按鈕的控制項識別碼。 |
| ESC            | 將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息傳送至對話方塊程式。 *WParam* 參數設定為 IDCANCEL。                                              |
| LEFT           | 將輸入焦點移至群組中的上一個控制項。                                                                                                               |
| *記憶*     | 將輸入焦點移至第一個控制項 (具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式) 在包含指定助憶鍵的靜態控制項之後。        |
| RIGHT          | 將輸入焦點移至群組中的下一個控制項。                                                                                                                   |
| SHIFT+TAB      | 將輸入焦點移至具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的上一個控制項。                                                                |
| TAB            | 將輸入焦點移至具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的下一個控制項。                                                                    |
| UP             | 將輸入焦點移至群組中的上一個控制項。                                                                                                               |

系統會自動提供所有強制回應對話方塊的鍵盤介面。 除非應用程式呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函式來篩選其主要訊息迴圈中的訊息，否則它不會提供非強制回應對話方塊的介面。 這表示應用程式必須在從訊息佇列中取出訊息之後，立即將訊息傳遞至 **IsDialogMessage** 。 如果訊息適用于對話方塊，而且會傳回非零值以表示訊息已經過處理，而且不得傳遞給 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 或 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函數，則函式會處理這些訊息。

由於對話方塊鍵盤介面會使用方向按鍵在對話方塊中的控制項之間移動，因此應用程式無法使用這些索引鍵來滾動任何強制回應對話方塊的內容，或呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 的任何非強制回應對話方塊。 當對話方塊有捲軸時，應用程式必須為捲軸提供替代的鍵盤介面。 請注意，當系統包含滑鼠時，可使用滑鼠介面進行滾動。

### <a name="the-ws_tabstop-style"></a>WS \_ TABSTOP 樣式

[**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles)樣式指定使用者可以藉由按下 TAB 鍵或 SHIFT + tab 鍵來移動的控制項。

當使用者按下 TAB 或 SHIFT + TAB 時，系統會先判斷這些按鍵是否由目前具有輸入焦點的控制項處理。 它會將一個 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 訊息傳送給控制項，而且如果控制項傳回 DLGC WANTTAB，系統就會將索引 \_ 鍵傳遞給控制項。 否則，系統會使用 [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) 函式來尋找可見、未停用且具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的下一個控制項。 搜尋會從目前具有輸入焦點的控制項開始，並依照控制項的建立順序進行（也就是在對話方塊範本中定義它們的順序）。 當系統找出具有必要特性的控制項時，系統會將輸入焦點移至該控制項。

如果搜尋下一個具有 [**ws \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的控制項遇到具有 **ws \_ EX \_ CONTROLPARENT** 樣式的視窗，系統會以遞迴方式搜尋視窗的子系。

應用程式也可以使用 [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) 來找出具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的控制項。 函式會抓取具有 **WS \_ TABSTOP** 樣式的下一個或上一個控制項的視窗控制碼，而不會移動輸入焦點。

### <a name="the-ws_group-style"></a>WS \_ 群組樣式

根據預設，每當使用者按下方向鍵時，系統就會將輸入焦點移至下一個或上一個控制項。 只要具有輸入焦點的目前控制項不會處理這些索引鍵，而下一個或上一個控制項不是靜態控制項，系統就會繼續將輸入焦點移到對話方塊中的所有控制項，因為使用者繼續按下方向鍵。

應用程式可以使用 [**WS \_ GROUP**](/windows/desktop/winmsg/window-styles) 樣式來修改此預設行為。 樣式會標示控制項群組的開頭。 如果群組中的控制項在使用者開始按下方向按鍵時具有輸入焦點，則焦點會保留在群組中。 一般而言，群組中的第一個控制項必須具有 **WS \_ 群組** 樣式，而且群組中的所有其他控制項都不能有這個樣式。 群組中的所有控制項都必須是連續的，也就是說，它們必須連續建立，且沒有任何仲介控制項。

當使用者按下方向鍵時，系統會先判斷具有輸入焦點的目前控制項是否處理方向按鍵。 系統會將 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 訊息傳送給控制項，如果控制項傳回 **DLGC \_ WANTARROWS** 值，就會將索引鍵傳遞給控制項。 否則，系統會使用 [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) 函數來判斷群組中的下一個控制項。

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) 會依順序 (或反向順序搜尋控制項，) 它們建立的順序。 如果使用者按下向右鍵或向下鍵，則 **GetNextDlgGroupItem** 會傳回下一個控制項（如果該控制項沒有 [**WS \_ 群組**](/windows/desktop/winmsg/window-styles) 樣式）。 否則，函式會反轉搜尋的順序，並傳回具有 **WS \_ 群組** 樣式的第一個控制項。 如果使用者按下左鍵或向上鍵，則函式會傳回前一個控制項，除非目前的控制項已經有 **WS \_ 群組** 樣式。 如果目前的控制項具有此樣式，則函式會反轉搜尋的順序、找出具有 **WS \_ 群組** 樣式的第一個控制項，並傳回緊接在定位控制項之前的控制項。

如果搜尋群組中的下一個控制項遇到 **WS \_ EX \_ CONTROLPARENT** 樣式的視窗，系統會以遞迴方式搜尋視窗的子系。

系統有下一個或上一個控制項之後，它會將 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 訊息傳送給控制項，以決定控制項類型。 系統接著會移動輸入焦點，以控制它是否不是靜態控制項。 如果控制項是自動選項按鈕，系統就會傳送 [**BM \_ CLICK**](../controls/bm-click.md) 訊息給它。 應用程式也可以使用 [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) 來尋找群組中的控制項。

一般而言，群組中的第一個控制項會結合 [**ws \_ 群組**](/windows/desktop/winmsg/window-styles) 和 [**ws \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式，讓使用者可以使用 TAB 鍵從群組移至群組。 如果群組包含選項按鈕，應用程式應該只將 **WS \_ TABSTOP** 樣式套用至群組中的第一個控制項。 當使用者在群組的控制項之間移動時，系統會自動移動樣式。 這可確保當使用者使用 TAB 鍵移至群組時，輸入焦點一律會位於最近選取的控制項上。

### <a name="mnemonics"></a>符號

助憶鍵是在按鈕的標籤或靜態控制項文字中選取的字母或數位。 當使用者按下對應于助憶鍵的按鍵，或按下此按鍵和 ALT 鍵組合時，系統就會將輸入焦點移至與助憶鍵相關聯的控制項。 助憶鍵提供快速的方法，讓使用者使用鍵盤移至指定的控制項。

應用程式會建立控制項的助憶鍵，方法是在標籤中的選取字母或數位之前插入連字號 (&) ，或將控制項的文字。 在大部分的情況下，對話方塊範本中的控制項提供的以 null 終止的字串包含連字號。 不過，應用程式可以使用 [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) 函式來取代控制項的現有標籤或文字，以隨時建立助憶鍵。 只能為每個控制項指定一個助憶鍵。 雖然建議使用，但對話方塊中的助憶鍵不需要是唯一的。

當使用者按下字母或數位鍵時，系統會先判斷具有輸入焦點的目前控制項是否處理該索引鍵。 系統會將 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 訊息傳送給控制項，如果控制項傳回 **DLGC \_ WANTALLKEYS** 或 **DLG \_ WANTMESSAGE** 值，系統就會將索引鍵傳遞給控制項。 否則，它會搜尋其助憶鍵符合指定字母或數位的控制項。 它會繼續搜尋，直到它找到控制項或檢查過所有控制項為止。 在搜尋期間，它會略過具有 [**SS \_ NOPREFIX**](../controls/static-control-styles.md) 樣式的任何靜態控制項。

如果搜尋具有相符助憶鍵的控制項遇到具有 **WS \_ EX \_ CONTROLPARENT** 樣式的視窗，系統會以遞迴方式搜尋視窗的子系。

如果系統找出靜態控制項，而且控制項並未停用，系統會將輸入焦點移至可見、未停用且具有 [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式的靜態控制項之後的第一個控制項。 如果系統找到具有相符助憶鍵的其他控制項，則會將輸入焦點移至該控制項。 如果控制項是預設的 [按下] 按鈕，系統就會將 [**BN \_ 按一下**](../controls/bn-clicked.md) 的通知訊息傳送至對話方塊程式。 如果控制項是另一種按鈕樣式，而對話方塊中沒有其他控制項具有相同的助憶鍵，則系統會將 [**BM \_ 按一下**](../controls/bm-click.md) 訊息傳送至控制項。

## <a name="dialog-box-settings"></a>對話方塊設定

對話方塊設定是對話方塊中控制項的目前選項和值。 對話方塊程式在建立對話方塊時，負責將控制項初始化為這些設定。 它也負責在終結對話方塊之前，先從控制項中取出目前的設定。 用來初始化和抓取設定的方法取決於控制項的類型。

如需詳細資訊，請參閱下列主題：

-   [選項按鈕和核取方塊](#radio-buttons-and-check-boxes)
-   [對話方塊編輯控制項](#dialog-box-edit-controls)
-   [清單方塊、下拉式方塊和目錄清單](#list-boxes-combo-boxes-and-directory-listings)
-   [對話方塊控制項訊息](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>選項按鈕和核取方塊

對話方塊使用選項按鈕和核取方塊，讓使用者從選項清單中選擇。 選項按鈕可讓使用者從互斥的選項中選擇;核取方塊可讓使用者挑選選項的組合。

對話方塊程式可以使用 [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) 函數設定或清除核取方塊，以設定核取方塊的初始狀態。 針對互斥選項按鈕群組中的選項按鈕，對話方塊程式可以使用 [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) 函式來設定適當的選項按鈕，並自動清除任何其他選項按鈕。

在對話方塊終止之前，對話方塊程式可以檢查每個選項按鈕的狀態，並使用 [**IsDlgButtonChecked**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) 函式來檢查按鈕的目前狀態。 對話方塊通常會儲存此資訊，以在下一次建立對話方塊時初始化按鈕。

### <a name="dialog-box-edit-controls"></a>對話方塊編輯控制項

許多對話方塊都有編輯控制項可讓使用者提供文字做為輸入。 當對話方塊初次開機時，大部分的對話方塊程式都會初始化編輯控制項。 例如，對話方塊程式可能會在控制項中放置建議的檔案名，讓使用者可以選取、修改或取代。 對話方塊程式可以使用 [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) 函式來設定編輯控制項中的文字，此函數會將文字從指定的緩衝區複製到編輯控制項。 當編輯控制項收到輸入焦點時，會自動選取完整的文字進行編輯。

因為編輯控制項不會自動將其文字傳回至對話方塊，所以對話方塊程式必須在結束之前取出文字。 它可以使用 [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) 函式來取出文字，此函式會將編輯控制項文字複製到緩衝區。 對話方塊程式通常會儲存此文字，稍後再將編輯控制項初始化，或將其傳遞至父視窗進行處理。

某些對話方塊使用編輯控制項，讓使用者輸入數位。 對話方塊程式可以使用 [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) 函式從編輯控制項取出數位，此函式會從編輯控制項中取出文字，然後將文字轉換成十進位值。 使用者以小數位數輸入數位。 它可以是帶正負號或不帶正負號的。 對話方塊程式可以使用 [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) 函數來顯示整數。 **SetDlgItemInt** 會將帶正負號或不帶正負號的整數轉換成十進位數的字串。

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>清單方塊、下拉式方塊和目錄清單

某些對話方塊會顯示名稱清單，使用者可以從中選取一或多個名稱。 例如，若要顯示檔案名清單，對話方塊通常會使用清單方塊和 [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) 和 [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) 函數。 **DlgDirList** 函式會自動在清單方塊中填入目前目錄中的檔案名。 **DlgDirSelect** 函式會從清單方塊中抓取選取的檔案名。 這兩個函式一起提供一個方便的方式，讓對話方塊顯示目錄清單，讓使用者可以選取檔案，而不需要輸入其名稱和位置。

對話方塊也可以使用下拉式方塊來顯示檔案名清單。 [**DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx)函式會自動將目前目錄中的檔案名填滿下拉式方塊的清單方塊部分。 [**DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx)函式會從清單方塊部分抓取選取的檔案名。

### <a name="dialog-box-control-messages"></a>對話方塊控制項訊息

許多控制項都可辨識預先定義的訊息，當控制項收到這些訊息時，會導致這些訊息執行某些動作。 例如， [**BM \_ SETCHECK**](../controls/bm-setcheck.md) 訊息會設定核取方塊中的核取方塊，而 [**EM \_ GETSEL**](../controls/em-getsel.md) 訊息會抓取目前選取之控制項文字的部分。 控制訊息提供的對話方塊程式比標準函式更大且更有彈性地存取控制項，因此通常會在對話方塊需要與使用者進行複雜互動時使用。

對話方塊程式可以傳送訊息給控制項，方法是提供控制項識別碼並使用 [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) 函式，這與 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式相同，不同之處在于它會使用控制項識別碼而非視窗控制碼來識別要接收訊息的控制項。 指定的訊息可能會要求對話程式傳送參數和訊息，而且訊息可能會有對應的傳回值。 每個控制訊息的作業和需求取決於訊息的用途以及處理它的控制項。

如需控制訊息的詳細資訊，請參閱 [Windows 控制項](../controls/window-controls.md)。

## <a name="custom-dialog-boxes"></a>自訂對話方塊

應用程式可以使用對話方塊的應用程式定義視窗類別來建立自訂對話方塊，而不使用預先定義的對話方塊類別。 應用程式通常會在對話方塊是其主視窗時使用這個方法，但是針對具有標準重迭視窗的應用程式建立強制回應和非強制回應對話方塊也很有用。

應用程式定義的視窗類別可讓應用程式定義對話方塊的視窗程式，並在將訊息傳送至對話方塊程式之前處理訊息。 它也可讓應用程式定義類別圖示、類別背景筆刷，以及對話方塊的類別功能表。 應用程式必須先註冊視窗類別，然後再嘗試建立對話方塊，而且必須提供對話方塊範本，其中包含 atom 值或視窗類別的名稱。

許多應用程式會先取得預先定義之對話方塊類別的類別資訊，然後將其傳遞至 [**GetClassInfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) 函式，並將資訊填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構，藉以建立新的對話方塊類別。 應用程式會修改結構的個別成員，例如類別名稱、筆刷和圖示，然後使用 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 函式來註冊新的類別。 如果應用程式本身填入 **WNDCLASS** 結構，則必須將 **cbWndExtra** 成員設定為 **DLGWINDOWEXTRA**，也就是系統針對每個對話方塊所需的額外位元組數目。 如果應用程式也針對每個對話方塊使用額外的位元組，它們必須超過系統所需的額外位元組。

自訂對話方塊的視窗程式具有與任何其他視窗程式相同的參數和需求。 不過，與其他視窗程式不同的是，此對話方塊的視窗程式應該呼叫 [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) 函式，而不是針對它未處理的任何訊息呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 **DefDlgProc** 會執行與預先定義之對話方塊的視窗程式相同的預設訊息處理，包括呼叫對話方塊程式。

應用程式也可以藉由子類別化預先定義之對話方塊的視窗程式來建立自訂對話方塊。 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函式可讓應用程式指定指定之視窗的視窗程式。 應用程式也可以使用 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函式嘗試子類別，但是這樣做會影響系統中的所有對話方塊，而不只是屬於應用程式的對話方塊。

建立自訂對話方塊的應用程式有時會為對話方塊提供替代的鍵盤介面。 若為非強制回應對話方塊，這可能表示應用程式不會呼叫 [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) 函式，而是會處理自訂視窗程式中的所有鍵盤輸入。 在這種情況下，應用程式可以使用 [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md) 訊息，將輸入焦點從一個控制項移至另一個控制項所需的程式碼降至最低。 此訊息傳遞至 [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)時，會將輸入焦點移至指定的控制項，並更新控制項的外觀，例如移動預設的按鈕框線或設定自動選項按鈕。

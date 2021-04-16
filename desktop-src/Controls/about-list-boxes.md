---
title: 關於清單方塊
description: 本章節描述清單方塊功能。
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463749"
---
# <a name="about-list-boxes"></a>關於清單方塊

清單方塊控制項包含一份簡單的清單，使用者通常可以從該清單中選取一或多個專案。 相較于 [清單視圖](list-view-control-reference.md) 控制項，清單方塊可提供有限的彈性。

清單方塊專案可以用文字字串、點陣圖或兩者表示。 如果清單方塊不夠大，無法一次顯示所有清單方塊專案，清單方塊會提供捲軸。 使用者會在清單方塊專案中滾動，並視需要套用或移除選取狀態。 選取清單方塊專案會變更其視覺外觀，通常是將文字和背景色彩變更為相關作業系統度量所指定的色彩。 當使用者選取或取消選取專案時，系統會將通知訊息傳送至清單方塊的父視窗。

若為 ANSI 應用程式，系統會使用 **CP \_ ACP** 字碼頁，將清單方塊中的文字轉換成 Unicode。 這可能會造成問題。 例如，在 Windows 的非 Unicode 清單方塊中，有重音的羅馬字元，日文版將會出現混亂。 若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。

本節將討論下列主題：

-   [建立清單方塊](#creating-a-list-box)
-   [清單方塊類型和樣式](#list-box-types-and-styles)
-   [清單方塊函數](#list-box-functions)
-   [清單方塊中的通知訊息](#notification-messages-from-list-boxes)
-   [傳送至清單方塊的訊息](#notification-messages-from-list-boxes)
-   [預設視窗訊息處理](#default-window-message-processing)
-   [擁有者繪製清單方塊](#owner-drawn-list-boxes)
-   [拖曳清單方塊](#drag-list-boxes)
    -   [建立拖曳清單方塊](#creating-drag-list-boxes)
    -   [拖曳清單方塊訊息](#drag-list-box-messages)
    -   [拖曳清單方塊通知碼](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>建立清單方塊

在對話方塊中建立清單方塊的最簡單方式，就是將它從 [工具箱] 中 Microsoft Visual Studio 拖曳至對話方塊資源。 若要動態建立清單方塊，或是在對話方塊以外的視窗中建立清單方塊，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**WC \_ LISTBOX**](common-control-window-classes.md) 視窗類別和適當的 [清單方塊樣式](list-box-styles.md)。

## <a name="list-box-types-and-styles"></a>清單方塊類型和樣式

清單方塊有兩種類型：單一選取 (預設) 和多重選取。 在單一選取清單方塊中，使用者一次只能選取一個專案。 在多重選取清單方塊中，使用者可以一次選取一個以上的專案。 若要建立多重選取清單方塊，請指定 [**磅 \_ MULTIPLESEL**](list-box-styles.md) 或 [**磅 \_ EXTENDEDSEL**](list-box-styles.md) 樣式。

清單方塊的外觀和操作是由 [清單方塊樣式](list-box-styles.md) 和視窗樣式所控制。 這些樣式表示清單是否經過排序、排列在多個資料行中，以及由應用程式所繪製，依此類推。 清單方塊的維度和樣式通常是在包含在應用程式資源中的對話方塊範本中定義。

> [!Note]  
> 若要搭配這些控制項使用視覺化樣式，應用程式必須包含資訊清單，而且必須在程式的開頭呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 。 如需視覺化樣式的詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="list-box-functions"></a>清單方塊函數

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)函式會將清單方塊的內容取代為符合指定準則組的磁片磁碟機、目錄和檔案的名稱。 [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa)函式會抓取由 **DlgDirList** 初始化的清單方塊中目前的選取範圍。 這些功能可以讓使用者從清單方塊中選取磁片磁碟機、目錄或檔案，而不需要輸入檔案的位置和名稱。

此外， [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) 函數會傳回指定清單方塊中每個資料行的專案數。

## <a name="notification-messages-from-list-boxes"></a>清單方塊中的通知訊息

當事件發生在清單方塊中時，清單方塊會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送通知碼至擁有者視窗的對話方塊程式。 當使用者選取、按兩下或取消清單方塊專案時，會傳送清單方塊通知碼;當清單方塊收到或失去鍵盤焦點時：當系統無法配置足夠的記憶體給清單方塊要求時。 **WM \_ 命令** 訊息包含 *wParam* 參數的低序位字組中的清單方塊識別碼，以及高序位單字中的通知碼。 *LParam* 參數包含控制項視窗控制碼。

不需要使用對話方塊程式來處理這些訊息;預設的視窗程式會進行處理。

應用程式應該監視並處理下列清單方塊通知碼。



| 通知碼                   | Description                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)       | 使用者按兩下清單方塊中的專案。                  |
| [LBN \_ ERRSPACE](lbn-errspace.md)   | 清單方塊無法配置足夠的記憶體來完成要求。 |
| [LBN \_ KILLFOCUS](lbn-killfocus.md) | 清單方塊失去鍵盤焦點。                           |
| [LBN \_ SELCANCEL](lbn-selcancel.md) | 使用者在清單方塊中取消選取專案。       |
| [LBN \_ SELCHANGE](lbn-selchange.md) | 清單方塊中的選取專案即將變更。                  |
| [LBN \_ SETFOCUS](lbn-setfocus.md)   | 清單方塊會收到鍵盤焦點。                        |



 

## <a name="messages-to-list-boxes"></a>傳送至清單方塊的訊息

對話方塊程式可將訊息傳送至清單方塊，以新增、刪除、檢查及變更清單方塊專案。 例如，對話方塊程式可能會將 [**lb \_ ADDSTRING**](lb-addstring.md) 訊息傳送至清單方塊以加入專案，並傳送 [**lb \_ GETSEL**](lb-getsel.md) 訊息來判斷是否已選取專案。 其他訊息則會設定並取得清單方塊的大小、外觀和行為的相關資訊。 例如， [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息會設定清單方塊的可滾動寬度。 對話方塊程式可以使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 或 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 函數，將任何訊息傳送至清單方塊。

清單方塊專案通常會由其 *索引* 參考，此整數代表清單方塊中專案的位置。 清單方塊中第一個專案的索引為0，第二個專案的索引為1，依此類推。

下表說明預先定義的清單方塊程式如何回應清單方塊訊息。



| 訊息                                                   | 回應                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | 將檔案插入至 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) 函式所填滿的目錄清單方塊，並抓取所插入專案的清單方塊索引。                                                                  |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | 將字串加入至清單方塊，並傳回其索引。                                                                                                                                                                               |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | 從清單方塊中移除字串，並傳回清單中剩餘的字串數目。                                                                                                                                      |
| [**LB \_ 目錄**](lb-dir.md)                                 | 將檔案名清單新增至清單方塊，並傳回所加入之最後一個檔案名的索引。                                                                                                                                       |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | 傳回清單方塊中以指定字串開頭之第一個字串的索引。                                                                                                                                       |
| [**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)         | 傳回清單方塊中等於指定之字串的字串索引。                                                                                                                                             |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | 傳回滑鼠最後選取之專案的索引。                                                                                                                                                                      |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | 傳回具有焦點矩形之專案的索引。                                                                                                                                                                      |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | 傳回清單方塊中的專案數。                                                                                                                                                                                     |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | 傳回目前選取專案的索引。                                                                                                                                                                                |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | 傳回清單方塊的可滾動寬度（以圖元為單位）。                                                                                                                                                                          |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | 傳回與指定專案相關聯的值。                                                                                                                                                                    |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | 傳回清單方塊中專案的高度（以圖元為單位）。                                                                                                                                                                         |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | 抓取指定清單方塊專案的用戶端座標。                                                                                                                                                                 |
| [**LB \_ GETLOCALE**](lb-getlocale.md)                     | 抓取清單方塊的地區設定。 高序位單字包含國家/地區代碼，而低序位字組則包含語言識別項。                                                                              |
| [**LB \_ GETSEL**](lb-getsel.md)                           | 傳回清單方塊專案的選取狀態。                                                                                                                                                                                  |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | 在多重選取清單方塊中傳回選取的專案數目。                                                                                                                                                           |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | 在多重選取清單方塊中建立所有選定專案的索引陣列，並傳回選取的專案總數。                                                                                           |
| [**LB \_ GETTEXT**](lb-gettext.md)                         | 抓取與指定專案相關聯的字串，以及字串的長度。                                                                                                                                              |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | 傳回與指定專案相關聯之字串的長度（以字元為單位）。                                                                                                                                               |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | 傳回清單方塊中第一個可見專案的索引。                                                                                                                                                                       |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | 為指定的專案數和其相關聯的字串配置記憶體。                                                                                                                                                 |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | 在清單方塊中的指定索引處插入字串。                                                                                                                                                                             |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | 抓取清單方塊中最接近指定點之專案的以零為基底的索引。                                                                                                                                            |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | 從清單方塊中移除所有專案。                                                                                                                                                                                               |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | 選取找到的第一個符合指定前置詞的字串。                                                                                                                                                               |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | 在清單方塊中選取指定的專案範圍。                                                                                                                                                                                |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | 如果範圍中第一個專案的索引小於範圍中最後一個專案的索引，則選取指定的專案範圍。 如果第一個專案的索引大於最後一個專案的索引，則取消選取範圍。 |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | 將滑鼠最後選取的專案設定為指定的專案。                                                                                                                                                                  |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | 將焦點矩形設定為指定的清單方塊專案。                                                                                                                                                                           |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | 設定清單方塊中所有資料行的寬度（以圖元為單位）。                                                                                                                                                                         |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | 設定清單方塊中的專案數。                                                                                                                                                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | 選取指定的清單方塊專案。                                                                                                                                                                                               |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | 設定清單方塊的可滾動寬度（以圖元為單位）。                                                                                                                                                                             |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | 使值與清單方塊專案產生關聯。                                                                                                                                                                                         |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | 設定清單方塊中專案或專案的高度（以圖元為單位）。                                                                                                                                                                   |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | 設定清單方塊的地區設定，並傳回先前的地區設定識別碼。                                                                                                                                                        |
| [**LB \_ SETSEL**](lb-setsel.md)                           | 在多重選取清單方塊中選取專案。                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | 將索引標籤設定為指定陣列中所指定的索引鍵。                                                                                                                                                                      |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | 滾動清單方塊，讓指定的專案位於可見範圍的最上方。                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>預設視窗訊息處理

預先定義的清單方塊視窗類別的視窗程式會針對清單方塊未處理的所有訊息執行預設處理。 當清單方塊程式針對訊息傳回 **FALSE** 時，預先定義的視窗程式會檢查訊息，並執行預設動作，如下表所示。



| 訊息                                            | 預設動作                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 字元**](/windows/desktop/inputdev/wm-char)                   | 將選取範圍移至以使用者輸入的字元開頭的第一個專案。 如果清單方塊具有 L [**BS \_ OWNERDRAW**](button-styles.md) 樣式，則不會發生任何動作。 在短時間間隔內鍵入的多個字元會視為群組，並選取以該字元系列開頭的第一個專案。<br/> |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                 | 建立空的清單方塊。                                                                                                                                                                                                                                                                                                                                               |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)               | 終結清單方塊並釋出其使用的任何資源。                                                                                                                                                                                                                                                                                                              |
|                                                    | 將訊息傳遞至對話方塊程式或父視窗進程。                                                                                                                                                                                                                                                                                                 |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)                 | 如果控制項是可見的，則會使矩形失效，讓字串可以繪製成灰色。                                                                                                                                                                                                                                                                                 |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | 清除清單方塊的背景。 如果清單方塊具有 L [**BS \_ OWNERDRAW**](button-styles.md) 樣式，則不會清除背景。                                                                                                                                                                                                                   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | 傳回 DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS，表示預設清單方塊程式會處理方向鍵和 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息。                                                                                                                                                                                                      |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | 將控制碼傳回至清單方塊的目前字型。                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ HSCROLL**](wm-hscroll.md)                  | 水準滾動清單方塊。                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | 處理虛擬機器碼以進行滾動。 虛擬機器碼是要將插入號移至其中的專案索引。 選取範圍不會變更。                                                                                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)         | 關閉並終結插入號。 將 [LBN \_ KILLFOCUS](lbn-killfocus.md) 通知碼傳送給清單方塊的擁有者。                                                                                                                                                                                                                                        |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | 追蹤清單方塊工作區中的滑鼠。 這可讓使用者在清單方塊用戶端區域之外放開滑鼠按鍵時，取消選取專案。                                                                                                                                                                                                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | 追蹤清單方塊工作區中的滑鼠。 這可讓使用者在清單方塊用戶端區域之外放開滑鼠按鍵時，取消選取專案。                                                                                                                                                                                                              |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | 追蹤清單方塊工作區中的滑鼠。 這可讓使用者在清單方塊用戶端區域之外放開滑鼠按鍵時，取消選取專案。                                                                                                                                                                                                              |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | 追蹤清單方塊工作區中的滑鼠。 這可讓使用者在清單方塊用戶端區域之外放開滑鼠按鍵時，取消選取專案。                                                                                                                                                                                                              |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                      | 使用 (DC) 的裝置內容清單方塊控制碼，執行子類別化繪製作業。                                                                                                                                                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | 開啟插入號，並將 [LBN 的 \_ SETFOCUS](lbn-setfocus.md) 通知碼傳送給清單方塊的擁有者。                                                                                                                                                                                                                                                        |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | 為清單方塊設定新的字型。                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)              | 根據 *wParam* 的值，設定或清除重繪旗標。                                                                                                                                                                                                                                                                                                           |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)                     | 將清單方塊的大小調整為整數專案數目。                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ VSCROLL**](wm-vscroll.md)                  | 垂直捲動清單方塊。                                                                                                                                                                                                                                                                                                                                         |



 

預先定義的清單方塊程式會將所有其他訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，以進行預設處理。

## <a name="owner-drawn-list-boxes"></a>Owner-Drawn 清單方塊

應用程式可以建立主控 *描繪清單方塊* ，以承擔繪製清單專案的責任。 主控描繪清單方塊的父視窗或對話方塊 (其 *擁有* 者) 需要繪製清單方塊的一部分時，才會收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 擁有者繪製清單方塊可以列出除了文字字串以外的資訊。

擁有者繪製清單方塊的擁有者必須處理 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 每當需要重新繪製清單方塊的一部分時，就會傳送此訊息。 擁有者可能需要處理其他訊息，視針對清單方塊所指定的樣式而定。

應用程式可以藉由指定 [**磅 \_ OWNERDRAWFIXED**](list-box-styles.md) 或 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式來建立主控描繪清單方塊。 如果清單方塊中的所有清單專案都有相同的高度（例如字串或圖示），則應用程式可以使用 **磅 \_ OWNERDRAWFIXED** 樣式。 如果清單專案具有不同的高度 (例如，不同大小的點陣圖) 應用程式可以使用 **磅 \_ OWNERDRAWVARIABLE** 樣式。

擁有者繪製清單方塊的擁有者可以處理 [**WM \_ MEASUREITEM**](wm-measureitem.md) 訊息，以指定清單專案的維度。 如果應用程式使用 [**磅 \_ OWNERDRAWFIXED**](list-box-styles.md) 樣式建立清單方塊，則系統只會傳送一次 **WM \_ MEASUREITEM** 訊息。 擁有者指定的維度會用於所有清單專案。 如果使用 [**磅 \_ OWNERDRAWVARIABLE**](list-box-styles.md) 樣式，系統就會針對每個新增至清單方塊的清單專案傳送 **WM \_ MEASUREITEM** 訊息。 擁有者可以在任何時間分別使用 [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md) 和 [**lb \_ SETITEMHEIGHT**](lb-setitemheight.md) 訊息來判斷或設定清單專案的高度。

如果顯示在主控描繪清單方塊中的資訊包含文字，應用程式可以藉由指定 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式來追蹤每個清單專案的文字。 具有 [**磅 \_ 排序**](list-box-styles.md) 樣式的清單方塊會根據此文字來排序。 如果清單方塊已排序，但不是 **磅 \_ HASSTRINGS** 樣式，則擁有者必須處理 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息。

在主控描繪清單方塊中，擁有者必須追蹤包含除了文字以外之資訊的清單專案。 其中一個方便的方式，就是使用 [**LB \_ SETITEMDATA**](lb-setitemdata.md) 訊息將資訊的控制碼儲存為專案資料。 若要釋放與清單方塊中的專案相關聯的資料物件，擁有者可以處理 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息。

如需主控描繪清單方塊的範例，請參閱 [如何建立 Owner-Drawn 清單方塊](create-an-owner-drawn-list-box.md)。

## <a name="drag-list-boxes"></a>拖曳清單方塊

拖曳清單方塊是一種特殊類型的清單方塊，可讓使用者將專案從某個位置拖曳至另一個位置。 應用程式可以使用拖曳清單方塊以特定順序顯示字串，並讓使用者將專案拖曳至 [位置] 來變更順序。

### <a name="creating-drag-list-boxes"></a>建立拖曳清單方塊

拖曳清單方塊具有相同的視窗樣式，並處理與標準清單方塊相同的訊息。 若要建立拖曳清單方塊，請先建立標準清單方塊，然後呼叫 [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) 函數。 若要將對話方塊中的清單方塊轉換成拖曳清單方塊，您可以在處理 WM INITDIALOG 訊息時呼叫 **MakeDragList** \_ 。

### <a name="drag-list-box-messages"></a>拖曳清單方塊訊息

拖曳清單方塊會透過將拖曳清單訊息傳送給父視窗，來通知拖曳事件的父視窗。 父視窗必須處理拖曳清單訊息。

當呼叫 [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) 函式時，拖曳清單方塊會註冊此訊息。 若要取得拖曳清單訊息 (數值) 的訊息識別碼，請呼叫 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) 函式，並指定 DRAGLISTMSGSTRING 值。

拖曳清單訊息的 *wParam* 參數是拖曳清單方塊的控制項識別碼。 *LParam* 參數是 [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的位址，其中包含拖曳事件的通知碼和其他資訊。 訊息的傳回值取決於通知。

### <a name="drag-list-box-notification-codes"></a>拖曳清單方塊通知碼

拖曳清單通知碼（由拖曳清單訊息所包含之 [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的 **uNotification** 成員識別）可以是 [ [dl \_ BEGINDRAG](dl-begindrag.md)]、[ [dl \_ 拖曳](dl-dragging.md)]、[ [dl \_ CANCELDRAG](dl-canceldrag.md)] 或 [dl 已卸載]。 [ \_](dl-dropped.md)

當游標位於清單專案，且使用者按下滑鼠左鍵時，會傳送 [DL \_ BEGINDRAG](dl-begindrag.md) 通知碼。 父視窗可以傳回 **TRUE** 來開始拖曳作業，或傳回 **FALSE** 以禁止拖曳。 如此一來，父視窗就可以針對某些清單專案進行拖曳，並為其他專案停用它。 您可以使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 函數，判斷哪個清單專案位於指定的位置。

如果正在進行拖曳，則每次移動滑鼠時，或是在未移動滑鼠時，以固定間隔傳送 [DL \_ 拖曳](dl-dragging.md) 通知碼。 父視窗應該會先使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 來判斷游標下的清單專案，然後使用 [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) 函數來繪製插入圖示。 藉由針對 **LBItemFromPt** 的 *BAutoScroll* 參數指定 **TRUE** ，如果游標位於其工作區的上方或下方，您就可以讓清單方塊以一行滾動。 您為此通知傳回的值會指定要設定拖曳清單方塊的滑鼠游標類型。

如果使用者以滑鼠右鍵按一下滑鼠右鍵，或按下 ESC 鍵，則會傳送 [DL \_ CANCELDRAG](dl-canceldrag.md) 通知碼。 如果使用者透過放開滑鼠左鍵完成拖曳作業，即使游標不在清單專案上，也會傳送 DL 已卸載的通知碼。 [ \_ ](dl-dropped.md) 拖曳清單方塊會在傳送任一通知之前，先放開滑鼠捕捉。 這兩個通知的傳回值會被忽略。 拖曳清單

 


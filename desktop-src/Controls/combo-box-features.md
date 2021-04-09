---
title: 下拉式列示方塊功能
description: 本檔討論下拉式方塊的功能。
ms.assetid: 7102beff-7f67-4e4e-a32b-9ccae1522ebd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735daf708785c8d7c18027ae13a9a9cdcf843dd6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024174"
---
# <a name="combo-box-features"></a>下拉式列示方塊功能

本檔討論下拉式方塊的功能。 如需詳細資訊，請參閱下列主題：

-   [特殊功能](#special-features)
    -   [目錄清單](#directory-lists)
    -   [與清單專案相關聯的資料](#data-associated-with-list-items)
    -   [擴充的消費者介面](#the-extended-user-interface)
    -   [提示橫幅](#cue-banners)
-   [下拉式方塊通知](#combo-box-notifications)
-   [預設下拉式方塊行為](#default-combo-box-behavior)

## <a name="special-features"></a>特殊功能

有一些特殊用途的訊息和函式，可讓應用程式在下拉式方塊中顯示目錄清單、將資料與下拉式方塊中的清單專案產生關聯，以及變更下拉式清單方塊或下拉式清單方塊的鍵盤介面。

-   [目錄清單](#directory-lists)
-   [與清單專案相關聯的資料](#data-associated-with-list-items)
-   [擴充的消費者介面](#the-extended-user-interface)
-   [提示橫幅](#cue-banners)

### <a name="directory-lists"></a>目錄清單

應用程式可以將 [**CB \_ DIR**](cb-dir.md) 訊息傳送給下拉式方塊，以將檔案或子目錄的名稱新增至下拉式方塊。 此訊息的 *wParam* 參數會指定要加入之檔案的屬性，而 *lParam* 參數則是定義檔案規格之文字字串的指標。

您可以使用 [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa) 函式來取代對話方塊中下拉式方塊的內容。 此函式會在下拉式方塊中填入符合一組指定準則的磁片磁碟機、目錄和檔案的名稱。 [**DlgDirSelectComboBoxEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectcomboboxexa)函式會抓取由 **DlgDirListComboBox** 初始化的下拉式方塊中目前的選取範圍。 這些功能可以讓使用者從下拉式方塊中選取磁片磁碟機、目錄或檔案，而不需要輸入檔案的位置和名稱。

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)和 [**DlgDirSelectComboBoxEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectcomboboxexa)函式和 [**CB \_ Dir**](cb-dir.md)訊息類似于 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)和 [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa)函數，以及搭配清單方塊使用的 [**LB \_ dir**](lb-dir.md)訊息。

### <a name="data-associated-with-list-items"></a>與清單專案相關聯的資料

應用程式可以將資料與下拉式方塊中的清單專案產生關聯。 [**Cb \_ SETITEMDATA**](cb-setitemdata.md)訊息會將 **DWORD** 值與清單專案產生關聯，而 [**cb \_ GETITEMDATA**](cb-getitemdata.md)會抓取與清單專案相關聯的值。

[ [建立擁有](using-combo-boxes.md) 者] 下拉式方塊中的範例會使用專案資料，將常數與下拉式清單方塊中的每個專案產生關聯。 這種唯一值會識別每個專案，而不受其排序的位置影響。

其他應用程式可能會使用專案資料，將控制碼或指標與清單專案產生關聯。 若是如此，當刪除清單專案時，應用程式可以處理 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息來刪除或釋放指定的物件。

### <a name="the-extended-user-interface"></a>擴充的消費者介面

下拉式方塊和下拉式清單方塊支援稱為「 *擴充使用者介面*」的替代鍵盤介面。 依預設，F4 鍵會開啟或關閉清單，而向下箭號會變更目前的選取範圍。 不過，在具有擴充使用者介面的下拉式方塊中，會停用 F4 鍵，然後按向下鍵以開啟下拉式清單。 此外，當設定擴充的 UI 時，滑鼠滾輪（通常會在清單中的專案之間滾動）沒有任何功能。

若要選取下拉式方塊的使用者介面，應用程式可以將 [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md) 訊息傳送至下拉式方塊。 *WParam* 參數的 **TRUE** 值會啟用擴充的使用者介面;**FALSE** 值會設定預設的使用者介面。 若要判斷下拉式方塊是否使用擴充的使用者介面，應用程式可以將 [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md) 訊息傳送至下拉式方塊。

### <a name="cue-banners"></a>提示橫幅

提示橫幅是編輯控制項和下拉式方塊的新功能。 提示橫幅的目的是要提供提示給使用者，以做為編輯控制項或下拉式方塊的目的。 下列螢幕擷取畫面顯示具有提示文字「搜尋」的編輯控制項。

![具有提示文字「搜尋」之編輯控制項的螢幕擷取畫面](images/cue-banner.png)

當編輯控制項沒有文字或下拉式方塊沒有選取專案時，就會顯示提示橫幅文字。 當使用者在編輯控制項中輸入文字或在下拉式方塊中選取時，提示橫幅就會消失。 根據預設，當編輯控制項或下拉式方塊收到焦點時，提示橫幅也會消失。

## <a name="combo-box-notifications"></a>下拉式方塊通知

來自下拉式方塊的訊息會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送為通知碼。 通知碼會儲存在 *wParam* 參數的最高文字中，應用程式可以處理下列下拉式方塊通知碼。



| 通知碼                         | Description                                                                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBN \_ 特寫](cbn-closeup.md)           | 表示下拉式清單方塊或下拉式清單方塊中的清單即將關閉。                                                                                   |
| [CBN \_ DBLCLK](cbn-dblclk.md)             | 指出使用者已在簡單下拉式方塊中按兩下清單專案。                                                                                               |
| [CBN \_ 下拉式清單](cbn-dropdown.md)         | 表示下拉式方塊或下拉式清單方塊中的清單即將開啟。                                                                                    |
| [CBN \_ EDITCHANGE](cbn-editchange.md)     | 指出使用者已在 [簡單] 或 [下拉式] 下拉式方塊的 [編輯] 控制項中變更文字。 此通知碼會在顯示變更的文字 *之後* 傳送。  |
| [CBN \_ EDITUPDATE](cbn-editupdate.md)     | 指出使用者已在 [簡單] 或 [下拉式] 下拉式方塊的 [編輯] 控制項中變更文字。 此通知碼會在顯示變更的文字 *之前* 傳送。 |
| [CBN \_ ERRSPACE](cbn-errspace.md)         | 指出下拉式方塊無法配置足夠的記憶體來執行要求，例如新增清單專案。                                                              |
| [CBN \_ KILLFOCUS](cbn-killfocus.md)       | 指出下拉式方塊即將遺失輸入焦點。                                                                                                              |
| [CBN \_ SELCHANGE](cbn-selchange.md)       | 指出目前的選取範圍已變更。                                                                                                                           |
| [CBN \_ SELENDCANCEL](cbn-selendcancel.md) | 指出在下拉式清單中所做的選擇（在卸載時）應該忽略。                                                                 |
| [CBN \_ SELENDOK](cbn-selendok.md)         | 表示應該接受 [選取範圍] 下拉式清單（當它被捨棄時）。                                                                       |
| [CBN \_ SETFOCUS](cbn-setfocus.md)         | 表示下拉式方塊已收到輸入焦點。                                                                                                                  |



 

## <a name="default-combo-box-behavior"></a>預設下拉式方塊行為

下表描述特別由預先定義的 COMBOBOX 類別視窗程式所處理的訊息。



| 訊息                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CB \_ ADDSTRING**](cb-addstring.md)                         | 將 [**LB \_ ADDSTRING**](lb-addstring.md) 訊息傳送至清單視窗，以新增清單專案。                                                                                                                                                                                                                                                                                        |
| [**CB \_ DELETESTRING**](cb-deletestring.md)                   | 將 [**LB \_ DELETESTRING**](lb-deletestring.md) 訊息傳送至清單視窗，以刪除清單專案。                                                                                                                                                                                                                                                                               |
| [**CB \_ 目錄**](cb-dir.md)                                     | 將符合指定屬性和路徑的檔案名加入至清單。                                                                                                                                                                                                                                                                                                          |
| [**CB \_ FINDSTRING**](cb-findstring.md)                       | 將 [**LB \_ FINDSTRING**](lb-findstring.md) 訊息傳送至清單視窗。 此訊息會傳回以指定文字開頭之第一個清單專案的索引。                                                                                                                                                                                                              |
| [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)             | 將 [**LB \_ FINDSTRING**](lb-findstring.md) 訊息傳送至清單視窗。 此訊息會傳回與指定的文字完全相符之第一個清單專案的索引。                                                                                                                                                                                                              |
| [**CB \_ GETCOUNT**](cb-getcount.md)                           | 將 [**LB \_ GETCOUNT**](lb-getcount.md) 訊息傳送至清單視窗。 它會傳回清單專案的數目。                                                                                                                                                                                                                                                                        |
| [**CB \_ GETCURSEL**](cb-getcursel.md)                         | 將 [**LB \_ GETCURSEL**](lb-getcursel.md) 訊息傳送至清單視窗。 它會傳回目前選取專案的索引（如果有的話）。                                                                                                                                                                                                                                              |
| [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) | 使用下拉式清單的螢幕座標，填滿指定的矩形結構。                                                                                                                                                                                                                                                                                             |
| [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)             | 如果下拉式清單是開啟的，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。                                                                                                                                                                                                                                                                                                       |
| [**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)             | 傳回下拉式清單中允許的最小寬度（以圖元為單位）。                                                                                                                                                                                                                                                                                                               |
| [**CB \_ GETEDITSEL**](cb-geteditsel.md)                       | 將 [**EM \_ GETSEL**](em-getsel.md) 訊息傳送至編輯控制項，它會傳回目前選取範圍的開始和結束位置。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                       |
| [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)                 | 如果下拉式方塊是下拉式方塊或下拉式清單方塊，且已設定擴充使用者介面旗標，則會傳回 **TRUE** ;否則，它會傳回 **FALSE**。                                                                                                                                                                                                                         |
| [**CB \_ GETHORIZONTALEXTENT**](cb-gethorizontalextent.md)     | 將 [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) 訊息傳送至清單視窗。 它會傳回下拉式清單的可滾動寬度（以圖元為單位）。                                                                                                                                                                                                                    |
| [**CB \_ GETITEMDATA**](cb-getitemdata.md)                     | 將 [**LB \_ GETITEMDATA**](lb-getitemdata.md) 訊息傳送至清單視窗。 它會傳回與指定清單專案相關聯的值。                                                                                                                                                                                                                                         |
| [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)                 | 將 [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md) 訊息傳送至清單視窗。 它會傳回所指定主控描繪清單專案的高度（以圖元為單位）。                                                                                                                                                                                                                         |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                         | 將 [**LB \_ GETTEXT**](lb-gettext.md) 訊息傳送至清單視窗。 它會將指定的清單文字複製到指定的緩衝區。                                                                                                                                                                                                                                                    |
| [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)                   | 將 [**LB \_ GETTEXTLEN**](lb-gettextlen.md) 訊息傳送至清單視窗。 它會傳回指定清單文字的長度（以 **TCHARs**）。                                                                                                                                                                                                                                       |
| [**CB \_ GETLOCALE**](cb-getlocale.md)                         | 將 [**LB \_ GETLOCALE**](lb-getlocale.md) 訊息傳送至清單視窗。 它會傳回清單目前的地區設定。                                                                                                                                                                                                                                                               |
| [**CB \_ GETMINVISIBLE**](cb-getminvisible.md)                 | 取得下拉式方塊下拉式清單中可見專案的最小數目。                                                                                                                                                                                                                                                                                                       |
| [**CB \_ GETTOPINDEX**](cb-gettopindex.md)                     | 將 [**LB \_ GETTOPINDEX**](lb-gettopindex.md) 訊息傳送至清單視窗。 它會傳回下拉式清單中第一個可見專案的索引。                                                                                                                                                                                                                                 |
| [**CB \_ INITSTORAGE**](cb-initstorage.md)                     | 將 [**LB \_ INITSTORAGE**](lb-initstorage.md) 訊息傳送至清單視窗。 它會針對指定的專案數和指定的位元組數，初始化專案字串的空間。                                                                                                                                                                                            |
| [**CB \_ INSERTSTRING**](cb-insertstring.md)                   | 將 [**LB \_ INSERTSTRING**](lb-insertstring.md) 訊息傳送至清單視窗。 它會在指定的位置插入清單專案。                                                                                                                                                                                                                                                   |
| [**CB \_ LIMITTEXT**](cb-limittext.md)                         | 將 [**EM \_ LIMITTEXT**](em-limittext.md) 訊息傳送至編輯控制項。 它會設定使用者可以在編輯控制項中輸入的最大字元數。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                            |
| [**CB \_ RESETCONTENT**](cb-resetcontent.md)                   | 將 [**LB \_ RESETCONTENT**](lb-resetcontent.md) 訊息傳送至清單視窗，並移除清單的內容。                                                                                                                                                                                                                                                            |
| [**CB \_ SELECTSTRING**](cb-selectstring.md)                   | 將 [**LB \_ SELECTSTRING**](lb-selectstring.md) 訊息傳送至清單視窗。 它會選取以指定文字中的字元開頭的第一個清單專案（如果有的話）。                                                                                                                                                                                                      |
| [**CB \_ SETCURSEL**](cb-setcursel.md)                         | 將 [**LB \_ SETCURSEL**](lb-setcursel.md) 訊息傳送至清單視窗，並設定目前的選取範圍。                                                                                                                                                                                                                                                                        |
| [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)             | 設定下拉式清單的允許寬度下限（以圖元為單位）。                                                                                                                                                                                                                                                                                                                  |
| [**CB \_ SETEDITSEL**](cb-seteditsel.md)                       | 將 [**EM \_ SETSEL**](em-setsel.md) 訊息傳送至編輯控制項。 它會選取指定的文字範圍。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                                                         |
| [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)                 | 設定或清除擴充的使用者介面旗標。 此旗標會變更開啟的按鍵，並關閉下拉式方塊或下拉式清單方塊中的清單。 如果下拉式方塊是簡單的下拉式方塊，則視窗程式會傳回 CB \_ ERR。                                                                                                                                               |
| [**CB \_ SETHORIZONTALEXTENT**](cb-sethorizontalextent.md)     | 將 [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) 訊息傳送至清單視窗。 它會設定下拉式清單的可滾動寬度（以圖元為單位）。                                                                                                                                                                                                                       |
| [**CB \_ SETITEMDATA**](cb-setitemdata.md)                     | 將 [**LB \_ SETITEMDATA**](lb-setitemdata.md) 訊息傳送至清單視窗。 它會將指定的值與清單專案產生關聯。                                                                                                                                                                                                                                                   |
| [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)                 | 將 [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md) 訊息傳送至清單視窗。 它會設定指定主控描繪清單專案或選取欄位的高度。                                                                                                                                                                                                                 |
| [**CB \_ SETLOCALE**](cb-setlocale.md)                         | 將 [**LB \_ SETLOCALE**](lb-setlocale.md) 訊息傳送至清單視窗，並設定清單的目前地區設定。 如果清單具有 [**CBS \_ 排序**](combo-box-styles.md) 樣式，且使用 [**CB \_ ADDSTRING**](cb-addstring.md)新增了字串，則地區設定會影響清單的排序方式。                                                                              |
| [**CB \_ SETMINVISIBLE**](cb-setminvisible.md)                 | 在下拉式方塊的下拉式清單中設定可見專案的最小數目。                                                                                                                                                                                                                                                                                                       |
| [**CB \_ SETTOPINDEX**](cb-settopindex.md)                     | 將 [**LB \_ SETTOPINDEX**](lb-settopindex.md) 訊息傳送至清單視窗。 它會滾動下拉式清單，讓指定的專案位於可見範圍的最上方。                                                                                                                                                                                                               |
| [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)                   | 顯示或隱藏下拉式清單。 此訊息不會影響簡單的下拉式方塊。                                                                                                                                                                                                                                                                                                 |
| [**WM \_ 字元**](/windows/desktop/inputdev/wm-char)                              | 處理字元輸入。 在下拉式清單方塊中，會將此訊息傳遞至清單視窗，該視窗會將選取範圍移至以指定字元開頭的第一個專案。 在 [簡單] 和 [下拉式] 下拉式方塊中，會將此訊息傳遞給編輯控制項。                                                                                                                  |
| [**WM \_ 清除**](/windows/desktop/dataxchg/wm-clear)                            | 刪除編輯選取專案。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                                                             |
| [**WM \_ 命令**](/windows/desktop/menurc/wm-command)                          | 從 [編輯控制項] 和 [清單] 視窗處理通知訊息，然後將對應的下拉式方塊通知碼傳送至父視窗。                                                                                                                                                                                                                                     |
|                                                               | 若為編輯控制項通知，視窗程式可能會更新清單視窗的目前選取範圍、插入號索引和頂端索引。 針對清單通知訊息，視窗程式可能會更新 [選取] 欄位的內容。                                                                                                                                                 |
| [**WM \_ COMPAREITEM**](wm-compareitem.md)                     | 將訊息傳遞至父視窗，讓應用程式指定兩個主控描繪清單專案的相對排序位置。 下拉式方塊視窗會從清單視窗接收此訊息。                                                                                                                                                                              |
| [**WM \_ 複製**](/windows/desktop/dataxchg/wm-copy)                              | 將編輯選項複製到剪貼簿。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                                             |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                            | 初始化下拉式方塊。                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ 剪下**](/windows/desktop/dataxchg/wm-cut)                                | 刪除編輯選取範圍，並將其放在剪貼簿上。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                              |
| [**WM \_ DELETEITEM**](wm-deleteitem.md)                       | 將訊息傳遞至父視窗，通知應用程式已刪除清單專案。 下拉式方塊視窗會從清單視窗接收此訊息。                                                                                                                                                                                                               |
| [**WM \_ DRAWITEM**](wm-drawitem.md)                           | 將訊息傳送至父視窗，讓應用程式繪製指定的清單專案。 下拉式方塊視窗會從清單視窗接收此訊息。 視窗程式也可以產生此訊息，讓應用程式繪製下拉式清單方塊的選取欄位。                                                                               |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)                            | 設定要啟用或禁止滑鼠和鍵盤輸入的狀態。                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)                    | 傳回1，表示背景已清除。                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)                    | 傳回 DLG \_ WANTCHARS 和 DLGC WANTARROWS 值的組合 \_ 。                                                                                                                                                                                                                                                                                                             |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                          | 傳回目前字型的控制碼，下拉式方塊會用它來繪製其文字。                                                                                                                                                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                          | 將選取專案欄位的內容複寫到指定的緩衝區。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。                                                                                                                                                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)              | 傳回選取範圍欄位中文字的長度（以字元為單位）。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。                                                                                                                                                                                                                                 |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)                        | 處理非字元鍵盤輸入。 在下拉式清單方塊中，此訊息會傳送到清單視窗（可能會顯示或隱藏本身），或變更其目前的選取範圍或插入號的索引。 在 [簡單] 和 [下拉式] 下拉式方塊中，會將此訊息傳遞給編輯控制項。 編輯控制項會將某些按鍵傳遞至清單視窗，例如向上和向下鍵，以及 F4 鍵。 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)                    | 視需要隱藏 [選取範圍] 欄位中的醒目提示，並關閉下拉式清單。 如果接收輸入焦點的視窗是下拉式方塊的一部分 (例如，編輯控制項) ，則會忽略此訊息。                                                                                                                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)            | 與 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)相同。                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)                | 將焦點設定在下拉式方塊中，而針對下拉式方塊和下拉式清單，則可以開啟或關閉清單。 如果開啟清單，視窗程式會藉由拖曳和放開滑鼠按鍵來捕捉滑鼠，以啟用選取。                                                                                                                                        |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)                    | 如果滑鼠開啟清單，則放開滑鼠捕捉。                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ MEASUREITEM**](wm-measureitem.md)                     | 將訊息張貼至父視窗，讓應用程式修改指定之 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) 結構的內容。 下拉式方塊視窗會從清單視窗接收此訊息。                                                                                                                                                  |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)                    | 如果滑鼠已開啟清單，且滑鼠按鍵仍處於關閉狀態，則會將訊息張貼到清單視窗。 這可讓使用者藉由將滑鼠指標拖曳至清單專案，然後放開按鈕的方式來選取專案。                                                                                                                                                          |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)                        | 配置下拉式列示方塊視窗程式所使用的內部資料結構。                                                                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)                      | 釋出配置以回應 [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate) 訊息的資源。                                                                                                                                                                                                                                                                                         |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                                 | 繪製下拉式方塊的無效區域。 如果 *wParam* 不是 **Null**，則會假設為從子類別函式傳遞 (DC) 控制碼的裝置內容。 視窗程式會使用指定的 DC，而不是呼叫 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint)。                                                                                          |
| [**WM \_ 貼上**](/windows/desktop/dataxchg/wm-paste)                            | 以剪貼簿的內容取代編輯選取專案。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                         |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)                      | 將焦點設定為編輯控制項，或在下拉式清單方塊中反轉選取欄位，並開啟清單視窗中的插入號。                                                                                                                                                                                                                                               |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                          | 將指定的字型控點儲存在內部結構中、調整選取欄位和清單的維度，以及使下拉式方塊視窗失效。 選取欄位中的文字和清單會以儲存的字型顯示。                                                                                                                                                     |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)                         | 設定或清除重繪旗標。 如果清除重繪旗標，則在重新設定旗標之前，不會重新繪製下拉式方塊。                                                                                                                                                                                                                                                           |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                          | 設定編輯控制項的內容。 在 [簡單] 和 [下拉式] 下拉式方塊中，編輯控制項會處理此訊息。 在下拉式清單方塊中，視窗程式會傳回 CB \_ ERR。                                                                                                                                                                                                  |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)                                | 視需要調整子視窗的大小。                                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)                  | 根據使用者所按下的箭號，開啟或關閉下拉式清單。                                                                                                                                                                                                                                                                                                    |



 

所有其他訊息都會傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式以進行預設處理。

 

 
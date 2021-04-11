---
title: 清單方塊
description: 本章節包含與清單方塊搭配使用之程式設計項目的相關資訊。 清單方塊是一個控制項視窗，其中包含使用者可以選擇的簡單專案清單。
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093352"
---
# <a name="list-box"></a>清單方塊

本章節包含與清單方塊搭配使用之程式設計項目的相關資訊。 清單方塊是一個控制項視窗，其中包含使用者可以選擇的簡單專案清單。 如需更複雜的清單，請改用 [清單視圖](list-view-control-reference.md) 。

### <a name="overviews"></a>概觀



| 主題                                    | 目錄                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [關於清單方塊](about-list-boxes.md) | 描述清單方塊功能。<br/>                               |
| [使用清單方塊](using-list-boxes.md) | 說明如何執行與清單方塊相關聯的工作。 <br/> |



 

### <a name="functions"></a>函式



| 主題                                    | 目錄                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | 以指定之目錄中的子目錄和檔案的名稱取代清單方塊的內容。<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | 從單一選取清單方塊抓取目前的選取範圍。<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | 在指定的拖曳清單方塊的父視窗中繪製插入圖示。 <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | 抓取指定清單方塊的相關資訊。<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | 在清單方塊中的指定點抓取專案的索引。 <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | 將指定的單一選取清單方塊變更為拖曳清單方塊。 <br/>                                         |



 

### <a name="messages"></a>訊息



| 主題                                                     | 目錄                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | 將指定的檔案名加入清單方塊，其中包含目錄清單。 <br/>                                                                                                                                                                                     |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | 將字串加入至清單方塊。 <br/>                                                                                                                                                                                                                                      |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | 刪除清單方塊中的字串。 <br/>                                                                                                                                                                                                                                   |
| [**LB \_ 目錄**](lb-dir.md)                                 | 將名稱加入清單方塊所顯示的清單中。 <br/>                                                                                                                                                                                                                   |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | 在清單方塊中尋找以指定字串開頭的第一個字串。 <br/>                                                                                                                                                                                       |
| [**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)         | 尋找完全符合指定字串的第一個清單方塊字串，不同之處在于搜尋不區分大小寫。 <br/>                                                                                                                                          |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | 取得錨定專案的索引，也就是多個選取範圍開始的專案。 <br/>                                                                                                                                                                       |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | 抓取在多重選取清單方塊中具有焦點矩形之專案的索引。 您可以或可能不會選取此專案。 <br/>                                                                                                                               |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | 取得清單方塊中的專案數。 <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | 取得單一選取清單方塊中目前選取之專案的索引（如果有的話）。 <br/>                                                                                                                                                                            |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | 取得清單方塊可水準滾動 (可滾動寬度的寬度（以圖元為單位）) 如果清單方塊具有水準捲軸。 <br/>                                                                                                                       |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | 取得與指定清單方塊專案相關聯的應用程式定義值。 <br/>                                                                                                                                                                                   |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | 取得清單方塊中專案的高度。 <br/>                                                                                                                                                                                                                           |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | 取得以清單方塊專案為範圍的矩形維度，這是清單方塊專案目前顯示在清單方塊中的範圍。 <br/>                                                                                                                                                    |
| [**LB \_ GETLISTBOXINFO**](lb-getlistboxinfo.md)           | 取得指定清單方塊中每個資料行的專案數。 <br/>                                                                                                                                                                                                      |
| [**LB \_ GETLOCALE**](lb-getlocale.md)                     | 取得清單方塊的目前地區設定。 <br/>                                                                                                                                                                                                                          |
| [**LB \_ GETSEL**](lb-getsel.md)                           | 取得專案的選取狀態。 <br/>                                                                                                                                                                                                                              |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | 取得多重選取清單方塊中選取的專案總數。 <br/>                                                                                                                                                                                         |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | 填滿具有整數陣列的緩衝區，以在多重選取清單方塊中指定選取專案的專案數目。 <br/>                                                                                                                                        |
| [**LB \_ GETTEXT**](lb-gettext.md)                         | 從清單方塊中取得字串。 <br/>                                                                                                                                                                                                                                    |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | 取得清單方塊中字串的長度。 <br/>                                                                                                                                                                                                                        |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | 取得清單方塊中第一個可見專案的索引。 <br/>                                                                                                                                                                                                           |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | 配置用來儲存清單方塊專案的記憶體。 在應用程式將大量專案加入清單方塊之前，會使用此訊息。<br/>                                                                                                                                |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | 將字串或專案資料插入清單方塊中。 與 [**lb \_ ADDSTRING**](lb-addstring.md) 訊息不同的是， [**lb \_ INSERTSTRING**](lb-insertstring.md) 訊息並不會造成具有 [**磅 \_ 排序**](list-box-styles.md) 樣式的清單進行排序。 <br/> |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | 取得最接近清單方塊中指定點之專案的以零為基底的索引。<br/>                                                                                                                                                                                   |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | 從清單方塊中移除所有專案。 <br/>                                                                                                                                                                                                                                |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | 在清單方塊中搜尋以指定字串中的字元開頭的專案。 <br/>                                                                                                                                                                            |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | 選取或取消選取多重選取清單方塊中的一或多個連續專案。 <br/>                                                                                                                                                                              |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | 選取多重選取清單方塊中的一或多個連續專案。 <br/>                                                                                                                                                                                           |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | 設定錨定專案，也就是多個選取範圍開始的專案。 多重選取範圍會橫跨錨定專案中的所有專案到插入點專案。<br/>                                                                                                        |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | 將焦點矩形設定為多重選取清單方塊中指定索引處的專案。 如果看不到專案，則會將它滾動到視野中。 <br/>                                                                                                               |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | 設定多資料行清單方塊中所有資料行的寬度（以圖元為單位）。 <br/>                                                                                                                                                                                          |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | 設定清單方塊中以 [**磅 \_ NODATA**](list-box-styles.md) 樣式建立的專案計數，而不是以 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式建立的專案計數。 <br/>                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | 視需要選取字串並將它滾動至 view。 <br/>                                                                                                                                                                                                          |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | 設定以圖元為單位的寬度（以圖元為單位），可將清單方塊水準滾動 (可滾動的寬度) 。 <br/>                                                                                                                                                               |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | 設定與清單方塊中指定之專案相關聯的值。 <br/>                                                                                                                                                                                            |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | 設定清單方塊中專案的高度（以圖元為單位）。 <br/>                                                                                                                                                                                                               |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | 設定清單方塊的目前地區設定。 <br/>                                                                                                                                                                                                                          |
| [**LB \_ SETSEL**](lb-setsel.md)                           | 選取多重選取清單方塊中的字串。 <br/>                                                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | 設定清單方塊中的定位停駐點位置。 <br/>                                                                                                                                                                                                                        |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | 確定清單方塊中的指定專案可以看見。 <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>通知



| 主題                                             | 目錄                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)                     | 通知應用程式，使用者在清單方塊中按兩下某個專案。 <br/>                                                                                                                                                                                                                                         |
| [LBN \_ ERRSPACE](lbn-errspace.md)                 | 通知應用程式清單方塊無法配置足夠的記憶體來符合特定的要求。 <br/>                                                                                                                                                                                                                     |
| [LBN \_ KILLFOCUS](lbn-killfocus.md)               | 通知應用程式清單方塊已失去鍵盤焦點。 <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ SELCANCEL](lbn-selcancel.md)               | 通知應用程式使用者已在清單方塊中取消選取。 <br/>                                                                                                                                                                                                                                         |
| [LBN \_ SELCHANGE](lbn-selchange.md)               | 通知應用程式清單方塊中的選取專案已變更。 <br/>                                                                                                                                                                                                                                                   |
| [LBN \_ SETFOCUS](lbn-setfocus.md)                 | 通知應用程式清單方塊已收到鍵盤焦點。 <br/>                                                                                                                                                                                                                                              |
| [**WM \_ CHARTOITEM**](wm-chartoitem.md)           | 由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息。 <br/>                                                                                                                                        |
| [**WM \_ CTLCOLORLISTBOX**](wm-ctlcolorlistbox.md) | 在系統繪製清單方塊之前，傳送至清單方塊的父視窗。 藉由回應此訊息，父視窗可以使用指定的顯示裝置內容控制碼，來設定清單方塊的文字和背景色彩。 <br/>                                                                              |
| [**WM \_ DELETEITEM**](wm-deleteitem.md)           | 當清單方塊或下拉式方塊終結時，或是當 [**lb \_ DELETESTRING**](lb-deletestring.md)、 [**lb \_ RESETCONTENT**](lb-resetcontent.md)、 [**CB \_ DELETESTRING**](cb-deletestring.md)或 [**CB \_ RESETCONTENT**](cb-resetcontent.md) 訊息移除專案時，傳送給清單方塊或下拉式方塊的擁有者。 <br/> |
| [**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)           | 由具有 [**磅 \_ WANTKEYBOARDINPUT**](list-box-styles.md) 樣式的清單方塊傳送給其擁有者，以回應 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息。 <br/>                                                                                                                                  |
| [DL \_ BEGINDRAG](dl-begindrag.md)                 | 通知拖曳清單方塊的父視窗，指出使用者已按下某個專案的滑鼠左鍵。 <br/>                                                                                                                                                                                                                   |
| [DL \_ CANCELDRAG](dl-canceldrag.md)               | 藉由按一下滑鼠右鍵或按下 ESC 鍵，表示使用者已取消拖曳作業。 <br/>                                                                                                                                                                                                          |
| [DL \_ 拖曳](dl-dragging.md)                   | 指出使用者在拖曳專案時移動滑鼠的信號。 <br/>                                                                                                                                                                                                                                                        |
| [DL \_ 已卸載](dl-dropped.md)                     | 透過放開滑鼠左鍵，表示使用者已完成拖曳操作。 <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>結構



| 主題                                        | 目錄                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | 包含已刪除清單方塊或下拉式方塊專案的相關資訊。<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | 包含拖曳事件的相關資訊。 [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)的指標會做為拖曳清單訊息的 *lParam* 參數傳遞。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                  | 目錄                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [清單方塊樣式](list-box-styles.md) | 描述定義清單方塊控制項的視窗樣式。 <br/> |



 

 


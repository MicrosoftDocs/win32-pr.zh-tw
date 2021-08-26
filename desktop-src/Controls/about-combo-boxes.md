---
title: 關於下拉式方塊
description: 本節討論不同類型的下拉式方塊。
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497bc6fc7e9254feb58ef95051ba1278e135ff241d3af93781f611373d2d096c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922506"
---
# <a name="about-combo-boxes"></a>關於下拉式方塊

下拉式方塊結合了編輯方塊或靜態文字和清單。

本主題包含下列各節。

-   [下拉式列示方塊類型和樣式](#combo-box-types-and-styles)
-   [下拉式方塊清單](#combo-box-list)
    -   [目前的選取範圍](#current-selection)
    -   [下拉式清單](#drop-down-lists)
    -   [清單內容](#list-contents)
-   [編輯控制項選取欄位](#edit-control-selection-fields)
-   [擁有者繪製的下拉式方塊](#owner-drawn-combo-boxes)
-   [子類別化下拉式方塊](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>下拉式列示方塊類型和樣式

下拉式方塊包含清單和選取欄位。 此清單會顯示使用者可以選取的選項，而 [選取範圍] 欄位則會顯示目前的選取專案。 如果選取欄位是編輯控制項，則使用者可以輸入清單中未提供的資訊;否則，使用者只能選取清單中的專案。

通用控制項程式庫包含三種主要的下拉式列示方塊樣式，如下表所示。



| 下拉式列示方塊類型             | 樣式常數                                                 | 描述                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 簡單                     | [**CBS \_ 簡單**](combo-box-styles.md)             | 每次都會顯示清單，並在編輯控制項中顯示選取的專案。              |
| Drop-down                  | [**CBS \_ 下拉式清單**](combo-box-styles.md)         | 當您按一下圖示時，會顯示清單，並在編輯控制項中顯示選取的專案。  |
| 下拉式清單 (下拉清單)  | [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) | 當您按一下圖示時，會顯示清單，並在靜態控制項中顯示選取的專案。 |



 

下列螢幕擷取畫面會顯示三種下拉式方塊，因為它們可能會出現在 Windows Vista 中。 在第一個螢幕擷取畫面中，使用者已在 [簡單] 下拉式方塊中選取專案。 使用者也可以在這個控制項的編輯方塊中輸入新值。 清單已在 Microsoft Visual Studio 資源編輯器中調整大小，只夠大以容納兩個專案。

![顯示簡單下拉式方塊中所選取專案的螢幕擷取畫面](images/simplecombo.png)

在第二個螢幕擷取畫面中，使用者在下拉式方塊的編輯控制項中輸入了新文字。 使用者也可以選取現有的專案。 清單方塊會展開以容納盡可能多的專案。

![顯示輸入至下拉式方塊之文字的螢幕擷取畫面](images/dropdown.png)

在第三個螢幕擷取畫面中，使用者已開啟下拉式清單下拉式方塊。 清單方塊會展開以容納盡可能多的專案。 使用者無法輸入新文字。

![顯示下拉式清單下拉式方塊中所選取專案的螢幕擷取畫面](images/droplist.png)

另外還有一些定義特定屬性的下拉式列示方塊樣式。 下拉式列示方塊樣式會定義下拉式方塊的特定屬性。 您可以結合樣式;不過，某些樣式只適用于特定的下拉式列示方塊類型。 如需下拉式列示方塊樣式的表格，請參閱 [下拉式列示方塊樣式](combo-box-styles.md)。

> [!Note]  
> 若要搭配使用視覺化樣式與下拉式方塊，應用程式必須包含資訊清單，而且必須在程式的開頭呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 。 如需視覺化樣式的詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="combo-box-list"></a>下拉式方塊清單

此清單是下拉式方塊的一部分，可顯示使用者可以選取的專案。 一般而言，應用程式會在建立下拉式方塊時，初始化清單的內容。 使用者選取的任何清單專案都是 *目前的選取* 專案。 無法選取多個專案。 在 [簡單] 和 [下拉式] 下拉式方塊中，使用者可以輸入選取欄位，而不是選取清單專案。 在這些情況下，沒有目前的選取專案，而且應用程式必須負責將專案新增至清單，並使其成為目前的選取專案（如果適合的話）。

本節將討論下列主題：

-   [目前的選取範圍](#current-selection)
-   [下拉式清單](#drop-down-lists)
-   [清單內容](#list-contents)

### <a name="current-selection"></a>目前的選取範圍

目前的選取範圍是使用者已選取的清單專案;選取的文字會出現在下拉式方塊的 [選取範圍] 欄位中。 不過，在簡單下拉式方塊或下拉式方塊的案例中，目前的選取範圍只是下拉式方塊中一種可能的使用者輸入形式。 使用者也可以在 [選取範圍] 欄位中輸入文字。

目前的選取範圍是由所選取清單專案以零為起始的索引來識別。 應用程式隨時都可以設定和取出。 當使用者變更下拉式方塊的目前選取範圍時，父視窗或對話方塊程式會收到通知。 當應用程式變更選取專案時，不會通知父視窗或對話方塊。

建立下拉式方塊時，沒有目前的選取範圍。 如果使用者已編輯選取欄位的內容，則這也適用于簡單或下拉式方塊。 若要設定目前的選取專案，應用程式會將 [**CB \_ SETCURSEL**](cb-setcursel.md) 訊息傳送至下拉式方塊。 應用程式也可以使用 [**CB \_ SELECTSTRING**](cb-selectstring.md) 訊息，將目前的選取範圍設定為其字串開頭為指定字串的清單專案。 若要判斷目前的選取專案，應用程式會將 [**CB \_ GETCURSEL**](cb-getcursel.md) 訊息傳送至下拉式方塊。 如果目前沒有選取範圍，則此訊息會傳回 CB \_ ERR。

當使用者變更下拉式方塊中目前的選取範圍時，父視窗或對話方塊程式會使用 *wParam* 參數的高序位字組中的 [CBN \_ SELCHANGE](cbn-selchange.md)通知碼來接收 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息。 使用 [**CB \_ SETCURSEL**](cb-setcursel.md) 訊息設定目前的選取範圍時，不會傳送此通知碼。

下拉式清單方塊或下拉式清單方塊會在下拉式清單關閉時，將 [CBN \_ 特寫](cbn-closeup.md) 通知程式碼傳送至父視窗或對話方塊程式。 如果使用者變更目前的選取範圍，下拉式方塊也會在下拉式清單關閉時傳送 [CBN \_ SELCHANGE](cbn-selchange.md) 通知碼。 若要在每次使用者選取清單專案時執行特定進程，您可以處理 CBN \_ SELCHANGE 或 CBN \_ 特寫通知碼。 一般來說，您會先等候 CBN \_ 特寫通知碼，再處理目前選取範圍內的變更。 如果需要大量的處理，這可能特別重要。

應用程式也可以處理 [CBN \_ SELENDOK](cbn-selendok.md) 和 [CBN \_ SELENDCANCEL](cbn-selendcancel.md) 通知碼。 \_當使用者選取清單專案時，系統會傳送 CBN SELENDOK，或選取專案然後關閉清單。 這表示使用者已完成，而且應該處理選取的專案。 CBN \_ SELENDCANCEL 會在使用者選取專案時傳送，但接著會選取另一個控制項，在下拉式清單開啟時按下 ESC 鍵，或關閉對話方塊。 這表示應該忽略使用者的選取專案。 CBN \_ SELENDOK 會在每個 [CBN \_ SELCHANGE](cbn-selchange.md) 訊息之前傳送。

在簡單的下拉式方塊中，當使用者按兩下清單專案時，系統會傳送 [CBN \_ DBLCLK](cbn-dblclk.md) 通知碼。 在下拉式清單方塊或下拉式清單中，按一下即會隱藏清單，因此不可能按兩下某個專案。

### <a name="drop-down-lists"></a>下拉式清單

某些通知和訊息只適用于包含下拉式清單的下拉式方塊。 當下拉式清單已開啟或關閉時，下拉式方塊的父視窗會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式接收通知。 如果正在開啟清單， *wParam* 的高序位字是 [CBN \_ 下拉式](cbn-dropdown.md)清單。 如果清單已關閉，則為 [CBN \_ 特寫](cbn-closeup.md)。

應用程式可以使用 [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md) 訊息開啟下拉式方塊或下拉式清單方塊的清單。 它可以使用 [**cb \_ GETDROPPEDSTATE**](cb-getdroppedstate.md) 訊息來判斷清單是否開啟，並且可以使用 [**cb \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) 訊息來判斷下拉式清單的座標。 應用程式也可以使用 [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md) 訊息來增加下拉式清單的寬度。

### <a name="list-contents"></a>清單內容

當應用程式建立下拉式方塊時，通常會藉由將一或多個專案加入至清單來初始化下拉式方塊。 之後，應用程式可以加入或刪除清單專案、重新初始化清單，或從中取出專案資訊。

應用程式會將 [**CB \_ ADDSTRING**](cb-addstring.md) 訊息傳送給下拉式方塊，以將清單專案新增至下拉式方塊。 指定的專案會加入至清單的結尾，或在排序的下拉式方塊中，根據專案的字串以正確排序的位置加入。 在未排序的下拉式方塊中，應用程式可以使用 [**CB \_ INSERTSTRING**](cb-insertstring.md) 訊息，在特定位置插入專案。 加入之後，清單專案的位置就會識別。

藉由使用 [**CB \_ FINDSTRING**](cb-findstring.md) 或 [**cb \_ FINDSTRINGEXACT**](cb-findstringexact.md) 訊息，應用程式可以決定清單專案的位置。 **CB \_FINDSTRING** 會尋找其字串開頭為指定字串的專案。 **CB \_FINDSTRINGEXACT** 會尋找其字串完全符合字串的專案。 這兩個訊息都不區分大小寫。

應用程式可以使用 [**CB \_ DELETESTRING**](cb-deletestring.md) 訊息來移除清單專案。 如果應用程式需要重新初始化下拉式方塊清單，則可以先使用 [**CB \_ RESETCONTENT**](cb-resetcontent.md) 訊息來清除其整個內容。 在下拉式方塊已經顯示之後，將多個專案加入清單中時，應用程式可以清除重繪旗標，以防止下拉式方塊在加入每個專案之後重新繪製。 如需重新繪製的詳細資訊，請參閱 [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) 訊息的說明。

若要取出與清單專案相關聯的字串，應用程式可以使用 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息。 專案的字串會複製到應用程式所指定的緩衝區。 為了確保緩衝區夠大而足以接收字串，應用程式可以先使用 [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 訊息來判斷字串的長度。 若要取得下拉式方塊中的清單專案數，應用程式可以使用 [**CB \_ GETCOUNT**](cb-getcount.md) 訊息。

## <a name="edit-control-selection-fields"></a>編輯控制項選取欄位

應用程式可以取出或設定選取欄位的內容，也可以決定或設定編輯選取範圍。 應用程式也可以限制使用者可在 [選取範圍] 欄位中輸入的文字數量。 當選取專案欄位的內容變更時，系統會將通知訊息傳送至父視窗或對話方塊程式。

若要抓取選取欄位的內容，應用程式可以將 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息傳送至下拉式方塊。 若要設定簡單或下拉式下拉式方塊的選取範圍內容，應用程式可以將 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息傳送至下拉式方塊。

編輯選取範圍是在 [簡單] 或 [下拉式] 下拉式方塊的 [選取範圍] 欄位中所選取文字的範圍（如果有的話）。 應用程式可以使用 [**CB \_ GETEDITSEL**](cb-geteditsel.md) 訊息來判斷目前選取範圍的開始和結束字元位置。 它也可以使用 [**CB \_ SETEDITSEL**](cb-seteditsel.md) 訊息選取編輯選取範圍中的字元。

一開始，使用者可以在選取欄位中輸入的文字數量受限於選取範圍欄位的大小。 但是，如果下拉式方塊具有 [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) 樣式，則文字可以繼續超出選取範圍欄位的大小。 無論控制項是否有 **CBS \_ AUTOHSCROLL** 樣式，應用程式都可以使用 [**CB \_ LIMITTEXT**](cb-limittext.md)訊息來限制使用者可在 [選取] 欄位中輸入的文字數量。

當使用者編輯選擇欄位的內容時，父視窗或對話方塊程式會收到通知訊息。 [CBN \_ EDITUPDATE](cbn-editupdate.md)通知碼會先傳送，表示已編輯選取欄位中的文字。 在變更的文字顯示之後，系統會傳送 [CBN \_ EDITCHANGE](cbn-editchange.md)。 當選取欄位內容因為選取清單專案的結果而變更時，不會傳送這些訊息。

## <a name="owner-drawn-combo-boxes"></a>Owner-Drawn 下拉式方塊

應用程式可以建立主控描繪的下拉式列示方塊，以負責繪製清單專案。 主控描繪下拉式方塊的父視窗 (其擁有者) 需要繪製下拉式方塊的一部分時，才會收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 主控描繪的下拉式列示方塊可以列出除了文字字串以外的資訊。 擁有者繪製的下拉式列示方塊可以是任何類型。 不過，在 [簡單] 或 [下拉式] 下拉式方塊中的編輯控制項只能顯示文字，而擁有者會在下拉式清單方塊中繪製選取欄位。

主控描繪下拉式方塊的擁有者必須處理 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 每當需要重新繪製下拉式方塊的一部分時，就會傳送此訊息。 擁有者可能需要根據為下拉式方塊指定的樣式來處理其他訊息。

應用程式可以藉由指定 [**cbs \_ OWNERDRAWFIXED**](combo-box-styles.md) 或 [**cbs \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式來建立主控描繪的下拉式方塊。 如果下拉式方塊中的所有清單專案都有相同的高度（例如字串或圖示），則應用程式可以使用 **CBS \_ OWNERDRAWFIXED** 樣式。 如果清單專案具有不同的高度（例如不同大小的點陣圖），則應用程式可以使用 **CBS \_ OWNERDRAWVARIABLE** 樣式。

主控描繪下拉式方塊的擁有者可以處理 [**WM \_ MEASUREITEM**](wm-measureitem.md) 訊息，以便在下拉式方塊中指定清單專案的維度。 如果應用程式使用 [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式建立下拉式方塊，系統只會傳送一次 **WM \_ MEASUREITEM** 訊息。 擁有者指定的維度會用於所有清單專案。 如果使用 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式，系統就會針對新增至下拉式方塊的每個清單專案傳送 **WM \_ MEASUREITEM** 訊息。 擁有者可以在任何時間使用 [**cb \_ GETITEMHEIGHT**](cb-getitemheight.md) 和 [**cb \_ SETITEMHEIGHT**](cb-setitemheight.md) 訊息，隨時決定或設定清單專案的高度。

如果顯示在主控描繪下拉式方塊中的資訊包含文字，應用程式可以藉由指定 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式來追蹤每個清單專案的文字。 具有 [**CBS \_ 排序**](combo-box-styles.md) 樣式的下拉式方塊會根據此文字來排序。 如果下拉式方塊已排序，而非 **CBS \_ HASSTRINGS** 樣式，則擁有者必須處理 [**WM \_ COMPAREITEM**](wm-compareitem.md) 訊息。

在主控描繪的下拉式方塊中，擁有者必須追蹤包含除了文字以外之資訊的清單專案。 其中一個方便的方式是將資訊的控制碼儲存為專案資料。 若要釋放與下拉式方塊中專案相關聯的資料物件，擁有者可以處理 [**WM \_ DELETEITEM**](wm-deleteitem.md) 訊息。

## <a name="subclassed-combo-boxes"></a>子類別化下拉式方塊

子類別化是允許應用程式攔截和處理傳送或張貼至視窗之訊息的程式。 藉由使用子類別化，應用程式可以替代特定訊息的處理，同時將大部分的訊息處理保留給類別定義的視窗程式。

當作業系統建立視窗時，會將它的相關資訊儲存在包含視窗程式指標的內部資料結構中。 若要子類別化視窗，應用程式會呼叫 [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) 函式，將該程式的指標取代為應用程式定義之子類別程式的指標。 之後，視窗中的所有訊息都會傳送至子類別程式。 此程式會接著使用 [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) 函式，將未處理的訊息傳遞給原始的視窗程式。 如需 COMBOBOX 類別視窗程式所執行之訊息處理的描述，請參閱 [預設下拉式方塊行為](combo-box-features.md)。

當下拉式方塊位於對話方塊外部時，除非它使用子類別程式，否則應用程式無法處理 TAB 鍵、ENTER 鍵和 ESC 鍵。 當簡單或下拉下拉式方塊收到輸入焦點時，它會立即將焦點設定為其子編輯控制項。 因此，應用程式必須將編輯控制項子類別化，才能攔截簡單或下拉式方塊的鍵盤輸入。 如需這項工作的範例，請參閱子類別化 [下拉式](using-combo-boxes.md)方塊。

如果子類別程式處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，則必須使用 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) 函式來準備繪製。 在呼叫 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 函式之前，它會將裝置內容 (DC) 控制碼傳遞為視窗程式的 *wParam* 參數。 如果先呼叫 **EndPaint** ，則類別視窗程式不會進行繪製，因為 **EndPaint** 會驗證整個視窗。

子類別化的相關技術 superclassing。 超類類似于任何其他類別，不同之處在于其視窗程式不會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 來處理未處理的訊息。 相反地，它會將未處理的訊息傳遞至父視窗類別的視窗程式。 遵循 [視窗程式](/windows/desktop/winmsg/window-procedures) 中的指導方針，以避免子類別化和 superclassing 可能發生的問題。

 

 
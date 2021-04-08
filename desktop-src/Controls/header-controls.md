---
title: 關於標題控制項
description: 標題控制項是通常位於文字或數位資料行上方的視窗。 它包含每個資料行的標題，而且可以分成幾個部分。
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683133"
---
# <a name="about-header-controls"></a>關於標題控制項

標題控制項是通常位於文字或數位資料行上方的視窗。 它包含每個資料行的標題，而且可以分成幾個部分。 使用者可以拖曳分隔各個部分的分隔線，以設定每個資料行的寬度。 下圖顯示的標題控制項具有標記的資料行，可提供目錄中檔案的詳細資訊。

![具有三欄標題控制項之對話方塊的螢幕擷取畫面](images/header.png)

您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立標題控制項，並指定 [**WC \_ 標頭**](common-control-window-classes.md) 視窗類別和適當的 [標題控制項樣式](header-control-styles.md)。 載入通用控制項 DLL 時，會註冊此視窗類別。 若要確定已載入此 DLL，請使用 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數。 建立標題控制項之後，您可以將它分割成部分、設定每個元件中的文字，以及使用標頭視窗訊息控制視窗的外觀。

標題控制項可以建立為另一個控制項（例如清單方塊）的子視窗。 不過，父控制項並不知道標題控制項，而且不允許標頭所佔用的空間，結果清單專案將出現在標頭後方。 如果您想要在清單方塊或其他控制項中使用標題控制項，父控制項必須是主控描繪，才能將所有專案顯示在正確的位置。

清單視圖控制項已經有標題控制項。 您可以使用 [**LVM \_ Messageheaders**](lvm-getheader.md) 或 [**ListView \_ messageheaders**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) 來取出現有的控制項，而不是建立清單視圖控制項的標題控制項。

-   [標題控制項大小和位置](#header-control-size-and-position)
-   [項目](#items)
-   [擁有者繪製的標題控制項](#owner-drawn-header-controls)
-   [標題控制項篩選](#header-control-filters)
-   [預設標頭控制訊息處理](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>標題控制項大小和位置

一般而言，您必須設定標題控制項的大小和位置，以符合特定矩形的界限，例如視窗的工作區。 藉由使用 [**HDM \_ 版面**](hdm-layout.md) 配置訊息，您可以從標題控制項取出適當的大小和位置值。

傳送 HDM 配置時，您可以指定 [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout)結構的位址，其中包含標題控制項要佔用的矩形座標，並提供 [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)結構的指標。 [**\_**](hdm-layout.md) 控制項會以適當的大小和位置值來填滿 **WINDOWPOS** 結構，以將控制項放置在指定矩形的上方。 高度值是控制項的水準框線高度，以及目前在控制項裝置內容中所選取之字型的平均高度。

如果您想要使用 [**HDM \_ 版面**](hdm-layout.md) 配置來設定標題控制項的初始大小和位置，請設定控制項的初始可見度狀態，使其隱藏。 傳送 HDM 配置以抓取大小和位置值之後，您可以使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)函式來設定新的大小、位置和可見度狀態。 **\_**

## <a name="items"></a>項目

標題控制項通常會有數個定義控制項資料行的標頭專案。 您可以藉由將 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息傳送至控制項，將專案加入至標題控制項。 訊息包含 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的位址。 此結構會定義標頭專案的屬性，其中可包含字串、點陣圖影像、初始大小，以及應用程式定義的 **LPARAM** 值。

專案 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的 **bcp.fmt** 成員可以包含 **HDF \_ 字串** 或 **HDF \_ 點陣圖** 旗標，以指出控制項是否顯示專案的字串或點陣圖。 如果您想要同時顯示字串和點陣圖，請將 **bcp.fmt** 成員設定為包含 **HDF \_ OWNERDRAW** 旗標，以建立主控描繪專案。 **HDITEM** 結構也會指定格式化旗標，告知控制項是要置中、靠左對齊還是靠右對齊專案矩形中的字串或點陣圖。

[**HDM \_INSERTITEM**](hdm-insertitem.md) 會傳回新加入之專案的索引。 您可以使用其他訊息中的索引來設定屬性或取得專案的相關資訊。 您可以使用 [**HDM \_ DELETEITEM**](hdm-deleteitem.md) 訊息來刪除專案，並指定要刪除之專案的索引。

您可以使用 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息來設定現有標題專案的屬性，以及使用 [**HDM \_ GETITEM**](hdm-getitem.md) 訊息來取得專案的目前屬性。 若要取出標題控制項中的專案計數，請使用 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md) 訊息。

## <a name="owner-drawn-header-controls"></a>Owner-Drawn 標題控制項

您可以將標題控制項的個別專案定義為主控描繪專案。 使用這項技術可讓您擁有更多的控制，而不是標頭專案的外觀。

您可以使用 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息，將新的主控描繪專案插入至標題控制項或 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息，以將現有專案變更為主控描繪專案。 這兩個訊息都包含 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的位址，其 **bcp.fmt** 成員應設定為 **HDF \_ OWNERDRAW** 值。

當標題控制項必須繪製主控描繪的專案時，它會將 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息傳送至父視窗。 訊息的 *wParam* 參數是標題控制項的子視窗識別碼，而 *LParam* 參數是 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構的位址。 父視窗會使用結構中的資訊來繪製專案。 如果是標題控制項中的主控描繪專案， **DRAWITEMSTRUCT** 結構會包含下列資訊。



| member         | 描述                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_標頭**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 擁有者繪製控制項類型。                                                                                        |
| **CtlID**      | 標題控制項的子視窗識別碼。                                                                                                         |
| **itemID**     | 要繪製之專案的索引。                                                                                                                         |
| **itemAction** | [**ODA \_DRAWENTIRE**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 繪圖-動作旗標。                                                                                         |
| **itemState**  | [**ODS \_選取**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 的繪圖-動作旗標（如果游標位於專案上且滑鼠按鍵已關閉）。 否則，此成員為零。 |
| **hwndItem**   | 標題控制項的控制碼。                                                                                                                          |
| **hDC**        | 標題控制項的裝置內容控制碼。                                                                                                    |
| **rcItem**     | 要繪製之標頭專案的座標。 座標是相對於標題控制項的左上角。                               |
| **itemData**   | 與專案相關聯的應用程式定義32位值。                                                                                             |



 

## <a name="header-control-filters"></a>標題控制項篩選

藉由指定標題控制項的 [**HDS \_ FILTERBAR**](header-control-styles.md) 視窗樣式，您可以在資料行標題底下啟用篩選編輯方塊的位置。 篩選按鈕會出現在編輯方塊旁邊。 您可以藉由回應 [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md)、 [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md)、 [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)或 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知碼來執行篩選。

根據預設，編輯方塊包含提示讓使用者輸入文字。 您可以使用 [**標頭 \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) 或 [**標頭 \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)，將編輯方塊還原為此預設狀態。

下列程式碼範例示範如何從清單視圖控制項取出標題控制項，以及加入篩選列。


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>預設標頭控制訊息處理

本節說明 [**WC \_ 標頭**](common-control-window-classes.md) 視窗類別的視窗程式所處理的視窗訊息。



| 訊息                                            | 處理已執行                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                 | 初始化標題控制項。                                                                                                                                                                                                                                                                               |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)               | 取消初始化標題控制項。                                                                                                                                                                                                                                                                             |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | 使用控制項目前的背景色彩，填滿標題控制項的背景。                                                                                                                                                                                                                      |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | 傳回 [**DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) 和 [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) 值的組合。                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | 傳回目前字型的控制碼，標題控制項會使用此控制碼來繪製其文字。                                                                                                                                                                                                                 |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | 捕捉滑鼠輸入。 如果滑鼠游標位於分隔線上，控制項會傳送 [HDN \_ BEGINTRACK](hdn-begintrack.md) 通知碼並開始拖曳分隔線。 如果資料指標位於專案上，則專案會顯示為已按下的狀態。                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | 與 [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) 訊息相同。                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | 釋放滑鼠捕捉。 如果控制項是追蹤滑鼠移動，它會傳送 [HDN \_ ENDTRACK](hdn-endtrack.md) 通知碼，並重新繪製標題控制項。 否則，控制項會傳送 [HDN \_ ITEMCLICK](hdn-itemclick.md) 通知碼，並重新繪製已按下的標頭專案。 |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | 如果正在拖曳分隔線，控制項會傳送 [HDN \_ TRACK](hdn-track.md) 通知程式碼，並在新位置顯示該專案。 如果滑鼠左鍵已關閉，且游標位於某個專案上，則專案會顯示為 [已按下] 狀態。                                                      |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)             | 配置並初始化內部資料結構。                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | 在標題控制項未初始化之後，釋出標題控制項所配置的資源。                                                                                                                                                                                                                |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                      | 繪製標題控制項的無效區域。 如果 *wParam* 參數不是 Null，則控制項會假設值為 HDC，並且使用該裝置內容繪製。                                                                                                                                    |
| [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)           | 設定資料指標圖形，視資料指標位於分割線或在標頭專案中而定。                                                                                                                                                                                                                   |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | 在標題控制項的裝置內容中選取新的字型控點。                                                                                                                                                                                                                                     |



 

 

 
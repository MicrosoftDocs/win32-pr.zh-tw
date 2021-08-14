---
title: 關於索引標籤控制項
description: 「索引標籤控制項」類似於筆記本裡的分隔頁或檔案櫃中的標籤。 藉由使用索引標籤控制項，應用程式可以定義視窗或對話方塊中同一個區域的多個頁面。
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 512955ec2b3426227366ef109669c52a6c07c8882374d935023123182de194ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670420"
---
# <a name="about-tab-controls"></a>關於索引標籤控制項

「索引標籤控制項」類似於筆記本裡的分隔頁或檔案櫃中的標籤。 藉由使用索引標籤控制項，應用程式可以定義視窗或對話方塊中同一個區域的多個頁面。 每個頁面都包含特定類型的資訊或應用程式在使用者選取對應的索引標籤時所顯示的一組控制項。

下列螢幕擷取畫面顯示簡單的索引標籤控制項，其中包含一周中各天的索引標籤。 已選取 [星期二] 索引標籤。

![包含五個索引標籤的屬性工作表螢幕擷取畫面，每週的每一天一次](images/tab-simple.png)

本主題包含下列各節。

-   [建立索引標籤控制項](#creating-tab-controls)
-   [索引標籤控制項樣式](#tab-control-styles)
-   [Tab 和 Tab 屬性](#tabs-and-tab-attributes)
-   [顯示區域](#display-area)
-   [索引標籤選項](#tab-selection)
-   [索引標籤控制項影像清單](#tab-control-image-lists)
-   [定位鍵大小和位置](#tab-size-and-position)
-   [主控描繪索引標籤](#owner-drawn-tabs)
-   [索引標籤控制項工具提示](#tab-control-tooltips)
-   [預設選項卡控制訊息處理](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>建立索引標籤控制項

您可以藉由呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立索引標籤控制項，並指定 [**WC \_ TABCONTROL**](common-control-window-classes.md) 視窗類別。 載入通用控制項 DLL 時，會註冊此視窗類別。 若要確定已載入 DLL，請使用 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數。

在 Microsoft Visual Studio 中，您可以使用 [工具箱] 來建立索引標籤控制項。

您會將訊息傳送至索引標籤控制項以加入索引標籤，否則會影響控制項的外觀和行為。 每個訊息都有您可以使用的對應宏，而不是明確地傳送訊息。 您無法停用 [選項卡] 控制項中的個別索引標籤。 不過，您可以停用對應的頁面，以停用屬性工作表中的索引標籤控制項。

## <a name="tab-control-styles"></a>索引標籤控制項樣式

您可以在建立控制項時指定索引標籤控制項樣式，將某些特性套用至索引標籤控制項。 例如，您可以在索引標籤控制項中指定索引標籤的對齊方式和一般外觀。

您可以藉由指定 [ [**TCS] \_ 按鈕**](tab-control-styles.md) 樣式，讓索引標籤看起來像按鈕。 這種索引標籤控制項中的索引標籤應該提供與按鈕控制項相同的功能;也就是說，按一下索引標籤應該執行命令，而不是顯示頁面。 因為 [按鈕] 索引標籤控制項中的顯示區域通常不會使用，所以不會在其周圍繪製框線。

您可以指定 [**TCS \_ FOCUSONBUTTONDOWN**](tab-control-styles.md) 樣式，讓索引標籤在按一下時接收輸入焦點。 此樣式通常僅適用于 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式。 您可以使用 [**TCS \_ FOCUSNEVER**](tab-control-styles.md) 樣式，指定索引標籤不會在按一下時收到輸入焦點。

依預設，索引標籤控制項只會顯示一列索引標籤。 如果未顯示所有索引標籤，則索引標籤控制項會顯示上下按鈕控制項，讓使用者可以將其他索引標籤移到視野中。 如果有必要，您可以藉由指定 [**TCS \_ 多行**](tab-control-styles.md) 樣式，讓索引標籤控制項顯示多個資料列的索引標籤。 使用此樣式，可以一次顯示所有索引標籤。 除非您指定 [**TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) 樣式，否則索引標籤會在每個資料列中保持靠左對齊。 在此情況下，每個索引標籤的寬度都會增加，讓索引標籤的每個資料列都填滿整個索引標籤控制項的寬度。

索引標籤控制項會自動調整每個索引標籤的大小，以符合其圖示（如果有的話）及其標籤。 若要提供相同寬度的所有索引標籤，您可以指定 [**TCS \_ FIXEDWIDTH**](tab-control-styles.md) 樣式。 控制項會調整所有索引標籤的大小以符合最寬的標籤，或您可以使用 [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) 訊息來指派特定的寬度和高度。 在每個索引標籤中，控制項會將圖示和標籤放在標籤的左邊。 您可以藉由指定 [**TCS \_ FORCEICONLEFT**](tab-control-styles.md) 樣式來強制左側的圖示，讓標籤保持在最中央。 您可以使用 [**TCS \_ FORCELABELLEFT**](tab-control-styles.md) 樣式，將圖示和標籤靠左對齊。 您無法將 **TCS \_ FIXEDWIDTH** 樣式與 [**TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) 樣式搭配使用。

您可以使用 [**TCS \_ OWNERDRAWFIXED**](tab-control-styles.md) 樣式，指定父視窗繪製控制項中的索引標籤。 如需詳細資訊，請參閱 [擁有者繪製](#owner-drawn-tabs)索引標籤。

您可以使用 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式，指定索引標籤控制項將建立工具提示控制項。 如需有關這個的詳細資訊，請參閱 [選項提示控制項](#tab-control-tooltips)。

## <a name="tabs-and-tab-attributes"></a>Tab 和 Tab 屬性

索引標籤控制項中的每個索引標籤都包含一個圖示、一個標籤和一個應用程式定義的資料。 這項資訊是由 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構所指定。 您可以將索引標籤加入至索引標籤控制項、取出索引標籤數目、抓取和設定索引標籤的內容，以及刪除索引標籤。 索引標籤是由其以零為基底的索引加以識別。

若要將索引標籤加入至索引標籤控制項，請使用 [**TCM \_ INSERTITEM**](tcm-insertitem.md) 訊息，並指定專案的位置和 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構的位址。 您可以使用 [**tcm \_ GETITEM**](tcm-getitem.md) 和 [**tcm \_ SETITEM**](tcm-setitem.md) 訊息來取得和設定現有索引標籤的內容。 針對每個索引標籤，您可以指定圖示、標籤或兩者。 您也可以指定要與索引標籤建立關聯的應用程式定義資料。

您可以使用 tcm [**\_ GETITEMCOUNT**](tcm-getitemcount.md) 訊息來取出目前的索引標籤數目、使用 [**tcm \_ DELETEITEM**](tcm-deleteitem.md) 訊息刪除索引標籤，以及使用 [**tcm \_ DELETEALLITEMS**](tcm-deleteallitems.md) 訊息刪除索引標籤控制項中的所有索引標籤。

您可以將應用程式定義資料與每一個索引標籤建立關聯。例如，您可以使用對應的索引標籤來儲存每個頁面的相關資訊。根據預設，索引標籤控制項會針對應用程式定義的資料，每個索引標籤配置四個額外的位元組。 您可以使用 [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) 訊息來變更每個索引標籤的額外位元組數目。 只有當選項卡控制項為空白時，才能使用此訊息。

應用程式定義的資料是由 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構的 **lParam** 成員所指定。 如果您使用超過4個位元組的應用程式定義資料，您需要定義自己的結構，並使用它來取代 **TCITEM**。 您可以使用 [**TCM \_ GETITEM**](tcm-getitem.md) 和 [**tcm \_ SETITEM**](tcm-setitem.md) 訊息，以抓取和設定索引標籤的其他相關資訊，來取得和設定應用程式定義的資料。

您結構的第一個成員必須是 [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) 結構，而其餘成員必須指定應用程式定義的資料。 **TCITEMHEADER** 與 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)相同，不同之處在于它沒有 **lParam** 成員。 您的結構大小與 **TCITEMHEADER** 大小之間的差異應等於每個索引標籤的額外位元組數目。

## <a name="display-area"></a>顯示區域

索引標籤控制項的顯示區域是應用程式顯示目前頁面的區域。 一般而言，應用程式會建立一個子視窗或對話方塊，設定視窗大小和位置以符合顯示區域。 針對索引標籤控制項的視窗矩形，您可以使用 [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) 訊息來計算顯示區域的周框。

有時顯示區域必須是特定大小，例如，非模式子對話方塊的大小。 若為顯示區域指定周框，您可以使用 [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) 來計算索引標籤控制項的對應視窗矩形。

## <a name="tab-selection"></a>索引標籤選項

當使用者選取索引標籤時，索引標籤控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送其父視窗通知碼。 [TCN \_ SELCHANGING](tcn-selchanging.md)通知碼會在選取範圍變更前傳送，而[TCN \_ SELCHANGE](tcn-selchange.md)通知碼會在選取範圍變更之後傳送。

您可以處理 [TCN \_ SELCHANGING](tcn-selchanging.md) 來儲存傳出頁面的狀態。 您可以傳回 **TRUE** 以防止選取範圍變更。 例如，您可能不想要切換離開控制項有無效設定的子對話方塊。

您必須處理 [TCN \_ SELCHANGE](tcn-selchange.md) ，才能在顯示區域中顯示傳入的頁面。 這可能只需要變更子視窗中所顯示的資訊。 更常發生的是，每個頁面都包含一個子視窗或一個對話方塊。 在此情況下，應用程式可能會藉由終結或隱藏外寄子視窗或對話方塊，以及建立或顯示內送的子視窗或對話方塊，來處理此通知。

您可以使用 [**tcm \_ GETCURSEL**](tcm-getcursel.md) 和 [**tcm \_ SETCURSEL**](tcm-setcursel.md) 訊息來取得和設定目前的選取範圍。

## <a name="tab-control-image-lists"></a>索引標籤控制項影像清單

每個索引標籤都可以有相關聯的圖示，此圖示是由索引標籤控制項影像清單中的索引所指定。 建立索引標籤控制項時，它沒有相關聯的影像清單。 應用程式可以使用 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函式來建立影像清單，然後使用 [**TCM \_ SETIMAGELIST**](tcm-setimagelist.md) 訊息將它指派給索引標籤控制項。

您可以將影像加入至索引標籤控制項的影像清單，就像您對任何其他影像清單一樣。 不過，應用程式應該使用 [**TCM \_ REMOVEIMAGE**](tcm-removeimage.md) 訊息來移除影像，而不是使用 [**ImageList \_ remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) 函數。 此訊息可確保每個索引標籤都會與之前的映射保持相關聯。

終結的索引標籤控制項不會摧毀與其相關聯的影像清單。 您必須分開終結影像清單。 如果您想要將相同的影像清單指派給多個索引標籤控制項，這會很有用。

若要取得目前與索引標籤控制項相關聯之影像清單的控制碼，您可以使用 [**TCM \_ GETIMAGELIST**](tcm-getimagelist.md) 訊息。

## <a name="tab-size-and-position"></a>定位鍵大小和位置

索引標籤控制項中的每個索引標籤都有大小和位置。 您可以設定索引標籤的大小、取出索引標籤的周框，或判斷哪個索引標籤位於指定的位置。

針對固定寬度和主控描繪的索引標籤控制項，您可以使用 [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) 訊息來設定索引標籤的精確寬度和高度。 在其他索引標籤控制項中，每個索引標籤的大小都是根據索引標籤的圖示和標籤來計算。索引標籤控制項包含框線和額外邊界的空間。 您可以使用 [**TCM \_ SETPADDING**](tcm-setpadding.md) 訊息來設定邊界的粗細。

您可以使用 [**TCM \_ GETITEMRECT**](tcm-getitemrect.md) 訊息來判斷索引標籤目前的周框。 您可以使用 [**TCM \_ system.windows.media.visualtreehelper.hittest**](tcm-hittest.md) 訊息，判斷哪一個索引標籤（如果有的話）位於指定的位置。

在具有 [**TCS \_ 多行**](tab-control-styles.md) 樣式的索引標籤控制項中，您可以使用 [**TCM \_ GETROWCOUNT**](tcm-getrowcount.md) 訊息來判斷目前的索引標籤數目。

## <a name="owner-drawn-tabs"></a>Owner-Drawn] 索引標籤

如果有 [**TCS \_ OWNERDRAWFIXED**](tab-control-styles.md) 樣式的索引標籤控制項，父視窗必須藉由處理 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息來繪製索引標籤。 當需要繪製索引標籤時，索引標籤控制項會傳送此訊息。 *LParam* 參數會指定 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的位址，其中包含索引標籤的索引、其周框，以及要在其中繪製 (DC) 的裝置內容。

依預設， [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)的 **itemData** 成員會包含 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)結構之 **lParam** 成員的值。 但是，如果您變更每個索引標籤的應用程式定義資料量， **itemData** 會改為包含資料的位址。 您可以使用 [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) 訊息來變更每個索引標籤上的應用程式定義資料量。

若要在索引標籤控制項中指定專案的大小，父視窗必須處理 [**WM \_ MEASUREITEM**](wm-measureitem.md) 訊息。 由於主控描繪索引標籤控制項中的所有索引標籤大小都相同，因此此訊息只會傳送一次。 針對不同大小的主控描繪索引標籤，沒有任何索引標籤控制項樣式。 您也可以使用 [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) 訊息來設定索引標籤的寬度和高度。

## <a name="tab-control-tooltips"></a>索引標籤控制項工具提示

您可以使用工具提示控制項，在索引標籤控制項中提供每個索引標籤的簡短描述。 具有 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式的索引標籤控制項，會在建立時建立工具提示控制項，並在工具提示控制項損毀時將它終結。 您也可以建立工具提示控制項，並將它指派給索引標籤控制項。

如果您使用具有索引標籤控制項的工具提示控制項，父視窗必須處理 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知程式碼，以提供要求上每個索引標籤的描述。

若要使用具有多個索引標籤控制項的相同工具提示控制項，請自行建立工具提示控制項，並使用 [**TCM \_ SETTOOLTIPS**](tcm-settooltips.md) 訊息將它指派給索引標籤控制項。 您可以使用 [**TCM \_ GETTOOLTIPS**](tcm-gettooltips.md) 訊息來抓取索引標籤控制項目前工具提示控制項的控制碼。 如果您建立自己的工具提示控制項，則不應使用 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式。

## <a name="default-tab-control-message-processing"></a>預設選項卡控制訊息處理

本節說明由索引標籤控制項執行的訊息處理。 本檔的其他章節將討論索引標籤控制項特定的訊息。



| 訊息                                                  | 處理已執行                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | 如果索引標籤控制項放開滑鼠捕捉本身，就不會執行任何動作。 如果另一個視窗已捕捉到滑鼠，而按鈕已關閉，則命令會放開按鈕。                                                                                                                                                                                                                                                                                                                |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                 | 配置並初始化內部資料結構。 如果指定了 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式，控制項會建立工具提示控制項。                                                                                                                                                                                                                                                                                                    |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)               | 釋出在 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 處理期間配置的資源。                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | 傳回 DLGC \_ WANTARROWS 和 DLGC WANTCHARS 值的組合 \_ 。                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | 傳回用於標籤之字型的控制碼。                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | 處理方向按鍵並變更選取範圍（如適用）。                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | 使具有焦點的索引標籤失效，因此將會重新繪製以反映未取得焦點狀態。                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | 將訊息轉送至工具提示控制項（如果有的話），並在使用者按一下索引標籤時變更選取專案。如果使用者按一下按鈕，控制項會重新繪製按鈕，以提供凹陷的外觀並捕捉滑鼠。 如果使用者按一下索引標籤或按鈕，並指定 [**TCS \_ FOCUSONBUTTONDOWN**](tab-control-styles.md) 樣式，控制項就會將焦點設為本身。                                                     |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | 如果已按下按鈕，則放開滑鼠。 如果游標停留在按鈕上且正在關閉，控制項會據以變更選取專案，並重新繪製按鈕。                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | 將訊息轉送至工具提示控制項（如果有的話）。 如果指定了 [ [**TCS] \_ 按鈕**](tab-control-styles.md) 樣式，並且在按一下之後將滑鼠按鍵保持在關閉狀態，則控制項也可以重繪受影響的按鈕，讓它成為引發或凹陷的外觀。                                                                                                                                                                                            |
| [**WM \_ 通知**](wm-notify.md)                          | 轉寄工具提示控制項所傳送的通知碼。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                            | 在顯示區域周圍繪製框線 (除非指定了 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式) 並繪製任何交集于無效矩形的索引標籤。 在每個索引標籤中，它會繪製 (的索引標籤主體，或將 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息傳送至父視窗) ，然後在索引標籤周圍繪製框線。如果 *wParam* 參數不是 Null，則控制項會假設值為 HDC，並且使用該裝置內容繪製。 |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)       | 將 [NM \_ RCLICK](nm-rclick-tab.md) 通知程式碼傳送至父視窗。                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | 使具有焦點的索引標籤失效，以便重新繪製以反映焦點狀態。                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | 設定用於標籤的字型。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)                    | 設定內部旗標的狀態，這個旗標會決定當插入和刪除專案時、變更字型時，是否重新繪製控制項。                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)                     | 重新計算索引標籤的位置，並且可能使部分的索引標籤控制項無效，以強制重新繪製部分或所有索引標籤。                                                                                                                                                                                                                                                                                                                                                             |



 

 

 
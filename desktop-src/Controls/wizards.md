---
title: 如何建立嚮導
description: Wizard 是一種屬性工作表，可提供簡單且強大的方式來引導使用者完成程式。
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4254b448c719e3e1397fceadfcdc28475eaeae588f6f1eb0f0168cea07327d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655816"
---
# <a name="how-to-create-wizards"></a>如何建立嚮導

Wizard 是一種屬性工作表，可提供簡單且強大的方式來引導使用者完成程式。

嚮導是簡化使用者體驗的其中一個關鍵。 它們可讓您執行複雜的作業，例如應用程式的設定，並將其分成一系列簡單的步驟。 在程式的每個階段，您可以提供所需專案的說明，並顯示可讓使用者進行選取並輸入文字的控制項。

Wizard 其實是一種屬性工作表。 屬性工作表基本上是 *頁面* 集合的容器，每個頁面都是個別的對話方塊。 雖然一般屬性工作表可讓使用者隨時存取任何頁面，但嚮導會依序顯示頁面。 按鈕是用來向前及向後導覽，而不是索引標籤。 頁面的顯示順序是由應用程式所控制，並且可以根據使用者輸入加以修改。

wizard 的主要樣式有兩種：舊版 Wizard97 樣式，以及 Windows Vista 中引進的 Aero 樣式。 如需圖例，請參閱 [關於屬性工作表](property-sheets.md)。  (第三種樣式，只使用 PSH \_ WIZARD 或 PSH \_ wizard \_ LITE 旗標，提供簡單的屬性工作表順序，不含標頭或浮水印。 ) 

> [!Note]  
> 在嚮導的內容中，「浮水印」是顯示在部分頁面左邊界的點陣圖。

 

本檔中的討論內容假設您正在為具有 [5.80 版](common-control-versions.md) 或更新版本之通用控制項的系統，執行嚮導。 如果您嘗試使用 Wizard97 樣式搭配舊版的通用控制項，則您的應用程式可能會進行編譯，但不會正確顯示。 如需有關如何在舊版系統上建立與 Wizard97 相容的 wizard 的討論，請參閱本主題稍後的回溯相容的 wizard。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="wizard-implementation"></a>Wizard 執行

執行嚮導與執行一般的屬性工作表類似。 在最基本的層級中，您可以在定義屬性工作表的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中，設定下列其中一個旗標或旗標組合。



| 旗標                           | 樣式                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| PSH \_ WIZARD                    | 沒有標頭或點陣圖的簡易 wizard。                                                                                                           |
| PSH \_ WIZARD \_ LITE              | 類似于 PSH \_ WIZARD，外觀上有些微差異; 例如，按鈕上方的分隔線會設定為視窗的全形。 |
| PSH \_ WIZARD97                  | Wizard97 wizard (選擇性的) 標頭、標頭點陣圖和浮水印。                                                                            |
| PSH \_ WIZARD \| PSH \_ AEROWIZARD | Aero Wizard。 Aero 的嚮導不會使用浮水印或標頭點陣圖。 它們需要單一執行緒的單元 (STA) 模型。                         |



 

執行嚮導的基本程式如下所示：

1.  為每個頁面建立對話方塊範本。
2.  藉由建立每個頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構來定義頁面。 此結構會定義頁面，並包含對話方塊範本和任何點陣圖或其他資源的指標。
3.  將在上一個步驟中建立的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構傳遞至 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函數，以建立頁面的 HPROPSHEETPAGE 控制碼。
4.  藉由建立 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構來定義嚮導。
5.  將 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構傳遞至 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式，以顯示嚮導。
6.  針對每個頁面執行對話方塊程式，以處理來自頁面控制項的通知訊息，以及 wizard 的按鈕和處理其他 Windows 訊息。

### <a name="create-the-dialog-box-templates"></a>建立對話方塊範本

有兩種基本類型的 wizard 頁面：外部和內部。 外部頁面是 (歡迎使用) 和完成頁面的簡介。 所有其他都是內部頁面。

**外部頁面對話方塊範本**

簡介和完成頁面的基本版面配置相同。 下圖顯示範例 Wizard97 簡介頁面，以及預留位置浮水印。

![顯示 wizard 頁面的螢幕擷取畫面，右邊有一個圖形、右邊的標題和內文文字，以及底部的 [上一頁] 和 [取消] 按鈕](images/wiz97exterior.png)

針對 Wizard97 的外部頁面，對話方塊範本為317x193 對話方塊單位。 它會填滿所有的 wizard，除了包含 [ **上一頁** **]、[下一頁]** 和 [ **取消** ] 按鈕的標題和頻外。 範本的左邊是保留給「浮水印」點陣圖，不應包含任何控制項。 浮水印是在 wizard 的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中指定，並且會自動加入至頁面。 設計資源範本時，您必須允許其空間。

當您建立浮水印點陣圖時，請記住，如果使用者選擇大型系統字型，對話方塊的大小可能會增加。 不同的語言也傾向于使用不同的字型計量。 當頁面成長時，為浮水印保留的區域會以比例放大。 不過，您無法變更浮水印點陣圖，也不能延展點陣圖以填滿較大的區域。 相反地，點陣圖會保留在保留區域左上角部分的原始大小。 浮水印未涵蓋的較大保留區域部分，會自動填入點陣圖左上角圖元的色彩。

如果您需要針對不同的字型計量使用不同大小的浮水印點陣圖，有兩個可能的解決方案：

-   建立嚮導之前取得字型計量，並指定適當大小的浮水印點陣圖。
-   建立嚮導時，請勿指定浮水印點陣圖。 Wizard97 會將浮水印區域保留空白。 然後，在為浮水印保留的區域上繪製適當大小的點陣圖。

您可以依照一般對話方塊的方式，將控制項放在浮水印右邊的區域中。 此區域的背景色彩是由系統決定，而不需要您採取任何動作。 您通常會在此區域中放置兩個靜態控制項。 上半部會保存標題，並使用大型粗體字型 (Wizard97) 的12點 Verdana 粗體。 另一種是解說文字，則使用標準對話方塊字型。

[簡介] 和 [完成] 頁面之間的主要差異是 [wizard] 按鈕和靜態控制項中的文字。 簡介頁面通常會有 **下** 一個按鈕和 [ **上一頁** ] 按鈕，而且只會啟用 [ **下一步]** 按鈕。 完成頁面會啟用 [ **上一頁** ] 按鈕，而 [ **下一步** ] 按鈕會由 **[完成]** 按鈕取代。

> [!Note]  
> 在 Aero 精靈中，[ **上一頁** ] 按鈕會由標題列中的箭號按鈕取代。

 

您可以將 [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)訊息傳送給 wizard，以修改 [**完成]** 按鈕上的文字。 依預設，[ **完成]** 按鈕不包含鍵盤快速鍵。 若要定義鍵盤快速鍵，請在您傳遞至 PSM SETFINISHTEXT 的文字字串中包含連字號 \_ 。 例如，「&完成」會將 ' F ' 定義為鍵盤對應鍵。

**內部頁面對話方塊範本**

內部頁面的外觀與外部頁面稍有不同。 下圖顯示範例 Wizard97 內部頁面，其中包含預留位置標頭點陣圖。

![頁面的螢幕擷取畫面，其中包含標題和子標題文字，以及頂端的文字、中間的文字，以及底部的按鈕](images/wiz97interior.png)

頁面頂端的標頭區域是由屬性工作表處理，因此不會包含在範本中。 標頭的內容會指定在頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構和 Wizard 的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中。 因為內部頁面必須符合標題和按鈕，所以 Wizard97 對話方塊範本是317x143 對話單位，稍微小於外部頁面的範本。

下圖顯示從相同範本建立的 Aero Wizard。

![螢幕擷取畫面，其頂端有標題區域，且底部只有 [下一步] 和 [取消] 按鈕，與上一個專案不同](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>定義嚮導頁面

建立對話方塊範本和相關資源（例如點陣圖和字串資料表）之後，您可以建立屬性工作表頁面。 此程式類似于標準屬性工作表的程式。 首先，填入 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的適當成員。  (部分成員是由嚮導所特有。 ) 接著呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式來建立頁面的 HPROPSHEETPAGE 控制碼。

下列與 wizard 相關的旗標可以在 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **dwFlags** 成員中設定。



| 旗標                   | 描述                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | 針對 Wizard97 中的外部頁面設定此旗標。 標頭不會顯示，而且可以顯示浮水印。                                |
| PSP \_ USEHEADERTITLE    | 為內部頁面設定此旗標，將標題放在 Wizard97 的標頭區域中，或在 Aero Wizard 中的工作區頂端。 |
| PSP \_ USEHEADERSUBTITLE | 為內部頁面設定此旗標，以在 Wizard97 的標頭區域中放入子標題。                                                  |



 

如果您已設定 PSP \_ USEHEADERTITLE 或 psp \_ USEHEADERSUBTITLE，請分別將標題和子標題文字指派給 **pszHeaderTitle** 和 **pszHeaderSubtitle** 成員。 當您將文字字串指派給 [**PROPSHEETPAGE**](pss-propsheetpage.md) 和 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構的成員時，您可以指派字串指標，或使用 **MAKEINTRESOURCE** 宏來指派字串資源的值。 字串資源是從 wizard **PROPSHEETHEADER** 結構的 **hInstance** 成員所指定的模組載入。

當您呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 來建立頁面時，請將結果指派給 HPROPSHEETPAGE 控制碼陣列的元素。 建立屬性工作表時，會使用這個陣列。 頁面控制碼的陣列索引會決定其顯示的預設順序。 建立頁面的 HPROPSHEETPAGE 控制碼之後，您可以重複使用相同的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，藉由指派新值給相關成員來建立下一頁。

建立頁面的另一種方式是為每個頁面使用不同的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，並建立結構的陣列。 建立屬性工作表時，會使用這個陣列，而不是 HPROPSHEETPAGE 控制碼的陣列。 使用個別的 **PROPSHEETPAGE** 結構，不需要呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ，但會使用更多的記憶體。 否則，這兩種方法之間並沒有顯著的差異。

下列範例會將值指派給 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，以定義內部 Wizard97 頁面。 在此範例中，頁面的標題、子標題和對話方塊範本都是由其資源識別碼所識別。 然後呼叫 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式來建立頁面的 HPROPSHEETPAGE 控制碼。 因為它將會是第二頁，所以會將控制碼指派給控制碼 *ahpsp* 的陣列，索引為1。


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>自訂頁面資料

當您建立網頁時，您可以使用 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **lParam** 成員將自訂資料指派給它，通常是藉由將指標指派給使用者定義的結構。

第一次選取頁面時，其對話方塊程式會收到 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。 訊息的 *lParam* 值指向頁面 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的複本，您可以從中取得自訂資料。 然後，您可以使用 [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) 搭配 GWL \_ USERDATA 作為索引參數，來儲存這項資料以用於後續訊息。 多個頁面可以有相同資料的指標，而任何頁面所做的資料變更都可供其對話方塊程式中的其他頁面使用。

### <a name="define-the-wizard-property-sheet"></a>定義 Wizard 屬性工作表

如同一般的屬性工作表，您可以藉由填入 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構的成員來定義 wizard 的屬性工作表。 此結構可讓您指定組成 wizard 的頁面，以及顯示的預設順序，以及數個相關的參數。 接著，您可以藉由呼叫 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式來啟動精靈。

在 Wizard97 樣式中，會忽略 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **pszCaption** 成員。 相反地，嚮導會顯示目前頁面的對話方塊範本中指定的標題。 如果範本缺少標題，則會顯示前一頁的標題。 因此，若要在所有頁面上顯示相同的標題，請在 [簡介] 頁面的範本中指定標題。

在 Aero Wizard 樣式中，對話方塊標題是取自 **pszCaption**。

如果您已建立頁面的 HPROPSHEETPAGE 控制碼陣列，請將陣列指派給 **phpage** 成員。 如果您改為建立 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的陣列，請將陣列指派給 **ppsp** 成員，然後 \_ 在 **dwFlags** 成員中設定 PSH PROPSHEETPAGE 旗標。

下列範例會將值指派給 *psh*、 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構，然後呼叫 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式來啟動 wizard。 Wizard97 樣式的 wizard 具有浮水印和標頭圖形，由其資源識別碼指定。 *Ahpsp* 陣列包含所有 HPROPSHEETPAGE 控制碼，並定義其顯示的預設順序。


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>對話方塊程式

wizard 的每一頁都需要一個對話方塊程式來處理 Windows 的訊息，特別是來自其控制項和 wizard 的通知。 幾乎所有嚮導都必須能夠處理的三個訊息為 [**wm \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)、 [**wm \_ 摧毀**](/windows/desktop/winmsg/wm-destroy)和 [**wm \_ 通知**](wm-notify.md)。

在顯示頁面之前，以及按一下任何 wizard 按鈕時，會收到 [**WM \_ 通知**](wm-notify.md) 訊息。 訊息的 *lParam* 參數是指向 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 標頭結構的指標。 通知的識別碼包含在結構的程式 **代碼** 成員中。 大部分的嚮導需要處理的這四個通知如下。



| 程式碼                                | 描述                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md) | 在頁面顯示前傳送。          |
| [PSN \_ WIZBACK](psn-wizback.md)     | 按一下 [ **上一頁** ] 按鈕時傳送。   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | 按一下 [ **下一步]** 按鈕時傳送。   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | 按一下 [ **完成]** 按鈕時傳送。 |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>處理 WM \_ INITDIALOG 和 wm 損 \_ 毀

第一次顯示頁面時，其對話方塊程式會收到 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。 處理此訊息可讓 wizard 進行任何必要的初始化工作，例如儲存自訂資料或設定字型。

當屬性工作表已損毀時，您會收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息。 系統會自動終結嚮導，但處理此訊息可讓您進行任何必要的清除。

### <a name="handle-psn_setactive"></a>處理 PSN \_ advanced.field.setactive

每次顯示頁面時，都會傳送 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知碼。 第一次造訪網頁時，PSN \_ advanced.field.setactive 會遵循 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。 如果後續正在使用頁面，它只會收到 PSN \_ advanced.field.setactive 通知。 這項通知通常是用來初始化頁面的資料，並啟用適當的按鈕。

根據預設，嚮導會顯示[上一頁 **]、[下一頁] 和 [****取消**] 按鈕，並啟用所有按鈕。 若要停用按鈕或顯示 **[完成** ] 而不是 **[下一步**]，您必須傳送 [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) 訊息。 傳送此訊息之後，按鈕的狀態會一直保留到另一個 **PSM \_ SETWIZBUTTONS** 訊息修改後，即使已選取新的頁面。 一般而言，所有 [PSN \_ advanced.field.setactive](psn-setactive.md) 處理常式都會傳送此訊息，以確保每個頁面都有正確的按鈕狀態。

您可以隨時變更此訊息的按鈕狀態。 例如，您可能想要一開始停用 [ **下一步]** 按鈕。 在使用者輸入所有必要的資訊之後，您可以傳送其他的 [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) 訊息來啟用 [ **下一步]** 按鈕，並讓使用者繼續前往下一個頁面。

下列程式碼片段會使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來啟用內部頁面上的 [ **上一頁** **] 和 [下一頁]** 按鈕，然後再顯示它。


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>處理 PSN \_ WIZNEXT、PSNWIZBACK 和 PSN \_ WIZFINISH

按一下 **[下一步] 或 [** **上一頁** ] 按鈕時，您會收到 [PSN \_ WIZNEXT](psn-wiznext.md) 或 [PSN \_ WIZBACK](psn-wizback.md) 通知碼。 根據預設，嚮導會依照建立屬性工作表時所定義的順序，自動移至下一個或前一個頁面。 處理這些通知的常見原因是防止使用者切換頁面，或覆寫預設的頁面順序。

若要防止使用者切換頁面，請處理按鈕通知、呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式，並將 DWL \_ MSGRESULT 值設定為–1，並傳回 **TRUE**。 例如：


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



若要覆寫標準順序並移至特定頁面，請呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ，並將 DWL \_ MSGRESULT 值設定為頁面的對話方塊資源識別碼，並傳回 **TRUE**。 例如：


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



按一下 [ **完成]** 或 [ **取消** ] 按鈕時，您會分別收到 [PSN \_ WIZFINISH](psn-wizfinish.md) 或 [PSN \_ 重設](psn-reset.md) 通知碼。 當您按一下其中一個按鈕時，系統就會自動終結 wizard。 但是，如果您需要在嚮導終結之前執行清除工作，則可以處理這些通知。 若要防止在您收到 PSN WIZFINISH 通知時無法終結嚮導 \_ ，請呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ，並將 DWL \_ MSGRESULT 值設定為 **true**，並傳回 **true**。 例如：


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>回溯相容的嚮導

上一節假設您正在為具有 [第5版](common-control-versions.md) 或更新版本之通用控制項的系統，執行嚮導。

如果您要為具有舊版通用控制項的系統撰寫嚮導，將無法使用上一節所討論的許多功能。 只有通用控制項第5版和更新版本才支援 Wizard97 樣式所使用的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 和 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的一些成員。 不過，您仍然可以使用類似 Wizard97 樣式的外觀來執行回溯 *相容* 的 wizard。 若要這樣做，您必須明確地執行下列動作：

-   將浮水印圖形新增至 [簡介] 和 [完成] 頁面的對話方塊範本。
-   讓所有範本的大小都相同。 內部頁面沒有個別的系統定義標頭區域。
-   在您的範本上明確建立內部頁面的標頭區域。
-   請勿使用標頭圖形，因為如果 wizard 變更大小，它可能會與標題或子標題發生衝突。

如需回溯相容性檢查的進一步討論，請參閱回溯 [相容的 Wizard 97](/previous-versions//ms737910(v=vs.85))。

## <a name="remarks"></a>備註

如需 Wizard97 設計問題的完整討論，請參閱 Windows SDK 中其他位置的[Wizard97 規格](/previous-versions//ms738248(v=vs.85))。 本檔包含對話方塊的維度、點陣圖維度和色彩，以及控制項位置等專案的指導方針。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用屬性工作表](using-property-sheets.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
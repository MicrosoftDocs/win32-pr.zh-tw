---
title: 關於屬性工作表
description: 屬性工作表是一種視窗，可讓使用者查看和編輯專案的屬性。
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3256959b588e2109740033692c0c528889fc939f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "107001524"
---
# <a name="about-property-sheets"></a>關於屬性工作表

*屬性工作表* 是一種視窗，可讓使用者查看和編輯專案的屬性。 例如，試算表應用程式可以使用屬性工作表，讓使用者設定儲存格的字型和框線內容，或查看和設定裝置的屬性，例如磁片磁碟機、印表機或滑鼠。

本節將討論下列主題。

-   [屬性工作表基本概念](#property-sheet-basics)
-   [屬性工作表對話方塊](#property-sheet-dialog-boxes)
-   [頁面](#pages)
-   [建立屬性工作表](#property-sheet-creation)
-   [新增和移除頁面](#adding-and-removing-pages)
-   [屬性工作表標題和頁面標籤](#property-sheet-title-and-page-labels)
-   [頁面啟用](#page-activation)
-   [說明按鈕](#help-button)
    -   [移除標題列說明按鈕](#removing-the-caption-bar-help-button)
-   [[確定]、[取消] 和 [套用] 按鈕](#ok-cancel-and-apply-buttons)
-   [精靈](#wizards)

## <a name="property-sheet-basics"></a>屬性工作表基本概念

若要在您的應用程式中執行屬性工作表，請在您的專案中包含 Prsht.idl .h 標頭檔。 Prsht.idl 包含所有與屬性工作表搭配使用的識別碼。

屬性工作表包含一或多個重迭的子視窗，稱為頁面，每個都包含可設定相關屬性群組的控制項視窗。 例如，頁面可以包含設定專案之字型屬性的控制項，包括類型樣式、點大小、色彩等等。 每個頁面都有一個索引標籤，使用者可以選取此索引標籤，讓頁面進入屬性工作表的前景。 例如，Date-Time [控制台] 應用程式會顯示下列屬性工作表。

![具有兩個索引標籤之屬性工作表的螢幕擷取畫面，其中一個顯示時鐘和每月行事曆控制項](images/propsheet1.png)

具有多個索引標籤式頁面的標準屬性工作表，可讓使用者隨機存取所有屬性。 如果更適合依序設定屬性，您可以使用 [嚮導](#wizards)。

## <a name="property-sheet-dialog-boxes"></a>屬性工作表對話方塊

屬性工作表和它所包含的頁面實際上是對話方塊。 屬性工作表是系統定義的對話方塊，可管理頁面並為其提供共同的容器。 屬性工作表對話方塊可以是強制回應或非模式。 它包含框架、標題列和四個按鈕： **[確定]、[****取消**]、[套用] 和 [ (選擇性 **地) 說明**]。  頁面的對話方塊程式在使用者按一下按鈕時，會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式接收通知碼。

> [!NOTE]  
> 並非本節中的所有資訊都適用于具有稍微不同外觀和行為的 [嚮導]。 例如，嚮導有一組不同的按鈕和沒有索引標籤。 如需詳細資訊，請參閱 [建立嚮導](wizards.md)。

屬性工作表中的每個頁面都是一個應用程式定義的非強制回應對話方塊，可管理用來查看和編輯專案屬性的控制項視窗。 您可以提供用來建立每個頁面的對話方塊範本，以及管理控制項的對話方塊程式以及設定對應專案的屬性。

當頁面取得或遺失啟用時，以及當使用者按一下 [**確定]** **、[****取消**]、[套用] 或 [說明]**按鈕時**，屬性工作表會將通知碼傳送給頁面的對話方塊程式。 通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 *LParam* 參數是 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的位址，其中包含 [屬性工作表] 對話方塊的視窗控制碼。

某些通知碼需要頁面傳回 **TRUE** 或 **FALSE** ，以回應 [**WM \_ 通知**](wm-notify.md) 訊息。 若要這樣做，頁面必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式，將 [頁面] 對話方塊的 [ **DWL \_ MSGRESULT** ] 值設定為 [ **TRUE** ] 或 [ **FALSE**]。

## <a name="pages"></a>頁面

屬性工作表必須包含至少一個頁面，但它不能包含超過 **MAXPROPPAGES** 的值，如 Windows 標頭檔中所定義。 每個頁面都有以零為基底的索引，屬性工作表會根據頁面加入至屬性工作表的順序來指派這些索引。 索引會用於您傳送至屬性工作表的訊息中。

屬性頁可以包含嵌套的對話方塊。 如果有的話，您必須在最上層的對話方塊中包含 [**WS \_ EX \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) 樣式，並使用父對話方塊的控制碼來呼叫 [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) 函數。 這可確保使用者可以使用助憶鍵和對話方塊導覽鍵，將焦點移至嵌套對話方塊中的控制項。

每個頁面都有對應的圖示和標籤。 屬性工作表會建立每個頁面的索引標籤，並在索引標籤中顯示圖示和標籤。所有屬性工作表頁面都應該使用 nonbold 字型。 若要確保字型不是粗體，請在對話方塊範本中指定 **DS \_ 3DLOOK** 樣式。

頁面的對話方塊程式不能呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函數。 這麼做會摧毀整個屬性工作表，而不只是頁面。

屬性工作表頁面的最小大小為212對話單位水準和114對話方塊單位。 如果頁面對話方塊小於此值，則會放大頁面，直到它符合大小下限為止。 Prsht.idl 標頭檔包含屬性工作表頁面的三組建議大小，如下表所示。

|  大小                |   Description                                                   |
|----------------------|-----------------------------------------------------------------|
| **\_SM \_ CXDLG**  | 小型屬性工作表頁面的寬度（以對話方塊單位為單位）。         |
| **\_SM \_ CYDLG**  | 小型屬性工作表頁面的高度（以對話方塊單位）。        |
| **主張 \_ MED-V \_ CXDLG** | 中型屬性工作表頁面的寬度（以對話方塊單位為單位）。  |
| **主張 \_ MED-V \_ CYDLG** | 中型屬性工作表頁面的高度（以對話方塊單位）。 |
| **\_LG \_ CXDLG 的**  | 大型屬性工作表頁面的寬度（以對話方塊單位）。         |
| **\_LG \_ CYDLG 的**  | 大型屬性工作表頁面的高度（以對話方塊單位）。        |

使用這些建議的大小將有助於確保您的應用程式與其他 Microsoft Windows 應用程式之間的視覺化一致性。

在 Microsoft Visual Studio 資源編輯器中，您可以在 [ **新增資源** ] 對話方塊中建立適當大小的頁面。 展開對話方塊節點，然後選取 [ **idd \_ PROPPAGE \_ 大型**、 **idd \_ PROPPAGE \_ 媒體** 或 **idd \_ PROPPAGE \_**]。

屬性工作表會自動調整大小以容納最大的頁面。

## <a name="property-sheet-creation"></a>建立屬性工作表

建立屬性工作表之前，您必須定義一或多個頁面。 這牽涉到以頁面的相關資訊（其圖示、標籤、對話方塊範本、對話方塊程式等）填滿 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構，然後在 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函數的呼叫中指定結構的位址。 函數會傳回可唯一識別頁面之 HPROPSHEETPAGE 類型的控制碼。

若要建立屬性工作表，您可以在 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)函數的呼叫中指定 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的位址。 結構會定義屬性工作表的圖示和標題，也會包含您使用 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)取得之 HPROPSHEETPAGE 控制碼陣列的位址。 當 **PropertySheet** 建立屬性工作表時，它會包含陣列中所識別的頁面。 頁面會以它們包含在陣列中的相同順序出現在屬性工作表中。

將頁面指派給屬性工作表的另一種方式是指定 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的陣列，而不是 **HPROPSHEETPAGE** 控點的陣列。 在此情況下， [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 會建立頁面的控制碼，然後將它們加入至屬性工作表。

建立頁面時，其對話方塊程式會收到 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。 訊息的 *lParam* 參數是在建立頁面時所定義之 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構的複本指標。 尤其是當建立頁面時，結構的 **lParam** 成員可以用來將應用程式定義的資訊傳遞給對話方塊程式。 除了 **lParam** 成員之外，此結構必須視為唯讀。 修改 **lParam** 以外的任何作業將會產生無法預期的結果。

當系統接著將頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md) 結構複本傳遞至您的應用程式時，它會使用相同的指標。 將會傳遞結構的任何變更。 由於系統會忽略 **lParam** 成員，因此可加以修改以將資訊傳送至應用程式的其他部分。 例如，您可以使用 **lParam** 將資訊傳遞至頁面的 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函數。

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 會自動設定屬性工作表的大小和初始位置。 位置是以主控視窗的位置為基礎，而大小則是根據建立屬性工作表時，在頁面陣列中所指定的最大頁面。 如果您希望頁面符合屬性工作表底部四個按鈕的寬度，請將最寬頁面的寬度設定為190對話單位。

屬性工作表的大小是從資源檔中對話方塊範本的 [ *寬度* ] 和 [ *高度* ] 屬性計算而得。 如需進一步的詳細資料，請參閱 [**對話方塊資源**](/windows/desktop/menurc/dialog-resource) 或 [**DIALOGEX 資源**](/windows/desktop/menurc/dialogex-resource) 。 不過請注意，基於相容性考慮，維度的計算方式相對於 MS Shell Dlg 字型，而不是頁面使用的字型。 如果您設計使用其他字型的頁面，則可以使用下列其中一個建議。

-   調整對話方塊範本的維度，以彌補 MS Shell Dlg 字型和頁面實際使用的字型之間的差異大小差異。 例如，如果您選擇的字型寬度和 MS Shell Dlg 的寬度兩倍，則將對話方塊範本的 width 屬性設定為一般使用的兩倍。
-   使用 [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) 範本並設定 [ **DS \_ SHELLFONT** ] 對話方塊樣式。 在這種情況下，屬性工作表管理員會根據對話方塊範本所使用的字型，來解讀對話方塊範本的維度。

## <a name="adding-and-removing-pages"></a>新增和移除頁面

建立屬性工作表之後，應用程式可以藉由傳送 [**PSM \_ ADDPAGE**](psm-addpage.md) 訊息，將頁面加入至現有頁面集的結尾。 若要在現有的頁面之間插入頁面，請傳送 [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) 訊息。 請注意，屬性工作表的大小在建立之後就無法變更。 任何加入或插入的頁面都不能大於目前在屬性工作表中的最大頁面。 若要移除頁面，請傳送 [**PSM \_ REMOVEPAGE**](psm-removepage.md) 訊息。

當您定義頁面時，可以指定 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 回呼函式的位址，當屬性工作表正在建立或移除頁面時，會呼叫該函式。 使用 *PropSheetPageProc* 可讓您有機會執行個別頁面的初始化和清除作業。

> [!NOTE]  
> 當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。 當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。 請勿在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)的執行中新增、插入或移除頁面，或處理下列通知和 Windows 訊息。
>
> -   [PSN \_ APPLY](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [PSN \_ 重設](psn-reset.md)
> -   [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)

如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 正在運作時，需要修改屬性工作表頁面，請張貼私用 Windows 訊息。 在內容工作表管理員完成工作之後，您的應用程式就不會收到該訊息，此時修改頁面清單是安全的。

當屬性工作表已損毀時，它會自動終結已新增至其中的所有頁面。 這些頁面會以反向順序從用來建立頁面的陣列中所指定的順序來銷毀。 若要終結 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式所建立但未加入至屬性工作表的頁面，請使用 [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) 函數。

## <a name="property-sheet-title-and-page-labels"></a>屬性工作表標題和頁面標籤

您可以在用來建立屬性工作表的 [**PROPSHEETHEADER**](pss-propsheetheader.md) 結構中指定屬性工作表的標題。 如果 **dwFlags** 成員包含 **PSH \_ PROPTITLE** 值，屬性工作表會根據版本，新增尾碼 "properties" 或 "properties for" 的前置詞。 您可以使用 [**PSM \_ SETTITLE**](psm-settitle.md) 訊息來變更屬性工作表之後的標題。 在 Aero Wizard 中，此訊息可以用來動態變更內部頁面的標題。

根據預設，屬性工作表會使用對話方塊範本中指定的名稱字串做為頁面的標籤。 您可以在定義頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **dwFlags** 成員中包含 **PSP \_ USETITLE** 值，藉以覆寫名稱字串。 指定 **PSP \_ USETITLE** 時， **pszTitle** 成員必須包含頁面的標籤字串位址。

## <a name="page-activation"></a>頁面啟用

屬性工作表一次只能有一個使用中的頁面。 具有啟用的頁面會在頁面的重迭堆疊的前景。 使用者藉由選取索引標籤來啟用頁面;應用程式會使用 [**PSM \_ SETCURSEL**](psm-setcursel.md) 訊息來啟動頁面。

屬性工作表會將 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼傳送至即將失去啟用的頁面。 為了回應，頁面必須驗證使用者對頁面所做的任何變更。 如果頁面在遺失啟用之前需要額外的使用者輸入，請使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數將頁面的 **DWL \_ MSGRESULT** 值設定為 **TRUE**。 此外，頁面必須顯示描述問題的訊息方塊，並提供建議的動作。 如果沒有啟用，請將 **DWL \_ MSGRESULT** 設定為 **FALSE** 。

在取得啟用的頁面顯示之前，屬性工作表會將 [PSN \_ advanced.field.setactive](psn-setactive.md) 通知程式碼傳送至頁面。 頁面必須藉由初始化其控制項視窗來回應。

## <a name="help-button"></a>說明按鈕

屬性工作表可以顯示兩個 [說明] 按鈕：顯示在畫面底部的 [屬性工作表說明] 按鈕、[**確定** 取消套用] 按鈕旁邊， /  / 以及提供即時線上說明的標準標題列按鈕。

[屬性工作表說明] 按鈕是選擇性的，可以逐頁啟用。 若要顯示一或多個頁面的屬性工作表說明按鈕：

-   在屬性工作表 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **dwFlags** 成員中設定 **PSH \_ HASHELP** 旗標。
-   針對將顯示 [說明] 按鈕的每個頁面，在頁面的 [**PROPSHEETPAGE**](pss-propsheetpage.md)結構的 **dwFlags** 成員中設定 **PSP \_ HASHELP** 旗標。

當使用者按一下 [說明] 按鈕時，使用中的頁面會收到 [PSN \_ ](psn-help.md) 說明通知碼。 頁面必須藉由顯示說明資訊（通常是藉由呼叫 [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) 函數）來回應。

### <a name="removing-the-caption-bar-help-button"></a>移除標題列說明按鈕

依預設會顯示 [標題列說明] 按鈕，讓 [確定]/[取消]/[套用] 按鈕一律可以使用即時線上說明。 不過，您可以視需要移除此按鈕。 若要移除屬性工作表的標題列說明按鈕：

-   針對 [5.80 版](common-control-versions.md)之前的通用控制項版本，您必須先執行 [**屬性工作表回呼函數**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)。
-   針對 [5.80 版](common-control-versions.md)和更新版本的通用控制項，您可以直接 \_ 在屬性工作表 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **dwFlags** 成員中設定 PSH NOCONTEXTHELP 旗標。 但是，如果您需要與舊版通用控制項版本的回溯相容性，則必須執行回呼函數。

若要執行可移除標題列說明按鈕的屬性工作表回呼函式：

-   在屬性工作表 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **dwFlags** 成員中設定 **PSH \_ USECALLBACK** 旗標。
-   設定 [**PROPSHEETHEADER**](pss-propsheetheader.md)結構的 **pfnCallBack** 成員，以指向回呼函數。
-   執行回呼函數。 當此函式收到 **PSCB \_ PRECREATE** 訊息時，它也會收到屬性工作表對話方塊範本的指標。 從這個範本移除 **DS \_ CONTEXTHELP** 樣式。

下列範例說明如何執行這類回呼函數：

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

如果未定義 [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) 結構，請包含下列宣告：

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>[確定]、[取消] 和 [套用] 按鈕

[ **確定]** **和 [** 套用] 按鈕類似;這兩個屬性工作表的頁面都會直接驗證並套用使用者所做的屬性變更。 唯一的差別是按一下 [ **確定]** 按鈕會在套用變更之後，將屬性工作表損毀。

當使用者按一下 [ **確定]** 或 **[** 套用] 按鈕時，屬性工作表會將 [PSN 的 \_ KILLACTIVE](psn-killactive.md) 通知傳送至使用中的頁面，讓它有機會驗證使用者的變更。 如果變更有效，頁面必須呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數，並將 **DWL \_ MSGRESULT** 值設定為 **FALSE**。 如果使用者的變更無效，頁面必須將 **DWL \_ MSGRESULT** 設定為 **TRUE** ，並顯示對話方塊來通知使用者問題。 頁面會保持作用中，直到它將 **DWL \_ MSGRESULT** 設定為 **FALSE** ，以回應 PSN \_ KILLACTIVE 訊息。

在頁面透過將 **DWL \_ MSGRESULT** 設定為 **FALSE** 來回應 [PSN \_ KILLACTIVE](psn-killactive.md)通知之後，屬性工作表會將 PSN 套用 [通知 \_](psn-apply.md)傳送至每個頁面。 當頁面收到此通知時，它必須將新的屬性套用至對應的專案。 若要向屬性工作表指出變更對頁面有效，請呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) ，並將 **DWL \_ MSGRESULT** 設定為 **PSNRET \_ >aad-userreadusingalternativesecurityid-noerror**。 如果變更對頁面無效，則傳回錯誤。 這樣做可防止屬性工作表被終結，並將焦點傳回至收到 PSN 的頁面套用 \_ 通知，或是在按下 [套用] 按鈕時 ，將焦點放在頁面上。 若要傳回錯誤並指出將獲得焦點的頁面，請將 **DWL \_ MSGRESULT** 設定為下列其中一個值。

-   **PSNRET \_無效**。 將不會終結屬性工作表，而且焦點將會傳回此頁面。
-   **PSNRET \_不正確 \_ NOCHANGEPAGE**。 將不會終結屬性工作表，而且焦點會在按下按鈕時，傳回具有焦點的頁面。

應用程式可以使用 [**PSM 套用 \_**](psm-apply.md) 訊息來 **模擬 [套用] 按鈕的** 選取專案。

當頁面變成使用中狀態時 **，[套用** ] 按鈕一開始是停用狀態，表示尚未套用任何屬性變更。 當頁面透過其控制項的其中一個控制項收到輸入時，表示使用者已編輯屬性，該頁面必須將 [**PSM \_ 變更**](psm-changed.md) 的訊息傳送至屬性工作表。 此訊息會讓屬性工作表啟用 [套用 **] 按鈕。** 如果使用者之後 **按一下 [套用** ] 或 [ **取消** ] 按鈕，頁面必須重新初始化其控制項，然後傳送 [**PSM \_ 未**](psm-unchanged.md) 變更的訊息，以再次停 **用 [套用** ] 按鈕。

有時候 [套用 **] 按鈕會** 讓頁面變更屬性工作表，而且變更無法復原。 發生這種情況時，頁面必須將 [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) 訊息傳送至屬性工作表。 此訊息會讓屬性工作表將 [ **確定]** 按鈕的文字變更為 [關閉]，表示無法取消套用的變更。

有時候，頁面會變更系統組態，需要重新開機 Windows 或重新開機系統，變更才會生效。 進行這類變更之後，頁面必須將 [**psm \_ RESTARTWINDOWS**](psm-restartwindows.md) 或 [**psm \_ REBOOTSYSTEM**](psm-rebootsystem.md) 訊息傳送至屬性工作表。 這些訊息會在屬性工作表終結之後，使 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式傳回 **Id \_ PSRESTARTWINDOWS** 或 **id \_ PSREBOOTSYSTEM** 值。

當使用者按一下 [ **取消** ] 按鈕時，屬性工作表會將 [PSN \_ 重設](psn-reset.md) 通知程式碼傳送至所有頁面，指出即將終結屬性工作表。 頁面必須使用通知以執行清除作業。

## <a name="wizards"></a>精靈

Wizard 是一種特殊類型的屬性工作表。 嚮導的設計目的是要以應用程式所控制的順序，一次顯示一個頁面。 使用者不需要按一下索引標籤從一組頁面中選取，只要按下按鈕，就可以在序列中向前及向後流覽一頁。 例如，下列螢幕擷取畫面顯示 [新增硬體嚮導] 中的 [歡迎使用] 頁面：

![wizard [歡迎使用] 頁面的螢幕擷取畫面](images/wizard97.png)

下列螢幕擷取畫面顯示 Aero Wizard 的第一頁，也就是 Windows Vista 中引進的新樣式。

![aero wizard 第一頁的螢幕擷取畫面](images/wizardaero.png)

如需完整的完整討論，請參閱 [建立嚮導](wizards.md) 。

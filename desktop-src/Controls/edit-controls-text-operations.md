---
title: 編輯控制項文字作業
description: 系統會自動處理所有使用者起始的文字作業，並在作業完成時通知應用程式。
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9640616cf70b9a2933ef9d4c3fdb2accbfdcabf0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024155"
---
# <a name="edit-control-text-operations"></a>編輯控制項文字作業

系統會自動處理所有使用者起始的文字作業，並在作業完成時通知應用程式。

下列主題將討論使用者起始的文字操作和應用程式的回應：

-   [選取編輯控制項](#selecting-an-edit-control)
-   [設定和取出文字](#setting-and-retrieving-text)
-   [選取文字](#selecting-text)
-   [取代文字](#replacing-text)
-   [變更編輯控制項所使用的字型](#changing-the-font-used-by-an-edit-control)
-   [剪下複製貼上和清除作業](#cut-copy-paste-and-clear-operations)
-   [修改文字](#modifying-text)
-   [限制使用者輸入的文字](#limiting-user-entered-text)
-   [字元和行作業](#character-and-line-operations)
-   [在編輯控制項中滾動文字](#scrolling-text-in-an-edit-control)
-   [設定制表位和邊界](#setting-tab-stops-and-margins)
-   [隱藏使用者輸入](#concealing-user-input)
-   [使用整數](#using-integers)
-   [復原文字作業](#undoing-text-operations)
-   [處理 Wordwrap 和換行](#handling-wordwrap-and-line-breaks)
-   [取出點和字元](#retrieving-points-and-characters)
-   [自動完成字串](#autocompletion-of-strings)
-   [編輯控制項中的複雜字集](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>選取編輯控制項

使用者可以選取編輯控制項，方法是按一下滑鼠或按下 TAB 鍵移至該控制項。 Tab 鍵方法是系統所提供的預先定義鍵盤介面的一部分。 如需此介面的完整描述，請參閱 [對話方塊](/windows/desktop/dlgbox/dialog-boxes)。 當使用者選取編輯控制項時，系統會將鍵盤焦點提供給控制項， (在) [鍵盤輸入](/windows/desktop/inputdev/about-keyboard-input) 中看到「鍵盤焦點和啟用」，並使用反向影片來反白顯示其文字。

## <a name="setting-and-retrieving-text"></a>設定和取出文字

應用程式可以使用 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) 函式、 [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) 函式，或將控制項傳送至 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息，來設定編輯控制項的文字。

若要從編輯控制項取出所有文字，請先使用 [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) 函式或 [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) 訊息來判斷包含文字所需的緩衝區大小。 接下來，使用 [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) 函式、 [**GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) 函式或 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息來取得文字。

## <a name="selecting-text"></a>選取文字

選取編輯控制項之後，使用者就可以使用滑鼠或鍵盤選取控制項中的文字。 應用程式可以藉由傳送 [**EM \_ GETSEL**](em-getsel.md) 訊息給控制項，來取出編輯控制項中目前選取範圍的開始和結束字元位置。 結束位置的傳回值會大於選取範圍中的最後一個字元 (也就是最後一個選取的字元) 之後第一個字元的位置。

應用程式也可以在編輯控制項中選取文字，方法是使用選取範圍的開頭和結尾字元索引來傳送 [**EM \_ SETSEL**](em-setsel.md) 訊息給控制項。 例如，應用程式可以使用 **em \_ SETSEL** 搭配 [**em \_ REPLACESEL**](em-replacesel.md) 來刪除編輯控制項中的文字。

這三個訊息適用于單行和多行編輯控制項。

## <a name="replacing-text"></a>取代文字

應用程式可以在編輯控制項中取代選取的文字，方法是將具有取代文字指標的 [**EM \_ REPLACESEL**](em-replacesel.md) 訊息傳送給控制項。 如果沒有目前的選取範圍， **EM \_ REPLACESEL** 會在插入點插入取代文字。 如果取代文字超過可用的記憶體，應用程式可能會收到 [EN \_ ERRSPACE](en-errspace.md) 通知碼。 這則訊息適用于單行和多行編輯控制項。

應用程式可以使用 [**EM \_ REPLACESEL**](em-replacesel.md) 來取代編輯控制項文字的一部分，或使用 [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) 函式來取代它的所有部分。

## <a name="changing-the-font-used-by-an-edit-control"></a>變更編輯控制項所使用的字型

應用程式可以藉由傳送 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息來變更編輯控制項所使用的字型。 大部分的應用程式會在處理 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息時這麼做。 變更字型不會變更編輯控制項的大小;傳送 **WM \_ SETFONT** 訊息的應用程式可能必須取得文字的字型計量，並重新計算編輯控制項的大小。 如需字型和字型度量的詳細資訊，請參閱字型 [和文字](/windows/desktop/gdi/fonts-and-text)。

## <a name="cut-copy-paste-and-clear-operations"></a>剪下複製貼上和清除作業

在編輯控制項和剪貼簿之間移動文字有四個訊息。 如果有任何) 從編輯控制項複製到剪貼簿，而不是從編輯控制項刪除，則會將目前的選取範圍複製 (。 [**\_**](/windows/desktop/dataxchg/wm-copy) 如果編輯控制項中有任何) ，然後將已刪除的文字複製到剪貼簿，則 [ [**WM \_ 剪**](/windows/desktop/dataxchg/wm-cut) 下] 訊息會刪除目前的選取範圍 (。 如果有任何) 來自編輯控制項，則 [ [**WM \_ 清除**](/windows/desktop/dataxchg/wm-clear) ] 訊息會刪除目前的選取範圍 (，但除非使用者按下 SHIFT 鍵) ，否則不會將它複製到剪貼簿 (。 [**WM \_ 貼**](/windows/desktop/dataxchg/wm-paste)上訊息會將剪貼簿中的文字複製到插入點的編輯控制項。 這四個訊息適用于單行和多行編輯控制項。

Microsoft Windows NT 4.0 和更新版本：編輯控制項包含內建的內容功能表，可讓使用者輕鬆地在編輯控制項和剪貼簿之間移動文字。 當使用者以滑鼠右鍵按一下控制項時，就會顯示內容功能表。 內容功能表中的命令包括 [**復原**]、[**剪** 下]、[**複製**]、[**貼** 上]、[**刪除**] 和 [全 **選**

## <a name="modifying-text"></a>修改文字

使用者可以選取、刪除或移動編輯控制項中的文字。 系統會維護每個編輯控制項的內部旗標，指出是否已修改控制項的內容。 系統會在建立控制項時清除此旗標，並在每次修改控制項中的文字時設定旗標。 應用程式可以藉由傳送 [**EM \_ GETMODIFY**](em-getmodify.md) 訊息的控制權來取得修改旗標。 然後，應用程式可以藉由傳送 [**EM \_ SETMODIFY**](em-setmodify.md) 訊息的控制權來設定或清除修改旗標。 這些訊息適用于單行和多行編輯控制項。

## <a name="limiting-user-entered-text"></a>限制使用者輸入的文字

使用者可以在編輯控制項中輸入的文字數量預設限制為 32 KB。 應用程式可以藉由傳送 [**EM \_ SETLIMITTEXT**](em-setlimittext.md) 訊息的控制權來變更預設限制。 這則訊息會設定使用者可以輸入至編輯控制項的位元組數目的固定限制，但不會影響在傳送訊息時，以及 [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) 函式或 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息複製到控制項中的文字。 例如，假設應用程式使用 **SetDlgItemText** 函式在編輯控制項中放置500個位元組，而使用者也輸入500個位元組， (1000 個位元組總計) 。 如果應用程式接著傳送 **EM \_ SETLIMITTEXT** 訊息，將使用者輸入的文字限制為300個位元組，則編輯控制項中的1000位元組仍會保留在該處，而且使用者也無法再加入任何文字。 另一方面，如果應用程式傳送 **EM \_ SETLIMITTEXT** 訊息將使用者輸入的文字限制為1300個位元組，則會保留1000個位元組，但使用者可以增加300個位元組。

當使用者達到編輯控制項的字元限制時，系統會傳送包含 [EN \_ MAXTEXT](en-maxtext.md)通知碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息給應用程式。 此通知碼不表示記憶體已用盡，但已達到使用者輸入文字的限制;使用者無法輸入任何文字。 若要變更此限制，應用程式必須以較高的限制將新的 [**EM \_ SETLIMITTEXT**](em-setlimittext.md) 訊息傳送給控制項。

使用 [**EM \_ SETLIMITTEXT**](em-setlimittext.md) 和 [EN \_ MAXTEXT](en-maxtext.md)的範例，假設應用程式必須在編輯控制項中將使用者限制為不超過四個字元。 應用程式會使用 **EM \_ SETLIMITTEXT** 來指定四個字元的限制。 如果使用者嘗試輸入第五個字元，系統會將 EN \_ MAXTEXT 通知碼傳送給應用程式。

## <a name="character-and-line-operations"></a>字元和行作業

有幾個訊息會傳回編輯控制項中的字元和行的相關資訊。 大部分的訊息會傳回索引（通常是以零為基底的數位）來參考字元或行。 例如，在包含 n 個字元的單行編輯控制項中，行索引為零，而字元是從零到 n-1 的索引。 在包含 m 行和 n 個字元的多行編輯控制項中，這些行會從零到 m-1 編制索引，而字元的索引則是從零到 n-1。 請注意，字元索引會忽略換行字元。

應用程式可以將 [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) 訊息傳送至編輯控制項，以判斷編輯控制項中的字元數。 此訊息會傳回單行或多行編輯控制項中文字的長度（以字元為單位） (不包括結束的 null 字元) ）。 [**EM \_ LINELENGTH**](em-linelength.md)訊息會以字元為單位傳回該行中字元索引所指定的行長度（以字元為單位）。 傳回的長度不包含任何選取的字元。 應用程式可以在單行或多行編輯控制項中使用這些訊息。

[**EM \_ GETFIRSTVISIBLELINE**](em-getfirstvisibleline.md)訊息會傳回多行編輯控制項中最上層可見行的以零為起始的索引，或單行編輯控制項中第一個可見字元的以零為基底的索引。 應用程式可以將 [**EM \_ GETLINE**](em-getline.md) 訊息傳送至編輯控制項，以從編輯控制項將一行複製到緩衝區。 該行是由其行索引所指定，而接收緩衝區的第一個單字則包含要複製到緩衝區的最大位元組數目。 傳回值是複製的位元組數目。 此訊息也可用於單行或多行編輯控制項。

有唯一的訊息可用來傳回多行編輯控制項中某一行的相關資訊。 [**EM \_ GETLINECOUNT**](em-getlinecount.md)訊息會傳回編輯控制項中的行數。 [**EM \_ LINEFROMCHAR**](em-linefromchar.md)訊息會傳回包含指定字元索引的行索引。 [**EM \_ LINEINDEX**](em-lineindex.md)訊息會傳回指定行中第一個字元的索引。

## <a name="scrolling-text-in-an-edit-control"></a>在編輯控制項中滾動文字

若要在編輯控制項中執行滾動功能，您可以使用 [編輯控制項類型和樣式](about-edit-controls.md)中所討論的自動滾動樣式，也可以明確地在編輯控制項中加入捲軸。 若要加入水準捲軸，請使用樣式 WS \_ HSCROLL; 若要加入垂直捲動條，請使用樣式 [**ws \_ VSCROLL**](/windows/desktop/winmsg/window-styles)。 具有捲軸的編輯控制項會處理自己的捲軸訊息。 如需加入捲軸以編輯控制項的詳細資訊，請參閱 [捲軸](scroll-bars.md)。

系統會提供三個訊息，讓應用程式可以使用捲軸傳送至編輯控制項。 [**EM \_ LINESCROLL**](em-linescroll.md)訊息可以垂直和水準地滾動多行編輯控制項。 *LParam* 參數會指定從目前的行垂直垂直捲動的行數，而 *wParam* 參數指定要水準滾動的字元數（從目前的字元開始）。 如果有 [**es \_ CENTER**](edit-control-styles.md) 或 [**es \_ 許可權**](edit-control-styles.md) 樣式，則編輯控制項不會認可水準滾動消息。 **EM \_ LINESCROLL** 訊息只適用于多行編輯控制項。

[**EM \_ 滾動**](em-scroll.md)條訊息會垂直捲動多行編輯控制項。 *WParam* 參數會指定滾動動作。 **EM \_ 滾動** 條訊息只適用于多行編輯控制項。 **EM \_滾動** 條的效果與 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息相同。

[**EM \_ SCROLLCARET**](em-scrollcaret.md)訊息會將插入號滾動至編輯控制項中的 view。

## <a name="setting-tab-stops-and-margins"></a>設定制表位和邊界

應用程式可以使用 [**EM \_ SETTABSTOPS**](em-settabstops.md) 訊息，在多行編輯控制項中設定制表位。  (定位停駐點的預設值為8個字元。 ) 當應用程式將文字加入編輯控制項時，文字中的定位字元會自動產生空間，直到下一個索引標籤停止為止。 **EM \_ SETTABSTOPS** 訊息不會自動造成系統重繪文字。 若要這樣做，應用程式可以呼叫 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) 函數。 **EM \_ SETTABSTOPS** 訊息只適用于多行編輯控制項。

應用程式可以使用 [**EM \_ SETMARGINS**](em-setmargins.md) 訊息來設定編輯控制項的左邊界和右邊界的寬度。 傳送此訊息之後，系統會重新繪製編輯控制項以反映新的邊界設定。 應用程式可以藉由傳送 [**EM \_ GETMARGINS**](em-getmargins.md) 訊息來取得左右邊界的寬度。 根據預設，編輯控制項邊界的寬度足以容納最大的字元水準懸垂 (負 ABC 寬度) 用於編輯控制項中目前的字型。

## <a name="concealing-user-input"></a>隱藏使用者輸入

應用程式可以使用編輯控制項中的密碼字元來隱藏使用者輸入。 設定密碼字元時，會顯示該字元來取代使用者輸入的每個字元。 移除密碼字元時，控制項會顯示使用者所輸入的字元。 如果應用程式使用 style [**ES \_ 密碼**](edit-control-styles.md)建立單行編輯控制項，則預設密碼字元是星號 (\*) 。 應用程式可以使用 [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) 訊息來移除或定義不同的密碼字元，並使用 [**em \_ GETPASSWORDCHAR**](em-getpasswordchar.md) 訊息來取出目前的密碼字元。 這些訊息只適用于單行編輯控制項。

## <a name="using-integers"></a>使用整數

針對只包含數位的編輯控制項，有兩個整數轉換函數。 [**SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint)函式會 (簽署或未簽署的) 來建立指定之整數的字串表示，並將字串傳送至編輯控制項。 **SetDlgItemInt** 不會傳回任何值。 [**GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint)函式會從編輯控制項中的字串表示，建立整數 (簽署或未簽署的) 。 **GetDlgItemInt** 會傳回整數 (或) 的錯誤值。

## <a name="undoing-text-operations"></a>復原文字作業

每個編輯控制項都會維護一個復原旗標，指出應用程式是否可以反轉或復原編輯控制項上最近的作業， (復原文字刪除，例如) 。 編輯控制項會設定復原旗標，以指出作業可以復原並重設，以表示作業無法復原。 應用程式可以藉由傳送 [**EM \_ CANUNDO**](em-canundo.md) 訊息的控制權，判斷復原旗標的設定。

應用程式可以藉由將「 [**EM \_ 復原**](em-undo.md) 」訊息傳送給控制項，來復原最近的操作。 如果沒有任何其他編輯控制項作業會先發生，就可以復原操作。 例如，使用者可以刪除文字、取代文字 (復原刪除) ，然後再刪除文字， (復原取代) 。 **EM \_ 復原** 訊息適用于單行和多行編輯控制項，而且一律適用于單行編輯控制項。

應用程式可以傳送 [**EM \_ EMPTYUNDOBUFFER**](em-emptyundobuffer.md) 訊息給控制項，以重設編輯控制項的復原旗標。 每當編輯控制項收到 [**EM \_ SETHANDLE**](em-sethandle.md) 或 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息時，系統就會自動重設復原旗標。 [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta)函式會傳送 **WM \_ SETTEXT** 訊息。

## <a name="handling-wordwrap-and-line-breaks"></a>處理 Wordwrap 和換行

應用程式可以搭配多行編輯控制項使用 Wordwrap 函式，以找出應該包裝到下一行的單字或單字片段。 使用系統提供的預設 Wordwrap 函式時，行一律會以單字之間的空格結尾。 應用程式可以指定它自己的 Wordwrap 函式，方法是提供 [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) Wordwrap 函式，並傳送 [**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) 訊息給編輯控制項。 應用程式可以藉由傳送 [**EM \_ GETWORDBREAKPROC**](em-getwordbreakproc.md) 訊息給控制項，來取得目前 Wordwrap 函式的位址。

應用程式可以指示多行編輯控制項在換行字元 (兩個換行字元，以及在換行文字行的結尾自動) 換行字元。 應用程式可以藉由傳送編輯控制項的 [**EM \_ FMTLINES**](em-fmtlines.md) 訊息，開啟或關閉此功能。 這則訊息只適用于多行編輯控制項，而且不會影響以硬換行結尾的行 (一個換行字元和使用者) 輸入的換行字元。 此外，在多行編輯控制項中，應用程式可以指定 [**ES \_ WANTRETURN**](edit-control-styles.md) 樣式，要求系統在使用者按下 [編輯] 控制項中的 ENTER 鍵時，插入一個回車。

## <a name="retrieving-points-and-characters"></a>取出點和字元

若要判斷最接近編輯控制項工作區中指定點的字元，請將 [**EM \_ CHARFROMPOS**](em-charfrompos.md) 訊息傳送至控制項。 訊息會傳回最接近點的字元索引和字元的行索引。 同樣地，您可以藉由傳送 [**EM \_ POSFROMCHAR**](em-posfromchar.md) 訊息來取出指定字元的工作區座標。 訊息會傳回指定字元左上角的 x 和 y 座標。

## <a name="autocompletion-of-strings"></a>自動完成字串

自動完成會將已部分在編輯控制項中輸入的字串展開為完整字串。 例如，當使用者開始在 [Windows Internet Explorer] 工具列中內嵌的 [位址] 編輯控制項中輸入 URL 時，自動完成功能會將字串展開為一或多個與現有部分字串一致的完整 Url。 部分 URL 字串（例如 "mic"）可能會展開為 " https://www.microsoft.com " 或 " https://www.microsoft.com/windows "。 自動完成通常會與編輯控制項或具有內嵌編輯控制項的控制項一起使用。

如需詳細資訊，請參閱 [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) 和 [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) 介面檔。

## <a name="complex-script-in-edit-controls"></a>編輯控制項中的複雜字集

*複雜的腳本* 是一種語言，其列印表單未以簡單的方式配置。 例如，複雜的腳本可能會允許雙向轉譯、字型的內容成形，或合併字元。 標準編輯控制項已經過擴充，可支援多語系文字和複雜的腳本。 這不僅包括輸入和顯示，也包括正確的資料指標移動 (在泰文和梵文腳本中的字元叢集，例如) 。

妥善撰寫的應用程式會自動收到此支援，而不需要修改。 同樣地，您應該考慮加入由右至左讀取順序和靠右對齊的支援。 在此情況下，請切換編輯控制項視窗的擴充樣式旗標來控制這些屬性，如下列範例所示。


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



設定 **lAlign** 值之後，請設定 [編輯控制項] 視窗的擴充樣式，以啟用新的顯示，如下所示。


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe 是另一組函數，可提供精確的控制來處理複雜的腳本。 如需詳細資訊，請參閱 [Uniscribe](/windows/desktop/Intl/uniscribe)。

 

 
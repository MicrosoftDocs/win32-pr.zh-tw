---
title: 按鈕訊息
description: 按鈕可以將訊息傳送至其父視窗，而且父視窗可以將訊息傳送至按鈕。
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103684043"
---
# <a name="button-messages"></a>按鈕訊息

按鈕可以將訊息傳送至其父視窗，而且父視窗可以將訊息傳送至按鈕。

本節將討論下列主題。

-   [傳送訊息到按鈕](#sending-messages-to-buttons)
-   [處理按鈕的訊息](#handling-messages-from-a-button)
-   [來自按鈕的通知訊息](#notification-messages-from-buttons)
-   [按鈕色彩訊息](#button-color-messages)
-   [按鈕預設訊息處理](#button-default-message-processing)
-   [相關主題](#related-topics)

## <a name="sending-messages-to-buttons"></a>傳送訊息到按鈕

父視窗可以使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，將訊息傳送至重迭或子視窗中的按鈕，也可以使用 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)、 [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)、 [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)和 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數，將訊息傳送至對話方塊中的按鈕。

應用程式可以使用 [**BM \_ GETCHECK**](bm-getcheck.md) 訊息來取得核取方塊或選項按鈕的核取狀態。 應用程式也可以使用 [**BM \_ >getstate**](bm-getstate.md) 訊息來取得按鈕的目前狀態， (檢查狀態、推播狀態和焦點狀態) 。 若要取得特定狀態的相關資訊，請在傳回的狀態值上使用位元遮罩。

[**BM \_ SETCHECK**](bm-setcheck.md)訊息會設定核取方塊或選項按鈕的檢查狀態，而訊息則會傳回零。 [**BM \_ SETSTATE**](bm-setstate.md)訊息會設定按鈕的推送狀態; 此訊息也會傳回零。 [**BM \_ >setstyle**](bm-setstyle.md)訊息會變更按鈕的樣式。 它是專為變更類型內的按鈕樣式所設計 (例如，將核取方塊變更為自動核取方塊) 。 它並非設計來變更類型 (例如，將核取方塊變更為選項按鈕) 。 應用程式不應該將按鈕從一種類型變更為另一種類型。

[**BS \_ 點陣圖**](button-styles.md)或 [**BS \_ 圖示**](button-styles.md)樣式的按鈕會顯示點陣圖或圖示，而不是文字。 [**BM \_ SETIMAGE**](bm-setimage.md)訊息會將點陣圖或圖示的控制碼與按鈕產生關聯。 [**BM \_ GETIMAGE**](bm-getimage.md)訊息會抓取與按鈕相關聯之點陣圖或圖示的控制碼。

應用程式也可以使用 [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) 訊息，在對話方塊中取出預設推播按鈕控制項的識別碼。 應用程式可以使用 [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) 訊息來設定對話方塊的預設推送按鈕。

呼叫 [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) 或 [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) 函數相當於傳送 [**BM \_ SETCHECK**](bm-setcheck.md) 訊息。 呼叫 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數相當於傳送 [**BM \_ GETCHECK**](bm-getcheck.md) 訊息。

## <a name="handling-messages-from-a-button"></a>處理按鈕的訊息

按鈕的通知會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送。 您可以在每個通知的 [參考] 頁面中找到所使用訊息的相關資訊。

如需如何處理訊息的詳細資訊，請參閱 [控制訊息](control-messages.md)。 另請參閱按鈕訊息。

## <a name="notification-messages-from-buttons"></a>來自按鈕的通知訊息

當使用者按一下按鈕時，其狀態會變更，而按鈕會將通知碼（以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式）傳送至其父視窗。 例如，每當使用者選擇按鈕時，按鈕控制項會傳送 BN 按下的通知碼。 [ \_ ](bn-clicked.md) 在所有情況下 (除了 [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)) 之外， *wParam* 參數的低序位字包含控制項識別碼、 *wParam* 的高序位字包含通知碼，而 *lParam* 參數則包含控制視窗控制碼。

訊息和父視窗的回應都取決於按鈕的類型、樣式和目前狀態。 以下是應用程式應該監視和處理的按鈕通知代碼。



| 通知碼                                                        | Description                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | 滑鼠已進入或離開按鈕的工作區。 |
| [BN \_ 按一下](bn-clicked.md)                                            | 使用者按一下按鈕。                             |
| [BN \_DBLCLK](bn-dblclk.md) 或 [BN \_ DOUBLECLICKED](bn-doubleclicked.md) | 使用者按兩下按鈕。                      |
| [BN \_ DISABLE](bn-disable.md)                                            | 按鈕已停用。                                  |
| [BN \_已推送](bn-pushed.md) 或 [BN \_ HILITE](bn-hilite.md)               | 使用者按下按鈕。                              |
| [BN \_ KILLFOCUS](bn-killfocus.md)                                        | 按鈕失去鍵盤焦點。                    |
| [BN \_ 油漆](bn-paint.md)                                                | 應繪製按鈕。                          |
| [BN \_ SETFOCUS](bn-setfocus.md)                                          | 按鈕會取得鍵盤焦點。                  |
| [BN \_未推送](bn-unpushed.md) 或 [BN \_ UNHILITE](bn-unhilite.md)       | 此按鈕不會再推送。                        |



 

按鈕只會在具有 [**BN \_ 通知**](button-styles.md)樣式的情況下傳送 [BN \_ DISABLE](bn-disable.md)、 [BN \_ 推送](bn-pushed.md)、 [BN \_ KILLFOCUS](bn-killfocus.md)、 [BN \_ PAINT](bn-paint.md)、 [BN \_ SETFOCUS](bn-setfocus.md)和 [未推送 \_ BS](bn-unpushed.md)通知碼。 [BN \_DBLCLK](bn-dblclk.md) 通知碼會自動傳送給 [**BS \_ USERBUTTON**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕和 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕。 其他按鈕類型只有在 \_ 有 **BS \_ 通知** 樣式時，才會傳送 BN DBLCLK。 無論按鈕樣式為何，所有按鈕都會傳送 BN 的已按下通知碼。 [ \_ ](bn-clicked.md)

針對 [自動] 按鈕，系統會變更推送狀態並繪製按鈕。 在此情況下，應用程式通常只會處理按下的 [BN \_ ](bn-clicked.md) ，並 [BN \_ DBLCLK](bn-dblclk.md) 通知碼。 對於非自動的按鈕，應用程式通常會傳送訊息來變更按鈕的狀態，以回應通知碼。 如需將訊息傳送至按鈕的相關資訊，請參閱 [將訊息傳送至按鈕](#sending-messages-to-buttons)。

當使用者選取主控描繪按鈕時，按鈕會傳送包含要繪製之控制項識別碼的 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息，以及其維度和狀態的相關資訊。

## <a name="button-color-messages"></a>按鈕色彩訊息

系統會為按鈕提供預設的色彩值。 應用程式可以藉由呼叫 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 函式來取得這些色彩的預設值，或藉由呼叫 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 函數來設定值。 下表顯示預設的按鈕色彩值。



| 值               | 元素著色                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| 色彩 \_ BTNFACE      | 按鈕臉部。                                                                                                              |
| 色彩 \_ BTNHIGHLIGHT | 醒目提示區域 (按鈕的上方和左邊緣) 。                                                                       |
| 色彩 \_ BTNSHADOW    | 陰影區域 (按鈕的下邊緣和右邊緣) 。                                                                      |
| 色彩 \_ BTNTEXT      | 一般 (nongrayed 按鈕中) 文字。                                                                                       |
| 色彩 \_ GRAYTEXT     | 停用 (灰色) 按鈕中的文字。 如果目前的顯示驅動程式不支援純灰色色彩，此色彩會設為0。 |
| 色彩 \_ 視窗       | 視窗背景。                                                                                                        |
| 色彩 \_ WINDOWFRAME  | 窗框。                                                                                                             |
| 色彩 \_ WINDOWTEXT   | Windows 中的文字。                                                                                                           |



 

不過，呼叫 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 會影響所有的應用程式，因此您不應該呼叫此函式來自訂應用程式的按鈕。

系統會在繪製按鈕之前，將 [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) 訊息傳送至按鈕的父視窗。 此訊息包含按鈕之裝置內容的控制碼，以及子視窗的控制碼。 父視窗可以使用這些控點來變更按鈕的文字和背景色彩。 不過，只有主控描繪的按鈕會回應處理訊息的父視窗。

## <a name="button-default-message-processing"></a>按鈕預設訊息處理

預先定義之按鈕控制項視窗類別的視窗程式，會針對按鈕控制項程式未處理的所有訊息執行預設處理。 當 button control 程式針對任何訊息傳回 **FALSE** 時，預先定義的視窗程式會檢查訊息，並執行下表所列的預設動作。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>訊息</th>
<th>預設動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>將 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> 和 <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> 訊息傳送給按鈕，並將父視窗傳送 <a href="bn-clicked.md">BN_CLICKED</a> 的通知碼。</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>傳回按鈕的檢查狀態。</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>傳回與按鈕相關聯之點陣圖或圖示的控制碼，如果按鈕沒有點陣圖或圖示，則為 <strong>Null</strong> 。</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>傳回按鈕的目前檢查狀態、推播狀態和焦點狀態。</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>設定選項按鈕和核取方塊樣式的檢查狀態。 如果選項按鈕的 <em>wParam</em> 參數大於零，則按鈕會獲得 <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> 的樣式。</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>將指定的點陣圖或圖示控制碼與按鈕建立關聯，並將控制碼傳回至上一個點陣圖或圖示。</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>設定按鈕的推送狀態。 針對主控描繪按鈕，如果按鈕的狀態已變更，則會將 <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> 訊息傳送至父視窗。</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>設定按鈕樣式。 如果 <em>lParam</em> 參數的低序位字是 <strong>TRUE</strong>，則會重新繪製按鈕。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>當使用者按下加號 (+) 或等於 (=) 索引鍵時，檢查核取方塊或 [自動] 核取方塊。 當使用者按下減號 (-) 鍵時，清除核取方塊或 [自動] 核取方塊。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>繪製按鈕。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>清除擁有者繪製按鈕的背景。 其他按鈕的背景會在 <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> 中清除，並 <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> 處理。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>傳回值，這個值表示預設按鈕程式所處理的輸入類型，如下表所示。 
<table>
<thead>
<tr class="header">
<th>按鈕樣式</th>
<th>傳回</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS |DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON |DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS |DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON |DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON |DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON |DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>傳回目前字型的控制碼。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>如果使用者按下空格鍵，則推送按鈕。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>除了 TAB 鍵之外，也會釋放所有案例的滑鼠捕捉。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>從按鈕中移除焦點矩形。 針對推播按鈕和預設的推播按鈕，焦點矩形會失效。 如果按鈕具有滑鼠捕捉，則會釋出抓取，並不會按一下按鈕，而且會移除任何推送狀態。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>將 <a href="bn-dblclk.md">BN_DBLCLK</a> 通知程式碼傳送至選項按鈕和主控描繪按鈕的父視窗。 針對其他按鈕，按兩下會被視為 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> 的訊息來處理。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>如果滑鼠游標的位置在按鈕的用戶端矩形內，則會反白顯示按鈕。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>如果按鈕具有滑鼠捕捉，則放開滑鼠捕捉。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>如果按鈕具有滑鼠捕捉，則執行與 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>相同的動作。 否則，就不會執行任何動作。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>將任何 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕變成 <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> 按鈕。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>如果按鈕控制項是群組方塊，則會傳回 HTTRANSPARENT。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>根據按鈕的樣式和目前狀態繪製按鈕。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>在按鈕上繪製焦點矩形以取得焦點。 針對選項按鈕和自動選項按鈕，父視窗會傳送 <a href="bn-clicked.md">BN_CLICKED</a> 通知碼。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>設定新的字型，並選擇性地更新視窗。</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>設定按鈕的文字。 在群組方塊的案例中，訊息會繪製預先存在的文字，然後再以新的文字重新繪製群組方塊。</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>除了 TAB 鍵之外，也會釋放所有案例的滑鼠捕捉。</td>
</tr>
</tbody>
</table>



 

預先定義的視窗程式會將所有其他訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以進行預設處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制訊息](control-messages.md)
</dt> </dl>

 

 
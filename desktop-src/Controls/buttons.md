---
title: 按鈕 (Windows 控制項)
description: 本章節包含與按鈕控制項搭配使用之程式設計項目的相關資訊。 按鈕是使用者可以按一下來提供應用程式輸入的控制項。
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babe31ec9f11ee445167e57394da0fa88fd781dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464049"
---
# <a name="button-windows-controls"></a>按鈕 (Windows 控制項)

本章節包含與按鈕控制項搭配使用之程式設計項目的相關資訊。 *按鈕* 是使用者可以按一下來提供應用程式輸入的控制項。

### <a name="overviews"></a>概觀



| 主題                                       | 目錄                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [按鈕訊息](button-messages.md)      | 本主題討論與按鈕搭配使用的訊息。<br/>                                               |
| [按鈕狀態](button-states.md)          | 本節將討論如何選取按鈕來變更其狀態，以及應用程式應該如何回應。<br/> |
| [按鈕類型](button-types-and-styles.md) | 本主題討論不同類型的按鈕。<br/>                                                    |
| [使用按鈕](using-buttons.md)          | 本節說明如何執行與按鈕相關聯的是否有工作。<br/>                            |



 

### <a name="functions"></a>函式



| 主題                                            | 目錄                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | 變更按鈕控制項的檢查狀態。<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | 將核取記號新增至 (檢查群組中) 指定的選項按鈕，然後從 (清除核取記號，以) 清除群組中的所有其他選項按鈕。 <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)函式會決定是否核取按鈕控制項，或是否已核取、未選取或不定的三狀態按鈕控制項。 <br/> |



 

### <a name="macros"></a>巨集



| 主題                                                                         | 目錄                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**按鈕 \_ 啟用**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | 啟用或停用按鈕。<br/>                                                                                                                                                                                                          |
| [**按鈕 \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | 取得選項按鈕或核取方塊的檢查狀態。 您可以使用這個宏，或明確地傳送 [**BM \_ GETCHECK**](bm-getcheck.md) 訊息。 <br/>                                                                                       |
| [**按鈕 \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | 取得最適合文字和影像的按鈕大小（如果有影像清單的話）。 您可以使用此宏或明確地傳送 [**BCM \_ GETIDEALSIZE**](bcm-getidealsize.md) 訊息。 <br/>                                      |
| [**按鈕 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | 取得 [**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) 結構，描述為按鈕控制項設定的影像清單。 您可以使用此宏或明確地傳送 [**BCM \_ GETIMAGELIST**](bcm-getimagelist.md) 訊息。 <br/> |
| [**按鈕 \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | 取得與命令連結按鈕相關聯的備註文字。 您可以使用此宏或明確地傳送 [**BCM \_ GETNOTE**](bcm-getnote.md) 訊息。<br/>                                                                            |
| [**按鈕 \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | 取得可在命令連結的描述中顯示的附注文字長度。 使用這個宏或明確地傳送 [**BCM \_ GETNOTELENGTH**](bcm-getnotelength.md) 訊息。<br/>                                           |
| [**按鈕 \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | 取得指定之分割按鈕控制項的資訊。 使用這個宏或明確地傳送 [**BCM \_ GETSPLITINFO**](bcm-getsplitinfo.md) 訊息。<br/>                                                                                    |
| [**按鈕 \_ >getstate**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | 取得選項按鈕或核取方塊的檢查狀態。 您可以使用這個宏，或明確地傳送 [**BM \_ >getstate**](bm-getstate.md) 訊息。 <br/>                                                                                       |
| [**按鈕 \_ GetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | 取得按鈕的文字。<br/>                                                                                                                                                                                                             |
| [**按鈕 \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | 取得按鈕文字中的字元數。<br/>                                                                                                                                                                                 |
| [**按鈕 \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | 取得用來在按鈕控制項中繪製文字的邊界。 您可以使用此宏或明確地傳送 [**BCM \_ GETTEXTMARGIN**](bcm-gettextmargin.md) 訊息。 <br/>                                                                        |
| [**按鈕 \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | 設定選項按鈕或核取方塊的核取狀態。 您可以使用這個宏，或明確地傳送 [**BM \_ SETCHECK**](bm-setcheck.md) 訊息。 <br/>                                                                                       |
| [**按鈕 \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | 設定具有 [**BS \_ SPLITBUTTON**](button-styles.md)樣式之指定按鈕的下拉式狀態。 使用這個宏或明確地傳送 [**BCM \_ SETDROPDOWNSTATE**](bcm-setdropdownstate.md) 訊息。 <br/>           |
| [**按鈕 \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | 設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。 使用這個宏或明確地傳送 [**BCM \_ SETSHIELD**](bcm-setshield.md) 訊息。 <br/>                                          |
| [**按鈕 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | 將影像清單指派給按鈕控制項。 您可以使用此宏或明確地傳送 [**BCM \_ SETIMAGELIST**](bcm-setimagelist.md) 訊息。 <br/>                                                                                       |
| [**按鈕 \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | 設定與指定的命令連結按鈕相關聯的備註文字。 您可以使用此宏或明確地傳送 [**BCM \_ SETNOTE**](bcm-setnote.md) 訊息。<br/>                                                                  |
| [**按鈕 \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | 設定指定之分割按鈕控制項的資訊。 使用這個宏或明確地傳送 [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) 訊息。<br/>                                                                                    |
| [**按鈕 \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | 設定按鈕的醒目提示狀態。 醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。 您可以使用這個宏，或明確地傳送 [**BM \_ SETSTATE**](bm-setstate.md) 訊息。 <br/>        |
| [**按鈕 \_ >setstyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | 設定按鈕的樣式。 您可以使用這個宏，或明確地傳送 [**BM \_ >setstyle**](bm-setstyle.md) 訊息。 <br/>                                                                                                                |
| [**按鈕 \_ SetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | 設定按鈕的文字。<br/>                                                                                                                                                                                                             |
| [**按鈕 \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | 設定在按鈕控制項中繪製文字的邊界。 您可以使用此宏或明確地傳送 [**BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md) 訊息。 <br/>                                                                         |



 

### <a name="messages"></a>訊息



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BCM \_ GETIDEALSIZE**](bcm-getidealsize.md)         | 取得最適合其文字和影像的按鈕大小（如果有影像清單）。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) 宏。<br/>                                                                                   |
| [**BCM \_ GETIMAGELIST**](bcm-getimagelist.md)         | 取得 [**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) 結構，描述指派給按鈕控制項的影像清單。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) 宏。<br/>                                                  |
| [**BCM \_ GETNOTE**](bcm-getnote.md)                   | 取得與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) 宏。<br/>                                                                                                                        |
| [**BCM \_ GETNOTELENGTH**](bcm-getnotelength.md)       | 取得可在 [命令連結] 按鈕的 [描述] 中顯示的附注文字長度。 明確地傳送此訊息，或使用 [**按鈕 \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) 宏。<br/>                                                                           |
| [**BCM \_ GETSPLITINFO**](bcm-getsplitinfo.md)         | 取得分割按鈕控制項的資訊。 明確地傳送此訊息，或使用 [**按鈕 \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) 宏。 <br/>                                                                                                                                    |
| [**BCM \_ GETTEXTMARGIN**](bcm-gettextmargin.md)       | 取得用來在按鈕控制項中繪製文字的邊界。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) 宏。<br/>                                                                                                                     |
| [**BCM \_ SETDROPDOWNSTATE**](bcm-setdropdownstate.md) | 設定具有樣式 [**TBSTYLE 下拉式 \_ 清單**](toolbar-control-and-button-styles.md)之按鈕的下拉式狀態。 明確地傳送此訊息，或使用 [**按鈕 \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) 宏。<br/>                                        |
| [**BCM \_ SETIMAGELIST**](bcm-setimagelist.md)         | 將影像清單指派給按鈕控制項。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) 宏。<br/>                                                                                                                                    |
| [**BCM \_ SETNOTE**](bcm-setnote.md)                   | 設定與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) 宏。<br/>                                                                                                                        |
| [**BCM \_ SETSHIELD**](bcm-setshield.md)               | 設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。 明確地傳送此訊息，或使用 [**按鈕 \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) 宏。<br/>                                                  |
| [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md)         | 設定分割按鈕控制項的資訊。 明確地傳送此訊息，或使用 [**按鈕 \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) 宏。<br/>                                                                                                                                     |
| [**BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md)       | [**BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md)訊息會設定在按鈕控制項中繪製文字的邊界。 <br/>                                                                                                                                                                      |
| [**BM \_ 按一下**](bm-click.md)                         | 模擬使用者按一下按鈕。 這則訊息會讓按鈕收到 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息，以及按鈕的父視窗，以接收 [BN \_ 按一下](bn-clicked.md) 的通知碼。<br/> |
| [**BM \_ GETCHECK**](bm-getcheck.md)                   | 取得選項按鈕或核取方塊的檢查狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) 宏。<br/>                                                                                                                                  |
| [**BM \_ GETIMAGE**](bm-getimage.md)                   | 抓取影像的控制碼 (圖示或點陣圖) 與按鈕相關聯。<br/>                                                                                                                                                                                                             |
| [**BM \_ >GETSTATE**](bm-getstate.md)                   | 抓取按鈕或核取方塊的狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ >getstate**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) 宏。<br/>                                                                                                                                         |
| [**BM \_ SETCHECK**](bm-setcheck.md)                   | 設定選項按鈕或核取方塊的核取狀態。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) 宏來傳送。<br/>                                                                                                                             |
| [**BM \_ SETDONTCLICK**](bm-setdontclick.md)           | 設定選項按鈕上的旗標，此旗標會在按鈕取得焦點時，控制 [BN \_ 按一下](bn-clicked.md) 訊息的產生。<br/>                                                                                                                                                     |
| [**BM \_ SETIMAGE**](bm-setimage.md)                   | 將新影像 (圖示或點陣圖) 與按鈕產生關聯。<br/>                                                                                                                                                                                                                                 |
| [**BM \_ SETSTATE**](bm-setstate.md)                   | 設定按鈕的醒目提示狀態。 醒目提示狀態會指出按鈕是否反白顯示，如同使用者是否已推送按鈕。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) 宏。<br/>                                                   |
| [**BM \_ >SETSTYLE**](bm-setstyle.md)                   | 設定按鈕的樣式。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ >setstyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) 宏。<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>通知



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>目錄</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bcn-dropdown.md">BCN_DROPDOWN</a></td>
<td>當使用者按一下按鈕上的下拉箭號時傳送。 控制項的父視窗會以 <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> 訊息的形式接收此通知碼。<br/></td>
</tr>
<tr class="even">
<td><a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a></td>
<td>通知按鈕控制項擁有者滑鼠正在進入或離開按鈕控制項的工作區。 按鈕控制項會以 <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> 訊息的形式傳送此通知碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-clicked.md">BN_CLICKED</a></td>
<td>當使用者按一下按鈕時傳送。 <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-clicked.md">BN_CLICKED</a>通知程式碼。 <br/></td>
</tr>
<tr class="even">
<td><a href="bn-dblclk.md">BN_DBLCLK</a></td>
<td>當使用者按兩下按鈕時傳送。 系統會自動為 <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>、 <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>和 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕傳送此通知碼。 其他按鈕類型只有在具有<a href="button-styles.md"><strong>BS_NOTIFY</strong></a>樣式時，才會傳送<a href="bn-dblclk.md">BN_DBLCLK</a> 。<br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-dblclk.md">BN_DBLCLK</a>通知程式碼。 <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-disable.md">BN_DISABLE</a></td>
<td>停用按鈕時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-disable.md">BN_DISABLE</a>通知程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a></td>
<td>當使用者按兩下按鈕時傳送。 系統會自動為 <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>、 <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>和 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕傳送此通知碼。 其他按鈕類型只有在具有<a href="button-styles.md"><strong>BS_NOTIFY</strong></a>樣式時，才會傳送<a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> 。<br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a>通知程式碼。 <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-hilite.md">BN_HILITE</a></td>
<td>當使用者選取按鈕時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-hilite.md">BN_HILITE</a>通知程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="bn-killfocus.md">BN_KILLFOCUS</a></td>
<td>當按鈕失去鍵盤焦點時傳送。 按鈕必須有 <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> 樣式才能傳送此通知碼。 <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-killfocus.md">BN_KILLFOCUS</a>通知程式碼。 <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-paint.md">BN_PAINT</a></td>
<td>在應繪製按鈕時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-paint.md">BN_PAINT</a>通知程式碼。 <br/></td>
</tr>
<tr class="even">
<td><a href="bn-pushed.md">BN_PUSHED</a></td>
<td>當按鈕的推送狀態設定為推送時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-pushed.md">BN_PUSHED</a>通知程式碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-setfocus.md">BN_SETFOCUS</a></td>
<td>當按鈕收到鍵盤焦點時傳送。 按鈕必須有 <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> 樣式才能傳送此通知碼。 <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-setfocus.md">BN_SETFOCUS</a>通知程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="bn-unhilite.md">BN_UNHILITE</a></td>
<td>當醒目提示應該從按鈕移除時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-unhilite.md">BN_UNHILITE</a>通知程式碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-unpushed.md">BN_UNPUSHED</a></td>
<td>當按鈕的推送狀態設定為未推送時傳送。
<blockquote>
[!Note]<br />
此通知碼僅提供與3.0 版之前的16位 Windows 版本的相容性。 應用程式應該使用這項工作的 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕樣式和 <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> 結構。
</blockquote>
<br/> <br/> 按鈕的父視窗會透過<a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a>訊息接收<a href="bn-unpushed.md">BN_UNPUSHED</a>通知程式碼。<br/></td>
</tr>
<tr class="even">
<td><a href="nm-customdraw-button.md">NM_CUSTOMDRAW (按鈕) </a></td>
<td>通知按鈕控制項的父視窗，有關按鈕上的自訂繪製作業。 <br/> 按鈕控制項會以 <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> 訊息的形式傳送此通知碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a></td>
<td>在繪製按鈕之前， <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> 的訊息會傳送至按鈕的父視窗。 父視窗可以變更按鈕的文字和背景色彩。 不過，只有主控描繪的按鈕會回應父視窗處理此訊息。 <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>結構



| 主題                                         | 目錄                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**按鈕 \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | 包含與按鈕控制項搭配使用之影像清單的相關資訊。<br/>                                                                                                                                                                                                                                 |
| [**按鈕 \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | 包含定義分割按鈕 ([**BS \_ SPLITBUTTON**](button-styles.md) 和 [**BS \_ DEFSPLITBUTTON**](button-styles.md) 樣式) 的資訊。 搭配 [**bcm \_ GETSPLITINFO**](bcm-getsplitinfo.md) 和 [**bcm \_ SETSPLITINFO**](bcm-setsplitinfo.md) 訊息使用。<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | 包含 [BCN \_ 下拉式](bcn-dropdown.md) 通知的相關資訊。<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | 包含將滑鼠移到按鈕控制項上的相關資訊。<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>常數



| 主題                              | 目錄                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [按鈕樣式](button-styles.md) | 指定按鈕樣式的組合。 如果您使用 BUTTON 類別和 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立按鈕，則可以指定下列任何按鈕樣式。<br/> |



 


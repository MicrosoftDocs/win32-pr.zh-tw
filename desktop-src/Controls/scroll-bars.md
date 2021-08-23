---
title: Scroll Bar
description: 本章節包含有關捲軸所使用之程式設計項目的資訊。
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca1aa4dc1b676cd5ce4f98c23035e462b9f4f87f8c20265848a8f0bcde80964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636988"
---
# <a name="scroll-bar"></a>Scroll Bar

本章節包含有關捲軸所使用之程式設計項目的資訊。 視窗可以顯示大於視窗工作區的資料物件，例如，檔或點陣圖。 當使用 *捲軸* 來提供時，使用者可以在工作區中滾動資料物件，以查看超出視窗框線的物件部分。

### <a name="overviews"></a>概觀



| 主題                                      | 目錄                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於捲軸](about-scroll-bars.md) | 捲軸包含一個陰影軸，其中每一端有一個箭號按鈕，而 *捲動方塊* (有時也稱為箭號按鈕之間的捲動方塊) 。<br/>                                                                                                                                                                     |
| [使用捲軸](using-scroll-bars.md) | 建立重迭、快顯視窗或子視窗時，您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**ws \_ HSCROLL**](/windows/desktop/winmsg/window-styles)、 [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)或這兩種樣式來新增標準捲軸。<br/> |



 

### <a name="functions"></a>函式



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
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a>函式會啟用或停用一或兩個捲軸箭號。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a>函式會捕獲指定捲軸的相關資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a>函式會抓取捲軸的參數，包括最小和最大滾動位置、頁面大小，以及捲動方塊 (thumb) 的位置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a>函式會在指定的捲軸中， (thumb) 來抓取捲動方塊的目前位置。 目前的位置是相依于目前滾動範圍的相對值。 例如，如果滾動的範圍是0到100，而且捲動方塊位於橫條的中間，則目前的位置是50。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a>函式是為了與舊版相容而提供。 新的應用程式應該使用 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> 函數。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a>函式會抓取指定捲軸的目前最小和最大捲動方塊 (thumb) 位置。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a>函式僅提供相容性。 新的應用程式應該使用 <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> 函數。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a>函式會水準且垂直地滾動位數的矩形。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a>函式會滾動指定之視窗工作區的內容。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a>函式是為了與舊版相容而提供。 新的應用程式應該使用 <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> 函數。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a>函式會滾動指定之視窗工作區的內容。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a>函式會設定捲軸的參數，包括最小和最大滾動位置、頁面大小，以及捲動方塊 (thumb) 的位置。 如果有要求，函式也會重新繪製捲軸。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a>函式會在指定的捲軸中設定捲動方塊 (thumb) 的位置，並在要求時，重新繪製捲軸以反映捲動方塊的新位置。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a>函式是為了與舊版相容而提供。 新的應用程式應該使用 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> 函數。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a>函式會設定指定捲軸的最小和最大捲動方塊位置。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a>函式是為了與舊版相容而提供。 新的應用程式應該使用 <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> 函數。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a>函式會顯示或隱藏指定的捲軸。 <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>訊息



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SBM \_ 啟用 \_ 箭號**](sbm-enable-arrows.md)      | 應用程式會傳送 [**SBM \_ 啟用 \_ 箭**](sbm-enable-arrows.md) 號訊息，以啟用或停用捲軸控制項的一個或兩個箭號。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SBM \_ GETPOS**](sbm-getpos.md)                     | 傳送 [**SBM \_ GETPOS**](sbm-getpos.md) 訊息，以抓取捲軸控制項捲動方塊的目前位置。 目前的位置是相依于目前滾動範圍的相對值。 例如，如果滾動的範圍是0到100，而且捲動方塊位於橫條的中間，則目前的位置是50。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollPos** 函數才能正常運作。<br/> |
| [**SBM \_ GETRANGE**](sbm-getrange.md)                 | 傳送 [**SBM \_ GETRANGE**](sbm-getrange.md) 訊息，以抓取捲軸控制項的最小和最大位置值。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollRange** 函數才能正常運作。<br/>                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLBARINFO**](sbm-getscrollbarinfo.md) | 由應用程式傳送以取得指定捲軸的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)       | 傳送 [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md) 訊息以抓取捲軸的參數。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollInfo** 函數才能正常運作。<br/>                                                                                                                                                                                                                                           |
| [**SBM \_ SETPOS**](sbm-setpos.md)                     | 傳送 [**SBM \_ SETPOS**](sbm-setpos.md) 訊息來設定捲動方塊 (thumb 的位置) 並在要求時，重繪捲軸以反映捲動方塊的新位置。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollPos** 函數才能正常運作。<br/>                                                                                                                                                                  |
| [**SBM \_ SETRANGE**](sbm-setrange.md)                 | 傳送 [**SBM \_ SETRANGE**](sbm-setrange.md) 訊息來設定捲軸控制項的最小和最大位置值。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollRange** 函數才能正常運作。<br/>                                                                                                                                                                                                                   |
| [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)     | 應用程式會將 [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md) 訊息傳送到捲軸控制項，以設定最小和最大位置值，以及重新繪製控制項。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)       | 傳送 [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md) 訊息來設定捲軸的參數。 <br/> 應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollInfo** 函數才能正常運作。<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>通知



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) | 當控制項即將繪製時，會將 [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) 訊息傳送到捲軸控制項的父視窗。 藉由回應此訊息，父視窗可以使用顯示內容控制碼來設定捲軸控制項的背景色彩。 <br/> 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 <br/> |
| [**WM \_ HSCROLL**](wm-hscroll.md)                     | 當捲軸事件發生在視窗的標準水準捲軸時，會將 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息傳送至視窗。 當控制項中發生滾動事件時，此訊息也會傳送給水準捲軸控制項的擁有者。 <br/> 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 <br/>                                        |
| [**WM \_ VSCROLL**](wm-vscroll.md)                     | 當捲軸事件發生在視窗的標準垂直捲動條時，會將 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息傳送至視窗。 當控制項中發生滾動事件時，此訊息也會傳送給垂直捲動條控制項的擁有者。 <br/> 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 <br/>                                            |



 

### <a name="structures"></a>結構



| 主題                                  | 目錄                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)結構包含捲軸資訊。<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)結構包含捲軸參數，這些參數是由 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)函數 (或 [**SBM \_ SetScrollInfo**](sbm-setscrollinfo.md) Message) 所設定，或是由 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)函數 (或 [**SBM \_ GetScrollInfo**](sbm-getscrollinfo.md) message) 所抓取。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                                      | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [捲軸控制項樣式](scroll-bar-control-styles.md) | 若要使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立捲軸控制項，請指定捲軸類別、適當的視窗樣式常數，以及下列捲軸控制項樣式的組合。 某些樣式會建立使用預設寬度或高度的捲軸控制項。 但是，當您呼叫 **CreateWindow** 或 **CreateWindowEx** 時，一定要指定捲軸的 x 和 y 座標和其他維度。 <br/> |



 

 


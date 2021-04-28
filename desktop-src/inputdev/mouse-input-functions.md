---
title: 滑鼠輸入功能
description: 滑鼠輸入功能
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a952a9ce90284f284b176c608228c0b852f5f4c8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112876"
---
# <a name="mouse-input-functions"></a>滑鼠輸入功能


## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。 此函數會呼叫 <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> （如果存在），否則會模擬它。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br/></td>
<td>擷取滑鼠並追蹤其移動，直到使用者放開左側按鈕、按下 ESC 鍵，或將滑鼠移到指定點周圍的拖曳矩形外。 拖曳矩形的寬度和高度是由<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a>函數所傳回的<strong>SM_CXDRAG</strong>和<strong>SM_CYDRAG</strong>值所指定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>抓取視窗的控制碼 (是否有任何) 已捕捉到滑鼠。 一次只能有一個視窗可捕獲滑鼠;無論游標是否在其框線內，此視窗都會收到滑鼠輸入。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br/></td>
<td>抓取滑鼠目前的按兩下時間。 按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。 按兩下時間是在按兩下的第一次和第二次按一下時，可能發生的最大毫秒數。 最大的按兩下時間是5000毫秒。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br/></td>
<td>抓取滑鼠或畫筆之前最多64個座標的歷程記錄。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>Mouse_event</strong></a>函式會會合成滑鼠動作並按一下按鈕。<br/>
<blockquote>
[!Note]<br />
此函數已被取代。 請改用 <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br/></td>
<td>從目前線程中的視窗釋放滑鼠捕捉，並還原一般滑鼠輸入處理。 不論游標的位置為何，已捕捉到滑鼠的視窗都會收到所有的滑鼠輸入，但在游標作用點位於另一個執行緒的視窗中，但在按下滑鼠按鍵時除外。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>將滑鼠捕捉設定為屬於目前線程的指定視窗。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a><br/></td>
<td>設定滑鼠的按兩下時間。 按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。 按兩下時間是在按兩下的第一個和第二個點之間可能發生的最大毫秒數。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br/></td>
<td>反轉或還原左右滑鼠按鍵的意義。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。<br/>
<blockquote>
[!Note]<br />
<a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a>函式會呼叫<a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> （如果存在），否則<strong>_TrackMouseEvent</strong>模擬<strong>TrackMouseEvent</strong>。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 


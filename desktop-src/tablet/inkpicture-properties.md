---
description: 此區段包含 InkPicture 控制項的屬性。
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: InkPicture 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694992"
---
# <a name="inkpicture-properties"></a>InkPicture 屬性

此區段包含 InkPicture 控制項的屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw 屬性</strong></a></td>
<td>取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否會在視窗失效時重新繪製 (是否會在與 InkPicture 相關聯的視窗收到) 的 WM_PAINT 訊息時，自動重新繪製目前與 InkPicture 控制項相關聯的 <a href="inkdisp-class.md"><strong>InkDisp</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>顏色</strong></a></td>
<td>取得或設定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的背景色彩。 預設的背景色彩是系統視窗背景色彩，通常是白色。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk 屬性</strong></a></td>
<td>取得值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否只 (執行時間) 收集筆跡。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>取得或設定收集模式，這個模式會決定是否要將筆墨、手勢或筆跡和手勢辨識為使用者寫入。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor 屬性</strong></a></td>
<td>取得可在<a href="inkpicture-control-reference.md">InkPicture</a>控制項的筆墨區域中使用的<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a>集合。<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>取得要使用筆墨來保存的 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> 集合 (設計階段) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>System.windows.controls.inkcanvas.defaultdrawingattributes 屬性</strong></a></td>
<td>取得或設定預設的 <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> 集合，以在只) 繪製和顯示筆墨 (執行時間時使用。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription 屬性</strong></a></td>
<td>取得或設定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的封包描述， (執行時間) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering 屬性</strong></a></td>
<td>取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否在收集時動態呈現筆墨。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>System.windows.controls.inkcanvas.editingmode</strong></a></td>
<td>取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否處於筆墨模式、刪除模式或選取/編輯模式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>啟用</strong></a></td>
<td>取得或設定值，這個值會決定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否可以回應使用者產生的事件。<br/>
<blockquote>
[!Note]<br />
這個屬性就相當於 <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> 屬性。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>取得或設定值，這個值會指定是否以筆劃或點抹除筆墨。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>取得或設定值，這個值會指定橡皮擦畫筆提示的寬度。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></td>
<td>取得 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項所系結的視窗控制碼。  (僅限執行時間) <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>筆跡</strong></a></td>
<td>取得或設定與<a href="inkpicture-control-reference.md">InkPicture</a>控制項相關聯的<a href="inkdisp-class.md"><strong>InkDisp</strong></a>物件 (執行時間僅) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>取得或設定值，這個值會指定 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項是否會收集 (的輸入、範圍事件中的資料指標，以及) 中的畫筆輸入。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX 屬性</strong></a></td>
<td>取得或設定以螢幕座標表示的視窗矩形周圍的 X 軸邊界。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY 屬性</strong></a></td>
<td>取得或設定以螢幕座標表示的視窗矩形周圍的 y 軸邊界。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon 屬性</strong></a></td>
<td>取得或設定目前的自訂滑鼠圖示。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer 屬性</strong></a></td>
<td>取得或設定值，這個值表示當滑鼠停留在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項的特定部分時，所顯示的滑鼠指標類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></td>
<td>取得要顯示在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項上的圖形檔案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>轉譯器屬性</strong></a></td>
<td>取得或設定 <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> 物件，這個物件是用來在 <a href="inkpicture-control-reference.md">InkPicture</a> 控制項上繪製筆墨 (只) 的執行時間。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>選取</strong></a></td>
<td>取得目前在<a href="inkpicture-control-reference.md">InkPicture</a>控制項內選取的<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a>集合 (執行時間) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>取得或設定控制項如何處理影像放置和調整大小。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk 屬性</strong></a></td>
<td>取得值，這個值會指定當系統處於高對比模式時，是否只將筆墨轉譯為一種色彩，Color = COLOR_WINDOWTEXT (從 GetSystemMetrics 呼叫) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>取得或設定值，這個值會指定當系統處於高對比模式時，是否將所有選取範圍的使用者介面 (選取範圍方塊和選取控點) 會以高對比繪製。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>平板電腦屬性</strong></a></td>
<td>取得<a href="inkpicture-control-reference.md">InkPicture</a>控制項目前用來收集輸入的<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a>物件。<br/></td>
</tr>
</tbody>
</table>



 


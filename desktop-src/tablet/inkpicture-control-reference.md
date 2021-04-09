---
description: InkPicture 控制項可讓您將影像放在應用程式中，並讓使用者在其上新增筆跡。
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: InkPicture 控制項參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8caaf1970394338f858cd0fdff0dab58153f53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945355"
---
# <a name="inkpicture-control-reference"></a>InkPicture 控制項參考

InkPicture 控制項可讓您將影像放在應用程式中，並讓使用者在其上新增筆跡。 它適用于無法將筆墨辨識為文字，但改為筆跡儲存的案例。

InkPicture 控制項可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

> [!Note]  
> InkPicture 控制項未標示為 safe 以進行腳本處理。 InkPicture 控制項不能用在 HTML 或 ASP.NET 網頁中。

 

在透明控制項背後建立 InkPicture 控制項 (例如，加上 WS \_ EX \_ 透明屬性集) 的分組會導致 InkPicture 無法收集筆跡。

## <a name="members"></a>成員



| 列舉型別                                      | 描述                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | 定義值，這些值會指定背景圖片在 InkPicture 控制項內的運作方式。<br/> |



 



| 事件                                                                              | 描述                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | 已取代。<br/>                                                                                                                                                                                                                                                                                             |
| [**按一下**](inkpicture-click.md)                                                  | 發生于使用者按一下 InkPicture 控制項時。<br/>                                                                                                                                                                                                                                                       |
| [**CursorButtonDown 事件**](inkpicture-cursorbuttondown.md)                      | 當 [**InkCollector**](inkcollector-class.md) 控制項偵測到關閉的 [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) 物件時發生。<br/>                                                                                                                                                         |
| [**CursorButtonUp 事件**](inkpicture-cursorbuttonup.md)                          | 當 InkPicture 控制項偵測到已啟動的 [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) 時發生。<br/>                                                                                                                                                                                                  |
| [**CursorDown 事件**](inkpicture-cursordown.md)                                  | 當游標提示接觸到數位化的 tablet 介面時發生。<br/>                                                                                                                                                                                                                                      |
| [**CursorInRange 事件**](inkpicture-cursorinrange.md)                            | 當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                                                                             |
| [**CursorOutOfRange 事件**](inkpicture-cursoroutofrange.md)                      | 當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                                                                           |
| [**DblClick**](inkpicture-dblclick.md)                                            | 發生于按兩下 InkPicture 控制項時。<br/> 此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEDblClick 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。<br/> |
| [**手勢事件**](inkpicture-gesture.md)                                        | 當應用程式手勢被辨識時發生。<br/>                                                                                                                                                                                                                                                       |
| [**KeyDown 事件 \[ InkPicture 控制項\]**](inkpicture-keydown.md)                 | 發生于按下按鍵時，以及在 InkPicture 控制項有焦點時的向下位置。<br/>                                                                                                                                                                                                           |
| [**KeyPress 事件 \[ InkPicture 控制項\]**](inkpicture-keypress.md)                | 發生于 InkPicture 控制項具有焦點時按下按鍵時。<br/>                                                                                                                                                                                                                                    |
| [**KeyUp 事件 \[ InkPicture 控制項\]**](inkpicture-keyup.md)                     | 當 InkPicture 控制項具有焦點時，放開按鍵時發生。<br/>                                                                                                                                                                                                                                   |
| [**MouseDown 事件 \[ InkPicture 控制項\]**](inkpicture-mousedown.md)             | 發生于滑鼠指標位於 InkPicture 控制項上方且按下滑鼠按鍵時。<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | 發生于滑鼠指標進入 InkPicture 控制項時。<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | 發生于滑鼠指標停留在 InkPicture 控制項上時。<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | 發生于滑鼠指標離開 InkPicture 控制項時。<br/>                                                                                                                                                                                                                                            |
| [**MouseMove 事件 \[ InkPicture 控制項\]**](inkpicture-mousemove.md)             | 發生于滑鼠指標移至 InkPicture 控制項時。<br/>                                                                                                                                                                                                                                     |
| [**MouseUp 事件 \[ InkPicture 控制項\]**](inkpicture-mouseup.md)                 | 發生于滑鼠指標位於 InkPicture 控制項上方並放開滑鼠按鍵時。<br/>                                                                                                                                                                                                            |
| [**滑鼠滾輪**](inkpicture-mousewheel.md)                                        | 發生于滑鼠滾輪移動時，InkPicture 控制項有焦點時。<br/>                                                                                                                                                                                                                               |
| [**NewInAirPackets 事件**](inkpicture-newinairpackets.md)                        | 當出現無線封包時發生。<br/>                                                                                                                                                                                                                                                                   |
| [**NewPackets 事件**](inkpicture-newpackets.md)                                  | InkPicture 控制項接收封包時發生。<br/>                                                                                                                                                                                                                                                   |
| [**畫**](inkpicture-painted.md)                                              | InkPicture 控制項已完成重繪本身時發生。<br/>                                                                                                                                                                                                                                      |
| [**繪畫**](inkpicture-painting.md)                                            | 發生于 InkPicture 控制項自行重繪之前。<br/>                                                                                                                                                                                                                                                    |
| [**調整大小**](inkpicture-resize.md)                                                | InkPicture 控制項調整大小時發生。<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | InkPicture 控制項中的文字選取範圍變更（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）時發生。<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | InkPicture 控制項中的文字選取範圍即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | 發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。<br/>                                                                                                  |
| [**SelectionMoving 事件 \[ InkPicture 控制項\]**](inkpicture-selectionmoving.md) | 當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性。<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | 發生于目前的選取範圍變更時（例如，透過對使用者介面的改變、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | 發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | 發生于調整 InkPicture 控制項的大小時，特別是在 [**寬度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) 或 [**高度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) 屬性值變更之後。<br/>                                                                                                      |
| [**SizeModeChanged**](inkpicture-sizemodechanged.md)                              | 發生于 InkPicture 控制項的 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) 屬性變更之後。<br/>                                                                                                                                                                                           |
| **StyleChanged**                                                                   | 未實作。<br/>                                                                                                                                                                                                                                                                                        |
| [**中風**](inkpicture-stroke.md)                                                | 當使用者在任何平板電腦上繪製新筆劃時發生。<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | 從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之後發生。<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | 發生于從 [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性中刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之前。<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | 發生于系統色彩變更之後。<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | 在辨識系統手勢時發生。<br/>                                                                                                                                                                                                                                                             |
| [**TabletAdded 事件**](inkpicture-tabletadded.md)                                | 當 tablet 新增至系統時發生。<br/>                                                                                                                                                                                                                                                            |
| [**TabletRemoved 事件**](inkpicture-tabletremoved.md)                            | 從系統移除平板電腦時發生。<br/>                                                                                                                                                                                                                                                        |



 



| 方法                                                                                   | 描述                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | 傳回值，這個值會指出 InkPicture 控制項是否對特定事件感興趣。<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | 傳回值，這個值會指出 InkPicture 控制項是否對特定的應用程式手勢感興趣。<br/>                                                     |
| [**GetWindowInputRectangle 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | 傳回用來繪製筆墨的視窗矩形（以圖元為單位）。<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | 傳回 [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) 列舉的成員，這個成員會指定點擊測試期間遇到的選取部分（如果有的話）。<br/> |
| [**SetAllTabletsMode 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | 讓 InkPicture 控制項從任何連接到 Tablet PC 的平板電腦收集筆跡。<br/>                                                                            |
| [**SetEventInterest 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | 設定值，這個值會指出 InkPicture 控制項是否對指定的事件感興趣。<br/>                                                                        |
| SetFocus                                                                                 | 將焦點移至 InkPicture 控制項。<br/>                                                                                                                          |
| [**SetGestureStatus 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | 在指定的應用程式手勢中設定 InkPicture 物件的感興趣。<br/>                                                                                      |
| [**SetSingleTabletIntegratedMode 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | 設定 InkPicture 控制項，以從一台連接到 Tablet PC 的平板電腦收集筆跡。 其他平板電腦的筆墨會被忽略。<br/>                                       |
| [**SetWindowInputRectangle 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | 指定視窗座標中要設定的視窗矩形，以在其中繪製筆墨。<br/>                                                                            |
| ShowWhatsThis                                                                            | 使用32位 Microsoft Windows 作業系統的 [說明] 中所提供的 [內容] 快顯視窗，在說明檔中顯示選取的主題 (設計階段) 。<br/>           |
| ZOrder                                                                                   | 將控制項放在圖形層級中的迭置順序前方或背面， (設計階段的) 。<br/>                                                               |



 



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
<td>取得或設定值，這個值會指定 InkPicture 控制項是否會在視窗失效時重新繪製 (是否會在與 InkPicture 相關聯的視窗收到) 的 WM_PAINT 訊息時，自動重新繪製目前與 InkPicture 控制項相關聯的 <a href="inkdisp-class.md"><strong>InkDisp</strong></a> 物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>顏色</strong></a></td>
<td>取得或設定 InkPicture 控制項的背景色彩。 預設的背景色彩是系統視窗背景色彩，通常是白色。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk 屬性</strong></a></td>
<td>取得值，這個值會指定 InkPicture 控制項是否只 (執行時間) 收集筆跡。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>取得或設定收集模式，這個模式會決定是否要將筆墨、手勢或筆跡和手勢辨識為使用者寫入。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor 屬性</strong></a></td>
<td>取得可在 InkPicture 控制項的筆墨區域中使用的 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> 集合。<br/></td>
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
<td>取得或設定 InkPicture 控制項的封包描述， (執行時間) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering 屬性</strong></a></td>
<td>取得或設定值，這個值會指定 InkPicture 控制項是否在收集時動態呈現筆墨。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>System.windows.controls.inkcanvas.editingmode</strong></a></td>
<td>取得或設定值，這個值會指定 InkPicture 控制項是否處於筆墨模式、刪除模式或選取/編輯模式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>啟用</strong></a></td>
<td>取得或設定值，這個值會決定 InkPicture 控制項是否可以回應使用者產生的事件。<br/>
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
<td>取得 InkPicture 控制項所系結的視窗控制碼。  (僅限執行時間) <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>筆跡</strong></a></td>
<td>取得或設定與 InkPicture 控制項相關聯的 <a href="inkdisp-class.md"><strong>InkDisp</strong></a> 物件 (執行時間僅) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>取得或設定值，這個值會指定 InkPicture 控制項是否會收集 (的輸入、範圍事件中的資料指標，以及) 中的畫筆輸入。<br/></td>
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
<td>取得或設定值，這個值表示當滑鼠停留在 InkPicture 控制項的特定部分時，所顯示的滑鼠指標類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></td>
<td>取得要顯示在 InkPicture 控制項上的圖形檔案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>轉譯器屬性</strong></a></td>
<td>取得或設定 <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> 物件，這個物件是用來在 InkPicture 控制項上繪製筆墨 (只) 的執行時間。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>選取</strong></a></td>
<td>取得目前在 InkPicture 控制項內選取的 <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> 集合 (執行時間) 。<br/></td>
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
<td>取得 InkPicture 控制項目前用來收集輸入的 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> 物件。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

InkPicture 控制項的執行時間使用者介面是具有不透明背景 (單一色彩、圖片背景，或包含不透明筆墨) 的視窗。

您可以使用 InkPicture 控制項，在 Microsoft Windows 2000、Windows Server 2003、Windows XP Tablet PC Edition 以外的任何 Windows XP 版本，以及任何版本的 Windows Vista 中轉譯筆墨。 不過，您可以在下列情況下輸入筆墨、接受手勢或辨識手寫：

-   如果已安裝 Windows Vista 或 XP Tablet PC Edition 2005，可以輸入和辨識筆跡。
-   也可以辨認手勢。
-   如果手寫是源自執行舊版 Windows 的電腦（只要辨識器存在的話），就可以將手寫辨識為文字。

如果您使用 windows 2000、Windows Server 2003、windows XP Tablet PC Edition 2005 以外的任何 Windows XP 版本，您可以將值指派給 InkPicture 控制項的環境屬性，然後將筆墨複製並貼到其他應用程式。 不過，其 InkEnabled 屬性的值永遠為 **FALSE**。

保存的 [**InkDisp**](inkdisp-class.md) 物件可以在所有 windows VISTA 和 XP 版本上，以及只安裝 Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 的系統上載入和顯示。 如果已安裝 Windows Vista 或 Windows XP Tablet PC Edition 2005， **InkDisp** 物件只能轉換成 (可辨識的文字) 。

如果此控制項上的作業不成功，則會傳回合法的 HRESULT。 如果錯誤條件結果，請檢查傳回的 HRESULT 是否發生錯誤。

如需筆墨控制項的詳細資訊，請參閱 [筆墨](ink-controls.md)。

如需哪些執行緒引發特定事件的詳細資訊，請參閱 [可引發事件的執行緒](threads-on-which-an-event-can-fire.md)。

若要改善應用程式的效能，請在不再需要 InkPicture 控制項時，手動加以處置。

> [!Note]  
> 當 InkPicture 控制項與另一個控制項重迭時（例如，將 [ **分組** ] 設定為 [透明]），InkPicture 將不會收集筆跡。 InkPicture 必須是 Z 順序中最上層的控制項，或者必須是 **群組方塊** 的子系。

 

## <a name="com-implementation"></a>COM 執行

這個物件會實 **IInkPicture** COM 介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkEdit 控制項參考](inkedit-control-reference.md)
</dt> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> </dl>


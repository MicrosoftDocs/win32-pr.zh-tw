---
title: 關於資料說明控制項
description: '[點擊線] 是一種視窗，其中包含滑杆 (有時也稱為頻道中) 的捲動方塊，以及選擇性的刻度標記。 當使用者使用滑鼠或方向按鍵移動滑杆時，會傳送通知訊息以指出變更。'
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450fba1c9b41cf5789bcda08263ff7a0b8b2d2d17db3746cf5d47bdc5d0b6a4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967934"
---
# <a name="about-trackbar-controls"></a>關於資料說明控制項

[點擊線] 是一種視窗，其中包含滑杆 (有時也稱為頻道中) 的捲動方塊，以及選擇性的刻度標記。 當使用者使用滑鼠或方向按鍵移動滑杆時，會傳送通知訊息以指出變更。

-   [選取範圍](#selection-range)
-   [訊息](#trackbar-messages)
-   [資訊提示通知訊息](#trackbar-notification-messages)
-   [預設的顯示訊息處理](#default-trackbar-message-processing)
-   [跟蹤工具工具提示](#trackbar-tooltips)

當您想要讓使用者在範圍內選取離散不帶正負號的整數值或一組連續不帶正負號的整數值時，Trackbars 會很有用。 例如，您可以使用標題，讓使用者將滑杆移至指定的刻度，以設定鍵盤的重複速度。 下圖顯示一般的敘述。

![具有標籤的快捷方式的螢幕擷取畫面，其具有緩慢和快速的結尾](images/tkb-simple.png)

當您建立時，會以您所指定的遞增順序來移動其中的滑杆。 此範圍中的值稱為邏輯單元。 例如，如果您指定 [提要的邏輯單元] 的範圍是從0到5，則滑杆只能佔用六個位置：位於提要欄左側的位置，以及範圍中每個遞增的一個位置。 通常，每個位置都是以刻度來識別;不過，刻度的數目是任意的，且可以少於邏輯位置的數目。

您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立程式，並指定 [並排] [**\_ 類別**](common-control-window-classes.md) 視窗類別。 在您建立了一個程式之後，您可以使用 [訊息] 訊息來設定和取出其許多屬性。 您可以進行的變更包括設定滑桿的最小和最大位置、繪製刻度標記、設定選取範圍，以及重新調整滑桿定位。

## <a name="selection-range"></a>選取範圍

如果您建立具有 [Tb] [**\_ ENABLESELRANGE**](trackbar-control-styles.md) 樣式的 [內容]，則可以指定選取範圍。 這些敘述會反白顯示選取範圍，並在開頭和結尾顯示三角形刻度標記，如下圖所示。

![醒目提示範圍的 [顯示] 的螢幕擷取畫面](images/tkb-selrange.png)

選取器的選取範圍不會以任何方式影響其功能。 它是由應用程式執行範圍所組成。 您可以透過下列其中一種方式來執行此動作：

-   您可以使用選取範圍來讓使用者設定某個參數的最大值和最小值。 例如，使用者可以將滑杆移至某個位置，然後按一下標示為「最大值」的按鈕。 然後，應用程式會設定選取範圍來顯示使用者選擇的值。
-   藉由處理 [**WM \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 通知，將滑杆的移動限制在控制項內預先決定的子範圍，並不允許在選取範圍之外進行任何移動。 例如，您可以執行這項作業，例如，如果使用者可用的值範圍因其他使用者所做的選擇，或根據可用的資源而變更。

## <a name="trackbar-messages"></a>訊息

資料條的邏輯單元是這些連續值的組合，可供這些連續值使用。 它們通常是藉由在建立資料 [**TBM \_**](tbm-setrange.md) 時，透過指定可能值的範圍來定義。 應用程式可以使用 **TBM \_ SETRANGE**、 [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)或 [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)，以動態方式改變範圍。

若要取出滑杆的位置 (也就是使用者已選擇) 的值，請使用 [**TBM \_ GETPOS**](tbm-getpos.md) 訊息。 若要設定滑杆的位置，請使用 [**TBM \_ SETPOS**](tbm-setpos.md) 訊息。

除非您指定 [ [**tb] \_ NOTICKS**](trackbar-control-styles.md) 樣式，否則會自動在其開頭和結尾顯示刻度標記。  (在 Microsoft Visual Studio 資源編輯器中，這表示將刻度標記屬性設為 False。 ) 您可以使用 [ [**tb] \_ AUTOTICKS**](trackbar-control-styles.md)樣式，以定期間隔沿著協助工具來自動顯示其他刻度標記。 根據預設，[ **tb] \_ AUTOTICKS** 的 [並排顯示] 會在每個 [並排顯示] 範圍的遞增位置顯示刻度標記。 若要指定自動刻度的不同間隔，請將 [**TBM \_ SETTICFREQ**](tbm-setticfreq.md) 訊息傳送至 [訊息]。 例如，您可以使用此訊息只顯示1到100範圍內的10個刻度標記。

若要設定單一刻度的位置，請傳送 [**TBM \_ SETTIC**](tbm-settic.md) 訊息。 使用的資料會維護一個 DWORD 值陣列，這些值會儲存每個刻度標記的位置。 陣列不包含第一個和最後一個刻度，它們會自動建立。 當您傳送 [**TBM \_ GETTIC**](tbm-gettic.md) 訊息來取得對應刻度的位置時，可以在此陣列中指定索引。 或者，您可以傳送 [**TBM \_ GETPTICS**](tbm-getptics.md) 訊息來取得陣列的指標。 陣列中的元素數目等於兩個小於 [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) 訊息所傳回的滴答計數。 這是因為 **TBM \_ GETNUMTICS** 所傳回的計數包含不包含在陣列中的第一個和最後一個刻度標記。 若要抓取刻度的實體位置，請在 [協調器] 視窗的用戶端座標中，傳送 [**TBM \_ GETTICPOS**](tbm-getticpos.md) 訊息。 [**TBM \_ CLEARTICS**](tbm-cleartics.md)訊息會移除所有的標頭和最後一個和最後一個的刻度標記。

追蹤程式的線條大小可決定滑杆從箭號按鍵回應鍵盤輸入的距離，例如向右箭號或向下鍵。 若要取得或設定行大小，請傳送 [**TBM \_ GETLINESIZE**](tbm-getlinesize.md) 和 [**TBM \_ SETLINESIZE**](tbm-setlinesize.md) 訊息。 \_當使用者按下方向鍵時，這些對應項也會將 tb 的組合和 tb \_ LINEDOWN 通知碼傳送至其父視窗。

追蹤點的頁面大小可決定滑杆回應鍵盤輸入的進度，例如 PAGE UP 或 PAGE DOWN 鍵，或滑鼠輸入，例如在 [追蹤] 通道中按一下。 若要取得或設定頁面大小，請傳送 [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md) 和 [**TBM \_ >setpagesize method**](tbm-setpagesize.md) 訊息。 \_當您收到滾動頁的鍵盤或滑鼠輸入時，這些頁首也會將 tb PAGEUP 和 tb \_ PAGEDOWN 通知碼傳送至其父視窗。 如需詳細資訊，請參閱「資料 [提示通知訊息](#trackbar-notification-messages)」。

應用程式可以傳送訊息，以抓取資訊提供程式的維度。 [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)訊息會抓取滑杆的周框。 [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)訊息會捕獲滑杆的長度。 [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)訊息會抓取用來表示滑杆通道的周框，也就是滑杆移動的區域。 它包含選取範圍時的醒目提示。 如果 FIXEDLENGTH 樣式有 [ [**TBS \_**](trackbar-control-styles.md) ]，您可以傳送 [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) 訊息來變更滑杆的長度。

您可以藉由將訊息傳送至 [選取範圍]，來取得或設定選取範圍。 使用 [**TBM \_ SETSEL**](tbm-setsel.md) 訊息來設定選取專案的開始和結束位置。 若只設定開始位置，或只設定選取範圍的結束位置，請傳送 [**TBM \_ SETSELSTART**](tbm-setselstart.md) 或 [**TBM \_ SETSELEND**](tbm-setselend.md) 訊息。 若要取得選取範圍的開始或結束位置，請傳送 [**TBM \_ GETSELSTART**](tbm-getselstart.md) 或 [**TBM \_ GETSELEND**](tbm-getselend.md) 訊息。 若要清除選取範圍，並將其還原至其原始範圍，請傳送 [**TBM \_ CLEARSEL**](tbm-clearsel.md) 訊息。

> [!Note]  
> 應用程式必須負責確保使用者無法選取選取範圍以外的值。 控制項本身不會防止使用者將滑杆移至範圍之外。

 

## <a name="trackbar-notification-messages"></a>資訊提示通知訊息

藉由將父系 [**\_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息傳送給父系，以將其父視窗通知使用者動作。 具有 [Tb] [**\_ HORZ**](trackbar-control-styles.md) 樣式的 [使用中]，會傳送 **WM \_ HSCROLL** 訊息。 具有 [**TBS \_ 垂直**](trackbar-control-styles.md) 樣式的「使用中」的訊息會傳送 **WM \_ VSCROLL** 訊息。 **Wm \_ HSCROLL** 或 **WM \_ VSCROLL** 之 *wParam* 參數的低序位文字包含通知碼。 針對 TB \_ THUMBPOSITION 和 tb \_ THUMBTRACK 通知碼， *wParam* 參數的高序位字組會指定滑杆的位置。 若為所有其他通知碼，高序位字是零;傳送 [**TBM \_ GETPOS**](tbm-getpos.md) 訊息來判斷滑杆的位置。 *LParam* 參數是對等的控制碼。

\_ \_ \_ \_ 只有當使用者使用鍵盤與頁首互動時，系統才會傳送 TB 的底部、tb LINEDOWN、TB 的組合和 tb 的最高通知碼。 \_ \_ 只有當使用者使用滑鼠時，才會傳送 TB THUMBPOSITION 和 tb THUMBTRACK 通知碼。 \_ \_ \_ 在這兩種情況下都會傳送 tb 的 ENDTRACK、TB PAGEDOWN 和 tb PAGEUP 通知碼。 下表列出的是 (的虛擬機器碼程式碼，以及會導致傳送 [**虛擬金鑰代碼**](/windows/desktop/inputdev/virtual-key-codes)通知的滑鼠事件) 的事件。



| 通知碼 | 已傳送的原因                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ 底部        | [**VK \_ 結束**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_KEYUP**](/windows/desktop/inputdev/wm-keyup) (使用者發行了一個傳送相關虛擬機器碼的金鑰)                               |
| TB \_ LINEDOWN      | [**VK \_向右**](/windows/desktop/inputdev/virtual-key-codes)或 [ **\_ 向下 VK**](/windows/desktop/inputdev/virtual-key-codes)     |
| TB 的 \_ 系列        | [**VK \_LEFT**](/windows/desktop/inputdev/virtual-key-codes)或 [ **VK \_ UP**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PAGEDOWN      | [**VK \_接下來**](/windows/desktop/inputdev/virtual-key-codes) (使用者按一下滑杆下方或右邊的頻道)    |
| TB \_ PAGEUP        | [**VK \_之前**](/windows/desktop/inputdev/virtual-key-codes) (使用者按一下滑杆上方或左邊的頻道)  |
| TB \_ THUMBPOSITION | [**WM \_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 遵循 TB \_ THUMBTRACK 通知碼                                         |
| TB \_ THUMBTRACK    | 滑杆移動 (使用者拖曳滑杆)                                                                                    |
| TB \_ TOP           | [**VK \_ 首頁**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>預設的顯示訊息處理

本章節描述由處理常式執行的視窗訊息處理。



| 訊息                                              | 處理已執行                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | 如果已在 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 處理期間設定計時器，則會將它刪除，並在必要時傳送 TB \_ THUMBPOSITION 通知碼。 它一律會傳送 TB 的 \_ ENDTRACK 通知程式碼。                                     |
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                   | 執行其他初始化，例如將行大小、頁面大小和刻度標記頻率設定為預設值。                                                                                                                                 |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)                 | 釋出資源。                                                                                                                                                                                                                                         |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)                   | 重新繪製 [[] [跟蹤條] 視窗。                                                                                                                                                                                                                            |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)           | 使用目前的背景色彩來清除視窗背景。                                                                                                                                                                       |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)           | 傳回 DLGC \_ WANTARROWS 值。                                                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | 適當地處理方向機碼，並傳送 TB 的 \_ 最高、tb 的 \_ 底部、tb \_ PAGEUP、TB \_ PAGEDOWN、TB 的組合 \_ 和 tb \_ LINEDOWN 通知碼。                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | \_如果金鑰是其中一個方向機碼，則傳送 TB 的 ENDTRACK 通知程式碼。                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | 重新繪製 [[] [跟蹤條] 視窗。                                                                                                                                                                                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | 將焦點和滑鼠捕捉設定至字幕。 必要時，它會設定計時器，以決定當使用者按住視窗中的滑鼠按鍵時，滑杆朝滑鼠游標移動的速度。                                      |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | 釋放滑鼠捕捉並終止計時器（如果在進行 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 處理期間設定計時器）。 如有必要，它會傳送 TB 的 \_ THUMBPOSITION 通知碼。 它一律會傳送 TB 的 \_ ENDTRACK 通知程式碼。 |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | 移動滑杆，並 \_ 在追蹤滑鼠 (查看 [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer)) 時傳送 TB 的 THUMBTRACK 通知程式碼。                                                                                                                          |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                        | 繪製跟蹤條。 如果 wParam 參數不是 Null，則控制項會假設值為 HDC，並且使用該裝置內容繪製。                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | 重新繪製 [[] [跟蹤條] 視窗。                                                                                                                                                                                                                            |
| [**WM \_ 大小**](/windows/desktop/winmsg/wm-size)                       | 設定捲軸的維度，如果沒有足夠空間可顯示滑杆，則移除滑杆。                                                                                                                                                      |
| [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer)                     | 抓取滑鼠位置並更新滑杆的位置。  (只有在使用者拖曳滑杆時，才會收到此功能。 )                                                                                                                          |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange)       | 初始化滑杆維度。                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>跟蹤工具工具提示

使用 [ [**tb] \_ 工具提示**](trackbar-control-styles.md) 樣式建立的 [使用的]，會有預設的工具提示控制項。 當使用者使用滑鼠拖曳滑杆時，工具提示會保持可見，並顯示目前的值。

您可以藉由傳送 [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md) 訊息，將新的工具提示控制項指派給程式。 若要取得指派的工具提示控制項的控制碼，請使用 [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md) 訊息。

 

 
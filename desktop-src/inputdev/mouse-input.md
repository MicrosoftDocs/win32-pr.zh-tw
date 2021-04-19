---
title: '滑鼠輸入 (鍵盤和滑鼠輸入) '
description: 本節說明系統如何提供滑鼠輸入給您的應用程式，以及應用程式如何接收和處理該輸入。
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\mouseinput.htm
keywords:
- 使用者輸入、滑鼠輸入
- 捕獲使用者輸入、滑鼠輸入
- 滑鼠輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cc21c9c02a91330483c7b65f7be076bb82e171
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106969551"
---
# <a name="mouse-input-keyboard-and-mouse-input"></a>滑鼠輸入 (鍵盤和滑鼠輸入) 

本節說明系統如何提供滑鼠輸入給您的應用程式，以及應用程式如何接收和處理該輸入。

## <a name="in-this-section"></a>本節內容



| 主題                                                         | 描述                                                       |
|---------------------------------------------------------------|-------------------------------------------------------------------|
| [關於滑鼠輸入](about-mouse-input.md)<br/>         | 本主題討論滑鼠輸入。<br/>                      |
| [使用滑鼠輸入](using-mouse-input.md)<br/>         | 本節涵蓋與滑鼠輸入相關聯的工作。<br/> |
| [滑鼠輸入參考](mouse-input-reference.md)<br/> |                                                                   |



 

### <a name="functions"></a>函式



| Name                                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_TrackMouseEvent**](/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent)             | 當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。 此函數會呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) （如果存在），否則會模擬它。<br/>                                                                                                                                                                                                                                                                                                              |
| [**DragDetect**](/windows/win32/api/winuser/nf-winuser-dragdetect)                          | 擷取滑鼠並追蹤其移動，直到使用者放開左側按鈕、按下 ESC 鍵，或將滑鼠移到指定點周圍的拖曳矩形外。 拖曳矩形的寬度和高度是由 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)函數所傳回的 **Sm \_ CXDRAG** 和 **sm \_ CYDRAG** 值所指定。<br/>                                                                                                                                                               |
| [**EnableMouseInPointer**](/windows/desktop/api/winuser/nf-winuser-enablemouseinpointer) | 讓滑鼠成為指向裝置。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)                          | 抓取視窗的控制碼 (是否有任何) 已捕捉到滑鼠。 一次只能有一個視窗可捕獲滑鼠;無論游標是否在其框線內，此視窗都會收到滑鼠輸入。 <br/>                                                                                                                                                                                                                                                                                                                        |
| [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)          | 抓取滑鼠目前的按兩下時間。 按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。 按兩下時間是在按兩下的第一次和第二次按一下時，可能發生的最大毫秒數。 <br/>                                                                                                                                                                                                              |
| [**GetMouseMovePointsEx**](/windows/win32/api/winuser/nf-winuser-getmousemovepointsex)      | 抓取滑鼠或畫筆之前最多64個座標的歷程記錄。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)                  | 從目前線程中的視窗釋放滑鼠捕捉，並還原一般滑鼠輸入處理。 不論游標的位置為何，已捕捉到滑鼠的視窗都會收到所有的滑鼠輸入，但在游標作用點位於另一個執行緒的視窗中，但在按下滑鼠按鍵時除外。 <br/>                                                                                                                                                                                                          |
| [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)                          | 將滑鼠捕捉設定為屬於目前線程的指定視窗。 當滑鼠停留在捕捉視窗上時，或當滑鼠停留在 [捕捉] 視窗上並按下滑鼠按鍵時， [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)會捕捉滑鼠輸入，而且按鈕仍會關閉。 一次只能有一個視窗能捕捉滑鼠。<br/> 如果滑鼠游標位於另一個執行緒所建立的視窗上方，則只有在滑鼠按鍵關閉時，系統才會將滑鼠輸入直接導向指定的視窗。<br/> |
| [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)          | 設定滑鼠的按兩下時間。 按兩下是按兩下滑鼠按鍵的一連串，第二個是在指定的時間內發生第二個點。 按兩下時間是在按兩下的第一個和第二個點之間可能發生的最大毫秒數。 <br/>                                                                                                                                                                                                                            |
| [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton)                | 反轉或還原左右滑鼠按鍵的意義。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)                | 當滑鼠指標離開視窗，或將滑鼠停留在視窗上一段指定的時間時張貼訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

下列函式已過時。



| 函式                            | 描述                                            |
|-------------------------------------|--------------------------------------------------------|
| [**滑鼠 \_ 事件**](/windows/win32/api/winuser/nf-winuser-mouse_event) | 會合成滑鼠動作並按一下按鈕。<br/> |



 

### <a name="notifications"></a>通知



| Name                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](wm-capturechanged.md)   | 傳送至遺失滑鼠捕捉的視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)     | 當使用者按兩下滑鼠左鍵，而游標位於視窗的工作區時，則會公佈。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                             |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)         | 當使用者按下滑鼠左鍵，而游標位於視窗的工作區時，則會公佈。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                   |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)             | 當使用者放開滑鼠左鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                  |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)     | 當使用者按兩下滑鼠左鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                           |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)         | 當使用者按下滑鼠左鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                 |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)             | 當使用者放開滑鼠左鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                |
| [**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md)     | 當游標在非作用中視窗，且使用者按下滑鼠按鍵時傳送。 只有當子視窗將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數時，父視窗才會接收此訊息。<br/>                                                                                                                                                                                                                                                   |
| [**WM \_ MOUSEHOVER**](wm-mousehover.md)           | 當游標停留在先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定的時間期間，將游標停留在視窗的工作區上時，就會張貼至視窗。<br/>                                                                                                                                                                                                                                                                                               |
| [**WM \_ MOUSEHWHEEL**](wm-mousehwheel.md)         | 當滑鼠的水準滾輪傾斜或旋轉時，傳送至焦點視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。 訊息不應該有內部轉送，因為 **DefWindowProc** 會將它向上傳播到父鏈，直到它找到處理它的視窗為止。<br/>                                                                                                                  |
| [**WM \_ MOUSELEAVE**](wm-mouseleave.md)           | 當游標離開先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定之視窗的工作區時，張貼至視窗。<br/>                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ MOUSEMOVE**](wm-mousemove.md)             | 當游標移動時張貼至視窗。 如果未捕捉到滑鼠，則會將訊息張貼至包含游標的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                                                                          |
| [**WM \_ 滑鼠滾輪**](wm-mousewheel.md)           | 當滑鼠滾輪旋轉時，傳送至焦點視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。 訊息不應該有內部轉送，因為 **DefWindowProc** 會將它向上傳播到父鏈，直到它找到處理它的視窗為止。<br/>                                                                                                                                              |
| [**WM \_ NCHITTEST**](wm-nchittest.md)             | 傳送至視窗，以判斷視窗的哪個部分對應至特定的螢幕座標。 例如，當游標移動時、按下或放開滑鼠按鍵時，或為了回應函式（例如 [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint)）的呼叫時，就會發生這種情況。 如果未捕捉到滑鼠，則會將訊息傳送至游標下的視窗。 否則，訊息會傳送至已捕捉滑鼠的視窗。<br/> |
| [**WM \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md) | 當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                         |
| [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md)     | 當使用者按下滑鼠左鍵，而游標位於視窗的非工作區內時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                               |
| [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md)         | 當使用者放開滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                              |
| [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md) | 當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區內時，即會張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                       |
| [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)     | 當使用者按下滑鼠左鍵，而游標位於視窗的非工作區內時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                             |
| [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)         | 當使用者放開滑鼠左鍵，而游標位於視窗的非工作區時，則會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                            |
| [**WM \_ NCMOUSEHOVER**](wm-ncmousehover.md)       | 當游標停留在視窗的非工作區時，在先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定的期間內，將滑鼠停留在視窗的非工作區上。<br/>                                                                                                                                                                                                                                                                                             |
| [**WM \_ NCMOUSELEAVE**](wm-ncmouseleave.md)       | 當游標離開先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定之視窗的非工作區時，張貼至視窗。<br/>                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md)         | 當游標移至視窗的非工作區中時，張貼至視窗。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                                                        |
| [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) | 當使用者按兩下滑鼠右鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                        |
| [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md)     | 當使用者按下滑鼠右鍵，而游標位於視窗的非工作區時，則會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                              |
| [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md)         | 當使用者放開滑鼠右鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                             |
| [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md) | 當使用者在滑鼠游標位於視窗的非工作區時，按兩下第一個或第二個 X 按鈕時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                      |
| [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)     | 當使用者按第一個或第二個 X 按鈕時，當游標位於視窗的非工作區時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                            |
| [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)         | 當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的非工作區時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。<br/>                                                                                                                                                                                                                           |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md)     | 當使用者按兩下滑鼠右鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                            |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)         | 當使用者按下滑鼠右鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                  |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)             | 當使用者放開滑鼠右鍵，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                                 |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)     | 當使用者在游標位於視窗的工作區時，按兩下第一個或第二個 X 按鈕時公佈。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                      |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)         | 當使用者按下第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。 <br/>                                                                                                                                                                                           |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)             | 當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。 如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。 否則，會將訊息張貼到已捕捉滑鼠的視窗。<br/>                                                                                                                                                                                           |



 

### <a name="structures"></a>結構



| Name                                           | 描述                                                                                                                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MOUSEMOVEPOINT**](/windows/win32/api/winuser/ns-winuser-mousemovepoint)       | 包含螢幕座標中滑鼠位置的相關資訊。<br/>                                                                                                  |
| [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) | 供 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 函式用來追蹤滑鼠指標何時離開視窗，或將滑鼠停留在視窗上一段指定的時間。<br/> |



 

 


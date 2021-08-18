---
title: 關於滑鼠輸入
description: 本主題討論滑鼠輸入。
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- 使用者輸入、滑鼠輸入
- 捕獲使用者輸入、滑鼠輸入
- 滑鼠輸入
- 滑鼠游標
- 游標、滑鼠輸入
- 滑鼠捕捉
- 滑鼠鎖定
- XBUTTONs
- 滑鼠設定
- 滑鼠訊息
- WM_NCHITTEST 訊息
- 滑鼠消失協助工具功能
- 滑鼠聲納協助工具功能
- 滑鼠滾輪
- WM_MOUSEWHEEL 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105787"
---
# <a name="about-mouse-input"></a>關於滑鼠輸入

滑鼠是適用于應用程式的重要但選用的使用者輸入裝置。 妥善撰寫的應用程式應該包含滑鼠介面，但不應該完全依賴滑鼠來取得使用者輸入。 應用程式也應該提供完整的鍵盤支援。

應用程式會以傳送或張貼至其 windows 的訊息形式來接收滑鼠輸入。

本節包含下列主題：

-   [滑鼠游標](#mouse-cursor)
-   [滑鼠捕捉](#mouse-capture)
-   [滑鼠鎖定](#mouse-clicklock)
-   [滑鼠設定](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [滑鼠訊息](#mouse-messages)
    -   [用戶端區域滑鼠訊息](#client-area-mouse-messages)
    -   [非工作區滑鼠訊息](#nonclient-area-mouse-messages)
    -   [WM \_ NCHITTEST 訊息](/windows)
-   [滑鼠聲納](#mouse-sonar)
-   [滑鼠消失](#mouse-vanish)
-   [滑鼠滾輪](#the-mouse-wheel)
-   [視窗啟動](#window-activation)

## <a name="mouse-cursor"></a>滑鼠游標

當使用者移動滑鼠時，系統會在螢幕上移動名為 *滑鼠游標* 的點陣圖。 滑鼠游標包含一個稱為「 *作用* 點」的單圖元點，也就是系統追蹤和辨識為游標位置的點。 當滑鼠事件發生時，包含作用點的視窗通常會收到事件所產生的滑鼠訊息。 視窗不需要使用中，或有鍵盤焦點可以接收滑鼠訊息。

系統會維護控制滑鼠速度的變數，也就是當使用者移動滑鼠時，游標移動的距離。 您可以使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式搭配 **Spi \_ GETMOUSE** 或 **spi \_ SETMOUSE** 旗標來取得或設定滑鼠速度。 如需滑鼠游標的詳細資訊，請參閱資料 [指標](/windows/desktop/menurc/cursors)。

## <a name="mouse-capture"></a>滑鼠捕捉

系統通常會在滑鼠事件發生時，將滑鼠訊息張貼至包含游標作用點的視窗。 應用程式可以使用 [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) 函式將滑鼠訊息路由至特定視窗，來變更此行為。 視窗會接收所有的滑鼠訊息，直到應用程式呼叫 [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) 函式或指定另一個捕獲視窗，或直到使用者按一下另一個執行緒所建立的視窗為止。

當滑鼠捕捉變更時，系統會將 [**WM \_ CAPTURECHANGED**](wm-capturechanged.md) 訊息傳送至遺失滑鼠捕捉的視窗。 訊息的 *lParam* 參數會指定取得滑鼠捕捉的視窗控制碼。

只有前景視窗可以捕獲滑鼠輸入。 當背景視窗嘗試捕捉滑鼠輸入時，它只會接收游標作用點位於視窗可見部分內時所發生滑鼠事件的訊息。

如果視窗必須接收所有滑鼠輸入，即使游標在視窗外移動，捕捉滑鼠輸入也相當有用。 例如，應用程式通常會追蹤滑鼠按鍵向下事件之後的游標位置，直到游標之後，再按下滑鼠按鍵的事件。 如果應用程式尚未捕捉到滑鼠輸入，而且使用者在視窗外放開滑鼠按鍵，則視窗不會收到按鈕的訊息。

執行緒可以使用 [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) 函式來判斷其中一個視窗是否已捕捉到滑鼠。 如果執行緒的其中一個視窗已捕捉到滑鼠， **GetCapture** 就會抓取視窗的控制碼。

## <a name="mouse-clicklock"></a>滑鼠鎖定

滑鼠點擊封鎖協助工具功能可讓使用者在按下滑鼠按鍵時，鎖定主要滑鼠按鍵。 在應用程式中，按鈕仍然會被按下。 若要解除鎖定按鈕，應用程式可以傳送任何滑鼠訊息，或使用者可以按一下任何滑鼠按鍵。 這項功能可讓使用者更輕鬆地進行複雜的滑鼠組合。 例如，具有特定實體限制的人可以更輕鬆地醒目提示文字、拖曳物件或開啟功能表。 如需詳細資訊，請參閱下列旗標和 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)中的備註：

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>滑鼠設定

雖然滑鼠對應用程式而言是重要的輸入裝置，但並非每位使用者都必須有滑鼠。 應用程式可以藉由將 **SM \_ MOUSEPRESENT** 值傳遞至 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式，來判斷系統是否包含滑鼠。

Windows 支援最多三個按鈕的滑鼠。 在三個按鈕的滑鼠上，按鈕會指定為左方、中間和右按鈕。 與滑鼠按鍵相關的訊息和命名常數會使用字母 L、M 和 R 來識別按鈕。 選項按鈕上的按鈕會被視為左按鈕。 雖然 Windows 支援具有多個按鈕的滑鼠，但大部分的應用程式通常會使用左側按鈕，而其他應用程式則使用最少（如果有的話）。

應用程式也可以支援滑鼠滾輪。 您可以按下或旋轉滑鼠滾輪。 按下滑鼠滾輪時，會作為中間的 (第三) 按鈕，將一般中間按鈕訊息傳送至您的應用程式。 當它旋轉時，滾輪訊息會傳送至您的應用程式。 如需詳細資訊，請參閱 [滑鼠滾輪](#the-mouse-wheel) 一節。

應用程式可以支援應用程式命令按鈕。 這些按鈕稱為 X 按鈕，其設計目的是為了讓您更輕鬆地存取網際網路瀏覽器、電子郵件和媒體服務。 按下 X 按鈕時，會將 [**WM \_ APPCOMMAND**](wm-appcommand.md) 訊息傳送至您的應用程式。 如需詳細資訊，請參閱 **WM \_ APPCOMMAND** 訊息中的描述。

應用程式可以藉由將 **SM \_ CMOUSEBUTTONS** 值傳遞至 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式，來判斷滑鼠上的按鈕數目。 若要設定左手使用者的滑鼠，應用程式可以使用 [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) 函式來反轉左右滑鼠按鍵的意義。 將 **SPI \_ SETMOUSEBUTTONSWAP** 值傳遞至 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式是另一種反轉按鈕意義的方法。 但請注意，滑鼠是共用資源，因此反轉按鈕的意義會影響所有應用程式。

## <a name="xbuttons"></a>XBUTTONs

Windows 支援具有五個按鈕的滑鼠。 除了左邊、中間和右方按鈕之外，還提供 XBUTTON1 和 XBUTTON2，可在使用瀏覽器時提供反向和向前流覽。

視窗管理員透過 **WM \_ XBUTTON \* *_ 和 _* WM \_ NCXBUTTON \* *_ 訊息支援 XBUTTON1 和 XBUTTON2。*** 這些訊息中 _ WPARAM 的 HIWORD 包含旗標，指出所按的 X 按鈕。 因為這些滑鼠訊息也可以放在常數 **WM \_ MOUSEFIRST** 和 **WM \_ MOUSELAST** 之間，所以應用程式可以使用 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)來篩選所有滑鼠訊息。

下列支援 XBUTTON1 和 XBUTTON2：

-   [**WM \_ APPCOMMAND**](wm-appcommand.md)
-   [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
-   [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
-   [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
-   [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
-   [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
-   [**WM \_ XBUTTONUP**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

下列 Api 已修改為支援下列按鈕：

-   [**滑鼠 \_ 事件**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

元件應用程式中的子視窗不太可能會直接執行 XBUTTON1 和 XBUTTON2 的命令。 因此，當按一下 X 按鈕時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會將 [**WM \_ APPCOMMAND**](wm-appcommand.md) 訊息傳送至視窗。 **DefWindowProc** 也會將 **WM \_ APPCOMMAND** 訊息傳送至其父視窗。 這與使用滑鼠右鍵叫用操作功能表的方式類似-**DefWindowProc** 會將 [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) 訊息傳送至功能表，並將其傳送到其父系。 此外，如果 **DefWindowProc** 收到最上層視窗的 **WM \_ APPCOMMAND** 訊息，它會使用程式碼 HSHELL APPCOMMAND 來呼叫 shell 攔截 \_ 。

有提供瀏覽器功能、媒體功能、應用程式啟動和電源管理等額外按鍵的鍵盤支援。 如需詳細資訊，請參閱 [流覽和其他功能的鍵盤按鍵](about-keyboard-input.md)。

## <a name="mouse-messages"></a>滑鼠訊息

當使用者移動滑鼠或按下或放開滑鼠按鍵時，滑鼠會產生輸入事件。 系統會將滑鼠輸入事件轉換為訊息，並將它們張貼到適當的執行緒訊息佇列。 當滑鼠訊息張貼的速度比執行緒可以處理的時間更快時，系統會捨棄所有最近的滑鼠訊息。

當游標位於視窗的框線內，或視窗已捕捉到滑鼠時，視窗會在滑鼠事件發生時收到滑鼠訊息。 滑鼠訊息分成兩個群組：用戶端區訊息和非工作區訊息。 一般而言，應用程式會處理用戶端區域訊息，並忽略非工作區訊息。

本節包含下列主題：

-   [用戶端區域滑鼠訊息](#client-area-mouse-messages)
-   [非工作區滑鼠訊息](#nonclient-area-mouse-messages)
-   [WM \_ NCHITTEST 訊息](/windows)

### <a name="client-area-mouse-messages"></a>用戶端區域滑鼠訊息

當滑鼠事件發生在視窗的工作區中時，視窗會收到工作區滑鼠訊息。 當使用者將游標移至工作區中時，系統會將 [**WM \_ MOUSEMOVE**](wm-mousemove.md) 訊息張貼至視窗。 當使用者按下或放開滑鼠按鍵，而游標位於工作區中時，它會張貼下列其中一則訊息。



| 訊息                                       | 意義                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md) | 按兩下滑鼠左鍵。   |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)     | 按滑鼠左鍵。          |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)         | 滑鼠左鍵已放開。         |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) | 按兩下滑鼠左鍵。 |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)     | 按滑鼠中間鍵。        |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)         | 中間的滑鼠按鍵已放開。       |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) | 按兩下滑鼠右鍵。  |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)     | 按滑鼠右鍵。         |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)         | 已放開滑鼠右鍵。        |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md) | 按兩下 X 滑鼠按鍵。       |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)     | 已按下滑鼠按鍵。              |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)         | 已釋放 X 滑鼠按鍵。             |



 

此外，應用程式可以呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 函式，讓系統傳送其他兩個訊息。 當游標停留在某段時間內的工作區時，它會張貼 [**WM \_ MOUSEHOVER**](wm-mousehover.md) 訊息。 當資料指標離開工作區時，它會張貼 [**WM \_ MOUSELEAVE**](wm-mouseleave.md) 訊息。

### <a name="message-parameters"></a>訊息參數

用戶端區域滑鼠訊息的 *lParam* 參數表示游標作用點的位置。 低序位單字表示作用點的 x 座標，而高序位單字表示 y 座標。 座標是以用戶端座標指定。 在用戶端座標系統中，畫面上的所有點都是相對於工作區左上角的座標 (0、0) 來指定。

*WParam* 參數包含旗標，指出滑鼠事件時的另一個滑鼠按鍵和 CTRL 和 SHIFT 鍵的狀態。 當滑鼠訊息處理取決於另一個滑鼠按鍵或 CTRL 或 SHIFT 鍵的狀態時，您可以檢查這些旗標。 *WParam* 參數可以是下列值的組合。



| 值            | 描述                      |
|------------------|----------------------------------|
| **MK \_ 控制項**  | CTRL 鍵已關閉。            |
| **MK \_ LBUTTON**  | 左邊的滑鼠按鍵已關閉。   |
| **MK \_ MBUTTON**  | 中間的滑鼠按鍵已關閉。 |
| **MK \_ RBUTTON**  | 滑鼠右鍵已關閉。  |
| **MK \_ 移位**    | SHIFT 鍵已關閉。           |
| **MK \_ XBUTTON1** | 第一個 X 按鈕已關閉。      |
| **MK \_ XBUTTON2** | 第二個 X 按鈕已關閉。     |



 

### <a name="double-click-messages"></a>Double-Click 訊息

當使用者按下滑鼠按鍵兩次快速連續時，系統會產生按兩下的訊息。 當使用者按一下按鈕時，系統會建立以游標作用點為中心的矩形。 它也會標示發生點擊的時間。 當使用者第二次按一下相同的按鈕時，系統會決定作用點是否仍在矩形內，並計算自第一次按一下後經過的時間。 如果作用點仍在矩形內，且經過時間未超過按兩下超時值，系統就會產生按兩下訊息。

應用程式可以分別使用 [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) 和 [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) 函數來取得和設定按兩下超時值。 或者，應用程式也可以使用 **SPI \_ SETDOUBLECLICKTIME** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，來設定按兩下-超時值。 它也可以將 **spi \_ SETDOUBLECLKWIDTH** 和 **spi \_ SETDOUBLECLKHEIGHT** 旗標傳遞給 **SystemParametersInfo**，以設定系統用來偵測按兩下的矩形大小。 不過，請注意，設定按兩下的 [超時值] 和 [矩形] 會影響所有應用程式。

依預設，應用程式定義的視窗不會收到按兩下訊息。 由於產生按兩下訊息時所牽涉到的系統負擔，因此這些訊息只會針對屬於具有 **CS \_ DBLCLKS** 類別樣式之類別的 windows 而產生。 註冊視窗類別時，您的應用程式必須設定這個樣式。 如需詳細資訊，請參閱 [視窗類別](/windows/desktop/winmsg/window-classes)。

按兩下訊息一律是四個訊息系列中的第三個訊息。 前兩個訊息是第一次按一下時所產生的按鈕和按鈕訊息。 第二次按一下會產生按兩下訊息，後面接著另一個按鈕訊息。 例如，按兩下滑鼠左鍵會產生下列訊息順序：

1.  [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)
2.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)
3.  [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
4.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)

由於視窗一律會在收到按兩下訊息之前收到按鈕下的訊息，因此，應用程式通常會使用按兩下訊息來擴充在按鈕的訊息期間開始的工作。 例如，當使用者按一下 Microsoft 小畫家的色彩選擇區中的色彩時，小畫家會顯示選取區旁的選取色彩。 當使用者按兩下色彩時，小畫家會顯示色彩，並開啟 [**編輯色彩**] 對話方塊。

### <a name="nonclient-area-mouse-messages"></a>非工作區滑鼠訊息

當視窗的任何部分（除了用戶端區域）發生滑鼠事件時，視窗都會收到非工作區滑鼠的訊息。 視窗的非工作區是由其框線、功能表列、標題列、捲軸、視窗功能表、最小化按鈕和最大化按鈕所組成。

系統會產生非工作區訊息，主要供自己使用。 例如，當游標作用點移至視窗的框線時，系統會使用非工作區訊息將游標變更為雙向箭號。 視窗必須將非工作區的滑鼠訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以利用內建的滑鼠介面。

每個用戶端區域滑鼠訊息都有對應的非工作區滑鼠訊息。 這些訊息的名稱很類似，不同之處在于非工作區訊息的命名常數包含字母 NC。 例如，將游標移至非工作區時，會產生 [**wm \_ NCMOUSEMOVE**](wm-ncmousemove.md) 訊息，並在游標位於非工作區時按下滑鼠左鍵，產生 [**wm \_ NCLBUTTONDOWN**](wm-nclbuttondown.md) 訊息。

非工作區滑鼠訊息的 *lParam* 參數是包含游標作用點之 x 和 y 座標的結構。 不同于工作區滑鼠訊息的座標，座標是以螢幕座標（而不是用戶端座標）來指定。 在螢幕座標系統中，畫面上的所有點都是相對於螢幕左上角的座標 (0、0) 。

*WParam* 參數包含點擊測試值，此值表示在非工作區中發生滑鼠事件的位置。 下一節說明點擊測試值的用途。

### <a name="the-wm_nchittest-message"></a>WM \_ NCHITTEST 訊息

每當發生滑鼠事件時，系統會將 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息傳送至包含資料指標作用點的視窗，或是已捕捉到滑鼠的視窗。 系統會使用此訊息來判斷是否要傳送工作區或非工作區的滑鼠訊息。 必須接收滑鼠移動和滑鼠按鍵訊息的應用程式必須將 **WM \_ NCHITTEST** 訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。

[**WM \_ NCHITTEST**](wm-nchittest.md)訊息的 *lParam* 參數包含游標作用點的螢幕座標。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會檢查座標，並傳回指出作用點位置的點擊測試值。 點擊測試值可以是下列其中一個值。



| 值             | 作用點的位置                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | 在沒有調整大小框線的視窗框線中。                                                                                                                                       |
| **HTBOTTOM**      | 在視窗的下水準框線中。                                                                                                                                                         |
| **HTBOTTOMLEFT**  | （在視窗框線的左下角）。                                                                                                                                                        |
| **HTBOTTOMRIGHT** | 在視窗框線的右下角。                                                                                                                                                       |
| **HTCAPTION**     | 在標題列中。                                                                                                                                                                                     |
| **HTCLIENT**      | 在工作區中。                                                                                                                                                                                   |
| **HTCLOSE**       | 在 [ **關閉** ] 按鈕中。                                                                                                                                                                              |
| **HTERROR**       | 在螢幕背景上或 windows (與 HTNOWHERE 相同的分隔線上，不同之處在于 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會產生系統嗶聲，指出) 錯誤。 |
| **HTGROWBOX**     | 在 [大小] 方塊中 (與 **HTSIZE**) 相同。                                                                                                                                                                 |
| **HTHELP**        | **在 [說明] 按鈕中**。                                                                                                                                                                               |
| **HTHSCROLL**     | 水準捲軸。                                                                                                                                                                         |
| **HTLEFT**        | 視窗的左框線。                                                                                                                                                                     |
| **HTMENU**        | 在功能表中。                                                                                                                                                                                          |
| **HTMAXBUTTON**   | 在 [ **最大化** ] 按鈕中。                                                                                                                                                                           |
| **HTMINBUTTON**   | 在 [ **最小化** ] 按鈕中。                                                                                                                                                                           |
| **HTNOWHERE**     | 在螢幕背景或視窗之間的分隔線上。                                                                                                                                     |
| **HTREDUCE**      | 在 [ **最小化** ] 按鈕中。                                                                                                                                                                           |
| **HTRIGHT**       | 視窗的右框線。                                                                                                                                                                    |
| **HTSIZE**        | 在 [大小] 方塊中 (與 **HTGROWBOX**) 相同。                                                                                                                                                              |
| **HTSYSMENU**     | 在 [ **系統** ] 功能表或子視窗的 [ **關閉** ] 按鈕中。                                                                                                                                    |
| **HTTOP**         | 在視窗的上水準框線中。                                                                                                                                                         |
| **HTTOPLEFT**     | 在視窗框線的左上角。                                                                                                                                                        |
| **HTTOPRIGHT**    | 在視窗框線的右上角。                                                                                                                                                       |
| **HTTRANSPARENT** | 在目前由相同執行緒中的另一個視窗所涵蓋的視窗中。                                                                                                                                 |
| **HTVSCROLL**     | 在垂直捲動條中。                                                                                                                                                                         |
| **HTZOOM**        | 在 [ **最大化** ] 按鈕中。                                                                                                                                                                           |



 

如果游標位於視窗的工作區中， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會將 **HTCLIENT** 點擊測試值傳回至視窗程式。 當視窗程式將此程式碼傳回給系統時，系統會將游標作用點的螢幕座標轉換成用戶端座標，然後張貼適當的用戶端區域滑鼠訊息。

當游標作用點位於視窗的非工作區時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會傳回其中一個其他的點擊測試值。 當視窗程式傳回這些點擊測試值的其中一個時，系統會張貼非工作區的滑鼠訊息，將點擊測試值放在訊息的 *wParam* 參數中，並在 *lParam* 參數中放置游標座標。

## <a name="mouse-sonar"></a>滑鼠聲納

當使用者按下並放開 CTRL 鍵時，滑鼠聲納協助工具功能會短暫地顯示指標周圍的數個同心圓。 這項功能可協助使用者在畫面上找出不整齊的滑鼠指標，或解析度設定為 high、品質不佳的監視器，或對視力受損的使用者。 如需詳細資訊，請參閱 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)中的下列旗標：

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>滑鼠消失

當使用者輸入時，滑鼠消失的協助工具功能會隱藏指標。 當使用者移動滑鼠時，滑鼠指標會再次出現。 這項功能可防止指標遮蔽輸入的文字，例如電子郵件或其他檔。 如需詳細資訊，請參閱 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)中的下列旗標：

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>滑鼠滾輪

滑鼠滾輪結合滾輪和滑鼠按鍵的功能。 輪子有離散的分隔凹槽。 當您旋轉滾輪時，會在每個凹槽出現時，將輪子訊息傳送至您的應用程式。 滾輪按鈕也可以像一般的 Windows 中間 (第三) 按鈕一樣運作。 按下並放開滑鼠滾輪會傳送標準的 [**WM \_ MBUTTONUP**](wm-mbuttonup.md) 和 [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) 訊息。 按兩下第三個按鈕會傳送標準的 [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) 訊息。

透過 [**WM \_ 滑鼠滾輪**](wm-mousewheel.md) 訊息可支援滑鼠滾輪。

旋轉滑鼠會將 [**WM \_ 滑鼠滾輪**](wm-mousewheel.md) 訊息傳送至焦點視窗。 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。 此訊息不應該有內部轉送，因為 **DefWindowProc** 會將它傳播到父鏈上，直到找到處理它的視窗為止。

### <a name="determining-the-number-of-scroll-lines"></a>決定捲軸的數目

應用程式應該使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來抓取檔的行數， (輪子凹槽) 的捲軸操作。 若要取出行數，應用程式可以進行下列呼叫：


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



變數 "pulScrollLines" 會指向不帶正負號的整數值，此值會在滑鼠滾輪旋轉時，收到建議的行數，而不會有輔助按鍵：

-   如果此數位為0，則不會進行任何滾動。
-   如果這個數位是 **滾輪 \_ PAGESCROLL**，則應該在捲軸的 page down 或 page up 區域中，將輪子轉譯為按一下一次。
-   如果要滾動的行數大於可看見的行數，則捲軸操作也應解釋為 page down 或 page up 操作。

捲軸數目的預設值將會是3。 如果使用者使用主控台中的滑鼠屬性工作表來變更捲軸的數目，作業系統會將 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) 訊息廣播到所有最上層視窗，並指定 **SPI \_ SETWHEELSCROLLLINES** 。 當應用程式收到 **WM \_ SETTINGCHANGE** 訊息時，它會呼叫下列程式碼來取得新的捲軸數目：


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>滾動的控制項

下表列出具有滾動功能的控制項 (包括使用者) 所設定的捲軸。 

| 控制                 | 捲動                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 編輯控制項            | 垂直和水準。                                                                                                                                                |
| 清單方塊控制項        | 垂直和水準。                                                                                                                                                |
| 下拉式方塊               | 若未卸載，每個捲軸都會抓取下一個或上一個專案。 當卸載時，每個都會將訊息轉送至清單方塊，並據此進行滾動。 |
| CMD (命令列)       | 垂直。                                                                                                                                                               |
| 樹狀目錄檢視               | 垂直和水準。                                                                                                                                                |
| [清單檢視]               | 垂直和水準。                                                                                                                                                |
| 向上/向下滾動         | 一次一個專案。                                                                                                                                                     |
| 捲軸捲軸        | 一次一個專案。                                                                                                                                                     |
| Microsoft Rich Edit 1。0 | 垂直。 請注意，Exchange 用戶端有自己的清單視圖版本和沒有滾輪支援的樹狀檢視控制項。                                        |
| Microsoft Rich Edit 2。0 | 垂直。                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>使用滾輪偵測滑鼠

若要判斷具有滾輪的滑鼠是否已連接，請使用 **SM \_ MOUSEWHEELPRESENT** 呼叫 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 。 傳回值 **TRUE** 表示滑鼠已連接。

下列範例是來自多行編輯控制項的視窗程式：


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>視窗啟動

當使用者按一下非使用中最上層視窗或非作用中最上層視窗的子視窗時，系統會將 [**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md) 訊息 (傳送給其他) 至最上層或子視窗。 系統會在將 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息張貼至視窗之後，但在張貼按鈕的訊息之前傳送此訊息。 當將 **WM \_ MOUSEACTI加值稅E** 傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式時，系統會啟動最上層視窗，然後將按鈕的訊息張貼至最上層或子視窗。

藉由處理 [**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md)，視窗可以控制最上層視窗是否會因為滑鼠點擊的結果而變成使用中視窗，以及所按下的視窗是否會收到後續的按鈕訊息。 其運作方式是在處理 **WM \_ MOUSEACTI加值稅E** 之後，傳回下列其中一個值。



| 值                    | 意義                                                              |
|--------------------------|----------------------------------------------------------------------|
| **MA \_ 啟用**         | 啟用視窗，而且不捨棄滑鼠訊息。         |
| **MA \_ NOACTI加值稅E**       | 不會啟動視窗，也不會捨棄滑鼠訊息。 |
| **MA \_ ACTI加值稅EANDEAT**   | 啟用視窗並捨棄滑鼠訊息。                 |
| **MA \_ NOACTI加值稅EANDEAT** | 不會啟動視窗，但會捨棄滑鼠訊息。         |

## <a name="see-also"></a>另請參閱

[利用 High-Definition 滑鼠移動](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)
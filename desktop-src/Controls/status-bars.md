---
title: '狀態列 (Windows 控制項) '
description: 狀態列是父視窗底部的水準視窗，其中應用程式可以顯示各種類型的狀態資訊。
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106969547"
---
# <a name="status-bars-windows-controls"></a>狀態列 (Windows 控制項) 

*狀態列* 是父視窗底部的水準視窗，其中應用程式可以顯示各種類型的狀態資訊。 狀態列可以分割成多個部分，以顯示一種以上的資訊。 下列螢幕擷取畫面顯示 Microsoft Windows 油漆應用程式中的狀態列。 在此情況下，狀態列會包含文字「若要協助，請按一下 [說明] 功能表上的 [說明主題]。 狀態列是視窗底部的區域，其中包含解說文字和座標資訊。

![繪圖應用程式的螢幕擷取畫面，包含包含線上說明相關提示的狀態列](images/sb-paint.png)

本節包含下列主題。

-   [類型和樣式](#types-and-styles)
-   [大小和高度](#size-and-height)
-   [多部分的狀態列](#multiple-part-status-bars)
-   [狀態列文字作業](#status-bar-text-operations)
-   [擁有者繪製的狀態列](#owner-drawn-status-bars)
-   [簡單模式狀態列](#simple-mode-status-bars)
-   [預設狀態列訊息處理](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>類型和樣式

狀態列的預設位置是在父視窗的底部，但您可以指定 [**CCS \_ top**](common-control-styles.md) 樣式，讓它出現在父視窗的工作區頂端。

您可以指定 [**SBARS \_ SIZEGRIP**](status-bar-styles.md) 樣式，在狀態列的右端包含調整大小的底框。

> [!Note]  
> 不建議結合 [**CCS \_ TOP**](common-control-styles.md) 和 [**SBARS \_ SIZEGRIP**](status-bar-styles.md) 樣式，因為產生的調整大小底框無法正常運作。

 

## <a name="size-and-height"></a>大小和高度

狀態列的視窗程式會自動設定視窗的初始大小和位置，並忽略 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數中指定的值。 這個寬度與父視窗工作區的寬度相同。 高度是根據目前在狀態列裝置內容中所選取之字型的度量，以及視窗框線的寬度。

視窗程式會在每次收到 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時，自動調整狀態列的大小。 一般而言，父視窗的大小變更時，父視窗會將 **WM \_ 大小** 訊息傳送到狀態列。

應用程式可以藉由傳送 [**SB \_ SETMINHEIGHT**](sb-setminheight.md) 訊息（以圖元為單位）來設定狀態列的繪圖區域最小高度。 繪圖區域不包括視窗框線。 最小高度適用于在主控描繪的狀態列中繪製。 如需詳細資訊，請參閱本章稍後的主控描繪 [狀態列](#owner-drawn-status-bars) 。

您可以藉由傳送 [**SB \_ GETBORDERS**](sb-getborders.md) 訊息的時間範圍，來取得狀態列的框線寬度。 訊息包含接收寬度之三個元素陣列的位址。

## <a name="multiple-part-status-bars"></a>Multiple-Part 狀態列

狀態列可以有許多不同的部分，每個部分會顯示不同的文字行。 您可以藉由傳送 [**SB \_ SETPARTS**](sb-setparts.md) 訊息給視窗，並指定要建立的部分數目和整數陣列的位址，將狀態列分割成各部分。 陣列中每個元件都包含一個元素，而每個元素都會指定元件右邊緣的用戶端座標。

狀態列的最大值為256個部分，但應用程式通常使用的數量遠低於該部分。 您可以藉由傳送 [**SB \_ GETPARTS**](sb-getparts.md) 訊息的時間範圍，抓取狀態列中的元件計數，以及每個元件右邊緣的座標。

## <a name="status-bar-text-operations"></a>狀態列文字作業

您可以藉由傳送 [**SB \_ SETTEXT**](sb-settext.md) 訊息、指定元件以零為起始的索引、要在元件中繪製之字串的位址，以及用來繪製字串的技巧，來設定狀態列任何部分的文字。 繪圖技術會判斷文字是否有框線，以及框線的樣式（如果有的話）。 它也會決定父視窗是否負責繪製文字。 如需詳細資訊，請參閱以下的主控描繪 [狀態列](#owner-drawn-status-bars) 一節。

根據預設，文字會在狀態列的指定部分中靠左對齊。 您可以 \\ 在文字中內嵌定位字元 (t) ，或將其靠右對齊。 單一索引標籤字元右邊的文字置中，而第二個定位字元右邊的文字靠右對齊。

若要從狀態列取出文字，請使用 [**sb \_ GETTEXTLENGTH**](sb-gettextlength.md) 和 [**sb \_ GETTEXT**](sb-gettext.md) 訊息。

如果您的應用程式使用只有一個部分的狀態列，您可以使用 [**wm \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)、 [**wm \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)和 [**wm \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) 訊息來執行文字作業。 這些訊息只會處理索引為零的部分，可讓您將狀態列視為靜態文字控制項。

若要顯示未建立狀態列的狀態行，請使用 [**DrawStatusText**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) 函數。 函式使用相同的技術，將狀態繪製為狀態列的視窗程式，但不會自動設定狀態資訊的大小和位置。 呼叫函式時，您必須指定狀態資訊的大小和位置，以及要在其中繪製它之視窗的裝置內容。

## <a name="owner-drawn-status-bars"></a>Owner-Drawn 狀態列

您可以將狀態列的個別部分定義為主控描繪的部分。 使用這項技術可讓您擁有更多的控制權，而不是視窗元件的外觀。 例如，您可以顯示點陣圖而非文字，或使用不同的字型來繪製文字。

若要將視窗元件定義為主控描繪，請將 [**SB \_ SETTEXT**](sb-settext.md) 訊息傳送至狀態列，並指定部分和 SBT \_ OWNERDRAW 繪圖技術。 當 \_ 指定 SBT OWNERDRAW 時， *lParam* 參數是應用程式在繪製元件時可使用的32位應用程式定義值。 例如，您可以指定字型控制碼、點陣圖控制碼、字串的位址等等。

當狀態列需要繪製擁有者繪製的元件時，它會將 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息傳送至父視窗。 訊息的 *wParam* 參數是狀態列的子視窗識別碼，而 *LParam* 參數是 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構的位址。 父視窗會使用結構中的資訊來繪製元件。 針對狀態列的主控描繪部分， **DRAWITEMSTRUCT** 包含下列資訊。



| member         | 描述                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | 明確請勿使用。                                                                                                 |
| **CtlID**      | 狀態列的子視窗識別碼。                                                                             |
| **itemID**     | 要繪製之部分的以零為基底的索引。                                                                              |
| **itemAction** | 明確請勿使用。                                                                                                 |
| **itemState**  | 明確請勿使用。                                                                                                 |
| **hwndItem**   | 狀態列的控制碼。                                                                                              |
| **hDC**        | 狀態列的裝置內容控制碼。                                                                        |
| **rcItem**     | 要繪製之視窗部分的座標。 座標是相對於狀態列的左上角。   |
| **itemData**   | 在 [**SB \_ SETTEXT**](sb-settext.md)訊息的 *lParam* 參數中指定的應用程式定義32位值。 |



 

## <a name="simple-mode-status-bars"></a>簡單模式狀態列

您可以藉由將一個 [**SB \_ 簡單**](sb-simple.md) 的訊息傳送給它，將狀態列放在「簡單模式」中。 簡單模式的狀態列只會顯示一個部分。 當視窗的文字設定完成時，視窗會失效，但在下一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)之前不會重新繪製。 藉由將重繪視窗的次數降到最低，等候訊息可減少螢幕閃爍。 簡單模式狀態列適用于顯示功能表項目的解說文字，而使用者會在功能表中滾動。

在簡單模式下，狀態列所顯示的字串會與在簡單模式中顯示的字串分開維護。 這表示您可以在簡單模式下放置視窗、設定它的文字，並切換回簡單模式，而不會變更簡單模式文字。

設定簡單模式狀態列的文字時，您可以指定 SBT OWNERDRAW 以外的任何繪圖技術 \_ 。 簡單模式的狀態列不支援「擁有者繪圖」。

## <a name="default-status-bar-message-processing"></a>預設狀態列訊息處理

本節說明由預先定義之 [**STATUSCLASSNAME**](common-control-window-classes.md) 類別的視窗程式所處理的訊息。



| 訊息               | 預設處理                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ 建立**        | 初始化狀態列。                                                                                                                                                                                                                                              |
| **WM 損 \_ 毀**       | 釋出配置給狀態列的資源。                                                                                                                                                                                                                            |
| **WM \_ GETFONT**       | 傳回目前字型的控制碼，狀態列會用它來繪製其文字。                                                                                                                                                                                         |
| **WM \_ GETTEXT**       | 從狀態列的第一個部分將文字複製到緩衝區。 它會傳回32位值，這個值會指定文字的長度（以字元為單位），以及用來繪製文字的技巧。                                                                                |
| **WM \_ GETTEXTLENGTH** | 傳回32位值，這個值會指定狀態列第一個部分中文字的長度（以字元為單位），以及用來繪製文字的技巧。                                                                                                                  |
| **WM \_ NCHITTEST**     | 如果滑鼠游標位於調整大小的底框中，則傳回 HTBOTTOMRIGHT 值，使系統顯示調整大小游標。 如果滑鼠游標不在調整大小的底框中，狀態列就會將此訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。 |
| **WM \_ 油漆**         | 繪製狀態列的無效區域。 如果 *wParam* 參數不是 **Null**，則控制項會假設值為 HDC，並且使用該裝置內容繪製。                                                                                               |
| **WM \_ SETFONT**       | 在狀態列的裝置內容中選取字型控點。                                                                                                                                                                                                      |
| **WM \_ SETTEXT**       | 使用預設的繪圖作業 (指定為零) ，將指定的文字複製到狀態列的第一個部分。 如果成功，則傳回 **TRUE** ，否則傳回 **FALSE** 。                                                                                       |
| **WM \_ 大小**          | 根據父視窗工作區的目前寬度和狀態列目前字型的高度，調整狀態列的大小。                                                                                                                               |



 

 

 

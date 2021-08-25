---
title: 關於靜態控制項
description: 本主題討論如何使用靜態控制項。
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa9b77ff7c1357cede494f60c1d345d0eb4b8f5f8cf63ace13176179d385794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922298"
---
# <a name="about-static-controls"></a>關於靜態控制項

應用程式通常會使用靜態控制項來標記其他控制項或分隔控制項群組。 雖然靜態控制項是子視窗，但無法選取。 因此，他們無法接收鍵盤焦點，也不能有鍵盤介面。 具有 SS 通知樣式的靜態控制項會 \_ 收到滑鼠輸入，當使用者按一下或按兩下控制項時，會通知父視窗。 靜態控制項屬於靜態視窗類別。

雖然可以在重迭、快顯視窗和子視窗中使用靜態控制項，但它們是設計來在對話方塊中使用，而系統會將其行為標準化。 藉由在對話方塊外使用靜態控制項，開發人員會提高應用程式可能以非標準方式運作的風險。 開發人員通常會在對話方塊中使用靜態控制項，或使用 SS \_ OWNERDRAW 樣式來建立自訂的靜態控制項。

本節將討論下列主題。

-   [靜態控制項類型](#static-control-types)
    -   [簡單圖形靜態控制項](#simple-graphics-static-control)
    -   [文字靜態控制項](#text-static-control)
    -   [影像靜態控制項](#image-static-control)
    -   [擁有者繪製的靜態控制項](#owner-drawn-static-control)
-   [靜態控制項預設訊息處理](#static-control-default-message-processing)

## <a name="static-control-types"></a>靜態控制項類型

靜態控制項有四種類型。 每個類型都有一或多個 [靜態控制項樣式](static-control-styles.md)。

-   [簡單圖形靜態控制項](#simple-graphics-static-control)
-   [文字靜態控制項](#text-static-control)
-   [影像靜態控制項](#image-static-control)
-   [擁有者繪製的靜態控制項](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>簡單圖形靜態控制項

簡單的圖形靜態控制項會顯示框架或填滿的矩形。 您可以使用許多樣式來繪製框架，包括黑色、灰色或白色。 此外，您可以繪製具有蝕刻樣式的框架，以提供三維外觀。 框架樣式包括 SS \_ BLACKFRAME、ss \_ GRAYFRAME、ss \_ WHITEFRAME、SS \_ ETCHEDHORZ、SS \_ ETCHEDVERT 和 SS \_ ETCHEDFRAME。

您可以使用下列三種樣式的其中一種來填滿矩形：黑色、灰色或白色。 這些樣式是由常數 SS \_ BLACKRECT、ss \_ GRAYRECT 和 SS WHITERECT 所定義 \_ 。

圖形樣式無法合併。

### <a name="text-static-control"></a>文字靜態控制項

文字靜態控制項會以五種樣式的其中一種來顯示矩形中的文字：

-   靠左對齊而不自動換行
-   使用自動換行來靠左對齊
-   置中
-   靠右對齊
-   simple

這些樣式是由常數 SS \_ LEFTNOWORDWRAP、ss \_ LEFT、ss \_ CENTER、SS \_ RIGHT 和 ss \_ 分別定義。 系統會以預先定義的方式重新排列這些控制項中的文字，但不會重新排列的「簡單」文字除外。

應用程式可以在任何時間使用 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) 函式或 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息來變更文字靜態控制項中的文字。

系統會盡可能顯示靜態控制項中的文字，以及不適合的剪輯。 若要為控制項計算適當的大小，請取得文字的字型度量。 如需字型和字型度量的詳細資訊，請參閱字型 [和文字](/windows/desktop/gdi/fonts-and-text)。

根據預設，靜態控制項的視窗文字（如其他控制項）可以包含 & 符號，以將下列字元定義為控制項的快速鍵 (或在大部分的靜態控制項中，針對其標籤的控制項（定位順序中的下一個控制項）) 。 如果您想要在文字中顯示符號，而不是使用它們來定義快捷方式，請包含 SS \_ NOPREFIX 樣式。

### <a name="image-static-control"></a>影像靜態控制項

影像靜態控制項可以顯示點陣圖、圖示 (包括動畫圖標) 或增強的中繼檔。 特定靜態控制項所顯示的圖形類型取決於控制項的樣式： SS \_ 點陣圖、ss \_ 圖示或 SS \_ ENHMETAFILE。 應用程式會在建立控制項時指定樣式，同時也會指定要顯示之控制項的點陣圖、圖示或中繼檔控制碼。 建立控制項之後，應用程式可以將不同的圖形與控制項產生關聯，方法是將其傳送至 [**STM \_ SETIMAGE**](stm-setimage.md) 訊息，並指定新繪圖物件的控制碼。 應用程式可以藉由傳送 [**.Stm \_ GETIMAGE**](stm-getimage.md) 訊息，取得目前與靜態控制項相關聯之繪圖物件的控制碼。 應用程式會使用 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 函數，將訊息傳送至靜態控制項。

### <a name="owner-drawn-static-control"></a>Owner-Drawn 靜態控制項

藉由使用 SS \_ OWNERDRAW 樣式，應用程式可能會負責繪製靜態控制項。 擁有者繪製之靜態控制項的父視窗 (其擁有者) 會在每次需要繪製靜態控制項時收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。 此訊息包含 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) 結構的指標，其中包含主控視窗繪製控制項時，擁有者視窗所使用的資訊。

## <a name="static-control-default-message-processing"></a>靜態控制項預設訊息處理

預先定義之靜態控制項視窗類別的視窗程式，會針對靜態控制程式未處理的所有訊息執行預設處理。 當靜態控制項會針對任何訊息傳回 **FALSE** 時，預先定義的視窗程式會檢查訊息，並執行下表所述的預設動作。 在資料表中，文字靜態控制項是一種靜態控制項，其樣式為 SS \_ LEFTNOWORDWRAP、ss \_ LEFT、ss \_ CENTER、SS \_ RIGHT 或 SS \_ SIMPLE。



| 訊息                                                | 預設動作                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)                     | 載入繪圖物件，並將視窗大小調整為物件的大小，適用于圖形靜態控制項。 其他靜態控制項不採取任何動作。 |
| [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)                   | 釋出並終結圖形靜態控制項的任何繪圖物件。 其他靜態控制項不採取任何動作。                              |
| [**\_啟用 WM**](/windows/desktop/winmsg/wm-enable)                     | 重新繪製可見的靜態控制項。                                                                                                           |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)             | 傳回 **TRUE**，表示控制項會清除背景。                                                                             |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)             | 傳回 DLGC \_ 靜態。                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | 傳回文字靜態控制項字型的控制碼。                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | 傳回復制的字元數。                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)       | 傳回文字靜態控制項文字的長度（以字元為單位）。                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)     | 如果控制項樣式為 SS NOTIFY，則傳送 [STN \_ DBLCLK](stn-dblclk.md) 通知碼給父視窗 \_ 。                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)         | 如果控制項樣式為 SS NOTIFY，則將 [STN \_ 按一下](stn-clicked.md) 的通知程式碼傳送至父視窗 \_ 。                            |
| [**WM \_ NCLBUTTONDBLCLK**](/windows/desktop/inputdev/wm-nclbuttondblclk) | 如果控制項樣式為 SS NOTIFY，則傳送 [STN \_ DBLCLK](stn-dblclk.md) 通知碼給父視窗 \_ 。                              |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown)     | 如果控制項樣式為 SS NOTIFY，則將 [STN \_ 按一下](stn-clicked.md) 的通知程式碼傳送至父視窗 \_ 。                            |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)             | 如果控制項樣式為 SS NOTIFY，則會傳回 HTCLIENT \_ ，否則會傳回 HTTRANSPARENT。                                                      |
| [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint)                          | 重新繪製控制項。                                                                                                                       |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                   | 設定文字靜態控制項的字型和重繪。                                                                                        |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | 設定文字靜態控制項的文字和重畫。                                                                                        |



 

預先定義的視窗程式會將所有其他訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，以進行預設處理。

 

 
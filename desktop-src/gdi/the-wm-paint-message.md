---
description: 一般而言，應用程式會在視窗中繪製以回應 WM \_ 繪製訊息。
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: WM_PAINT 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965178"
---
# <a name="the-wm_paint-message"></a>WM \_ 油漆訊息

一般而言，應用程式會在視窗中繪製以回應 [**WM \_ 繪製**](wm-paint.md) 訊息。 當視窗的變更已改變工作區的內容時，系統會將此訊息傳送至視窗程式。 只有當應用程式訊息佇列中沒有其他訊息時，系統才會傳送訊息。

收到 [**WM \_ 油漆**](wm-paint.md) 訊息時，應用程式可以呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 來取得工作區的顯示裝置內容，並在 GDI 函式的呼叫中使用它來執行更新工作區所需的任何繪製作業。 完成繪圖作業之後，應用程式會呼叫 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函式來釋放顯示裝置內容。

在 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 傳回顯示裝置內容之前，系統會為指定的視窗準備裝置內容。 它會先將裝置內容的裁剪區域設定為等於需要更新之視窗部分的交集，以及使用者可以看見的部分。 只有已變更之視窗的部分會重繪。 在此區域外部繪製的嘗試會遭到裁剪，而且不會出現在畫面上。

系統也可以在 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)傳回之前，將 [**Wm \_ NCPAINT**](wm-ncpaint.md)和 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)訊息傳送至視窗程式。 這些訊息會指示應用程式繪製非工作區和視窗背景。 *非工作區* 是位於工作區之外之視窗的一部分。 此區域包含標題列、視窗功能表 (也稱為 **系統** 功能表) 和捲軸等功能。 大部分的應用程式都依賴預設視窗函式 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，以繪製此區域，因此會將 **WM \_ NCPAINT** 訊息傳遞至此函式。 *視窗背景* 是在其他繪圖作業開始之前，填滿視窗的色彩或模式。 背景涵蓋了先前在視窗中或視窗下畫面上的任何影像。 如果視窗屬於具有類別背景筆刷的視窗類別，則 **DefWindowProc** 函式會自動繪製視窗背景。

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 會填滿 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) 結構，其中包含要更新之視窗部分的維度，以及指出是否已繪製視窗背景的旗標。 應用程式可以使用此資訊來優化繪圖。 例如，它可以使用 **rcPaint** 成員所指定之更新區域的維度，將只繪製到需要更新之視窗的部分。 如果應用程式有非常簡單的輸出，它可以忽略更新區域，然後在整個視窗中繪製，依賴系統來捨棄 (的剪輯) 任何不需要的輸出。 由於系統剪輯繪圖是延伸在裁剪區域外部，因此只會顯示位於更新區域中的繪圖。

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 會將視窗的更新區域設定為 **Null**。 這會清除區域，使其無法產生後續的 [**WM \_ 繪製**](wm-paint.md) 訊息。 如果應用程式處理 **WM \_ 油漆** 訊息，但未呼叫 **BeginPaint** 或清除更新區域，則只要區域不是空的，應用程式就會繼續接收 **WM \_ 油漆** 訊息。 在所有情況下，應用程式都必須先清除更新區域，再從 **WM \_ 油漆** 訊息傳回。

在應用程式完成繪製之後，它應該呼叫 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)。 針對大部分的 windows， **EndPaint** 會釋出顯示裝置內容，使其可供其他視窗使用。 **EndPaint** 也會顯示插入號（如果先前已由 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)隱藏）。 **BeginPaint** 會隱藏插入號，以防止繪圖作業損毀。

-   [更新區域](the-update-region.md)
-   [使更新區域失效並進行驗證](invalidating-and-validating-the-update-region.md)
-   [正在抓取更新區域](retrieving-the-update-region.md)
-   [排除更新區域](excluding-the-update-region.md)
-   [同步和非同步繪圖](synchronous-and-asynchronous-drawing.md)

 

 

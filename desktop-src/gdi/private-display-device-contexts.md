---
description: 私用裝置內容可讓應用程式在每次應用程式必須在視窗中繪製時，避免每次都必須抓取並初始化顯示裝置內容。
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: 私用顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512852"
---
# <a name="private-display-device-contexts"></a>私用顯示裝置內容

*私用裝置內容* 可讓應用程式在每次應用程式必須在視窗中繪製時，避免每次都必須抓取並初始化顯示裝置內容。 私用裝置內容適用于需要對裝置內容的屬性值進行許多變更，以準備進行繪製的 windows。 私用裝置內容可減少準備裝置內容所需的時間，因而縮短在視窗中執行繪圖所需的時間。

應用程式會指示系統建立視窗的私用裝置內容，方法是 \_ 在視窗類別中指定 CS OWNDC 樣式。 系統會在每次建立屬於類別的新視窗時建立唯一的私用裝置內容。 一開始，私用裝置內容具有與一般裝置內容相同的屬性預設值，但應用程式可以隨時修改這些屬性。 系統會保留視窗存留期內的裝置內容變更，或直到應用程式進行其他變更為止。

應用程式可以在建立視窗之後隨時使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式，以取得私人裝置內容的控制碼。 應用程式必須只抓取一次控制碼。 之後，它可以保留並使用控制碼任意次數。 因為私用裝置內容不是顯示裝置內容快取的一部分，所以應用程式不需要使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放裝置內容。

系統會自動調整裝置內容，以反映視窗的變更，例如移動或調整大小。 這樣可確保所有重迭的視窗一律會正確地裁剪;也就是說，應用程式不需要採取任何動作來確保裁剪。 不過，系統不會修改裝置內容以包含更新區域。 因此，在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時，應用程式必須藉由呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 或藉由抓取更新區域並與目前的裁剪區域交集，來併入更新區域。 如果應用程式未呼叫 **BeginPaint**，則必須使用 [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) 或 [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) 函數來明確驗證更新區域。 如果應用程式不會驗證更新區域，則視窗會收到一系列的一系列的 **WM \_ 油漆** 訊息。

由於 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 會在視窗顯示時隱藏插入號，因此呼叫 **BeginPaint** 的應用程式也應該呼叫 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函數來還原插入號。 **EndPaint** 對私用裝置內容沒有任何其他效果。

雖然私用裝置內容很方便使用，但它在系統資源方面是記憶體密集的，需要儲存800或更多的位元組。 當效能考慮超過儲存體成本時，建議使用私用裝置內容。

將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至應用程式時，系統會包含私用裝置內容。 當應用程式或系統處理這些訊息時，私用裝置內容的目前選取範圍（包括對應模式）會生效。 為了避免不適當的效果，系統會在清除背景時使用邏輯座標;例如，它會使用 [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) 函式來取出要清除之區域的邏輯座標，並將這些座標傳遞給 [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect) 函式。 處理這些訊息的應用程式可以使用類似的技術。

應用程式可以使用 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來強制系統傳回具有私用裝置內容之視窗的一般裝置內容。 這有助於在不變更私用裝置內容的目前屬性值的情況下，對視窗執行快速觸控。

 

 

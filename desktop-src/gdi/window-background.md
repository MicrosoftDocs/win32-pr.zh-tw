---
description: 視窗背景是在視窗開始繪圖之前用來填滿工作區的色彩或模式。
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: 視窗背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819f3bf333728909bdd0e374d41b7665f0517bcc17666b88c58f610e0127d942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848938"
---
# <a name="window-background"></a>視窗背景

視窗背景是在視窗開始繪圖之前用來填滿工作區的色彩或模式。 視窗背景涵蓋視窗移至該處之前出現在螢幕上的任何內容、清除現有的影像，並防止應用程式的新輸出與不相關的資訊混合。

系統會繪製視窗的背景，或是在應用程式呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)時，將一個 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)訊息傳送給視窗，讓視窗有機會這麼做。 如果應用程式未處理訊息，但是將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，系統會將背景填滿視窗類別所指定的背景筆刷中的模式，以清除背景。 如果筆刷無效或類別沒有背景筆刷，系統會在 **BeginPaint** 傳回的 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構中設定 **fErase** 成員，但不會執行任何其他動作。 然後，應用程式會有第二個機會繪製視窗背景（如有必要）。

如果它處理了 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)，則應用程式應該使用訊息的 *wParam* 參數來繪製背景。 此參數包含視窗的顯示裝置內容控制碼。 繪製背景之後，應用程式應該會傳回非零值。 這可確保 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)不會錯誤地將 [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)結構的 **fErase** 成員設定為非零值 (指出當應用程式處理後續的 [**WM \_ 油漆**](wm-paint.md)訊息時，應該清除) 背景。

應用程式可以在向 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)函式註冊類別時，將筆刷控制碼或系統色彩值指派給 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hbrBackground** 成員，藉此定義類別背景筆刷。 [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)或 [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)函數可用來建立筆刷控點。 系統色彩值可以是定義給 [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) 函式的其中一個。  (在將值指派給成員之前，必須先增加一個值。 ) 

即使定義了類別背景筆刷，應用程式還是可以處理 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息。 這在應用程式中很常見，可讓使用者變更指定視窗的視窗背景色彩或模式，而不會影響類別中的其他視窗。 在這種情況下，應用程式不能將訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。

應用程式不需要對齊筆刷，因為系統會使用視窗來源作為參考點來繪製筆刷。 如此一來，使用者就可以移動視窗，而不會影響模式筆刷的對齊方式。

 

 

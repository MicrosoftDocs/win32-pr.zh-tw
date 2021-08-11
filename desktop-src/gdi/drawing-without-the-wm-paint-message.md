---
description: 雖然應用程式會在執行 WM 油漆訊息時執行大部分的繪圖作業，但是在 \_ 不依賴 WM 油漆訊息的情況下，應用程式通常會更有效率地在視窗中直接繪製 \_ 。
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: 沒有 WM_PAINT 訊息的繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff9a18e923feceb33f961c9427852b2c2daddfcfc4e093809e24cd42f32869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250337"
---
# <a name="drawing-without-the-wm_paint-message"></a>不含 WM \_ 油漆訊息的繪圖

雖然應用程式會在執行 [**WM \_ 油漆**](wm-paint.md) 訊息時執行大部分的繪圖作業，但是在不依賴 **WM \_ 油漆** 訊息的情況下，應用程式通常會更有效率地在視窗中直接繪製。 當使用者需要立即意見反應時（例如選取文字和拖曳或調整物件大小時），這會很有用。 在這種情況下，應用程式通常會在處理鍵盤或滑鼠訊息時繪製。

若要在視窗中繪製，而不使用 [**WM \_ 油漆**](wm-paint.md) 訊息，應用程式會使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來取得視窗的顯示裝置內容。 使用顯示裝置內容時，應用程式可以在視窗中繪製，並避免侵到其他視窗。 當應用程式完成繪圖時，它會呼叫 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放顯示裝置內容，以供其他應用程式使用。

在不使用 [**WM \_ 油漆**](wm-paint.md) 訊息的情況下繪製時，應用程式通常不會使視窗失效。 相反地，它會以方便您還原視窗和移除繪圖的方式進行繪製。 例如，當使用者選取文字或物件時，應用程式通常會藉由反轉視窗中已有的專案來繪製選取專案。 應用程式可以移除選取專案，並還原視窗的原始內容，只要再次反轉就可以了。

應用程式會負責仔細管理它對視窗所做的任何變更。 尤其是，如果應用程式繪製選取專案，並出現中間的 [**WM \_ 油漆**](wm-paint.md) 訊息，應用程式必須確保在訊息期間完成的任何繪製都不會損毀選取專案。 為了避免這種情況，許多應用程式會移除選取專案、執行一般繪圖作業，然後在繪圖完成時還原選取專案。

 

 




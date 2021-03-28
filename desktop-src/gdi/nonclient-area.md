---
description: '\_當視窗的非工作區的一部分（例如標題列、功能表列或視窗框架）必須更新時，系統就會將 WM NCPAINT 訊息傳送至視窗。'
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: 非工作區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191930"
---
# <a name="nonclient-area"></a>非工作區

當視窗的非工作區的一部分（例如標題列、功能表列或視窗框架）必須更新時，系統就會將 [**WM \_ NCPAINT**](wm-ncpaint.md) 訊息傳送至視窗。 系統也可能會傳送其他訊息，以指示視窗更新部分的工作區。例如，當視窗變成作用中或非使用中時，它會傳送 [**WM \_ NCACTI加值稅E**](../winmsg/wm-ncactivate.md) 訊息來更新其標題列。 一般情況下，不建議處理標準視窗的這些訊息，因為應用程式必須能夠為視窗的非工作區繪製所有必要的部分。 基於這個理由，大部分的應用程式都會將這些訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，以進行預設處理。

為其 windows 建立自訂非工作區的應用程式必須處理這些訊息。 當您這樣做時，應用程式必須使用視窗裝置內容在視窗中執行繪圖。 *視窗裝置內容* 可讓應用程式在視窗的所有部分（包括非工作區）中繪製。 應用程式會使用 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來抓取視窗裝置內容，而且當繪圖完成時，必須使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放視窗裝置內容。

系統會維護非工作區的更新區域。 當應用程式收到 [**WM \_ NCPAINT**](wm-ncpaint.md) 訊息時， *wParam* 參數會包含定義更新區域維度之區域的控制碼。 應用程式可以使用此控制碼，將更新區域與視窗裝置內容的裁剪區域合併。 除非應用程式使用 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 並同時指定區域控制碼和 DCX INTERSECTRGN 旗標，否則系統不會在抓取視窗裝置內容時自動合併更新區域 \_ 。 如果應用程式未結合更新區域，則只會裁剪在視窗之外延伸的繪圖作業。 應用程式不負責清除更新區域，不論它是否使用該區域。

如果應用程式處理 [**WM \_ NCACTI加值稅E**](../winmsg/wm-ncactivate.md) 訊息，則在處理之後必須傳回 **TRUE** ，以指示系統完成使用中視窗的變更。 當應用程式收到 **WM \_ NCACTI加值稅E** 訊息時，如果視窗最小化，則應該將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。 在這種情況下，預設函式會重繪圖示的標籤。

 

 

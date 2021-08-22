---
description: 應用程式會藉由呼叫 BeginPaint、GetDC 或 GetDCEx 函式，並識別要顯示對應輸出的視窗，來取得顯示 DC。
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: 顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761322"
---
# <a name="display-device-contexts"></a>顯示裝置內容

應用程式會藉由呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)、 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式，並識別要顯示對應輸出的視窗，來取得顯示 DC。 一般而言，應用程式必須在工作區中繪製時，才會取得顯示 DC。 不過，您可以藉由呼叫 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)函式來取得 [視窗裝置內容](#window-device-contexts)。 當應用程式完成繪圖時，必須呼叫 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 或 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放 DC。

有五種類型的 Dc 可供影片顯示：

-   類別
-   通用
-   Private
-   時間範圍
-   父代

## <a name="class-device-contexts"></a>類別裝置內容

為了與16位版本的 Windows 相容，我們完全支援 *類別裝置* 內容。 撰寫您的應用程式時，請避免使用類別裝置內容;請改用私用裝置內容。

## <a name="common-device-contexts"></a>一般裝置內容

*一般裝置* 內容會顯示系統在特殊快取中維護的 dc。 一般裝置內容會用於執行不頻繁繪圖作業的應用程式。 在系統傳回 DC 控制碼之前，它會使用預設物件、屬性和模式來初始化一般裝置內容。 應用程式所執行的任何繪圖作業都會使用這些預設值，除非呼叫其中一個 GDI 函數來選取新的物件、變更現有物件的屬性，或選取新的模式。

因為只有有限數目的常見裝置內容存在，所以應用程式應該在完成繪製之後釋放它們。 當應用程式釋放一般裝置內容時，對預設資料所做的任何變更都會遺失。

## <a name="private-device-contexts"></a>私用裝置內容

*私人裝置* 內容會顯示 dc，與通用裝置內容不同的是，即使在應用程式發行之後，仍會保留對預設資料所做的任何變更。 私用裝置內容會用於執行許多繪圖作業的應用程式，例如電腦輔助設計 (CAD) 應用程式、桌面發佈應用程式、繪圖和繪製應用程式等等。 私用裝置內容不是系統快取的一部分，因此不需要在使用後釋出。 系統會在該類別的最後一個視窗終結之後，自動移除私用裝置內容。

應用程式 \_ 會在初始化 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **樣式** 成員並呼叫 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)函式時，先指定 CS OWNDC 視窗類別的樣式，藉以建立私用裝置內容。  (如需視窗類別的詳細資訊，請參閱 [視窗類別](../winmsg/window-classes.md)。 ) 

使用 CS OWNDC 樣式建立視窗之後 \_ ，應用程式就可以呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)、 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)或 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式一次，以取得識別私用裝置內容的控制碼。 應用程式可以繼續使用這個控制碼 (以及相關聯的 DC) ，直到它刪除以此類別建立的視窗為止。 系統會保留所有繪圖物件及其屬性的變更，或圖形模式，直到刪除視窗為止。

## <a name="window-device-contexts"></a>視窗裝置內容

*視窗裝置內容* 可讓應用程式在視窗中的任何位置繪製，包括非工作區。 使用自訂非工作區的應用程式，通常會使用視窗裝置內容來處理適用于 windows 的 [**wm \_ NCPAINT**](wm-ncpaint.md) 和 [**WM \_ NCACTI加值稅E**](../winmsg/wm-ncactivate.md) 訊息。 不建議針對任何其他用途使用視窗裝置內容。 如需詳細資訊，請參閱 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)。

## <a name="parent-device-contexts"></a>父裝置內容

*父裝置內容* 可讓應用程式將設定視窗裁剪區域所需的時間減至最少。 應用程式通常會使用上層裝置內容來加速控制視窗的繪製，而不需要私人或類別的裝置內容。 例如，系統會使用推播按鈕和編輯控制項的父裝置內容。 父裝置內容僅適用于子視窗，絕不會使用最上層或快顯視窗。 如需詳細資訊，請參閱 [父代顯示裝置](parent-display-device-contexts.md)內容。

 

 

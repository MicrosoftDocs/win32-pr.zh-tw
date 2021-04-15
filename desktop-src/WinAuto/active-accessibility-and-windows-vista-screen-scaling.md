---
title: Active Accessibility 和 Windows Vista 螢幕縮放比例
description: Windows Vista 可讓使用者變更每英寸 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db8e192dc01d4c7d75f19741cdfac7b3b08d22c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463480"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility 和 Windows Vista 螢幕縮放比例

Windows Vista 可讓使用者變更每英寸 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。 雖然這項功能已在 Microsoft Windows 中提供，但在舊版中，調整必須由應用程式執行。 在 Windows Vista 中，桌面視窗管理員會對所有不會處理自己調整規模的應用程式執行預設調整。 Microsoft Active Accessibility 用戶端應用程式必須將這項功能納入考慮。

## <a name="scaling-in-windows-vista"></a>Windows Vista 中的縮放比例

預設的 DPI 設定為96，這表示96圖元佔用一個名義英寸的寬度或高度。 「英吋」的確切測量值取決於監視器的大小和實體解析度。 例如，在 12 英吋寬、1280 像素水平解析度的監視器上，96 像素的水平線長度約一英吋的 9/10。

變更 DPI 設定與變更螢幕解析度不同。 在 DPI 縮放比例中，螢幕上的實體圖元數目會維持不變。 不過，縮放比例會套用至 UI 元素的大小和位置。 針對未明確要求不縮放的桌面和應用程式，桌面視窗管理員 (DWM) 會自動執行縮放。

實際上，當使用者將縮放比例設定為 120 DPI 時，螢幕上的垂直或水準英寸會變大25%。 所有維度都會因此調整。 視窗的上邊緣和左邊緣的位移會增加25%。 視窗的大小會以相同比例增加，以及它所包含之所有 UI 元素的位移和大小。

根據預設，當使用者將 DPI 設定為120時，DWM 不會執行非 DPI 感知應用程式的縮放比例，但當 DPI 設定為自訂值144或更高時，則會執行此工作。 不過，使用者可以覆寫此預設行為。

針對重視畫面座標的應用程式，畫面縮放比例會產生新挑戰。 畫面現在包含兩個座標系統：實體和邏輯。 點的實體座標是來自原點左上方的實際位移 (以像素為單位)。 邏輯座標則是像素本身縮放時，跟著縮放的位移。

假設您設計的對話方塊在座標 (100, 48) 上有一個按鈕。 當此對話方塊顯示為預設 96 DPI 時，此按鈕會位於 (100，48) 的實體座標。 以 120 DPI 為單位，位於 (125，60) 的實體座標。 但是在任何 DPI 設定中，邏輯座標都相同： (100、48) 。

邏輯座標很重要，因為它們會讓作業系統和應用程式的行為保持一致，而不論 DPI 設定為何。 例如， **system.object** 通常會傳回邏輯座標，。 如果您將游標移到對話方塊中的專案上方，則會傳回相同的座標，不論 DPI 設定為何。 如果您在 (100、100) 繪製控制項，則會將它繪製至這些邏輯座標，而且會佔用與任何 DPI 設定相同的相對位置。

## <a name="scaling-in-active-accessibility-clients"></a>Active Accessibility 用戶端進行調整

Microsoft Active Accessibility 不會使用邏輯座標。 下列方法和函式會傳回實體座標或將它們視為參數。

-   [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

根據預設，在非 96 DPI 環境中執行的 Microsoft Active Accessibility 用戶端應用程式將無法從這些呼叫取得正確的結果。 例如，因為游標位置是以邏輯座標為單位，所以用戶端無法直接將這些座標傳遞給 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) ，以取得游標下的元素。

此外，在其工作區之外建立視窗的應用程式（例如強調焦點 UI 元素的協助工具應用程式）將不會在正確的畫面位置上建立視窗，因為視窗將放置於邏輯座標，而不是 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)所傳回的實體座標。

解決方案分為兩個部分：

-   將用戶端應用程式設為「DPI 感知」。 若要這樣做，請在啟動時呼叫 [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) 函數。 這個函式會讓整個進程具有 DPI 感知，這表示所有屬於進程的視窗都是無比例的。
-   使用可感知 DPI 的函式。 例如，若要取得資料指標座標，請呼叫 [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) 函數。 請勿使用 [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos);在 DPI 感知的應用程式中，其行為是未定義的。

如果您的應用程式執行與非 DPI 感知應用程式的直接跨進程通訊，您可能會使用 [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) 和 [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) 函式，在邏輯和實體座標之間進行轉換。

 

 
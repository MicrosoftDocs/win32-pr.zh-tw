---
title: 瞭解螢幕縮放問題
description: Windows Vista 和更新版本的作業系統可讓使用者變更每英寸的點 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。
ms.assetid: 27dc49e7-2466-4ea3-a6d9-5ea86d6b4c60
keywords:
- 用戶端，消費者介面自動化螢幕縮放比例
- 用戶端，螢幕縮放比例
- 用戶端，調整規模
- 消費者介面自動化，螢幕縮放比例
- 消費者介面自動化，調整規模
- 螢幕縮放比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d790ee7747f258847cd23aea8bbbe8c25813fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382481"
---
# <a name="understanding-screen-scaling-issues"></a>瞭解螢幕縮放問題

Windows Vista 和更新版本的作業系統可讓使用者變更每英寸的點 (DPI) 設定，讓螢幕上大部分的 UI 元素顯示較大。 在舊版的 Windows 中，調整必須由應用程式來執行。 在 Windows Vista （含）以後版本中，桌面視窗管理員 (DWM) 會針對所有不會處理其本身調整的應用程式執行預設調整。 Microsoft 消費者介面自動化用戶端應用程式必須將這項功能納入考慮。

本主題包含下列幾節：

-   [在 Windows Vista 和更新版本中進行調整](#scaling-in-windows-vista-and-later)
-   [使用者介面自動化用戶端中的縮放比例](#scaling-in-ui-automation-clients)

## <a name="scaling-in-windows-vista-and-later"></a>在 Windows Vista 和更新版本中進行調整

預設的 DPI 設定為96，這表示96圖元佔用一個名義英寸的寬度或高度。 「英吋」的確切測量值取決於監視器的大小和實體解析度。 例如，在 12 英吋寬、1280 像素水平解析度的監視器上，96 像素的水平線長度約一英吋的 9/10。

變更 DPI 設定與變更螢幕解析度不同。 在 DPI 縮放比例中，螢幕上的實體圖元數目會維持不變。 不過，縮放比例會套用至 UI 元素的大小和位置。 這項調整可由桌上型電腦的 DWM 以及未明確要求不要調整的應用程式自動執行。

實際上，當使用者將縮放比例設定為 120 DPI 時，螢幕上的垂直或水準英寸會變大25%。 所有維度都會因此調整。 應用程式視窗在螢幕上邊緣和左邊緣的位移會增加25%。 如果應用程式調整已啟用，且應用程式不是 DPI 感知，則視窗的大小會以相同比例增加，以及其所包含之所有 UI 元素的位移和大小。

> [!Note]  
> 根據預設，當使用者將 DPI 設定為120時，DWM 不會執行非 DPI 感知應用程式的縮放比例，但當 DPI 設定為自訂值144或更高時，則會執行調整。 不過，使用者可以覆寫此預設行為。

 

針對重視畫面座標的應用程式，畫面縮放比例會產生新挑戰。 畫面現在包含兩個座標系統：實體和邏輯。 點的實體座標是來自原點左上角的實際位移（以圖元為單位）。 邏輯座標則是像素本身縮放時，跟著縮放的位移。

假設您設計的對話方塊在座標 (100, 48) 上有一個按鈕。 當此對話方塊顯示為預設 96 DPI 時，此按鈕會位於 (100，48) 的實體座標。 以 120 DPI 為單位，位於 (125，60) 的實體座標。 但是在任何 DPI 設定中，邏輯座標都相同： (100、48) 。

邏輯座標很重要，因為它們會使作業系統和應用程式的行為保持一致，無論 DPI 設定為何。 例如， [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) 函數通常會傳回邏輯座標。 如果您將游標移到對話方塊中的專案上方，則會傳回相同的座標，不論 DPI 設定為何。 如果您在 (100、100) 繪製控制項，則會將它繪製至這些邏輯座標，而且會佔用與任何 DPI 設定相同的相對位置。

## <a name="scaling-in-ui-automation-clients"></a>使用者介面自動化用戶端中的縮放比例

消費者介面自動化 API 不會使用邏輯座標。 下列方法和屬性會傳回實體座標或將實體座標視為參數。

-   [**IUIAutomation::ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
-   [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache)
-   [**IUIAutomationElement::GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint)
-   [**IUIAutomationElement::CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle)
-   [**IUIAutomationElement::CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)
-   [**IRawElementProviderFragment::BoundingRectangle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-get_boundingrectangle)

根據預設，在未設定為 96 DPI 的環境中執行的消費者介面自動化應用程式，將無法從這些方法和屬性取得正確的結果。 例如，因為游標位置是以邏輯座標為單位，所以用戶端無法將這些座標傳遞給 [**IUIAutomation：： ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) ，以取得游標下的元素。 此外，應用程式也將無法在其用戶端區域之外正確放置視窗。

解決方案有兩個部分。

首先，將用戶端應用程式設為 DPI 感知。 若要這樣做，請在啟動時呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函數。 這個函式會讓整個進程具有 DPI 感知，這表示所有屬於進程的視窗都是無比例的。

其次，若要取得資料指標座標，請呼叫 [**GetPhysicalCursorPos**](/windows/desktop/api/winuser/nf-winuser-getphysicalcursorpos) 函數。

 

 
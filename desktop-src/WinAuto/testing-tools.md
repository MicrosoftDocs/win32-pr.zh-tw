---
title: 測試工具
description: 描述用來測試應用程式協助工具實作為的工具，以確保 UI 可供用戶端應用程式完整存取，以及透過鍵盤存取您應用程式的使用者。
ms.assetid: abacbec4-6ccd-4853-afcd-a92a6656f393
keywords:
- 輔助功能測試工具
- 測試控管，協助工具
- 輔助功能測試
- UIA
- MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcd5d8b0777eb80cf5b2935cc8652d328dfc219cb56bc654c1eeae0761bbd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133591"
---
# <a name="testing-tools"></a>測試工具

以程式設計方式存取和鍵盤存取是在您的應用程式中支援協助工具的重要需求。 如果沒有足夠的存取權，許多輔助技術的使用者 (在) ，例如螢幕閱讀程式和螢幕小鍵盤使用者，將無法使用您的應用程式。 確定您已徹底測試應用程式的協助工具執行，以確認它提供有關其 UI 元素的適當資訊，而且所有應用程式案例都只能使用鍵盤來完成。

除了驗證程式設計存取之外，某些工具可協助您評估應用程式鍵盤存取的執行情況。 不過，單獨的工具不夠。 手動確認所有案例都可以使用鍵盤來完成是很重要的。

針對程式設計和鍵盤需求，沒有任何一項可驗證完整執行的工具。 請嘗試使用各種不同的工具來驗證您的執行，並盡可能找出輔助技術（例如螢幕讀取器）的使用者，以使用您的 UI。

本節說明可用來測試 Microsoft 消費者介面自動化 (UIA) 和 Microsoft Active Accessibility (MSAA) 執行的工具。

## <a name="tools"></a>工具

[協助工具 Insights](https://accessibilityinsights.io/) -協助開發人員尋找和修正網站和 Windows 應用程式中的協助工具問題。

- [web 的協助工具 Insights](https://accessibilityinsights.io/docs/web/overview)是適用于 Chrome 和[Microsoft Edge Insider](https://www.microsoftedgeinsider.com)的延伸模組，可協助開發人員尋找並修正 web 應用程式和網站中的協助工具問題。 它支援兩種主要案例：
  - **FastPass** -一項輕量、雙步驟的程式，可協助開發人員在五分鐘內找出常見、高衝擊的協助工具問題。  
  - **評** 量-讓任何人都能使用協助工具標準和指導方針，確認網站是否符合100% 的規範。 [協助工具 Insights](https://accessibilityinsights.io/)也可讓您查看消費者介面自動化專案、屬性、控制項模式和事件 (類似于下一節) 所述的[檢查](/windows/desktop/winauto/inspect-objects)和[AccEvent](/windows/desktop/winauto/accessible-event-watcher)舊版工具。

- [適用于 Windows 的協助工具 Insights](https://accessibilityinsights.io/docs/windows/overview)可協助開發人員尋找並修正 Windows 應用程式中的協助工具問題。 此工具支援三種主要案例：
  - **即時檢查** 可讓開發人員藉由將滑鼠暫留在專案上，或設定鍵盤焦點，來確認應用程式中的元素有正確的消費者介面自動化屬性。
  - **FastPass** -一項輕量、雙步驟的程式，可協助開發人員在五分鐘內找出常見、高衝擊的協助工具問題。
  - **疑難排解** 可讓您診斷並修正特定的協助工具問題。

### <a name="legacy-testing-tools"></a>舊版測試控管

下列工具仍可在 Windows SDK 中使用，並記載于此處以取得持續支援，但建議您轉換至[協助工具 Insights](https://accessibilityinsights.io/)。

- [**可存取的事件**](accessible-event-watcher.md)監看員：「可存取的事件監看員」 (AccEvent) 工具會檢查協助工具資料以協助驗證應用程式 ui 元素，以確保 ui 元素會在 ui 變更時引發適當的 Microsoft Active Accessibility 和消費者介面自動化事件。 AccEvent 通常用來偵測問題，並驗證自訂和擴充的控制項是否正常運作。

- [**檢查**](inspect-objects.md)：檢查可讓您查看任何 UI 元素中的協助工具資料。 這在擴充通用控制項或建立自訂控制項時特別有用，以確保正確設定屬性和控制項模式。

- [**AccScope**](accscope.md)： AccScope 工具可讓開發人員在早期設計和開發階段，以視覺化的方式評估其應用程式的可存取性。 AccScope 可協助視覺化螢幕閱讀程式如何使用應用程式提供的消費者介面自動化資訊。 它會顯示將資訊或支援新增至您的應用程式，以改善其存取範圍的區域。

- [**Ui 協助工具檢查**](ui-accessibility-checker.md)程式： (AccChecker) 工具的 Ui 協助工具檢查程式，可驗證是否符合重要的 ui 協助工具需求。 AccChecker 包含 (ARIA) 消費者介面自動化、Microsoft Active Accessibility 和可存取的豐富網際網路應用程式的驗證檢查。 它可以提供靜態檢查，以尋找遺漏名稱、樹狀問題等錯誤。 它有助於驗證程式設計的存取，並具有支援自動化輔助功能測試的先進功能。

- [**消費者介面自動化驗證**](ui-automation-verify.md)：消費者介面自動化驗證 (UIA 確認) 是測試架構，適用于手動和自動測試控制項或應用程式的消費者介面自動化執行。 它也可以記錄測試結果。 您可以將應用程式整合到測試程式碼中，並定期進行自動化測試或消費者介面自動化案例的點檢查。 這項工具適用于驗證具有已建立功能之應用程式的變更，在新功能以外的區域中沒有新的問題或回歸。

### <a name="obsolete-tools"></a>淘汰的工具

**可存取的瀏覽器** 和 **UI Spy** 工具已淘汰且無法再使用。 請改用 [ [**檢查**](inspect-objects.md) ] 或 [ [**AccScope**](accscope.md) ]。

## <a name="related-topics"></a>相關主題

- [協助工具開發人員中樞](https://developer.microsoft.com/windows/accessible-apps)
- [Microsoft 協助工具](https://www.microsoft.com/accessibility/)
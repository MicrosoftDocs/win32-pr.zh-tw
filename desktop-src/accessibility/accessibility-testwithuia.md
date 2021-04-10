---
description: 概述如何使用消費者介面自動化和其他工具來測試您的應用程式。
title: 測試協助工具
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 0d589c9b7bd598c0829ff9941ab2facabfaf10d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111465"
---
# <a name="testing-for-accessibility"></a>測試協助工具

以程式設計方式存取和鍵盤存取是在您的應用程式中支援協助工具的重要需求。 測試 Windows 應用程式的可存取性、) 工具的輔助技術 (，以及 UI 架構，對於確保具有各種殘障和 (限制的人員（包括願景、學習、機動/行動性、語言/通訊障礙) 或單純偏好使用鍵盤的人）而言，是非常重要的。

如果沒有足夠的存取權，例如螢幕讀取器和螢幕小鍵盤，則具有視覺、學習、機動/行動力的使用者，以及語言/通訊障礙或限制 (以及只偏好使用鍵盤) 的使用者，將無法使用您的應用程式。

本節說明可用來測試 Windows 和 web 應用程式的協助工具實作為各種工具。

> [!NOTE]
> 也請務必手動測試，以確認鍵盤對您應用程式的存取。

## <a name="tools"></a>工具

[協助工具深入](https://accessibilityinsights.io/) 解析-協助開發人員尋找和修正網站和 Windows 應用程式中的協助工具問題。

- [適用于 web 的協助工具深入](https://accessibilityinsights.io/docs/web/overview) 解析是適用于 Chrome 和 [Microsoft Edge Insider](https://www.microsoftedgeinsider.com) 的延伸模組，可協助開發人員尋找並修正 Web 應用程式和網站中的協助工具問題。 它支援兩種主要案例：
  - **FastPass** -一項輕量、雙步驟的程式，可協助開發人員在五分鐘內找出常見、高衝擊的協助工具問題。  
  - **評** 量-讓任何人都能使用協助工具標準和指導方針，確認網站是否符合100% 的規範。 [協助工具深入](https://accessibilityinsights.io/) 解析也可讓您複習消費者介面自動化專案、屬性、控制項模式和事件 (類似下一節中所述的 [檢查](/windows/desktop/winauto/inspect-objects) 和 [AccEvent](/windows/desktop/winauto/accessible-event-watcher) 舊版工具) 。

- [適用于 windows 的協助工具見解](https://accessibilityinsights.io/docs/windows/overview) 可協助開發人員尋找和修正 windows 應用程式中的協助工具問題。 此工具支援三種主要案例：
  - **即時檢查** 可讓開發人員藉由將滑鼠暫留在專案上，或設定鍵盤焦點，來確認應用程式中的元素有正確的消費者介面自動化屬性。
  - **FastPass** -一項輕量、雙步驟的程式，可協助開發人員在五分鐘內找出常見、高衝擊的協助工具問題。
  - **疑難排解** 可讓您診斷並修正特定的協助工具問題。

### <a name="legacy-testing-tools"></a>舊版測試控管

下列工具仍可在 Windows SDK 中使用，並記載于此處以取得持續支援，但建議您轉換至 [協助工具深入](https://accessibilityinsights.io/)解析。

- [檢查](/windows/desktop/winauto/inspect-objects)：讓您查看任何 UI 元素的協助工具資料。 這特別適用于在擴充通用控制項或建立自訂控制項時，確保屬性和控制項模式的設定正確。
- [可存取的事件監看員 (AccEvent) ](/windows/desktop/winauto/accessible-event-watcher)：檢查協助工具資料來驗證應用程式 UI 專案，並確保 ui 元素能引發適當的 Microsoft Active Accessibility 並消費者介面自動化 ui 事件上的事件。 AccEvent 通常用來偵測問題，並驗證自訂和擴充的控制項是否正常運作。
- [AccScope](/windows/desktop/winauto/accscope)：可在早期設計和開發階段進行應用程式協助工具的視覺化評估。 AccScope 有助於視覺化螢幕閱讀程式如何使用應用程式所提供的消費者介面自動化資訊，並顯示在應用程式中新增資訊或支援的位置，如何改善其存取範圍。
- [UI 協助工具檢查](/windows/desktop/winauto/ui-accessibility-checker)程式：確認已完成應用程式中的主要 UI 協助工具需求。 AccChecker 包含 (ARIA) 消費者介面自動化、Microsoft Active Accessibility 和可存取的豐富網際網路應用程式的驗證檢查。 它可為錯誤提供靜態檢查，例如遺漏名稱、樹狀問題等等。 它有助於驗證程式設計存取，並包含自動化輔助功能測試的先進功能。
- [消費者介面自動化驗證](/windows/desktop/winauto/ui-automation-verify)：在控制項或應用程式中手動和自動測試消費者介面自動化執行的架構 (可以記錄) 的結果。 您可以將應用程式整合到測試程式碼中，並定期進行自動化測試或消費者介面自動化案例的點檢查。 這項工具適用于驗證具有已建立功能之應用程式的變更，在新功能以外的區域中沒有新的問題或回歸。

---
title: '協助工具工具-AccChecker (UI 協助工具檢查程式) '
description: 描述 AccChecker (UI 協助工具檢查工具) ，此工具可用於測試應用程式的消費者介面自動化或 Microsoft Active Accessibility (MSAA) 執行。
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI 協助工具檢查程式
- AccChecker
- 消費者介面自動化的實作為測試
- UIA 實施，測試
- Microsoft Active Accessibility 的實作為測試
- MSAA 執行，測試
- 測試消費者介面自動化
- 測試 UIA
- 測試 Microsoft Active Accessibility
- 測試 MSAA
- UIA 測試控管
- 消費者介面自動化測試控管
- MSAA 測試控管
- Microsoft Active Accessibility 測試控管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106996364"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>協助工具工具-AccChecker (UI 協助工具檢查程式) 

**AccChecker** (UI 協助工具檢查工具) 驗證消費者介面自動化 (UIA) 的設計和實行中是否符合重要的 ui 協助工具需求，或 MICROSOFT ACTIVE ACCESSIBILITY (MSAA) ，不論基礎 UI 架構為何。 **AccChecker** 也包含一組 web 協助工具驗證。

**AccChecker** 提供下列層級的功能：

- 支援手動測試、訊息記錄和抑制產生的 Windows GUI 應用程式。
- 用於自動化測試架構的 API。
- 在無法使用 **AccChecker** 受控 API 的情況下，支援非受控測試自動化的主控台應用程式。

所有層級的 **AccChecker** 功能都提供用來驗證 Microsoft Active Accessibility 程式設計存取、程式設計事件產生、控制項配置和鍵盤流覽的常式。 **AccChecker** 也提供基本的螢幕讀取器轉譯服務。

**AccChecker** 會隨 WINDOWS 軟體開發套件 (SDK) 安裝。 它位於 \\ \\ <  > \\ < SDK 安裝路徑的 bin version *platform* > \\ AccChecker 資料夾中。

> [!NOTE]
> **AccChecker** 是一種舊版工具。 建議您改為使用 [協助工具深入](https://accessibilityinsights.io/) 解析。

## <a name="requirements"></a>規格需求

需要 .NET Framework 2.0 或更新版本。

**AccChecker** 可以用來檢查沒有 Microsoft 消費者介面自動化的系統上的協助工具資料，但只能檢查 Microsoft Active Accessibility 屬性。 若要檢查消費者介面自動化，消費者介面自動化必須存在於系統上。 如需詳細資訊，請參閱 [消費者介面自動化](entry-uiauto-win32.md)的「需求」一節。

**AccChecker** 會安裝為 windows SDK 中整個工具組的一部分，而不是以個別的 exe 下載方式來散發。 Windows SDK 包含本節中記載的所有協助工具相關工具。 [取得 Windows SDK。](https://developer.microsoft.com/) 如果您需要先前的版本， (也有從該頁面連結的 SDK 下載封存。 ) 

## <a name="related-topics"></a>相關主題

- [協助工具事件監控程式](accessible-event-watcher.md)
- [檢查](inspect-objects.md)
- [測試控管](testing-tools.md)
- [使用者介面自動化確認](ui-automation-verify.md)

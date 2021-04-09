---
title: 架構和互通性
description: 本主題簡要說明 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化的架構，以及允許應用程式之間的互通性的元件（以兩種不同的技術為基礎）。
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104092505"
---
# <a name="architecture-and-interoperability"></a>架構和互通性

本主題簡要說明 Microsoft Active Accessibility 和 Microsoft 消費者介面自動化的架構，以及允許應用程式之間的互通性的元件（以兩種不同的技術為基礎）。

如需 Microsoft Active Accessibility 和消費者介面自動化互通性的詳細資訊，請參閱 [通用基礎結構](common-infrastructure.md)。

本主題包含下列各節。

-   [Microsoft Active Accessibility 架構](#microsoft-active-accessibility-architecture)
-   [消費者介面自動化架構](#ui-automation-architecture)
-   [Microsoft Active Accessibility 和消費者介面自動化互通性](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [IAccessibleEx 介面](#the-iaccessibleex-interface)
-   [相關主題](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Microsoft Active Accessibility 架構

Microsoft Active Accessibility 會公開有關控制項的基本資訊，例如控制項名稱、畫面上的位置和控制項類型，以及狀態資訊，例如可見度和啟用/停用狀態。 UI 會以可存取物件的階層表示;變更和動作會以 WinEvents 表示。

Microsoft Active Accessibility 是由下列元件所組成：

-   可存取的物件-邏輯 UI 元素 (例如按鈕) ，此專案是由 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 元件物件模型所表示 (COM) 介面和整數子識別碼 (ChildID) 。
-   WinEvents：一種事件系統，可讓伺服器在可存取的物件變更時通知用戶端。 如需詳細資訊，請參閱 [WinEvents](winevents-infrastructure.md)。
-   OLEACC.dll：提供 Microsoft Active Accessibility API 和協助工具系統架構的執行時間動態連結程式庫。 OLEACC 會執行可提供標準 UI 元素之預設協助工具資訊的 proxy 物件，包括使用者控制項、使用者功能表和通用控制項。

針對 Microsoft Active Accessibility，協助工具架構 (OLEACC) 的系統元件，可協助輔助技術 (協助工具工具) 和應用程式之間的通訊，如下圖所示。

![圖例顯示協助工具工具如何與應用程式互動](images/msaaarch.gif)

應用程式 (Microsoft Active Accessibility 伺服器) 提供 UI 協助工具資訊給 (Microsoft Active Accessibility 用戶端) 的工具，這會代表使用者與 UI 互動。 程式碼界限是以程式設計方式和進程界限。

## <a name="ui-automation-architecture"></a>消費者介面自動化架構

使用消費者介面自動化，消費者介面自動化核心元件 (UIAutomationCore.dll) 會載入至協助工具工具和應用程式的進程。 核心元件可管理跨進程通訊、提供較高層級的服務，例如依屬性值搜尋元素，以及啟用大量提取或快取屬性，以提供比 Microsoft Active Accessibility 的執行更好的效能。

消費者介面自動化包含的 proxy 物件可提供有關標準 UI 元素的 UI 資訊，例如使用者控制項、使用者功能表和通用控制項。 它也包含可讓消費者介面自動化用戶端從 Microsoft Active Accessibility 伺服器取得 UI 資訊的 proxy。

下圖顯示協助工具工具 (用戶端) 和應用程式 (提供者) 中所使用的各種消費者介面自動化元件之間的關聯性。

![圖例顯示協助工具工具的元件如何與應用程式中的元件互動](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Microsoft Active Accessibility 和消費者介面自動化互通性

Microsoft Active Accessibility 橋接器的消費者介面自動化可讓 Microsoft Active Accessibility 用戶端藉由將消費者介面自動化物件模型轉換成 Microsoft Active Accessibility 物件模型，來存取消費者介面自動化提供者。 下圖顯示消費者介面自動化對 Microsoft Active Accessibility 橋接器的角色。

![圖例顯示 ui 自動化如何與協助工具工具和應用程式搭配運作](images/uiatomsaabridge.gif)

同樣地，Microsoft Active Accessibility 對消費者介面自動化 Proxy 會為消費者介面自動化用戶端轉譯以 Microsoft Active Accessibility 為基礎的伺服器物件模型。 下圖顯示 Microsoft Active Accessibility 對消費者介面自動化 Proxy 的角色。

![圖例顯示 ui automation proxy 如何搭配協助工具工具和應用程式運作](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>IAccessibleEx 介面

[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)介面可讓現有的應用程式或 UI 程式庫擴充其 Microsoft Active Accessibility 物件模型，以支援消費者介面自動化，而不需要從頭重寫執行。 使用 **IAccessibleEx**，您可以只執行完整描述 UI 和其功能所需的其他消費者介面自動化屬性和控制項模式。

由於 Microsoft Active Accessibility 對消費者介面自動化 Proxy 會將已啟用 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)之 Microsoft Active Accessibility 伺服器的物件模型轉譯成消費者介面自動化物件模型，因此消費者介面自動化用戶端不需要執行任何額外的工作。 **IAccessibleEx** 介面也可以啟用同進程 Microsoft Active Accessibility 用戶端直接與消費者介面自動化提供者互動。

如需詳細資訊，請參閱 [IAccessibleEx 介面](iaccessibleex.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Automation API 總覽](windows-automation-api-overview.md)
</dt> <dt>

[IAccessibleEx 介面](iaccessibleex.md)
</dt> <dt>

[輔助技術的安全性考慮](uiauto-securityoverview.md)
</dt> </dl>

 

 





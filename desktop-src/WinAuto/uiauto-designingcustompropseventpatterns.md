---
title: 設計自訂屬性、事件和控制項模式
description: 自訂屬性、事件或控制項模式的設計應該適用于各種控制項的執行。
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- 消費者介面自動化，自訂屬性
- 消費者介面自動化，事件總覽
- 消費者介面自動化，控制項模式總覽
- 消費者介面自動化，設計自訂屬性
- 消費者介面自動化，設計事件
- 消費者介面自動化，設計控制項模式
- 消費者介面自動化、WinEvents
- 自訂屬性，設計
- 事件，設計
- 事件，WinEvents
- 控制項模式，設計
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6973356fe6be922e73eef70e5107b6dcabe0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375432"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>設計自訂屬性、事件和控制項模式

自訂屬性、事件或控制項模式的設計應該適用于各種控制項的執行。 只有在有限案例中才有用的控制項或應用程式特定設計，應予以避免。 設計應該遵循現有的 Microsoft 消費者介面自動化屬性、事件和控制項模式的範例，這些都是謹慎指定的，以符合各種協助工具和自動化測試應用程式的需求。

執行自訂屬性、事件或控制項模式的規格，牽涉到用戶端和提供者雙方雙方的合作與合約，同時要求雙方都能以一致的方式來執行規格。 我們鼓勵公司與產業組織合作，例如 [協助工具互通性聯盟 (AIA) ](https://www.atia.org/) 來設計和發佈自訂屬性、事件或控制項模式的規格。 如此一來，就可以達成共識，並確保可與最廣泛的應用程式交互操作。

本主題包含下列幾節：

-   [使用自訂屬性和事件的時機](#when-to-use-custom-properties-and-events)
-   [設計自訂屬性](#designing-custom-properties)
-   [設計自訂事件](#designing-custom-events)
    -   [自訂消費者介面自動化事件和 WinEvents](#custom-ui-automation-events-and-winevents)
-   [設計自訂控制項模式](#designing-custom-control-patterns)
-   [自訂控制項類型](#custom-control-types)
-   [相關主題](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>使用自訂屬性和事件的時機

在建立自訂屬性、事件或控制項模式之前，請確定消費者介面自動化不會提供現有的方案。 例如，您不需要建立自訂的「Click」控制項模式，因為叫 [用控制項模式](uiauto-implementinginvoke.md) 已經描述該功能。

如果您決定需要自訂的屬性、事件或控制項模式，請確定它不太清楚或不是泛型。 例如，名為 "Show" 的控制項模式並不實用，因為控制項的可見度可由專案上的 availability 屬性指出，例如 [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) 或 [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md)。

在執行自訂解決方案之前，請仔細確認是否需要，然後完全設計功能。

## <a name="designing-custom-properties"></a>設計自訂屬性

消費者介面自動化包含兩種基本類型的屬性： Automation 元素屬性和控制項模式屬性。 Automation 元素屬性是由所有消費者介面自動化專案所公開的一組通用屬性（例如 Name、AcceleratorKey 和 ClassName）所組成，不論控制項型別為何。 控制項模式屬性是由控制項透過特定的控制項模式公開。 每個控制項模式都有一組對應的控制項模式屬性，控制項必須公開這些屬性。 例如，支援 [方格](uiauto-implementinggrid.md) 控制項模式的控制項會公開 ColumnCount 和 RowCount 屬性。

自訂 automation 元素屬性或控制項模式屬性應遵守下列設計指導方針：

-   自訂屬性必須有 [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) 列舉所指定的下列其中一種資料類型。 自訂屬性不支援其他資料類型。
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **UIAutomationType \_ 元素**
    -   **UIAutomationType \_ Int**
    -   **UIAutomationType \_ 點**
    -   **UIAutomationType \_ 字串**
-   如果自訂屬性包含字串資料 ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)) ，此規格必須指出屬性是否可當地語系化 (也就是字串是否可以轉譯成不同的 UI 語言) 。
-   自訂屬性不應與現有屬性的特性或功能重迭。

## <a name="designing-custom-events"></a>設計自訂事件

應用程式會使用消費者介面自動化事件通知，來回應涉及 UI 專案的變更和動作。 大部分屬性都有相關聯的屬性變更事件，這些事件會在屬性值變更時引發消費者介面自動化引發。 如果您引進自訂屬性，您應該考慮引入任何可能也需要的對應自訂事件。

自訂事件應遵守下列設計指導方針：

-   自訂事件必須是「無狀態」。 它不能與特定屬性或值產生關聯。
-   自訂事件不應與任何現有事件的定義或角色重迭。

### <a name="custom-ui-automation-events-and-winevents"></a>自訂消費者介面自動化事件和 WinEvents

[WinEvents](winevents-infrastructure.md) 在 Microsoft Windows 平臺中是一個有用的處理序間通訊和事件機制。 不過，引入新的 New-winevent 識別碼會有風險，因為這可能會導致與其他應用程式或作業系統發生衝突，導致系統變得不穩定。 為了避免衝突，Microsoft 定義了數種不同的 WinEvents 類別，每個類別目錄都定義了一或多個範圍的值，以做為 New-winevent 識別碼使用。 如需詳細資訊，請參閱 [配置 New-winevent 識別碼](allocation-of-winevent-ids.md)。

自訂消費者介面自動化事件會藉由在消費者介面自動化架構內部配置事件識別碼，來避免發生衝突。

## <a name="designing-custom-control-patterns"></a>設計自訂控制項模式

控制項模式是具有屬性、方法和事件的介面，這些屬性定義了可從 automation 元素使用的離散功能。 控制項模式方法可讓消費者介面自動化用戶端操作控制項的特定層面。 控制項模式屬性和事件提供有關控制項某些方面的資訊，並提供可執行控制項模式之 automation 元素狀態的相關資訊。

自訂控制項模式應遵守下列設計指導方針：

-   自訂控制項模式應該涵蓋特定案例。 例如， [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式的目的是要查詢包含的物件（不論虛擬化狀態為何），但不會列舉或計算所包含的物件。
-   自訂控制項模式不應與現有控制項模式的功能重迭。 例如，[叫用] 和 [ [ExpandCollapse](uiauto-implementingexpandcollapse.md) ] 控制項模式不應結合[，並以](uiauto-implementinginvoke.md)新的控制項模式呈現。 請重複使用現有的控制項模式，或使用新的控制項模式來定義獨特的情節。
-   多個自訂控制項模式可以一起設計，以支援複雜的案例。 例如， [選取專案](uiauto-implementingselection.md) 和 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式會一起運作，以支援一般物件選取案例。

## <a name="custom-control-types"></a>自訂控制項類型

雖然本主題的重點在於如何註冊自訂消費者介面自動化屬性、事件和控制項模式，但是也可以引進新的控制項類型。 和自訂屬性、事件和控制項模式不同的是，自訂控制項類型無法在執行時間以程式設計方式註冊，因為它其實只是消費者介面自動化 ControlType 屬性的可能值。 不過，您可以定義、發佈自訂控制項類型識別碼，並可讓其他用戶端和提供者使用。 如需控制項類型的詳細資訊，請參閱 [消費者介面自動化控制項類型總覽](uiauto-controltypesoverview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[註冊自訂屬性、事件和控制項模式](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 
---
title: 消費者介面自動化規格
description: 本主題提供 Microsoft 消費者介面自動化規格的總覽，以構成消費者介面自動化的 Windows 實作為基礎。
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d78298299241545033b25dccc8d79376ec55e1b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987641"
---
# <a name="ui-automation-specification"></a>消費者介面自動化規格

本主題提供 Microsoft 消費者介面自動化規格的總覽，以構成消費者介面自動化的 Windows 實作為基礎。 Microsoft Windows 以外的所有平臺都可支援消費者介面自動化規格。 如需詳細資訊，請參閱 [消費者介面自動化規格](./uiauto-specandcommunitypromise.md)

本主題包含下列幾節：

-   [Introducton](#introducton)
-   [消費者介面自動化元素](#ui-automation-elements)
-   [消費者介面自動化樹狀結構](#ui-automation-tree)
-   [消費者介面自動化屬性](#ui-automation-properties)
-   [UI 自動化控制項模式](#ui-automation-control-patterns)
-   [UI 自動化控制項類型](#ui-automation-control-types)
-   [消費者介面自動化事件](#ui-automation-events)
-   [相關主題](#related-topics)

## <a name="introducton"></a>Introducton

消費者介面自動化規格提供彈性的程式設計方式，讓您能夠以程式設計方式存取 Windows 桌面上的 ui 元素，讓輔助技術產品（例如螢幕讀取器）提供 UI 的相關資訊給使用者，以及透過標準輸入以外的方式操作 ui。

消費者介面自動化在範圍內的範圍更廣，只限于介面定義。 它提供：

-   物件模型和函式，可讓用戶端應用程式輕鬆地接收事件、抓取屬性值，以及操作 UI 元素。
-   跨進程界限尋找和提取的核心基礎結構。
-   提供者的一組介面，用來表示 UI 元素的樹狀結構、一般屬性和功能。
-   「控制項類型」屬性，可讓用戶端和提供者清楚地指出 UI 物件的通用屬性、功能和結構。

消費者介面自動化可透過下列方式改善 Microsoft Active Accessibility：

-   啟用有效率的跨進程用戶端，同時繼續允許同進程存取。
-   以允許用戶端跨進程的方式，公開 UI 的詳細資訊。
-   共存並利用 Microsoft Active Accessibility 而不會繼承其限制。 如需詳細資訊，請參閱 [Microsoft Active Accessibility 和消費者介面自動化比較](microsoft-active-accessibility-and-ui-automation-compared.md)。
-   提供可輕鬆執行的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 替代方案。

在 Windows 功能元件物件模型中， (COM) 型介面和 managed 介面的消費者介面自動化規格的實作為基礎。

## <a name="ui-automation-elements"></a>消費者介面自動化元素

消費者介面自動化會將 UI 的每個部分以 *Automation 元素* 公開至用戶端應用程式。 提供者會提供每個元素的屬性值。 元素會以樹狀結構的形式公開，並以桌面作為根項目。

Automation 元素會公開其所代表之 UI 元素的通用屬性。 其中一個屬性是控制項類型，描述其基本外觀和功能 (例如按鈕或核取方塊) 。

## <a name="ui-automation-tree"></a>消費者介面自動化樹狀結構

消費者介面自動化樹狀結構代表整個 UI：根項目是目前的桌面，而子項目則是應用程式視窗。 每個子專案都可以包含代表功能表、按鈕、工具列等專案的元素。 這些專案接著可以包含像清單專案的專案，如下圖所示。

![顯示使用者介面自動化樹狀結構的螢幕擷取畫面](images/uiatree.gif)

請注意，消費者介面自動化樹狀結構中的同級順序相當重要。 在視覺效果中彼此連續的物件也應該在消費者介面自動化樹狀結構中的彼此旁邊。

消費者介面自動化特定控制項的提供者，支援該控制項的子項目之間的導覽。 但是，提供者不在意這些控制項子樹之間的導覽。 這是由消費者介面自動化 core 管理，並使用預設視窗提供者的資訊。

為了協助用戶端更有效率地處理 UI 資訊，架構支援自動化樹狀結構的替代視圖：原始視圖、控制項視圖和內容視圖。 如下表所示，篩選的類型會決定視圖，而用戶端會定義視圖的範圍。



| 自動化樹狀結構 | Description                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| 未經處理的檢視        | 桌面為其根目錄之 automation 元素物件的完整樹狀目錄。                                          |
| 控制項檢視    | 當使用者感覺到 UI 結構時，會緊密對應至該原始視圖的子集。                                |
| 內容檢視    | 控制項視圖的子集，其中包含與使用者最相關的內容，例如下拉式方塊中的值。 |



 

如需詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。

## <a name="ui-automation-properties"></a>消費者介面自動化屬性

消費者介面自動化規格會定義兩種屬性： Automation 元素屬性和控制項模式屬性。 Automation 元素屬性會套用至大部分的控制項，並提供專案的相關基本資訊，例如其名稱。 控制項模式屬性適用于下一節所述的控制項模式。

不同于 Microsoft Active Accessibility，每個消費者介面自動化屬性都是由 GUID 和程式設計名稱所識別，讓新的屬性更容易引進。

如需詳細資訊，請參閱 [UI Automation Properties Overview](uiauto-propertiesoverview.md)。

## <a name="ui-automation-control-patterns"></a>UI 自動化控制項模式

控制項模式描述 automation 元素功能的特定層面。 例如，簡單的「可點擊式」控制項（例如按鈕或超連結）應該支援叫用控制項模式，以代表「按一下」動作。

每個控制項模式都是可能的 UI 功能和函數的標準標記法。 消費者介面自動化的目前執行會定義22個控制項模式。 Windows Automation API 也可以支援自訂控制項模式。 不同于 Microsoft Active Accessibility 角色或狀態屬性，一個 automation 元素可以支援多個消費者介面自動化控制項模式。

如需詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。

## <a name="ui-automation-control-types"></a>UI 自動化控制項類型

控制項類型是 automation 元素屬性，可指定專案所代表的知名控制項。 目前，消費者介面自動化定義38控制項類型，包括按鈕、核取方塊、下拉式方塊、DataGrid、檔、超連結、影像、工具提示、樹狀結構和視窗。

在您可以將控制項類型指派給專案之前，專案必須符合特定條件，包括特定的自動化樹狀結構、屬性值、控制項模式和事件。 不過，您不一定要這樣做。 您可以使用自訂模式和屬性，以及預先定義的屬性來擴充控制項。

預先定義的控制項類型總數明顯低於 Microsoft Active Accessibility [物件角色](object-roles.md)，因為消費者介面自動化控制項模式可以合併以表示一組較大的功能，而 Microsoft Active Accessibility 的角色則無法使用。

如需詳細資訊，請參閱 [UI Automation Control Types Overview](uiauto-controltypesoverview.md)。

## <a name="ui-automation-events"></a>消費者介面自動化事件

消費者介面自動化事件會通知應用程式變更和自動化元素所採取的動作。 有四種不同類型的消費者介面自動化事件，而且不一定表示 UI 的視覺狀態已變更。 消費者介面自動化事件模型與 Windows 中的[new-winevent](winevents-infrastructure.md)架構無關，不過 Windows Automation API 可讓消費者介面自動化事件與 Microsoft Active Accessibility framework 互通。

如需詳細資訊，請參閱 [UI Automation Events Overview](uiauto-eventsoverview.md)。

## <a name="related-topics"></a>相關主題

[消費者介面自動化規格](./uiauto-specandcommunitypromise.md)， [Windows Automation API 總覽](windows-automation-api-overview.md)

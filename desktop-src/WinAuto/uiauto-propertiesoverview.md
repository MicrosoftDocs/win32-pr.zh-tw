---
title: UI 自動化屬性概觀
description: Microsoft 消費者介面自動化提供者會公開消費者介面自動化元素上的屬性。 屬性可讓用戶端應用程式抓取控制項的相關資訊。
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- 消費者介面自動化，屬性總覽
- 消費者介面自動化、屬性與事件的比較
- 消費者介面自動化、事件與屬性的比較
- 屬性，關於
- 屬性，識別碼
- 屬性、值
- 屬性、事件
- 事件，屬性
- 屬性，動態
- 動態屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745028"
---
# <a name="ui-automation-properties-overview"></a>UI 自動化屬性概觀

Microsoft 消費者介面自動化提供者會公開消費者介面自動化元素上的屬性。 屬性可讓用戶端應用程式抓取控制項的相關資訊。

消費者介面自動化會公開兩種不同的屬性： *Automation 元素屬性* 和 *控制項模式 propertes*。 Automation 元素屬性是由所有消費者介面自動化專案所公開的一組通用屬性（例如 Name、AcceleratorKey 和 ClassName）所組成，不論控制項型別為何。 大部分 automation 元素屬性都是靜態值。

控制項模式屬性是由支援特定控制項模式的控制項所公開的屬性。 每個控制項模式都有一組對應的控制項模式屬性，控制項必須公開這些屬性。 例如，支援 [方格](uiauto-implementinggrid.md) 控制項模式的控制項會公開 ColumnCount 和 RowCount 屬性。 大部分的控制項模式屬性都是動態值。

本主題包含下列各節。

-   [屬性識別項](#property-identifiers)
-   [屬性值](#property-values)
-   [屬性和事件](#properties-and-events)
-   [相關主題](#related-topics)

## <a name="property-identifiers"></a>屬性識別項

每個屬性都是由稱為 *屬性識別碼* (識別碼) 的 **PROPERTYID** 數值來識別。 提供者和用戶端會在方法呼叫（例如 [**IRawElementProviderAdviseEvents：： AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) 和 [**IUIAutomationElement：： GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) ）中使用數值識別碼，以識別屬性要求。 如需每個消費者介面自動化屬性識別碼的詳細說明，包括每個屬性的資料類型和預設值，請參閱 [屬性識別碼](uiauto-entry-propids.md)。

## <a name="property-values"></a>屬性值

所有屬性都是唯讀的，不過某些屬性可以使用對控制項採取的方法來變更，例如 [**IDockProvider：： SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) 或 [**IUIAutomationDockPattern：： SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (用戶端) 。

如需有關如何抓取屬性值的詳細資訊，請參閱 [從消費者介面自動化元素抓取屬性](uiauto-propertiesforclients.md)。

## <a name="properties-and-events"></a>屬性和事件

與消費者介面自動化中的屬性緊密相關聯，是 *屬性變更事件* 的概念。 若為動態屬性，用戶端應用程式需要一種方法來知道屬性值已變更，以便它可以更新其資訊的快取，或以其他方式回應新的資訊。 用戶端可以註冊來接聽任何屬性的屬性變更事件。

當 UI 中的某些內容變更時，提供者會引發事件。 例如，如果選取或清除核取方塊，則會由 [切換](uiauto-implementingtoggle.md) 控制項模式的提供者執行來引發屬性變更事件。 提供者可以視任何用戶端是否正在接聽事件或接聽特定事件，以選擇性地引發事件。

並非所有屬性變更都會引發事件，這完全由項目的使用者介面自動化提供者實作所決定。 例如，清單方塊的標準 proxy 提供者不會在選取專案屬性變更時引發屬性變更事件。 在此情況下，應用程式必須接聽選取範圍變更 ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) 時引發的事件。

用戶端會藉由訂閱事件來接聽事件，如 [訂閱消費者介面自動化事件](uiauto-eventsforclients.md)中所述。 針對屬性變更的事件，用戶端必須執行 [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) 並將介面傳遞至 [**IUIAutomation：： AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) 或 [**IUIAutomation：： AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> </dl>

 

 





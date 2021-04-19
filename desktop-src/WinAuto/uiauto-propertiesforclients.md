---
title: 從消費者介面自動化元素抓取屬性
description: IUIAutomationElement 物件上的屬性包含 UI 元素的相關資訊，通常是控制項。
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- 用戶端，取得消費者介面自動化元素
- 用戶端，消費者介面自動化元素
- 用戶端，屬性
- 用戶端，正在抓取屬性
- 用戶端，消費者介面自動化屬性
- 消費者介面自動化，取得元素
- 消費者介面自動化，元素
- 消費者介面自動化，屬性
- 消費者介面自動化，正在抓取屬性
- 正在抓取屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996565"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>從消費者介面自動化元素抓取屬性

[**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)物件上的屬性包含 UI 元素的相關資訊，通常是控制項。 元素的屬性為泛型;亦即，不是控制項類型的特定。 專案的控制項特定屬性是由其控制項模式介面所公開。

Microsoft 消費者介面自動化屬性是唯讀的。 若要設定控制項的屬性，您必須使用適當控制項模式的方法。 例如，使用 [**IUIAutomationScrollPattern：： Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) 來變更滾動視窗的位置值。

若要改善效能，您可以在抓取專案時快取控制項和控制項模式的屬性值。 如需詳細資訊，請參閱快取 [消費者介面自動化屬性和控制項模式](uiauto-cachingforclients.md)。

本主題包含下列各節。

-   [屬性識別碼](#property-ids)
-   [屬性條件](#property-conditions)
-   [擷取屬性](#retrieving-properties)
-   [預設屬性值](#default-property-values)
-   [相關主題](#related-topics)

## <a name="property-ids"></a>屬性識別碼

屬性識別碼是在 Uiautomationclient.dll 中定義。 當您訂閱屬性變更的事件、抓取屬性值和結構屬性條件時，會使用這些屬性來指定屬性。 屬性識別碼也會識別在呼叫 [**IUIAutomationPropertyChangedEventHandler：： HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) 時已變更的屬性。

如需消費者介面自動化屬性識別碼的清單，請參閱 [屬性識別碼](uiauto-entry-propids.md)。

## <a name="property-conditions"></a>屬性條件

屬性識別碼是用來建立用來尋找消費者介面自動化元素的 [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) 物件。 例如，您可能想要尋找具有特定名稱或已啟用之所有控制項的元素。 每個屬性條件都會指定屬性識別碼和屬性必須符合的值。

如需詳細資訊，請參閱下列主題：

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement：： FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement：： FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>擷取屬性

有些泛型屬性（以及所有控制項模式屬性）可做為 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 或控制項模式介面上的屬性，而且可以使用存取子來抓取，例如 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) 或 [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition)。

此外，您可以使用下列其中一種方法來抓取控制項模式屬性以外的任何目前或快取屬性 () ：

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

這些方法可提供更佳的效能，並可存取完整的屬性範圍。 不過，值會在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構中傳回，而個別的屬性存取子則會將值轉換成適當的類型。

## <a name="default-property-values"></a>預設屬性值

如果消費者介面自動化提供者不會執行屬性，消費者介面自動化可以提供預設值。 例如，如果控制項的提供者不支援 [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)所識別的屬性，消費者介面自動化會傳回空字串。 同樣地，如果提供者不支援 [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md)所識別的屬性，消費者介面自動化會傳回 **FALSE**。

[**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)與 [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (之間，以及類似的方法組之間的差異) 是 "Ex" 方法可以指定不傳回預設值。 在此情況下，傳回值是特殊的唯一常數，表示不支援此屬性。 收到此值時，應用程式可以提供自己的值，或直接忽略屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化屬性概觀](uiauto-propertiesoverview.md)
</dt> <dt>

[屬性識別項](uiauto-entry-propids.md)
</dt> </dl>

 

 
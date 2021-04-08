---
title: IAccessibleEx 實施指導方針
description: Microsoft 消費者介面自動化 core 可以透過 IAccessible 介面，取得由伺服器公開之任何可存取物件的所有 Microsoft Active Accessibility 屬性。
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103679531"
---
# <a name="iaccessibleex-implementation-guidelines"></a>IAccessibleEx 實施指導方針

Microsoft 消費者介面自動化 core 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，取得由伺服器公開之任何可存取物件的所有 Microsoft Active Accessibility 屬性。 在執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)時，您必須只公開無法透過現有 Microsoft Active Accessibility 屬性公開的 UI 功能的層面。 本主題會識別消費者介面自動化屬性和控制項模式，這些模式代表 Microsoft Active Accessibility 中沒有對應的 UI 功能，它們是您可以在 **IAccessibleEx** 執行中公開的屬性和控制項模式。

本主題包含下列幾節：

-   [屬性](#properties)
-   [控制項模式](#control-patterns)
-   [消費者介面自動化屬性已變更事件的 WinEvents](#winevents-for-ui-automation-property-changed-events)
-   [相關主題](#related-topics)

## <a name="properties"></a>屬性

下列消費者介面自動化屬性不會與 Microsoft Active Accessibility 功能重迭。 它們可以在 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行中使用：

-   AriaProperties
-   AriaRole
-   AutomationId
-   ClassName
-   ClickablePoint
-   ControllerFor
-   文化特性
-   DescribedBy
-   FlowsTo
-   FrameworkId
-   IsContentElement
-   IsControlElement
-   IsDataValidForForm
-   IsRequiredForForm
-   ItemStatus
-   ItemType
-   LabeledBy
-   LocalizedControlType
-   Orientation

雖然 AcceleratorKey 和 AccessKey 消費者介面自動化屬性與 accKeyboardShortcut Microsoft Active Accessibility 屬性重迭，但您仍然可以在具有便捷鍵和快速鍵的控制項的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行中使用它們。 同樣地，ControlType 消費者介面自動化屬性會與 Microsoft Active Accessibility accRole 屬性重迭，但您仍然可以在 **IAccessibleEx** 的執行中使用它來為控制項定義更明確的角色。

因為 Microsoft Active Accessibility 屬性已涵蓋下列消費者介面自動化專案屬性，所以不需要在 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行中使用它們。



| 使用者介面自動化屬性 | Microsoft Active Accessibility 相等                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BoundingRectangle      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState，以 [**狀態 \_ 系統為 \_ 焦點**](object-state-constants.md)                                                                                       |
| IsEnabled              | accState， [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)                                                                               |
| IsKeyboardFocusable    | accState， [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md)                                                                                   |
| IsPassword             | accState， [**狀態 \_ 系統 \_ 保護**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Name                   | accName                                                                                                                                                                       |
| NativeWindowHandle     | [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState，[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) / [**狀態 \_ 系統 \_**](object-state-constants.md)未按螢幕 |
| ProcessId              | 由消費者介面自動化 core 提供                                                                                                                                                |



 

針對任何不支援的消費者介面自動化屬性，您的 [**IRawElementProviderSimple：： GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) 方法的執行應該將 *pRetVal* 參數設定為 VT \_ 空白，並傳回 S \_ OK。 傳回 [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) 可能會導致 MSAA 對 UIA Proxy 移除對應屬性的預設對應。

## <a name="control-patterns"></a>控制項模式

下列消費者介面自動化控制項模式不會與 Microsoft Active Accessibility 功能重迭。 它們可以在 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行中使用：

-   Dock
-   ExpandCollapse
-   方格
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   資料表
-   TableItem
-   轉換

針對 RangeValue 和轉換控制項模式，消費者介面自動化控制項模式和 Microsoft Active Accessibility 方法之間有一些方法重迭。 在這些情況下，兩者都必須執行。 例如，Microsoft Active Accessibility 的 [**IAccessible：： get \_ AccValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 和 [**IAccessible：:p 的 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) 方法都必須實作為消費者介面自動化 [**system.windows.automation.provider.irangevalueprovider>：： Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) 和 [**system.windows.automation.provider.irangevalueprovider>：： SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) 方法。 就內部而言，執行可以共用程式碼。 執行這兩個集合的這項需求可避免使用部分模式介面，同時讓現有 Microsoft Active Accessibility 用戶端可以使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。

當控制項具有以下所述的其中一個角色時，不需要下列消費者介面自動化控制項模式;否則，應該明確地支援（如果相關）。



| 消費者介面自動化控制項模式 | Microsoft Active Accessibility 角色                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**角色 \_系統 \_ 按鈕**](object-roles.md)、 [**角色 \_ 系統 \_ MENUITEM**](object-roles.md)、 [**角色 \_ 系統 \_ BUTTONDROPDOWN**](object-roles.md)、 [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)，以及 accDefaultAction 屬性值不是 **Null** 的任何其他角色。 |
| SelectionItemPattern          | [**角色 \_系統 \_ 的 [系統**](object-roles.md)]，[ [**角色 \_ 系統] \_ 選項按鈕**](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**角色 \_ 系統 \_ 清單**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**角色 \_ 系統 \_ CHECKBUTTON**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**角色 \_當 \_**](object-roles.md) accValue 屬性的值不是 **Null** 時，系統文字 (不是唯讀) 、 [**role \_ system \_ PROGRESSBAR**](object-roles.md)、 [**role \_ system \_ COMBOBOX**](object-roles.md)和任何其他角色。                                                                            |
| WindowPattern                 | 最上層 Microsoft Win32 **HWND** s 自動支援。                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>消費者介面自動化屬性已變更事件的 WinEvents

除了針對 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)所定義的事件之外，也會定義下列事件識別碼，並可搭配 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 實作為相對應消費者介面自動化屬性的屬性變更事件使用。 這些使用的機制與針對 **IAccessible** 定義的事件相同。 如需詳細資訊，請參閱 [WinEvents](winevents-infrastructure.md)。



| IAccessibleEx 實施的 New-winevent 識別碼                                                                                              | Microsoft Active Accessibility 的相關 New-winevent 識別碼                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ AriaPropertiesPropertyId**](uiauto-automation-element-propids.md)                                    | 無                                                                                   |
| [**UIA \_ AriaRolePropertyId**](uiauto-automation-element-propids.md)                                                | 無                                                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)                                      | 無                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                                          | 無                                                                                   |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) | [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ FlowsToPropertyId**](uiauto-automation-element-propids.md)                                                  | 無                                                                                   |
| [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md)                                                           | 無                                                                                   |
| [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md)                                       | 無                                                                                   |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md)                                                   | 無                                                                                   |
| [**UIA \_ IsDataValidForFormPropertyId**](uiauto-automation-element-propids.md)                            | 無                                                                                   |
| [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)                                              | [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                                            | 無                                                                                   |
| [**UIA \_ MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md)                     | 無                                                                                   |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md)           | 無                                                                                   |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)         | [**事件 \_ 物件 \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md)                   | 無                                                                                   |
| [**UIA \_ ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md)               | 無                                                                                   |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)             | [**事件 \_ 物件 \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md)                       | 無                                                                                   |
| [**UIA \_ ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md)                                 | [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md)         |



 

針對上面有 \_ 列出事件物件值的事件 \_ ，除了列出的已變更事件之外， [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 的執行也應該引發此事件。 這可讓現有的 **IAccessibleEx** 用戶端程式代碼繼續運作，同時將更細微的事件資訊傳達給感興趣的用戶端。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[IAccessibleEx 介面](iaccessibleex.md)
</dt> </dl>

 

 





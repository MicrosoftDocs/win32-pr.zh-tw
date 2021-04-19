---
title: SelectionItem 控制項模式
description: 描述執行 ISelectionItemProvider 的方針和慣例，包括屬性、方法和事件的相關資訊。
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- 消費者介面自動化，執行 SelectionItem 控制項模式
- 消費者介面自動化，SelectionItem 控制項模式
- 消費者介面自動化、ISelectionItemProvider
- ISelectionItemProvider
- 執行消費者介面自動化 SelectionItem 控制項模式
- SelectionItem 控制項模式
- 控制項模式，ISelectionItemProvider
- 控制模式，消費者介面自動化執行 SelectionItem
- 控制項模式，SelectionItem
- 介面，ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966783"
---
# <a name="selectionitem-control-pattern"></a>SelectionItem 控制項模式

描述執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)的方針和慣例，包括屬性、方法和事件的相關資訊。 **SelectionItem** 控制項模式用來支援控制項，這些控制項可作為執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)之容器控制項的個別可選取子專案。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ISelectionItemProvider** 的必要成員](#required-members-for-iselectionitemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **SelectionItem** 控制項模式時，請注意下列方針和慣例：

-   管理子控制項以執行 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)的單一選取控制項（例如 Windows 的 **顯示內容** 對話方塊中的 [**螢幕解析度**] 滑杆）應該會執行 [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider);其子系應同時執行 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)和 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。

## <a name="required-members-for-iselectionitemprovider"></a>**ISelectionItemProvider** 的必要成員

執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) 介面需要下列屬性、方法和事件。



| 必要成員                                                                                                                        | 成員類型 | 備註 |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | 方法      | 無  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | 屬性    | 無  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | 方法      | 無  |
| [**選擇**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | 方法      | 無  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | 屬性    | 無  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)         | 事件       | 無  |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | 事件       | 無  |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | 事件       | 無  |



 

如果 [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)、 [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)或 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection)的結果是單一選取的專案，則應引發 **ElementSelected** 事件 ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) ; 否則，請將 **ElementAddedToSelection** (UIA SelectionItem ElementAddedToSelectionEventId) 或 **ElementRemovedFromSelection** (UIA SelectionItem ElementRemovedFromSelectionEventId) 事件適當。 [**\_ \_**](uiauto-event-ids.md) [**\_ \_**](uiauto-event-ids.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 





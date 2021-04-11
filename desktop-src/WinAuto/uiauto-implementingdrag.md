---
title: 拖曳控制項模式
description: 提供使用 IDragProvider 來執行拖曳控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。 拖曳控制項模式用來支援可拖曳的控制項，或具有可拖曳專案的控制項。
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- 消費者介面自動化，執行拖曳控制項模式
- 消費者介面自動化，拖曳控制項模式
- 消費者介面自動化、IDragProvider
- IDragProvider
- 執行消費者介面自動化拖曳控制項模式
- 拖曳控制項模式
- 控制項模式，IDragProvider
- 控制項模式，實施消費者介面自動化拖曳
- 控制項模式，拖曳
- 介面，IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023697"
---
# <a name="drag-control-pattern"></a>拖曳控制項模式

提供使用 [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider)來執行 **拖曳** 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。 **拖曳** 控制項模式用來支援可拖曳的控制項，或具有可拖曳專案的控制項。

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

當您執行 **拖曳** 控制項模式時，請使用下列方針和慣例：

-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider)介面支援兩種不同的拖曳樣式：來源/目標樣式，以及僅限來源的樣式。 您必須選擇最適合拖放案例的樣式：
    -   **來源/目標樣式：** 每個可能的放置目標都是以實 [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) 介面的元素來表示。 在拖曳作業期間，Microsoft 消費者介面自動化的事件是來自正在拖曳的元素，以及從放置目標元素。
    -   **僅限來源樣式：** 卸載目標不會以消費者介面自動化元素表示。 在拖曳作業期間，事件只源自于正在拖曳的元素。
-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) 是唯讀介面，適用于監視拖曳作業。 您無法使用它來控制拖曳作業。 您可以藉由將滑鼠輸入傳送至控制項，將拖曳作業自動化。
-   需要 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性。
-   [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)和 [**IDragProvider：:D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)屬性是僅限來源樣式的實作為必要屬性，且禁止來源/目標樣式的執行。 在來源/目標樣式的執行中，可以查詢放置目標元素的卸載效果。
-   [**IDragProvider：： GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)屬性工作表示拖曳多個專案。 當使用者開始拖曳作業時，您必須建立新的消費者介面自動化專案，做為事件來源元素。 這個新的元素會引發來源專案在來源/目標或僅限來源模式下引發的所有事件，但實際上不會拖曳的元素會引發任何事件。 當拖曳作業完成時，摧毀事件來源元素。
-   專案必須在變更時，引發 **DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) 和 **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) 屬性的屬性變更事件。 其他屬性的屬性變更事件是允許的，但可以從必要的 **DragStart** 中推斷 ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 、 **DragCancel** ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) ，以及 **DragComplete** ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。
-   

## <a name="required-members-for-idragprovider"></a>**IDragProvider** 的必要成員

執行 [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) 介面需要下列屬性和方法。



| 必要成員                                                                        | 成員類型 | 備註                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | 屬性    | 無                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | 屬性    | 僅限來源樣式的執行所需。                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | 屬性    | 如果抓取專案有一個以上可能的卸載效果，則為必要項。 |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | 方法      | 多重專案拖曳作業的必要專案。                                  |
| [**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)       | 事件       | 無                                                                          |
| [**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)     | 事件       | 無                                                                          |
| [**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md) | 事件       | 無                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[DropTarget 控制項模式](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[消費者介面自動化的拖放支援](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 
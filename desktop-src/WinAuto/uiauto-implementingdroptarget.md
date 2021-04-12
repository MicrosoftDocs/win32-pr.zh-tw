---
title: DropTarget 控制項模式
description: 提供使用 IDropTargetProvider 來執行 DropTarget 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- 消費者介面自動化，執行 DropTarget 控制項模式
- 消費者介面自動化，DropTarget 控制項模式
- 消費者介面自動化、IDropTargetProvider
- IDropTargetProvider
- 執行消費者介面自動化 DropTarget 控制項模式
- DropTarget 控制項模式
- 控制項模式，IDropTargetProvider
- 控制模式，消費者介面自動化執行 DropTarget
- 控制項模式，DropTarget
- 介面，IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315670"
---
# <a name="droptarget-control-pattern"></a>DropTarget 控制項模式

提供使用 [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider)來執行 **DropTarget** 控制項模式的指導方針和慣例，包括屬性和方法的相關資訊。 **DropTarget** 控制項模式是用來支援可作為拖放作業目標的控制項。

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **DropTarget** 控制項模式時，請使用下列指導方針和慣例：

-   當拖曳作業正在進行時，必須支援 **DropTarget** 模式。 即使未進行拖曳作業，也可以支援此功能。
-   [**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)屬性為必要項。
-   當目標有一個以上可能的卸載效果時，需要 [**IDropTargetProvider：:D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) 屬性。
-   專案變更時，專案必須引發 **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) 和 **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) 屬性的屬性變更事件。

## <a name="required-members-for-idroptargetprovider"></a>**IDropTargetProvider** 的必要成員

執行 [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) 介面需要下列屬性和方法。



| 必要成員                                                                              | 成員類型 | 備註                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | 屬性    | 無                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | 屬性    | 如果放置目標支援多個可能的卸載效果，則為必要項。 |
| [**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | 事件       | 無                                                                     |
| [**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | 事件       | 無                                                                     |
| [**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)     | 事件       | 無                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[拖曳控制項模式](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[消費者介面自動化的拖放支援](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 
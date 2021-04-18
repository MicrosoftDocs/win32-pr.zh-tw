---
title: 消費者介面自動化的拖放支援
description: 本主題描述的控制項模式會公開專案拖放功能的相關資訊。
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- 消費者介面自動化，拖放支援
- 消費者介面自動化，拖曳模式總覽
- 消費者介面自動化，DropTarget 模式總覽
- 消費者介面自動化，拖放總覽
- 拖放模式，關於
- 拖曳控制項模式
- DropTarget 控制項模式
- 控制項模式，拖曳
- 控制項模式，DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965026"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>消費者介面自動化的拖放支援

Microsoft 消費者介面自動化定義兩種控制項模式，可支援拖放案例、 [拖曳](/windows/desktop/WinAuto/uiauto-implementingdrag) 控制項模式，以及 [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) 控制項模式。 您可以針對可以拖曳的元素，以及可接收拖曳專案的專案 DropTarget 控制項模式，來執行拖曳控制項模式;也就是放置目標。 這兩個控制項模式會公開輔助技術可用於協助協助工具使用者完成拖放作業的資訊。

-   [拖曳樣式](#dragging-styles)
    -   [來源/目標樣式](#sourcetarget-style)
    -   [僅限來源的樣式](#source-only-style)
-   [拖曳多個專案](#dragging-multiple-items)
-   [拖放的用戶端介面](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>拖曳樣式

當您針對可 [拖曳](/windows/desktop/WinAuto/uiauto-implementingdrag) 的元素執行拖曳控制項模式時，您必須決定要執行 *來源/目標* 拖曳樣式，還是要執行 *僅限來源* 的拖曳樣式。

### <a name="sourcetarget-style"></a>來源/目標樣式

在拖放的來源/目標樣式中，拖曳的元素 (「來源」 ) ，而「目標」 )  (的放置目標元素則是相異的，且每個專案都會引發一組不同的事件。 以下是使用來源/目標樣式之拖曳操作的生命週期： <dl> 當使用者開始拖曳作業時：

-   來源會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。
-   來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。
-   目標會更新其 [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性。

  
當拖曳作業進入目的地區域時：

-   目標會引發 System.windows.dragdrop.dragenter> ([**UIA \_ DropTarget \_ DragEnterEventId**](uiauto-event-ids.md)) 事件。

  
當拖曳作業離開目的地區域時：

-   目標會引發 DragLeave ([**UIA \_ DropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)) 事件。

  
當使用者放開非目標的拖曳專案時：

-   來源會引發 DragCancel ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) 事件。
-   來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。

  
當使用者在目標上放開拖曳的專案時：

-   來源會引發 DragComplete ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。
-   來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。
-   目標會設定 [**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性，以指出所發生的效果。
-   目標會引發已卸載的 ([**UIA \_ DropTarget \_ DroppedEventId**](uiauto-event-ids.md)) 事件。

  
</dl>

來源與目標物件中的事件是密切相關的，但相異。 所要拖曳之內容的相關資料來自來源，而關於「發生什麼事」和「發生什麼事」的資料則來自于目標。

當拖曳作業正在進行時，拖曳的專案可以在作業完成之前，任意次數地拖曳至目的地區域。

任何需要更新其 [**IDropTargetProvider：:D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) 屬性的放置目標，都應該在該屬性上引發額外的屬性變更事件。

### <a name="source-only-style"></a>僅限來源的樣式

僅限來源的拖曳樣式可讓提供者避免執行卸載目標。 未執行卸載目標有助於降低執行成本，但不會提供協助工具用戶端應用程式任何有關接收捨棄之物件的資訊。 以下是使用僅限來源樣式之拖曳作業的生命週期： <dl> 當使用者開始拖曳作業時：

-   來源會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。
-   來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。

  
當拖曳作業進入目的地區域時：

-   來源會將 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性設定為適當的值。

  
當拖曳作業離開目的地區域時：

-   來源會將 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性設定為適當的值。

  
當使用者放開非目標的拖曳專案時：

-   來源會引發 DragCancel ([**UIA \_ 拖曳 \_ DragCancelEventId**](uiauto-event-ids.md)) 事件。
-   來源會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **FALSE**。

  
當使用者在目標上放開拖曳的專案時：

-   來源會引發 DragComplete ([**UIA \_ 拖曳 \_ DragCompleteEventId**](uiauto-event-ids.md)) 事件。
-   來源會設定 [**IDragProvider：:D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性，以指出卸載專案時所發生的效果。

  
</dl>

## <a name="dragging-multiple-items"></a>拖曳多個專案

如果提供者所執行的拖放作業可讓使用者同時拖曳多個物件，則提供者會依照上一節所述，使用來源/目標或僅限來源的樣式，但差異較小。 當使用者開始拖曳作業時，提供者會建立主要來源元素，以代表正在拖曳的整組專案。 主要來源元素會代表一組拖曳的專案來引發所有事件;這些專案不會引發自己的任何事件。<dl> 當使用者開始拖曳作業時：

-   提供者會建立主要來源元素。
-   主要來源元素會引發 DragStart ([**UIA \_ 拖曳 \_ DragStartEventId**](uiauto-event-ids.md)) 事件。
-   主要來源元素會將 [**IDragProvider：： IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) 屬性設定為 **TRUE**。
-   主要來源元素會更新抓取專案的清單，以包含所有要拖曳的專案，讓 [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) 方法可以取得清單。

  
</dl>

針對該點，主要來源專案會依照上一節所述，執行與來源元素相同的角色。

## <a name="client-interfaces-for-drag-and-drop"></a>拖放的用戶端介面

消費者介面自動化用戶端應用程式會使用 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 和 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) 介面來存取 UI 元素的拖放資訊。

 

 
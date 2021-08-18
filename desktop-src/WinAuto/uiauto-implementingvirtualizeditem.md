---
title: VirtualizedItem 控制項模式
description: 描述執行 IVirtualizedItemProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- 消費者介面自動化，執行 VirtualizedItem 控制項模式
- 消費者介面自動化，VirtualizedItem 控制項模式
- 消費者介面自動化、IVirtualizedItemProvider
- IVirtualizedItemProvider
- 執行消費者介面自動化 VirtualizedItem 控制項模式
- VirtualizedItem 控制項模式
- 控制項模式，IVirtualizedItemProvider
- 控制模式，消費者介面自動化執行 VirtualizedItem
- 控制項模式，VirtualizedItem
- 介面，IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d883eec2e0f5fa4c4ede4c3fa2ef73770cc706114b6536ad002d11ff73f8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997758"
---
# <a name="virtualizeditem-control-pattern"></a>VirtualizedItem 控制項模式

描述執行 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)的方針和慣例，包括屬性和方法的相關資訊。 **VirtualizedItem** 控制項模式用來支援虛擬化專案，這些專案是由 Microsoft 消費者介面自動化樹狀結構中的預留位置自動化元素所表示的專案。

虛擬化專案可以包含從支援 [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式的控制項取出的專案，或是從支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式的控制項抓取的虛擬化内嵌物件。 虛擬化專案的預留位置可能尚未載入所有消費者介面自動化屬性的資料，而且可能會傳回 [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) ，以回應無法使用的屬性查詢。 **VirtualizedItem** 控制項模式提供了一種方法，可讓您瞭解虛擬專案，讓專案可以使用完整資訊，而且可以在消費者介面自動化樹狀結構中建立專案的完整自動化專案。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IVirtualizedItemProvider** 的必要成員](#required-members-for-ivirtualizeditemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **VirtualizedItem** 控制項模式時，請注意下列方針和慣例：

-   任何可以虛擬化消費者介面自動化預留位置專案都必須藉由公開 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)介面，支援 **VirtualizedItem** 控制項模式。
-   呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 時，預留位置物件必須使用其屬性和控制項模式的完整實作為更新。
-   當呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 時，提供者可以變更此分割區，讓虛擬化專案變成可供觀看。 不需要將專案帶入 view;不過，非虛擬化的專案應該支援 [**IScrollItemProvider：： ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) 方法。

## <a name="required-members-for-ivirtualizeditemprovider"></a>**IVirtualizedItemProvider** 的必要成員

執行 [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) 介面需要下列屬性和方法。



| 必要成員                                           | 成員類型 | 備註 |
|------------------------------------------------------------|-------------|-------|
| [**實現**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行消費者介面自動化 >itemcontainer 控制項模式](uiauto-implementingitemcontainer.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[使用虛擬化專案](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 





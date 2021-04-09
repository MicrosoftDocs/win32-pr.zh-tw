---
title: 停駐控制項模式
description: 描述執行 IDockProvider 的方針和慣例，包括屬性和方法的相關資訊。 Dock 控制項模式是用來公開停駐容器內控制項的停駐屬性。
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- 消費者介面自動化，實施 dock 控制項模式
- 消費者介面自動化，停駐控制項模式
- 消費者介面自動化、IDockProvider
- IDockProvider
- 執行消費者介面自動化 dock 控制項模式
- 停駐控制項模式
- 控制項模式，IDockProvider
- 控制模式，實施消費者介面自動化 dock
- 控制項模式，dock
- 介面，IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839875"
---
# <a name="dock-control-pattern"></a>停駐控制項模式

描述執行 [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)的方針和慣例，包括屬性和方法的相關資訊。 **Dock** 控制項模式是用來公開停駐容器內控制項的停駐屬性。

停駐容器是一種控制項，可讓您依垂直和水平的相對位置排列子項目。 下圖顯示具有兩個子項目的停駐容器。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

![顯示具有兩個停駐子系之銜接容器的螢幕擷取畫面](images/dockxmpl.jpg)

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IDockProvider** 的必要成員](#required-members-for-idockprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在實施 **Dock** 控制項模式時，請注意下列方針和慣例：

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) 不會公開停駐容器的任何屬性，或停駐于停駐容器內目前控制項連續的控制項屬性。
-   控制項會根據其目前的疊置順序，在彼此相對的位置停駐；疊置順序的位置愈高，控制項離停駐容器的指定邊緣就愈遠。
-   如果停駐容器可以調整大小，容器內的任何停駐控制項會再次對齊到原始停駐的相同邊緣。 停駐的控制項也會調整大小，以根據其 [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) 屬性的銜接行為填滿容器內的任何空間。 例如，如果指定了 **DockPosition \_ Top** ，則控制項的左邊和右邊將會展開以填滿任何可用的空間。 如果指定了 **DockPosition \_ Fill** ，則會展開控制項的四個邊來填滿任何可用的空間。
-   在多監視器系統上，控制項應停駐到目前監視器的左或右邊。 若不可行，則應停駐到最左邊監視器的左邊，或最右邊監視器的右邊。

## <a name="required-members-for-idockprovider"></a>**IDockProvider** 的必要成員

執行 [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) 介面需要下列屬性和方法。



| 必要成員                                                | 成員類型 | 備註 |
|-----------------------------------------------------------------|-------------|-------|
| [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | 屬性    | 無  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 





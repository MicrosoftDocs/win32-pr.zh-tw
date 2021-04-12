---
title: 切換控制項模式
description: 描述執行 IToggleProvider 的方針和慣例，包括屬性和方法的相關資訊。 切換控制項模式是用來支援可在一組狀態之間迴圈的控制項，並在設定之後維護狀態。
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- 消費者介面自動化，執行切換控制項模式
- 消費者介面自動化，切換控制項模式
- 消費者介面自動化、IToggleProvider
- IToggleProvider
- 執行消費者介面自動化切換控制項模式
- 切換控制項模式
- 控制項模式，IToggleProvider
- 控制項模式，執行消費者介面自動化切換
- 控制項模式，切換
- 介面，IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372003"
---
# <a name="toggle-control-pattern"></a>切換控制項模式

描述執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)的方針和慣例，包括屬性和方法的相關資訊。 **切換** 控制項模式是用來支援可在一組狀態之間迴圈的控制項，並在設定之後維護狀態。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IToggleProvider** 的必要成員](#required-members-for-itoggleprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **切換** 控制項模式時，請注意下列方針和慣例：

-   啟動時不會維持狀態的控制項（例如按鈕、工具列按鈕和超連結）必須改為執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) 。
-   控制項必須依照下列順序，迴圈切換其切換狀態 ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) ： **ToggleState \_ On**、 **ToggleState \_ Off** 和（如果支援的話） **ToggleState \_ 不定**。
-   **切換** 不會提供設定狀態方法，因為在三個狀態的直接設定方面有問題，而不會迴圈其適當的 [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) 序列。
-   選項按鈕控制項不會執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)，因為它無法迴圈其有效狀態。

## <a name="required-members-for-itoggleprovider"></a>**IToggleProvider** 的必要成員

執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) 介面需要下列屬性和方法。



| 必要成員                                          | 成員類型 | 備註 |
|-----------------------------------------------------------|-------------|-------|
| [**切換**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | 方法      | 無  |
| [**ToggleState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | 屬性    | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 





---
title: RangeValue 控制項模式
description: 描述執行 System.windows.automation.provider.irangevalueprovider> 的方針和慣例，包括屬性和方法的相關資訊。 RangeValue 控制項模式用來支援可以設定為範圍內值的控制項。
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- 消費者介面自動化，執行 RangeValue 控制項模式
- 消費者介面自動化，RangeValue 控制項模式
- 消費者介面自動化、System.windows.automation.provider.irangevalueprovider>
- IRangeValueProvider
- 執行消費者介面自動化 RangeValue 控制項模式
- RangeValue 控制項模式
- 控制項模式，System.windows.automation.provider.irangevalueprovider>
- 控制模式，消費者介面自動化執行 RangeValue
- 控制項模式，RangeValue
- 介面，System.windows.automation.provider.irangevalueprovider>
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae87ca25fd1ada2f57ce77412fb589875792541fd2b5d31d6eb0aa86192dee36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114859"
---
# <a name="rangevalue-control-pattern"></a>RangeValue 控制項模式

描述執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)的方針和慣例，包括屬性和方法的相關資訊。 **RangeValue** 控制項模式用來支援可以設定為範圍內值的控制項。

如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**System.windows.automation.provider.irangevalueprovider>** 的必要成員](#required-members-for-irangevalueprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **RangeValue** 控制項模式時，請注意下列方針和慣例：

-   控制項可以根據地區設定或使用者偏好設定，重新劃分所支援屬性的刻度。 例如，溫度計控制項可以設為顯示華氏或攝氏溫度。
-   範圍值不明確的控制項 (如進度列或滑桿) 應將這些值正規化。

## <a name="required-members-for-irangevalueprovider"></a>**System.windows.automation.provider.irangevalueprovider>** 的必要成員

執行 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面需要下列屬性和方法。



| 必要成員                                              | 成員類型 | 備註 |
|---------------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | 屬性    | 無  |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | 屬性    | 無  |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | 屬性    | 無  |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | 屬性    | 無  |
| [**最大值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | 屬性    | 無  |
| [**最小值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | 屬性    | 無  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 





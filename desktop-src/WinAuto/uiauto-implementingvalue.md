---
title: 值控制項模式
description: 描述執行 IValueProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- 消費者介面自動化，實值控制項模式
- 消費者介面自動化，值控制項模式
- 消費者介面自動化、IValueProvider
- IValueProvider
- 實消費者介面自動化值控制項模式
- 值控制項模式
- 控制項模式，IValueProvider
- 控制項模式，實施消費者介面自動化值
- 控制項模式、值
- 介面，IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b30d8c84bc5f998d55ee17d7699bb37f33b7e19c52a2694578c3d11ef1d888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997801"
---
# <a name="value-control-pattern"></a>值控制項模式

描述執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)的方針和慣例，包括屬性和方法的相關資訊。 **值** 控制項模式用來支援具有未跨越範圍且可以表示為字串之內建值的控制項。

您可以根據控制項及其設定，來編輯值字串。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IValueProvider** 的必要成員](#required-members-for-ivalueprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在實 **值** 控制項模式時，請注意下列方針和慣例：

-   如果任何專案的值都是可編輯的，則控制項（例如清單專案或樹狀結構專案）必須支援 **值** 控制項模式，不論控制項目前的編輯模式為何。 如果子專案是可編輯的，父控制項也必須支援 **值** 控制項模式。 下圖顯示可編輯清單專案的範例。

    ![顯示可編輯清單專案的圖例](images/uia-valuepattern-editable-listitem.jpg)

- 單一和多行編輯控制項必須執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 來公開其唯讀內容。
- 如果可以變更多行編輯控制項的內容，則必須執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 。
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 不支援抓取格式化資訊或子字串值。 在這些案例中執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 。
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)必須由 Microsoft Word (的色彩選擇器選取控制項等控制項來執行，請參閱下圖) ，它支援色彩 (值之間的字串對應，例如，"黃色" ) 和相等的內部 [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)值。

    ![顯示色樣字串對應的圖例](images/uia-valuepattern-colorpicker.jpg)

- 控制項應將其 **IsEnabled** 屬性設定為 **TRUE** ，並在允許呼叫 [**ITextProvider：： SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)之前，將其 [**ITextProvider：： IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)屬性設定為 **FALSE** 。

## <a name="required-members-for-ivalueprovider"></a>**IValueProvider** 的必要成員

執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 介面需要下列屬性和方法。



| 必要成員                                       | 成員類型 | 備註 |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | 屬性    | 無  |
| [**值**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | 屬性    | 無  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | 方法      | 無  |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> <dt>

[Text 和 TextRange 控制項模式](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 
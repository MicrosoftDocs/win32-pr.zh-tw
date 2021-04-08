---
title: SpreadsheetItem 控制項模式
description: 描述執行 ISpreadsheetItemProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- 消費者介面自動化，執行 SpreadsheetItem 控制項模式
- 消費者介面自動化，SpreadsheetItem 控制項模式
- 消費者介面自動化、ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- 執行消費者介面自動化 SpreadsheetItem 控制項模式
- SpreadsheetItem 控制項模式
- 控制項模式，ISpreadsheetItemProvider
- 控制模式，消費者介面自動化執行 SpreadsheetItem
- 控制項模式，SpreadsheetItem
- 介面，ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023964"
---
# <a name="spreadsheetitem-control-pattern"></a>SpreadsheetItem 控制項模式

描述執行 [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)的方針和慣例，包括屬性和方法的相關資訊。 **SpreadsheetItem** 控制項模式是用來公開試算表或其他以方格為基礎之檔中的儲存格屬性。

**SpreadsheetItem** 控制項模式與 [GridItem](uiauto-implementinggriditem.md)控制項模式緊密相關;實 **SpreadsheetItem** 控制項模式的控制項也應執行 GridItem 控制項模式。 控制項也可以執行 [TableItem](uiauto-implementingtableitem.md) 控制項模式（如果適用）。 如需執行這些控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ISpreadsheetItemProvider** 的必要成員](#required-members-for-ispreadsheetitemprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **SpreadsheetItem** 控制項模式時，請注意下列方針和慣例：

-   在執行 [**ISpreadsheetItemProvider：： GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) 和 [**ISpreadsheetItemProvider：： GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) 方法時，請參閱 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 檔。 這些方法都會傳回陣列，讓提供者支援單一資料格上的多個批註。
-   某些類型的注釋不需要完整執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面。 例如，可以藉由讓 [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) 傳回 [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)的文字屬性識別碼，並讓 [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) 傳回 null 值，來表示簡單的拼寫錯誤指標。

## <a name="required-members-for-ispreadsheetitemprovider"></a>**ISpreadsheetItemProvider** 的必要成員

執行 [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) 介面需要下列屬性和方法。



| 必要成員                                                                         | 成員類型 | 備註                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | 屬性    | 因為資料格的 [Value](value-property.md)屬性通常會傳回資料格的計算值，所以必須執行個別的 [**公式**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)屬性。 如果未設定任何公式， **公式** 屬性應為 **Null** 。 |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | 方法      | 傳回專案提供者的陣列，這些提供者會參考連結至此儲存格的批註。 如果批註沒有連結的提供者，陣列內的指標可以是 null。                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | 方法      | 傳回批註類型識別碼的陣列，描述此資料格上的批註。 陣列的大小必須與 [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)所傳回的陣列相同。                                         |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[試算表控制項模式](uiauto-implementingspreadsheet.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 
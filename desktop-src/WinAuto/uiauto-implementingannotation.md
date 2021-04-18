---
title: Annotation 控制項模式
description: 描述執行 IAnnotationProvider 的方針和慣例，包括屬性和方法的相關資訊。 批註控制項模式是用來公開檔中批註的屬性。
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- 消費者介面自動化，執行批註控制項模式
- 消費者介面自動化，annotation 控制項模式
- 消費者介面自動化、IAnnotationProvider
- IAnnotationProvider
- 執行消費者介面自動化 annotation 控制項模式
- annotation 控制項模式
- 控制項模式，IAnnotationProvider
- 控制項模式，執行消費者介面自動化注釋
- 控制項模式、注釋
- 介面，IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a0441816e548faaa9076b3a9717c0aa76f08a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966044"
---
# <a name="annotation-control-pattern"></a>Annotation 控制項模式

描述執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)的方針和慣例，包括屬性和方法的相關資訊。 **批註** 控制項模式是用來公開檔中批註的屬性。

其中一個範例是檔邊界中的批註批註提示，並連接到某些檔文字或試算表儲存格。

下圖顯示批註的範例。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

![顯示檔中批註 baloon 的螢幕擷取畫面](images/annotation.png)

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IAnnotationProvider** 的必要成員](#required-members-for-iannotationprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **注釋** 控制項模式時，請注意下列方針和慣例：

-   有許多不同類型的批註。 Uiautomationclient.dll 標頭檔會定義一組命名的常數值，這些值會識別 Microsoft 消費者介面自動化支援的批註類型。 如需詳細資訊，請參閱 [**批註類型識別碼**](uiauto-annotation-type-identifiers.md)。
-   如果您使用 [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md)，則必須執行 [**IAnnotationProvider：： AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) 屬性，讓用戶端能夠探索批註類型的名稱。 您不需要為標準注釋類型執行 **AnnotationTypeName** ，因為消費者介面自動化提供預設名稱，但如果您需要覆寫預設名稱，可以執行此動作。
-   [**IAnnotationProvider：： Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)屬性是選擇性的。
-   [**IAnnotationProvider：:D atetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)屬性是選擇性的。
-   [**IAnnotationProvider：： Target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)屬性是必要的，因為它會將批註連結至 ui 元素，讓用戶端可以從批註導覽至批註所參考的 ui 專案。
-   由於批註可以採用許多不同的表單，因此 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面不會定義用來儲存批註值或文字的屬性。 簡單的批註應該會公開 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 介面，而 [**IValueProvider：： Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) 屬性應該會傳回指定註解文字的唯讀值。 更豐富的批註應該會公開 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 介面，以提供更豐富的文字給用戶端。
-   從 UI 元素導覽至專案上的注釋，取決於要標注的元素類型，如下所示：
    -   針對試算表儲存格，請執行 [**ISpreadsheetItemProvider：： GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) 方法來參考批註。
    -   若為文字內容，請在 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面上執行 [**AnnotationObjects**](uiauto-textattribute-ids.md)文字屬性，以參考批註。
-   某些類型的注釋不需要完整執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面。 例如，您可以讓 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面傳回 [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)的 [**AnnotationTypes**](uiauto-textattribute-ids.md) text 屬性，以及 [**AnnotationObjects**](uiauto-textattribute-ids.md) text 屬性的 null 值，來表示簡單的拼寫錯誤指標。
-   在不可見的 UI 元素上執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面可能會很有用。 例如，您可以建立一個非可見的消費者介面自動化元素來執行 **IAnnotationProvider** ，以提供有關文法錯誤的延伸資訊。
-   如果控制項包含重迭的批註，以文字為基礎之控制項中的注釋可能會很複雜。 使用下列指導方針來處理複雜的批註：
    -   沒有批註的文字範圍應該會傳回 [**AnnotationTypes**](uiauto-textattribute-ids.md) text 屬性的空陣列，以及 [**AnnotationObjects**](uiauto-textattribute-ids.md) text 屬性的空陣列。
    -   具有一個批註的文字範圍應針對 [**AnnotationTypes**](uiauto-textattribute-ids.md)文字屬性傳回一個整數值的陣列，並針對 [**AnnotationObjects**](uiauto-textattribute-ids.md) Text 屬性傳回一個 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)介面的陣列。
    -   具有多個批註的文字範圍應傳回 [**AnnotationTypes**](uiauto-textattribute-ids.md) text 屬性的多個整數值陣列，以及 [**AnnotationObjects**](uiauto-textattribute-ids.md) Text 屬性之相符 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)介面數目的陣列。
    -   具有不同批註的文字範圍（例如具有批註和非註解文字的範圍）應該會傳回 [**AnnotationTypes**](uiauto-textattribute-ids.md)和 [**AnnotationObjects**](uiauto-textattribute-ids.md)的 [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)屬性。 接收此回應的用戶端可以細分文字範圍，以找出批註的開始和結束位置。

## <a name="required-members-for-iannotationprovider"></a>**IAnnotationProvider** 的必要成員

執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面需要下列屬性。



| 必要成員                                                                | 成員類型 | 備註 |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | 屬性    | 無。 |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | 屬性    | 無。 |
| [**作者**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | 屬性    | 無。 |
| [**Datetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | 屬性    | 無。 |
| [**目標**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | 屬性    | 無。 |



 

此控制項模式沒有任何相關聯的事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 
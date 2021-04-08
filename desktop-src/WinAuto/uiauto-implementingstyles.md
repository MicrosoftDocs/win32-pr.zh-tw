---
title: 樣式控制項模式
description: 描述執行 IStylesProvider 的方針和慣例，包括屬性和方法的相關資訊。 樣式控制項模式是用來描述具有特定樣式、填滿色彩、填滿模式或圖形的 UI 元素。
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- 消費者介面自動化，執行樣式控制項模式
- 消費者介面自動化，樣式控制項模式
- 消費者介面自動化、IStylesProvider
- IStylesProvider
- 執行消費者介面自動化樣式控制項模式
- 樣式控制項模式
- 控制項模式，IStylesProvider
- 控制項模式，執行消費者介面自動化樣式
- 控制項模式、樣式
- 介面，IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682933"
---
# <a name="styles-control-pattern"></a>樣式控制項模式

描述執行 [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)的方針和慣例，包括屬性和方法的相關資訊。 **樣式** 控制項模式是用來描述具有特定樣式、填滿色彩、填滿模式或圖形的 UI 元素。

**樣式** 控制項模式特別適用于描述檔中的專案，這通常會有這類樣式。 樣式通常會攜帶適用于殘障客戶的資訊;例如，樣式可以將特定字串描述為檔的標題，或是將特定流程圖物件描述為鑽石或圓形。 如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**IStylesProvider** 的必要成員](#required-members-for-istylesprovider)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **樣式** 控制項模式時，請注意下列方針和慣例：

-   Uiautomationclient.dll 標頭檔會定義一組命名的常數值，用來識別數個常見的樣式。 如需詳細資訊，請參閱 [**樣式識別碼**](uiauto-style-identifiers.md)。
-   如果您使用 [**StyleId \_ 自訂**](uiauto-style-identifiers.md)，則必須執行 [**IStylesProvider：： StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) 屬性，讓用戶端能夠探索樣式的名稱。 您不需要執行標準樣式的 **StyleName** 屬性，因為 Microsoft 消費者介面自動化會提供預設名稱，但如果您需要覆寫預設名稱，則可以加以執行。
-   **樣式** 模式中的其他屬性是選擇性的;提供者可以針對不支援的屬性傳回 [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) 。
-   文字範圍中的樣式可透過下列文字屬性來表示：
    -   回應 [**StyleId**](uiauto-textattribute-ids.md) text 屬性的要求時，文字範圍應傳回 [**樣式識別碼**](uiauto-style-identifiers.md)中所述的其中一個樣式識別碼。
    -   如果使用 [**StyleId \_ Custom**](uiauto-style-identifiers.md) ，則文字範圍應傳回 [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) text 屬性的字串值，讓用戶端能夠探索樣式名稱。
    -   具有多個樣式的文字範圍（例如標題和一般文字）應該會傳回 [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)和 [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)屬性的特殊消費者介面自動化 [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)屬性。 接收此回應的用戶端可以細分文字範圍，以找出樣式的開頭和結尾。
-   應用程式可以使用各式各樣的樣式來描述物件，但是消費者介面自動化只代表最常見的物件。 若要表示其他樣式屬性，例如框線色彩，提供者可以傳回 [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) 屬性中的其他屬性清單。 這基本上是具有一組擴充屬性的屬性包，例如 "邊框： = 0xFF0000;BorderStyle = 點線」。 擴充屬性的值可以是應用程式特定的值。

## <a name="required-members-for-istylesprovider"></a>**IStylesProvider** 的必要成員

執行 [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) 介面需要下列屬性。



| 必要成員                                                            | 成員類型 | 備註 |
|-----------------------------------------------------------------------------|-------------|-------|
| [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | 屬性    | 無  |
| [**FillColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | 屬性    | 無  |
| [**FillPatternColor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | 屬性    | 無  |
| [**FillPatternStyle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | 屬性    | 無  |
| [**形狀**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | 屬性    | 無  |
| [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | 屬性    | 無  |
| [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | 屬性    | 無  |



 

此控制項模式沒有任何相關聯的方法或事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 
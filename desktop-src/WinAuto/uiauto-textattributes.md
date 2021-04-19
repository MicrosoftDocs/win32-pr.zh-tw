---
title: 消費者介面自動化 Text 屬性
description: 本主題說明 Microsoft 消費者介面自動化如何公開格式和樣式屬性 (文字內容) 的 text 屬性，並提供支援的文字屬性清單。
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- 消費者介面自動化，text 屬性
- text 屬性，關於
- 文字屬性、變異類型
- 文字屬性，資料類型
- 消費者介面自動化，屬性清單
- 消費者介面自動化，文字屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106980276"
---
# <a name="ui-automation-text-attributes"></a>消費者介面自動化 Text 屬性

本主題說明 Microsoft 消費者介面自動化如何公開格式和樣式屬性 (文字內容) 的 *text 屬性* ，並提供支援的文字屬性清單。

消費者介面自動化提供者會透過 [TextRange](uiauto-about-text-and-textrange-patterns.md)控制項模式的 [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)和 [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)方法來公開文字屬性。 用戶端應用程式會使用 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法來抓取文字範圍的特定文字屬性值。 用戶端可以使用 [**IUIAutomationTextRange：： FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) 方法，在文字範圍中搜尋具有特定屬性的文字。 如果找到任何相符的文字，方法會建立包含相符文字的新文字範圍。

**TextRange** 控制項模式支援下列清單中的 text 屬性。 屬性名稱衍生自消費者介面自動化的 text 屬性識別碼。 例如， **AnimationStyle** 屬性是由用戶端識別為 [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (定義于) uiautomationclient.dll 中，而提供者則是 AnimationStyle. h) 中定義的 **Text \_ Uiautomationcoreapi \_ attribute \_ GUID** (。 如需每個支援的 text 屬性的詳細資訊，請參閱 [**文字屬性識別碼**](uiauto-textattribute-ids.md)。

> [!Note]  
> 從 Windows 8 開始支援列出的部分屬性。 如需有關版本支援的附注，請參閱 [**文字屬性識別碼**](uiauto-textattribute-ids.md) 。

 

本主題包含下列幾節：

-   [註釋屬性](#annotation-attributes)
-   [字型屬性](#font-attributes)
-   [語言屬性](#language-attributes)
-   [連結屬性](#link-attribute)
-   [頁面邊界屬性](#page-margin-attributes)
-   [文字對齊屬性](#text-alignment-attributes)
-   [文字色彩屬性](#text-color-attributes)
-   [文字裝飾屬性](#text-decoration-attributes)
-   [文字樣式屬性](#text-style-attributes)
-   [互動和選取屬性](#interaction-and-selection-attributes)
-   [相關主題](#related-topics)

## <a name="annotation-attributes"></a>註釋屬性

批註物件和批註類型可透過下列屬性取得。



| 屬性             | 識別碼                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a>字型屬性

您可以透過下列屬性取得字型的名稱、大小和權數。



| 屬性      | 識別碼                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>語言屬性

您可以透過下列屬性取得文字語言的相關資訊。



| 屬性              | 識別碼                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **文化特性**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>連結屬性

下列屬性提供的文字範圍是檔中連結的目標。



| 屬性 | 識別碼                                                                   |
|-----------|------------------------------------------------------------------------------|
| **連結**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>頁面邊界屬性

文字範圍的周框矩形不會公開頁面中文字的座標。 但是，提供者可以使用下列文字屬性來公開頁面邊界資訊。



| 屬性          | 識別碼                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>文字對齊屬性

您可以透過下列屬性取得文字對齊方式的相關資訊，例如縮排、定位鍵設定和水準對齊。



| 屬性                   | 識別碼                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **索引標籤**                    | [**UIA \_ TabsAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>文字色彩屬性

前景和背景文字色彩可透過下列 text 屬性取得。 這兩種色彩都指定為 [**COLORREF**](/windows/desktop/gdi/colorref) 資料類型。



| 屬性           | 識別碼                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>文字裝飾屬性

文字裝飾包括專案符號、底線和動畫等區域。 如果文字包含前置的專案符號或數位，則文字資料流程中應包含專案符號或數位所使用的符號或文字（如果適用）。

您可以透過下列屬性取得文字裝飾的相關資訊。



| 屬性              | 識別碼                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **BulletStyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>文字樣式屬性

您可以使用下列屬性來取得文字樣式的相關資訊。



| 屬性         | 識別碼                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>互動和選取屬性

您可以透過下列屬性，取得範圍和焦點狀態中目前文字選取範圍的相關資訊。



| 屬性              | 識別碼                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[關於消費者介面自動化 Text 和 TextRange 控制項模式](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Text 和 TextRange 控制項模式](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
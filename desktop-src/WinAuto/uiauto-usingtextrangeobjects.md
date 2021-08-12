---
title: 使用文字範圍
description: 本主題說明如何使用 IUIAutomationTextRange 介面的屬性和方法，來存取和操作以文字為基礎之控制項的文字內容。
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- 用戶端，使用文字範圍物件
- 以文字為基礎的控制項
- 用戶端、文字範圍
- 用戶端、TextRange 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563980"
---
# <a name="using-text-ranges"></a>使用文字範圍

本主題說明如何使用 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) 介面的屬性和方法，來存取和操作以文字為基礎之控制項的文字內容。 它包含下列區段：

-   [什麼是文字範圍？](#using-text-ranges)
-   [取得文字範圍物件](#acquiring-text-range-objects)
-   [選取文字範圍中的文字](#selecting-text-in-a-text-range)
-   [從文字範圍中取出文字](#retrieving-text-from-a-text-range)
-   [從文字範圍中取出文字屬性](#retrieving-text-attributes-from-a-text-range)
-   [從文字範圍中取出内嵌物件](#retrieving-embedded-objects-from-a-text-range)
-   [操作文字範圍](#manipulating-a-text-range)
-   [將文字範圍滾動至視野](#scrolling-a-text-range-into-view)
-   [取出文字範圍的封閉元素](#retrieving-the-enclosing-element-of-a-text-range)
-   [比較和複製文字範圍](#comparing-and-cloning-text-ranges)
-   [正在抓取注釋](#retrieving-annotations)
    -   [從文字範圍中取出批註類型](#retrieving-annotations-types-from-a-text-range)
    -   [從文字範圍中取出所有批註](#retrieving-all-annotations-from-a-text-range)
    -   [抓取特定注釋的相關資訊](#retrieving-information-about-a-particular-annotation)
    -   [正在抓取注釋目標文字](#retrieving-the-annotation-target-text)
-   [正在抓取視覺化樣式](#retrieving-visual-styles)
-   [從文字範圍叫用內容功能表](#invoking-context-menus-from-text-ranges)
-   [相關主題](#related-topics)

## <a name="what-is-a-text-range"></a>什麼是文字範圍？

Microsoft 消費者介面自動化 text 物件模型是以 *文字範圍* 的概念為基礎。 文字範圍是公開 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) 介面的物件，代表以文字為基礎之控制項中的連續文字範圍。 每個文字範圍都有起始端點和結束端點，而兩個端點之間的所有文字內容都被視為範圍的一部分。 起始端點和結束端點位於相同位置的文字範圍稱為「 *退化* (」或「空的) 文字範圍。 退化文字範圍用來標示控制項文字內的特定位置，例如文字插入點的位置。

## <a name="acquiring-text-range-objects"></a>取得文字範圍物件

用戶端應用程式會使用 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 介面的屬性和方法，取得文字範圍物件。 [**IUIAutomationTextRangePattern：:D ocumentrange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange)屬性會抓取表示以文字為基礎之控制項之整個文字內容的文字範圍，而其他方法則會取得代表部分內容的文字範圍，例如選取的文字、可見的文字，或內嵌在文字中的物件。

[**IUIAutomationTextRangePattern：： GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges)和 [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection)方法可以取出文字範圍物件的陣列。 如果控制項以重迭的視窗或其他物件部分遮蔽， **GetVisibleRanges** 會傳回陣列，其中包含每個部分可見文字行的文字範圍物件。 同樣地，如果以文字為基礎的控制項支援選取多個不連續的文字範圍， **GetSelection** 會傳回陣列，其中包含每個所選範圍的文字範圍物件。

[**IUIAutomationTextRangePattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)方法可讓用戶端應用程式取出內嵌于文字內容中之物件的文字範圍。 用戶端會指定内嵌物件的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面指標（例如影像、資料表或超連結），而且方法會傳回包含物件的文字範圍。 但是，如果内嵌物件沒有相關聯的文字，則方法會傳回一個退化文字範圍。

用戶端應用程式可以使用 [**IUIAutomationTextRangePattern：： RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) 方法，以取得最接近指定螢幕座標的可見文字或内嵌物件的文字範圍。

## <a name="selecting-text-in-a-text-range"></a>選取文字範圍中的文字

[**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)介面包含一些方法，可讓用戶端應用程式控制以文字為基礎之控制項中的文字選取範圍。

用戶端應用程式可以使用 [**IUIAutomationTextRange：： select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) 方法來選取對應至文字範圍的文字，以及從文字控制項移除先前的選取專案（如果有的話）。 使用退化文字範圍呼叫 **Select** ，會將插入點移至文字範圍的位置，而不會選取任何文字。

如果控制項支援選取多個不連續的文字範圍，用戶端可以使用 [**IUIAutomationTextRange：： AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) 和 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) 方法，將文字範圍加入至所選文字範圍的集合，並將其從集合中移除。 如果控制項一次只支援一個選取的文字範圍，但是選取作業會導致選取多個不連續的文字範圍，則方法會傳回 **電子 \_ INVALIDOPERATION** 錯誤，或擴充或截斷目前的選取範圍。 用戶端應用程式可以檢查 [**IUIAutomationTextPattern：： SupportedTextSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection) 屬性，以探索控制項是否支援選取單一或多個文字範圍，或完全無。

如果以文字為基礎的控制項支援文字插入，則在控制項中的退化文字範圍上呼叫 [**IUIAutomationTextRange：： AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) 或 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) 會移動插入點，但不會選取任何文字。

## <a name="retrieving-text-from-a-text-range"></a>從文字範圍中取出文字

用戶端應用程式可以使用 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) 方法來取出文字範圍的純文字。 純文字包含在來源文字中找到的所有控制字元，例如，換行字元和 Unicode 從左至右的標記 (LRM) 。 純文字不包含任何可能存在於來源文字中的標記標記，例如 HTML。 此外，來源文字中的任何轉義碼都會轉換成純文字對應專案。 例如，" &nbsp; " 會轉換成簡單的空白字元。

如果內嵌的物件跨越某個範圍的文字，則純文字會包含物件的內部文字，但不會包含 (内嵌物件之 [名稱] 屬性) 的替代文字。 如需詳細資訊，請參閱 [消費者介面自動化如何公開内嵌物件](uiauto-textpattern-and-embedded-objects-overview.md)。

[**IUIAutomationTextRange：： FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext)方法會搜尋特定字串的文字範圍，如果找到的話，則會傳回包含字串的新文字範圍。

## <a name="retrieving-text-attributes-from-a-text-range"></a>從文字範圍中取出文字屬性

Text 屬性會決定文字型控制項中文字的格式化樣式，並包含前景色彩、專案符號樣式、字型大小等專案。 消費者介面自動化支援一些 text 屬性，並為每個支援的屬性定義識別碼。 用戶端應用程式可以在 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法的呼叫中指定屬性識別碼，以及接收屬性值的 [**變異**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構指標，藉以查詢特定文字屬性值的文字範圍。 如需消費者介面自動化支援的每個 text 屬性的詳細資訊，請參閱 [文字屬性識別碼](uiauto-textattribute-ids.md)。

[**GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)抓取的值代表整個文字範圍內的屬性值。 如果範圍內的所有文字都共用指定之屬性的相同值，則 **GetAttributeValue** 會傳回該值。 但是，如果屬性值在整個文字範圍中不同， **GetAttributeValue** 會將 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標傳回給名為 **ReservedMixedAttribute** 物件的靜態權杖物件。 若要探索屬性值是否會在文字範圍內改變，用戶端應用程式應將 **GetAttributeValue** 的結果與從 [**IUIAutomation：： ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue)屬性抓取的 **ReservedMixedAttribute** 物件進行比較。

不需要以文字為基礎的控制項，就能支援所有消費者介面自動化的 text 屬性。 如果用戶端呼叫 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法，並傳遞不支援屬性的識別碼，則方法會將 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標傳回給稱為 **ReservedNotSupported** 物件的靜態權杖物件。 若要探索是否支援特定屬性，用戶端應用程式應將 **GetAttributeValue** 的結果與從 [**IUIAutomation：： ReservedNotSupportedValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue)屬性抓取的 **ReservedNotSupported** 物件進行比較。

用戶端應用程式可以使用 [**IUIAutomationTextRange：： FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) 方法，在文字範圍中搜尋具有特定文字屬性的文字。 如果找到，則方法會傳回包含相符文字的新文字範圍。 請注意，即使沒有顯示文字， **FindAttribute** 也會傳回相符文字的文字範圍。

## <a name="retrieving-embedded-objects-from-a-text-range"></a>從文字範圍中取出内嵌物件

文字範圍可以包含内嵌物件，例如資料表、影像、超連結等等。 用戶端應用程式可以藉由呼叫 [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 方法，來取得範圍中所有内嵌物件的集合。 與範圍重迭但未完全括住的内嵌物件也會包含在集合中。 如果範圍未包含任何内嵌物件， **GetChildren** 會抓取空集合。

雖然它相依于以文字為基礎之控制項的提供者，但 [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 方法通常不會傳回任何內嵌元素的子系。 例如，如果文字範圍包含的資料表具有多個子儲存格，則 **GetChildren** 方法通常只會傳回 table 元素而非資料格元素。

基於效能或架構原因， [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 可能無法針對文字範圍中的所有内嵌物件取得 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件。 相反地，提供者可能會傳回包含虛擬化專案的集合。 如需詳細資訊，請參閱 [使用虛擬化專案](uiauto-workingwithvirtualizeditems.md)。

## <a name="manipulating-a-text-range"></a>操作文字範圍

[**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)介面提供數種方法，可在以文字為基礎的控制項中操作和導覽文字範圍。 [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)、 [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)和 [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)方法會依據指定的文字單位（例如字元、字、段落等等）移動文字範圍或其中一個端點。 如需詳細資訊，請參閱 [消費者介面自動化文字單位](/windows/desktop/WinAuto/uiauto-uiautomationtextunits)。

雖然 [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) 方法的名稱不一定要展開文字範圍。 相反地，它會藉由移動端點來「正規化」文字範圍，讓範圍完全包含指定的文字單位。 如果範圍小於指定的單位，則範圍會展開，如果超過指定的單位，則會縮短。 下圖顯示 **ExpandToEnclosingUnit** 如何藉由移動範圍的端點，將文字範圍標準化。

![顯示呼叫 expandtoenclosingunit 前後端點位置的圖表](images/expandtoenclosingunit.jpg)

如果文字範圍是從文字單位的開頭開始，而且在下一個文字單位界限的開頭或之前結束，則結束端點會移至下一個文字單位界限 (請參閱上圖中的1和 2) 。

如果文字範圍是從文字單位的開頭開始，並在下一個單位界限結束或之後結束，則結束端點會維持或移至下一個單元界限之後的起點 (請參閱上圖中的3和 4) 。 如果開始與結束端點之間有多個文字單位界限，結束端點就會向後移至起始端點之後的下一個單位界限，而產生長度為一個文字單位的文字範圍。

如果文字範圍是從文字單位的中間開始，則起始端點會往回移至文字單元的開頭，而結束端點則會視需要向後移或往後移動至起始端點之後的下一個單位界限 (在上圖中看到5到8的) 。

呼叫 [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) 方法時，提供者會根據指定的文字單位來將文字範圍標準化。 然後，提供者會將範圍向後或向前移動指定的文字單位數目。 移動範圍時，提供者會忽略文字中任何内嵌物件的界限。  (不過，單位界限本身可能會受到内嵌物件) 的影響。 下圖將示範 **Move** 方法如何在内嵌物件和文字單位界限之間移動文字範圍（單位為單位）。

![顯示移動方法如何跨物件和文字單位界限移動端點範圍的圖表](images/move.jpg)

[**IUIAutomationTextRange：： MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)方法會依指定的文字單位，向前或向後移動其中一個端點。 下圖顯示端點如何向前移動。

![顯示 moveendpointbyunit 如何移動範圍端點的圖表](images/moveendpointbyunit.gif)

[**IUIAutomationTextRange：： MoveEndpointByRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange)方法可讓用戶端應用程式將文字範圍的一個端點設定為與第二個文字範圍之指定端點相同的位置。

## <a name="scrolling-a-text-range-into-view"></a>將文字範圍滾動至視野

[**IUIAutomationTextRange：： ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview)方法會滾動文字範圍，讓文字可以顯示在以文字為基礎之控制項的視口中。 當呼叫 **ScrollIntoView** 時，用戶端可以指定文字是否應該與區首或底部對齊。

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>取出文字範圍的封閉元素

用戶端應用程式可以使用 [**IUIAutomationTextRange：： GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) 方法，來抓取括住文字範圍之最內層元素的 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面指標。 封閉元素通常是提供文字範圍的文字提供者。 但是，如果文字提供者支援子項目（例如資料表或超連結），封入專案可以是文字提供者的子系。

## <a name="comparing-and-cloning-text-ranges"></a>比較和複製文字範圍

[**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)介面包含兩種比較文字範圍的方法。 [**IUIAutomationTextRange：： Compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints)方法會比較兩個文字範圍的開始與結束端點，如果兩個端點相同，則傳回 **TRUE** 。 **IUIAutomationTextRange：： CompareEndpoints** 方法會比較兩個範圍的開始或結束端點。 如果端點相同，則傳回值為零，或是指出兩個端點之相對位置的正值或負數值。

用戶端應用程式可以使用 [**IUIAutomationTextRange：： Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) 方法來建立完整的文字範圍複本。 新的文字範圍可以與原始文字範圍分開操作。

## <a name="retrieving-annotations"></a>正在抓取注釋

文字範圍可包含批註（如果以文字為基礎的控制項支援的話）。 有許多不同類型的批註。 Uiautomationclient.dll 標頭檔會定義一組命名的常數值，以識別消費者介面自動化支援的批註類型。 如需詳細資訊，請參閱 [**批註類型識別碼**](uiauto-annotation-type-identifiers.md)。

某些類型的注釋是以支援 [Annotation](uiauto-implementingannotation.md) 控制項模式 ([**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) 介面) 的 automation 元素表示。 其他類型的注釋會透過 [TextRange](uiauto-about-text-and-textrange-patterns.md) 控制項模式公開。 例如，提供者可能會藉由讓 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)方法傳回 [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)的 [**AnnotationTypes**](uiauto-textattribute-ids.md) text 屬性，以及 [**AnnotationObjects**](uiauto-textattribute-ids.md) text 屬性的 null 值，來公開簡單的拼寫錯誤指標。

### <a name="retrieving-annotations-types-from-a-text-range"></a>從文字範圍中取出批註類型

您可以使用 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法，來取得文字範圍中出現的批註類型清單。 當呼叫方法時，請指定 [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) 的文字屬性識別碼和 [**變數**](/windows/win32/api/oaidl/ns-oaidl-variant)型別的指標。 當方法傳回時， **VARIANT** 參數會包含批註類型識別碼的清單，這是文字範圍中每一個批註類型的清單。 如需詳細資訊，請參閱 [**批註類型識別碼**](uiauto-annotation-type-identifiers.md)。

### <a name="retrieving-all-annotations-from-a-text-range"></a>從文字範圍中取出所有批註

若要從文字範圍中取出批註，請呼叫 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法，並指定 [**UIA \_ ANNOTATIONOBJECTSATTRIBUTEID**](uiauto-textattribute-ids.md) 的文字屬性識別碼和類型 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)的參數指標。 當方法傳回時， **VARIANT** 參數會包含代表 automation 元素陣列的 [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) 介面，文字範圍中的每個批註各一個。 [**IUIAutomationElementArray：： Length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length)屬性指出陣列中的元素數目，而 [**IUIAutomationElementArray：： GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement)方法會抓取特定元素的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)介面。

### <a name="retrieving-information-about-a-particular-annotation"></a>抓取特定注釋的相關資訊

若要抓取特定批註的相關資訊，請先依照上一節所述，取得 annotation 元素的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面。 接下來，藉由呼叫 [**IUIAutomationElement：： GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)方法和 [**UIA \_ AnnotationPatternId**](uiauto-controlpattern-ids.md)的控制項模式識別碼、IID IUIAutomationAnnotationPattern 的介面識別碼 [](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) \_ ，以及接收批註之 **IUIAutomationAnnotation** 指標的變數位址，來取得注釋的 IUIAutomationAnnotationPattern 介面。 查詢 **IUIAutomationAnnotation** 介面的屬性，以抓取注釋型別名稱和類型識別碼、注釋作者的名稱、批註的日期和時間，以及要標注之元素的 **IUIAutomationElement** 介面。

### <a name="retrieving-the-annotation-target-text"></a>正在抓取注釋目標文字

批註通常會套用至文字範圍中某個文字的子集。 在您取得批註的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面之後，您可以將介面傳遞至 [**IUIAutomationTextRange2：： RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) 方法，以抓取包含批註目標文字的文字範圍。

## <a name="retrieving-visual-styles"></a>正在抓取視覺化樣式

提供者會實 [樣式](/windows/desktop/WinAuto/uiauto-implementingstyles) 控制項模式來描述具有特定樣式、填滿色彩、填滿模式或圖形的 UI 元素。 這在描述檔中的專案時特別有用，因為這類樣式經常會有這類樣式。 像這樣的樣式通常會攜帶適用于殘障客戶的資訊;例如，樣式可以將特定字串描述為檔的標題，或是將特定流程圖物件描述為鑽石或圓形。

您可以使用 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法來抓取文字範圍中所使用之視覺化樣式的名稱和識別碼。 您可以使用 [**UIA \_ StyleNameAttributeId**](uiauto-textattribute-ids.md) text 屬性來取得樣式名稱，並使用 [**UIA \_ StyleIdAttributeId**](uiauto-textattribute-ids.md) 來取得樣式識別碼。

支援視覺效果樣式的文字型控制項可以執行 [樣式](/windows/desktop/WinAuto/uiauto-implementingstyles) 控制項模式，讓用戶端存取控制項所使用之視覺化樣式的相關資訊。 用戶端會透過 [**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) 介面存取樣式控制項模式。 您可以藉由呼叫 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 或 [**GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) 方法來取得這個介面，並指定 [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) 做為控制項模式識別碼。

[**IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern)介面包含屬性和方法，可提供視覺化樣式的下列資訊：

-   視覺化樣式的名稱，例如「一般」或「標題1」。
-   視覺化樣式的識別碼。 如需詳細資訊，請參閱 [**樣式識別碼**](uiauto-style-identifiers.md)。
-   用來填滿以文字為基礎之控制項的色彩。
-   用來填滿以文字為基礎之控制項的模式色彩。
-   以文字為基礎之控制項的圖形。
-   擴充屬性;也就是控制項特定樣式名稱和值的清單。

## <a name="invoking-context-menus-from-text-ranges"></a>從文字範圍叫用內容功能表

從 Windows 8.1 開始，文字範圍可能會支援 [**IUIAutomationTextRange2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2)介面。 此介面支援 [**ShowCoNtextMenu**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) 方法。 您可以呼叫這個方法來叫用任何與文字範圍相關聯的內容功能表。 這種情況的案例是文字範圍或 IME 候選選取專案的自動校正。 在這些情況下，會出現支援使用者互動的內容功能表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Text 和 TextRange 控制項模式](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
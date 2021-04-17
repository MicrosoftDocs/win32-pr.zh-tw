---
title: Text 和 TextRange 控制項模式
description: 描述用於執行 ITextProvider、ITextProvider2 和 ITextRangeProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 4d541c31-11f7-4d7e-a0e0-9ed1da873d07
keywords:
- 消費者介面自動化，執行文字控制項模式
- 消費者介面自動化，執行 TextRange 控制項模式
- 消費者介面自動化，文字控制項模式
- 消費者介面自動化，TextRange 控制項模式
- 消費者介面自動化、ITextProvider
- 消費者介面自動化、ITextRangeProvider
- ITextProvider
- ITextRangeProvider
- 實消費者介面自動化的文字控制項模式
- 執行消費者介面自動化 TextRange 控制項模式
- 文字控制項模式
- TextRange 控制項模式
- 控制項模式，ITextProvider
- 控制項模式，ITextRangeProvider
- 控制項模式，執行消費者介面自動化文字
- 控制項模式，執行消費者介面自動化 TextRange
- 控制項模式、文字
- 控制項模式、TextRange
- 介面，ITextProvider
- 介面，ITextRangeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53429dc8ec137a83b6a40db377b5c84aeb36120
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559055"
---
# <a name="text-and-textrange-control-patterns"></a>Text 和 TextRange 控制項模式

描述用於執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)、 [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)和 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)的方針和慣例，包括屬性和方法的相關資訊。 **文字** 控制項模式可讓應用程式和控制項公開簡單的文字物件模型，讓用戶端可以從以文字為基礎的控制項取出文字內容、文字屬性和内嵌物件。

為了支援 **文字** 控制項模式，控制項會執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 和 [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) 介面。 應該支援 **文字** 控制項模式的控制項類型包括 [編輯](uiauto-supporteditcontroltype.md) 和 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型，以及任何其他可讓使用者輸入文字或選取唯讀文字的控制項類型。

**文字** 控制項模式可以與其他 Microsoft 消費者介面自動化控制項模式搭配使用，以支援文字中的數種類型的内嵌物件，包括資料表、超連結和命令按鈕。

[**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)和 [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2)介面包含一些用來取得文字範圍的方法。 *文字範圍* 是一種物件，代表文字容器中連續的文字範圍（或多個不連續的文字範圍）。 其中一個 **ITextProvider** 方法會取得代表整份檔的文字範圍，而有些則會取得代表檔某部分的文字範圍，例如選取的文字、可見的文字或內嵌于文字中的物件。

文字範圍物件是透過 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面所實作為的 **TextRange** 控制項模式來表示。 **TextRange** 控制項模式提供了方法和屬性，可用來公開範圍內文字的相關資訊、移動範圍的端點、選取或取消選取文字、將範圍滾動到視野等等。

如需 **Text** 和 **TextRange** 控制項模式的詳細資訊，請參閱 [消費者介面自動化文字內容支援](uiauto-ui-automation-textpattern-overview.md)。

從 Windows 8.1 提供者開始可以執行 [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) 介面。 這可讓您叫用與文字範圍相關聯的內容功能表。 這可支援文字自動校正或輸入法編輯器等案例 (IME) 候選項目選取專案。

本主題包含下列各節。

-   [實作方針和慣例](#implementation-guidelines-and-conventions)
-   [**ITextProvider** 的必要成員](#required-members-for-itextprovider)
-   [**ITextRangeProvider** 的必要成員](#required-members-for-itextrangeprovider)
-   [支援文字範圍](#supporting-text-ranges)
    -   [依文字單位操作文字範圍](#manipulating-a-text-range-by-text-unit)
    -   [選取文字範圍中的文字](#selecting-text-in-a-text-range)
    -   [從文字範圍取得文字](#acquiring-text-from-a-text-range)
    -   [執行 ShowCoNtextMenu](#implementing-showcontextmenu)
-   [與系統插入點的互通性](#interoperability-with-the-system-caret)
-   [相關主題](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>實作方針和慣例

在執行 **文字** 控制項模式時，請注意下列方針和慣例：

-   任何可存取文字 (例如輸入文字或選取唯讀文字) 的控制項都應該支援 **文字** 控制項模式。
-   **文字** 控制項模式可以與任何呈現文字的 UI 元素搭配使用，甚至是標準按鈕控制項上的靜態標籤。 但是，無法選取或沒有插入點的靜態文字控制項則不需要它。
-   為了確保文字可以完全存取，執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 的控制項也應該支援 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 介面。 **IValueProvider** 可提供程式設計方式來變更文字，以補充 **ITextProvider** 。 它也提供與輔助技術用戶端應用程式更高的相容性，包括以舊版技術（例如 Microsoft Active Accessibility）為基礎的應用程式。 當兩個控制項模式都執行時 **，TextChanged** 事件 ([**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)) 和 **AutomationPropertyChanged** event ([**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md)) 等同于 **Value** 屬性 ([**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md)) 。 必須同時支援這兩個事件。
-   **文字** 控制項模式僅支援一個文字資料流程和一個控制項的一個區。 如果應用程式在窗格中提供多個檔的視圖，每個 view (控制項) 應該獨立支援 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 。
-   [**ITextProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)方法可能會傳回單一文字範圍，代表目前選取的文字。 如果控制項支援選取多個非連續的文字範圍， **GetSelection** 方法應該會傳回陣列，其中包含每個所選文字範圍的一個 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 介面。
-   **文字** 控制項模式將插入點表示為退化 (空白) 文字範圍。 當插入點存在且未選取任何文字時， [**ITextProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) 方法應該會傳回退化文字範圍。 如需詳細資訊，請參閱 [與系統插入號的互通性](#interoperability-with-the-system-caret)。
-   [**ITextProvider：： GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)方法可能會在區域中看到連續的文字範圍時傳回單一文字範圍，或者，它可能會傳回不相鄰文字範圍的陣列，代表多個部分可見的文字行。
-   如果子項目未包含任何文字， [**ITextProvider：： RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) 方法應該會傳回一個退化範圍。 因為内嵌物件可以包含文字，所以 **RangeFromChild** 方法不一定會傳回退化文字範圍。 如需詳細資訊，請參閱 [消費者介面自動化如何公開内嵌物件](uiauto-textpattern-and-embedded-objects-overview.md)。
-   [**ITextProvider：： RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)方法會使用指定的螢幕座標，在檔區域中執行點擊測試。 產生的文字範圍應該與插入點或選取專案一致，因為在指定的螢幕座標上按一下位置會產生此結果。 例如，如果影像位於指定的螢幕座標，則產生的文字範圍應該與 [**ITextProvider：： RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) 方法為影像取得的文字範圍相同。 同樣地，如果用戶端應用程式要求系統插入點中央位置的文字範圍 (插入點) ，則產生的文字範圍應該與系統插入點位置相同。
-   [**ITextProvider：:D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)屬性應該一律提供文字範圍，其中包含對應的 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)執行所支援的所有文字。
-   [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)事件必須在任何文字變更發生之後引發，即使在隱藏區中看不到變更。 例如，提供者應該引發事件，即使使用者在選取的文字上貼上完全相同的文字也是一樣。
-   [**UIA \_ 文字 \_ TextSelectionChangedEventId**](uiauto-event-ids.md)必須在選取文字變更時引發，或每次插入點 (插入點) 在文字之間移動時引發。

在執行 **TextRange** 控制項模式時，請注意下列方針和慣例：

-   **TextRange** 控制項模式的所有方法都應該執行文字作業，不論文字的可見度狀態為何。 您可以藉由查詢 **IsHidden** text 屬性 ([**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)) 來判斷文字範圍的可見度。
-   如果可能，提供者應該確保任何文字變更（例如刪除、插入和移動）都會反映在相關聯的文字範圍物件中， ([**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 介面的實例) 並引發 [**UIA 的 \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md) 事件。 用戶端可以使用事件做為提示來確認編輯控制項文字的編輯變更。
-   [**ITextRangeProvider：： Compare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)、 [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)和 [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)方法所使用的所有文字範圍物件都必須是相同的 **文字** 控制項模式執行的對等。
-   雖然並非必要，但 [**ITextRangeProvider：： CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)方法所抓取的 *pRetVal* 值可以指出兩個端點之間的距離（以字元為單位 ([**TextUnit \_ 字元**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)) ）。 不過，用戶端應用程式不應該依賴 *pRetVal* 的精確度，而不是其正值或負數值。
-   [**ITextRangeProvider：： ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)、 [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)和 [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)方法需要仔細考慮指定的文字單位。 如需詳細資訊，請參閱依文字單位操作 TextRange。
-   如需與 [**ITextRangeProvider：： Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)、 [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)和 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) 方法相關的實作需求，請參閱選取文字範圍中的文字。
-   [**ITextRangeProvider：： FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)和 [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)方法會針對單一相符的文字字串或文字屬性向前或向後搜尋。 如果找不到相符項，則應該傳回 **Null** 。
-   如果相關聯的屬性在範圍內，或是文字控制項不支援屬性，則 [**ITextRangeProvider：： GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) 方法必須傳回從 [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) 或 [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue) 函數取得的位址。 **TextRange** 控制項模式規格不允許加入新的文字屬性識別碼或變更現有屬性的定義方式。
-   可能的話， [**ITextRangeProvider：： GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) 方法應該會傳回陣列，其中包含文字範圍中每一個完整或部分可見的文字行的周框。 如果無法這麼做，則提供者可以傳回陣列，其中包含只有全可見行的周框矩形;不過，這會限制用戶端應用程式能夠準確描述螢幕上文字的呈現方式。
-   [**ITextRangeProvider：： GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)方法應該會傳回內嵌于文字範圍中的所有子項目，但不需要傳回子項目的任何子系。 例如，如果文字範圍包含的資料表具有多個子儲存格，則 **GetChildren** 方法可能只會傳回 table 元素，而不會傳回資料格元素。 基於效能或架構原因，提供者可能無法公開自動化樹狀結構中的檔所裝載的所有内嵌物件。 在此情況下，提供者至少應該支援透過 **GetChildren** 方法來列舉子物件，而在選項中，則是支援解除虛擬化支援的 [VirtualizedItem](uiauto-implementingvirtualizeditem.md) 控制項模式。
-   [**ITextRangeProvider：： GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)方法通常會傳回提供文字範圍的文字提供者。 但是，如果文字提供者支援子物件（例如資料表或超連結），封入專案可以是文字提供者的子代。 **GetEnclosingElement** 所傳回的元素應該是最接近指定文字範圍的專案。 例如，如果文字範圍是在資料表的資料格中， **GetEnclosingElement** 應該會傳回包含資料格，而不是 table 元素。
-   [**ITextRangeProvider：： GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)方法應該會傳回範圍中的純文字。 如需詳細資訊，請參閱從文字範圍取得文字。
-   呼叫 [**ITextRangeProvider：： ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview) 應該將文字控制項的視口中的文字對齊，如 *alignToTop* 參數所指定。 雖然水準對齊沒有任何需求，但是文字範圍應該會以水準和垂直方式顯示。 評估 *alignToTop* 參數時，提供者必須考慮文字控制項的方向和文字的流程方向。 例如，如果 *alignToTop* 為 **TRUE** ，代表包含由右至左流動之文字的垂直方向文字控制項，則提供者應該將文字範圍對齊至區域的右側。
-   當您透過 [**TextUnit \_ 線**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)移動檔時，如果文字範圍輸入了內嵌的表格，則資料格中的每一行文字都應該視為線條。

## <a name="required-members-for-itextprovider"></a>**ITextProvider** 的必要成員

執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 介面需要下列屬性和方法。



| 必要成員                                                                                        | 成員類型 | 備註 |
|---------------------------------------------------------------------------------------------------------|-------------|-------|
| [**DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange)                                             | 屬性    | 無  |
| [**SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)                           | 屬性    | 無  |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection)                                               | 方法      | 無  |
| [**GetVisibleRanges**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getvisibleranges)                                       | 方法      | 無  |
| [**RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)                                           | 方法      | 無  |
| [**RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint)                                           | 方法      | 無  |
| [**UIA \_ 文字 \_ TextChangedEventId**](uiauto-event-ids.md)                   | 事件       | 無  |
| [**UIA \_ 文字 \_ TextSelectionChangedEventId**](uiauto-event-ids.md) | 事件       | 無  |



 

執行 [**ITextProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2) 介面需要下列其他屬性和方法。



| 必要成員                                                         | 成員類型 | 備註 |
|--------------------------------------------------------------------------|-------------|-------|
| [**GetCaretRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange)         | 方法      | 無  |
| [**RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) | 方法      | 無  |



 

## <a name="required-members-for-itextrangeprovider"></a>**ITextRangeProvider** 的必要成員

執行 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 介面需要下列屬性和方法。



| 必要成員                                                                 | 成員類型 | 備註 |
|----------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection)               | 方法      | 無  |
| [**克隆**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-clone)                                 | 方法      | 無  |
| [**比較**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compare)                             | 方法      | 無  |
| [**CompareEndpoints**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-compareendpoints)           | 方法      | 無  |
| [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) | 方法      | 無  |
| [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)                 | 方法      | 無  |
| [**FindText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findtext)                           | 方法      | 無  |
| [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)         | 方法      | 無  |
| [**GetBoundingRectangles**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getboundingrectangles) | 方法      | 無  |
| [**GetChildren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren)                     | 方法      | 無  |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getenclosingelement)     | 方法      | 無  |
| [**GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)                             | 方法      | 無  |
| [**移動**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)                                   | 方法      | 無  |
| [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)       | 方法      | 無  |
| [**MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)     | 方法      | 無  |
| [**選擇**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)                               | 方法      | 無  |
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-scrollintoview)               | 方法      | 無  |



 

執行 [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) 介面需要下列其他屬性和方法。



| 必要成員                                                      | 成員類型 | 備註                                      |
|-----------------------------------------------------------------------|-------------|--------------------------------------------|
| [**ShowContextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) | 方法      | 請參閱「執行 ShowCoNtextMenu」一節 |



 

**TextRange** 控制項模式沒有相關聯的事件。

## <a name="supporting-text-ranges"></a>支援文字範圍

本節說明提供者如何執行 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 和 [**ITextRangeProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider2) 介面的各種方法，以支援 **TextRange** 控制項模式。

### <a name="manipulating-a-text-range-by-text-unit"></a>依文字單位操作文字範圍

[**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面提供數種方法，可在以文字為基礎的控制項中操作和導覽文字範圍。 [**ITextRangeProvider：： Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)、 [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)和 [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)方法會依據指定的文字單位（例如字元、字、段落等等）移動文字範圍或其中一個端點。 如需詳細資訊，請參閱 [消費者介面自動化文字單位](/windows/desktop/WinAuto/uiauto-uiautomationtextunits)。

不論其名稱為何， [**ITextRangeProvider：： ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) 方法都不一定會展開文字範圍。 相反地，它會藉由移動端點來「標準化」文字範圍，使範圍包含指定的文字單位。 如果範圍小於指定的單位，則範圍會展開，如果超過指定的單位，則會縮短。 **ExpandToEnclosingUnit** 方法一定要以一致的方式來正規化文字範圍是很重要的。否則，文字範圍操作的其他方面將無法預期。 下圖顯示 **ExpandToEnclosingUnit** 如何藉由移動範圍的端點，將文字範圍標準化。

![顯示呼叫 expandtoenclosingunit 前後文字範圍端點位置的圖表](images/expandtoenclosingunit.jpg)

如果文字範圍是從文字單位的開頭開始，而且在下一個文字單位界限的開頭或之前結束，則結束端點會移至下一個文字單位界限， (在上圖中看到1和 2) 。

如果文字範圍是從文字單位的開頭開始，並在下一個單位界限結束或之後結束，則結束端點會維持或移至下一個單元界限之後的起點 (請參閱上圖中的3和 4) 。 如果開始與結束端點之間有多個文字單位界限，結束端點就會向後移至起始端點之後的下一個單位界限，而產生長度為一個文字單位的文字範圍。

如果文字範圍是從文字單位的中間開始，則起始端點會往回移至文字單元的開頭，而結束端點則會視需要向後移或往後移動至起始端點之後的下一個單位界限 (在上圖中看到5到8的) 。

呼叫 [**ITextRangeProvider：： Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move) 方法時，提供者會使用與 [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit) 方法相同的正規化邏輯，以指定的文字單位來將文字範圍標準化。 然後，提供者會將範圍向後或向前移動指定的文字單位數目。 移動範圍時，提供者應該忽略文字中任何内嵌物件的界限。  (不過，單位界限本身可能會受到内嵌物件) 的影響。 下圖將示範 **Move** 方法如何在内嵌物件和文字單位界限之間移動文字範圍（單位為單位）。

![顯示移動方法如何跨物件和文字單位界限移動端點範圍的圖表](images/move.jpg)

[**ITextRangeProvider：： MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)方法會依指定的文字單位，向前或向後移動其中一個端點，如下圖所示。

![顯示 moveendpointbyunit 如何移動範圍端點的圖表](images/moveendpointbyunit.gif)

[**ITextRangeProvider：： MoveEndpointByRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyrange)方法可讓用戶端應用程式將文字範圍的一個端點設定為與第二個文字範圍之指定端點相同的位置。

### <a name="selecting-text-in-a-text-range"></a>選取文字範圍中的文字

[**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面包含數個方法，可控制以文字為基礎之控制項中的文字選取範圍。

[**ITextRangeProvider：： Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select)方法應該選取對應至文字範圍的文字，並從文字控制項移除先前的選取專案（如果有的話）。 如果在退化文字範圍上呼叫 **Select** ，則提供者應該將插入點移至文字範圍的位置，而不需要選取任何文字。

如果控制項支援選取多個不連續的文字範圍， [**ITextRangeProvider：： AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) 和 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) 方法會將文字範圍加入至所選文字範圍的集合，並將其從集合中移除。 如果控制項一次只支援一個選取的文字範圍，但是選取作業會導致選取多個不連續的文字範圍，則提供者應該傳回 **電子 \_ INVALIDOPERATION** 錯誤，或是延伸或截斷目前的選取範圍。 [**ITextProvider：： SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection)屬性應該指出控制項是否支援選取單一或多個文字範圍，或完全無。

如果以文字為基礎的控制項支援文字插入，則在控制項中的退化文字範圍上呼叫 [**ITextRangeProvider：： AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-addtoselection) 或 [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-removefromselection) 應移動插入點，但不應選取任何文字。

### <a name="acquiring-text-from-a-text-range"></a>從文字範圍取得文字

[**ITextRangeProvider：： GetText**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-gettext)方法應該會傳回文字範圍的純文字。 純文字應該包含在來源文字中找到的所有控制字元，例如，換行字元和 Unicode 從左至右的標記 (LRM) 。 純文字不應包含任何標記標記，例如可能存在於來源文字中的 HTML。 此外，來源文字中的任何轉義碼都應轉換成純文字對等專案。 例如，" &nbsp; " 應該轉換成簡單的空白字元。

如果内嵌物件跨越某個範圍的文字，則純文字應該包含物件的內部文字，而不是內嵌) 物件的 [名稱] 屬性 (替代文字，因為它可能與描述性的內部文字不一致。 如需詳細資訊，請參閱 [消費者介面自動化如何公開内嵌物件](uiauto-textpattern-and-embedded-objects-overview.md)。

### <a name="implementing-showcontextmenu"></a>執行 ShowCoNtextMenu

[**ITextRangeProvider2：： ShowCoNtextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) 應該一律在範圍的起點點顯示內容功能表。 這應該相當於使用者按下內容功能表鍵或 SHIFT + F10 與範圍開頭的插入點時所發生的情況。

如果顯示操作功能表通常會導致插入點移動到指定的位置，則它應該這麼做，以程式設計方式叫用 [**ShowCoNtextMenu**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider2-showcontextmenu) 來消費者介面自動化支援。

## <a name="interoperability-with-the-system-caret"></a>與系統插入點的互通性

正確支援插入點對於許多用戶端應用程式都很重要，包括不是以消費者介面自動化為基礎的應用程式。 在 **文字** 控制項模式中，插入點是以 (空白) 文字範圍在系統插入號的位置來表示。 當插入點移動時，控制項應該會引發 **TextSelectionChanged** 事件， ([**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)) 。 某些用戶端應用程式相依于此事件來監視插入點的位置，以及追蹤文字選取範圍。

當控制項包含選取的文字時，目前的 **文字** 控制項模式設計不會提供直接將插入點位置與特定文字範圍產生關聯的方式。 提供者必須追蹤文字選取範圍，並適當地設定插入點的位置。 因為選取文字通常是藉由在按住 SHIFT 或 CTRL 鍵時移動插入點來完成，或兩者都有，所以提供者可以在選取專案變更時，藉由檢查這些按鍵的狀態來追蹤文字選取範圍。

由於協助工具架構會為系統插入號提供內建的支援，但不會針對自訂插入號提供內建支援，因此，以文字為基礎的控制項應該盡可能使用系統插入號。 使用自訂插入號的控制項可讓您建立與自訂插入號相同維度的系統插入號，並將系統插入點放置在控制項 UI 中的相同位置，以做為自訂插入點（也就是插入點），來確保插入號可以存取。 或者，使用自訂插入號的控制項可以執行 [**OBJID \_ 插入**](object-identifiers.md) 號的 Microsoft Active Accessibility 提供者，以直接為您的自訂插入號提供協助工具資訊。

如需系統插入號的詳細資訊，請參閱 [游標](/windows/desktop/menurc/carets)。

若要測試您的控制項是否適當地公開系統插入號的位置，請使用 [檢查](inspect-objects.md) 和 [可存取的事件](accessible-event-watcher.md) 監看員工具。

系統插入號點陣圖中間的螢幕座標應該一律符合插入點的位置。 如此一來，用戶端就可以在 [**ITextProvider：： RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) 的呼叫中使用插入號螢幕座標，以取得可精確表示插入點位置的文字範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)
</dt> <dt>

[Text 控制項類型](uiauto-supporttextcontroltype.md)
</dt> <dt>

[Macos textedit 控制項模式](textedit-control-pattern.md)
</dt> <dt>

[TextChild 控制項模式](textchild-control-pattern.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[UI 自動化樹狀目錄概觀](uiauto-treeoverview.md)
</dt> </dl>

 

 
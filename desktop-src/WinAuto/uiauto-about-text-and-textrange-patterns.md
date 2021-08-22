---
title: 關於 Text 和 TextRange 控制項模式
description: 您可以使用文字控制項模式來公開控制項的文字內容，表示文字容器的內容做為文字資料流程。
ms.assetid: acc2b513-9367-416a-b0d9-3c2bcc14a8a7
keywords:
- 消費者介面自動化，文字內容支援
- 消費者介面自動化，文字模式總覽
- 消費者介面自動化，文字控制項總覽
- 消費者介面自動化，文字控制項模式
- '消費者介面自動化，文字服務架構 (TSF) '
- 消費者介面自動化、TSF
- 消費者介面自動化，效能
- 文字模式，關於
- '文字模式，文字服務架構 (TSF) '
- 文字控制項，關於
- 文字內容，支援
- 文字控制項，效能
- 文字控制項模式
- 控制項模式、文字
- Text Services Framework (TSF)
- 'TSF (文字服務架構) '
- 效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04112e0233db056c5ff3e81b68256229aa45f60cfdb1258e565e10aea1cd43ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052356"
---
# <a name="about-the-text-and-textrange-control-patterns"></a>關於 Text 和 TextRange 控制項模式

您可以使用 [文字](uiauto-implementingtextandtextrange.md) 控制項模式來公開控制項的文字內容，表示文字容器的內容做為文字資料流程。 文字控制項模式必須支援 TextRange 控制項模式，才能公開格式和樣式屬性。 TextRange 控制項模式支援文字控制項模式，其方式是在具有開始和結束端點集合的文字容器中表示連續或多個不連續的文字範圍 (或範圍) 。 TextRange 控制項模式支援選取專案、比較、抓取和遍歷等功能。

> [!Note]  
> [文字](uiauto-implementingtextandtextrange.md)控制項模式不提供插入或修改文字的方法。 不過，根據控制項，這可以使用 Microsoft 消費者介面自動化 [Value](uiauto-implementingvalue.md) 控制項模式或透過直接鍵盤輸入來完成。 另外還有一種 [**macos textedit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) 模式，可支援以程式設計方式變更為文字。

 

本主題所述的功能對輔助技術廠商及其使用者來說非常重要。 輔助技術可以使用消費者介面自動化來收集使用者的完整文字格式資訊，並藉由 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (字元、單字、線條或段落) 來提供以程式設計方式流覽和選取文字。

本主題包含下列幾節：

-   [消費者介面自動化 TextPattern 和文字服務架構](#ui-automation-textpattern-and-the-text-services-framework)
-   [控制項類型](#control-types)
-   [提供者介面](#provider-interfaces)
-   [用戶端介面](#client-interfaces)
-   [效能](#performance)
-   [文字模式和虛擬化内嵌物件](#text-pattern-and-virtualized-embedded-objects)
-   [使用具有文字控制項模式的自訂控制項類型](#using-the-custom-control-type-with-the-text-control-pattern)
-   [文字範圍的存留期](#lifetime-of-a-text-range)
-   [相關主題](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a>消費者介面自動化 TextPattern 和文字服務架構

文字服務架構 (TSF) 是一個簡單且可擴充的系統架構，可在桌面和應用程式中啟用自然語言服務和先進的文字輸入。 除了提供介面讓應用程式公開其文字存放區之外，還支援文字存放區的中繼資料。

TSF 是針對需要將輸入插入內容感知案例的應用程式所設計。 不過， [文字](uiauto-implementingtextandtextrange.md) 控制項模式是唯讀的方案，目的是要為螢幕讀取器和盲文裝置的文字存放區提供優化的存取權。

需要文字存放區之唯讀存取權的可存取技術可以使用文字控制項模式，但需要 TSF 的功能才能進行內容感知輸入。

如需詳細資訊，請參閱 [文字服務架構](/windows/desktop/TSF/text-services-framework)。

## <a name="control-types"></a>控制項類型

消費者介面自動化 [編輯](uiauto-supporteditcontroltype.md) 控制項類型和 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型必須支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式。 為了改善協助工具，Microsoft 建議 [工具提示](uiauto-supporttooltipcontroltype.md) 和文字控制項類型也支援文字控制項模式，但並非必要。

## <a name="provider-interfaces"></a>提供者介面

消費者介面自動化提供者藉由執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)和 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面，支援控制項的 [文字](uiauto-implementingtextandtextrange.md)控制項模式。 這些介面會公開控制項中文字的詳細屬性資訊，並提供強大的導覽功能。

如果控制項缺少任何特定屬性的支援，則提供者不需要支援所有的 text 屬性。

提供者必須支援 [**ITextProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) 和 [**ITextRangeProvider：： Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) 方法（如果控制項支援文字資料指標的文字選取或位置） (或文字區域內的系統插入號) 。 如果控制項不支援這項功能，則不需要支援其中一種方法。 不過，控制項必須藉由實 [**ITextProvider：： SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) 屬性，來公開所支援的文字選取類型。

提供者一律必須支援 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 常數、 **TextUnit \_ 字元** 和 **TextUnit \_ 檔**，以及它能夠支援的其他專案。

> [!Note]  
> 提供者可以跳到下一個最大的單位（依下列順序支援），以略過對特定 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 的支援： **TextUnit \_ Character**、 **TextUnit \_ Format**、 **TextUnit \_ Word**、 **TextUnit \_ Line**、 **TextUnit \_ 段落**、 **TextUnit \_ 頁面** 和 **TextUnit \_ 檔**。

 

## <a name="client-interfaces"></a>用戶端介面

消費者介面自動化用戶端應用程式會使用 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) 介面來存取文字控制項的文字內容。 用戶端會使用 **IUIAutomationTextPattern** 來選取稱為 *文字範圍* 的文字範圍，以及取得範圍的 **IUIAutomationTextRange** 介面指標。 **IUIAutomationTextRange** 介面可讓用戶端操作文字範圍，以及抓取範圍內文字的相關資訊，包括字型名稱、前景色彩、底線樣式等屬性。 如需詳細資訊，請參閱 [文字屬性識別碼](uiauto-textattribute-ids.md)。

## <a name="performance"></a>效能

**文字** 控制項模式依賴跨進程呼叫來處理大部分的功能，因此它不會提供快取機制來改善處理內容時的效能。 您可以使用 [**IUIAutomationElement：： GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) 方法來存取 Microsoft 消費者介面自動化中的其他控制項模式。

改善效能的其中一種技術，是確保消費者介面自動化用戶端使用 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) 方法，嘗試取出適度大小的文字區塊。 例如，使用 **GetText** 抓取單一字元將會產生每個字元的跨進程叫用，而不會在呼叫 **GetText** 時指定最大長度，而會產生一個跨進程叫用，但視文字範圍的大小而定，可能會有高延遲。

## <a name="text-pattern-and-virtualized-embedded-objects"></a>文字模式和虛擬化内嵌物件

如果可能的話， [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 和 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 的提供者必須支援檔的整個文字，包括在視口以外的任何文字。 針對已虛擬化的非螢幕文字或内嵌物件，提供者應該支援 [VirtualizedItem 控制項模式](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)) 。

如果檔是在整個文字資料流程仍然可用的情況下進行虛擬化， [**ITextProvider：:D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) 屬性將會取出包含整份檔的文字範圍。 不過，呼叫 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) 方法將會取得虛擬化物件的集合，這些物件代表檔中的所有内嵌物件。 若要與虛擬化的内嵌物件互動，用戶端必須呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 方法，使專案可完全作為消費者介面自動化專案來存取。 用戶端必須遵循類似的程式來處理內嵌資料表中的方格元素，其中部分資料表是在螢幕上，而虛擬化。

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a>使用具有文字控制項模式的自訂控制項類型

雖然 [文字](uiauto-implementingtextandtextrange.md) 控制項模式支援許多文字屬性和内嵌物件，但無法預先定義所有可能的檔專案和呈現類型。 針對現有的屬性或標準控制項類型不支援的檔專案，提供者可以使用消費者介面自動化 **自訂** 控制項類型所提供的擴充功能。

對於以頁面簡報為基礎的應用程式和使用者介面，「頁面」的界限和版面配置呈現也可以表示為具有自訂控制項類型的内嵌物件， (也就是 `LocalizedControlType="page"`) 。 如此一來，内嵌物件就可以裝載其他無法輕易成為檔文字資料流程一部分的頁面元素，例如，每個頁面的頁首和頁尾欄位，做為「頁面」内嵌物件的子系。 或者，每個「頁面」物件都可以獨立支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，這適用于製作投影片放映簡報或以頁面為基礎的桌面發行環境等應用程式。

## <a name="lifetime-of-a-text-range"></a>文字範圍的存留期

可能的話，提供者應該確保任何文字變更（例如刪除、插入和移動）都會反映在相關聯的文字範圍中。 如果無法更新文字範圍，則提供者應該引發 [**UIA \_ text \_ TextChangedEventId**](uiauto-event-ids.md) 事件，以通知用戶端文字範圍已不再有效，而且必須抓取新的範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[消費者介面自動化如何支援内嵌物件](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[使用以文字為基礎的控制項](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[Text Services Framework (TSF)](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 
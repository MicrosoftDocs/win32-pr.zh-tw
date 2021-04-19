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
ms.openlocfilehash: bb9ff1eb75227454e3e9df6035798a304096a958
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106995571"
---
# <a name="about-the-text-and-textrange-control-patterns"></a><span data-ttu-id="5521d-120">關於 Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="5521d-120">About the Text and TextRange Control Patterns</span></span>

<span data-ttu-id="5521d-121">您可以使用 [文字](uiauto-implementingtextandtextrange.md) 控制項模式來公開控制項的文字內容，表示文字容器的內容做為文字資料流程。</span><span class="sxs-lookup"><span data-stu-id="5521d-121">The textual content of a control is exposed by using the [Text](uiauto-implementingtextandtextrange.md) control pattern, which represents the contents of a text container as a text stream.</span></span> <span data-ttu-id="5521d-122">文字控制項模式必須支援 TextRange 控制項模式，才能公開格式和樣式屬性。</span><span class="sxs-lookup"><span data-stu-id="5521d-122">The Text control pattern requires the support of the TextRange control pattern to expose format and style attributes.</span></span> <span data-ttu-id="5521d-123">TextRange 控制項模式支援文字控制項模式，其方式是在具有開始和結束端點集合的文字容器中表示連續或多個不連續的文字範圍 (或範圍) 。</span><span class="sxs-lookup"><span data-stu-id="5521d-123">The TextRange control pattern supports the Text control pattern by representing contiguous or multiple, disjoint text spans (or ranges) in a text container with a collection of start and end endpoints.</span></span> <span data-ttu-id="5521d-124">TextRange 控制項模式支援選取專案、比較、抓取和遍歷等功能。</span><span class="sxs-lookup"><span data-stu-id="5521d-124">The TextRange control pattern supports functionality such as selection, comparison, retrieval and traversal.</span></span>

> [!Note]  
> <span data-ttu-id="5521d-125">[文字](uiauto-implementingtextandtextrange.md)控制項模式不提供插入或修改文字的方法。</span><span class="sxs-lookup"><span data-stu-id="5521d-125">The [Text](uiauto-implementingtextandtextrange.md) control pattern does not provide a means to insert or modify text.</span></span> <span data-ttu-id="5521d-126">不過，根據控制項，這可以使用 Microsoft 消費者介面自動化 [Value](uiauto-implementingvalue.md) 控制項模式或透過直接鍵盤輸入來完成。</span><span class="sxs-lookup"><span data-stu-id="5521d-126">However, depending on the control, this may be accomplished by using the Microsoft UI Automation [Value](uiauto-implementingvalue.md) control pattern or through direct keyboard input.</span></span> <span data-ttu-id="5521d-127">另外還有一種 [**macos textedit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) 模式，可支援以程式設計方式變更為文字。</span><span class="sxs-lookup"><span data-stu-id="5521d-127">There's also a [**TextEdit**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) pattern that supports programmatic change to text.</span></span>

 

<span data-ttu-id="5521d-128">本主題所述的功能對輔助技術廠商及其使用者來說非常重要。</span><span class="sxs-lookup"><span data-stu-id="5521d-128">The functionality described in this topic is vital to assistive technology vendors and their end users.</span></span> <span data-ttu-id="5521d-129">輔助技術可以使用消費者介面自動化來收集使用者的完整文字格式資訊，並藉由 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (字元、單字、線條或段落) 來提供以程式設計方式流覽和選取文字。</span><span class="sxs-lookup"><span data-stu-id="5521d-129">Assistive technologies can use UI Automation to gather complete text formatting information for the user and provide programmatic navigation and selection of text by [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) (character, word, line, or paragraph).</span></span>

<span data-ttu-id="5521d-130">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="5521d-130">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5521d-131">消費者介面自動化 TextPattern 和文字服務架構</span><span class="sxs-lookup"><span data-stu-id="5521d-131">UI Automation TextPattern and the Text Services Framework</span></span>](#ui-automation-textpattern-and-the-text-services-framework)
-   [<span data-ttu-id="5521d-132">控制項類型</span><span class="sxs-lookup"><span data-stu-id="5521d-132">Control Types</span></span>](#control-types)
-   [<span data-ttu-id="5521d-133">提供者介面</span><span class="sxs-lookup"><span data-stu-id="5521d-133">Provider Interfaces</span></span>](#provider-interfaces)
-   [<span data-ttu-id="5521d-134">用戶端介面</span><span class="sxs-lookup"><span data-stu-id="5521d-134">Client Interfaces</span></span>](#client-interfaces)
-   [<span data-ttu-id="5521d-135">效能</span><span class="sxs-lookup"><span data-stu-id="5521d-135">Performance</span></span>](#performance)
-   [<span data-ttu-id="5521d-136">文字模式和虛擬化内嵌物件</span><span class="sxs-lookup"><span data-stu-id="5521d-136">Text Pattern and Virtualized Embedded Objects</span></span>](#text-pattern-and-virtualized-embedded-objects)
-   [<span data-ttu-id="5521d-137">使用具有文字控制項模式的自訂控制項類型</span><span class="sxs-lookup"><span data-stu-id="5521d-137">Using the Custom Control Type with the Text Control Pattern</span></span>](#using-the-custom-control-type-with-the-text-control-pattern)
-   [<span data-ttu-id="5521d-138">文字範圍的存留期</span><span class="sxs-lookup"><span data-stu-id="5521d-138">Lifetime of a Text Range</span></span>](#lifetime-of-a-text-range)
-   [<span data-ttu-id="5521d-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="5521d-139">Related topics</span></span>](#related-topics)

## <a name="ui-automation-textpattern-and-the-text-services-framework"></a><span data-ttu-id="5521d-140">消費者介面自動化 TextPattern 和文字服務架構</span><span class="sxs-lookup"><span data-stu-id="5521d-140">UI Automation TextPattern and the Text Services Framework</span></span>

<span data-ttu-id="5521d-141">文字服務架構 (TSF) 是一個簡單且可擴充的系統架構，可在桌面和應用程式中啟用自然語言服務和先進的文字輸入。</span><span class="sxs-lookup"><span data-stu-id="5521d-141">Text Services Framework (TSF) is a simple and scalable system framework that enables natural language services and advanced text input on the desktop and in applications.</span></span> <span data-ttu-id="5521d-142">除了提供介面讓應用程式公開其文字存放區之外，還支援文字存放區的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5521d-142">In addition to providing interfaces for applications to expose their text store, it also supports metadata for the text store.</span></span>

<span data-ttu-id="5521d-143">TSF 是針對需要將輸入插入內容感知案例的應用程式所設計。</span><span class="sxs-lookup"><span data-stu-id="5521d-143">TSF was designed for applications that need to inject input into context-aware scenarios.</span></span> <span data-ttu-id="5521d-144">不過， [文字](uiauto-implementingtextandtextrange.md) 控制項模式是唯讀的方案，目的是要為螢幕讀取器和盲文裝置的文字存放區提供優化的存取權。</span><span class="sxs-lookup"><span data-stu-id="5521d-144">The [Text](uiauto-implementingtextandtextrange.md) control pattern, however, is a read-only solution that is intended to provide optimized access to a text store for screen-readers and Braille devices.</span></span>

<span data-ttu-id="5521d-145">需要文字存放區之唯讀存取權的可存取技術可以使用文字控制項模式，但需要 TSF 的功能才能進行內容感知輸入。</span><span class="sxs-lookup"><span data-stu-id="5521d-145">Accessible technologies that require read-only access to a text store can use the Text control pattern, but will need the functionality of TSF for context-aware input.</span></span>

<span data-ttu-id="5521d-146">如需詳細資訊，請參閱 [文字服務架構](/windows/desktop/TSF/text-services-framework)。</span><span class="sxs-lookup"><span data-stu-id="5521d-146">For more information, see [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>

## <a name="control-types"></a><span data-ttu-id="5521d-147">控制項類型</span><span class="sxs-lookup"><span data-stu-id="5521d-147">Control Types</span></span>

<span data-ttu-id="5521d-148">消費者介面自動化 [編輯](uiauto-supporteditcontroltype.md) 控制項類型和 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型必須支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5521d-148">The UI Automation [Edit](uiauto-supporteditcontroltype.md) control type and [Document](uiauto-supportdocumentcontroltype.md) control type must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span> <span data-ttu-id="5521d-149">為了改善協助工具，Microsoft 建議 [工具提示](uiauto-supporttooltipcontroltype.md) 和文字控制項類型也支援文字控制項模式，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="5521d-149">For improved accessibility, Microsoft recommends that the [ToolTip](uiauto-supporttooltipcontroltype.md) and Text control types also support the Text control pattern, but it is not required.</span></span>

## <a name="provider-interfaces"></a><span data-ttu-id="5521d-150">提供者介面</span><span class="sxs-lookup"><span data-stu-id="5521d-150">Provider Interfaces</span></span>

<span data-ttu-id="5521d-151">消費者介面自動化提供者藉由執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)和 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider)介面，支援控制項的 [文字](uiauto-implementingtextandtextrange.md)控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5521d-151">UI Automation providers support the [Text](uiauto-implementingtextandtextrange.md) control pattern for a control by implementing the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) interfaces.</span></span> <span data-ttu-id="5521d-152">這些介面會公開控制項中文字的詳細屬性資訊，並提供強大的導覽功能。</span><span class="sxs-lookup"><span data-stu-id="5521d-152">These interfaces expose detailed attribute information for text in the control and provide robust navigational capabilities.</span></span>

<span data-ttu-id="5521d-153">如果控制項缺少任何特定屬性的支援，則提供者不需要支援所有的 text 屬性。</span><span class="sxs-lookup"><span data-stu-id="5521d-153">A provider does not need to support all text attributes if the control lacks support for any particular attribute.</span></span>

<span data-ttu-id="5521d-154">提供者必須支援 [**ITextProvider：： GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) 和 [**ITextRangeProvider：： Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) 方法（如果控制項支援文字資料指標的文字選取或位置） (或文字區域內的系統插入號) 。</span><span class="sxs-lookup"><span data-stu-id="5521d-154">A provider must support the [**ITextProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-getselection) and [**ITextRangeProvider::Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-select) methods if the control supports text selection or placement of the text cursor (or system caret) within the text area.</span></span> <span data-ttu-id="5521d-155">如果控制項不支援這項功能，則不需要支援其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="5521d-155">If the control does not support this functionality, it does not need to support either of these methods.</span></span> <span data-ttu-id="5521d-156">不過，控制項必須藉由實 [**ITextProvider：： SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) 屬性，來公開所支援的文字選取類型。</span><span class="sxs-lookup"><span data-stu-id="5521d-156">However, the control must expose the type of text selection it supports by implementing the [**ITextProvider::SupportedTextSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_supportedtextselection) property.</span></span>

<span data-ttu-id="5521d-157">提供者一律必須支援 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 常數、 **TextUnit \_ 字元** 和 **TextUnit \_ 檔**，以及它能夠支援的其他專案。</span><span class="sxs-lookup"><span data-stu-id="5521d-157">A provider must always support the [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) constants, **TextUnit\_Character** and **TextUnit\_Document**, as well as any others it is capable of supporting.</span></span>

> [!Note]  
> <span data-ttu-id="5521d-158">提供者可以跳到下一個最大的單位（依下列順序支援），以略過對特定 [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) 的支援： **TextUnit \_ Character**、 **TextUnit \_ Format**、 **TextUnit \_ Word**、 **TextUnit \_ Line**、 **TextUnit \_ 段落**、 **TextUnit \_ 頁面** 和 **TextUnit \_ 檔**。</span><span class="sxs-lookup"><span data-stu-id="5521d-158">The provider may skip support for a specific [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) by deferring to the next largest unit supported in the following order: **TextUnit\_Character**, **TextUnit\_Format**, **TextUnit\_Word**, **TextUnit\_Line**, **TextUnit\_Paragraph**, **TextUnit\_Page**, and **TextUnit\_Document**.</span></span>

 

## <a name="client-interfaces"></a><span data-ttu-id="5521d-159">用戶端介面</span><span class="sxs-lookup"><span data-stu-id="5521d-159">Client Interfaces</span></span>

<span data-ttu-id="5521d-160">消費者介面自動化用戶端應用程式會使用 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) 介面來存取文字控制項的文字內容。</span><span class="sxs-lookup"><span data-stu-id="5521d-160">UI Automation client applications use the [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces to access the textual content of a text control.</span></span> <span data-ttu-id="5521d-161">用戶端會使用 **IUIAutomationTextPattern** 來選取稱為 *文字範圍* 的文字範圍，以及取得範圍的 **IUIAutomationTextRange** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5521d-161">Clients use **IUIAutomationTextPattern** to select spans of text called *text ranges*, and to retrieve pointers to **IUIAutomationTextRange** interfaces for the ranges.</span></span> <span data-ttu-id="5521d-162">**IUIAutomationTextRange** 介面可讓用戶端操作文字範圍，以及抓取範圍內文字的相關資訊，包括字型名稱、前景色彩、底線樣式等屬性。</span><span class="sxs-lookup"><span data-stu-id="5521d-162">The **IUIAutomationTextRange** interface enables clients to manipulate the text range, and to retrieve information about the text in the range, including attributes such as font name, foreground color, underline style, and so on.</span></span> <span data-ttu-id="5521d-163">如需詳細資訊，請參閱 [文字屬性識別碼](uiauto-textattribute-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="5521d-163">For more information, see [Text Attribute Identifiers](uiauto-textattribute-ids.md).</span></span>

## <a name="performance"></a><span data-ttu-id="5521d-164">效能</span><span class="sxs-lookup"><span data-stu-id="5521d-164">Performance</span></span>

<span data-ttu-id="5521d-165">**文字** 控制項模式依賴跨進程呼叫來處理大部分的功能，因此它不會提供快取機制來改善處理內容時的效能。</span><span class="sxs-lookup"><span data-stu-id="5521d-165">The **Text** control pattern relies on cross-process calls for most of its functionality, so it does not provide a caching mechanism to improve performance when it processes content.</span></span> <span data-ttu-id="5521d-166">您可以使用 [**IUIAutomationElement：： GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) 方法來存取 Microsoft 消費者介面自動化中的其他控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5521d-166">Other control patterns in Microsoft UI Automation can be accessed by using the [**IUIAutomationElement::GetCachedPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern) method.</span></span>

<span data-ttu-id="5521d-167">改善效能的其中一種技術，是確保消費者介面自動化用戶端使用 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) 方法，嘗試取出適度大小的文字區塊。</span><span class="sxs-lookup"><span data-stu-id="5521d-167">One technique for improving performance is to ensure that UI Automation clients attempt to retrieve moderately sized blocks of text by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method.</span></span> <span data-ttu-id="5521d-168">例如，使用 **GetText** 抓取單一字元將會產生每個字元的跨進程叫用，而不會在呼叫 **GetText** 時指定最大長度，而會產生一個跨進程叫用，但視文字範圍的大小而定，可能會有高延遲。</span><span class="sxs-lookup"><span data-stu-id="5521d-168">For example, using **GetText** to retrieve single characters will incur cross-process hits for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="text-pattern-and-virtualized-embedded-objects"></a><span data-ttu-id="5521d-169">文字模式和虛擬化内嵌物件</span><span class="sxs-lookup"><span data-stu-id="5521d-169">Text Pattern and Virtualized Embedded Objects</span></span>

<span data-ttu-id="5521d-170">如果可能的話， [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 和 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) 的提供者必須支援檔的整個文字，包括在視口以外的任何文字。</span><span class="sxs-lookup"><span data-stu-id="5521d-170">Whenever possible, a provider implementation of [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) should support the entire text of a document, including any text outside of the viewport.</span></span> <span data-ttu-id="5521d-171">針對已虛擬化的非螢幕文字或内嵌物件，提供者應該支援 [VirtualizedItem 控制項模式](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)) 。</span><span class="sxs-lookup"><span data-stu-id="5521d-171">For off-screen text or embedded objects that are virtualized, providers should support the [VirtualizedItem control pattern](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)).</span></span>

<span data-ttu-id="5521d-172">如果檔是在整個文字資料流程仍然可用的情況下進行虛擬化， [**ITextProvider：:D ocumentrange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) 屬性將會取出包含整份檔的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="5521d-172">If a document is virtualized while the entire text stream is still available, the [**ITextProvider::DocumentRange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-get_documentrange) property will retrieve a text range that includes the entire document.</span></span> <span data-ttu-id="5521d-173">不過，呼叫 [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) 方法將會取得虛擬化物件的集合，這些物件代表檔中的所有内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="5521d-173">However, calling the [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getchildren) method will retrieve a collection of virtualized objects that represent all embedded objects in the document.</span></span> <span data-ttu-id="5521d-174">若要與虛擬化的内嵌物件互動，用戶端必須呼叫 [**IVirtualizedItemProvider：：意識**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) 方法，使專案可完全作為消費者介面自動化專案來存取。</span><span class="sxs-lookup"><span data-stu-id="5521d-174">To interact with a virtualized embedded object, clients must call the [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) method, which makes the items fully accessible as UI Automation elements.</span></span> <span data-ttu-id="5521d-175">用戶端必須遵循類似的程式來處理內嵌資料表中的方格元素，其中部分資料表是在螢幕上，而虛擬化。</span><span class="sxs-lookup"><span data-stu-id="5521d-175">Clients must follow a similar process to work with grid elements in an embedded table where a portion of the table is off-screen and virtualized.</span></span>

## <a name="using-the-custom-control-type-with-the-text-control-pattern"></a><span data-ttu-id="5521d-176">使用具有文字控制項模式的自訂控制項類型</span><span class="sxs-lookup"><span data-stu-id="5521d-176">Using the Custom Control Type with the Text Control Pattern</span></span>

<span data-ttu-id="5521d-177">雖然 [文字](uiauto-implementingtextandtextrange.md) 控制項模式支援許多文字屬性和内嵌物件，但無法預先定義所有可能的檔專案和呈現類型。</span><span class="sxs-lookup"><span data-stu-id="5521d-177">While the [Text](uiauto-implementingtextandtextrange.md) control pattern supports many text attributes and embedded objects, it is not possible to define in advance all possible document elements and presentation types.</span></span> <span data-ttu-id="5521d-178">針對現有的屬性或標準控制項類型不支援的檔專案，提供者可以使用消費者介面自動化 **自訂** 控制項類型所提供的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="5521d-178">For document elements that are not supported by the existing attributes or standard control types, providers can use the extensibility features provided by the UI Automation **Custom** control type.</span></span>

<span data-ttu-id="5521d-179">對於以頁面簡報為基礎的應用程式和使用者介面，「頁面」的界限和版面配置呈現也可以表示為具有自訂控制項類型的内嵌物件， (也就是 `LocalizedControlType="page"`) 。</span><span class="sxs-lookup"><span data-stu-id="5521d-179">For applications and user interfaces that are based on page presentations, the boundary and layout presentation of "page" can also be expressed as an embedded object that has a custom control type (that is, `LocalizedControlType="page"`).</span></span> <span data-ttu-id="5521d-180">如此一來，内嵌物件就可以裝載其他無法輕易成為檔文字資料流程一部分的頁面元素，例如，每個頁面的頁首和頁尾欄位，做為「頁面」内嵌物件的子系。</span><span class="sxs-lookup"><span data-stu-id="5521d-180">That way, the embedded object can host other page elements that cannot easily be part of the document text stream, such as the header and footer fields of each page, as children of the "page" embedded object.</span></span> <span data-ttu-id="5521d-181">或者，每個「頁面」物件都可以獨立支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，這適用于製作投影片放映簡報或以頁面為基礎的桌面發行環境等應用程式。</span><span class="sxs-lookup"><span data-stu-id="5521d-181">Alternatively, each "page" object can support the [Text](uiauto-implementingtextandtextrange.md) control pattern independently, which works well for applications such as authoring tools for slide show presentations, or page-based desktop publishing environments.</span></span>

## <a name="lifetime-of-a-text-range"></a><span data-ttu-id="5521d-182">文字範圍的存留期</span><span class="sxs-lookup"><span data-stu-id="5521d-182">Lifetime of a Text Range</span></span>

<span data-ttu-id="5521d-183">可能的話，提供者應該確保任何文字變更（例如刪除、插入和移動）都會反映在相關聯的文字範圍中。</span><span class="sxs-lookup"><span data-stu-id="5521d-183">If possible, a provider should ensure that any text changes, such as deletions, insertions, and moves, are reflected in the associated text range.</span></span> <span data-ttu-id="5521d-184">如果無法更新文字範圍，則提供者應該引發 [**UIA \_ text \_ TextChangedEventId**](uiauto-event-ids.md) 事件，以通知用戶端文字範圍已不再有效，而且必須抓取新的範圍。</span><span class="sxs-lookup"><span data-stu-id="5521d-184">If updating the text range is not possible, the provider should raise a [**UIA\_Text\_TextChangedEventId**](uiauto-event-ids.md) event to notify clients that the text range is no longer valid and a new one must be retrieved.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5521d-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="5521d-185">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5521d-186">**概念**</span><span class="sxs-lookup"><span data-stu-id="5521d-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5521d-187">消費者介面自動化如何支援内嵌物件</span><span class="sxs-lookup"><span data-stu-id="5521d-187">How UI Automation Supports Embedded Objects</span></span>](uiauto-textpattern-and-embedded-objects-overview.md)
</dt> <dt>

[<span data-ttu-id="5521d-188">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="5521d-188">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="5521d-189">消費者介面自動化文字內容的支援</span><span class="sxs-lookup"><span data-stu-id="5521d-189">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="5521d-190">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="5521d-190">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> <dt>

<span data-ttu-id="5521d-191">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5521d-191">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5521d-192">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="5521d-192">Text Services Framework</span></span>](/windows/desktop/TSF/text-services-framework)
</dt> </dl>

 

 
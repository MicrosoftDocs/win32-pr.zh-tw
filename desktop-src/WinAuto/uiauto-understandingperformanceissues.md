---
title: 瞭解效能問題
description: 本主題描述與使用 Text 和 TextRange 控制項模式相關聯的效能問題。
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- 用戶端，瞭解效能問題
- 用戶端，以文字為基礎的控制項
- 用戶端、文字範圍
- 用戶端、文字控制項模式
- 用戶端、TextRange 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316825"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="baa75-108">瞭解效能問題</span><span class="sxs-lookup"><span data-stu-id="baa75-108">Understanding Performance Issues</span></span>

<span data-ttu-id="baa75-109">本主題描述與使用 [Text 和 TextRange](uiauto-implementingtextandtextrange.md) 控制項模式相關聯的效能問題。</span><span class="sxs-lookup"><span data-stu-id="baa75-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="baa75-110">[**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern)和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)介面會依賴跨進程呼叫，而不會提供快取機制來改善在抓取或處理文字內容時的效能。</span><span class="sxs-lookup"><span data-stu-id="baa75-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="baa75-111">用戶端應用程式可以使用 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) 方法來取得中等大小的文字區塊，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="baa75-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="baa75-112">例如，使用 **GetText** 來取出單一字元將會對每個字元產生跨進程效能的影響，而不會在呼叫 **GetText** 時指定最大長度，而會產生一個跨進程叫用，但視文字範圍的大小而定，可能會有高延遲。</span><span class="sxs-lookup"><span data-stu-id="baa75-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baa75-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="baa75-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa75-114">Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="baa75-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="baa75-115">消費者介面自動化文字內容的支援</span><span class="sxs-lookup"><span data-stu-id="baa75-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="baa75-116">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="baa75-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 





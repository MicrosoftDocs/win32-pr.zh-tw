---
description: 決定何時以及如何在應用程式中使用分界線物件時，請考慮下列事項：
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: 其他分隔因素考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193718"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="b8e83-103">其他分隔因素考慮</span><span class="sxs-lookup"><span data-stu-id="b8e83-103">Other Divider Considerations</span></span>

<span data-ttu-id="b8e83-104">決定何時以及如何在應用程式中使用 [**分界線**](inkdivider-class.md) 物件時，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="b8e83-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="b8e83-105">[**分隔**](inkdivider-class.md)物件是設計用來分隔繪圖和手寫區塊，但無法辨識較高層級的結構，例如資料表或資料行。</span><span class="sxs-lookup"><span data-stu-id="b8e83-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="b8e83-106">[**分隔**](inkdivider-class.md)物件不會提供特別用來更正版面配置分析結果的介面。</span><span class="sxs-lookup"><span data-stu-id="b8e83-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="b8e83-107">使用 timeout 和筆劃啟發學習法來從 [**分隔**](inkdivider-class.md) 物件中的筆劃一次新增或移除多個筆劃，可能會改善效能。</span><span class="sxs-lookup"><span data-stu-id="b8e83-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="b8e83-108">Reanalysis 考慮</span><span class="sxs-lookup"><span data-stu-id="b8e83-108">Reanalysis Considerations</span></span>

<span data-ttu-id="b8e83-109">如果您考慮在應用程式中使用 [**分割**](inkdivider-class.md) 物件，而該應用程式中的 **分隔** 物件可能必須重新分析大量筆墨，請記住下列事項。</span><span class="sxs-lookup"><span data-stu-id="b8e83-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="b8e83-110">保留筆跡和筆劃的複本</span><span class="sxs-lookup"><span data-stu-id="b8e83-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="b8e83-111">應用程式可以針對稍後會在應用程式會話中進行的應用程式專案，保留 [**筆跡**](inkdisp-class.md) 和 [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件的複本。</span><span class="sxs-lookup"><span data-stu-id="b8e83-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="b8e83-112">如此一來，如果使用者返回專案，就不需要重新分析 **筆墨** 物件。</span><span class="sxs-lookup"><span data-stu-id="b8e83-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="b8e83-113">這種方法會將記憶體交易成更好的效能。</span><span class="sxs-lookup"><span data-stu-id="b8e83-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="b8e83-114">資料縮減啟發學習法</span><span class="sxs-lookup"><span data-stu-id="b8e83-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="b8e83-115">您或許可以將分析結果記錄為應用程式資料，並執行啟發學習法來決定何時要重新分析一組筆劃。</span><span class="sxs-lookup"><span data-stu-id="b8e83-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="b8e83-116">這種作法可減少在應用程式會話之間重新分析應用程式中所有筆墨的需求。</span><span class="sxs-lookup"><span data-stu-id="b8e83-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="b8e83-117">但是，必須小心保留結構化專案界限，或重新分析受影響專案的所有筆觸。</span><span class="sxs-lookup"><span data-stu-id="b8e83-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8e83-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8e83-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e83-119">**InkDivider 類別**</span><span class="sxs-lookup"><span data-stu-id="b8e83-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="b8e83-120">[Node.js 類別](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="b8e83-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 

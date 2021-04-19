---
description: 複雜的指令碼語言會依 ScriptShape 分割成叢集。 字元重新排列一律會出現在叢集界限內。 叢集本身保證會以讀取順序的方向前進。
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: 管理插入號放置和點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977186"
---
# <a name="managing-caret-placement-and-hit-testing"></a><span data-ttu-id="da86c-105">管理插入號放置和點擊測試</span><span class="sxs-lookup"><span data-stu-id="da86c-105">Managing Caret Placement and Hit Testing</span></span>

<span data-ttu-id="da86c-106">複雜的指令碼語言會依 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)[分割成](uniscribe-glossary.md)叢集。</span><span class="sxs-lookup"><span data-stu-id="da86c-106">Complex script languages are broken into [clusters](uniscribe-glossary.md) by [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).</span></span> <span data-ttu-id="da86c-107">字元重新排列一律會出現在叢集界限內。</span><span class="sxs-lookup"><span data-stu-id="da86c-107">Character reordering always occurs within cluster boundaries.</span></span> <span data-ttu-id="da86c-108">叢集本身保證會以讀取順序的方向前進。</span><span class="sxs-lookup"><span data-stu-id="da86c-108">The clusters themselves are guaranteed to advance in the direction of the reading order.</span></span>

<span data-ttu-id="da86c-109">邏輯群集陣列中的叢集資訊是用來在它們所代表的邏輯字元之間，平均共用圖像的群集寬度。</span><span class="sxs-lookup"><span data-stu-id="da86c-109">Cluster information in the logical cluster array is used to share the width of a cluster of glyphs equally among the logical characters they represent.</span></span> <span data-ttu-id="da86c-110">例如，有四個區域可以分為四個區域：</span><span class="sxs-lookup"><span data-stu-id="da86c-110">For example, the lam alef glyph is divided into four areas:</span></span>

-   <span data-ttu-id="da86c-111">Lam 的上半部。</span><span class="sxs-lookup"><span data-stu-id="da86c-111">The leading half of the lam.</span></span>
-   <span data-ttu-id="da86c-112">Lam 的尾端半部。</span><span class="sxs-lookup"><span data-stu-id="da86c-112">The trailing half of the lam.</span></span>
-   <span data-ttu-id="da86c-113">後半的 alef。</span><span class="sxs-lookup"><span data-stu-id="da86c-113">The leading half of the alef.</span></span>
-   <span data-ttu-id="da86c-114">Alef 的尾端半部。</span><span class="sxs-lookup"><span data-stu-id="da86c-114">The trailing half of the alef.</span></span>

<span data-ttu-id="da86c-115">在叢集內放置插入號的慣例取決於腳本。</span><span class="sxs-lookup"><span data-stu-id="da86c-115">Conventions for caret placement within clusters depend on the script.</span></span> <span data-ttu-id="da86c-116">若是阿拉伯文腳本，如果在基底字元與其組合標記之間設定插入號位置，插入號會顯示在基底字元的中間。</span><span class="sxs-lookup"><span data-stu-id="da86c-116">For the Arabic script, if the caret position is set between a base character and its combining mark, the caret is displayed halfway through the base character.</span></span> <span data-ttu-id="da86c-117">若為泰文腳本，插入號不能放在叢集內。</span><span class="sxs-lookup"><span data-stu-id="da86c-117">For the Thai script, the caret cannot be positioned within a cluster.</span></span> <span data-ttu-id="da86c-118">因此，當使用者將插入號前移時，應用程式必須提前超過組成叢集的所有字元。</span><span class="sxs-lookup"><span data-stu-id="da86c-118">Thus, when the user advances the caret, the application must advance past all the glyphs that make up the cluster.</span></span>

<span data-ttu-id="da86c-119">[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)和 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)函式會轉譯 (于程式碼點位移) 和 x 位置 (以圖元) 表示的插入號位置。</span><span class="sxs-lookup"><span data-stu-id="da86c-119">The [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) and [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) functions translate between caret positions (in code point offsets) and x positions (in pixels).</span></span> <span data-ttu-id="da86c-120">**ScriptXtoCP** 函式知道每個腳本的插入號位置慣例：</span><span class="sxs-lookup"><span data-stu-id="da86c-120">The **ScriptXtoCP** function has knowledge of the caret position conventions of each script:</span></span>

-   <span data-ttu-id="da86c-121">針對印度和泰文，插入號位置會貼齊至叢集界限。</span><span class="sxs-lookup"><span data-stu-id="da86c-121">For Indian and Thai, caret positions are snapped to cluster boundaries.</span></span>
-   <span data-ttu-id="da86c-122">若是阿拉伯文，插入號位置會與叢集插補。</span><span class="sxs-lookup"><span data-stu-id="da86c-122">For Arabic, caret positions are interpolated with clusters.</span></span>
-   <span data-ttu-id="da86c-123">若為希伯來文，在 1.420 Usp10.dll 之前的版本中，會將插入號的位置插上叢集。</span><span class="sxs-lookup"><span data-stu-id="da86c-123">For Hebrew, in versions prior to Usp10.dll, version 1.420, caret positions are interpolated with clusters.</span></span> <span data-ttu-id="da86c-124">從 Usp10.dll 開始，1.420 版，插入號位置會貼齊至叢集界限。</span><span class="sxs-lookup"><span data-stu-id="da86c-124">Beginning with Usp10.dll, version 1.420, caret positions are snapped to cluster boundaries.</span></span>

<span data-ttu-id="da86c-125">[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)和 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)只會在執行內運作。</span><span class="sxs-lookup"><span data-stu-id="da86c-125">Both [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) and [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) operate only within runs.</span></span> <span data-ttu-id="da86c-126">這些函式需要某些參數來自先前的 Uniscribe 呼叫，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="da86c-126">The functions require that certain parameters come from earlier Uniscribe calls, as shown in the following table.</span></span>



| <span data-ttu-id="da86c-127">參數</span><span class="sxs-lookup"><span data-stu-id="da86c-127">Parameter</span></span>                                        | <span data-ttu-id="da86c-128">來源</span><span class="sxs-lookup"><span data-stu-id="da86c-128">Source</span></span>                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="da86c-129">*Psa*</span><span class="sxs-lookup"><span data-stu-id="da86c-129">*psa*</span></span>                                            | <span data-ttu-id="da86c-130">[**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)所傳回的。</span><span class="sxs-lookup"><span data-stu-id="da86c-130">As returned by [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize).</span></span> |
| <span data-ttu-id="da86c-131">*cGlyphspwLogClust*</span><span class="sxs-lookup"><span data-stu-id="da86c-131">*cGlyphspwLogClust*</span></span><br/> <span data-ttu-id="da86c-132">*psva*</span><span class="sxs-lookup"><span data-stu-id="da86c-132">*psva*</span></span><br/> | <span data-ttu-id="da86c-133">[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)所傳回的。</span><span class="sxs-lookup"><span data-stu-id="da86c-133">As returned by [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).</span></span>     |
| <span data-ttu-id="da86c-134">*piAdvance*</span><span class="sxs-lookup"><span data-stu-id="da86c-134">*piAdvance*</span></span>                                      | <span data-ttu-id="da86c-135">[**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)所傳回的。</span><span class="sxs-lookup"><span data-stu-id="da86c-135">As returned by [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).</span></span>     |



 

<span data-ttu-id="da86c-136">應用程式必須在將資訊傳遞至 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) 或 [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)之前，建立指定的插入號位移或 x 位置的執行。</span><span class="sxs-lookup"><span data-stu-id="da86c-136">The application must establish the run in which a given caret offset or x position is before passing the information to [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) or [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp).</span></span> <span data-ttu-id="da86c-137">如果應用程式未儲存寬度資訊，它可以在顯示每次執行之後，執行點擊測試和插入號放置。</span><span class="sxs-lookup"><span data-stu-id="da86c-137">If the application does not save the width information, it can do hit testing and caret placement after displaying each run.</span></span> <span data-ttu-id="da86c-138">或者，應用程式可以快取足夠的資訊，以便在目前的行上進行點擊測試和插入號放置，而不需要重新處理段落。</span><span class="sxs-lookup"><span data-stu-id="da86c-138">As an alternative, the application can cache enough information to do hit testing and caret placement on the current line without requiring reprocessing of the paragraph.</span></span>

<span data-ttu-id="da86c-139">[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 會傳回尾端的邊緣值，讓應用程式知道使用者已按下的字元或叢集的側邊。</span><span class="sxs-lookup"><span data-stu-id="da86c-139">[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) returns a trailing edge value so that the application knows the side of the character or cluster on which the user has clicked.</span></span> <span data-ttu-id="da86c-140">在程式碼點中，此值為0或字元或叢集的寬度。</span><span class="sxs-lookup"><span data-stu-id="da86c-140">The value is either 0 or the width of the character or cluster in code points.</span></span> <span data-ttu-id="da86c-141">傳回的字元位置是使用者按一下的字元位置。</span><span class="sxs-lookup"><span data-stu-id="da86c-141">The returned character position is the position of the character on which the user clicked.</span></span> <span data-ttu-id="da86c-142">如需詳細資訊，請參閱 [以雙向字串顯示插入](displaying-the-caret-in-bidirectional-strings.md)號。</span><span class="sxs-lookup"><span data-stu-id="da86c-142">For more information, see [Displaying the Caret in Bidirectional Strings](displaying-the-caret-in-bidirectional-strings.md).</span></span>

<span data-ttu-id="da86c-143">若為泰文之類的語言，如果使用者不想將插入號放入叢集中， [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 會將尾端的側旗標設為0或叢集寬度。</span><span class="sxs-lookup"><span data-stu-id="da86c-143">For languages such as Thai, for which the user conventionally does not want to place the caret into a cluster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) sets the trailing side flag to 0 or to the cluster width.</span></span> <span data-ttu-id="da86c-144">若是阿拉伯文等語言，使用者預期能夠在叢集中進行編輯， **ScriptXtoCP** 會將尾端的側旗標設定為0或1。</span><span class="sxs-lookup"><span data-stu-id="da86c-144">For languages such as Arabic, for which the user expects to be able to edit within a cluster, **ScriptXtoCP** sets the trailing side flag to 0 or to 1.</span></span>

<span data-ttu-id="da86c-145">為了協助應用程式在處理箭號鍵時建立插入號的有效位置，Uniscribe 會在 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)所傳回的邏輯屬性中，提供 **fCharStop** 成員中有效插入號位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da86c-145">To help the application establish valid locations for the caret when handling the arrow keys, Uniscribe provides information on valid caret positions in the **fCharStop** member in the logical attributes returned by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span> <span data-ttu-id="da86c-146">針對大部分的字元，會傳回 **TRUE** ，而在像是泰文的腳本中，intercluster 字元則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="da86c-146">**TRUE** is returned for most characters and **FALSE** for intercluster characters in scripts such as Thai.</span></span> <span data-ttu-id="da86c-147">應用程式應該檢查項目的 [**腳本 \_ 屬性**](/windows/desktop/api/Usp10/ns-usp10-script_properties)結構中的 **fNeedsCaretInfo** 值，以查看是否需要呼叫 **ScriptBreak** 來檢查有效的插入號位置。</span><span class="sxs-lookup"><span data-stu-id="da86c-147">The application should check the **fNeedsCaretInfo** value in the [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) structure for an item to see if it is necessary to call **ScriptBreak** to check for valid caret positions.</span></span> <span data-ttu-id="da86c-148">如果 **fNeedsCaretInfo** 值為 **FALSE**，則所有的程式碼點都是有效的插入號位置。</span><span class="sxs-lookup"><span data-stu-id="da86c-148">If the **fNeedsCaretInfo** value is **FALSE**, all code points are valid caret positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da86c-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="da86c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da86c-150">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="da86c-150">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 





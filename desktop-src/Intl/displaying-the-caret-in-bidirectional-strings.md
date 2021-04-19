---
description: 在單向文字中，插入號位置沒有任何明確的原因，因為字元的開頭邊緣與上一個字元的尾端邊緣位於相同的位置。
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: 以雙向字串顯示插入號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985066"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="85a8d-103">以雙向字串顯示插入號</span><span class="sxs-lookup"><span data-stu-id="85a8d-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="85a8d-104">在單向文字中，插入號位置沒有任何明確的原因，因為字元的開頭邊緣與上一個字元的尾端邊緣位於相同的位置。</span><span class="sxs-lookup"><span data-stu-id="85a8d-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="85a8d-105">不過，在雙向文字中，相反方向的執行插入號位置不明確。</span><span class="sxs-lookup"><span data-stu-id="85a8d-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="85a8d-106">例如，在從左至右的段落 "hellosalaam" 中，"hello" 的最後一個字母會緊接在 "salaam" 的第一個字母之前。</span><span class="sxs-lookup"><span data-stu-id="85a8d-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="85a8d-107">要在其中顯示插入號的最佳位置，取決於是否要將它視為緊接在 "hello" 的 "o" 或 "salaam" 的 "s" 之前。</span><span class="sxs-lookup"><span data-stu-id="85a8d-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="85a8d-108">Uniscribe 會使用下表所示的插入號定位慣例。</span><span class="sxs-lookup"><span data-stu-id="85a8d-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="85a8d-109">情況</span><span class="sxs-lookup"><span data-stu-id="85a8d-109">Situation</span></span>       | <span data-ttu-id="85a8d-110">視覺插入號放置</span><span class="sxs-lookup"><span data-stu-id="85a8d-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="85a8d-111">輸入</span><span class="sxs-lookup"><span data-stu-id="85a8d-111">Typing</span></span>          | <span data-ttu-id="85a8d-112">最後一個輸入字元的尾端邊緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="85a8d-113">粘貼</span><span class="sxs-lookup"><span data-stu-id="85a8d-113">Pasting</span></span>         | <span data-ttu-id="85a8d-114">貼上最後一個字元的尾端邊緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="85a8d-115">插入號前移</span><span class="sxs-lookup"><span data-stu-id="85a8d-115">Caret advancing</span></span> | <span data-ttu-id="85a8d-116">最後一個傳遞的字元的尾端邊緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="85a8d-117">插入號淘汰</span><span class="sxs-lookup"><span data-stu-id="85a8d-117">Caret retiring</span></span>  | <span data-ttu-id="85a8d-118">最後一個傳遞的字元開頭緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="85a8d-119">首頁</span><span class="sxs-lookup"><span data-stu-id="85a8d-119">Home</span></span>            | <span data-ttu-id="85a8d-120">直線的開頭緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="85a8d-121">結束</span><span class="sxs-lookup"><span data-stu-id="85a8d-121">End</span></span>             | <span data-ttu-id="85a8d-122">行的尾端邊緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="85a8d-123">插入號可以定位，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="85a8d-123">The caret can be positioned as shown in the following example:</span></span>


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



<span data-ttu-id="85a8d-124">如果 *fAdvancing* 值限制為 **TRUE** 或 **FALSE**，插入號的位置可能更簡單（如下所示）：</span><span class="sxs-lookup"><span data-stu-id="85a8d-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="85a8d-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) 會以邏輯方式處理超出範圍的位置。</span><span class="sxs-lookup"><span data-stu-id="85a8d-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="85a8d-126">它會傳回 *iCharPos* 執行的開頭緣 <0，以及 *iCharPos* >= length 回合的尾端邊緣。</span><span class="sxs-lookup"><span data-stu-id="85a8d-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="85a8d-127">如需詳細資訊，請參閱 [管理插入點放置和點擊測試](managing-caret-placement-and-hit-testing.md)</span><span class="sxs-lookup"><span data-stu-id="85a8d-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="85a8d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="85a8d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a8d-129">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="85a8d-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




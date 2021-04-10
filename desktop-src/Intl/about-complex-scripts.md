---
description: 複雜字集是腳本屬性的 fComplex 成員 \_ 設為 TRUE 的腳本。 本主題詳細說明複雜字集可能具有的屬性。
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: 關於複雜字集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027033"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="61b42-104">關於複雜字集</span><span class="sxs-lookup"><span data-stu-id="61b42-104">About Complex Scripts</span></span>

<span data-ttu-id="61b42-105">[複雜字集](uniscribe-glossary.md)是腳本 [**\_ 屬性**](/windows/desktop/api/Usp10/ns-usp10-script_properties)的 **fComplex** 成員設為 **TRUE** 的腳本。</span><span class="sxs-lookup"><span data-stu-id="61b42-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="61b42-106">本主題詳細說明複雜字集可能具有的屬性。</span><span class="sxs-lookup"><span data-stu-id="61b42-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="61b42-107">雙向轉譯</span><span class="sxs-lookup"><span data-stu-id="61b42-107">Bidirectional Rendering</span></span>

<span data-ttu-id="61b42-108">雙向轉譯會處理從左至右和由右至左讀取的文字。</span><span class="sxs-lookup"><span data-stu-id="61b42-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="61b42-109">例如，在阿拉伯文的雙向轉譯中，文字的預設讀取方向是由右至左，但某些數位的預設讀取方向是由左至右。</span><span class="sxs-lookup"><span data-stu-id="61b42-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="61b42-110">處理複雜的腳本必須考慮邏輯 (按鍵) 順序和圖像視覺效果順序之間的差異。</span><span class="sxs-lookup"><span data-stu-id="61b42-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="61b42-111">此外，處理必須正確處理插入號移動和點擊測試。</span><span class="sxs-lookup"><span data-stu-id="61b42-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="61b42-112">畫面位置和字元索引之間的對應需要瞭解特定顯示器的版面配置演算法，例如選取的文字或插入號顯示。</span><span class="sxs-lookup"><span data-stu-id="61b42-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="61b42-113">內容塑造</span><span class="sxs-lookup"><span data-stu-id="61b42-113">Contextual Shaping</span></span>

<span data-ttu-id="61b42-114">在內容成形中，腳本字元會根據周圍的字元來變更圖形。</span><span class="sxs-lookup"><span data-stu-id="61b42-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="61b42-115">當小寫的 "l" 變更圖形（視其前面的字元而定，例如 "a" (連接較低至 "l" ) 或 "o" (連接高) 時，就會在英文中撰寫這類成形。</span><span class="sxs-lookup"><span data-stu-id="61b42-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="61b42-116">例如，阿拉伯文是展示內容成形的腳本。</span><span class="sxs-lookup"><span data-stu-id="61b42-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="61b42-117">合併字元</span><span class="sxs-lookup"><span data-stu-id="61b42-117">Combining Characters</span></span>

<span data-ttu-id="61b42-118">合併字元（也稱為「連字號」）是將字元放在一起時，會加入一個字元的字元。</span><span class="sxs-lookup"><span data-stu-id="61b42-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="61b42-119">阿拉伯文是具有許多合併字元的腳本。</span><span class="sxs-lookup"><span data-stu-id="61b42-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="61b42-120">使用合併字元的其中一個範例是 "a"，後面接著「組合重音符號」，其呈現的標記法為 "à"。</span><span class="sxs-lookup"><span data-stu-id="61b42-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="61b42-121">Unicode 資料流程 "U + 0061 U + 0300" 需要進行一些處理，以確保「組合的抑音符號」正確定位在 "a" 的上方。</span><span class="sxs-lookup"><span data-stu-id="61b42-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="61b42-122">特製化斷詞和對齊方式</span><span class="sxs-lookup"><span data-stu-id="61b42-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="61b42-123">某些腳本（例如，泰文）有複雜的規則，可將文字行之間的單字分隔，或線上條上對齊文字。</span><span class="sxs-lookup"><span data-stu-id="61b42-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="61b42-124">篩選不合法的字元組合</span><span class="sxs-lookup"><span data-stu-id="61b42-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="61b42-125">例如，當語言不允許某些字元組合時，複雜的腳本（例如，泰文）可以篩選出不合法的字元組合。</span><span class="sxs-lookup"><span data-stu-id="61b42-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="61b42-126">字型 Fallback</span><span class="sxs-lookup"><span data-stu-id="61b42-126">Font Fallback</span></span>

<span data-ttu-id="61b42-127">字型回復是除了使用者選取的字型之外，自動選取字型。</span><span class="sxs-lookup"><span data-stu-id="61b42-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="61b42-128">在 Uniscribe 中，當所有或部分文字都在使用者選取的字型不支援的腳本中時， [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) 函式會套用字型回復。</span><span class="sxs-lookup"><span data-stu-id="61b42-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="61b42-129">如需詳細資訊，請參閱 [使用字型](using-font-fallback.md)回復。</span><span class="sxs-lookup"><span data-stu-id="61b42-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b42-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="61b42-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b42-131">關於 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="61b42-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 




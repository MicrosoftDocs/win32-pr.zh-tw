---
description: ABC 寬度是由 GDI ABC 結構所定義的複合值。 結構包含 abcA、abcB 和 abcC 的成員，對應于 &\# 0034;A&\# 0034;，&\# 0034;B&\# 0034; 和 &\# 0034;C&\# 0034; 圖像或執行的寬度。
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Uniscribe 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e154e65c103ce6e4287ac8aa2e76e0be4206f9fd
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316723"
---
# <a name="uniscribe-glossary"></a><span data-ttu-id="ebea9-104">Uniscribe 詞彙</span><span class="sxs-lookup"><span data-stu-id="ebea9-104">Uniscribe Glossary</span></span>

<span data-ttu-id="ebea9-105">ABC 寬度是由 GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) 結構所定義的複合值。</span><span class="sxs-lookup"><span data-stu-id="ebea9-105">An ABC width is a composite value defined by a GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) structure.</span></span> <span data-ttu-id="ebea9-106">結構包含 **abcA**、 **abcB** 和 **abcC** 的成員，對應至圖像的 "A"、"B" 和 "C"[寬度或](#glyph)[執行](#run)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-106">The structure contains members **abcA**, **abcB**, and **abcC**, corresponding to the "A", "B", and "C" widths of a [glyph](#glyph) or [run](#run).</span></span>

<span data-ttu-id="ebea9-107">"A" 寬度是 [underhang](#underhang) (正數;也稱為「填補」 ) 或 [懸垂](#overhang) (在代表圖像或執行之筆墨的螢幕上對等的負面) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-107">The "A" width is [underhang](#underhang) (positive; also known as "padding") or [overhang](#overhang) (negative) to the left of the on-screen equivalent of ink that represents the glyph or run.</span></span> <span data-ttu-id="ebea9-108">「B」寬度是黑色寬度，從最左邊的筆墨到最右邊的筆墨寬度。</span><span class="sxs-lookup"><span data-stu-id="ebea9-108">The "B" width is the black width, the width from the leftmost ink to the rightmost ink.</span></span> <span data-ttu-id="ebea9-109">"C" 寬度是筆墨右邊的懸垂。</span><span class="sxs-lookup"><span data-stu-id="ebea9-109">The "C" width is overhang to the right of the ink.</span></span>

<span data-ttu-id="ebea9-110">下圖顯示斜體小寫 F，其左邊和右邊都有懸垂。</span><span class="sxs-lookup"><span data-stu-id="ebea9-110">The following illustration shows an italic lowercase F with overhang to both its left and right.</span></span> <span data-ttu-id="ebea9-111">也就是說，此處的 "A" 和 "C" 寬度皆為負數。</span><span class="sxs-lookup"><span data-stu-id="ebea9-111">That is, the "A" and "C" widths here are both negative.</span></span> <span data-ttu-id="ebea9-112">如需正面「A」和「C」寬度的圖例，請參閱 [underhang](#underhang) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-112">See [underhang](#underhang) for an illustration of positive "A" and "C" widths.</span></span>

![圖例顯示斜體小寫 F，其左邊和右邊都有懸垂。](images/abcwidth.gif)

<span data-ttu-id="ebea9-114">當兩個或更多的字元顯示為一個單位時，通常只有最左邊的字元會提供給回合的「A」寬度，且最右邊的字元會成為執行的「C」寬度。</span><span class="sxs-lookup"><span data-stu-id="ebea9-114">When two or more glyphs are displayed as a unit, usually only the leftmost glyph contributes to the "A" width of the run, and only the rightmost glyph contributes to the "C" width of the run.</span></span> <span data-ttu-id="ebea9-115">不過，這並不是嚴格的規則。</span><span class="sxs-lookup"><span data-stu-id="ebea9-115">However, this is not a strict rule.</span></span> <span data-ttu-id="ebea9-116">例如，如果執行中的第一個圖像是窄字母，而第二個字元是寬的變音符號，並以個別的字元來處理，則變音符號可能會實際延伸超過字母。</span><span class="sxs-lookup"><span data-stu-id="ebea9-116">For example, if the first glyph in a run is a narrow letter and the second glyph is a wide diacritical mark, and they are handled as separate glyphs, the diacritical mark might actually extend beyond the letter.</span></span>

## <a name="abc-width"></a><span data-ttu-id="ebea9-117">ABC 寬度</span><span class="sxs-lookup"><span data-stu-id="ebea9-117">ABC width</span></span>

<span data-ttu-id="ebea9-118">ABC 寬度是由 GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) 結構所定義的複合值。</span><span class="sxs-lookup"><span data-stu-id="ebea9-118">An ABC width is a composite value defined by a GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) structure.</span></span> <span data-ttu-id="ebea9-119">結構包含 **abcA**、 **abcB** 和 **abcC** 的成員，對應至圖像的 "A"、"B" 和 "C"[寬度或](#glyph)[執行](#run)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-119">The structure contains members **abcA**, **abcB**, and **abcC**, corresponding to the "A", "B", and "C" widths of a [glyph](#glyph) or [run](#run).</span></span>

<span data-ttu-id="ebea9-120">"A" 寬度是 [underhang](#underhang) (正數;也稱為「填補」 ) 或 [懸垂](#overhang) (在代表圖像或執行之筆墨的螢幕上對等的負面) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-120">The "A" width is [underhang](#underhang) (positive; also known as "padding") or [overhang](#overhang) (negative) to the left of the on-screen equivalent of ink that represents the glyph or run.</span></span> <span data-ttu-id="ebea9-121">「B」寬度是黑色寬度，從最左邊的筆墨到最右邊的筆墨寬度。</span><span class="sxs-lookup"><span data-stu-id="ebea9-121">The "B" width is the black width, the width from the leftmost ink to the rightmost ink.</span></span> <span data-ttu-id="ebea9-122">"C" 寬度是筆墨右邊的懸垂。</span><span class="sxs-lookup"><span data-stu-id="ebea9-122">The "C" width is overhang to the right of the ink.</span></span>

<span data-ttu-id="ebea9-123">下圖顯示斜體小寫 F，其左邊和右邊都有懸垂。</span><span class="sxs-lookup"><span data-stu-id="ebea9-123">The following illustration shows an italic lowercase F with overhang to both its left and right.</span></span> <span data-ttu-id="ebea9-124">也就是說，此處的 "A" 和 "C" 寬度皆為負數。</span><span class="sxs-lookup"><span data-stu-id="ebea9-124">That is, the "A" and "C" widths here are both negative.</span></span> <span data-ttu-id="ebea9-125">如需正面「A」和「C」寬度的圖例，請參閱 [underhang](#underhang) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-125">See [underhang](#underhang) for an illustration of positive "A" and "C" widths.</span></span>

![圖例顯示斜體小寫 F，其左邊和右邊都有懸垂。](images/abcwidth.gif)

<span data-ttu-id="ebea9-127">當兩個或更多的字元顯示為一個單位時，通常只有最左邊的字元會提供給回合的「A」寬度，且最右邊的字元會成為執行的「C」寬度。</span><span class="sxs-lookup"><span data-stu-id="ebea9-127">When two or more glyphs are displayed as a unit, usually only the leftmost glyph contributes to the "A" width of the run, and only the rightmost glyph contributes to the "C" width of the run.</span></span> <span data-ttu-id="ebea9-128">不過，這並不是嚴格的規則。</span><span class="sxs-lookup"><span data-stu-id="ebea9-128">However, this is not a strict rule.</span></span> <span data-ttu-id="ebea9-129">例如，如果執行中的第一個圖像是窄字母，而第二個字元是寬的變音符號，並以個別的字元來處理，則變音符號可能會實際延伸超過字母。</span><span class="sxs-lookup"><span data-stu-id="ebea9-129">For example, if the first glyph in a run is a narrow letter and the second glyph is a wide diacritical mark, and they are handled as separate glyphs, the diacritical mark might actually extend beyond the letter.</span></span>

## <a name="advance-width"></a><span data-ttu-id="ebea9-130">前進寬度</span><span class="sxs-lookup"><span data-stu-id="ebea9-130">advance width</span></span>

<span data-ttu-id="ebea9-131">圖像的前進寬度是從起點開始的方向 [移動，以便](#glyph) 將該圖像轉譯成起點以轉譯下一個圖像。</span><span class="sxs-lookup"><span data-stu-id="ebea9-131">The advance width of a [glyph](#glyph) is the movement in the direction of writing from the starting point for rendering that glyph to the starting point for rendering the next glyph.</span></span>

## <a name="bidirectional-stack"></a><span data-ttu-id="ebea9-132">雙向堆疊</span><span class="sxs-lookup"><span data-stu-id="ebea9-132">bidirectional stack</span></span>

<span data-ttu-id="ebea9-133">雙向堆疊是5位整數，可追蹤從左至右和由右至左的文字之間的嵌套層級。</span><span class="sxs-lookup"><span data-stu-id="ebea9-133">The bidirectional stack is a 5-bit integer that keeps track of nesting levels between left-to-right and right-to-left text.</span></span> <span data-ttu-id="ebea9-134">從左至右，一律從零開始。</span><span class="sxs-lookup"><span data-stu-id="ebea9-134">It always starts at zero for left-to-right.</span></span> <span data-ttu-id="ebea9-135">因此，所有偶數值都代表由左至右的文字，而且所有奇數值都代表由右至左的文字。</span><span class="sxs-lookup"><span data-stu-id="ebea9-135">Thus all even-numbered values represent left-to-right text and all odd-numbered values represent right-to-left text.</span></span> <span data-ttu-id="ebea9-136">雙向堆疊會以 [**腳本 \_ 狀態**](/windows/win32/api/usp10/ns-usp10-script_state)結構的 **uBidiLevel** 成員表示。</span><span class="sxs-lookup"><span data-stu-id="ebea9-136">The bidirectional stack is represented in the **uBidiLevel** member of a [**SCRIPT\_STATE**](/windows/win32/api/usp10/ns-usp10-script_state) structure.</span></span>

## <a name="bidirectional-text"></a><span data-ttu-id="ebea9-137">雙向文字</span><span class="sxs-lookup"><span data-stu-id="ebea9-137">bidirectional text</span></span>

<span data-ttu-id="ebea9-138">雙向文字包含由左至右和由右至左的部分，但有時也會鬆散地套用到純由右至左的文字。</span><span class="sxs-lookup"><span data-stu-id="ebea9-138">Bidirectional text contains both left-to-right and right-to left portions, but the term is also sometimes loosely applied to pure right-to-left text.</span></span> <span data-ttu-id="ebea9-139">所有由右至左的文字都需要使用 [雙向堆疊](#bidirectional-stack)，因為預設的內嵌 [層級](#embedding-level) 為零表示由左至右的文字。</span><span class="sxs-lookup"><span data-stu-id="ebea9-139">All right-to-left text requires the use of the [bidirectional stack](#bidirectional-stack), because the default [embedding level](#embedding-level) of zero implies left-to-right text.</span></span>

## <a name="cell-width"></a><span data-ttu-id="ebea9-140">儲存格寬度</span><span class="sxs-lookup"><span data-stu-id="ebea9-140">cell width</span></span>

<span data-ttu-id="ebea9-141">應用程式可以藉由調整特定字元的儲存格寬度，來調整文字以符合線條。</span><span class="sxs-lookup"><span data-stu-id="ebea9-141">An application can justify text to fit a line by adjusting the cell width for certain glyphs.</span></span> <span data-ttu-id="ebea9-142">若為對齊文字，圖像的資料格寬度與其 [前進寬度](#advance-width)相同。</span><span class="sxs-lookup"><span data-stu-id="ebea9-142">For unjustified text, the cell width for a glyph is the same as its [advance width](#advance-width).</span></span>

## <a name="cluster"></a><span data-ttu-id="ebea9-143">叢集</span><span class="sxs-lookup"><span data-stu-id="ebea9-143">cluster</span></span>

<span data-ttu-id="ebea9-144">群集是可塑造的最小語言單位。</span><span class="sxs-lookup"><span data-stu-id="ebea9-144">A cluster is the smallest linguistic unit that can be shaped.</span></span> <span data-ttu-id="ebea9-145">在阿拉伯文和許多印度文等語言中，用來代表每個字元的字元 (Unicode 程式碼點) 會依賴于構成叢集的周圍程式碼點。</span><span class="sxs-lookup"><span data-stu-id="ebea9-145">In languages such as Arabic and many of the Indic languages, the glyphs used to represent each character (Unicode code point) depend strongly on the surrounding code points, which constitute the cluster.</span></span> <span data-ttu-id="ebea9-146">在這些語言中，應用程式只能藉由查看叢集，將程式碼點轉譯為適當的字元。</span><span class="sxs-lookup"><span data-stu-id="ebea9-146">In these languages, applications can translate code points into appropriate glyphs only by looking at the cluster.</span></span> <span data-ttu-id="ebea9-147">在某些腳本中，例如梵文，在叢集中的字元順序可能會與相對應的 Unicode 程式碼點順序不同。</span><span class="sxs-lookup"><span data-stu-id="ebea9-147">In some scripts, such as Devanagari, the order of glyphs within a cluster can differ from the order of the corresponding Unicode code points.</span></span> <span data-ttu-id="ebea9-148">如需詳細資訊，請參閱 Microsoft 印刷樣式網站上的 [Windows 影像處理](/typography/develop/processing-part1) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-148">For more information, see [Windows Glyph Processing](/typography/develop/processing-part1) on the Microsoft typography site.</span></span>

## <a name="complex-script"></a><span data-ttu-id="ebea9-149">複雜字集</span><span class="sxs-lookup"><span data-stu-id="ebea9-149">complex script</span></span>

<span data-ttu-id="ebea9-150">複雜字集是具有下列任何屬性的 [腳本](#complex-script) ：</span><span class="sxs-lookup"><span data-stu-id="ebea9-150">A complex script is a [script](#complex-script) with any of the following properties:</span></span>

-   <span data-ttu-id="ebea9-151">允許雙向轉譯。</span><span class="sxs-lookup"><span data-stu-id="ebea9-151">Allows bidirectional rendering.</span></span>
-   <span data-ttu-id="ebea9-152">有內容成形。</span><span class="sxs-lookup"><span data-stu-id="ebea9-152">Has contextual shaping.</span></span>
-   <span data-ttu-id="ebea9-153">有組合字元。</span><span class="sxs-lookup"><span data-stu-id="ebea9-153">Has combining characters.</span></span>
-   <span data-ttu-id="ebea9-154">具有特製化的斷詞和理由規則。</span><span class="sxs-lookup"><span data-stu-id="ebea9-154">Has specialized word-breaking and justification rules.</span></span>
-   <span data-ttu-id="ebea9-155">篩選出不合法的字元組合。</span><span class="sxs-lookup"><span data-stu-id="ebea9-155">Filters out illegal character combinations.</span></span>
-   <span data-ttu-id="ebea9-156">不支援核心 Windows 字型，因此可能需要 [字型](#font-fallback)回復。</span><span class="sxs-lookup"><span data-stu-id="ebea9-156">Is not supported in the core Windows fonts and therefore might require [font fallback](#font-fallback).</span></span>

<span data-ttu-id="ebea9-157">在某些複雜的腳本中，圖像的順序可能與它們所代表之基礎 Unicode 字元的順序相當不同。</span><span class="sxs-lookup"><span data-stu-id="ebea9-157">In some complex scripts, the order of the glyphs might be quite different from the order of the underlying Unicode characters they represent.</span></span> <span data-ttu-id="ebea9-158">如需詳細資訊，請參閱 [關於複雜字集](about-complex-scripts.md) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-158">See [About Complex Scripts](about-complex-scripts.md) for more detail.</span></span>

> [!Note]  
> <span data-ttu-id="ebea9-159">在印刷環境中，有時需要處理用來撰寫英文做為複雜字集的拉丁腳本。</span><span class="sxs-lookup"><span data-stu-id="ebea9-159">In the context of typography, it is sometimes desirable to handle the Latin script used in writing English as a complex script.</span></span> <span data-ttu-id="ebea9-160">範例包括 [**OPENTYPE \_ 功能 \_ 記錄**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)檔中所述的樣式替代功能，或連字號（例如 "fi"），其中單一字元代表兩個或多個連續字元。</span><span class="sxs-lookup"><span data-stu-id="ebea9-160">Examples include the Stylistic Alternates feature described in the documentation of [**OPENTYPE\_FEATURE\_RECORD**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record), or ligatures, such as "ﬁ", where a single glyph represents two or more consecutive characters.</span></span>

 

## <a name="embedding-level"></a><span data-ttu-id="ebea9-161">內嵌層級</span><span class="sxs-lookup"><span data-stu-id="ebea9-161">embedding level</span></span>

<span data-ttu-id="ebea9-162">在 [雙向文字](#bidirectional-text)中，內嵌層級是 [雙向堆疊](#bidirectional-stack)的索引。</span><span class="sxs-lookup"><span data-stu-id="ebea9-162">In [bidirectional text](#bidirectional-text), the embedding level is the index of the [bidirectional stack](#bidirectional-stack).</span></span>

## <a name="font-fallback"></a><span data-ttu-id="ebea9-163">字型 fallback</span><span class="sxs-lookup"><span data-stu-id="ebea9-163">font fallback</span></span>

<span data-ttu-id="ebea9-164">字型回復是在應用程式中使用者所選取的字型以外自動選取字型。</span><span class="sxs-lookup"><span data-stu-id="ebea9-164">Font fallback is automated selection of a font other than the font selected by the user in an application.</span></span> <span data-ttu-id="ebea9-165">在 Uniscribe 中，當所有或部分文字都在使用者選取的字型不支援的腳本中時， [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) 函式會套用字型回復。</span><span class="sxs-lookup"><span data-stu-id="ebea9-165">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span>

## <a name="glyph"></a><span data-ttu-id="ebea9-166">Glyph - 圖像</span><span class="sxs-lookup"><span data-stu-id="ebea9-166">glyph</span></span>

<span data-ttu-id="ebea9-167">圖像是以字型顯示的單一單位。</span><span class="sxs-lookup"><span data-stu-id="ebea9-167">A glyph is a single unit of display in a font.</span></span> <span data-ttu-id="ebea9-168">針對 OpenType，此單位是由外框所定義。</span><span class="sxs-lookup"><span data-stu-id="ebea9-168">For OpenType, this unit is defined by an outline.</span></span> <span data-ttu-id="ebea9-169">針對其他類型的字型，可由點陣圖、一組圖形命令和 like 來定義。</span><span class="sxs-lookup"><span data-stu-id="ebea9-169">For other types of fonts, it can be defined by a bitmap, a set of graphic commands, and the like.</span></span> <span data-ttu-id="ebea9-170">圖像不一定會對應到單一字元。</span><span class="sxs-lookup"><span data-stu-id="ebea9-170">A glyph does not necessarily correspond to a single character.</span></span> <span data-ttu-id="ebea9-171">例如，"fi" 連筆 ( "fi" ) 代表兩個字元 "f" 和 "i"。</span><span class="sxs-lookup"><span data-stu-id="ebea9-171">For example, the "fi" ligature ("ﬁ") represents the two characters "f" and "i".</span></span> <span data-ttu-id="ebea9-172">具有標點符號和波狀符號 ( "ỗ" ) 的越南文小寫 "o" 通常是由多個字元所組成。</span><span class="sxs-lookup"><span data-stu-id="ebea9-172">The Vietnamese lowercase "o" with circumflex and tilde ("ỗ") is typically composed from multiple glyphs.</span></span>

## <a name="item"></a><span data-ttu-id="ebea9-173">item</span><span class="sxs-lookup"><span data-stu-id="ebea9-173">item</span></span>

<span data-ttu-id="ebea9-174">專案具有單一 [腳本](#complex-script) 和方向。</span><span class="sxs-lookup"><span data-stu-id="ebea9-174">An item has a single [script](#complex-script) and direction.</span></span> <span data-ttu-id="ebea9-175">[**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)或 [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)函數可將段落分析為專案。</span><span class="sxs-lookup"><span data-stu-id="ebea9-175">The [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) or [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) function can analyze a paragraph into items.</span></span> <span data-ttu-id="ebea9-176">專案不一定是 [執行](#run)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-176">An item is not necessarily a [run](#run).</span></span> <span data-ttu-id="ebea9-177">它可以包含多個樣式的字元。</span><span class="sxs-lookup"><span data-stu-id="ebea9-177">It can contain characters of multiple styles.</span></span> <span data-ttu-id="ebea9-178">專案和執行資訊必須合併以判斷 [範圍](#range)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-178">Item and run information must be combined to determine [ranges](#range).</span></span>

## <a name="lrm"></a><span data-ttu-id="ebea9-179">LRM</span><span class="sxs-lookup"><span data-stu-id="ebea9-179">LRM</span></span>

<span data-ttu-id="ebea9-180">LRM 指出 (Unicode 程式碼點 U + 200E) 的左到右標記。</span><span class="sxs-lookup"><span data-stu-id="ebea9-180">LRM indicates the LEFT-TO-RIGHT MARK (Unicode code point U+200E).</span></span> <span data-ttu-id="ebea9-181">這個標記會指定在邏輯順序後面遵循的字元應該由左至右轉譯。</span><span class="sxs-lookup"><span data-stu-id="ebea9-181">This mark specifies that characters following it in logical order should be rendered left-to-right.</span></span>

## <a name="ltr"></a><span data-ttu-id="ebea9-182">LTR</span><span class="sxs-lookup"><span data-stu-id="ebea9-182">LTR</span></span>

<span data-ttu-id="ebea9-183">LTR 表示由左到右。</span><span class="sxs-lookup"><span data-stu-id="ebea9-183">LTR indicates left-to-right.</span></span>

## <a name="range"></a><span data-ttu-id="ebea9-184">range</span><span class="sxs-lookup"><span data-stu-id="ebea9-184">range</span></span>

<span data-ttu-id="ebea9-185">範圍是 [執行](#run)的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="ebea9-185">A range is a special case of a [run](#run).</span></span> <span data-ttu-id="ebea9-186">它完全落在一個 [專案](#item)內。</span><span class="sxs-lookup"><span data-stu-id="ebea9-186">It falls entirely within one [item](#item).</span></span> <span data-ttu-id="ebea9-187">因此，如果某個專案被細分為執行，則每個執行都是一個範圍。</span><span class="sxs-lookup"><span data-stu-id="ebea9-187">Thus, if an item is broken into runs, each of those runs is a range.</span></span>

## <a name="rlm"></a><span data-ttu-id="ebea9-188">RLM</span><span class="sxs-lookup"><span data-stu-id="ebea9-188">RLM</span></span>

<span data-ttu-id="ebea9-189">RLM 指出 (Unicode 程式碼點 U + 200F) 的由右至左標記。</span><span class="sxs-lookup"><span data-stu-id="ebea9-189">RLM indicates the RIGHT-TO-LEFT MARK (Unicode code point U+200F).</span></span> <span data-ttu-id="ebea9-190">此標記表示以邏輯順序接在後面的字元應由右至左呈現。</span><span class="sxs-lookup"><span data-stu-id="ebea9-190">This mark indicates that characters following it in logical order should be rendered right-to-left.</span></span>

## <a name="rtl"></a><span data-ttu-id="ebea9-191">RTL</span><span class="sxs-lookup"><span data-stu-id="ebea9-191">RTL</span></span>

<span data-ttu-id="ebea9-192">RTL 表示由右至左。</span><span class="sxs-lookup"><span data-stu-id="ebea9-192">RTL indicates right-to-left.</span></span>

## <a name="run"></a><span data-ttu-id="ebea9-193">執行</span><span class="sxs-lookup"><span data-stu-id="ebea9-193">run</span></span>

<span data-ttu-id="ebea9-194">回合是一段文字，可供 Uniscribe 轉譯。</span><span class="sxs-lookup"><span data-stu-id="ebea9-194">A run is a passage of text for Uniscribe to render.</span></span> <span data-ttu-id="ebea9-195">它應該有單一樣式，也就是字型、大小和色彩，但可以從各種不同的 [腳本](#complex-script)中繪製。</span><span class="sxs-lookup"><span data-stu-id="ebea9-195">It should have a single style, that is, font, size, and color, but can be drawn from a variety of [scripts](#complex-script).</span></span> <span data-ttu-id="ebea9-196">執行可以同時包含由左至右和由右至左的內容。</span><span class="sxs-lookup"><span data-stu-id="ebea9-196">A run can contain both left-to-right and right-to-left content.</span></span>

## <a name="nads"></a><span data-ttu-id="ebea9-197">NADS</span><span class="sxs-lookup"><span data-stu-id="ebea9-197">NADS</span></span>

<span data-ttu-id="ebea9-198">NADS 表示國家/地區數位圖形 (Unicode 代碼點 U + 206E。</span><span class="sxs-lookup"><span data-stu-id="ebea9-198">NADS indicates NATIONAL DIGIT SHAPES (Unicode code point U+206E.</span></span> <span data-ttu-id="ebea9-199">此詞彙指定歐洲數位 (U + 0030 到 U + 0039) 應轉譯為國家/地區數位。</span><span class="sxs-lookup"><span data-stu-id="ebea9-199">The term specifies that European digits (U+0030 through U+0039) should be rendered as national digits.</span></span> <span data-ttu-id="ebea9-200">如需國家/地區數位的進一步討論，請參閱 [數位圖形](digit-shapes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-200">See [Digit Shapes](digit-shapes.md) for further discussion of national digits.</span></span>

## <a name="nods"></a><span data-ttu-id="ebea9-201">點頭</span><span class="sxs-lookup"><span data-stu-id="ebea9-201">NODS</span></span>

<span data-ttu-id="ebea9-202">節點表示名義數位圖形 (Unicode 程式碼點 U + 206F) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-202">NODS indicates NOMINAL DIGIT SHAPES (Unicode code point U+206F).</span></span> <span data-ttu-id="ebea9-203">此詞彙指定歐洲數位 (U + 0030 到 U + 0039) 應正常轉譯，而不是國家/地區數位。</span><span class="sxs-lookup"><span data-stu-id="ebea9-203">The term specifies that European digits (U+0030 through U+0039) should be rendered normally, not as national digits.</span></span>

## <a name="overhang"></a><span data-ttu-id="ebea9-204">過剩</span><span class="sxs-lookup"><span data-stu-id="ebea9-204">overhang</span></span>

<span data-ttu-id="ebea9-205">懸垂是圖像的筆墨一部分，超出圖像的 [前進寬度](#advance-width) 。</span><span class="sxs-lookup"><span data-stu-id="ebea9-205">The overhang is the part of the ink of a glyph that extends beyond the [advance width](#advance-width) of the glyph.</span></span> <span data-ttu-id="ebea9-206">大部分的字元 (例如 "H" ) 沒有任何懸垂，因為任一側邊都有一個空格，可將它們與連續的字元分隔。</span><span class="sxs-lookup"><span data-stu-id="ebea9-206">Most glyphs (such as "H") have no overhang, as there is a little white space on either side to separate them from adjacent glyphs.</span></span> <span data-ttu-id="ebea9-207">具有懸垂的圖像範例是本主題中使用的斜體 "f"，以說明 [ABC 的寬度](#abc-width)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-207">An example of a glyph with overhang is the italic "f" used in this topic to illustrate [ABC width](#abc-width).</span></span> <span data-ttu-id="ebea9-208">斜體 "f" 的頂端和底端都會延伸連續的圖像。</span><span class="sxs-lookup"><span data-stu-id="ebea9-208">Both the top and bottom of the italic "f" overhang the adjacent glyphs.</span></span> <span data-ttu-id="ebea9-209">懸垂會對應至負的 "A" 或 "C" 寬度。</span><span class="sxs-lookup"><span data-stu-id="ebea9-209">Overhang corresponds to a negative "A" or "C" width.</span></span>

## <a name="padding"></a><span data-ttu-id="ebea9-210">填補 (padding)</span><span class="sxs-lookup"><span data-stu-id="ebea9-210">padding</span></span>

<span data-ttu-id="ebea9-211">請參閱 [underhang](#underhang)。</span><span class="sxs-lookup"><span data-stu-id="ebea9-211">See [underhang](#underhang).</span></span>

## <a name="script"></a><span data-ttu-id="ebea9-212">指令碼</span><span class="sxs-lookup"><span data-stu-id="ebea9-212">script</span></span>

<span data-ttu-id="ebea9-213">腳本是撰寫語言的系統，例如，拉丁腳本、阿拉伯文腳本、中文腳本。</span><span class="sxs-lookup"><span data-stu-id="ebea9-213">A script is a system of written language, for example, Latin script, Arabic script, Chinese script.</span></span> <span data-ttu-id="ebea9-214">單一腳本可以套用至一或多個人類語言。</span><span class="sxs-lookup"><span data-stu-id="ebea9-214">A single script can apply to one or many human languages.</span></span> <span data-ttu-id="ebea9-215">腳本與字型沒有特定的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ebea9-215">The script has no particular relation to a font.</span></span> <span data-ttu-id="ebea9-216">例如，您可以透過新的羅馬字元或 Arial 字型，以同樣的方式轉譯拉丁腳本。</span><span class="sxs-lookup"><span data-stu-id="ebea9-216">For example, the Latin script can be rendered equally well by the Times New Roman or the Arial font.</span></span>

## <a name="underhang"></a><span data-ttu-id="ebea9-217">underhang</span><span class="sxs-lookup"><span data-stu-id="ebea9-217">underhang</span></span>

<span data-ttu-id="ebea9-218">Underhang 是字元左邊或右邊的泛空白字元寬度（空白部分）。</span><span class="sxs-lookup"><span data-stu-id="ebea9-218">The underhang is a width of white space to the left or right of the solid portion of a glyph.</span></span> <span data-ttu-id="ebea9-219">Underhang 會對應至正的 "A" 或 "C" 寬度（如 [ABC 寬度](#abc-width)所述）。</span><span class="sxs-lookup"><span data-stu-id="ebea9-219">Underhang corresponds to a positive "A" or "C" width, as described for [ABC width](#abc-width).</span></span> <span data-ttu-id="ebea9-220">Underhang 有時稱為「填補」。</span><span class="sxs-lookup"><span data-stu-id="ebea9-220">Underhang is sometimes known as "padding".</span></span> <span data-ttu-id="ebea9-221">下圖顯示小寫字母 n 的 underhang。</span><span class="sxs-lookup"><span data-stu-id="ebea9-221">The following illustration shows the underhang for the lowercase letter n.</span></span>

![顯示小寫字母 n underhang 的圖例。](images/underhang.gif)

## <a name="related-topics"></a><span data-ttu-id="ebea9-223">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebea9-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebea9-224">關於 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="ebea9-224">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 

---
description: 應用程式可以使用 Unicode 來代表多種形式的字串。
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: 使用 Unicode 正規化來代表字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852956"
---
# <a name="using-unicode-normalization-to-represent-strings"></a><span data-ttu-id="43ffe-103">使用 Unicode 正規化來代表字串</span><span class="sxs-lookup"><span data-stu-id="43ffe-103">Using Unicode Normalization to Represent Strings</span></span>

<span data-ttu-id="43ffe-104">應用程式可以使用 Unicode 來代表多種形式的字串。</span><span class="sxs-lookup"><span data-stu-id="43ffe-104">Applications can use Unicode to represent strings in multiple forms.</span></span> <span data-ttu-id="43ffe-105">當 Unicode 接受成長時（尤其是透過網際網路），這項需求零件出現了了，以消除 Unicode 字串中不重要的差異。</span><span class="sxs-lookup"><span data-stu-id="43ffe-105">As Unicode acceptance has grown, especially via the Internet, the need has arisen to eliminate non-essential differences in Unicode strings.</span></span> <span data-ttu-id="43ffe-106">字元組合的多重表示會使軟體變得複雜，例如，當 Web 服務器回應頁面要求或連結器搜尋程式庫中的特定識別碼時。</span><span class="sxs-lookup"><span data-stu-id="43ffe-106">Multiple representations for a combination of characters complicate software, for example, when a Web server responds to a page request or a linker seeks a particular identifier in a library.</span></span>

> [!Caution]  
> <span data-ttu-id="43ffe-107">不同的 Unicode 字串可能會以視覺化方式呈現，並引發安全性問題。</span><span class="sxs-lookup"><span data-stu-id="43ffe-107">Different Unicode strings can appear to be visually identical, raising security concerns.</span></span> <span data-ttu-id="43ffe-108">如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="43ffe-108">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

<span data-ttu-id="43ffe-109">為了回應這項需求，Unicode 聯盟已定義一個稱為「正規化」的處理常式，它會針對字元的任何對等二進位表示產生一個二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="43ffe-109">In response to this requirement, the Unicode Consortium has defined a process called "normalization," which produces one binary representation for any of the equivalent binary representations of a character.</span></span> <span data-ttu-id="43ffe-110">一旦正規化之後，如果兩個字串具有相同的二進位表示，則它們都是相等的。</span><span class="sxs-lookup"><span data-stu-id="43ffe-110">Once normalized, two strings are equivalent if and only if they have identical binary representations.</span></span> <span data-ttu-id="43ffe-111">正規化會消除某些差異，但會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="43ffe-111">The normalization eliminates some differences but preserves case.</span></span>

<span data-ttu-id="43ffe-112">若要使用 Unicode 正規化，應用程式可以呼叫 [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) 和 [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) 函式，以便將字串重新排列 ACCCORDING 為 Unicode 4.0 TR \# 15。</span><span class="sxs-lookup"><span data-stu-id="43ffe-112">To use Unicode normalization, an application can call the [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) and [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) functions for rearrangement of strings acccording to Unicode 4.0 TR\#15.</span></span> <span data-ttu-id="43ffe-113">正規化有助於藉由減少具有相同語言意義的替代字串表示來改善安全性。</span><span class="sxs-lookup"><span data-stu-id="43ffe-113">Normalization can help improve security by reducing alternate string representations that have the same linguistic meaning.</span></span> <span data-ttu-id="43ffe-114">不過請記住，該正規化無法完全刪除替代表示。</span><span class="sxs-lookup"><span data-stu-id="43ffe-114">Remember, however, that normalization cannot eliminate alternate representations entirely.</span></span>

<span data-ttu-id="43ffe-115">如需正規化 Unicode 標準的詳細說明，請參閱 [Unicode 標準附錄 \# 15： Unicode 正規化表單](https://www.unicode.org/reports/tr15) (UAX \# 15) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-115">For a detailed description of the Unicode standards for normalization, refer to [Unicode Standard Annex \#15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \#15).</span></span>

> [!Caution]  
> <span data-ttu-id="43ffe-116">因為正規化可能會變更字串的形式，所以安全性機制或字元驗證演算法通常應該在正規化之後執行。</span><span class="sxs-lookup"><span data-stu-id="43ffe-116">Because normalization can change the form of a string, security mechanisms or character validation algorithms should usually be implemented after normalization.</span></span> <span data-ttu-id="43ffe-117">如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="43ffe-117">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="provide-multiple-representations-of-the-same-string"></a><span data-ttu-id="43ffe-118">提供相同字串的多個表示</span><span class="sxs-lookup"><span data-stu-id="43ffe-118">Provide Multiple Representations of the Same String</span></span>

<span data-ttu-id="43ffe-119">在許多情況下，Unicode 允許以多個語言表示相同的字串。</span><span class="sxs-lookup"><span data-stu-id="43ffe-119">In many cases, Unicode allows multiple representations of what is, linguistically, the same string.</span></span> <span data-ttu-id="43ffe-120">例如：</span><span class="sxs-lookup"><span data-stu-id="43ffe-120">For example:</span></span>

-   <span data-ttu-id="43ffe-121">具有分字元 (變音符號的大寫 A) 可以表示為單一 Unicode 程式碼點 "Ä" (U + 00C4) 或大寫 A 與結合的分字元字元 ( "A" + "？"，也就是 U + 0041 U + 0308) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-121">Capital A with dieresis (umlaut) can be represented either as a single Unicode code point "Ä" (U+00C4) or the combination of Capital A and the combining Dieresis character ("A" + "¨", that is, U+0041 U+0308).</span></span> <span data-ttu-id="43ffe-122">類似的考慮也適用于許多其他有變音符號的字元。</span><span class="sxs-lookup"><span data-stu-id="43ffe-122">Similar considerations apply for many other characters with diacritic marks.</span></span>
-   <span data-ttu-id="43ffe-123">大寫 A 本身可以用一般方式來表示 (拉丁大寫字母 A、U + 0041) 或以全形拉丁大寫字母 A (U + FF21) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-123">Capital A itself can be represented either in the usual manner (Latin Capital Letter A, U+0041) or by Fullwidth Latin Capital Letter A (U+FF21).</span></span> <span data-ttu-id="43ffe-124">其他簡單的拉丁字母也有類似的考慮， (大寫和小寫) ，以及用來寫入日文的片假名字元。</span><span class="sxs-lookup"><span data-stu-id="43ffe-124">Similar considerations apply for the other simple Latin letters (both uppercase and lowercase) and for the katakana characters used in writing Japanese.</span></span>
-   <span data-ttu-id="43ffe-125">字串 "fi" 可以用字元 "f" 和 "i" (U + 0066 U + 0069) 或連字號 "fi" (U + FB01) 來表示。</span><span class="sxs-lookup"><span data-stu-id="43ffe-125">The string "fi" can be represented either by the characters "f" and "i" (U+0066 U+0069) or by the ligature "ﬁ" (U+FB01).</span></span> <span data-ttu-id="43ffe-126">Unicode 定義連字號的許多其他字元組合也適用類似的考慮。</span><span class="sxs-lookup"><span data-stu-id="43ffe-126">Similar considerations apply for many other combinations of characters for which Unicode defines ligatures.</span></span>

## <a name="use-the-four-defined-normalization-forms"></a><span data-ttu-id="43ffe-127">使用四個已定義的正規化形式</span><span class="sxs-lookup"><span data-stu-id="43ffe-127">Use the Four Defined Normalization Forms</span></span>

<span data-ttu-id="43ffe-128">您的應用程式可以使用數種演算法（稱為「正規化表單」）來執行 Unicode 正規化，而這些演算法會遵守不同的規則。</span><span class="sxs-lookup"><span data-stu-id="43ffe-128">Your applications can perform Unicode normalization using several algorithms, called "normalization forms," that obey different rules.</span></span> <span data-ttu-id="43ffe-129">Unicode 協會已定義四種正規化形式： NFC (表單 C) 、NFD (表單 D) 、NFKC (表單 KC) 和 NFKD (表單 KD) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-129">The Unicode Consortium has defined four normalization forms: NFC (form C), NFD (form D), NFKC (form KC), and NFKD (form KD).</span></span> <span data-ttu-id="43ffe-130">每個表單都會消除一些差異，但會保留大小寫。</span><span class="sxs-lookup"><span data-stu-id="43ffe-130">Each form eliminates some differences but preserves case.</span></span> <span data-ttu-id="43ffe-131">Win32 和 .NET Framework 支援全部四種正規化形式。</span><span class="sxs-lookup"><span data-stu-id="43ffe-131">Win32 and the .NET Framework support all four normalization forms.</span></span>

<span data-ttu-id="43ffe-132">NLS 列舉型別 [**標準 \_ 格式**](/windows/desktop/api/Winnls/ne-winnls-norm_form) 支援四種標準 Unicode 正規化形式。</span><span class="sxs-lookup"><span data-stu-id="43ffe-132">The NLS enumeration type [**NORM\_FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supports the four standard Unicode normalization forms.</span></span> <span data-ttu-id="43ffe-133">表單 C 和 D 提供字串的標準格式。</span><span class="sxs-lookup"><span data-stu-id="43ffe-133">Forms C and D provide canonical forms for strings.</span></span> <span data-ttu-id="43ffe-134">非標準格式的 KC 和 KD 提供進一步的相容性，而且可以顯示表單 C 和 D 中不明顯的特定語義 equivalences。不過，他們會在遺失資訊的同時，通常不應該將其當成標準的儲存字串的方式來使用。</span><span class="sxs-lookup"><span data-stu-id="43ffe-134">Non-canonical forms KC and KD provide further compatibility, and can reveal certain semantic equivalences that are not apparent in forms C and D. However, they do so at the expense of a certain loss of information, and generally should not be used as a canonical way to store strings.</span></span>

<span data-ttu-id="43ffe-135">在兩種標準格式中，表單 C 是「組成」表單，而表單 D 是「已分解」的表單。</span><span class="sxs-lookup"><span data-stu-id="43ffe-135">Of the two canonical forms, form C is a "composed" form and form D is a "decomposed" form.</span></span> <span data-ttu-id="43ffe-136">例如，表單 C 使用單一 Unicode 代碼點 "Ä" (U + 00C4) ，而表單 D 則使用 ( "A" + "？"，也就是 U + 0041 U + 0308) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-136">For example, form C uses the single Unicode code point "Ä" (U+00C4), while form D uses ("A" + "¨", that is U+0041 U+0308).</span></span> <span data-ttu-id="43ffe-137">這些呈現方式相同，因為 "？" (U + 0308) 是合併字元。</span><span class="sxs-lookup"><span data-stu-id="43ffe-137">These render identically, because "¨" (U+0308) is a combining character.</span></span> <span data-ttu-id="43ffe-138">Form D 可以使用任意數目的程式碼點來代表表單 C 所使用的單一程式碼點。</span><span class="sxs-lookup"><span data-stu-id="43ffe-138">Form D can use any number of code points to represent a single code point used by form C.</span></span>

<span data-ttu-id="43ffe-139">如果兩個字串在表單 C 或形式 D 中相同，則在另一個表單中相同。</span><span class="sxs-lookup"><span data-stu-id="43ffe-139">If two strings are identical in either form C or form D, they are identical in the other form.</span></span> <span data-ttu-id="43ffe-140">此外，當正確轉譯時，它們會顯示彼此的 indistinguishably，以及從原始的非正規化字串。</span><span class="sxs-lookup"><span data-stu-id="43ffe-140">Furthermore, when correctly rendered, they display indistinguishably from one another and from the original non-normalized string.</span></span>

<span data-ttu-id="43ffe-141">一旦正規化之後，字串就無法一致地傳回至其原始標記法。</span><span class="sxs-lookup"><span data-stu-id="43ffe-141">Once normalized, strings cannot be consistently returned to their original representation.</span></span> <span data-ttu-id="43ffe-142">例如，如果將組合成組合和分解字元表示的字串轉換成正規化格式，則無法將它解除標準化為原始的混合字串。</span><span class="sxs-lookup"><span data-stu-id="43ffe-142">For example, if a string with a mixture of composed and decomposed character representations is converted to a normalized form, there is no way to un-normalize it to the original mixed string.</span></span> <span data-ttu-id="43ffe-143">因此，如果應用程式需要字串的原始標記法，它必須明確地儲存該標記法。</span><span class="sxs-lookup"><span data-stu-id="43ffe-143">Therefore, if an application requires the original representation of the string, it must store that representation explicitly.</span></span> <span data-ttu-id="43ffe-144">不過，在兩個標準格式之間轉換是可還原的。</span><span class="sxs-lookup"><span data-stu-id="43ffe-144">However, converting between the two canonical forms is reversible.</span></span> <span data-ttu-id="43ffe-145">C 格式的字串可以轉換成 D 格式，然後再轉換成 C 格式，而結果與原始表單 C 字串相同。</span><span class="sxs-lookup"><span data-stu-id="43ffe-145">A string in form C can be converted to form D and then back to form C, and the result is identical to the original form C string.</span></span>

<span data-ttu-id="43ffe-146">Forms KC 和 KD 分別類似表單 C 和 D，但這些「相容性表單」具有與每個字元基本形式的相容字元的額外對應。</span><span class="sxs-lookup"><span data-stu-id="43ffe-146">Forms KC and KD are similar to forms C and D, respectively, but these "compatibility forms" have additional mappings of compatible characters to the basic form of each character.</span></span> <span data-ttu-id="43ffe-147">這類對應可能會造成次要字元的變化遺失。</span><span class="sxs-lookup"><span data-stu-id="43ffe-147">Such mappings can cause minor character variations to be lost.</span></span> <span data-ttu-id="43ffe-148">它們結合了以視覺化方式區分的特定字元。</span><span class="sxs-lookup"><span data-stu-id="43ffe-148">They combine certain characters that are visually distinct.</span></span> <span data-ttu-id="43ffe-149">例如，它們結合了具有相同語義意義的全形和半形字元，或相同阿拉伯文字母的不同形式，或連字號 "fi" (U + FB01) 和字元組 "fi" (U + 0066 U + 0069) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-149">For example, they combine full-width and half-width characters with the same semantic meaning, or different forms of the same Arabic letter, or the ligature "ﬁ" (U+FB01) and the character pair "fi" (U+0066 U+0069).</span></span> <span data-ttu-id="43ffe-150">它們也會結合某些有時可能會有不同語義意義的字元，例如以上標寫的數位、做為注標，或以圓圈括住。</span><span class="sxs-lookup"><span data-stu-id="43ffe-150">They also combine some characters that might sometimes have a different semantic meaning, such as a digit written as a superscript, as a subscript, or enclosed in a circle.</span></span> <span data-ttu-id="43ffe-151">由於這項資訊遺失，表單 KC 和 KD 通常不應該當做標準格式的字串使用，但它們對某些應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="43ffe-151">Because of this information loss, forms KC and KD generally should not be used as canonical forms of strings, but they are useful for certain applications.</span></span>

<span data-ttu-id="43ffe-152">表單 KC 是組成的表單，而表單 KD 是分解的表單。</span><span class="sxs-lookup"><span data-stu-id="43ffe-152">Form KC is a composed form and form KD is a decomposed form.</span></span> <span data-ttu-id="43ffe-153">應用程式可以在表單 KC 與 KD 之間來回移動，但沒有一致的方式可從表單 KC 或 KD 回原始字串，即使原始字串的格式為 C 或 D。</span><span class="sxs-lookup"><span data-stu-id="43ffe-153">The application can go back and forth between forms KC and KD, but there is no consistent way to go from form KC or KD back to the original string, even if the original string is in form C or D.</span></span>

<span data-ttu-id="43ffe-154">Windows、Microsoft 應用程式和 .NET Framework 通常會使用一般的輸入方法，以 C 格式產生字元。</span><span class="sxs-lookup"><span data-stu-id="43ffe-154">Windows, Microsoft applications, and the .NET Framework generally generate characters in form C using normal input methods.</span></span> <span data-ttu-id="43ffe-155">針對大部分的 Windows 用途，表單 C 是慣用的形式。</span><span class="sxs-lookup"><span data-stu-id="43ffe-155">For most purposes on Windows, form C is the preferred form.</span></span> <span data-ttu-id="43ffe-156">例如，C 格式的字元是由 Windows 鍵盤輸入所產生。</span><span class="sxs-lookup"><span data-stu-id="43ffe-156">For example, characters in form C are produced by Windows keyboard input.</span></span> <span data-ttu-id="43ffe-157">不過，從 Web 和其他平臺匯入的字元可能會將其他正規化形式引入資料流程中。</span><span class="sxs-lookup"><span data-stu-id="43ffe-157">However, characters imported from the Web and other platforms can introduce other normalization forms into the data stream.</span></span>

<span data-ttu-id="43ffe-158">下列範例取自 UAX \# 15，並說明四種正規化表單之間的差異。</span><span class="sxs-lookup"><span data-stu-id="43ffe-158">The following examples are drawn from UAX \#15, and illustrate the differences among the four normalization forms.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="43ffe-159">原始</span><span class="sxs-lookup"><span data-stu-id="43ffe-159">Original</span></span></th>
<th><span data-ttu-id="43ffe-160">表單 D</span><span class="sxs-lookup"><span data-stu-id="43ffe-160">Form D</span></span></th>
<th><span data-ttu-id="43ffe-161">表單 C</span><span class="sxs-lookup"><span data-stu-id="43ffe-161">Form C</span></span></th>
<th><span data-ttu-id="43ffe-162">備註</span><span class="sxs-lookup"><span data-stu-id="43ffe-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43ffe-163">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-163">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="43ffe-164">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-164">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="43ffe-165">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-165">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="43ffe-166">Ffi_ligature (U + FB03) 未分解，因為它有相容性對應，而非標準對應。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-166">The ffi_ligature (U+FB03) is not decomposed, because it has a compatibility mapping, not a canonical mapping.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-167">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-167">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="43ffe-168">&quot;A\u0308\uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-168">&quot;A\u0308\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="43ffe-169">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-169">&quot;Ä\uFB03n&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-170">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-170">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="43ffe-171">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-171">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="43ffe-172">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-172">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="43ffe-173">不會分解羅馬數字 IV (U + 2163) 。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-173">The ROMAN NUMERAL IV (U+2163) is not decomposed.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-174">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-174">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="43ffe-175">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-175">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="43ffe-176">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-176">&quot;Henry \u2163&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-177">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-177">ga</span></span></td>
<td><span data-ttu-id="43ffe-178">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-178">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-179">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-179">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="43ffe-180">與單一日文字元不同的相容性，不會產生相同的字串，格式為 C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-180">Different compatibility equivalents of a single Japanese character do not result in the same string in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-181">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-181">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-182">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-182">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-183">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-183">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-184">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-184">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-185">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-185">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-186">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-186">hw_ka +hw_ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-187">ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-187">ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-188">ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-188">ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-189">ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-189">ka +hw_ten</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-190">hw_ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-190">hw_ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-191">hw_ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-191">hw_ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-192">hw_ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-192">hw_ka +ten</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-193">kaks</span><span class="sxs-lookup"><span data-stu-id="43ffe-193">kaks</span></span></td>
<td><span data-ttu-id="43ffe-194">k <sub>i</sub> + a m + ks <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="43ffe-194">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="43ffe-195">kaks</span><span class="sxs-lookup"><span data-stu-id="43ffe-195">kaks</span></span></td>
<td><span data-ttu-id="43ffe-196">韓文音節是在正規化下維護。</span><span class="sxs-lookup"><span data-stu-id="43ffe-196">Hangul syllables are maintained under normalization.</span></span><br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="43ffe-197">原始</span><span class="sxs-lookup"><span data-stu-id="43ffe-197">Original</span></span></th>
<th><span data-ttu-id="43ffe-198">表單 KD</span><span class="sxs-lookup"><span data-stu-id="43ffe-198">Form KD</span></span></th>
<th><span data-ttu-id="43ffe-199">表單 KC</span><span class="sxs-lookup"><span data-stu-id="43ffe-199">Form KC</span></span></th>
<th><span data-ttu-id="43ffe-200">備註</span><span class="sxs-lookup"><span data-stu-id="43ffe-200">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43ffe-201">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-201">&quot;Äffin&quot;</span></span></td>
<td><span data-ttu-id="43ffe-202">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-202">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="43ffe-203">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-203">&quot;Äffin&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="43ffe-204">Ffi_ligature (U + FB03) 是在表單 KC 中分解，但不是在表單 C. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-204">The ffi_ligature (U+FB03) is decomposed in form KC, but not in form C.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-205">&quot;Ä \ uFB03n&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-205">&quot;Ä\uFB03n&quot;</span></span></td>
<td><span data-ttu-id="43ffe-206">&quot;A\u0308ffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-206">&quot;A\u0308ffin&quot;</span></span></td>
<td><span data-ttu-id="43ffe-207">&quot;Äffin&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-207">&quot;Äffin&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-208">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-208">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="43ffe-209">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-209">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="43ffe-210">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-210">&quot;Henry IV&quot;</span></span></td>
<td rowspan="2"><span data-ttu-id="43ffe-211">此處產生的字串在表單 KC 中是相同的。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-211">The resulting strings here are identical in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-212">&quot;Henry \u2163&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-212">&quot;Henry \u2163&quot;</span></span></td>
<td><span data-ttu-id="43ffe-213">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-213">&quot;Henry IV&quot;</span></span></td>
<td><span data-ttu-id="43ffe-214">&quot;Henry IV&quot;</span><span class="sxs-lookup"><span data-stu-id="43ffe-214">&quot;Henry IV&quot;</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-215">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-215">ga</span></span></td>
<td><span data-ttu-id="43ffe-216">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-216">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-217">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-217">ga</span></span></td>
<td rowspan="5"><span data-ttu-id="43ffe-218">與單一日文字元不同的相容性，會導致表單 KC 中的相同字串產生相同的字串。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="43ffe-218">Different compatibility equivalents of a single Japanese character result in the same string in form KC.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-219">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-219">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-220">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-220">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-221">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-221">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-222">hw_ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-222">hw_ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-223">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-223">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-224">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-224">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-225">ka + hw_ten</span><span class="sxs-lookup"><span data-stu-id="43ffe-225">ka +hw_ten</span></span></td>
<td><span data-ttu-id="43ffe-226">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-226">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-227">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-227">ga</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="43ffe-228">hw_ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-228">hw_ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-229">ka + 十</span><span class="sxs-lookup"><span data-stu-id="43ffe-229">ka +ten</span></span></td>
<td><span data-ttu-id="43ffe-230">ga</span><span class="sxs-lookup"><span data-stu-id="43ffe-230">ga</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="43ffe-231">kaks</span><span class="sxs-lookup"><span data-stu-id="43ffe-231">kaks</span></span></td>
<td><span data-ttu-id="43ffe-232">k <sub>i</sub> + a m + ks <sub>f</sub></span><span class="sxs-lookup"><span data-stu-id="43ffe-232">k <sub>i</sub> + a ₘ + ks <sub>f</sub></span></span></td>
<td><span data-ttu-id="43ffe-233">kaks</span><span class="sxs-lookup"><span data-stu-id="43ffe-233">kaks</span></span></td>
<td><span data-ttu-id="43ffe-234">韓文音節是在正規化下維護。</span><span class="sxs-lookup"><span data-stu-id="43ffe-234">Hangul syllables are maintained under normalization.</span></span> <span data-ttu-id="43ffe-235">在舊版的 Unicode 版本中，拼音字母字元（例如，ks <sub>f</sub> ）有 k <sub>f</sub> + s <sub>f</sub>的相容性對應。</span><span class="sxs-lookup"><span data-stu-id="43ffe-235">In earlier Unicode versions, jamo characters like ks <sub>f</sub> had compatibility mappings to k <sub>f</sub> + s <sub>f</sub>.</span></span> <span data-ttu-id="43ffe-236">這些對應已在 Unicode 2.1.9 中移除，以確保會維護韓文音節。</span><span class="sxs-lookup"><span data-stu-id="43ffe-236">These mappings were removed in Unicode 2.1.9 to ensure that Hangul syllables are maintained.</span></span><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="43ffe-237">上述兩個數據表具有© 1998-2006 Unicode，Inc. 的著作權。保留的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="43ffe-237">The two tables above have a copyright of © 1998-2006 Unicode, Inc. All Rights Reserved.</span></span>

 

## <a name="use-composed-forms-for-single-glyphs"></a><span data-ttu-id="43ffe-238">針對單一字元使用組合的表單</span><span class="sxs-lookup"><span data-stu-id="43ffe-238">Use Composed Forms for Single Glyphs</span></span>

<span data-ttu-id="43ffe-239">許多對應到單一圖像的字元序列都沒有組成的表單。</span><span class="sxs-lookup"><span data-stu-id="43ffe-239">Many character sequences that correspond to a single glyph do not have composed forms.</span></span> <span data-ttu-id="43ffe-240">即使以表單 C 進行標準化，單一視覺化圖像或邏輯文字元素也可以由多個 Unicode 程式碼點組成。</span><span class="sxs-lookup"><span data-stu-id="43ffe-240">Even when normalized by form C, a single visual glyph or logical text element can be composed of multiple Unicode code points.</span></span> <span data-ttu-id="43ffe-241">例如，用來書寫立陶宛文的數個字元都有雙音符號，因為它們只會有分解的表單。</span><span class="sxs-lookup"><span data-stu-id="43ffe-241">For example, several characters used in writing Lithuanian have double diacritics, as they have only decomposed forms.</span></span> <span data-ttu-id="43ffe-242">例如，小寫 U 加上時間和波狀符號 ( "ū̃"、U + 016b U + 0303，其中第一個程式碼點是具有長時間的小寫 U，而第二個則是合併銳角的強調式) 。</span><span class="sxs-lookup"><span data-stu-id="43ffe-242">An example is lowercase U with macron and tilde ("ū̃", U+016b U+0303, where the first code point is a lowercase U with macron and the second is a combining acute accent).</span></span>

## <a name="example"></a><span data-ttu-id="43ffe-243">範例</span><span class="sxs-lookup"><span data-stu-id="43ffe-243">Example</span></span>

<span data-ttu-id="43ffe-244">您可以在 [NLS： Unicode 正規化範例](nls--unicode-normalization-sample.md)中找到相關的範例。</span><span class="sxs-lookup"><span data-stu-id="43ffe-244">A relevant example can be found in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43ffe-245">相關主題</span><span class="sxs-lookup"><span data-stu-id="43ffe-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43ffe-246">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="43ffe-246">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="43ffe-247">安全性考慮：國際功能</span><span class="sxs-lookup"><span data-stu-id="43ffe-247">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> <dt>

[<span data-ttu-id="43ffe-248">**IsNormalizedString**</span><span class="sxs-lookup"><span data-stu-id="43ffe-248">**IsNormalizedString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[<span data-ttu-id="43ffe-249">**NormalizeString**</span><span class="sxs-lookup"><span data-stu-id="43ffe-249">**NormalizeString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 





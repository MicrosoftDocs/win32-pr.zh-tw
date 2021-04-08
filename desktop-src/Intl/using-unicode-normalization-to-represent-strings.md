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
# <a name="using-unicode-normalization-to-represent-strings"></a>使用 Unicode 正規化來代表字串

應用程式可以使用 Unicode 來代表多種形式的字串。 當 Unicode 接受成長時（尤其是透過網際網路），這項需求零件出現了了，以消除 Unicode 字串中不重要的差異。 字元組合的多重表示會使軟體變得複雜，例如，當 Web 服務器回應頁面要求或連結器搜尋程式庫中的特定識別碼時。

> [!Caution]  
> 不同的 Unicode 字串可能會以視覺化方式呈現，並引發安全性問題。 如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

為了回應這項需求，Unicode 聯盟已定義一個稱為「正規化」的處理常式，它會針對字元的任何對等二進位表示產生一個二進位標記法。 一旦正規化之後，如果兩個字串具有相同的二進位表示，則它們都是相等的。 正規化會消除某些差異，但會保留大小寫。

若要使用 Unicode 正規化，應用程式可以呼叫 [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) 和 [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) 函式，以便將字串重新排列 ACCCORDING 為 Unicode 4.0 TR \# 15。 正規化有助於藉由減少具有相同語言意義的替代字串表示來改善安全性。 不過請記住，該正規化無法完全刪除替代表示。

如需正規化 Unicode 標準的詳細說明，請參閱 [Unicode 標準附錄 \# 15： Unicode 正規化表單](https://www.unicode.org/reports/tr15) (UAX \# 15) 。

> [!Caution]  
> 因為正規化可能會變更字串的形式，所以安全性機制或字元驗證演算法通常應該在正規化之後執行。 如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

## <a name="provide-multiple-representations-of-the-same-string"></a>提供相同字串的多個表示

在許多情況下，Unicode 允許以多個語言表示相同的字串。 例如：

-   具有分字元 (變音符號的大寫 A) 可以表示為單一 Unicode 程式碼點 "Ä" (U + 00C4) 或大寫 A 與結合的分字元字元 ( "A" + "？"，也就是 U + 0041 U + 0308) 。 類似的考慮也適用于許多其他有變音符號的字元。
-   大寫 A 本身可以用一般方式來表示 (拉丁大寫字母 A、U + 0041) 或以全形拉丁大寫字母 A (U + FF21) 。 其他簡單的拉丁字母也有類似的考慮， (大寫和小寫) ，以及用來寫入日文的片假名字元。
-   字串 "fi" 可以用字元 "f" 和 "i" (U + 0066 U + 0069) 或連字號 "fi" (U + FB01) 來表示。 Unicode 定義連字號的許多其他字元組合也適用類似的考慮。

## <a name="use-the-four-defined-normalization-forms"></a>使用四個已定義的正規化形式

您的應用程式可以使用數種演算法（稱為「正規化表單」）來執行 Unicode 正規化，而這些演算法會遵守不同的規則。 Unicode 協會已定義四種正規化形式： NFC (表單 C) 、NFD (表單 D) 、NFKC (表單 KC) 和 NFKD (表單 KD) 。 每個表單都會消除一些差異，但會保留大小寫。 Win32 和 .NET Framework 支援全部四種正規化形式。

NLS 列舉型別 [**標準 \_ 格式**](/windows/desktop/api/Winnls/ne-winnls-norm_form) 支援四種標準 Unicode 正規化形式。 表單 C 和 D 提供字串的標準格式。 非標準格式的 KC 和 KD 提供進一步的相容性，而且可以顯示表單 C 和 D 中不明顯的特定語義 equivalences。不過，他們會在遺失資訊的同時，通常不應該將其當成標準的儲存字串的方式來使用。

在兩種標準格式中，表單 C 是「組成」表單，而表單 D 是「已分解」的表單。 例如，表單 C 使用單一 Unicode 代碼點 "Ä" (U + 00C4) ，而表單 D 則使用 ( "A" + "？"，也就是 U + 0041 U + 0308) 。 這些呈現方式相同，因為 "？" (U + 0308) 是合併字元。 Form D 可以使用任意數目的程式碼點來代表表單 C 所使用的單一程式碼點。

如果兩個字串在表單 C 或形式 D 中相同，則在另一個表單中相同。 此外，當正確轉譯時，它們會顯示彼此的 indistinguishably，以及從原始的非正規化字串。

一旦正規化之後，字串就無法一致地傳回至其原始標記法。 例如，如果將組合成組合和分解字元表示的字串轉換成正規化格式，則無法將它解除標準化為原始的混合字串。 因此，如果應用程式需要字串的原始標記法，它必須明確地儲存該標記法。 不過，在兩個標準格式之間轉換是可還原的。 C 格式的字串可以轉換成 D 格式，然後再轉換成 C 格式，而結果與原始表單 C 字串相同。

Forms KC 和 KD 分別類似表單 C 和 D，但這些「相容性表單」具有與每個字元基本形式的相容字元的額外對應。 這類對應可能會造成次要字元的變化遺失。 它們結合了以視覺化方式區分的特定字元。 例如，它們結合了具有相同語義意義的全形和半形字元，或相同阿拉伯文字母的不同形式，或連字號 "fi" (U + FB01) 和字元組 "fi" (U + 0066 U + 0069) 。 它們也會結合某些有時可能會有不同語義意義的字元，例如以上標寫的數位、做為注標，或以圓圈括住。 由於這項資訊遺失，表單 KC 和 KD 通常不應該當做標準格式的字串使用，但它們對某些應用程式很有用。

表單 KC 是組成的表單，而表單 KD 是分解的表單。 應用程式可以在表單 KC 與 KD 之間來回移動，但沒有一致的方式可從表單 KC 或 KD 回原始字串，即使原始字串的格式為 C 或 D。

Windows、Microsoft 應用程式和 .NET Framework 通常會使用一般的輸入方法，以 C 格式產生字元。 針對大部分的 Windows 用途，表單 C 是慣用的形式。 例如，C 格式的字元是由 Windows 鍵盤輸入所產生。 不過，從 Web 和其他平臺匯入的字元可能會將其他正規化形式引入資料流程中。

下列範例取自 UAX \# 15，並說明四種正規化表單之間的差異。



<table>
<thead>
<tr class="header">
<th>原始</th>
<th>表單 D</th>
<th>表單 C</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Ffi_ligature (U + FB03) 未分解，因為它有相容性對應，而非標準對應。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">不會分解羅馬數字 IV (U + 2163) 。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka + 十</td>
<td>ga</td>
<td rowspan="5">與單一日文字元不同的相容性，不會產生相同的字串，格式為 C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>ka + 十</td>
<td>ka + 十</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>ka + hw_ten</td>
<td>ka + hw_ten</td>
<td>ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + 十</td>
<td>hw_ka + 十</td>
<td>hw_ka + 十</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>韓文音節是在正規化下維護。<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>原始</th>
<th>表單 KD</th>
<th>表單 KC</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Ffi_ligature (U + FB03) 是在表單 KC 中分解，但不是在表單 C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">此處產生的字串在表單 KC 中是相同的。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka + 十</td>
<td>ga</td>
<td rowspan="5">與單一日文字元不同的相容性，會導致表單 KC 中的相同字串產生相同的字串。 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>ka + 十</td>
<td>ka + 十</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>ka + 十</td>
<td>ga</td>

</tr>
<tr class="even">
<td>ka + hw_ten</td>
<td>ka + 十</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + 十</td>
<td>ka + 十</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>韓文音節是在正規化下維護。 在舊版的 Unicode 版本中，拼音字母字元（例如，ks <sub>f</sub> ）有 k <sub>f</sub> + s <sub>f</sub>的相容性對應。 這些對應已在 Unicode 2.1.9 中移除，以確保會維護韓文音節。<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 上述兩個數據表具有© 1998-2006 Unicode，Inc. 的著作權。保留的擁有權限。

 

## <a name="use-composed-forms-for-single-glyphs"></a>針對單一字元使用組合的表單

許多對應到單一圖像的字元序列都沒有組成的表單。 即使以表單 C 進行標準化，單一視覺化圖像或邏輯文字元素也可以由多個 Unicode 程式碼點組成。 例如，用來書寫立陶宛文的數個字元都有雙音符號，因為它們只會有分解的表單。 例如，小寫 U 加上時間和波狀符號 ( "ū̃"、U + 016b U + 0303，其中第一個程式碼點是具有長時間的小寫 U，而第二個則是合併銳角的強調式) 。

## <a name="example"></a>範例

您可以在 [NLS： Unicode 正規化範例](nls--unicode-normalization-sample.md)中找到相關的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[安全性考慮：國際功能](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 





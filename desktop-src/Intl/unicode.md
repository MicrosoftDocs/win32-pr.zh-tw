---
description: Unicode 是全球字元編碼標準。 系統會專門針對字元和字串操作使用 Unicode。 如需 Unicode 所有方面的詳細說明，請參閱 Unicode 標準。
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99a7af4d4fbb6b7783f97ceba37b1bf6b0bf54811beaf9c7c2348ec0125c73b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764768"
---
# <a name="unicode"></a>Unicode

Unicode 是全球字元編碼標準。 系統會專門針對字元和字串操作使用 Unicode。 如需 Unicode 所有方面的詳細說明，請參閱 [Unicode 標準](https://www.unicode.org/standard/standard.html)。

相較于處理字元和字串資料的舊版機制，Unicode 可簡化軟體當地語系化並改善多語系文字處理。 藉由使用 Unicode 來表示應用程式中的字元和字串資料，您可以為全域行銷啟用通用資料交換功能，並針對每個可能的字元碼使用單一二進位檔案。 Unicode 會執行下列動作：

-   允許任意組合的字元（從腳本和語言的任何組合所繪製），以並存存在於單一檔中。
-   定義每個字元的語法。
-   將腳本行為標準化。
-   提供雙向文字的標準演算法。
-   定義其他標準的跨對應。
-   定義單一字元集的多個編碼： UTF-7、UTF-8、UTF-16 和 UTF-32。 這些編碼之間的資料轉換不會失真。

Unicode 支援許多語言所使用的腳本，以及用於發佈的許多技術符號和特殊字元。 支援的腳本包括（但不限於）拉丁文、希臘文、斯拉夫文、希伯來文、阿拉伯文、梵文、泰文、漢字、韓文、平假名和片假名。 支援的語言包括（但不限於）德文、法文、英文、希臘文、俄文、希伯來文、阿拉伯文、印度文、泰文、繁體中文、韓文及日文。 Unicode 目前可代表現代電腦在世界各地使用的大部分字元，並持續更新以使其更完整。

[函數原型的慣例](conventions-for-function-prototypes.md)中描述了啟用 Unicode 的函式。 這些函式使用 utf-16 (寬字元) 編碼，這是 Unicode 的最常見編碼方式，以及用於 Windows 作業系統上的原生 Unicode 編碼的編碼方式。 每個程式碼值都是16位寬，相較于較舊的 [字碼頁](code-pages.md) 方法和字元和字串資料，其使用8位的程式碼值。 使用16位可允許65536個字元的直接編碼。 事實上，用來轉譯人類語言的符號 universe 甚至更大，而範圍 U + D800 到 U + DFFF 的 UTF-16 程式碼點則是用來形成代理程式配對，其中構成了32位的補充字元編碼。 如需進一步討論，請參閱 [代理程式和補充字元](surrogates-and-supplementary-characters.md) 。

Unicode 字元集包含許多合併字元，例如 U + 0308 ( "$" ) ，結合分字元或變音符號。 Unicode 通常可以在「組成」或「已分解的」表單中代表相同的圖像：例如，「Ä」組成的形式是單一 Unicode 代碼點 "Ä" (U + 00C4) ，而其分解形式為 "A" + "？" (U + 0041 U + 0308) 。 Unicode 不會為每個圖像定義組成的表單。 例如，以標點符號和波狀符號 ( "ỗ" ) 的越南小寫 "o" 是由 U + 006f U + 0302 U + 0303 (o + 揚揚號 + 波狀符號) 來表示。 如需合併字元和相關問題的進一步討論，請參閱 [使用 Unicode 正規化來代表字串](using-unicode-normalization-to-represent-strings.md)。

為了與8位和7位環境相容，Unicode 也可以分別編碼為 UTF-8 和 UTF-7。 雖然 Windows 中支援 Unicode 的函式會使用 utf-16，但是也可以使用以 utf-8 或 utf-7 編碼的資料，這些資料在 Windows 中支援為多位元組字元集[字碼頁](code-pages.md)。

新的 Windows 應用程式應該使用 utf-16 作為其內部資料表示。 Windows 也提供對字碼頁的廣泛支援，而且可以在相同的應用程式中使用混合用途。 即使是新的 Unicode 應用程式，有時還是必須使用字碼頁。 這種情況的原因將在 [字碼頁](code-pages.md)中討論。

應用程式可以使用 [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，根據字碼頁和 Unicode 字串在字串之間進行轉換。 雖然它們的名稱是指「多位元組」，但這些函式同樣適用于 [單一位元組字元集](single-byte-character-sets.md) (SBCS) 、 [雙位元組字元集](double-byte-character-sets.md) (DBCS) 和多位元組字元集 (MBCS) 字碼頁。

一般來說，Windows 應用程式應該在內部使用 utf-16，只在必須使用其他格式的介面上，轉換成「精簡層」的一部分。 這項技術會防範資料遺失和損毀。 每個字碼頁都支援不同的字元，但不支援 Unicode 提供的完整字元範圍。 大部分的字碼頁支援不同的子集，以不同方式編碼。 UTF-8 和 UTF-7 的字碼頁是例外狀況，因為它們支援完整的 Unicode 字元集，而且這些編碼和 UTF-16 之間的轉換不會失真。

直接從某個字碼頁使用的編碼轉換成另一個字碼頁所使用的編碼的資料會受到損毀，因為不同字碼頁上的相同資料值可以編碼不同的字元。 即使您的應用程式盡可能地轉換為靠近介面，您也應該仔細考慮要處理的資料範圍。

從 Unicode 轉換成字碼頁的資料會受到資料遺失的影響，因為指定的字碼頁可能無法表示該特定 Unicode 資料中使用的每個字元。 因此，請注意，如果目標字碼頁無法代表 Unicode 字串中的所有字元， [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) 可能會遺失一些資料。

現代化以字碼頁為基礎的繼承應用程式使用 Unicode 時，您可以使用泛型函式和 [**文字**](/windows/win32/api/Winnt/nf-winnt-text) 宏來維護一組來源，以從中編譯應用程式的兩個版本。 其中一個版本支援 Unicode，另一個版本則適用于 Windows 字碼頁。 您可以使用這項機制，將大型的應用程式從 Windows 字碼頁轉換成 Unicode，同時維護可在轉換的所有階段進行編譯、建立和測試的應用程式來源。 如需詳細資訊，請參閱 [函數原型的慣例](conventions-for-function-prototypes.md)。

Unicode 字元和字串會使用與以字碼頁為基礎的字元和字串不同的資料類型。 除了一系列的宏和命名慣例之外，這項區別也可將不小心混用兩種字元資料類型的機率降到最低。 它會協助編譯器類型檢查，以確保只有 Unicode 參數值會搭配需要 Unicode 字串的函式使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字元集](character-sets.md)
</dt> <dt>

[排序](sorting.md)
</dt> <dt>

[代理和補充字元](surrogates-and-supplementary-characters.md)
</dt> <dt>

[使用 Unicode 正規化來代表字串](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 




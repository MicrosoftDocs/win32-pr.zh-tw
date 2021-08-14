---
description: 有幾個字型和文字輸出函數具有指定文字輸出字串長度的參數。 典型的範例是 DrawTextEx 的 cchText 參數。
ms.assetid: 695fd0f9-abd4-4666-acad-2c409624ddc6
title: 指定文字輸出字串的長度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35a673a23a310da33536f389c85a44af68b895e4f05e0a0f835656e7bc3fbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885946"
---
# <a name="specifying-length-of-text-output-string"></a>指定文字輸出字串的長度

有幾個字型和文字輸出函數具有指定文字輸出字串長度的參數。 典型的範例是 [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)的 *cchText* 參數。

這些函式中的每一個都有 "ANSI" 版本和 Unicode 版本 (例如， [**DrawTextExA**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa) 和 **DrawTextExW** 分別) 。 針對每個函式的「ANSI」版本，長度會指定為位元組計數，而 Unicode 函數則會指定為文字計數。

傳統的是將此視為「字元計數」。 這對許多語言（包括英文）來說通常是正確的，但一般並不精確。 在 "ANSI" 字串中， [SBCS](../intl/single-byte-character-sets.md) 字碼頁中的字元各採用一個位元組，但 [DBCS](../intl/double-byte-character-sets.md) 字碼頁中的大部分字元都需要兩個位元組。 同樣地，大部分的目前定義的 Unicode 字元都位於基本多語系平面中 (BMP) 和其 UTF-16 標記法符合一個單字，但增補字元是以 Unicode 表示（需要兩個字組）。

這些函式中的每一個都採用長度計數。 針對每個函式的 "ANSI" 版本，長度會指定為字串的位元組計數長度，而不包含 **Null** 結束字元。 針對 Unicode 函式，長度計數是位元組計數除以 sizeof (WCHAR) ，也就是2，不包括 **Null** 結束字元。 字元計數是字元數的計數，可能不等於字串的長度計數。 在某些情況下，ANSI 的字元會採用一個以上的位元組 (例如， [DBCS](../intl/double-byte-character-sets.md) 字元) 以及 Unicode (一個以上的字組，例如) 的代理字元。 此外，圖像的數目可能不等於字元數，因為可能會有多個字元組成一個字元。 長度計數是資料量。 字元計數是以一個實體處理的單位數目。 圖像是呈現的內容。 例如，在 Unicode 中，您可以有長度為3的字串，也就是2個字元，而且會轉譯1個圖像。 不過，通常大部分的 Unicode 字串長度、字元計數和轉譯的圖像數目都相等。

您可以使用 \_ tcslen () 取得字串長度。 若是 ANSI， \_ tcslen () 會傳回位元組數目。 若是 Unicode， \_ tcslen () 會傳回 (WCHARs 的數目，也就是) 的單字。

不一定會繪製的特殊處理字元（例如定位字元和軟連字號）可能會影響繪製的輸出。 它們會包含在字串長度和字元計數中，但可能不會直接以轉譯的圖像表示。

這些函式的部分可讓呼叫者將長度指定為-1，以表示字串以 null 結束;在此情況下，函式會自動計算字元計數。 並非所有函數都提供這項功能。 這是以函式為基礎指定的：請參閱個別的函數檔。

 

 

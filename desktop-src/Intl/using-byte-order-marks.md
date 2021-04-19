---
description: 一律在 Unicode 純文字檔前面加上位元組順序標記，這會通知應用程式接收檔案的位元組順序。
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: 使用位元組順序標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000199"
---
# <a name="using-byte-order-marks"></a>使用位元組順序標記

一律在 Unicode 純文字檔前面加上位元組順序標記，這會通知應用程式接收檔案的位元組順序。 下表列出可用的位元組順序標記。 因為 Unicode 純文字是16位程式碼值的序列，所以它會區分寫入文字時使用的位元組順序。

> [!Note]  
> 位元組順序標記不是選取文字位元組順序的控制字元。

 



| 位元組順序符號 | Description           |
|-----------------|-----------------------|
| EF BB BF        | UTF-8                 |
| FF FE           | UTF-16、位元組由小到大 |
| FE FF           | UTF-16、big endian    |
| FF FE 00 00     | UTF-32，位元組由小到大 |
| 00 00 FE FF     | 32 UTF-8、位元組由大到小    |



 

> [!Note]  
> Microsoft 使用 UTF-16、位元組由小到小的位元組順序。

 

在理想的情況下，所有 Unicode 文字只會遵循一組位元組順序規則。 不過，這並不可行，因為微處理器在放置最不重要的位元組時，會有所不同。 Intel 和 MIPS 處理器會先定位最不重要的位元組，而 Motorola 處理器 (和所有位元組反向的 Unicode 檔案) 定位到最後一個位置。 只有一組位元組順序規則，每次讀取或寫入純文字檔時，一種類型的微處理器的使用者都會強制交換位元組順序，即使檔案永遠不會根據不同的微處理器傳送到另一個作業系統。

指定位元組順序的慣用位置是在檔案標頭中，但是文字檔沒有標頭。 因此，Unicode 已定義字元 (U + FEFF) ，而非字元 (U + FFFE) 為位元組順序標記。 它們是彼此的鏡像位元組影像。

由於序列 U + FEFF 在一般非 Unicode 文字檔的開頭非常罕見，因此可以作為隱含標記或簽章，以將檔案識別為 Unicode 檔案。 同時讀取 Unicode 和非 Unicode 文字檔的應用程式應該使用此順序的存在，作為檔案最可能是 Unicode 檔案的指標。 比較這項技術與使用 MS-DOS EOF 標記來終止文字檔。

當應用程式在文字檔的開頭找到 U + FEFF 時，它通常會將檔案處理為 Unicode 檔案，但它可以執行進一步的啟發式檢查以進行驗證。 這樣的檢查可以像測試一樣簡單，找出低序位位元組的變化是否遠高於高序位位元組的變化。 例如，如果 ASCII 文字轉換成 Unicode 文字，則每秒的位元組都是0。 此外，同時檢查換行字元和換行字元 (U + 000A 和 U + 000D) ，甚至或奇數檔案大小，都可以提供檔案本質的強式指標。

當應用程式在文字檔的開頭找到 U + FFFE 時，它會將它解讀為表示檔案是位元組反轉的 Unicode 檔案。 應用程式可以交換位元組的順序，或警示使用者發生錯誤。

因為在任何字碼頁中找不到 Unicode 位元組順序標記字元，所以如果資料轉換成 ANSI，它就會消失。 不同于其他 Unicode 字元，轉換時不會以預設字元取代。 如果在檔案中間找到位元組順序標記，則不會將它視為 Unicode 字元，而且對文字輸出沒有任何影響。

> [!Note]  
> Unicode 值 U + FFFF 在純文字檔中是不合法的，而且無法在應用程式之間傳遞。 它是保留供私用應用程式使用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 中的特殊字元](using-special-characters-in-unicode.md)
</dt> </dl>

 

 




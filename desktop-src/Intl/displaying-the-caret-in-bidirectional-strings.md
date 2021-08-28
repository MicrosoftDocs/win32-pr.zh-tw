---
description: 在單向文字中，插入號位置沒有任何明確的原因，因為字元的開頭邊緣與上一個字元的尾端邊緣位於相同的位置。
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: 以雙向字串顯示插入號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a2e4c9fa06a45b4c653b76395854ee37e0dfdb6f555926987ab4f1a4decb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328798"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>以雙向字串顯示插入號

在單向文字中，插入號位置沒有任何明確的原因，因為字元的開頭邊緣與上一個字元的尾端邊緣位於相同的位置。 不過，在雙向文字中，相反方向的執行插入號位置不明確。 例如，在從左至右的段落 "hellosalaam" 中，"hello" 的最後一個字母會緊接在 "salaam" 的第一個字母之前。 要在其中顯示插入號的最佳位置，取決於是否要將它視為緊接在 "hello" 的 "o" 或 "salaam" 的 "s" 之前。

Uniscribe 會使用下表所示的插入號定位慣例。



| 情況       | 視覺插入號放置                       |
|-----------------|----------------------------------------------|
| 輸入          | 最後一個輸入字元的尾端邊緣。       |
| 粘貼         | 貼上最後一個字元的尾端邊緣。      |
| 插入號前移 | 最後一個傳遞的字元的尾端邊緣。 |
| 插入號淘汰  | 最後一個傳遞的字元開頭緣。  |
| 首頁            | 直線的開頭緣。                        |
| 結束             | 行的尾端邊緣。                       |



 

插入號可以定位，如下列範例所示：


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



如果 *fAdvancing* 值限制為 **TRUE** 或 **FALSE**，插入號的位置可能更簡單（如下所示）：


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) 會以邏輯方式處理超出範圍的位置。 它會傳回 *iCharPos* 執行的開頭緣 <0，以及 *iCharPos* >= length 回合的尾端邊緣。 如需詳細資訊，請參閱 [管理插入點放置和點擊測試](managing-caret-placement-and-hit-testing.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




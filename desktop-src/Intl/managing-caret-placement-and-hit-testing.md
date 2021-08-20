---
description: 複雜的指令碼語言會依 ScriptShape 分割成叢集。 字元重新排列一律會出現在叢集界限內。 叢集本身保證會以讀取順序的方向前進。
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: 管理插入號放置和點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e1c6d3b9dbd54f3df2b458a3f7473d1021dceafd6772730b8482b06c4e1c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788398"
---
# <a name="managing-caret-placement-and-hit-testing"></a>管理插入號放置和點擊測試

複雜的指令碼語言會依 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)[分割成](uniscribe-glossary.md)叢集。 字元重新排列一律會出現在叢集界限內。 叢集本身保證會以讀取順序的方向前進。

邏輯群集陣列中的叢集資訊是用來在它們所代表的邏輯字元之間，平均共用圖像的群集寬度。 例如，有四個區域可以分為四個區域：

-   Lam 的上半部。
-   Lam 的尾端半部。
-   後半的 alef。
-   Alef 的尾端半部。

在叢集內放置插入號的慣例取決於腳本。 若是阿拉伯文腳本，如果在基底字元與其組合標記之間設定插入號位置，插入號會顯示在基底字元的中間。 若為泰文腳本，插入號不能放在叢集內。 因此，當使用者將插入號前移時，應用程式必須提前超過組成叢集的所有字元。

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)和 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)函式會轉譯 (于程式碼點位移) 和 x 位置 (以圖元) 表示的插入號位置。 **ScriptXtoCP** 函式知道每個腳本的插入號位置慣例：

-   針對印度和泰文，插入號位置會貼齊至叢集界限。
-   若是阿拉伯文，插入號位置會與叢集插補。
-   若為希伯來文，在 1.420 Usp10.dll 之前的版本中，會將插入號的位置插上叢集。 從 Usp10.dll 開始，1.420 版，插入號位置會貼齊至叢集界限。

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)和 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)只會在執行內運作。 這些函式需要某些參數來自先前的 Uniscribe 呼叫，如下表所示。



| 參數                                        | 來源                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *Psa*                                            | [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)所傳回的。 |
| *cGlyphspwLogClust*<br/> *psva*<br/> | [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)所傳回的。     |
| *piAdvance*                                      | [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)所傳回的。     |



 

應用程式必須在將資訊傳遞至 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) 或 [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)之前，建立指定的插入號位移或 x 位置的執行。 如果應用程式未儲存寬度資訊，它可以在顯示每次執行之後，執行點擊測試和插入號放置。 或者，應用程式可以快取足夠的資訊，以便在目前的行上進行點擊測試和插入號放置，而不需要重新處理段落。

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 會傳回尾端的邊緣值，讓應用程式知道使用者已按下的字元或叢集的側邊。 在程式碼點中，此值為0或字元或叢集的寬度。 傳回的字元位置是使用者按一下的字元位置。 如需詳細資訊，請參閱 [以雙向字串顯示插入](displaying-the-caret-in-bidirectional-strings.md)號。

若為泰文之類的語言，如果使用者不想將插入號放入叢集中， [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 會將尾端的側旗標設為0或叢集寬度。 若是阿拉伯文等語言，使用者預期能夠在叢集中進行編輯， **ScriptXtoCP** 會將尾端的側旗標設定為0或1。

為了協助應用程式在處理箭號鍵時建立插入號的有效位置，Uniscribe 會在 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)所傳回的邏輯屬性中，提供 **fCharStop** 成員中有效插入號位置的相關資訊。 針對大部分的字元，會傳回 **TRUE** ，而在像是泰文的腳本中，intercluster 字元則傳回 **FALSE** 。 應用程式應該檢查項目的 [**腳本 \_ 屬性**](/windows/desktop/api/Usp10/ns-usp10-script_properties)結構中的 **fNeedsCaretInfo** 值，以查看是否需要呼叫 **ScriptBreak** 來檢查有效的插入號位置。 如果 **fNeedsCaretInfo** 值為 **FALSE**，則所有的程式碼點都是有效的插入號位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 





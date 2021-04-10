---
description: 為了提供文字對齊，應用程式可以使用兩種方法的其中一種。
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: 處理複雜的腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bea5b75e87afc4177b03c03f4263ba2592a0e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026179"
---
# <a name="processing-complex-scripts"></a>處理複雜的腳本

為了提供文字對齊，應用程式可以使用兩種方法的其中一種。 為了簡單執行多語系的理由，應用程式應該呼叫 [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)。 它會藉由考慮 kashida、interword 間距及 intercharacter 間距來產生 delta dx 陣列。 為了更精密的理由，應用程式可以使用自己的語言知識，以及 [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)陣列中 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)抓取的資訊，來產生更新的 delta dx 陣列。

應該插入對齊空間或 kashida，在 [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)的 **uJustification** 成員所識別的位置。 執行字元間對齊時，應用程式應該只在標記有腳本對齊字元的字元之後插入額外的空間 \_ \_ 。

應用程式會使用 [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) 和 [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)進行插入號放置和點擊測試。 如需詳細資訊，請參閱 [管理插入點放置和點擊測試](managing-caret-placement-and-hit-testing.md)。

若要以與字型無關的方式取得寬度，應用程式會呼叫 [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)。 藉由將邏輯寬度傳遞給 [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)，即使原始字型無法使用，也可以在相同的界限內重新顯示一段文字，但仍可接受品質的損失。 它會產生字元寬度的陣列 ([進寬度](uniscribe-glossary.md)) 適合傳遞至 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)。 以與字型無關的方式錄製和重新套用前進寬度資訊，會在以應用程式定義格式 metafiling 的情況下很有用。

> [!Note]  
> 中繼檔不支援圖像索引。 若要寫入至增強型中繼檔，應用程式應該使用 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 並直接寫入邏輯字元。 使用這種機制，在播放文字之前，不會發生圖像產生和放置。

 

若要針對目前的字型取出預設、空白、kashida 等所使用的特定圖像，應用程式應該呼叫 [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)。 為了判斷選取的字型支援執行中的哪些字元，應用程式會呼叫 [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)。 無法使用的字元在圖像緩衝區中會有預設的圖像。 請注意，如果字型轉譯的字元是使用字元的組合而非單一圖像，則這個方法會失敗。 例如，00C9;您可以使用大寫 E 字元和銳角圖像來轉譯具有銳角的拉丁大寫字母 E。 若要判斷包含這類程式碼點之字串的字型支援，應用程式可以呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)。 如需詳細資訊，請參閱 [使用成形引擎](using-shaping-engines.md)。

[**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)函式會從字型快取傳回字型的高度。 [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) 提供所有腳本所需之特殊處理的相關資訊，以腳本編制索引。 例如，它包含與腳本相關聯的主要語言、指出腳本是否為數值的資料，以及指出腳本是否為複雜字集的資料。

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) 會傳回指定圖像的 [ABC 寬度](uniscribe-glossary.md) ，這對繪製圖像圖表可能很有用。 不過，它不應該用於一般複雜的腳本文字格式。

## <a name="related-topics"></a>[相關主題]

[使用 Uniscribe](using-uniscribe.md)


 

 

---
description: 複雜字集是腳本屬性的 fComplex 成員 \_ 設為 TRUE 的腳本。 本主題詳細說明複雜字集可能具有的屬性。
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: 關於複雜字集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e865b7638419178e3339169e56e8ceb111bcc65b925d9c337b5b71d0341827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520648"
---
# <a name="about-complex-scripts"></a>關於複雜字集

[複雜字集](uniscribe-glossary.md)是腳本 [**\_ 屬性**](/windows/desktop/api/Usp10/ns-usp10-script_properties)的 **fComplex** 成員設為 **TRUE** 的腳本。 本主題詳細說明複雜字集可能具有的屬性。

## <a name="bidirectional-rendering"></a>雙向轉譯

雙向轉譯會處理從左至右和由右至左讀取的文字。 例如，在阿拉伯文的雙向轉譯中，文字的預設讀取方向是由右至左，但某些數位的預設讀取方向是由左至右。 處理複雜的腳本必須考慮邏輯 (按鍵) 順序和圖像視覺效果順序之間的差異。 此外，處理必須正確處理插入號移動和點擊測試。 畫面位置和字元索引之間的對應需要瞭解特定顯示器的版面配置演算法，例如選取的文字或插入號顯示。

## <a name="contextual-shaping"></a>內容塑造

在內容成形中，腳本字元會根據周圍的字元來變更圖形。 當小寫的 "l" 變更圖形（視其前面的字元而定，例如 "a" (連接較低至 "l" ) 或 "o" (連接高) 時，就會在英文中撰寫這類成形。 例如，阿拉伯文是展示內容成形的腳本。

## <a name="combining-characters"></a>合併字元

合併字元（也稱為「連字號」）是將字元放在一起時，會加入一個字元的字元。 阿拉伯文是具有許多合併字元的腳本。 使用合併字元的其中一個範例是 "a"，後面接著「組合重音符號」，其呈現的標記法為 "à"。 Unicode 資料流程 "U + 0061 U + 0300" 需要進行一些處理，以確保「組合的抑音符號」正確定位在 "a" 的上方。

## <a name="specialized-word-break-and-justification"></a>特製化斷詞和對齊方式

某些腳本（例如，泰文）有複雜的規則，可將文字行之間的單字分隔，或線上條上對齊文字。

## <a name="filtering-for-illegal-character-combinations"></a>篩選不合法的字元組合

例如，當語言不允許某些字元組合時，複雜的腳本（例如，泰文）可以篩選出不合法的字元組合。

## <a name="font-fallback"></a>字型 Fallback

字型回復是除了使用者選取的字型之外，自動選取字型。 在 Uniscribe 中，當所有或部分文字都在使用者選取的字型不支援的腳本中時， [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) 函式會套用字型回復。 如需詳細資訊，請參閱 [使用字型](using-font-fallback.md)回復。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 




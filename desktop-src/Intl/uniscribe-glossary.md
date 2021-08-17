---
description: ABC 寬度是由 GDI ABC 結構所定義的複合值。 結構包含 abcA、abcB 和 abcC 的成員，對應于 &\# 0034;A&\# 0034;，&\# 0034;B&\# 0034; 和 &\# 0034;C&\# 0034; 圖像或執行的寬度。
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Uniscribe 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146965"
---
# <a name="uniscribe-glossary"></a>Uniscribe 詞彙

ABC 寬度是由 GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) 結構所定義的複合值。 結構包含 **abcA**、 **abcB** 和 **abcC** 的成員，對應至圖像的 "A"、"B" 和 "C"[寬度或](#glyph)[執行](#run)。

"A" 寬度是 [underhang](#underhang) (正數;也稱為「填補」 ) 或 [懸垂](#overhang) (在代表圖像或執行之筆墨的螢幕上對等的負面) 。 「B」寬度是黑色寬度，從最左邊的筆墨到最右邊的筆墨寬度。 "C" 寬度是筆墨右邊的懸垂。

下圖顯示斜體小寫 F，其左邊和右邊都有懸垂。 也就是說，此處的 "A" 和 "C" 寬度皆為負數。 如需正面「A」和「C」寬度的圖例，請參閱 [underhang](#underhang) 。

![圖例顯示斜體小寫 F，其左邊和右邊都有懸垂。](images/abcwidth.gif)

當兩個或更多的字元顯示為一個單位時，通常只有最左邊的字元會提供給回合的「A」寬度，且最右邊的字元會成為執行的「C」寬度。 不過，這並不是嚴格的規則。 例如，如果執行中的第一個圖像是窄字母，而第二個字元是寬的變音符號，並以個別的字元來處理，則變音符號可能會實際延伸超過字母。

## <a name="abc-width"></a>ABC 寬度

ABC 寬度是由 GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) 結構所定義的複合值。 結構包含 **abcA**、 **abcB** 和 **abcC** 的成員，對應至圖像的 "A"、"B" 和 "C"[寬度或](#glyph)[執行](#run)。

"A" 寬度是 [underhang](#underhang) (正數;也稱為「填補」 ) 或 [懸垂](#overhang) (在代表圖像或執行之筆墨的螢幕上對等的負面) 。 「B」寬度是黑色寬度，從最左邊的筆墨到最右邊的筆墨寬度。 "C" 寬度是筆墨右邊的懸垂。

下圖顯示斜體小寫 F，其左邊和右邊都有懸垂。 也就是說，此處的 "A" 和 "C" 寬度皆為負數。 如需正面「A」和「C」寬度的圖例，請參閱 [underhang](#underhang) 。

![圖例顯示斜體小寫 F，其左邊和右邊都有懸垂。](images/abcwidth.gif)

當兩個或更多的字元顯示為一個單位時，通常只有最左邊的字元會提供給回合的「A」寬度，且最右邊的字元會成為執行的「C」寬度。 不過，這並不是嚴格的規則。 例如，如果執行中的第一個圖像是窄字母，而第二個字元是寬的變音符號，並以個別的字元來處理，則變音符號可能會實際延伸超過字母。

## <a name="advance-width"></a>前進寬度

圖像的前進寬度是從起點開始的方向 [移動，以便](#glyph) 將該圖像轉譯成起點以轉譯下一個圖像。

## <a name="bidirectional-stack"></a>雙向堆疊

雙向堆疊是5位整數，可追蹤從左至右和由右至左的文字之間的嵌套層級。 從左至右，一律從零開始。 因此，所有偶數值都代表由左至右的文字，而且所有奇數值都代表由右至左的文字。 雙向堆疊會以 [**腳本 \_ 狀態**](/windows/win32/api/usp10/ns-usp10-script_state)結構的 **uBidiLevel** 成員表示。

## <a name="bidirectional-text"></a>雙向文字

雙向文字包含由左至右和由右至左的部分，但有時也會鬆散地套用到純由右至左的文字。 所有由右至左的文字都需要使用 [雙向堆疊](#bidirectional-stack)，因為預設的內嵌 [層級](#embedding-level) 為零表示由左至右的文字。

## <a name="cell-width"></a>儲存格寬度

應用程式可以藉由調整特定字元的儲存格寬度，來調整文字以符合線條。 若為對齊文字，圖像的資料格寬度與其 [前進寬度](#advance-width)相同。

## <a name="cluster"></a>叢集

群集是可塑造的最小語言單位。 在阿拉伯文和許多印度文等語言中，用來代表每個字元的字元 (Unicode 程式碼點) 會依賴于構成叢集的周圍程式碼點。 在這些語言中，應用程式只能藉由查看叢集，將程式碼點轉譯為適當的字元。 在某些腳本中，例如梵文，在叢集中的字元順序可能會與相對應的 Unicode 程式碼點順序不同。 如需詳細資訊，請參閱 Microsoft 印刷樣式網站上的[Windows 影像處理](/typography/develop/processing-part1)。

## <a name="complex-script"></a>複雜字集

複雜字集是具有下列任何屬性的 [腳本](#complex-script) ：

-   允許雙向轉譯。
-   有內容成形。
-   有組合字元。
-   具有特製化的斷詞和理由規則。
-   篩選出不合法的字元組合。
-   不支援核心 Windows 字型，因此可能需要[字型](#font-fallback)回復。

在某些複雜的腳本中，圖像的順序可能與它們所代表之基礎 Unicode 字元的順序相當不同。 如需詳細資訊，請參閱 [關於複雜字集](about-complex-scripts.md) 。

> [!Note]  
> 在印刷環境中，有時需要處理用來撰寫英文做為複雜字集的拉丁腳本。 範例包括 [**OPENTYPE \_ 功能 \_ 記錄**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)檔中所述的樣式替代功能，或連字號（例如 "fi"），其中單一字元代表兩個或多個連續字元。

 

## <a name="embedding-level"></a>內嵌層級

在 [雙向文字](#bidirectional-text)中，內嵌層級是 [雙向堆疊](#bidirectional-stack)的索引。

## <a name="font-fallback"></a>字型 fallback

字型回復是在應用程式中使用者所選取的字型以外自動選取字型。 在 Uniscribe 中，當所有或部分文字都在使用者選取的字型不支援的腳本中時， [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) 函式會套用字型回復。

## <a name="glyph"></a>Glyph - 圖像

圖像是以字型顯示的單一單位。 針對 OpenType，此單位是由外框所定義。 針對其他類型的字型，可由點陣圖、一組圖形命令和 like 來定義。 圖像不一定會對應到單一字元。 例如，"fi" 連筆 ( "fi" ) 代表兩個字元 "f" 和 "i"。 具有標點符號和波狀符號 ( "ỗ" ) 的越南文小寫 "o" 通常是由多個字元所組成。

## <a name="item"></a>item

專案具有單一 [腳本](#complex-script) 和方向。 [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)或 [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)函數可將段落分析為專案。 專案不一定是 [執行](#run)。 它可以包含多個樣式的字元。 專案和執行資訊必須合併以判斷 [範圍](#range)。

## <a name="lrm"></a>LRM

LRM 指出 (Unicode 程式碼點 U + 200E) 的左到右標記。 這個標記會指定在邏輯順序後面遵循的字元應該由左至右轉譯。

## <a name="ltr"></a>LTR

LTR 表示由左到右。

## <a name="range"></a>range

範圍是 [執行](#run)的特殊案例。 它完全落在一個 [專案](#item)內。 因此，如果某個專案被細分為執行，則每個執行都是一個範圍。

## <a name="rlm"></a>RLM

RLM 指出 (Unicode 程式碼點 U + 200F) 的由右至左標記。 此標記表示以邏輯順序接在後面的字元應由右至左呈現。

## <a name="rtl"></a>RTL

RTL 表示由右至左。

## <a name="run"></a>執行

回合是一段文字，可供 Uniscribe 轉譯。 它應該有單一樣式，也就是字型、大小和色彩，但可以從各種不同的 [腳本](#complex-script)中繪製。 執行可以同時包含由左至右和由右至左的內容。

## <a name="nads"></a>NADS

NADS 表示國家/地區數位圖形 (Unicode 代碼點 U + 206E。 此詞彙指定歐洲數位 (U + 0030 到 U + 0039) 應轉譯為國家/地區數位。 如需國家/地區數位的進一步討論，請參閱 [數位圖形](digit-shapes.md) 。

## <a name="nods"></a>點頭

節點表示名義數位圖形 (Unicode 程式碼點 U + 206F) 。 此詞彙指定歐洲數位 (U + 0030 到 U + 0039) 應正常轉譯，而不是國家/地區數位。

## <a name="overhang"></a>過剩

懸垂是圖像的筆墨一部分，超出圖像的 [前進寬度](#advance-width) 。 大部分的字元 (例如 "H" ) 沒有任何懸垂，因為任一側邊都有一個空格，可將它們與連續的字元分隔。 具有懸垂的圖像範例是本主題中使用的斜體 "f"，以說明 [ABC 的寬度](#abc-width)。 斜體 "f" 的頂端和底端都會延伸連續的圖像。 懸垂會對應至負的 "A" 或 "C" 寬度。

## <a name="padding"></a>填補 (padding)

請參閱 [underhang](#underhang)。

## <a name="script"></a>指令碼

腳本是撰寫語言的系統，例如，拉丁腳本、阿拉伯文腳本、中文腳本。 單一腳本可以套用至一或多個人類語言。 腳本與字型沒有特定的關聯性。 例如，您可以透過新的羅馬字元或 Arial 字型，以同樣的方式轉譯拉丁腳本。

## <a name="underhang"></a>underhang

Underhang 是字元左邊或右邊的泛空白字元寬度（空白部分）。 Underhang 會對應至正的 "A" 或 "C" 寬度（如 [ABC 寬度](#abc-width)所述）。 Underhang 有時稱為「填補」。 下圖顯示小寫字母 n 的 underhang。

![顯示小寫字母 n underhang 的圖例。](images/underhang.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 

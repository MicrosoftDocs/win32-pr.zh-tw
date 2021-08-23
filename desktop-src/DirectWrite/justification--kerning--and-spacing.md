---
title: 理由、字偶間距和間距
description: 從 Windows 8 開始，DirectWrite 提供許多功能，可讓您控制基本的印刷樣式、配置和間距功能，例如字元間距、配對的間距和對齊方式。
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdd82e201429adb62e687021f003d7d5d6bedcd228c3102f448b04d1f079f71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632627"
---
# <a name="justification-kerning-and-spacing"></a>理由、字偶間距和間距

從 Windows 8 開始， [DirectWrite](direct-write-portal.md)提供許多功能，可讓您控制基本的印刷樣式、配置和間距功能，例如字元間距、配對的間距和對齊方式。

## <a name="character-spacing"></a>字元間距

字元間距也稱為「追蹤」，這是執行文字中的字元之間的間距。

以下是追蹤的範例。 第一行不會對文字套用任何追蹤。 第二行會增加字元間距，而第三行則會減少字元間距。

![相同文字的三個範例，沒有追蹤、更多間距及間距較少。](images/spacing.png)

從 Windows 8 開始， [DirectWrite](direct-write-portal.md)在這裡新增這些方法，以控制文字中的字元間距。

如果您使用 [DirectWrite](direct-write-portal.md)配置，您可以針對此用途使用 [**IDWriteTextLayout1：： GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing)和 [**IDWriteTextLayout1：： SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing)方法。

您可以使用 [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) 方法來判斷目前的字元間距，並傳回目前的字元、字元之前和之後的間距、最小的前進寬度，以及包含剩餘文字之開始位置與長度相關資訊的 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 結構。

使用 [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)介面上的 [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) ，將您自己的字元間距套用至版面配置中的文字。 **SetCharacterSpacing** 方法會採用您要在字元之前和之後的空間量、允許的最小預付，以及定義要套用間距之範圍的 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range)。

如果您使用自訂版面配置， [DirectWrite](direct-write-portal.md)支援使用 [**IDWriteTextAnalyzer1：： ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing)來設定字元間距。 如果您需要自訂文字版面配置，才能對版面配置進行先進的控制，請使用這個方法。 這種方法可讓您提供 **ApplyCharacterSpacing** 的開頭和尾端間距、最小的前進寬度、叢集對應的長度、圖像數目、從字元範圍到字元的對應，以及在使用自訂版面配置時，每個圖像的前進寬度。 方法會傳回修改過的圖像前進和 [**DWRITE 的圖像 \_ \_ 位移**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) 列舉，以及每個字元原點的新位移。

## <a name="kerning"></a>字元

字偶間距調整是一組字母的配對或 triplet 之間的內容間距調整。 字元集之間的特定間距可提高可讀性，讓文字外觀更好。 字偶間距和字元間距之間的重要差異，在於字母間距與文字的空格無關，而在某些情況下，會在字型中定義的特定字元集間使用字偶間距調整。

影像的影像是字偶間距的範例。 在最上方的文字文字會進行間距調整，讓文字看起來更自然。 您可以從字元周圍的紅色方塊中看出，前四個字母之間會有更多間距，而結尾的 R 有更多空間。 沒有間距的原始文字會在第二行上。 此範例中的字偶間距讓文字更容易閱讀且更自然。

![已套用或不套用間距的相同單字範例。](images/kerning.png)

字元會在字型 kerns 儲存于字偶間距表中的字元配對之間前進， [DirectWrite](direct-write-portal.md)剖析該資料表，並透過字偶間距調整 api 將資訊傳回給您。

如果您想要知道字型是否支援配對的字偶間距調整，您可以使用 [**IDWriteFontFace1：： HasKerningPairs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) 方法。 如果字型支援字偶間距配對，則這個方法會傳回布林值1。

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)也有一種方法，可讓您存取圖像索引的字偶間距配對調整。 [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments)可讓您輸入圖像索引的陣列， [DirectWrite](direct-write-portal.md)會傳回圖像向前調整的陣列。 如果字型不支援字偶間距調整表格，則此方法會傳回零，以供圖像預先調整之用。

如果您使用 [DirectWrite](direct-write-portal.md)配置， [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)介面上有兩個方法可讓您設定配對的字偶間距調整，並深入瞭解版面配置中的配對間距。 如果您想要啟用配對字偶間距調整， [**SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) 方法會採用布林標記法，並使用 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 來定義要套用的文字範圍。 如果您想要瞭解是否在文字範圍上啟用成對的字偶間距調整，您可以使用 [**GetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) 方法，它會接受目前的位置並傳回布林值，對應於是否啟用配對的字偶間距調整，以及要套用字偶間距設定的文字範圍。

## <a name="justification"></a>理由

理由是對齊文字以填滿資料行內所有空間的程式，其方式是增加字元或字元叢集之間的前進量，或加入對齊字元以達成相同的效果。 一般而言，這是藉由判斷需要將空間加入至文字的位置，以及在這些中斷的機會中插入間距字元來達成。 這些間距專案也可以不同，在拉丁的腳本中，文字會藉由增加元素之間的前進寬度來對齊，而在阿拉伯文中，文字會與 kashida 對齊。 以下是對齊和不對齊的阿拉伯文和拉丁腳本範例。

![對齊和不對齊的阿拉伯文和拉丁腳本範例。](images/justification.png)

從 Windows 8 開始， [DirectWrite](direct-write-portal.md)有一些方法可讓您在應用程式中對齊文字。

[**DWRITE \_ 文字 \_ 對齊**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment)列舉中有額外的值。 您可以使用 [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)方法，並傳入 DWRITE 的 **\_ 文字 \_ 對齊對齊 \_** 常數， [DirectWrite](direct-write-portal.md)對齊文字並為腳本插入適當的對齊字元。

如果您使用自訂版面配置，有許多方法可供使用，因此您可以利用理由。 [DirectWrite](direct-write-portal.md)在 [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)介面上有三個方法，可讓您用來將理由新增至自訂版面配置。

第一個方法是 [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities)，它接受您想要對齊的文字，並傳回 DWRITE 的 [**\_ 理由 \_ 機會**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) 結構，以概述可加入對齊字元以調整文字的位置。

第二個函式是 [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances)，它會對齊字元前進的陣列，使其符合線條寬度。 這個方法會採用 [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities)所產生的 [**DWRITE \_ 對齊 \_ 商機**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity)結構、圖像前進和字元位移。 然後，它會產生對齊的圖像前進，以及包含對齊的圖像 [**位移的 DWRITE 圖像 \_ \_ 位移**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) 列舉。

第三個函式是 [**GetJustifiedGlyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs)，它會填入複雜字集的新字元，其中的理由已增加字元的前進量。 只有當腳本有 [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties)所傳回的特定對齊字元時，才需要呼叫 **GetJustifiedGlyphs** 。 這個方法會取得有關字型、文字長度、圖像的 em 大小、文字腳本、字元數、叢集對應、原始字元前進/位移、對齊圖像前進/位移和圖像屬性的資訊。 方法會傳回實際的圖像計數、更新的叢集對應、已更新的圖像索引（具有插入的對齊圖像、更新的圖像位移，以及更新的字元前進）。

 

 
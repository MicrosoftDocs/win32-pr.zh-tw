---
description: 本節描述印刷樣式和複雜字集處理的功能。
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Uniscribe 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984260"
---
# <a name="uniscribe-functions"></a>Uniscribe 函式

本節描述印刷樣式和複雜字集處理的功能。



| 函式                                                               | 描述                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | 將指定的數位替代設定套用至指定的腳本控制項和腳本狀態結構。                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | 取得回合的前進寬度陣列，並產生經過調整的前進字元寬度陣列。                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | 抓取用來判斷分行符號的資訊。                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | 抓取目前快取字型的高度。                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | 從執行的左邊緣或開頭緣到邏輯字元叢集的開頭或尾端邊緣產生 x 位移。                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | 釋放腳本快取。                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | 根據為舊樣式字型所執行的 TrueType cmap 資料表或標準 cmap 資料表，抓取字串中 Unicode 字元的圖像索引。         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | 抓取可透過指定的 OpenType 功能存取之指定字元的替代字型清單。                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | 抓取針對 OpenType 處理所定義書寫系統的印刷樣式功能清單。                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | 抓取語言標記清單，這些標記可供指定的專案使用，並由 OpenType 處理的指定腳本標記支援。                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | 在字型所使用的特殊字元上，從字型快取中抓取資訊。                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | 抓取 OpenType 處理字型中可用的腳本清單。                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | 抓取指定圖像的 ABC 寬度。                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | 將特定字型的圖像前移寬度轉換成邏輯寬度。                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | 抓取目前腳本的相關資訊。                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | 判斷 Unicode 字串是否需要複雜的腳本處理。                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | 將 Unicode 字串分割成個別的 shapeable 專案。                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | 將 Unicode 字串分成個別的 shapeable 專案，並針對 OpenType 處理的每個 shapeable 專案提供功能標記的陣列。                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | 建立前移寬度資料表，以在傳遞至 [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) 函式時允許文字對齊。                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | 將執行內嵌層級的陣列轉換為視覺效果與邏輯位置的對應，以及/或邏輯到視覺化的位置。                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | 從 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)的輸出產生圖像前進寬度和二維位移資訊。                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | 使用來自 [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)輸出的 OpenType 資訊，產生 Unicode 執行的字元和視覺屬性。                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | 使用在 OpenType 處理字型中提供的指定功能，以單一調整來放置單一圖像。                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | 讀取 (NLS) 原生數位和數位替代設定的國家語言支援，並將其記錄在 [**腳本 \_ DIGITSUBSTITUTE**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) 結構中。 |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | 產生 Unicode 執行的字元和視覺屬性。                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | 使用 OpenType 資訊產生 Unicode 執行的字元和視覺屬性。                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | 分析純文字字串。                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | 抓取字元位置開頭或尾端邊緣的 x 座標。                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | 釋放 [**腳本 \_ 字串 \_ 分析**](script-string-analysis.md) 結構。                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | 將視覺效果寬度轉換成邏輯寬度。                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | 建立將原始字元位置對應至圖像位置的陣列。                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | 顯示先前呼叫 [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) 所產生的字串，並選擇性地新增反白顯示。                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | 傳回裁剪後的字串長度指標。                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | 傳回已分析之字串的邏輯屬性緩衝區指標。                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | 傳回已分析之字串的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構指標。                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | 檢查 [**腳本 \_ 字串 \_ 分析**](script-string-analysis.md) 結構中是否有不正確順序。                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | 將 x 座標轉換成字元位置。                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | 允許以相同影像處理的一種替代形式來替代單一圖像。                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | 顯示指定之腳本圖形和位置資訊的文字。                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | 從執行的 x 位移產生邏輯字元叢集的開頭或尾端邊緣。                                                                                 |



 

 

 

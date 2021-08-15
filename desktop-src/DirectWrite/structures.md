---
title: DirectWrite 結構
description: DirectWrite 定義下列結構。
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa3d4d98588e3585022bb0887c6224e29d67e0c0d011437526b33ff0bcf1334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815951"
---
# <a name="directwrite-structures"></a>DirectWrite 結構

DirectWrite 定義下列結構。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | 代表 BGRA32 格式的點陣圖資料。 |
| [**DWRITE \_ 插入號 \_ 計量**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | [**DWRITE \_ 插入號 \_ 度量**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics)結構會指定字型中插入號位置的度量。 |
| [**DWRITE \_ 叢集 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | 包含圖像叢集的相關資訊。 |
| [**DWRITE \_ 色彩 \_ F**](dwrite-color-f.md) | 描述色彩的紅色、綠色、藍色和 Alpha 元件。 |
| [**DWRITE \_ 色彩 \_ 字型 \_ 執行**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | 包含轉譯器用來繪製具有圖像色彩資訊之圖像執行所需的資訊。 |
| [**DWRITE \_ 色彩 \_ 字型 \_ >run1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | 表示色彩圖像執行。 IDWriteFactory4：： TranslateColorGlyphRun 方法會根據字型所支援的內容，傳回不同類型之色彩圖像執行的已排序集合。 |
| [**DWRITE \_ 檔案 \_ 片段**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | 代表字型檔案中的位元組範圍。 |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | 表示字型軸可能值的最小和最大範圍。 |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | 表示字型軸的值。 在查詢和建立字型實例時使用。 |
| [**DWRITE \_ 字型 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | 指定用來識別和執行目前字型字型之印刷樣式功能的屬性。 |
| [**DWRITE \_ 字型 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | [**DWRITE \_ 字型 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)結構會指定適用于字型內所有字型的度量。 |
| [**DWRITE \_ 字型 \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | [**DWRITE \_ font-family \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1)結構會指定適用于字型內所有圖像的度量。 |
| [**DWRITE \_ 字型 \_ 屬性**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | 字型屬性，用於篩選字型集合，以及建立具有明確屬性的字型。 |
| [**DWRITE \_ \_ 圖像的 \_ 資料**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | GetGlyphImageData 中單一圖像的資料。 |
| [**DWRITE \_ 圖像 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | 指定個別字元的度量。 |
| [**DWRITE \_ 圖像 \_ 位移**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | 選擇性地調整圖像的位置。 |
| [**DWRITE \_ 圖像 \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | 包含轉譯器用來繪製圖像執行所需的資訊。 |
| [**DWRITE \_ 圖像 \_ 執行 \_ 描述**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | 包含與 [**DWRITE 圖像 \_ \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)相關的其他屬性。 |
| [**DWRITE \_ 點擊 \_ 測試 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | 描述點擊測試所取得的區域。 |
| [**DWRITE \_ 內嵌 \_ 物件 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | 包含描述應用程式定義内嵌物件之幾何量值的屬性。 |
| [**DWRITE \_ 理由 \_ 機會**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | [**DWRITE \_ 理由 \_ 商機**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity)結構會指定每個字元的理由資訊。 |
| [**DWRITE \_ 行 \_ 中斷點**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | 字元的行中斷點特性。 |
| [**DWRITE \_ 線 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | 包含格式化文字行的相關資訊。 |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | 包含格式化文字行的相關資訊。 |
| [**DWRITE \_ 行距 \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)結構會指定要套用至轉譯圖像的圖形轉換。 |
| [**DWRITE \_ 懸垂 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | 指出 (與裝置無關的圖元之間，) 超過配置或内嵌物件的每一側的任何可見 Dip 量。 |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose)聯集描述您搭配 [**IDWriteFont1：： GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose)使用的字型分類值，以選取並符合字型。 |
| [**DWRITE \_ 腳本 \_ 分析**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | 儲存文字與其書寫系統腳本的關聯，以及一些顯示內容。 |
| [**DWRITE \_ 腳本 \_ 屬性**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | [**DWRITE \_ 腳本 \_ 屬性**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties)結構會指定插入點流覽和對齊的腳本屬性。 |
| [**DWRITE \_ 成形 \_ 圖像 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | 包含輸出圖像的成形輸出屬性。 |
| [**DWRITE \_ 成形 \_ 文本 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | 塑造輸出圖像的輸出屬性。 |
| [**DWRITE \_ 刪除線**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | 包含 strikethroughs 大小和位置的相關資訊。 |
| [**DWRITE \_ 文字 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | 包含在版面配置之後與文字相關聯的度量。 |
| [**DWRITE \_ 文字 \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | 包含在版面配置之後與文字相關聯的度量。 |
| [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | 指定格式套用於 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件所代表之文字中的文字位置範圍。 |
| [**DWRITE \_ 修剪**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | 指定文字的修剪選項，讓版面配置框溢位。  |
| [**DWRITE \_ 印刷樣式 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | 包含要在文字成形期間套用的一組印刷樣式功能。 |
| [**DWRITE \_ 底線**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | 包含底線的寬度、粗細、位移、執行高度、閱讀方向和流動方向的相關資訊。  |
| [**DWRITE \_ UNICODE \_ 範圍**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | [**DWRITE 的 \_ unicode \_ 範圍**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range)結構會指定 unicode 程式碼點的範圍。 |



 


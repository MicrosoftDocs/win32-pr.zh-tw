---
title: DirectWrite 列舉
description: DirectWrite 定義下列列舉。
ms.assetid: 809ccacd-ff23-4d7b-a177-e7a9937c0c5a
keywords:
- DirectWrite，列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b5e889186c32874af93687ccceb9818bf4dacefeda717fceee3e7c06302a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830528"
---
# <a name="directwrite-enumerations"></a>DirectWrite 列舉

DirectWrite 定義下列列舉。

## <a name="in-this-section"></a>本節內容

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes"><strong>DWRITE_AUTOMATIC_FONT_AXES</strong></a></td>
<td>定義常數，指定可在字型選取期間自動套用至版面配置的特定座標軸。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_baseline"><strong>DWRITE_BASELINE</strong></a>列舉包含值，這些值會指定文字對齊的基線。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_break_condition"><strong>DWRITE_BREAK_CONDITION</strong></a></td>
<td>指出内嵌物件邊緣的條件，或用來判斷行中斷行為的文字。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_container_type"><strong>DWRITE_CONTAINER_TYPE</strong></a></td>
<td>指定字型資源的容器格式。 容器格式與字型檔案格式不同 (DWRITE_FONT_FILE_TYPE) ，因為容器會描述用來封裝基礎字型檔案的容器。 </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE</strong></a></td>
<td>指定 DirectWrite factory 物件的類型。</td>
</tr>
<tr>
<td><a href="/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type"><strong>DWRITE_FACTORY_TYPE (DWriteCore) </strong></a></td>
<td>指定 DirectWrite factory 物件的類型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction"><strong>DWRITE_FLOW_DIRECTION</strong></a></td>
<td>指出文字行相對於彼此的放置方向。 </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes"><strong>DWRITE_FONT_AXIS_ATTRIBUTES</strong></a></td>
<td>定義指定字型軸屬性的常數。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag"><strong>DWRITE_FONT_AXIS_TAG</strong></a></td>
<td>定義常數，指定字型軸的四個字元識別碼。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type"><strong>DWRITE_FONT_FACE_TYPE</strong></a></td>
<td>表示完整字型字型的檔案格式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model"><strong>DWRITE_FONT_FAMILY_MODEL</strong></a></td>
<td>定義常數，指定如何將字型系列群組在一起。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag"><strong>DWRITE_FONT_FEATURE_TAG</strong></a></td>
<td>值，指出字型所提供文字的印刷樣式功能。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type"><strong>DWRITE_FONT_FILE_TYPE</strong></a></td>
<td>以單一字型檔案表示的字型類型。 包含多個檔案的字型格式，例如類型1。PFM 和。PFB，每個檔案類型都有個別的列舉值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage"><strong>DWRITE_FONT_LINE_GAP_USAGE</strong></a></td>
<td>指定 <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics"><strong>DWRITE_FONT_METRICS</strong></a>：： lineGap 值是否應該是行度量的一部分</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id"><strong>DWRITE_FONT_PROPERTY_ID</strong></a></td>
<td>識別字型中的字串。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations"><strong>DWRITE_FONT_SIMULATIONS</strong></a></td>
<td>指定要套用至字型的演算法樣式模擬。 粗體和傾斜模擬可以透過位 OR 運算來合併。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type"><strong>DWRITE_FONT_SOURCE_TYPE</strong></a></td>
<td>定義常數，指定字型要包含在字型集中的機制。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch"><strong>DWRITE_FONT_STRETCH</strong></a></td>
<td>表示相較于字型的一般外觀比例，字型已伸展的程度。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style"><strong>DWRITE_FONT_STYLE</strong></a></td>
<td>表示字型的樣式，以標準、斜體或傾斜表示。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight"><strong>DWRITE_FONT_WEIGHT</strong></a></td>
<td>以筆劃的亮度或 heaviness 表示字樣的密度。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats"><strong>DWRITE_GLYPH_IMAGE_FORMATS</strong></a></td>
<td>指定字型中支援的格式，不論是在全字型層級或每個字元。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_glyph_orientation_angle"><strong>DWRITE_GLYPH_ORIENTATION_ANGLE</strong></a>列舉包含的值，可指定如何將圖像導向 X 軸。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode"><strong>DWRITE_GRID_FIT_MODE</strong></a></td>
<td>指定是否要啟用圖像大綱的貼齊格線 (也稱為提示) 。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id"><strong>DWRITE_INFORMATIONAL_STRING_ID</strong></a></td>
<td>參考字串列舉，識別內嵌于字型檔中的字串。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method"><strong>DWRITE_LINE_SPACING_METHOD</strong></a></td>
<td>用於文字版面配置之行距的方法。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_locality"><strong>DWRITE_LOCALITY</strong></a></td>
<td>指定資源的位置。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode"><strong>DWRITE_MEASURING_MODE</strong></a></td>
<td>表示用於文字版面配置的測量方法。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_number_substitution_method"><strong>DWRITE_NUMBER_SUBSTITUTION_METHOD</strong></a></td>
<td>指定如何針對數位和相關標點符號套用數位替換。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_optical_alignment"><strong>DWRITE_OPTICAL_ALIGNMENT</strong></a></td>
<td>光學邊界對齊模式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_outline_threshold"><strong>DWRITE_OUTLINE_THRESHOLD</strong></a>列舉包含值，這些值會指定<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode"><strong>IDWriteFontFace1：： GetRecommendedRenderingMode</strong></a>方法所使用的原則，以判斷是否要在大綱模式中轉譯圖像。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_arm_style"><strong>DWRITE_PANOSE_ARM_STYLE</strong></a>列舉包含值，這些值會指定文字的終止和圓角 letterforms 的樣式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect"><strong>DWRITE_PANOSE_ASPECT</strong></a>列舉包含值，這些值會指定字元臉部的寬度和高度之間的比率。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_aspect_ratio"><strong>DWRITE_PANOSE_ASPECT_RATIO</strong></a>列舉包含值，這些值會指定字元臉部的寬度和高度之間的比率資訊。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_character_ranges"><strong>DWRITE_PANOSE_CHARACTER_RANGES</strong></a>列舉包含值，這些值會指定字型中可用的字元類型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_contrast"><strong>DWRITE_PANOSE_CONTRAST</strong></a>列舉包含值，這些值會指定字母的 thickest 和最薄點之間的比例，例如大寫的 ' O '。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_class"><strong>DWRITE_PANOSE_DECORATIVE_CLASS</strong></a>列舉包含的值，可指定字元臉部的一般外觀。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_decorative_topology"><strong>DWRITE_PANOSE_DECORATIVE_TOPOLOGY</strong></a>列舉包含值，這些值會指定字型的整體形狀特性。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_family"><strong>DWRITE_PANOSE_FAMILY</strong></a>列舉包含指定字樣分類種類的值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_fill"><strong>DWRITE_PANOSE_FILL</strong></a>列舉包含的值，可指定填滿和行處理的類型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_finials"><strong>DWRITE_PANOSE_FINIALS</strong></a>列舉包含值，這些值會指定如何處理字元結束和相比簡直小巫見大巫 ascenders。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_letterform"><strong>DWRITE_PANOSE_LETTERFORM</strong></a>列舉包含值，這些值會指定文字的 LETTERFORM 圓度。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_lining"><strong>DWRITE_PANOSE_LINING</strong></a>列舉包含值，這些值會指定裝飾性字樣的輪廓處理。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_midline"><strong>DWRITE_PANOSE_MIDLINE</strong></a>列舉包含值，這些值會指定在大寫字元之間放置中線的資訊，以及對角線 apexes 的處理方式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_proportion"><strong>DWRITE_PANOSE_PROPORTION</strong></a>列舉包含值，這些值會考慮使用標準字元的額外詳細資料，來指定圖像圖形的比例。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_form"><strong>DWRITE_PANOSE_SCRIPT_FORM</strong></a>列舉包含的值，可指定字元臉部的一般外觀（考慮其斜率和連接結尾）。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_script_topology"><strong>DWRITE_PANOSE_SCRIPT_TOPOLOGY</strong></a>列舉包含指定 letterforms 拓撲的值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_serif_style"><strong>DWRITE_PANOSE_SERIF_STYLE</strong></a>列舉包含的值，可指定襯線文字的外觀。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_spacing"><strong>DWRITE_PANOSE_SPACING</strong></a>列舉包含的值，可指定 (等寬和依比例) 的字元間距。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_stroke_variation"><strong>DWRITE_PANOSE_STROKE_VARIATION</strong></a>列舉包含值，這些值會指定文字字元的精簡和粗詞幹之間的關聯性。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_aspect_ratio"><strong>DWRITE_PANOSE_SYMBOL_ASPECT_RATIO</strong></a>列舉包含值，這些值會指定符號字元的長寬比。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_symbol_kind"><strong>DWRITE_PANOSE_SYMBOL_KIND</strong></a>列舉包含指定符號集種類的值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_tool_kind"><strong>DWRITE_PANOSE_TOOL_KIND</strong></a>列舉包含值，這些值會指定用來建立字元格式的工具種類。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_weight"><strong>DWRITE_PANOSE_WEIGHT</strong></a>列舉包含指定字元權數的值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xascent"><strong>DWRITE_PANOSE_XASCENT</strong></a>列舉包含的值，可指定小寫字母的相對大小。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_panose_xheight"><strong>DWRITE_PANOSE_XHEIGHT</strong></a>列舉包含值，這些值會指定小寫字母之相對大小的相關資訊，以及 (XHEIGHT) 之變音符號標記的處理方式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_paragraph_alignment"><strong>DWRITE_PARAGRAPH_ALIGNMENT</strong></a></td>
<td>指定相對於流程的版面配置方塊頂端和底部，沿著流程方向軸的段落文字對齊方式。 </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry"><strong>DWRITE_PIXEL_GEOMETRY</strong></a></td>
<td>代表裝置圖元的內部結構 (也就是紅色、綠色和藍色色彩元件的實體相片順序，) 因應轉譯文字的用途。 </td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction"><strong>DWRITE_READING_DIRECTION</strong></a></td>
<td>指定讀取進度的方向。 
<blockquote>
[!Note]<br />
<strong>DWRITE_READING_DIRECTION_TOP_TO_BOTTOM</strong>和<strong>DWRITE_READING_DIRECTION_BOTTOM_TO_TOP</strong>可在 Windows 8.1 和更新版本中使用。
</blockquote>
</td>
</tr>
<tr>
<td><a href="/windows/win32/directwrite/dwrite-rendering-mode-enumerations">DWRITE_RENDERING_MODE 列舉</a></td>
<td>從 Windows 8 開始， <strong>DWRITE_RENDERING_MODE</strong>列舉新增了新的列舉值，並已取代其他列舉值。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_rendering_mode1"><strong>DWRITE_RENDERING_MODE1</strong></a></td>
<td>指定如何轉譯字型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_script_shapes"><strong>DWRITE_SCRIPT_SHAPES</strong></a></td>
<td>指出文字的其他成形需求。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment"><strong>DWRITE_TEXT_ALIGNMENT</strong></a></td>
<td>指定相對於版面配置方塊的開頭和尾端邊緣，在閱讀方向軸上的段落文字對齊方式。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode"><strong>DWRITE_TEXT_ANTIALIAS_MODE</strong></a>列舉包含值，這些值會指定轉譯模式呼叫消除鋸齒時要用於文字的消除鋸齒類型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_texture_type"><strong>DWRITE_TEXTURE_TYPE</strong></a></td>
<td>識別 Alpha 材質的類型。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_trimming_granularity"><strong>DWRITE_TRIMMING_GRANULARITY</strong></a></td>
<td>指定文字資料細微性，用來修剪版面配置方塊中的文字。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a></td>
<td><a href="/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_vertical_glyph_orientation"><strong>DWRITE_VERTICAL_GLYPH_ORIENTATION</strong></a>列舉包含值，這些值會指定文字所需的字元方向種類。</td>
</tr>
<tr>
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping"><strong>DWRITE_WORD_WRAPPING</strong></a></td>
<td>指定要在特定多行段落中使用的換行。 
<blockquote>
[!Note]<br />
<strong>DWRITE_WORD_WRAPPING_EMERGENCY_BREAK</strong>、 <strong>DWRITE_WORD_WRAPPING_WHOLE _WORD</strong>和<strong>DWRITE_WORD_WRAPPING_CHARACTER</strong>只能在 Windows 8.1 和更新版本中使用。
</blockquote>
</td>
</tr>
</tbody>
</table>



 

 

 






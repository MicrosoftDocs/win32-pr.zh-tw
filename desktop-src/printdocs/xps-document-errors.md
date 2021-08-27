---
description: 下表列出 XPS 檔 API 的方法可傳回的所有 HRESULT 值。
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: 'XPS 檔錯誤 (Xpsobjectmodel .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f15f1cc5a1908010d7a46dca9c63b12218e53b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471604"
---
# <a name="xps-document-errors"></a>XPS 檔錯誤

下表列出 XPS 檔 API 的方法可傳回的所有 **HRESULT** 值。 請注意，並非每個方法都會傳回此資料表中所列的每個傳回值。




| 傳回碼/值 | Description | 
|-------------------|-------------|
| <span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl><dt><strong>XPS_E_ALREADY_OWNED</strong></dt><dt>0x80520503</dt></dl> | 介面已經有擁有者。<br /> | 
| <span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt><dt>0x80520509</dt></dl> | 出血方塊維度與頁面尺寸不相容。<br /> 出血方塊寬度值必須大於或等於頁面寬度，加上出血方塊來源 x 座標的絕對值。 出血方塊高度值必須大於或等於頁面高度，以及出血方塊來源 y 座標的絕對值。 <br /> | 
| <span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt><dt>0x80520507</dt></dl> | <strong>PathGeometry</strong>專案包含一組以<strong>圖形</strong>屬性或子<strong>PathFigure</strong>元素指定的路徑圖形。 幾何的路徑圖形不能同時有 <strong>圖形</strong> 屬性和子 <strong>PathFigure</strong> 元素。 <br /> | 
| <span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt><dt>0x80520508</dt></dl> | 在其<strong>來源</strong>屬性中指定遠端資源字典的<strong>ResourceDictionary</strong>元素不能包含任何資源定義子系。<br /> | 
| <span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt><dt>0x80520306</dt></dl> | 插入號位置值未按順序。 位置值必須以遞增順序排序。 <br /> | 
| <span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt><dt>0x80520305</dt></dl> | 指定空字串的插入號停止;或者，插入號跳躍索引已超過 Unicode 字串的長度。 <br /> | 
| <span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt><dt>0x80520506</dt></dl> | 色彩值超出範圍。<br /> 針對 <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> 色彩類型，Alpha 色板的值必須大於或等於0.0 且小於或等於 + 1.0。<br /> 針對 <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> 色彩類型，表示 Alpha 色板值的 <strong>channelValues [0]</strong> 必須大於或等於0.0 且小於或等於 + 1.0。 <br /> | 
| <span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt><dt>0x80520401</dt></dl> | 資源字典中的視覺效果具有 <strong>Name</strong> 屬性，可能不會在 <strong>ResourceDictionary</strong> 元素的任何子系上指定。<br /> | 
| <span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt><dt>0x80520209</dt></dl> | 字典中已經存在具有此名稱的物件。<br /> | 
| <span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt><dt>0x80520200</dt></dl> | 字典中已經有具有此索引鍵名稱的物件。<br /> | 
| <span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt><dt>0x80520500</dt></dl> | 保留的。<br /> | 
| <span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt><dt>0x80520004</dt></dl> | 出血方塊矩形包含一或多個無效值。 請參閱參數描述以取得有效的值。 <br /> | 
| <span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt><dt>0x8052000b</dt></dl> | Content box 矩形包含一或多個不正確值。 請參閱參數描述以取得有效的值。 <br /> | 
| <span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt><dt>0x8052000e</dt></dl> | 內容類型字串無效。<br /> | 
| <span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl><dt><strong>XPS_E_INVALID_FLOAT</strong></dt><dt>0x80520007</dt></dl> | <strong>FLOAT</strong>值無效。 它是無限或非數位 (NAN) 。<br /> | 
| <span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt><dt>0x8052000a</dt></dl> | 字型 URI 無效，可能是因為它包含不正確空白片段或字元。<br /> | 
| <span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt><dt>0x80520000</dt></dl> | 指定的語言無效或格式不正確。<br /> | 
| <span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt><dt>0x80520006</dt></dl> | 查閱索引鍵名稱參考的物件不是正確的呼叫類型。例如，如果方法傳回筆刷，但是查閱索引鍵名稱參考幾何物件。<br /> | 
| <span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl><dt><strong>XPS_E_INVALID_MARKUP</strong></dt><dt>0x8052000c</dt></dl> | 正在讀取的標記包含不符合 <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML 檔規格</a>的元素或屬性。<br /><blockquote>[!Note]<br />為了表示浮點值，XPS OM 會使用 <strong>FLOAT</strong> 資料類型，而不是 <strong>雙精度</strong>浮點數。 如果 XPS 檔的元素具有不符合 <strong>FLOAT</strong> 值的浮點數據，則在還原序列化期間遇到該值時，將會傳回此錯誤。</blockquote><br /><br /> | 
| <span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl><dt><strong>XPS_E_INVALID_NAME</strong></dt><dt>0x80520001</dt></dl> | 根據 XML 檔規格，傳遞的字串不是有效的名稱。 <br /> | 
| <span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt><dt>0x8052000f</dt></dl> | 保留的。<br /> | 
| <span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt><dt>0x80520003</dt></dl> | 頁面尺寸包含不正確頁面大小值。 <br /> | 
| <span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt><dt>0x80520002</dt></dl> | 根據 <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML 檔規格</a>，查閱索引鍵字串無效。<br /> | 
| <span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt><dt>0x80520005</dt></dl> | 不支援縮圖影像類型。<br /> | 
| <span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt><dt>0x8052000d</dt></dl> | 找到不正確或格式不正確的 XML 標記。<br /> | 
| <span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt><dt>0x80520302</dt></dl> | 在一或多個 <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> 結構中，元素不會序列。 <br /> | 
| <span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt><dt>0x80520304</dt></dl> | 影像地圖超過圖像索引的數目。<br /> | 
| <span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt><dt>0x80520303</dt></dl> | 影像地圖中發生錯誤。<br /> 如果 Unicode 字串是空的，則此錯誤表示也已定義圖像對應。 如果 Unicode 字串是空的，則不得定義圖像對應。<br /> 如果 Unicode 字串不是空的，則此錯誤表示已針對 Unicode 字串以外的字元定義圖像對應。 無法為超出 Unicode 字串長度的字元定義影像地圖。<br /> | 
| <span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt><dt>0x80520104</dt></dl> | 色彩設定檔參數為 <strong>Null</strong>，但需要色彩設定檔。 當 XPS_COLOR_TYPE_CONTEXT 色彩類型時，就需要色彩設定檔。 <br /> | 
| <span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt><dt>0x80520112</dt></dl> | 頁面指的是 discardable 資源，但不會指定 DiscardControl 元件名稱。<br /> | 
| <span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt><dt>0x80520109</dt></dl> | <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter：： AddPage</strong></a> 是在 <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter：： StartNewDocument</strong></a>之前呼叫。<br /> | 
| <span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt><dt>0x80520108</dt></dl> | 封裝未包含 FixedDocumentSequence。<br /> | 
| <span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl><dt><strong>XPS_E_MISSING_FONTURI</strong></dt><dt>0x80520107</dt></dl> | <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a>介面需要字型 URI，但未指定一個。<br /> | 
| <span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt><dt>0x80520102</dt></dl> | 沒有 Unicode 字串的 <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> 介面不會指定任何圖像索引。 <strong>IXpsOMGlyphs</strong>介面必須指定 Unicode 字串或圖像索引的陣列。<br /> | 
| <span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt><dt>0x8052010e</dt></dl> | 找不到影像筆刷的影像資源。<br /> | 
| <span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt><dt>0x80520101</dt></dl> | 遠端資源具有未預期的物件。<br /> | 
| <span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl><dt><strong>XPS_E_MISSING_NAME</strong></dt><dt>0x80520100</dt></dl> | 頁面尚未命名;只有當頁面具有名稱時，才能設定超連結目標狀態。<br /> | 
| <span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt><dt>0x8052010c</dt></dl> | FixedDocument 不包含任何 FixedPage 部分。 XPS 檔必須至少包含一個 FixedPage 部分。<br /> | 
| <span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt><dt>0x8052010d</dt></dl> | 頁面參考沒有對應的頁面。<br /> | 
| <span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt><dt>0x80520110</dt></dl> | 未參考所需的目標群組件。<br /> | 
| <span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt><dt>0x80520113</dt></dl> | 未指定資源的資料流程。<br /> | 
| <span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt><dt>0x8052010a</dt></dl> | 找不到 FixedDocumentSequence 所參考的 FixedDocument 部分。 XPS 檔必須包含至少一個 FixedDocument。<br /> | 
| <span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt><dt>0x8052010b</dt></dl> | 找不到 FixedDocument 所參考的 FixedPage 部分。 XPS 檔必須至少包含一個 FixedPage 部分。<br /> | 
| <span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt><dt>0x80520105</dt></dl> | 關聯性目標群組件不存在於封裝關聯性中。<br /> | 
| <span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt><dt>0x8052010f</dt></dl> | 未指定資源的 <strong>x：Key</strong> 屬性。<br /> | 
| <span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt><dt>0x80520106</dt></dl> | 頁面或遠端字典內容所參考的資源，不會以頁面關聯性的形式存在。<br /> | 
| <span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt><dt>0x80520111</dt></dl> | 呼叫 <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter：： StartNewDocument</strong></a>時，未指定參考的受限字型。<br /> | 
| <span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt><dt>0x80520103</dt></dl> | 區段資料陣列的專案少於區段類型陣列。 <br /> | 
| <span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt><dt>0x80520202</dt></dl> | 已嘗試將 FixedDocumentSequence 新增至已經有一個套件的封裝。 XPS 檔必須只包含一個 FixedDocumentSequence 元件。<br /> | 
| <span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt><dt>0x80520206</dt></dl> | 嘗試將檔層級列印票證新增至已有一個的 FixedDocument。 XPS 檔中的 FixedDocument 只能包含一個檔層級列印票證。<br /> | 
| <span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt><dt>0x80520207</dt></dl> | 嘗試將作業層級列印票證新增至已有一個的 FixedDocumentSequence。 XPS 檔中的 FixedDocumentSequence 只能包含一個作業層級列印票證。<br /> | 
| <span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt><dt>0x80520205</dt></dl> | 嘗試將頁面層級列印票證新增至已有一個的 FixedPage。 XPS 檔中的 FixedPage 只能包含一個頁面層級的列印票證。<br /> | 
| <span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt><dt>0x80520208</dt></dl> | 受限制的字型集合包含重複的受限字型專案。 每個字型專案只可出現在集合中。<br /> | 
| <span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt><dt>0x80520201</dt></dl> | 依該元件名稱的資源已經存在。<br /> | 
| <span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt><dt>0x80520204</dt></dl> | 嘗試將縮圖影像新增至已經有一個的封裝。 XPS 檔只能包含一個封裝層級的縮圖影像。<br /> | 
| <span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt><dt>0x80520203</dt></dl> | 嘗試將頁面層級的縮圖影像新增至已有一個的 FixedPage。 XPS 檔中的 FixedPage 只能包含一個頁面層級的縮圖影像。<br /> | 
| <span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt><dt>0x8052030a</dt></dl> | 專案包含負值，但它必須包含非負數值。 <br /> | 
| <span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt><dt>0x80520402</dt></dl> | 嘗試將遠端字典參考新增至遠端字典。 遠端字典無法參考另一個遠端字典。<br /> | 
| <span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt><dt>0x80520502</dt></dl> | 介面指標未指向可辨識的介面執行。 不支援自訂 XPS 檔 API 介面的執行。<br /> | 
| <span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt><dt>0x8052050b</dt></dl> | 漸層停駐點的集合少於兩個。 漸層停駐點集合至少必須有兩個漸層停駐點。<br /> | 
| <span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt><dt>0x80520307</dt></dl> | 文字字串已指定為面向方向和由右至左。 如果文字是側向方向的，則其雙向層級不能是奇數值 (由右至左) 。 同樣地，如果雙向層級為奇數值，則無法側嚮導向文字。<br /> | 
| <span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt><dt>0x80520308</dt></dl> | 影像地圖不符合 Unicode 字串內容。<br /> | 
| <span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt><dt>0x8052050c</dt></dl> | 封裝寫入器在發行之前未關閉。<br /> | 
| <span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt><dt>0x8052050a</dt></dl> | 關聯性是指 XPS 檔之外的部分。 Xps 檔中要轉譯的所有內容都必須包含在 XPS 檔中。<br /> | 
| <span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt><dt>0x80520504</dt></dl> | 保留的。<br /> | 
| <span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt><dt>0x80520309</dt></dl> | <em>保留</em>。<br /> | 
| <span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt><dt>0x80520300</dt></dl> | 嘗試將字串複製到新的緩衝區時發生 <strong>size_t</strong> 溢位。<br /> | 
| <span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt><dt>0x80520301</dt></dl> | 有比 Unicode 程式碼點更多的圖像索引。 如果沒有圖像對應，則圖像索引的數目必須小於或等於 Unicode 程式碼點的數目。<br /> | 
| <span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt><dt>0x80520114</dt></dl> | 發生嚴重錯誤，而且 XPS OM 的內容可能無法復原。 XPS OM 的某些元件可能仍可使用，但必須先進行驗證，才能繼續使用。 因為在傳回此錯誤之後無法預測 XPS OM 的狀態，所以應該釋放並捨棄 XPS OM 的所有元件。<br /> | 
| <span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt><dt>0x80520505</dt></dl> | 當色彩設定檔未預期時，即會出現。 只有在 <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>色彩類型時，才允許色彩設定檔。 <br /> | 
| <span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt><dt>0x80520008</dt></dl> | 關聯性的目標不是關聯性內容所預期的型別。 <br /> | 
| <span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt><dt>0x80520010</dt></dl> | 無法辨識關聯性類型。<br /> | 
| <span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt><dt>0x80520011</dt></dl> | 限制的字型集合包含不受限制的字型。<br /> | 
| <span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt><dt>0x80520501</dt></dl> | 保留的。<br /> | 
| <span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt><dt>0x80520400</dt></dl> | 不在資源字典中的路徑幾何已指定 <strong>x：Key</strong> 屬性。 不在資源字典中的路徑幾何不能有 <strong>x：Key</strong> 屬性。<br /> | 




 

## <a name="remarks"></a>備註

某些 XPS 檔 API 方法會對 [封裝](/previous-versions/windows/desktop/opc/packaging) API 進行呼叫。 如需封裝 API 傳回值的相關資訊，請參閱 [封裝錯誤](/previous-versions/windows/desktop/opc/packaging-errors)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2）和僅適用于 Windows Vista \[ 桌面應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和平臺更新，適用于 Windows Server 2008 \[ desktop 應用程式\]<br/> |
| 標頭<br/>                   | <dl> <dt>Xpsobjectmodel。h</dt> </dl>                                       |
| IDL<br/>                      | <dl> <dt>XpsObjectModel .idl</dt> </dl>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM 中的錯誤處理](../com/error-handling-in-com.md)
</dt> </dl>

 


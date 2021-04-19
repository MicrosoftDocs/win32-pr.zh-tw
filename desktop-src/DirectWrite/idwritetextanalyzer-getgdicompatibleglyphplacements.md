---
title: IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements 方法
description: 根據字型和書寫系統的轉譯規則，來放置 GetGlyphs 方法的圖像輸出。
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- GetGdiCompatibleGlyphPlacements 方法直接寫入
- GetGdiCompatibleGlyphPlacements 方法 Direct Write，IDWriteTextAnalyzer 介面
- IDWriteTextAnalyzer 介面 Direct Write，GetGdiCompatibleGlyphPlacements 方法
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001543"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>IDWriteTextAnalyzer：： GetGdiCompatibleGlyphPlacements 方法

根據字型和書寫系統的轉譯規則，來放置 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) 方法的圖像輸出。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*textString* \[在\]
</dt> <dd>

Type： **CONST WCHAR \***

字元陣列，包含圖像的來源原始字串。

</dd> <dt>

*clusterMap* \[在\]
</dt> <dd>

類型： **CONST UINT16 \***

從字元範圍到字元範圍的對應指標。 這是由 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回。

</dd> <dt>

*textProps* \[在\]
</dt> <dd>

類型： **[ **DWRITE \_ 成形 \_ 文本 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

結構陣列的指標，其中包含每個字元的成形屬性。 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)會傳回這個結構。

</dd> <dt>

*textLength* 
</dt> <dd>

類型： **UINT32**

*TextString* 的文字長度。

</dd> <dt>

*glyphIndices* \[在\]
</dt> <dd>

類型： **CONST UINT16 \***

[**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回的圖像索引陣列。

</dd> <dt>

*glyphProps* \[在\]
</dt> <dd>

Type： **Const [**DWRITE \_ 成形 \_ 圖像 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

結構陣列的指標，其中包含 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回之每個圖像的成形屬性。

</dd> <dt>

*glyphCount* 
</dt> <dd>

類型： **UINT32**

從 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)傳回的字元數。

</dd> <dt>

*fontFace* \[在\]
</dt> <dd>

類型： **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

字型的指標，其為輸出字元的來源。

</dd> <dt>

*fontEmSize* 
</dt> <dd>

類型： **FLOAT**

Dip 中的邏輯字型大小。

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

類型： **FLOAT**

每個 DIP 的實體圖元數目。

</dd> <dt>

*轉換* \[在中，選擇性\]
</dt> <dd>

Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

套用至字型及其位置的選擇性轉換。 此轉換會在字型大小和 *pixelsPerDip* 所指定的縮放比例之後套用。

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

類型： **BOOL**

當設定為 **FALSE** 時，計量與 GDI 別名文字的計量相同。 當設定為 **TRUE** 時，計量會與使用以 **CLEARTYPE \_ 自然 \_ 品質** 建立之字型所測量的文字計量相同。

</dd> <dt>

 *isSideways* 
</dt> <dd>

類型： **BOOL**

如果文字是要垂直繪製，則布林值旗標會設定為 **TRUE** 。

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

類型： **BOOL**

由右至左文字設定為 **TRUE** 的布林值旗標。

</dd> <dt>

 *scriptAnalysis* \[在\]
</dt> <dd>

類型： **Const [**DWRITE \_ 腳本 \_ 分析**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

[**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)呼叫的腳本分析結果指標。

</dd> <dt>

 *>localename* \[在中，選擇性\]
</dt> <dd>

Type： **CONST WCHAR \***

字元陣列，包含選取字元時要使用的地區設定。 例如，相同的字元可能對應至 ja-jp 與 zh-chs 的不同圖像。 如果這是 **Null**，則會使用以腳本為基礎的預設對應。

</dd> <dt>

 *功能* \[在中，選擇性\]
</dt> <dd>

Type： **Const [**DWRITE \_ 印刷樣式 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

要在每個功能範圍中使用的一組印刷樣式功能的指標陣列。

</dd> <dt>

 *featureRangeLengths* \[在中，選擇性\]
</dt> <dd>

類型： **CONST UINT32 \***

每個特徵範圍的長度（以字元為單位）。 所有長度的總和應等於 *textLength*。

</dd> <dt>

 *featureRanges* 
</dt> <dd>

類型： **UINT32**

功能範圍的數目。

</dd> <dt>

 *glyphAdvances* \[擴展\]
</dt> <dd>

類型： **FLOAT \***

當此方法傳回時，會包含每個字元的前進寬度。

</dd> <dt>

 *glyphOffsets* \[擴展\]
</dt> <dd>

類型： **[ **DWRITE \_ 圖像 \_ 位移**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

當此方法傳回時，會包含每個字元原點的位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 


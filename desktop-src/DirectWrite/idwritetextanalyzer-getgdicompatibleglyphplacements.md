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
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="bab31-106">IDWriteTextAnalyzer：： GetGdiCompatibleGlyphPlacements 方法</span><span class="sxs-lookup"><span data-stu-id="bab31-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="bab31-107">根據字型和書寫系統的轉譯規則，來放置 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) 方法的圖像輸出。</span><span class="sxs-lookup"><span data-stu-id="bab31-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab31-108">語法</span><span class="sxs-lookup"><span data-stu-id="bab31-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bab31-109">參數</span><span class="sxs-lookup"><span data-stu-id="bab31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab31-110">*textString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-111">Type： **CONST WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="bab31-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="bab31-112">字元陣列，包含圖像的來源原始字串。</span><span class="sxs-lookup"><span data-stu-id="bab31-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-113">*clusterMap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-114">類型： **CONST UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="bab31-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="bab31-115">從字元範圍到字元範圍的對應指標。</span><span class="sxs-lookup"><span data-stu-id="bab31-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="bab31-116">這是由 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回。</span><span class="sxs-lookup"><span data-stu-id="bab31-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="bab31-117">*textProps* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-118">類型： **[ **DWRITE \_ 成形 \_ 文本 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="bab31-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="bab31-119">結構陣列的指標，其中包含每個字元的成形屬性。</span><span class="sxs-lookup"><span data-stu-id="bab31-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="bab31-120">[**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)會傳回這個結構。</span><span class="sxs-lookup"><span data-stu-id="bab31-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="bab31-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="bab31-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-122">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bab31-122">Type: **UINT32**</span></span>

<span data-ttu-id="bab31-123">*TextString* 的文字長度。</span><span class="sxs-lookup"><span data-stu-id="bab31-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-124">*glyphIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-125">類型： **CONST UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="bab31-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="bab31-126">[**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回的圖像索引陣列。</span><span class="sxs-lookup"><span data-stu-id="bab31-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="bab31-127">*glyphProps* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-128">Type： **Const [**DWRITE \_ 成形 \_ 圖像 \_ 屬性**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***</span><span class="sxs-lookup"><span data-stu-id="bab31-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="bab31-129">結構陣列的指標，其中包含 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)所傳回之每個圖像的成形屬性。</span><span class="sxs-lookup"><span data-stu-id="bab31-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="bab31-130">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="bab31-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-131">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bab31-131">Type: **UINT32**</span></span>

<span data-ttu-id="bab31-132">從 [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)傳回的字元數。</span><span class="sxs-lookup"><span data-stu-id="bab31-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="bab31-133">*fontFace* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-134">類型： **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="bab31-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="bab31-135">字型的指標，其為輸出字元的來源。</span><span class="sxs-lookup"><span data-stu-id="bab31-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-136">*fontEmSize*</span><span class="sxs-lookup"><span data-stu-id="bab31-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-137">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="bab31-137">Type: **FLOAT**</span></span>

<span data-ttu-id="bab31-138">Dip 中的邏輯字型大小。</span><span class="sxs-lookup"><span data-stu-id="bab31-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="bab31-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-140">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="bab31-140">Type: **FLOAT**</span></span>

<span data-ttu-id="bab31-141">每個 DIP 的實體圖元數目。</span><span class="sxs-lookup"><span data-stu-id="bab31-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-142">*轉換* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bab31-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-143">Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="bab31-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="bab31-144">套用至字型及其位置的選擇性轉換。</span><span class="sxs-lookup"><span data-stu-id="bab31-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="bab31-145">此轉換會在字型大小和 *pixelsPerDip* 所指定的縮放比例之後套用。</span><span class="sxs-lookup"><span data-stu-id="bab31-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="bab31-146">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="bab31-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-147">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="bab31-147">Type: **BOOL**</span></span>

<span data-ttu-id="bab31-148">當設定為 **FALSE** 時，計量與 GDI 別名文字的計量相同。</span><span class="sxs-lookup"><span data-stu-id="bab31-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="bab31-149">當設定為 **TRUE** 時，計量會與使用以 **CLEARTYPE \_ 自然 \_ 品質** 建立之字型所測量的文字計量相同。</span><span class="sxs-lookup"><span data-stu-id="bab31-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-150">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="bab31-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-151">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="bab31-151">Type: **BOOL**</span></span>

<span data-ttu-id="bab31-152">如果文字是要垂直繪製，則布林值旗標會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bab31-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-153">*isRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="bab31-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-154">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="bab31-154">Type: **BOOL**</span></span>

<span data-ttu-id="bab31-155">由右至左文字設定為 **TRUE** 的布林值旗標。</span><span class="sxs-lookup"><span data-stu-id="bab31-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-156">*scriptAnalysis* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bab31-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-157">類型： **Const [**DWRITE \_ 腳本 \_ 分析**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="bab31-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="bab31-158">[**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)呼叫的腳本分析結果指標。</span><span class="sxs-lookup"><span data-stu-id="bab31-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-159">*>localename* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bab31-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-160">Type： **CONST WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="bab31-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="bab31-161">字元陣列，包含選取字元時要使用的地區設定。</span><span class="sxs-lookup"><span data-stu-id="bab31-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="bab31-162">例如，相同的字元可能對應至 ja-jp 與 zh-chs 的不同圖像。</span><span class="sxs-lookup"><span data-stu-id="bab31-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="bab31-163">如果這是 **Null**，則會使用以腳本為基礎的預設對應。</span><span class="sxs-lookup"><span data-stu-id="bab31-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-164">*功能* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bab31-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-165">Type： **Const [**DWRITE \_ 印刷樣式 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***</span><span class="sxs-lookup"><span data-stu-id="bab31-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="bab31-166">要在每個功能範圍中使用的一組印刷樣式功能的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="bab31-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-167">*featureRangeLengths* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bab31-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-168">類型： **CONST UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="bab31-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="bab31-169">每個特徵範圍的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bab31-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="bab31-170">所有長度的總和應等於 *textLength*。</span><span class="sxs-lookup"><span data-stu-id="bab31-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-171">*featureRanges*</span><span class="sxs-lookup"><span data-stu-id="bab31-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="bab31-172">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bab31-172">Type: **UINT32**</span></span>

<span data-ttu-id="bab31-173">功能範圍的數目。</span><span class="sxs-lookup"><span data-stu-id="bab31-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-174">*glyphAdvances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bab31-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-175">類型： **FLOAT \***</span><span class="sxs-lookup"><span data-stu-id="bab31-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="bab31-176">當此方法傳回時，會包含每個字元的前進寬度。</span><span class="sxs-lookup"><span data-stu-id="bab31-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="bab31-177">*glyphOffsets* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bab31-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab31-178">類型： **[ **DWRITE \_ 圖像 \_ 位移**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="bab31-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="bab31-179">當此方法傳回時，會包含每個字元原點的位移。</span><span class="sxs-lookup"><span data-stu-id="bab31-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab31-180">傳回值</span><span class="sxs-lookup"><span data-stu-id="bab31-180">Return value</span></span>

<span data-ttu-id="bab31-181">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bab31-181">Type: **HRESULT**</span></span>

<span data-ttu-id="bab31-182">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bab31-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bab31-183">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bab31-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab31-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="bab31-184">Requirements</span></span>



| <span data-ttu-id="bab31-185">需求</span><span class="sxs-lookup"><span data-stu-id="bab31-185">Requirement</span></span> | <span data-ttu-id="bab31-186">值</span><span class="sxs-lookup"><span data-stu-id="bab31-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bab31-187">程式庫</span><span class="sxs-lookup"><span data-stu-id="bab31-187">Library</span></span><br/> | <dl> <span data-ttu-id="bab31-188"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bab31-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="bab31-189">DLL</span><span class="sxs-lookup"><span data-stu-id="bab31-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="bab31-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab31-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab31-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bab31-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab31-192">**IDWriteTextAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="bab31-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 


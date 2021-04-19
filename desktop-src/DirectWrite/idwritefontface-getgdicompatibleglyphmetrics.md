---
title: IDWriteFontFace GetGdiCompatibleGlyphMetrics 方法
description: 使用與 GDI 產生的值相容的傳回值，取得字型設計單位中的字元度量。
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- GetGdiCompatibleGlyphMetrics 方法直接寫入
- GetGdiCompatibleGlyphMetrics 方法 Direct Write，IDWriteFontFace 介面
- IDWriteFontFace 介面 Direct Write，GetGdiCompatibleGlyphMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999371"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="3919b-106">IDWriteFontFace：： GetGdiCompatibleGlyphMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="3919b-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="3919b-107">使用與 GDI 產生的值相容的傳回值，取得字型設計單位中的字元度量。</span><span class="sxs-lookup"><span data-stu-id="3919b-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="3919b-108">語法</span><span class="sxs-lookup"><span data-stu-id="3919b-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3919b-109">參數</span><span class="sxs-lookup"><span data-stu-id="3919b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3919b-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="3919b-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3919b-111">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="3919b-111">Type: **FLOAT**</span></span>

<span data-ttu-id="3919b-112">以 DIP 單位表示的字型邏輯大小。</span><span class="sxs-lookup"><span data-stu-id="3919b-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="3919b-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="3919b-114">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="3919b-114">Type: **FLOAT**</span></span>

<span data-ttu-id="3919b-115">每個 DIP 的實體圖元數目。</span><span class="sxs-lookup"><span data-stu-id="3919b-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-116">*轉換* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3919b-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3919b-117">Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="3919b-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="3919b-118">套用至字型及其位置的選擇性轉換。</span><span class="sxs-lookup"><span data-stu-id="3919b-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="3919b-119">此轉換會在字型大小和 *pixelsPerDip* 所指定的縮放比例之後套用。</span><span class="sxs-lookup"><span data-stu-id="3919b-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-120">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="3919b-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="3919b-121">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="3919b-121">Type: **BOOL**</span></span>

<span data-ttu-id="3919b-122">當設定為 **FALSE** 時，計量與 GDI 別名文字的計量相同。</span><span class="sxs-lookup"><span data-stu-id="3919b-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="3919b-123">當設定為 **TRUE** 時，計量會與使用以 **CLEARTYPE \_ 自然 \_ 品質** 建立之字型所測量的文字計量相同。</span><span class="sxs-lookup"><span data-stu-id="3919b-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-124">*glyphIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3919b-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3919b-125">類型： **CONST UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="3919b-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="3919b-126">要計算度量的圖像索引陣列。</span><span class="sxs-lookup"><span data-stu-id="3919b-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-127">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="3919b-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3919b-128">類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3919b-128">Type: **UINT32**</span></span>

<span data-ttu-id="3919b-129">*GlyphIndices* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="3919b-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-130">*glyphMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3919b-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3919b-131">類型： **[ **DWRITE \_ 圖像 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="3919b-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="3919b-132">這個函式所填滿的 [**DWRITE 圖像 \_ \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="3919b-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="3919b-133">計量是以字型設計單位表示。</span><span class="sxs-lookup"><span data-stu-id="3919b-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="3919b-134">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="3919b-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="3919b-135">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="3919b-135">Type: **BOOL**</span></span>

<span data-ttu-id="3919b-136">布林值，指出是否在側邊執行中使用字型。</span><span class="sxs-lookup"><span data-stu-id="3919b-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="3919b-137">如果字型有傾斜的模擬，這可能會影響圖像度量，因為側向傾斜模擬與非側面傾斜模擬不同。</span><span class="sxs-lookup"><span data-stu-id="3919b-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3919b-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="3919b-138">Return value</span></span>

<span data-ttu-id="3919b-139">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3919b-139">Type: **HRESULT**</span></span>

<span data-ttu-id="3919b-140">標準 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3919b-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="3919b-141">如果任何輸入圖像索引是在目前字型臉部的有效圖像索引範圍之外，則會傳回 **E \_ INVALIDARG** 。</span><span class="sxs-lookup"><span data-stu-id="3919b-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="3919b-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="3919b-142">Requirements</span></span>



| <span data-ttu-id="3919b-143">需求</span><span class="sxs-lookup"><span data-stu-id="3919b-143">Requirement</span></span> | <span data-ttu-id="3919b-144">值</span><span class="sxs-lookup"><span data-stu-id="3919b-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3919b-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="3919b-145">Library</span></span><br/> | <dl> <span data-ttu-id="3919b-146"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3919b-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="3919b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3919b-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="3919b-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3919b-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3919b-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3919b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3919b-150">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="3919b-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="3919b-151">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="3919b-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


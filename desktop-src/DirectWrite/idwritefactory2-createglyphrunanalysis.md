---
title: IDWriteFactory2 CreateGlyphRunAnalysis 方法
description: 建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- CreateGlyphRunAnalysis 方法直接寫入
- CreateGlyphRunAnalysis 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，CreateGlyphRunAnalysis 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384926"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="19343-106">IDWriteFactory2：： CreateGlyphRunAnalysis 方法</span><span class="sxs-lookup"><span data-stu-id="19343-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="19343-107">建立圖像執行分析物件，此物件會封裝用來呈現圖像執行的資訊。</span><span class="sxs-lookup"><span data-stu-id="19343-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="19343-108">語法</span><span class="sxs-lookup"><span data-stu-id="19343-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="19343-109">參數</span><span class="sxs-lookup"><span data-stu-id="19343-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19343-110">*glyphRun* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19343-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19343-111">類型： \**Const [**DWRITE \_ 圖像 \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _</span><span class="sxs-lookup"><span data-stu-id="19343-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="19343-112">結構，指定圖像執行的屬性。</span><span class="sxs-lookup"><span data-stu-id="19343-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="19343-113">_transform \* \[ in，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="19343-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19343-114">類型： \**Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="19343-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="19343-115">套用至字型及其位置的選擇性轉換。</span><span class="sxs-lookup"><span data-stu-id="19343-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="19343-116">這項轉換會在 emSize 和 pixelsPerDip 所指定的縮放比例之後套用。</span><span class="sxs-lookup"><span data-stu-id="19343-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="19343-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="19343-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-118">類型： **DWRITE \_ 轉譯 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="19343-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="19343-119">指定轉譯模式，它必須是其中一個光柵轉譯模式 (也就是，不是預設值，也不是外框) 。</span><span class="sxs-lookup"><span data-stu-id="19343-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="19343-120">*measuringMode*</span><span class="sxs-lookup"><span data-stu-id="19343-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-121">類型： **[ **DWRITE \_ 測量 \_ 模式**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="19343-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="19343-122">指定量值的方法。</span><span class="sxs-lookup"><span data-stu-id="19343-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="19343-123">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="19343-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-124">類型： **[ **DWRITE \_ 格線 \_ 擬合 \_ 模式**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="19343-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="19343-125">如何將貼齊格線圖像大綱。</span><span class="sxs-lookup"><span data-stu-id="19343-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="19343-126">這必須為非預設值。</span><span class="sxs-lookup"><span data-stu-id="19343-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="19343-127">*antialiasMode*</span><span class="sxs-lookup"><span data-stu-id="19343-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-128">類型： **[ **DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="19343-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="19343-129">指定消除鋸齒模式。</span><span class="sxs-lookup"><span data-stu-id="19343-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="19343-130">*baselineOriginX*</span><span class="sxs-lookup"><span data-stu-id="19343-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-131">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="19343-131">Type: **FLOAT**</span></span>

<span data-ttu-id="19343-132">基準原點的水準位置（Dip）。</span><span class="sxs-lookup"><span data-stu-id="19343-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="19343-133">*baselineOriginY*</span><span class="sxs-lookup"><span data-stu-id="19343-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="19343-134">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="19343-134">Type: **FLOAT**</span></span>

<span data-ttu-id="19343-135">基準原點的垂直位置（Dip）。</span><span class="sxs-lookup"><span data-stu-id="19343-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="19343-136">*glyphRunAnalysis* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19343-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19343-137">類型： **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="19343-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="19343-138">接收新建立之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="19343-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19343-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="19343-139">Return value</span></span>

<span data-ttu-id="19343-140">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19343-140">Type: **HRESULT**</span></span>

<span data-ttu-id="19343-141">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="19343-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19343-142">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19343-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19343-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="19343-143">Requirements</span></span>



| <span data-ttu-id="19343-144">需求</span><span class="sxs-lookup"><span data-stu-id="19343-144">Requirement</span></span> | <span data-ttu-id="19343-145">值</span><span class="sxs-lookup"><span data-stu-id="19343-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19343-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19343-146">Minimum supported client</span></span><br/> | <span data-ttu-id="19343-147">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19343-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="19343-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19343-148">Minimum supported server</span></span><br/> | <span data-ttu-id="19343-149">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19343-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="19343-150">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="19343-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="19343-151">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19343-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="19343-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="19343-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="19343-153"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19343-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="19343-154">DLL</span><span class="sxs-lookup"><span data-stu-id="19343-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19343-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19343-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19343-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19343-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19343-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="19343-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 


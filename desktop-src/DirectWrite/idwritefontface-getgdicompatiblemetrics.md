---
title: IDWriteFontFace GetGdiCompatibleMetrics 方法
description: 取得字型字型的設計單位和一般度量。 這些計量適用于 fontface 內的所有字元，而且應用程式會使用這些計量來進行版面配置計算。
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- GetGdiCompatibleMetrics 方法直接寫入
- GetGdiCompatibleMetrics 方法 Direct Write，IDWriteFontFace 介面
- IDWriteFontFace 介面 Direct Write，GetGdiCompatibleMetrics 方法
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982555"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="07ab6-107">IDWriteFontFace：： GetGdiCompatibleMetrics 方法</span><span class="sxs-lookup"><span data-stu-id="07ab6-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="07ab6-108">取得字型字型的設計單位和一般度量。</span><span class="sxs-lookup"><span data-stu-id="07ab6-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="07ab6-109">這些計量適用于 fontface 內的所有字元，而且應用程式會使用這些計量來進行版面配置計算。</span><span class="sxs-lookup"><span data-stu-id="07ab6-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ab6-110">語法</span><span class="sxs-lookup"><span data-stu-id="07ab6-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="07ab6-111">參數</span><span class="sxs-lookup"><span data-stu-id="07ab6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07ab6-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="07ab6-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="07ab6-113">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="07ab6-113">Type: **FLOAT**</span></span>

<span data-ttu-id="07ab6-114">以 DIP 單位表示之字型的邏輯大小。</span><span class="sxs-lookup"><span data-stu-id="07ab6-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="07ab6-115">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="07ab6-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="07ab6-116">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="07ab6-116">Type: **FLOAT**</span></span>

<span data-ttu-id="07ab6-117">每個 DIP 的實體圖元數目。</span><span class="sxs-lookup"><span data-stu-id="07ab6-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="07ab6-118">*轉換* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="07ab6-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07ab6-119">Type： **Const [**DWRITE \_ 矩陣**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="07ab6-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="07ab6-120">套用至字型及其位置的選擇性轉換。</span><span class="sxs-lookup"><span data-stu-id="07ab6-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="07ab6-121">此轉換會在字型大小和 *pixelsPerDip* 所指定的縮放比例之後套用。</span><span class="sxs-lookup"><span data-stu-id="07ab6-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="07ab6-122">*fontFaceMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07ab6-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07ab6-123">類型： **[ **DWRITE \_ 字型 \_ 計量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="07ab6-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="07ab6-124">要填入之 [**DWRITE \_ 字型 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="07ab6-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="07ab6-125">此函式所傳回的度量是在字型設計單位中。</span><span class="sxs-lookup"><span data-stu-id="07ab6-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07ab6-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="07ab6-126">Return value</span></span>

<span data-ttu-id="07ab6-127">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="07ab6-127">Type: **HRESULT**</span></span>

<span data-ttu-id="07ab6-128">標準 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="07ab6-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="07ab6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="07ab6-129">Requirements</span></span>



| <span data-ttu-id="07ab6-130">需求</span><span class="sxs-lookup"><span data-stu-id="07ab6-130">Requirement</span></span> | <span data-ttu-id="07ab6-131">值</span><span class="sxs-lookup"><span data-stu-id="07ab6-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07ab6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="07ab6-132">Library</span></span><br/> | <dl> <span data-ttu-id="07ab6-133"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07ab6-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="07ab6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07ab6-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="07ab6-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ab6-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07ab6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07ab6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ab6-137">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="07ab6-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="07ab6-138">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="07ab6-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 


---
title: IDWriteFactory2 CreateCustomRenderingParams 方法
description: 使用指定的屬性建立呈現參數物件。
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- CreateCustomRenderingParams 方法直接寫入
- CreateCustomRenderingParams 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，CreateCustomRenderingParams 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384929"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="1ae75-106">IDWriteFactory2：： CreateCustomRenderingParams 方法</span><span class="sxs-lookup"><span data-stu-id="1ae75-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="1ae75-107">使用指定的屬性建立呈現參數物件。</span><span class="sxs-lookup"><span data-stu-id="1ae75-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae75-108">語法</span><span class="sxs-lookup"><span data-stu-id="1ae75-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="1ae75-109">參數</span><span class="sxs-lookup"><span data-stu-id="1ae75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae75-110">*伽 瑪*</span><span class="sxs-lookup"><span data-stu-id="1ae75-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-111">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-111">Type: **FLOAT**</span></span>

<span data-ttu-id="1ae75-112">用於 gamma 更正的 gamma 值，必須大於零且不能超過256。</span><span class="sxs-lookup"><span data-stu-id="1ae75-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-113">*enhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="1ae75-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-114">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-114">Type: **FLOAT**</span></span>

<span data-ttu-id="1ae75-115">對比增強功能（零或更大）的數量。</span><span class="sxs-lookup"><span data-stu-id="1ae75-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-116">*grayscaleEnhancedContrast*</span><span class="sxs-lookup"><span data-stu-id="1ae75-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-117">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-117">Type: **FLOAT**</span></span>

<span data-ttu-id="1ae75-118">對比增強功能（零或更大）的數量。</span><span class="sxs-lookup"><span data-stu-id="1ae75-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-119">*clearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="1ae75-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-120">類型： **FLOAT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-120">Type: **FLOAT**</span></span>

<span data-ttu-id="1ae75-121">ClearType 層級的程度，從 0.0 f (無 ClearType) 到 1.0 f (完整 ClearType) 。</span><span class="sxs-lookup"><span data-stu-id="1ae75-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-122">*pixelGeometry*</span><span class="sxs-lookup"><span data-stu-id="1ae75-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-123">類型： **[ **DWRITE \_ 圖元 \_ 幾何**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="1ae75-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="1ae75-124">裝置圖元的幾何。</span><span class="sxs-lookup"><span data-stu-id="1ae75-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-125">*renderingMode*</span><span class="sxs-lookup"><span data-stu-id="1ae75-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-126">類型： **[ **DWRITE \_ 轉譯 \_ 模式**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="1ae75-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="1ae75-127">轉譯字型的方法。</span><span class="sxs-lookup"><span data-stu-id="1ae75-127">Method of rendering glyphs.</span></span> <span data-ttu-id="1ae75-128">在大多數情況下，這應該是 DWRITE 轉譯 \_ \_ 模式 \_ 預設值，以自動使用適當的模式。</span><span class="sxs-lookup"><span data-stu-id="1ae75-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-129">*gridFitMode*</span><span class="sxs-lookup"><span data-stu-id="1ae75-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae75-130">類型： **[ **DWRITE \_ 格線 \_ 擬合 \_ 模式**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="1ae75-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="1ae75-131">如何讓格線符合圖像的輪廓。</span><span class="sxs-lookup"><span data-stu-id="1ae75-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="1ae75-132">在大部分的情況下，這應該是 DWRITE \_ 方格 \_ 符合 \_ 預設值，以自動選擇適當的模式。</span><span class="sxs-lookup"><span data-stu-id="1ae75-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="1ae75-133">*renderingParams* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1ae75-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae75-134">類型： **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ae75-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="1ae75-135">保存新建立的轉譯參數物件，或如果發生失敗，則為 Null。</span><span class="sxs-lookup"><span data-stu-id="1ae75-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae75-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ae75-136">Return value</span></span>

<span data-ttu-id="1ae75-137">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1ae75-137">Type: **HRESULT**</span></span>

<span data-ttu-id="1ae75-138">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1ae75-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ae75-139">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ae75-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae75-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ae75-140">Requirements</span></span>



| <span data-ttu-id="1ae75-141">需求</span><span class="sxs-lookup"><span data-stu-id="1ae75-141">Requirement</span></span> | <span data-ttu-id="1ae75-142">值</span><span class="sxs-lookup"><span data-stu-id="1ae75-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae75-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ae75-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae75-144">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ae75-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1ae75-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ae75-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae75-146">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ae75-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="1ae75-147">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="1ae75-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="1ae75-148">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ae75-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="1ae75-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ae75-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ae75-150"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ae75-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1ae75-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1ae75-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ae75-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ae75-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ae75-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ae75-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae75-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="1ae75-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 


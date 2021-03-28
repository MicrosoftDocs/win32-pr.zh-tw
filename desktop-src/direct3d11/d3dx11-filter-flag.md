---
title: 'D3DX11_FILTER_FLAG 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 材質篩選旗標。
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG 列舉 Direct3D 11
- LPD3DX11_FILTER_FLAG 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974714"
---
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="4dfdb-106">D3DX11 \_ 篩選 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="4dfdb-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="4dfdb-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="4dfdb-108">材質篩選旗標。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dfdb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dfdb-109">Syntax</span></span>


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="4dfdb-110">常數</span><span class="sxs-lookup"><span data-stu-id="4dfdb-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4dfdb-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ 篩選 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-112">不會進行調整或篩選。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="4dfdb-113">來源影像界限外的圖元會假設為透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11 \_ 篩選 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-115">每個目的地圖元都是從來源影像取樣最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ 篩選 \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-117">每個目的地圖元都是從來源影像取樣四個最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="4dfdb-118">當兩個軸的刻度小於2時，此篩選器的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11 \_ 篩選 \_ 三角形**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-120">來源影像中的每個圖元平均占目的地映射。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="4dfdb-121">這是篩選器的最慢。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11 \_ 篩選 \_ 方塊**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-123">每個圖元的計算方式是將來源影像中的 2x2 (x2) box 圖元平均。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="4dfdb-124">只有當目的地的維度為來源的一半時，此篩選才會運作，如同 mipmap 的情況。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ 篩選 \_ 鏡像 \_ U**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-126">U 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ 篩選 \_ 鏡像 \_ V**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-128">在 v 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11 \_ 篩選 \_ 鏡像 \_ W**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-130">在 w 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11 \_ 篩選 \_ 鏡像**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-132">指定此旗標與指定 D3DX \_ 濾波器 \_ 鏡像 \_ U、D3DX \_ FILTER \_ 鏡像 \_ V 和 D3DX \_ 濾波器 \_ mirror （ \_ W 旗標）相同。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11 \_ 篩選 \_ 遞色**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-134">產生的影像必須使用4x4 排序的遞色量演算法進行遞色。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="4dfdb-135">從某種格式轉換成另一種格式時，就會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11 \_ 篩選 \_ 遞色 \_ 擴散**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-137">從某種格式變更為另一種格式時，對影像進行擴散遞色。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ FILTER \_ SRGB \_ IN**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-139">輸入資料是在標準 RGB (sRGB) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="4dfdb-140">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ FILTER \_ SRGB \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-142">輸出資料是在標準 RGB (sRGB) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="4dfdb-143">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4dfdb-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ 篩選 \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="4dfdb-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="4dfdb-145">與 \_ \_ \_ 在 \| D3DX \_ 篩選 \_ srgb 中 \_ 指定 D3DX 篩選 srgb 的方式相同。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="4dfdb-146">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dfdb-147">備註</span><span class="sxs-lookup"><span data-stu-id="4dfdb-147">Remarks</span></span>

<span data-ttu-id="4dfdb-148">D3DX11 會自動執行 gamma 更正 (將色彩資料從 RGB 空間轉換成標準的 RGB 空間，) 載入材質資料時。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="4dfdb-149">當 RGB 資料從 .png 檔案載入至 sRGB 材質時，就會自動完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="4dfdb-150">使用 SRGB 篩選旗標來指出資料是否不需要轉換成 sRGB 空間。</span><span class="sxs-lookup"><span data-stu-id="4dfdb-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dfdb-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dfdb-151">Requirements</span></span>



| <span data-ttu-id="4dfdb-152">需求</span><span class="sxs-lookup"><span data-stu-id="4dfdb-152">Requirement</span></span> | <span data-ttu-id="4dfdb-153">值</span><span class="sxs-lookup"><span data-stu-id="4dfdb-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dfdb-154">標頭</span><span class="sxs-lookup"><span data-stu-id="4dfdb-154">Header</span></span><br/> | <dl> <span data-ttu-id="4dfdb-155"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4dfdb-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dfdb-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dfdb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dfdb-157">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="4dfdb-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 






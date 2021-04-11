---
description: 材質篩選旗標。
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: 'D3DX10_FILTER_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946224"
---
# <a name="d3dx10_filter_flag-enumeration"></a><span data-ttu-id="5b370-103">D3DX10 \_ 篩選 \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="5b370-103">D3DX10\_FILTER\_FLAG enumeration</span></span>

<span data-ttu-id="5b370-104">材質篩選旗標。</span><span class="sxs-lookup"><span data-stu-id="5b370-104">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b370-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b370-105">Syntax</span></span>


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="5b370-106">常數</span><span class="sxs-lookup"><span data-stu-id="5b370-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b370-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ 篩選 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="5b370-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-108">不會進行調整或篩選。</span><span class="sxs-lookup"><span data-stu-id="5b370-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="5b370-109">來源影像界限外的圖元會假設為透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="5b370-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10 \_ 篩選 \_ 點**</span><span class="sxs-lookup"><span data-stu-id="5b370-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-111">每個目的地圖元都是從來源影像取樣最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="5b370-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10 \_ 篩選 \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="5b370-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-113">每個目的地圖元都是從來源影像取樣四個最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="5b370-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="5b370-114">當兩個軸的刻度小於2時，此篩選器的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="5b370-114">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10 \_ 篩選 \_ 三角形**</span><span class="sxs-lookup"><span data-stu-id="5b370-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-116">來源影像中的每個圖元平均占目的地映射。</span><span class="sxs-lookup"><span data-stu-id="5b370-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="5b370-117">這是篩選器的最慢。</span><span class="sxs-lookup"><span data-stu-id="5b370-117">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10 \_ 篩選 \_ 方塊**</span><span class="sxs-lookup"><span data-stu-id="5b370-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-119">每個圖元的計算方式是將來源影像中的 2x2 (x2) box 圖元平均。</span><span class="sxs-lookup"><span data-stu-id="5b370-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="5b370-120">只有當目的地的維度為來源的一半時，此篩選才會運作，如同 mipmap 的情況。</span><span class="sxs-lookup"><span data-stu-id="5b370-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ U**</span><span class="sxs-lookup"><span data-stu-id="5b370-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-122">U 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="5b370-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ V**</span><span class="sxs-lookup"><span data-stu-id="5b370-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-124">在 v 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="5b370-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ 篩選 \_ 鏡像 \_ W**</span><span class="sxs-lookup"><span data-stu-id="5b370-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-126">在 w 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="5b370-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10 \_ 篩選 \_ 鏡像**</span><span class="sxs-lookup"><span data-stu-id="5b370-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-128">指定此旗標與指定 D3DX \_ 濾波器 \_ 鏡像 \_ U、D3DX \_ FILTER \_ 鏡像 \_ V 和 D3DX \_ 濾波器 \_ mirror （ \_ W 旗標）相同。</span><span class="sxs-lookup"><span data-stu-id="5b370-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10 \_ 篩選 \_ 遞色**</span><span class="sxs-lookup"><span data-stu-id="5b370-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-130">產生的影像必須使用4x4 排序的遞色量演算法進行遞色。</span><span class="sxs-lookup"><span data-stu-id="5b370-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="5b370-131">從某種格式轉換成另一種格式時，就會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="5b370-131">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10 \_ 篩選 \_ 遞色 \_ 擴散**</span><span class="sxs-lookup"><span data-stu-id="5b370-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-133">從某種格式變更為另一種格式時，對影像進行擴散遞色。</span><span class="sxs-lookup"><span data-stu-id="5b370-133">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ FILTER \_ SRGB \_ IN**</span><span class="sxs-lookup"><span data-stu-id="5b370-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-135">輸入資料是在標準 RGB (sRGB) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="5b370-135">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="5b370-136">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5b370-136">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ FILTER \_ SRGB \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="5b370-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-138">輸出資料是在標準 RGB (sRGB) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="5b370-138">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="5b370-139">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5b370-139">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5b370-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ 篩選 \_ SRGB**</span><span class="sxs-lookup"><span data-stu-id="5b370-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="5b370-141">與 \_ \_ \_ 在 \| D3DX \_ 篩選 \_ srgb 中 \_ 指定 D3DX 篩選 srgb 的方式相同。</span><span class="sxs-lookup"><span data-stu-id="5b370-141">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="5b370-142">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5b370-142">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b370-143">備註</span><span class="sxs-lookup"><span data-stu-id="5b370-143">Remarks</span></span>

<span data-ttu-id="5b370-144">D3DX10 會自動執行 gamma 更正 (將色彩資料從 RGB 空間轉換成標準的 RGB 空間，) 載入材質資料時。</span><span class="sxs-lookup"><span data-stu-id="5b370-144">D3DX10 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="5b370-145">當 RGB 資料從 .png 檔案載入至 sRGB 材質時，就會自動完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="5b370-145">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="5b370-146">使用 SRGB 篩選旗標來指出資料是否不需要轉換成 sRGB 空間。</span><span class="sxs-lookup"><span data-stu-id="5b370-146">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b370-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b370-147">Requirements</span></span>



| <span data-ttu-id="5b370-148">需求</span><span class="sxs-lookup"><span data-stu-id="5b370-148">Requirement</span></span> | <span data-ttu-id="5b370-149">值</span><span class="sxs-lookup"><span data-stu-id="5b370-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b370-150">標頭</span><span class="sxs-lookup"><span data-stu-id="5b370-150">Header</span></span><br/> | <dl> <span data-ttu-id="5b370-151"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b370-151"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b370-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b370-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b370-153">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="5b370-153">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 





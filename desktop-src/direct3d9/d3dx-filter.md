---
description: 下列旗標用來指定要在材質中操作的通道。
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997325"
---
# <a name="d3dx_filter"></a><span data-ttu-id="449fd-103">D3DX \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="449fd-103">D3DX\_FILTER</span></span>

<span data-ttu-id="449fd-104">下列旗標用來指定要在材質中操作的通道。</span><span class="sxs-lookup"><span data-stu-id="449fd-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="449fd-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="449fd-105">\#define</span></span>                | <span data-ttu-id="449fd-106">Description</span><span class="sxs-lookup"><span data-stu-id="449fd-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="449fd-107">D3DX \_ 篩選 \_ 無</span><span class="sxs-lookup"><span data-stu-id="449fd-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="449fd-108">不會進行調整或篩選。</span><span class="sxs-lookup"><span data-stu-id="449fd-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="449fd-109">來源影像界限外的圖元會假設為透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="449fd-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="449fd-110">D3DX \_ 篩選 \_ 點</span><span class="sxs-lookup"><span data-stu-id="449fd-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="449fd-111">每個目的地圖元都是從來源影像取樣最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="449fd-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="449fd-112">D3DX \_ 篩選 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="449fd-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="449fd-113">每個目的地圖元都是從來源影像取樣四個最接近的圖元來計算。</span><span class="sxs-lookup"><span data-stu-id="449fd-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="449fd-114">當兩個軸的刻度小於2時，此篩選器的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="449fd-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="449fd-115">D3DX \_ 篩選 \_ 三角形</span><span class="sxs-lookup"><span data-stu-id="449fd-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="449fd-116">來源影像中的每個圖元平均占目的地映射。</span><span class="sxs-lookup"><span data-stu-id="449fd-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="449fd-117">這是篩選器的最慢。</span><span class="sxs-lookup"><span data-stu-id="449fd-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="449fd-118">D3DX \_ 篩選 \_ 方塊</span><span class="sxs-lookup"><span data-stu-id="449fd-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="449fd-119">每個圖元的計算方式是將來源影像中的 2x2 (x2) box 圖元平均。</span><span class="sxs-lookup"><span data-stu-id="449fd-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="449fd-120">只有當目的地的維度為來源的一半時，此篩選才會運作，如同 mipmap 的情況。</span><span class="sxs-lookup"><span data-stu-id="449fd-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="449fd-121">D3DX \_ 篩選 \_ 鏡像 \_ U</span><span class="sxs-lookup"><span data-stu-id="449fd-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="449fd-122">U 軸上材質邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="449fd-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="449fd-123">D3DX \_ 篩選 \_ 鏡像 \_ V</span><span class="sxs-lookup"><span data-stu-id="449fd-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="449fd-124">在 v 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="449fd-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="449fd-125">D3DX \_ 篩選 \_ 鏡像 \_ W</span><span class="sxs-lookup"><span data-stu-id="449fd-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="449fd-126">在 w 軸上紋理邊緣的圖元應進行鏡像，而不會換行。</span><span class="sxs-lookup"><span data-stu-id="449fd-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="449fd-127">D3DX \_ 篩選 \_ 鏡像</span><span class="sxs-lookup"><span data-stu-id="449fd-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="449fd-128">指定此旗標與指定 D3DX \_ 濾波器 \_ 鏡像 \_ U、D3DX \_ FILTER \_ 鏡像 \_ V 和 D3DX \_ 濾波器 \_ mirror （ \_ W 旗標）相同。</span><span class="sxs-lookup"><span data-stu-id="449fd-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="449fd-129">D3DX \_ 篩選 \_ 遞色</span><span class="sxs-lookup"><span data-stu-id="449fd-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="449fd-130">產生的影像必須使用4x4 排序的遞色量演算法進行遞色。</span><span class="sxs-lookup"><span data-stu-id="449fd-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="449fd-131">D3DX \_ FILTER \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="449fd-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="449fd-132">輸入資料位於 sRGB (gamma 2.2) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="449fd-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="449fd-133">D3DX \_ FILTER \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="449fd-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="449fd-134">輸出資料位於 sRGB (gamma 2.2) 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="449fd-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="449fd-135">D3DX \_ 篩選 \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="449fd-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="449fd-136">與 \_ \_ \_ 在 \| D3DX \_ 篩選 \_ srgb 中 \_ 指定 D3DX 篩選 srgb 的方式相同。</span><span class="sxs-lookup"><span data-stu-id="449fd-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="449fd-137">每個有效的篩選都必須只包含下列其中一個旗標： D3DX \_ filter \_ NONE、D3DX \_ FILTER \_ POINT、D3DX \_ filter \_ 線性、D3DX \_ filter \_ 三角形或 D3DX \_ filter \_ BOX。</span><span class="sxs-lookup"><span data-stu-id="449fd-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="449fd-138">此外，您可以使用或運算子，以有效的篩選準則來指定下列一個或多個選擇性旗標： D3DX \_ filter \_ mirror \_ U、D3DX \_ FILTER \_ mirror \_ V、D3DX \_ filter \_ mirror \_ W、D3DX \_ filter \_ 鏡像、D3DX \_ filter \_ 遞色、D3DX \_ filter \_ srgb \_ IN、D3DX filter \_ \_ srgb \_ OUT 或 D3DX \_ filter \_ srgb。</span><span class="sxs-lookup"><span data-stu-id="449fd-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="449fd-139">指定 \_ 這個參數的 D3DX 預設值，通常相當於指定 D3DX \_ 濾波器 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="449fd-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="449fd-140">不過，D3DX \_ 預設值可以有不同的意義，視使用篩選的方法而定。</span><span class="sxs-lookup"><span data-stu-id="449fd-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="449fd-141">例如：</span><span class="sxs-lookup"><span data-stu-id="449fd-141">For example:</span></span>

-   <span data-ttu-id="449fd-142">使用 [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)時，D3DX \_ 預設對應至 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="449fd-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="449fd-143">使用 [**D3DXFilterTexture**](d3dxfiltertexture.md)時， \_ \_ \_ 如果紋理大小是2的乘冪，D3DX 預設會對應到 D3DX 篩選方塊，否則會使用 D3DX \_ 篩選方塊 \_ \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="449fd-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="449fd-144">參考每個方法，以查看如何對應 D3DX \_ 預設篩選的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="449fd-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="449fd-145">常數資訊</span><span class="sxs-lookup"><span data-stu-id="449fd-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="449fd-146">標頭</span><span class="sxs-lookup"><span data-stu-id="449fd-146">Header</span></span>                   | <span data-ttu-id="449fd-147">d3dx9tex。h</span><span class="sxs-lookup"><span data-stu-id="449fd-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="449fd-148">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="449fd-148">Minimum operating system</span></span> | <span data-ttu-id="449fd-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="449fd-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="449fd-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="449fd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="449fd-151">D3DX 常數</span><span class="sxs-lookup"><span data-stu-id="449fd-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




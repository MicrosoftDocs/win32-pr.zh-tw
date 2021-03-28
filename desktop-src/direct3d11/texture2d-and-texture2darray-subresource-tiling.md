---
title: Texture2D 和 Texture2DArray 子資源拼貼
description: 這些表格顯示了 Texture2D 和 Texture2DArray 子資源拼接的方式。
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375969"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="3b98f-103">Texture2D 和 Texture2DArray 子資源拼貼</span><span class="sxs-lookup"><span data-stu-id="3b98f-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="3b98f-104">這些表格顯示 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源的並排顯示方式。</span><span class="sxs-lookup"><span data-stu-id="3b98f-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="3b98f-105">這些表格中的數值並未計入結尾 mip 包裝。</span><span class="sxs-lookup"><span data-stu-id="3b98f-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="3b98f-106">下表顯示了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和多重採樣次數為 1 之 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源拼接的方式。</span><span class="sxs-lookup"><span data-stu-id="3b98f-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="3b98f-107">位元數/像素 (1 個樣本/像素)</span><span class="sxs-lookup"><span data-stu-id="3b98f-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="3b98f-108">磚的維度 (像素，寬 x 高)</span><span class="sxs-lookup"><span data-stu-id="3b98f-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="3b98f-109">8</span><span class="sxs-lookup"><span data-stu-id="3b98f-109">8</span></span>                           | <span data-ttu-id="3b98f-110">256 x 256</span><span class="sxs-lookup"><span data-stu-id="3b98f-110">256x256</span></span>                       |
| <span data-ttu-id="3b98f-111">16</span><span class="sxs-lookup"><span data-stu-id="3b98f-111">16</span></span>                          | <span data-ttu-id="3b98f-112">256 x 128</span><span class="sxs-lookup"><span data-stu-id="3b98f-112">256x128</span></span>                       |
| <span data-ttu-id="3b98f-113">32</span><span class="sxs-lookup"><span data-stu-id="3b98f-113">32</span></span>                          | <span data-ttu-id="3b98f-114">128 x 128</span><span class="sxs-lookup"><span data-stu-id="3b98f-114">128x128</span></span>                       |
| <span data-ttu-id="3b98f-115">64</span><span class="sxs-lookup"><span data-stu-id="3b98f-115">64</span></span>                          | <span data-ttu-id="3b98f-116">128 x 64</span><span class="sxs-lookup"><span data-stu-id="3b98f-116">128x64</span></span>                        |
| <span data-ttu-id="3b98f-117">128</span><span class="sxs-lookup"><span data-stu-id="3b98f-117">128</span></span>                         | <span data-ttu-id="3b98f-118">64x64</span><span class="sxs-lookup"><span data-stu-id="3b98f-118">64x64</span></span>                         |
| <span data-ttu-id="3b98f-119">BC1,4</span><span class="sxs-lookup"><span data-stu-id="3b98f-119">BC1,4</span></span>                       | <span data-ttu-id="3b98f-120">512 x 256</span><span class="sxs-lookup"><span data-stu-id="3b98f-120">512x256</span></span>                       |
| <span data-ttu-id="3b98f-121">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="3b98f-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="3b98f-122">256 x 256</span><span class="sxs-lookup"><span data-stu-id="3b98f-122">256x256</span></span>                       |



 

<span data-ttu-id="3b98f-123">並排顯示的資源不支援格式位元數目為 96 bpp 格式、影片格式、DXGI \_ 格式 \_ R1 \_ UNORM、dxgi \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM 和 dxgi \_ 格式 \_ R8R8 \_ G8B8 UNORM \_ 。</span><span class="sxs-lookup"><span data-stu-id="3b98f-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="3b98f-124">下表顯示了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和多重採樣次數超過 1 之 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源拼接的方式。</span><span class="sxs-lookup"><span data-stu-id="3b98f-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="3b98f-125">多級取樣計數</span><span class="sxs-lookup"><span data-stu-id="3b98f-125">Multisample Count</span></span>           | <span data-ttu-id="3b98f-126"> (WxH 來分割上方的磚維度) </span><span class="sxs-lookup"><span data-stu-id="3b98f-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="3b98f-127">1</span><span class="sxs-lookup"><span data-stu-id="3b98f-127">1</span></span>                           | <span data-ttu-id="3b98f-128">1 x 1</span><span class="sxs-lookup"><span data-stu-id="3b98f-128">1x1</span></span>                           |
| <span data-ttu-id="3b98f-129">2</span><span class="sxs-lookup"><span data-stu-id="3b98f-129">2</span></span>                           | <span data-ttu-id="3b98f-130">2 x 1</span><span class="sxs-lookup"><span data-stu-id="3b98f-130">2x1</span></span>                           |
| <span data-ttu-id="3b98f-131">4</span><span class="sxs-lookup"><span data-stu-id="3b98f-131">4</span></span>                           | <span data-ttu-id="3b98f-132">2 x 2</span><span class="sxs-lookup"><span data-stu-id="3b98f-132">2x2</span></span>                           |
| <span data-ttu-id="3b98f-133">8</span><span class="sxs-lookup"><span data-stu-id="3b98f-133">8</span></span>                           | <span data-ttu-id="3b98f-134">4 x 2</span><span class="sxs-lookup"><span data-stu-id="3b98f-134">4x2</span></span>                           |
| <span data-ttu-id="3b98f-135">16</span><span class="sxs-lookup"><span data-stu-id="3b98f-135">16</span></span>                          | <span data-ttu-id="3b98f-136">4x4</span><span class="sxs-lookup"><span data-stu-id="3b98f-136">4x4</span></span>                           |



 

<span data-ttu-id="3b98f-137"> (只需要取樣計數1和4，而且可讓磚的資源支援) 。</span><span class="sxs-lookup"><span data-stu-id="3b98f-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="3b98f-138">並排顯示的資源目前不支援2、8和16，但仍會顯示。</span><span class="sxs-lookup"><span data-stu-id="3b98f-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="3b98f-139">即使磚的資源不支援，您也可以選擇支援2、8及/或16個取樣的多重取樣消除鋸齒， (MSAA) 模式的非並排資源。</span><span class="sxs-lookup"><span data-stu-id="3b98f-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="3b98f-140">使用大於1的取樣計數來將資源並排顯示，無法使用 128 bpp 格式。</span><span class="sxs-lookup"><span data-stu-id="3b98f-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b98f-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b98f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b98f-142">磚式資源的區域如何並排顯示</span><span class="sxs-lookup"><span data-stu-id="3b98f-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 
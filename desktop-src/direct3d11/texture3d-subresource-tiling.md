---
title: Texture3D 子資源拼貼
description: 下表顯示了 Texture3D 子資源的拼接方式。
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991026"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="4909e-103">Texture3D 子資源拼貼</span><span class="sxs-lookup"><span data-stu-id="4909e-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="4909e-104">下表說明 [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) 子資源如何並排顯示。</span><span class="sxs-lookup"><span data-stu-id="4909e-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="4909e-105">此表格中的數值並未計入結尾 mip 包裝。</span><span class="sxs-lookup"><span data-stu-id="4909e-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="4909e-106">此表格利用了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 拼接，將 x 及 y 維度各除以 4，並且增加了 16 層的深度。</span><span class="sxs-lookup"><span data-stu-id="4909e-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="4909e-107">所有第一個平面的磚 (2D 磚的平面定義了前 16 層深度) 都會在後續平面之前顯示。</span><span class="sxs-lookup"><span data-stu-id="4909e-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="4909e-108">磚資源的 [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d)支援不會在初始的並排資源執行中公開，但所需的磚圖形會在此列出，因為未來版本中可能會考慮到支援。</span><span class="sxs-lookup"><span data-stu-id="4909e-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="4909e-109">位元數/像素 (1 個樣本/像素)</span><span class="sxs-lookup"><span data-stu-id="4909e-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="4909e-110">磚尺寸 (像素，寬 x 高 x 深)</span><span class="sxs-lookup"><span data-stu-id="4909e-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="4909e-111">8</span><span class="sxs-lookup"><span data-stu-id="4909e-111">8</span></span>                           | <span data-ttu-id="4909e-112">64 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="4909e-112">64x32x32</span></span>                        |
| <span data-ttu-id="4909e-113">16</span><span class="sxs-lookup"><span data-stu-id="4909e-113">16</span></span>                          | <span data-ttu-id="4909e-114">32 x 32 x 32</span><span class="sxs-lookup"><span data-stu-id="4909e-114">32x32x32</span></span>                        |
| <span data-ttu-id="4909e-115">32</span><span class="sxs-lookup"><span data-stu-id="4909e-115">32</span></span>                          | <span data-ttu-id="4909e-116">32 x 32 x 16</span><span class="sxs-lookup"><span data-stu-id="4909e-116">32x32x16</span></span>                        |
| <span data-ttu-id="4909e-117">64</span><span class="sxs-lookup"><span data-stu-id="4909e-117">64</span></span>                          | <span data-ttu-id="4909e-118">32 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="4909e-118">32x16x16</span></span>                        |
| <span data-ttu-id="4909e-119">128</span><span class="sxs-lookup"><span data-stu-id="4909e-119">128</span></span>                         | <span data-ttu-id="4909e-120">16 x 16 x 16</span><span class="sxs-lookup"><span data-stu-id="4909e-120">16x16x16</span></span>                        |
| <span data-ttu-id="4909e-121">BC1,4</span><span class="sxs-lookup"><span data-stu-id="4909e-121">BC1,4</span></span>                       | <span data-ttu-id="4909e-122">128 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="4909e-122">128x64x16</span></span>                       |
| <span data-ttu-id="4909e-123">BC2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="4909e-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="4909e-124">64 x 64 x 16</span><span class="sxs-lookup"><span data-stu-id="4909e-124">64x64x16</span></span>                        |



 

<span data-ttu-id="4909e-125">並排顯示的資源不支援格式位元數目為 96 bpp 格式、影片格式、DXGI \_ 格式 \_ R1 \_ UNORM、dxgi \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM 和 dxgi \_ 格式 \_ R8R8 \_ G8B8 UNORM \_ 。</span><span class="sxs-lookup"><span data-stu-id="4909e-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4909e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="4909e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4909e-127">磚式資源的區域如何並排顯示</span><span class="sxs-lookup"><span data-stu-id="4909e-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 
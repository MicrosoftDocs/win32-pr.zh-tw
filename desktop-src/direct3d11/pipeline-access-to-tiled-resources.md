---
title: 磚資源的管線存取
description: 磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682846"
---
# <a name="pipeline-access-to-tiled-resources"></a><span data-ttu-id="0f325-103">磚資源的管線存取</span><span class="sxs-lookup"><span data-stu-id="0f325-103">Pipeline access to tiled resources</span></span>

<span data-ttu-id="0f325-104">磚資源可用於著色器資源檢視 (SRV) 、轉譯目標視圖 (RTV) 、深度樣板視圖 (DSV) 和未排序的存取權視圖 (UAV) ，以及某些未使用視圖的系結點，例如頂點緩衝區系結。</span><span class="sxs-lookup"><span data-stu-id="0f325-104">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <span data-ttu-id="0f325-105">如需支援的系結清單，請參閱 [建立資源的參數](tiled-resource-creation-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0f325-105">For the list of supported bindings, see [Tiled resource creation parameters](tiled-resource-creation-parameters.md).</span></span> <span data-ttu-id="0f325-106">複製 \* 作業也適用于並排顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="0f325-106">Copy\* operations also work on tiled resources.</span></span>

<span data-ttu-id="0f325-107">如果有一個或多個檢視中的多個磚座標繫結相同的記憶體位置、從不同路徑讀取和寫入方式到相同記憶體，會發生不確定和非重複順序的記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="0f325-107">If multiple tile coordinates in one or more views is bound to the same memory location, reads and writes from different paths to the same memory will occur in a non-deterministic and non-repeatable order of memory accesses.</span></span>

<span data-ttu-id="0f325-108">如果從著色器的記憶體存取使用量後所有磚對應到獨特的磚，所有實作到以非磚方式具有相同的記憶體內容的表面的行為是相同的。</span><span class="sxs-lookup"><span data-stu-id="0f325-108">If all tiles behind a memory access footprint from a shader are mapped to unique tiles, behavior is identical on all implementations to the surface having the same memory contents in a non-tiled fashion.</span></span>

<span data-ttu-id="0f325-109">本節提供有關管線存取並排資源的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0f325-109">This section provides more info about pipeline access to tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0f325-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="0f325-110">In this section</span></span>



| <span data-ttu-id="0f325-111">主題</span><span class="sxs-lookup"><span data-stu-id="0f325-111">Topic</span></span>                                                                                                              | <span data-ttu-id="0f325-112">描述</span><span class="sxs-lookup"><span data-stu-id="0f325-112">Description</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f325-113">非對應磚的 SRV 行為</span><span class="sxs-lookup"><span data-stu-id="0f325-113">SRV behavior with non-mapped tiles</span></span>](srv-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="0f325-114">著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。</span><span class="sxs-lookup"><span data-stu-id="0f325-114">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <br/>                                          |
| [<span data-ttu-id="0f325-115">非對應磚的 UAV 行為</span><span class="sxs-lookup"><span data-stu-id="0f325-115">UAV behavior with non-mapped tiles</span></span>](uav-behavior-with-non-mapped-tiles.md)<br/>                            | <span data-ttu-id="0f325-116">未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。</span><span class="sxs-lookup"><span data-stu-id="0f325-116">Behavior of unordered access view (UAV) reads and writes depends on the level of hardware support.</span></span> <br/>                                                            |
| [<span data-ttu-id="0f325-117">非對應磚的轉譯器行為</span><span class="sxs-lookup"><span data-stu-id="0f325-117">Rasterizer behavior with non-mapped tiles</span></span>](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | <span data-ttu-id="0f325-118">本節說明非對應磚的轉譯器行為。</span><span class="sxs-lookup"><span data-stu-id="0f325-118">This section describes rasterizer behavior with non-mapped tiles.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0f325-119">重複對應的磚存取限制</span><span class="sxs-lookup"><span data-stu-id="0f325-119">Tile access limitations with duplicate mappings</span></span>](tile-access-limitations-with-duplicate-mappings-.md)<br/> | <span data-ttu-id="0f325-120">本節說明重複對應的磚存取限制。</span><span class="sxs-lookup"><span data-stu-id="0f325-120">This section describes tile access limitations with duplicate mappings.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0f325-121">磚資源紋理取樣功能</span><span class="sxs-lookup"><span data-stu-id="0f325-121">Tiled resources texture sampling features</span></span>](tiled-resources-texture-sampling-features.md)<br/>              | <span data-ttu-id="0f325-122">本節說明並排顯示的資源紋理取樣功能。</span><span class="sxs-lookup"><span data-stu-id="0f325-122">This section describes tiled resources texture sampling features.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0f325-123">HLSL 磚的資源曝光</span><span class="sxs-lookup"><span data-stu-id="0f325-123">HLSL tiled resources exposure</span></span>](hlsl-tiled-resources-exposure.md)<br/>                                      | <span data-ttu-id="0f325-124">需要新的 Microsoft 高階著色器語言 (HLSL) 語法，以支援 [著色器模型 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5)中的磚資源。</span><span class="sxs-lookup"><span data-stu-id="0f325-124">New Microsoft High Level Shader Language (HLSL) syntax is required to support tiled resources in [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5).</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0f325-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f325-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f325-126">磚資源</span><span class="sxs-lookup"><span data-stu-id="0f325-126">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 


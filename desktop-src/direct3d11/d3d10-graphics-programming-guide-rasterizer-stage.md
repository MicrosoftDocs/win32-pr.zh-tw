---
title: 轉譯器階段
description: 點陣化階段會轉換向量資訊 (由圖形或基本類型組成) 為點陣影像 (由像素組成)，以顯示即時 3D 圖形。
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933746"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="fd455-103">轉譯器階段</span><span class="sxs-lookup"><span data-stu-id="fd455-103">Rasterizer Stage</span></span>

<span data-ttu-id="fd455-104">點陣化階段會轉換向量資訊 (由圖形或基本類型組成) 為點陣影像 (由像素組成)，以顯示即時 3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="fd455-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="fd455-105">在點陣化期間，每個基本類型會轉換成像素，同時針對每個基本類型插入每個頂點值。</span><span class="sxs-lookup"><span data-stu-id="fd455-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="fd455-106">點陣化包含裁剪頂點到檢視範圍、執行以 z 相除以提供透視圖、將基本類型對應到 2D 檢視區，以及決定如何叫用像素著色器。</span><span class="sxs-lookup"><span data-stu-id="fd455-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="fd455-107">當使用像素著色器為選擇性時，而轉譯器階段始終會執行裁剪，分割透視圖以將點轉換為同質空間，以及將頂點對應到檢視區。</span><span class="sxs-lookup"><span data-stu-id="fd455-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="fd455-108">進入轉譯器階段的頂點 (x、y、z、w) ，會假設位於同質的剪輯空間中。</span><span class="sxs-lookup"><span data-stu-id="fd455-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="fd455-109">在這個座標空間中，X 軸指向右，Y 指向上，Z 偏離相機。</span><span class="sxs-lookup"><span data-stu-id="fd455-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="fd455-110">您可以使用 [**>id3d11devicecoNtext：:P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) ，並停用深度和樣板測試 (將 [**D3D11 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)) 中的 **DepthEnable** 和 **StencilEnable** 設定為 **FALSE** ，以停用柵格化，方法是告知管線沒有圖元著色器 (將圖元著色器階段設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fd455-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="fd455-111">停用時，不會更新與點陣化相關的管線計數器。</span><span class="sxs-lookup"><span data-stu-id="fd455-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="fd455-112">此外，也提供了 [柵格化規則](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)的完整描述。</span><span class="sxs-lookup"><span data-stu-id="fd455-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="fd455-113">在執行階層式 Z 緩衝區優化的硬體上，您可以在啟用深度和樣板測試時，將圖元著色器階段設定為 **Null** ，藉以啟用載入 z 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fd455-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="fd455-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="fd455-114">In this section</span></span>



| <span data-ttu-id="fd455-115">主題</span><span class="sxs-lookup"><span data-stu-id="fd455-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="fd455-116">描述</span><span class="sxs-lookup"><span data-stu-id="fd455-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd455-117">使用轉譯器階段開始使用</span><span class="sxs-lookup"><span data-stu-id="fd455-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="fd455-118">本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。</span><span class="sxs-lookup"><span data-stu-id="fd455-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="fd455-119">柵格化規則</span><span class="sxs-lookup"><span data-stu-id="fd455-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="fd455-120">點陣化規則定義向量資料對應至點陣資料的方式。</span><span class="sxs-lookup"><span data-stu-id="fd455-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="fd455-121">點陣資料會貼齊至整數位置，該整數位置接著會進行揀選和裁剪 (以繪製像素數目下限)，而每個像素屬性會在傳遞至像素著色器之前進行插入 (從每個頂點屬性)。</span><span class="sxs-lookup"><span data-stu-id="fd455-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fd455-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd455-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd455-123">圖形管線</span><span class="sxs-lookup"><span data-stu-id="fd455-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="fd455-124"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="fd455-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 


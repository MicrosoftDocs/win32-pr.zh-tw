---
description: Direct3D 10 定義了數種基本資源類型的介面：緩衝區和紋理。
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: " (Direct3D 10 圖形) 的資源介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110537"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="1c270-103"> (Direct3D 10 圖形) 的資源介面</span><span class="sxs-lookup"><span data-stu-id="1c270-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="1c270-104">Direct3D 10 定義了數種基本資源類型的介面： [緩衝區](d3d10-graphics-programming-guide-resources-types.md) 和紋理。</span><span class="sxs-lookup"><span data-stu-id="1c270-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="1c270-105">介面</span><span class="sxs-lookup"><span data-stu-id="1c270-105">Interfaces</span></span>                                           | <span data-ttu-id="1c270-106">Description</span><span class="sxs-lookup"><span data-stu-id="1c270-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="1c270-107">**ID3D10Buffer 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="1c270-108">存取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="1c270-109">**ID3D10Resource 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="1c270-110">資源的基類。</span><span class="sxs-lookup"><span data-stu-id="1c270-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="1c270-111">**ID3D10Texture1D 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="1c270-112">存取1D 材質或1D 材質陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="1c270-113">**ID3D10Texture2D 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="1c270-114">存取2D 材質或2D 材質陣列中的資料</span><span class="sxs-lookup"><span data-stu-id="1c270-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="1c270-115">**ID3D10Texture3D 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="1c270-116">存取3D 紋理或3D 紋理陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="1c270-117">應用程式會使用 view 將資源系結至 [管線階段](d3d10-graphics-programming-guide-pipeline-stages.md)。</span><span class="sxs-lookup"><span data-stu-id="1c270-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="1c270-118">此 [視圖](d3d10-graphics-programming-guide-resources-access-views.md) 會定義在轉譯期間存取資源的方式。</span><span class="sxs-lookup"><span data-stu-id="1c270-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="1c270-119">API 包含這些 view 介面。</span><span class="sxs-lookup"><span data-stu-id="1c270-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="1c270-120">介面</span><span class="sxs-lookup"><span data-stu-id="1c270-120">Interfaces</span></span>                                                               | <span data-ttu-id="1c270-121">Description</span><span class="sxs-lookup"><span data-stu-id="1c270-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c270-122">**ID3D10DepthStencilView 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="1c270-123">存取 [深度](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) 樣板材質中的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="1c270-124">**ID3D10RenderTargetView 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="1c270-125">存取轉譯 [目標](d3d10-graphics-programming-guide-resources-creating-textures.md)中的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="1c270-126">**ID3D10ShaderResourceView 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="1c270-127">存取在 Direct3D 10.0 中著色器資源的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="1c270-128">**ID3D10ShaderResourceView1 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="1c270-129">存取在 Direct3D 10.1 中著色器資源的資料。</span><span class="sxs-lookup"><span data-stu-id="1c270-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="1c270-130">**ID3D10View 介面**</span><span class="sxs-lookup"><span data-stu-id="1c270-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="1c270-131">視圖的基類。</span><span class="sxs-lookup"><span data-stu-id="1c270-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="1c270-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c270-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c270-133">資源參考</span><span class="sxs-lookup"><span data-stu-id="1c270-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 

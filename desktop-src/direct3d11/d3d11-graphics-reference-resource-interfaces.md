---
title: " (Direct3D 11 圖形) 的資源介面"
description: 有一些介面適用于兩種基本類型的資源緩衝區和紋理。
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- 介面，Direct3D 11 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d8f01e8d485fcdf575e8aea1a5beeb2184946b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685436"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a><span data-ttu-id="6d752-104"> (Direct3D 11 圖形) 的資源介面</span><span class="sxs-lookup"><span data-stu-id="6d752-104">Resource Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="6d752-105">有一些介面適用于兩種基本類型的資源：緩衝區和紋理。</span><span class="sxs-lookup"><span data-stu-id="6d752-105">There are a number of interfaces for the two basic types of resources: buffers and textures.</span></span> <span data-ttu-id="6d752-106">另外還有一些介面可用於資源的查看。</span><span class="sxs-lookup"><span data-stu-id="6d752-106">There are also interfaces for views of resources.</span></span>

<span data-ttu-id="6d752-107">應用程式會使用 view 將資源系結至管線階段。</span><span class="sxs-lookup"><span data-stu-id="6d752-107">An application uses a view to bind a resource to a pipeline stage.</span></span> <span data-ttu-id="6d752-108">此視圖會定義在轉譯期間存取資源的方式。</span><span class="sxs-lookup"><span data-stu-id="6d752-108">The view defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="6d752-109">本節說明 view 介面。</span><span class="sxs-lookup"><span data-stu-id="6d752-109">This section describes the view interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="6d752-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="6d752-110">In this section</span></span>



| <span data-ttu-id="6d752-111">主題</span><span class="sxs-lookup"><span data-stu-id="6d752-111">Topic</span></span>                                                                       | <span data-ttu-id="6d752-112">描述</span><span class="sxs-lookup"><span data-stu-id="6d752-112">Description</span></span>                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d752-113">**ID3D11Buffer**</span><span class="sxs-lookup"><span data-stu-id="6d752-113">**ID3D11Buffer**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | <span data-ttu-id="6d752-114">緩衝區介面會存取非結構化記憶體的緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-114">A buffer interface accesses a buffer resource, which is unstructured memory.</span></span> <span data-ttu-id="6d752-115">緩衝區通常會儲存頂點或索引資料。</span><span class="sxs-lookup"><span data-stu-id="6d752-115">Buffers typically store vertex or index data.</span></span><br/>                                                                  |
| [<span data-ttu-id="6d752-116">**ID3D11DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="6d752-116">**ID3D11DepthStencilView**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | <span data-ttu-id="6d752-117">深度樣板視圖介面會在深度樣板測試期間存取材質資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-117">A depth-stencil-view interface accesses a texture resource during depth-stencil testing.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6d752-118">**ID3D11RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="6d752-118">**ID3D11RenderTargetView**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | <span data-ttu-id="6d752-119">轉譯目標視圖介面會識別轉譯時可以存取的呈現目標子資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-119">A render-target-view interface identifies the render-target subresources that can be accessed during rendering.</span></span><br/>                                                                             |
| [<span data-ttu-id="6d752-120">**ID3D11RenderTargetView1**</span><span class="sxs-lookup"><span data-stu-id="6d752-120">**ID3D11RenderTargetView1**</span></span>](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | <span data-ttu-id="6d752-121">轉譯目標視圖介面代表可在轉譯期間存取的轉譯目標子資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-121">A render-target-view interface represents the render-target subresources that can be accessed during rendering.</span></span><br/>                                                                             |
| [<span data-ttu-id="6d752-122">**ID3D11Resource**</span><span class="sxs-lookup"><span data-stu-id="6d752-122">**ID3D11Resource**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | <span data-ttu-id="6d752-123">資源介面可提供所有資源的一般動作。</span><span class="sxs-lookup"><span data-stu-id="6d752-123">A resource interface provides common actions on all resources.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="6d752-124">**ID3D11ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="6d752-124">**ID3D11ShaderResourceView**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | <span data-ttu-id="6d752-125">著色器-資源檢視介面會指定著色器在轉譯期間可以存取的子資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-125">A shader-resource-view interface specifies the subresources a shader can access during rendering.</span></span> <span data-ttu-id="6d752-126">著色器資源的範例包括常數緩衝區、材質緩衝區和材質。</span><span class="sxs-lookup"><span data-stu-id="6d752-126">Examples of shader resources include a constant buffer, a texture buffer, and a texture.</span></span><br/>  |
| [<span data-ttu-id="6d752-127">**ID3D11ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="6d752-127">**ID3D11ShaderResourceView1**</span></span>](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | <span data-ttu-id="6d752-128">著色器-資源檢視介面代表著色器在轉譯期間可以存取的子資源。</span><span class="sxs-lookup"><span data-stu-id="6d752-128">A shader-resource-view interface represents the subresources a shader can access during rendering.</span></span> <span data-ttu-id="6d752-129">著色器資源的範例包括常數緩衝區、材質緩衝區和材質。</span><span class="sxs-lookup"><span data-stu-id="6d752-129">Examples of shader resources include a constant buffer, a texture buffer, and a texture.</span></span><br/> |
| [<span data-ttu-id="6d752-130">**ID3D11Texture1D**</span><span class="sxs-lookup"><span data-stu-id="6d752-130">**ID3D11Texture1D**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | <span data-ttu-id="6d752-131">1D 紋理介面會存取材質資料，也就是結構化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-131">A 1D texture interface accesses texel data, which is structured memory.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6d752-132">**ID3D11Texture2D**</span><span class="sxs-lookup"><span data-stu-id="6d752-132">**ID3D11Texture2D**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | <span data-ttu-id="6d752-133">2D 材質介面會管理材質資料，也就是結構化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-133">A 2D texture interface manages texel data, which is structured memory.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="6d752-134">**ID3D11Texture2D1**</span><span class="sxs-lookup"><span data-stu-id="6d752-134">**ID3D11Texture2D1**</span></span>](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | <span data-ttu-id="6d752-135">2D 材質介面代表材質資料，也就是結構化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-135">A 2D texture interface represents texel data, which is structured memory.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="6d752-136">**ID3D11Texture3D**</span><span class="sxs-lookup"><span data-stu-id="6d752-136">**ID3D11Texture3D**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | <span data-ttu-id="6d752-137">3D 紋理介面會存取材質資料，也就是結構化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-137">A 3D texture interface accesses texel data, which is structured memory.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6d752-138">**ID3D11Texture3D1**</span><span class="sxs-lookup"><span data-stu-id="6d752-138">**ID3D11Texture3D1**</span></span>](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | <span data-ttu-id="6d752-139">3D 紋理介面代表材質資料，也就是結構化的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-139">A 3D texture interface represents texel data, which is structured memory.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="6d752-140">**ID3D11UnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="6d752-140">**ID3D11UnorderedAccessView**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | <span data-ttu-id="6d752-141">View 介面會指定在轉譯期間，管線可以存取的資源部分。</span><span class="sxs-lookup"><span data-stu-id="6d752-141">A view interface specifies the parts of a resource the pipeline can access during rendering.</span></span><br/>                                                                                                |
| [<span data-ttu-id="6d752-142">**ID3D11UnorderedAccessView1**</span><span class="sxs-lookup"><span data-stu-id="6d752-142">**ID3D11UnorderedAccessView1**</span></span>](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | <span data-ttu-id="6d752-143">未排序的存取視圖介面代表管線在轉譯期間可以存取的資源部分。</span><span class="sxs-lookup"><span data-stu-id="6d752-143">An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering.</span></span><br/>                                                                             |
| [<span data-ttu-id="6d752-144">**ID3D11View**</span><span class="sxs-lookup"><span data-stu-id="6d752-144">**ID3D11View**</span></span>](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | <span data-ttu-id="6d752-145">View 介面會指定在轉譯期間，管線可以存取的資源部分。</span><span class="sxs-lookup"><span data-stu-id="6d752-145">A view interface specifies the parts of a resource the pipeline can access during rendering.</span></span><br/>                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="6d752-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d752-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d752-147">資源參考</span><span class="sxs-lookup"><span data-stu-id="6d752-147">Resource Reference</span></span>](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 






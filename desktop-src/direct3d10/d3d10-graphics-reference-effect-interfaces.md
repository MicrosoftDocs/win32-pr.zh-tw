---
description: 本節包含下列效果系統介面的相關資訊：
ms.assetid: ebe0afc7-6261-4c96-a54e-9b491e240c03
title: " (Direct3D 10) 的效果介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1946e7b9e3711bf2d79c0876efca1c533e0ff4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688684"
---
# <a name="effect-interfaces-direct3d-10"></a><span data-ttu-id="bbc36-103"> (Direct3D 10) 的效果介面</span><span class="sxs-lookup"><span data-stu-id="bbc36-103">Effect Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="bbc36-104">本節包含下列效果系統介面的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="bbc36-104">This section contains information about the following effect-system interfaces:</span></span>



| <span data-ttu-id="bbc36-105">介面</span><span class="sxs-lookup"><span data-stu-id="bbc36-105">Interfaces</span></span>                                                                                     | <span data-ttu-id="bbc36-106">Description</span><span class="sxs-lookup"><span data-stu-id="bbc36-106">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="bbc36-107">**ID3D10EffectBlendVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-107">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)                       | <span data-ttu-id="bbc36-108">存取 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc36-108">Accesses blend state.</span></span>                                            |
| [<span data-ttu-id="bbc36-109">**ID3D10EffectConstantBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-109">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="bbc36-110">存取材質緩衝區或常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bbc36-110">Accesses a texture-buffer or a constant-buffer.</span></span>                  |
| [<span data-ttu-id="bbc36-111">**ID3D10EffectDepthStencilVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-111">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable)         | <span data-ttu-id="bbc36-112">存取深度範本的狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc36-112">Accesses depth-stencil state.</span></span>                                    |
| [<span data-ttu-id="bbc36-113">**ID3D10EffectDepthStencilViewVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-113">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="bbc36-114">存取深度範本視圖。</span><span class="sxs-lookup"><span data-stu-id="bbc36-114">Accesses a depth-stencil view.</span></span>                                   |
| [<span data-ttu-id="bbc36-115">**ID3D10Effect 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-115">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                                                 | <span data-ttu-id="bbc36-116">封裝一或多個轉譯技術中的管線狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc36-116">Encapsulates pipeline state in one or more rendering techniques.</span></span> |
| <span data-ttu-id="bbc36-117">[**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bbc36-117">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                                               | <span data-ttu-id="bbc36-118">用來讀取 include 檔的使用者執行方法。</span><span class="sxs-lookup"><span data-stu-id="bbc36-118">User-implemented methods for reading include files.</span></span>              |
| [<span data-ttu-id="bbc36-119">**ID3D10EffectMatrixVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-119">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable)                     | <span data-ttu-id="bbc36-120">存取矩陣。</span><span class="sxs-lookup"><span data-stu-id="bbc36-120">Accesses a matrix.</span></span>                                               |
| [<span data-ttu-id="bbc36-121">**ID3D10EffectPass 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-121">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)                                         | <span data-ttu-id="bbc36-122">將效果狀態封裝在傳遞中。</span><span class="sxs-lookup"><span data-stu-id="bbc36-122">Encapsulates effect state in a pass.</span></span>                             |
| [<span data-ttu-id="bbc36-123">**ID3D10EffectPool 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-123">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)                                         | <span data-ttu-id="bbc36-124">識別共用效果變數。</span><span class="sxs-lookup"><span data-stu-id="bbc36-124">Identifies shared-effect variables.</span></span>                              |
| [<span data-ttu-id="bbc36-125">**ID3D10EffectRasterizerVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-125">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)             | <span data-ttu-id="bbc36-126">存取轉譯器狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc36-126">Accesses rasterizer state.</span></span>                                       |
| [<span data-ttu-id="bbc36-127">**ID3D10EffectRenderTargetViewVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-127">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="bbc36-128">存取呈現目標。</span><span class="sxs-lookup"><span data-stu-id="bbc36-128">Accesses a render target.</span></span>                                        |
| [<span data-ttu-id="bbc36-129">**ID3D10EffectSamplerVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-129">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)                   | <span data-ttu-id="bbc36-130">存取取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc36-130">Accesses sampler state.</span></span>                                          |
| [<span data-ttu-id="bbc36-131">**ID3D10EffectScalarVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-131">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable)                     | <span data-ttu-id="bbc36-132">存取純量變數。</span><span class="sxs-lookup"><span data-stu-id="bbc36-132">Accesses a scalar variable.</span></span>                                      |
| [<span data-ttu-id="bbc36-133">**ID3D10EffectShaderResourceVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-133">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="bbc36-134">存取著色器資源。</span><span class="sxs-lookup"><span data-stu-id="bbc36-134">Accesses a shader resource.</span></span>                                      |
| [<span data-ttu-id="bbc36-135">**ID3D10EffectShaderVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-135">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable)                     | <span data-ttu-id="bbc36-136">存取著色器變數。</span><span class="sxs-lookup"><span data-stu-id="bbc36-136">Accesses a shader variable.</span></span>                                      |
| [<span data-ttu-id="bbc36-137">**ID3D10EffectStringVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-137">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable)                     | <span data-ttu-id="bbc36-138">存取字串。</span><span class="sxs-lookup"><span data-stu-id="bbc36-138">Accesses a string.</span></span>                                               |
| [<span data-ttu-id="bbc36-139">**ID3D10EffectTechnique 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-139">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique)                               | <span data-ttu-id="bbc36-140">封裝一或多個階段。</span><span class="sxs-lookup"><span data-stu-id="bbc36-140">Encapsulates one or more passes.</span></span>                                 |
| [<span data-ttu-id="bbc36-141">**ID3D10EffectType 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-141">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                                         | <span data-ttu-id="bbc36-142">實行存取效果變數的方法。</span><span class="sxs-lookup"><span data-stu-id="bbc36-142">Implements methods for accessing effect variables.</span></span>               |
| [<span data-ttu-id="bbc36-143">**ID3D10EffectVectorVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="bbc36-143">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable)                     | <span data-ttu-id="bbc36-144">存取 vector。</span><span class="sxs-lookup"><span data-stu-id="bbc36-144">Accesses a vector.</span></span>                                               |



 

<span data-ttu-id="bbc36-145">效果架構中有兩種介面：轉譯介面以轉譯效果和反映介面，以使用 API 來取得和設定效果變數。</span><span class="sxs-lookup"><span data-stu-id="bbc36-145">There are two kinds of interfaces in the effect framework: rendering interfaces for rendering an effect and reflection interfaces for getting and setting effect variables with the API.</span></span> <span data-ttu-id="bbc36-146">所有反映介面都是衍生自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)。</span><span class="sxs-lookup"><span data-stu-id="bbc36-146">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbc36-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbc36-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc36-148">效果參考</span><span class="sxs-lookup"><span data-stu-id="bbc36-148">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 

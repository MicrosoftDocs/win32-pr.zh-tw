---
description: 效果系統會定義許多用於管理效果狀態的介面。 有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: " (Direct3D 10) 的效果系統介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110384"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="4dd7b-104"> (Direct3D 10) 的效果系統介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="4dd7b-105">效果系統會定義許多用於管理效果狀態的介面。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="4dd7b-106">有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="4dd7b-107">效果執行時間介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="4dd7b-108">效果反映介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="4dd7b-109">效果執行時間介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="4dd7b-110">使用執行時間介面來呈現效果。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="4dd7b-111">執行時間介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="4dd7b-112">Description</span><span class="sxs-lookup"><span data-stu-id="4dd7b-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="4dd7b-113">**ID3D10Effect 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="4dd7b-114">收集一或多個用於轉譯的技巧。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="4dd7b-115">[**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dd7b-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="4dd7b-116">在讀取包含檔案時，用來加入自訂行為的介面。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="4dd7b-117">**ID3D10EffectPass 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="4dd7b-118">狀態指派的集合。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="4dd7b-119">**ID3D10EffectPool 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="4dd7b-120">建立要在效果之間共用之變數的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="4dd7b-121">**ID3D10EffectTechnique 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="4dd7b-122">一或多個傳遞的集合。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="4dd7b-123">效果反映介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="4dd7b-124">反映會在效果系統中執行，以支援讀取 (和寫入) 效果狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="4dd7b-125">有多種方式可存取效果變數。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="4dd7b-126">設定效果狀態的群組</span><span class="sxs-lookup"><span data-stu-id="4dd7b-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="4dd7b-127">使用這些介面來取得和設定一組狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="4dd7b-128">反映介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="4dd7b-129">Description</span><span class="sxs-lookup"><span data-stu-id="4dd7b-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="4dd7b-130">**ID3D10EffectBlendVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="4dd7b-131">取得並設定 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="4dd7b-132">**ID3D10EffectDepthStencilVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="4dd7b-133">取得並設定深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="4dd7b-134">**ID3D10EffectRasterizerVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="4dd7b-135">取得並設定轉譯器狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="4dd7b-136">**ID3D10EffectSamplerVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="4dd7b-137">取得並設定取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="4dd7b-138">設定效果資源</span><span class="sxs-lookup"><span data-stu-id="4dd7b-138">Setting Effect Resources</span></span>

<span data-ttu-id="4dd7b-139">使用這些介面來取得和設定資源。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="4dd7b-140">反映介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="4dd7b-141">Description</span><span class="sxs-lookup"><span data-stu-id="4dd7b-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="4dd7b-142">**ID3D10EffectConstantBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="4dd7b-143">存取材質緩衝區或常數緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="4dd7b-144">**ID3D10EffectDepthStencilViewVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="4dd7b-145">存取深度樣板資源中的資料。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="4dd7b-146">**ID3D10EffectRenderTargetViewVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="4dd7b-147">存取轉譯目標中的資料。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="4dd7b-148">**ID3D10EffectShaderResourceVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="4dd7b-149">存取著色器資源中的資料。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="4dd7b-150">設定其他效果變數</span><span class="sxs-lookup"><span data-stu-id="4dd7b-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="4dd7b-151">使用這些介面可依變數類型來取得和設定狀態。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="4dd7b-152">反映介面</span><span class="sxs-lookup"><span data-stu-id="4dd7b-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="4dd7b-153">Description</span><span class="sxs-lookup"><span data-stu-id="4dd7b-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="4dd7b-154">**ID3D10EffectMatrixVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="4dd7b-155">取得和設定矩陣。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="4dd7b-156">**ID3D10EffectScalarVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="4dd7b-157">取得和設定純量。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="4dd7b-158">**ID3D10EffectShaderVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="4dd7b-159">取得和設定著色器變數。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="4dd7b-160">**ID3D10EffectStringVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="4dd7b-161">取得並設定字串。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="4dd7b-162">**ID3D10EffectType 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="4dd7b-163">取得變數型別。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="4dd7b-164">**ID3D10EffectVectorVariable 介面**</span><span class="sxs-lookup"><span data-stu-id="4dd7b-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="4dd7b-165">取得和設定向量。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="4dd7b-166">所有反映介面都是衍生自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable)。</span><span class="sxs-lookup"><span data-stu-id="4dd7b-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dd7b-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="4dd7b-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd7b-168">影響</span><span class="sxs-lookup"><span data-stu-id="4dd7b-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="4dd7b-169">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="4dd7b-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 

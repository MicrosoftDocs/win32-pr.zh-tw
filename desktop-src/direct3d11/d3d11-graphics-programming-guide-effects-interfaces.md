---
title: " (Direct3D 11) 的效果系統介面"
description: 效果系統會定義許多用於管理效果狀態的介面。
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671896"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="e0922-103"> (Direct3D 11) 的效果系統介面</span><span class="sxs-lookup"><span data-stu-id="e0922-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="e0922-104">效果系統會定義許多用於管理效果狀態的介面。</span><span class="sxs-lookup"><span data-stu-id="e0922-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="e0922-105">有兩種類型的介面：執行時間用來呈現效果和反映介面以取得和設定效果變數的介面。</span><span class="sxs-lookup"><span data-stu-id="e0922-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="e0922-106">效果執行時間介面</span><span class="sxs-lookup"><span data-stu-id="e0922-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="e0922-107">效果反映介面</span><span class="sxs-lookup"><span data-stu-id="e0922-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="e0922-108">效果執行時間介面</span><span class="sxs-lookup"><span data-stu-id="e0922-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="e0922-109">使用執行時間介面來呈現效果。</span><span class="sxs-lookup"><span data-stu-id="e0922-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="e0922-110">執行時間介面</span><span class="sxs-lookup"><span data-stu-id="e0922-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="e0922-111">Description</span><span class="sxs-lookup"><span data-stu-id="e0922-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e0922-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="e0922-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="e0922-113">用於轉譯的一或多個群組和技術的集合。</span><span class="sxs-lookup"><span data-stu-id="e0922-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="e0922-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="e0922-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="e0922-115">狀態指派的集合。</span><span class="sxs-lookup"><span data-stu-id="e0922-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="e0922-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="e0922-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="e0922-117">一或多個傳遞的集合。</span><span class="sxs-lookup"><span data-stu-id="e0922-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="e0922-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="e0922-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="e0922-119">一或多個技術的集合。</span><span class="sxs-lookup"><span data-stu-id="e0922-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="e0922-120">效果反映介面</span><span class="sxs-lookup"><span data-stu-id="e0922-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="e0922-121">反映會在效果系統中執行，以支援讀取 (和寫入) 效果狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="e0922-122">有多種方式可存取效果變數。</span><span class="sxs-lookup"><span data-stu-id="e0922-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="e0922-123">設定效果狀態的群組</span><span class="sxs-lookup"><span data-stu-id="e0922-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="e0922-124">使用這些介面來取得和設定一組狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="e0922-125">反映介面</span><span class="sxs-lookup"><span data-stu-id="e0922-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="e0922-126">Description</span><span class="sxs-lookup"><span data-stu-id="e0922-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="e0922-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="e0922-128">取得並設定 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="e0922-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="e0922-130">取得並設定深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="e0922-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="e0922-132">取得並設定轉譯器狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="e0922-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="e0922-134">取得並設定取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="e0922-135">設定效果資源</span><span class="sxs-lookup"><span data-stu-id="e0922-135">Setting Effect Resources</span></span>

<span data-ttu-id="e0922-136">使用這些介面來取得和設定資源。</span><span class="sxs-lookup"><span data-stu-id="e0922-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="e0922-137">反映介面</span><span class="sxs-lookup"><span data-stu-id="e0922-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="e0922-138">Description</span><span class="sxs-lookup"><span data-stu-id="e0922-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="e0922-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="e0922-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="e0922-140">存取材質緩衝區或常數緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0922-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="e0922-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="e0922-142">存取深度樣板資源中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0922-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="e0922-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="e0922-144">存取轉譯目標中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0922-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="e0922-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="e0922-146">存取著色器資源中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0922-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="e0922-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="e0922-148">存取未排序存取視圖中的資料。</span><span class="sxs-lookup"><span data-stu-id="e0922-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="e0922-149">設定其他效果變數</span><span class="sxs-lookup"><span data-stu-id="e0922-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="e0922-150">使用這些介面可依變數類型來取得和設定狀態。</span><span class="sxs-lookup"><span data-stu-id="e0922-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="e0922-151">反映介面</span><span class="sxs-lookup"><span data-stu-id="e0922-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="e0922-152">Description</span><span class="sxs-lookup"><span data-stu-id="e0922-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="e0922-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="e0922-154">取得類別實例。</span><span class="sxs-lookup"><span data-stu-id="e0922-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="e0922-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="e0922-156">取得和設定介面。</span><span class="sxs-lookup"><span data-stu-id="e0922-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="e0922-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="e0922-158">取得和設定矩陣。</span><span class="sxs-lookup"><span data-stu-id="e0922-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="e0922-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="e0922-160">取得和設定純量。</span><span class="sxs-lookup"><span data-stu-id="e0922-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="e0922-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="e0922-162">取得著色器變數。</span><span class="sxs-lookup"><span data-stu-id="e0922-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="e0922-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="e0922-164">取得並設定字串。</span><span class="sxs-lookup"><span data-stu-id="e0922-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="e0922-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="e0922-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="e0922-166">取得變數型別。</span><span class="sxs-lookup"><span data-stu-id="e0922-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="e0922-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="e0922-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="e0922-168">取得和設定向量。</span><span class="sxs-lookup"><span data-stu-id="e0922-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="e0922-169">所有反映介面都是衍生自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="e0922-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0922-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0922-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0922-171"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="e0922-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="e0922-172">Direct3D 11 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e0922-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





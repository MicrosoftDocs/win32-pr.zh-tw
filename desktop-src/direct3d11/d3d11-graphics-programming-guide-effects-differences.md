---
title: 效果的差異10和效果11
description: 本主題顯示效果10和效果11之間的差異。
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682590"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="6ce40-103">效果的差異10和效果11</span><span class="sxs-lookup"><span data-stu-id="6ce40-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="6ce40-104">本主題顯示效果10和效果11之間的差異。</span><span class="sxs-lookup"><span data-stu-id="6ce40-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="6ce40-105">裝置內容、執行緒和複製</span><span class="sxs-lookup"><span data-stu-id="6ce40-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="6ce40-106">ID3D10Device 介面已在 Direct3D 11： ID3D11Device 和 >id3d11devicecoNtext 中分割成兩個介面。</span><span class="sxs-lookup"><span data-stu-id="6ce40-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="6ce40-107">您可以建立多個 ID3D11DeviceCoNtexts，以協助在多個執行緒上同時執行。</span><span class="sxs-lookup"><span data-stu-id="6ce40-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="6ce40-108">效果11將此概念延伸至效果架構。</span><span class="sxs-lookup"><span data-stu-id="6ce40-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="6ce40-109">效果11的執行時間為單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="6ce40-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="6ce40-110">基於這個理由，您不應該同時使用具有多個執行緒的單一 ID3DX11Effect 實例。</span><span class="sxs-lookup"><span data-stu-id="6ce40-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="6ce40-111">若要在多個實例上使用效果11執行時間，您必須建立個別的 ID3DX11Effect 實例。</span><span class="sxs-lookup"><span data-stu-id="6ce40-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="6ce40-112">由於 >id3d11devicecoNtext 也是單一執行緒，因此您應該在套用時將不同的 >id3d11devicecoNtext 實例傳遞至每個效果實例。</span><span class="sxs-lookup"><span data-stu-id="6ce40-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="6ce40-113">您可以使用這些不同的裝置內容來建立命令清單，讓轉譯執行緒可以將它們套用至立即裝置內容。</span><span class="sxs-lookup"><span data-stu-id="6ce40-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="6ce40-114">若要建立多個封裝相同功能的效果，以在多個執行緒上使用，最簡單的方式就是建立一個效果，然後製作複製的複本。</span><span class="sxs-lookup"><span data-stu-id="6ce40-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="6ce40-115">相較于從頭開始建立多個複本，複製的優點如下：</span><span class="sxs-lookup"><span data-stu-id="6ce40-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="6ce40-116">複製常式比建立常式更快。</span><span class="sxs-lookup"><span data-stu-id="6ce40-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="6ce40-117">複製的效果會共用已建立的著色器、狀態欄塊和類別實例 (因此不需要重新建立) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="6ce40-118">複製的效果可以共用常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ce40-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="6ce40-119">複製的效果會從符合目前效果的狀態開始 (變數值，不論它是否已優化) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="6ce40-120">如需詳細資訊，請參閱 [複製效果](d3d11-graphics-programming-guide-effects-cloning.md) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="6ce40-121">效果集區和群組</span><span class="sxs-lookup"><span data-stu-id="6ce40-121">Effect Pools and Groups</span></span>

<span data-ttu-id="6ce40-122">到目前為止，Direct3D 10 中效果集區最普遍的使用是用於群組材質。</span><span class="sxs-lookup"><span data-stu-id="6ce40-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="6ce40-123">效果集區已從效果11移除，而新增了群組，這是更有效率的分組材質方法。</span><span class="sxs-lookup"><span data-stu-id="6ce40-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="6ce40-124">效果群組只是一組技術。</span><span class="sxs-lookup"><span data-stu-id="6ce40-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="6ce40-125">如需詳細資訊，請參閱 [效果群組語法 (Direct3D 11) ](d3d11-effect-group-syntax.md) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="6ce40-126">請考慮下列具有四個子效果和一個效果集區的效果階層：</span><span class="sxs-lookup"><span data-stu-id="6ce40-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="6ce40-127">您可以使用群組在效果11中達成相同的功能：</span><span class="sxs-lookup"><span data-stu-id="6ce40-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="6ce40-128">新的著色器階段</span><span class="sxs-lookup"><span data-stu-id="6ce40-128">New Shader Stages</span></span>

<span data-ttu-id="6ce40-129">Direct3D 11 中有三個新的著色器階段：輪廓著色器、網域著色器和計算著色器。</span><span class="sxs-lookup"><span data-stu-id="6ce40-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="6ce40-130">效果11以類似頂點著色器、幾何著色器和圖元著色器的方式來處理這些結果。</span><span class="sxs-lookup"><span data-stu-id="6ce40-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="6ce40-131">有三個新的變數類型已新增到效果11：</span><span class="sxs-lookup"><span data-stu-id="6ce40-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="6ce40-132">HullShader</span><span class="sxs-lookup"><span data-stu-id="6ce40-132">HullShader</span></span>
-   <span data-ttu-id="6ce40-133">DomainShader</span><span class="sxs-lookup"><span data-stu-id="6ce40-133">DomainShader</span></span>
-   <span data-ttu-id="6ce40-134">ComputeShader</span><span class="sxs-lookup"><span data-stu-id="6ce40-134">ComputeShader</span></span>

<span data-ttu-id="6ce40-135">如果您在技術中使用這些著色器，則必須將該技術標示為「technique11」，而不是「technique10」。</span><span class="sxs-lookup"><span data-stu-id="6ce40-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="6ce40-136">計算著色器不能與任何其他圖形狀態設定相同的傳遞 (其他著色器、狀態欄塊或轉譯目標) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="6ce40-137">新的材質類型</span><span class="sxs-lookup"><span data-stu-id="6ce40-137">New Texture Types</span></span>

<span data-ttu-id="6ce40-138">Direct3D 11 支援下列材質類型：</span><span class="sxs-lookup"><span data-stu-id="6ce40-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="6ce40-139">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="6ce40-140">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="6ce40-141">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="6ce40-142">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="6ce40-143">未排序的存取權視圖</span><span class="sxs-lookup"><span data-stu-id="6ce40-143">Unordered Access Views</span></span>

<span data-ttu-id="6ce40-144">效果11支援取得和設定新的未排序存取檢視類型。</span><span class="sxs-lookup"><span data-stu-id="6ce40-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="6ce40-145">其運作方式與紋理類似。</span><span class="sxs-lookup"><span data-stu-id="6ce40-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="6ce40-146">請考慮此效果 HLSL 範例：</span><span class="sxs-lookup"><span data-stu-id="6ce40-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="6ce40-147">您可以在 c + + 中設定此變數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6ce40-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="6ce40-148">Direct3D 11 支援下列未排序的存取檢視類型：</span><span class="sxs-lookup"><span data-stu-id="6ce40-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="6ce40-149">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-149">RWBuffer</span></span>
-   <span data-ttu-id="6ce40-150">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="6ce40-151">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="6ce40-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="6ce40-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="6ce40-152">RWTexture1D</span></span>
-   <span data-ttu-id="6ce40-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="6ce40-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="6ce40-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="6ce40-154">RWTexture2D</span></span>
-   <span data-ttu-id="6ce40-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="6ce40-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="6ce40-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="6ce40-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="6ce40-157">介面和類別實例</span><span class="sxs-lookup"><span data-stu-id="6ce40-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="6ce40-158">如需介面和類別語法，請參閱 [介面和類別](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class)。</span><span class="sxs-lookup"><span data-stu-id="6ce40-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="6ce40-159">如需使用介面和類別的效果，請參閱 [效果中的介面和類別](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="6ce40-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="6ce40-160">可定址的資料流程輸出</span><span class="sxs-lookup"><span data-stu-id="6ce40-160">Addressable Stream Out</span></span>

<span data-ttu-id="6ce40-161">在 Direct3D 10 中，幾何著色器可以將一個資料流程輸出到資料流程輸出單位和轉譯器單位。</span><span class="sxs-lookup"><span data-stu-id="6ce40-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="6ce40-162">在 Direct3D11 中，幾何著色器最多可以將四個數據流輸出到資料流程輸出單位，而且大部分的串流都是轉譯器單位。</span><span class="sxs-lookup"><span data-stu-id="6ce40-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="6ce40-163">已更新 **ConstructGSWithSO** 內建，以反映這種新功能。</span><span class="sxs-lookup"><span data-stu-id="6ce40-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="6ce40-164">如需詳細資訊，請參閱 [資料流程輸出語法](d3d11-graphics-reference-effect-streamout.md) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="6ce40-165">設定和取消裝置狀態</span><span class="sxs-lookup"><span data-stu-id="6ce40-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="6ce40-166">在效果10中，您可以使用 [**ID3D10EffectConstantBuffer：： SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) 和 [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) 函式，讓使用者管理常數緩衝區和材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ce40-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="6ce40-167">在您呼叫這些函式之後，10個執行時間的效果就不再管理常數緩衝區或紋理緩衝區，而使用者必須使用 ID3D10Device 介面填滿資料。</span><span class="sxs-lookup"><span data-stu-id="6ce40-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="6ce40-168">在效果11中，您也可以使用下列呼叫，讓狀態欄塊 (blend 狀態、轉譯器狀態、深度樣板狀態和取樣器狀態) 使用者管理：</span><span class="sxs-lookup"><span data-stu-id="6ce40-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="6ce40-169">**ID3DX11EffectBlendVariable::SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="6ce40-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="6ce40-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="6ce40-172">**ID3DX11EffectSamplerVariable::SetSampler**</span><span class="sxs-lookup"><span data-stu-id="6ce40-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="6ce40-173">在您呼叫這些函式之後，效果11的執行時間就不會再管理狀態欄塊變數，且值會維持不變。</span><span class="sxs-lookup"><span data-stu-id="6ce40-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="6ce40-174">請注意，因為狀態欄塊是不可變的，所以使用者必須設定新的狀態欄塊來變更值。</span><span class="sxs-lookup"><span data-stu-id="6ce40-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="6ce40-175">您也可以將常數緩衝區、材質緩衝區和狀態欄塊還原為非使用者管理的狀態。</span><span class="sxs-lookup"><span data-stu-id="6ce40-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="6ce40-176">如果您取消設定這些變數，則在必要時，11執行時間會繼續更新這些變數。</span><span class="sxs-lookup"><span data-stu-id="6ce40-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="6ce40-177">您可以使用下列呼叫來取消設定使用者管理的變數：</span><span class="sxs-lookup"><span data-stu-id="6ce40-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="6ce40-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="6ce40-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="6ce40-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="6ce40-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="6ce40-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="6ce40-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="6ce40-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="6ce40-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="6ce40-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="6ce40-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="6ce40-184">效果虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6ce40-184">Effects Virtual Machine</span></span>

<span data-ttu-id="6ce40-185">已移除在函式之外評估複雜運算式的效果虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6ce40-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="6ce40-186">下列複雜運算式範例不受支援：</span><span class="sxs-lookup"><span data-stu-id="6ce40-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="6ce40-187">SetPixelShader ( myPSArray ( i \* 3 + j ) ) ;</span><span class="sxs-lookup"><span data-stu-id="6ce40-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="6ce40-188">SetPixelShader ( myPSArray ( (float) i ) ;</span><span class="sxs-lookup"><span data-stu-id="6ce40-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="6ce40-189">篩選 = i + 2;</span><span class="sxs-lookup"><span data-stu-id="6ce40-189">FILTER = i + 2;</span></span>

<span data-ttu-id="6ce40-190">以下是支援的非複雜運算式範例：</span><span class="sxs-lookup"><span data-stu-id="6ce40-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="6ce40-191">SetPixelShader ( myPS ) ;</span><span class="sxs-lookup"><span data-stu-id="6ce40-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="6ce40-192">SetPixelShader ( myPS \[ \] ) ;</span><span class="sxs-lookup"><span data-stu-id="6ce40-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="6ce40-193">SetPixelShader ( myPS \[ uIndex \] ) ;//uIndex 是 uint 變數</span><span class="sxs-lookup"><span data-stu-id="6ce40-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="6ce40-194">篩選 = i;</span><span class="sxs-lookup"><span data-stu-id="6ce40-194">FILTER = i;</span></span>
5.  <span data-ttu-id="6ce40-195">FILTER = 各向異性;</span><span class="sxs-lookup"><span data-stu-id="6ce40-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="6ce40-196">這些運算式可能會出現在狀態欄塊運算式 (例如篩選) 和傳遞運算式 (例如 SetPixelShader) 。</span><span class="sxs-lookup"><span data-stu-id="6ce40-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="6ce40-197">來源可用性和位置</span><span class="sxs-lookup"><span data-stu-id="6ce40-197">Source Availability and Location</span></span>

<span data-ttu-id="6ce40-198">在 D3D10.dll 中散佈了10個效果。</span><span class="sxs-lookup"><span data-stu-id="6ce40-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="6ce40-199">效果11會以來源的形式散發，並以對應的 Visual Studio 解決方案來進行編譯。</span><span class="sxs-lookup"><span data-stu-id="6ce40-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="6ce40-200">當您建立效果類型的應用程式時，建議您直接在這些應用程式中包含效果11來源。</span><span class="sxs-lookup"><span data-stu-id="6ce40-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="6ce40-201">您可以從 [Direct3D 11 Update 的效果](https://github.com/Microsoft/FX11)得到11個效果。</span><span class="sxs-lookup"><span data-stu-id="6ce40-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce40-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ce40-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce40-203"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="6ce40-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
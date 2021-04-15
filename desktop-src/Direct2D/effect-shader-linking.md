---
title: 效果著色器連結
description: Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321676"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="ac70c-103">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="ac70c-103">Effect Shader Linking</span></span>

<span data-ttu-id="ac70c-104">Direct2D 會使用稱為效果著色器的優化連結，此連結會將多個效果圖形轉譯傳遞合併成單一階段。</span><span class="sxs-lookup"><span data-stu-id="ac70c-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="ac70c-105">效果著色器連結總覽</span><span class="sxs-lookup"><span data-stu-id="ac70c-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="ac70c-106">使用效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="ac70c-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="ac70c-107">撰寫著色器連結相容的自訂效果</span><span class="sxs-lookup"><span data-stu-id="ac70c-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="ac70c-108">連結相容效果著色器範例</span><span class="sxs-lookup"><span data-stu-id="ac70c-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="ac70c-109">編譯連結相容-著色器</span><span class="sxs-lookup"><span data-stu-id="ac70c-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="ac70c-110">步驟1：編譯匯出函數</span><span class="sxs-lookup"><span data-stu-id="ac70c-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="ac70c-111">步驟2：編譯完整的著色器並內嵌匯出函式</span><span class="sxs-lookup"><span data-stu-id="ac70c-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="ac70c-112">匯出函式規格</span><span class="sxs-lookup"><span data-stu-id="ac70c-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="ac70c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac70c-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="ac70c-114">效果著色器連結總覽</span><span class="sxs-lookup"><span data-stu-id="ac70c-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="ac70c-115">效果著色器連結優化是以 HLSL 著色器連結為基礎，這是一項 Direct3D 11.2 功能，可讓您藉由連結預先編譯的著色器函式，在執行時間產生圖元和頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ac70c-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="ac70c-116">下圖說明效果圖形中效果著色器連結的概念。</span><span class="sxs-lookup"><span data-stu-id="ac70c-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="ac70c-117">第一個圖顯示具有四個轉譯轉換的典型 Direct2D 效果圖形。</span><span class="sxs-lookup"><span data-stu-id="ac70c-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="ac70c-118">如果沒有著色器連結，每個轉換都會取用轉譯行程，且需要中繼介面;此圖表總共需要4個階段和3個中繼。</span><span class="sxs-lookup"><span data-stu-id="ac70c-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![沒有著色器連結的轉換圖形：4階段和3中繼。](images/shader-transform-graph.png) |



 

<span data-ttu-id="ac70c-120">第二張圖顯示相同的效果圖形，其中每個轉譯轉換都已取代為可連結函式版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="ac70c-121">Direct2D 可以連結整個圖形，並在不需要任何中繼的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="ac70c-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="ac70c-122">這可大幅降低 GPU 執行時間，並減少最大的 GPU 記憶體耗用量。</span><span class="sxs-lookup"><span data-stu-id="ac70c-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![具有著色器連結的轉換圖形：1次傳遞、0中繼。](images/shader-linking-graph.png) |



 

<span data-ttu-id="ac70c-124">效果著色器連結會在效果內的個別轉換上運作;這表示即使是具有單一效果的圖表，如果該效果有多個有效的轉換，也可能會受益于著色器連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="ac70c-125">使用效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="ac70c-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="ac70c-126">如果您要建立使用效果的 Direct2D 應用程式，則不需要執行任何動作，即可利用效果著色器連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="ac70c-127">Direct2D 會自動分析效果圖形，以決定連結每個轉換的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="ac70c-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="ac70c-128">效果作者負責以支援效果著色器連結的方式來實行其效果;如需詳細資訊，請參閱下面的 [編寫著色器連結相容的自訂效果](#authoring-a-shader-linking-compatible-custom-effect) 一節。</span><span class="sxs-lookup"><span data-stu-id="ac70c-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="ac70c-129">所有內建效果都支援著色器連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="ac70c-130">Direct2D 只會在有用的情況下連結連續的轉譯轉換。</span><span class="sxs-lookup"><span data-stu-id="ac70c-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="ac70c-131">決定是否要連結兩個轉換時，會考慮多個因素。</span><span class="sxs-lookup"><span data-stu-id="ac70c-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="ac70c-132">例如，如果其中一個轉換使用頂點或計算著色器，則不會執行著色器連結，因為只有圖元著色器可以連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="ac70c-133">此外，如果未撰寫效果以與著色器連結相容，則周圍的轉換將不會與它連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="ac70c-134">如果有這類連結危險，Direct2D 就不會將任何轉換連結到危險的旁邊，但仍會嘗試連結圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="ac70c-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![具有連結危險的轉換圖形：2個通過，1個中繼。](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="ac70c-136">撰寫著色器連結相容的自訂效果</span><span class="sxs-lookup"><span data-stu-id="ac70c-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="ac70c-137">如果您要撰寫自己的自訂 Direct2D 效果，您必須確定其轉換支援效果著色器連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="ac70c-138">這需要一些從先前的自訂效果執行的微小變更。</span><span class="sxs-lookup"><span data-stu-id="ac70c-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="ac70c-139">如果您自訂效果內的轉換不支援著色器連結，則 Direct2D 不會將它與效果圖形中任何與其連續的轉換連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="ac70c-140">如果您是自訂效果的作者，您應該留意幾項重要概念和需求：</span><span class="sxs-lookup"><span data-stu-id="ac70c-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="ac70c-141">**沒有變更效果介面的執行**</span><span class="sxs-lookup"><span data-stu-id="ac70c-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="ac70c-142">您不需要修改任何執行各種效果介面的程式碼，例如 [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)。</span><span class="sxs-lookup"><span data-stu-id="ac70c-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="ac70c-143">**提供完整和匯出函式版本的著色器**</span><span class="sxs-lookup"><span data-stu-id="ac70c-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="ac70c-144">您必須提供由 Direct2D 可連結之效果著色器的匯出函式版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="ac70c-145">此外，您也必須繼續提供原始的完整著色器;這是因為 Direct2D 會在執行時間根據著色器連結是否要套用至圖形中的特定連結來選取適當的著色器版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="ac70c-146">如果轉換只透過 [ID2D1EffectCoNtext：： LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)) 提供完整的圖元著色器 blob (，則不會連結到連續的轉換。</span><span class="sxs-lookup"><span data-stu-id="ac70c-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="ac70c-147">**Helper 函式**</span><span class="sxs-lookup"><span data-stu-id="ac70c-147">**Helper functions**</span></span>

    <span data-ttu-id="ac70c-148">Direct2D 會提供 [HLSL helper](hlsl-helpers.md) 函式和宏，以自動產生著色器的完整和匯出函式版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="ac70c-149">這些協助程式可在 d2d1effecthelpers. hlsli 中找到。</span><span class="sxs-lookup"><span data-stu-id="ac70c-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="ac70c-150">此外，HLSL 編譯器 (FXC.EXE) 可讓您在完整著色器中，將匯出函數著色器插入私用欄位。</span><span class="sxs-lookup"><span data-stu-id="ac70c-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="ac70c-151">如此一來，您只需要撰寫一次著色器，並同時將這兩個版本傳遞至 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="ac70c-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="ac70c-152">D2d1effecthelpers. hlsli 和 FXC.EXE 編譯器都會包含 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ac70c-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="ac70c-153">Helper 函式：</span><span class="sxs-lookup"><span data-stu-id="ac70c-153">The helper functions:</span></span>

  - [<span data-ttu-id="ac70c-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="ac70c-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="ac70c-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="ac70c-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="ac70c-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="ac70c-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="ac70c-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="ac70c-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="ac70c-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="ac70c-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="ac70c-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="ac70c-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="ac70c-160">D2D \_ PS \_ 專案</span><span class="sxs-lookup"><span data-stu-id="ac70c-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="ac70c-161">您也可以手動撰寫每個著色器的兩個版本，並將它們編譯兩次，只要符合以下所述的匯出函式 [規格](#export-function-specifications) 中所述的規格。</span><span class="sxs-lookup"><span data-stu-id="ac70c-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="ac70c-162">**僅圖元著色器**</span><span class="sxs-lookup"><span data-stu-id="ac70c-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="ac70c-163">Direct2D 不支援連結計算或頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="ac70c-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="ac70c-164">但是，如果您的效果同時使用了頂點和圖元著色器，則圖元著色器的輸出仍可連結。</span><span class="sxs-lookup"><span data-stu-id="ac70c-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="ac70c-165">**簡單與複雜的取樣**</span><span class="sxs-lookup"><span data-stu-id="ac70c-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="ac70c-166">著色器函式連結的運作方式是將一個圖元著色器的輸出連接到後續圖元著色器傳遞的輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="ac70c-167">只有當取用的圖元著色器只需要單一輸入值來執行計算時，才可能發生這種情況;此值通常是從頂點著色器所發出的材質座標取樣輸入材質。</span><span class="sxs-lookup"><span data-stu-id="ac70c-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="ac70c-168">這類圖元著色器是用來執行簡單的取樣。</span><span class="sxs-lookup"><span data-stu-id="ac70c-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![灰階轉換是簡單取樣的範例。](images/simple-sampling.png) |

    

     

    <span data-ttu-id="ac70c-171">某些圖元著色器（例如高斯模糊）會從多個輸入範例計算其輸出，而不只是單一樣本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="ac70c-172">這類圖元著色器稱為執行複雜的取樣。</span><span class="sxs-lookup"><span data-stu-id="ac70c-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![高斯模糊是複雜取樣的範例。](images/complex-sampling.png) |

    

     

    <span data-ttu-id="ac70c-175">只有具有簡單輸入的著色器函式可以有其他著色器函式提供的輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="ac70c-176">具有複雜輸入的著色器函數必須提供輸入材質給範例。</span><span class="sxs-lookup"><span data-stu-id="ac70c-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="ac70c-177">這表示 Direct2D 不會將具有複雜輸入的著色器連結到其前身。</span><span class="sxs-lookup"><span data-stu-id="ac70c-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="ac70c-178">使用「 [DIRECT2D HLSL](hlsl-helpers.md)協助程式」時，您必須在 HLSL 中指出著色器是否使用複雜或簡單的輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="ac70c-179">連結相容效果著色器範例</span><span class="sxs-lookup"><span data-stu-id="ac70c-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="ac70c-180">使用 D2D 協助程式時，下列程式碼片段代表簡單連結相容效果著色器：</span><span class="sxs-lookup"><span data-stu-id="ac70c-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="ac70c-181">在這個簡短的範例中，請注意，不會宣告任何函式參數，每個輸入的輸入和類型數目是在輸入函式之前宣告，而是藉由呼叫 [D2DGetInput](d2dgetinput.md)來取出輸入，而且必須先定義預處理器指示詞，才能包含 helper 檔案。</span><span class="sxs-lookup"><span data-stu-id="ac70c-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="ac70c-182">連結相容的著色器必須同時提供一般的單一傳遞圖元著色器和匯出著色器函數。</span><span class="sxs-lookup"><span data-stu-id="ac70c-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="ac70c-183">當您搭配著色器編譯腳本使用時， [D2D \_ PS \_ 專案](d2d-ps-entry.md) 宏可讓您從相同的程式碼產生這些專案。</span><span class="sxs-lookup"><span data-stu-id="ac70c-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="ac70c-184">編譯完整的著色器時，宏會展開至下列程式碼，其中包含與 D2D 效果相容的輸入簽章。</span><span class="sxs-lookup"><span data-stu-id="ac70c-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="ac70c-185">當編譯相同程式碼的匯出函數版本時，會產生下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ac70c-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="ac70c-186">請注意，通常透過取樣 Texture2D 來取出的材質輸入已取代為函式輸入 (input0) 。</span><span class="sxs-lookup"><span data-stu-id="ac70c-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="ac70c-187">若要查看完整的逐步說明，瞭解您需要如何撰寫連結相容效果，請參閱 [自訂效果教學](custom-effects.md) 課程和 [Direct2D 自訂影像效果範例](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)。</span><span class="sxs-lookup"><span data-stu-id="ac70c-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="ac70c-188">編譯連結相容-著色器</span><span class="sxs-lookup"><span data-stu-id="ac70c-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="ac70c-189">若要可連結，傳遞給 D2D 的圖元著色器 blob 必須同時包含著色器的完整和匯出函式版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="ac70c-190">將已編譯的匯出函式內嵌至 D3D \_ BLOB 私用 \_ 資料區域，即可完成此作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ac70c-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="ac70c-191">使用 D2D 協助程式函式撰寫著色器時，必須在編譯時定義 D2D 編譯目標。</span><span class="sxs-lookup"><span data-stu-id="ac70c-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="ac70c-192">編譯目標型別是 D2D \_ 完整 \_ 著色器和 d2d \_ 函數。</span><span class="sxs-lookup"><span data-stu-id="ac70c-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="ac70c-193">編譯連結相容效果著色器的程式有兩個步驟：</span><span class="sxs-lookup"><span data-stu-id="ac70c-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="ac70c-194">編譯匯出函數</span><span class="sxs-lookup"><span data-stu-id="ac70c-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="ac70c-195">編譯完整的著色器並內嵌匯出函式</span><span class="sxs-lookup"><span data-stu-id="ac70c-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="ac70c-196">使用 Visual Studio 編譯效果時，您應該建立一個批次檔來執行這兩個 FXC.EXE 命令，並執行這個批次檔做為編譯步驟之前執行的自訂群組建步驟。</span><span class="sxs-lookup"><span data-stu-id="ac70c-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="ac70c-197">步驟1：編譯匯出函數</span><span class="sxs-lookup"><span data-stu-id="ac70c-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="ac70c-198">若要編譯著色器的匯出函式版本，您必須將下列旗標傳遞給 FXC.EXE。</span><span class="sxs-lookup"><span data-stu-id="ac70c-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac70c-199">**旗標**</span><span class="sxs-lookup"><span data-stu-id="ac70c-199">**Flag**</span></span>                       | <span data-ttu-id="ac70c-200">**說明**</span><span class="sxs-lookup"><span data-stu-id="ac70c-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="ac70c-201">一起 <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="ac70c-201">/T <ShaderModel></span></span>         | <span data-ttu-id="ac70c-202">設定 <ShaderModel> 為適當的圖元著色器設定檔，如 [fxc.exe 語法](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)中所定義。</span><span class="sxs-lookup"><span data-stu-id="ac70c-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="ac70c-203">這必須是 [HLSL 著色器連結] 下所列的其中一個設定檔。</span><span class="sxs-lookup"><span data-stu-id="ac70c-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="ac70c-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="ac70c-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="ac70c-205">設定 <MyShaderFile> 為 HLSL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac70c-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="ac70c-206">/D D2D \_ 函數</span><span class="sxs-lookup"><span data-stu-id="ac70c-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="ac70c-207">此定義會指示 FXC.EXE 編譯著色器的匯出函式版本。</span><span class="sxs-lookup"><span data-stu-id="ac70c-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="ac70c-208">/D D2D \_ 專案 =<entry></span><span class="sxs-lookup"><span data-stu-id="ac70c-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="ac70c-209">設定 <entry> 為您在 [D2D \_ PS \_ 專案](d2d-ps-entry.md) 宏中定義的 HLSL 進入點名稱。</span><span class="sxs-lookup"><span data-stu-id="ac70c-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="ac70c-210">/Fl <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="ac70c-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="ac70c-211">設定 <MyShaderfile> 為您要儲存著色器匯出函式版本的位置。</span><span class="sxs-lookup"><span data-stu-id="ac70c-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="ac70c-212">請注意，fxlib 副檔名只是為了方便識別。</span><span class="sxs-lookup"><span data-stu-id="ac70c-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="ac70c-213">步驟2：編譯完整的著色器並內嵌匯出函式</span><span class="sxs-lookup"><span data-stu-id="ac70c-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="ac70c-214">若要使用內嵌的匯出版本編譯著色器的完整版本，您必須將下列旗標傳遞給 FXC.EXE。</span><span class="sxs-lookup"><span data-stu-id="ac70c-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac70c-215">**旗標**</span><span class="sxs-lookup"><span data-stu-id="ac70c-215">**Flag**</span></span>                               | <span data-ttu-id="ac70c-216">**說明**</span><span class="sxs-lookup"><span data-stu-id="ac70c-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ac70c-217">一起 <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="ac70c-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="ac70c-218">設定 <ShaderModel> 為適當的圖元著色器設定檔，如 [fxc.exe 語法](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)中所定義。</span><span class="sxs-lookup"><span data-stu-id="ac70c-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="ac70c-219">這必須是對應至步驟1中所指定連結設定檔的圖元著色器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ac70c-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="ac70c-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="ac70c-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="ac70c-221">設定 <MyShaderFile> 為 HLSL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac70c-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="ac70c-222">/D D2D \_ 完整 \_ 著色器</span><span class="sxs-lookup"><span data-stu-id="ac70c-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="ac70c-223">此定義會指示 FXC.EXE 編譯完整版的著色器。</span><span class="sxs-lookup"><span data-stu-id="ac70c-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="ac70c-224">/D D2D \_ 專案 =<entry></span><span class="sxs-lookup"><span data-stu-id="ac70c-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="ac70c-225">設定 <entry> 為您在 D2D \_ PS 專案 () 宏中定義的 HLSL 進入點名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ac70c-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="ac70c-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="ac70c-226">/E <entry></span></span>                       | <span data-ttu-id="ac70c-227">設定 <entry> 為您在 D2D \_ PS 專案 () 宏中定義的 HLSL 進入點名稱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ac70c-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="ac70c-228">/setprivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="ac70c-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="ac70c-229">此引數會指示 FXC.EXE 將步驟1中產生的匯出函式著色器內嵌至 D3D \_ BLOB \_ 私用 \_ 資料區域。</span><span class="sxs-lookup"><span data-stu-id="ac70c-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="ac70c-230">/Fo <MyShader></span><span class="sxs-lookup"><span data-stu-id="ac70c-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="ac70c-231">設定 <MyShader> 為，您要在其中儲存最後一個合併的編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="ac70c-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="ac70c-232">/Fh <MyShader> 。h</span><span class="sxs-lookup"><span data-stu-id="ac70c-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="ac70c-233">設定 <MyShader> 為您要在其中儲存最後一個合併的標頭。</span><span class="sxs-lookup"><span data-stu-id="ac70c-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="ac70c-234">匯出函式規格</span><span class="sxs-lookup"><span data-stu-id="ac70c-234">Export function specifications</span></span>

<span data-ttu-id="ac70c-235">雖然不建議使用，但不建議使用 D2D 提供的協助程式撰寫相容效果著色器。</span><span class="sxs-lookup"><span data-stu-id="ac70c-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="ac70c-236">請務必小心，以確保完整的著色器和匯出函式輸入簽章都符合 D2D 規格。</span><span class="sxs-lookup"><span data-stu-id="ac70c-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="ac70c-237">完整著色器的規格與先前的 Windows 版本相同。</span><span class="sxs-lookup"><span data-stu-id="ac70c-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="ac70c-238">簡單地說，圖元著色器輸入參數必須是 SV \_ 位置、場景 \_ 位置和一個 TEXCOORD 的每個效果輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="ac70c-239">針對 export 函式，函式必須傳回 float4，而且其輸入必須是下列其中一種類型：</span><span class="sxs-lookup"><span data-stu-id="ac70c-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="ac70c-240">簡單輸入</span><span class="sxs-lookup"><span data-stu-id="ac70c-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="ac70c-241">針對簡單的輸入，D2D 會在輸入材質和著色器函式之間插入範例函式，否則會由另一個著色器函式的輸出提供輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="ac70c-242">複雜輸入</span><span class="sxs-lookup"><span data-stu-id="ac70c-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="ac70c-243">針對複雜的輸入，D2D 只會傳遞材質座標，如 Windows 8 檔中所述。</span><span class="sxs-lookup"><span data-stu-id="ac70c-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="ac70c-244">輸出位置</span><span class="sxs-lookup"><span data-stu-id="ac70c-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="ac70c-245">只能定義一個場景 \_ 位置輸入。</span><span class="sxs-lookup"><span data-stu-id="ac70c-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="ac70c-246">只有在必要時才會包含這個參數，因為每個連結的著色器只有一個函式可以使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ac70c-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="ac70c-247">必須如上面所述定義此語義，因為 D2D 將檢查此語義，以決定如何將函數連結在一起。</span><span class="sxs-lookup"><span data-stu-id="ac70c-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="ac70c-248">如果任何函式輸入不符合上述其中一個類型，則會拒絕著色器連結的函式。</span><span class="sxs-lookup"><span data-stu-id="ac70c-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac70c-249">相關主題</span><span class="sxs-lookup"><span data-stu-id="ac70c-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac70c-250">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="ac70c-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="ac70c-251">ID3D11Linker 介面</span><span class="sxs-lookup"><span data-stu-id="ac70c-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="ac70c-252">ID3D11FunctionLinkingGraph 介面</span><span class="sxs-lookup"><span data-stu-id="ac70c-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
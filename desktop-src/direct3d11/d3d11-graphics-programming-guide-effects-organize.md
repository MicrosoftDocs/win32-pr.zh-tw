---
title: '將效果中的狀態組織 (Direct3D 11) '
description: 使用 Direct3D 11 時，會依結構來組織特定管線階段的效果狀態。
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990959"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="c42ab-103">將效果中的狀態組織 (Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="c42ab-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="c42ab-104">使用 Direct3D 11 時，會依結構來組織特定管線階段的效果狀態。</span><span class="sxs-lookup"><span data-stu-id="c42ab-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="c42ab-105">結構如下：</span><span class="sxs-lookup"><span data-stu-id="c42ab-105">Here are the structures:</span></span>



| <span data-ttu-id="c42ab-106">管線狀態</span><span class="sxs-lookup"><span data-stu-id="c42ab-106">Pipeline State</span></span> | <span data-ttu-id="c42ab-107">結構</span><span class="sxs-lookup"><span data-stu-id="c42ab-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c42ab-108">光柵</span><span class="sxs-lookup"><span data-stu-id="c42ab-108">Rasterization</span></span>  | [<span data-ttu-id="c42ab-109">**D3D11 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="c42ab-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="c42ab-110">輸出合併</span><span class="sxs-lookup"><span data-stu-id="c42ab-110">Output Merger</span></span>  | <span data-ttu-id="c42ab-111">[**D3D11 \_BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)和 [ **D3D11 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="c42ab-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="c42ab-112">著色器</span><span class="sxs-lookup"><span data-stu-id="c42ab-112">Shaders</span></span>        | <span data-ttu-id="c42ab-113">請參閱下方</span><span class="sxs-lookup"><span data-stu-id="c42ab-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="c42ab-114">針對著色器階段，其中的狀態變更數目需要更多應用程式控制，狀態已分割成常數緩衝區狀態、取樣器狀態、著色器資源狀態，以及圖元和計算著色器) 的未排序存取檢視狀態 (。</span><span class="sxs-lookup"><span data-stu-id="c42ab-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="c42ab-115">這可讓精心設計的應用程式只更新變更狀態，藉由減少必須傳遞至 GPU 的資料量來改善效能。</span><span class="sxs-lookup"><span data-stu-id="c42ab-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="c42ab-116">那麼，您要如何在效果中組織管線狀態呢？</span><span class="sxs-lookup"><span data-stu-id="c42ab-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="c42ab-117">答案是，順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="c42ab-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="c42ab-118">全域變數不需要位於頂端。</span><span class="sxs-lookup"><span data-stu-id="c42ab-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="c42ab-119">不過，SDK 中的所有範例都遵循相同的順序，因為最好的做法是以相同的方式來組織資料。</span><span class="sxs-lookup"><span data-stu-id="c42ab-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="c42ab-120">這是 DirectX SDK 範例中資料排序的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c42ab-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="c42ab-121">全域變數</span><span class="sxs-lookup"><span data-stu-id="c42ab-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="c42ab-122">著色器</span><span class="sxs-lookup"><span data-stu-id="c42ab-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="c42ab-123">群組、技術和通過</span><span class="sxs-lookup"><span data-stu-id="c42ab-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="c42ab-124">全域變數</span><span class="sxs-lookup"><span data-stu-id="c42ab-124">Global Variables</span></span>

<span data-ttu-id="c42ab-125">就像標準 C 實務一樣，全域變數是在檔案頂端先宣告。</span><span class="sxs-lookup"><span data-stu-id="c42ab-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="c42ab-126">最常見的情況是，這些變數會由應用程式初始化，然後用於效果中。</span><span class="sxs-lookup"><span data-stu-id="c42ab-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="c42ab-127">有時候它們會初始化且永遠不會變更，而在其他情況下，則會更新每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="c42ab-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="c42ab-128">如同 C 函式範圍規則，在效果函式範圍外宣告的效果變數在整個效果中都是可見的;只有在該函式內才能看到任何在效果函式內宣告的變數。</span><span class="sxs-lookup"><span data-stu-id="c42ab-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="c42ab-129">以下是在 BasicHLSL10 中宣告的變數範例。</span><span class="sxs-lookup"><span data-stu-id="c42ab-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="c42ab-130">效果變數的語法在 [ (Direct3D 11) 的效果變數語法 ](d3d11-effect-variable-syntax.md)中是更完整的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="c42ab-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="c42ab-131">效果紋理取樣器的語法在 [取樣器類型 (DIRECTX HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)中更詳盡。</span><span class="sxs-lookup"><span data-stu-id="c42ab-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="c42ab-132">著色器</span><span class="sxs-lookup"><span data-stu-id="c42ab-132">Shaders</span></span>

<span data-ttu-id="c42ab-133">著色器是小型的可執行程式。</span><span class="sxs-lookup"><span data-stu-id="c42ab-133">Shaders are small executable programs.</span></span> <span data-ttu-id="c42ab-134">您可以將著色器視為封裝著色器狀態，因為 HLSL 程式碼會執行著色器功能。</span><span class="sxs-lookup"><span data-stu-id="c42ab-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="c42ab-135">圖形管線最多五種不同的著色器。</span><span class="sxs-lookup"><span data-stu-id="c42ab-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="c42ab-136">頂點著色器-在頂點資料上操作。</span><span class="sxs-lookup"><span data-stu-id="c42ab-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="c42ab-137">中的一個頂點會產生一個頂點。</span><span class="sxs-lookup"><span data-stu-id="c42ab-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="c42ab-138">輪廓著色器-操作修補程式資料。</span><span class="sxs-lookup"><span data-stu-id="c42ab-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="c42ab-139">控制點階段：一個調用會產生一個控制點;針對每個分叉和聯結階段：一個修補程式會產生一些修補常數資料。</span><span class="sxs-lookup"><span data-stu-id="c42ab-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="c42ab-140">網域著色器-操作基本資料。</span><span class="sxs-lookup"><span data-stu-id="c42ab-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="c42ab-141">其中一個基本專案可能會產生0、1或許多基本專案。</span><span class="sxs-lookup"><span data-stu-id="c42ab-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="c42ab-142">幾何著色器-操作基本資料。</span><span class="sxs-lookup"><span data-stu-id="c42ab-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="c42ab-143">中的一個基本專案可能會產生0、1或許多基本專案。</span><span class="sxs-lookup"><span data-stu-id="c42ab-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="c42ab-144">圖元著色器-在圖元資料上操作。</span><span class="sxs-lookup"><span data-stu-id="c42ab-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="c42ab-145">中的一個圖元會產生1圖元輸出 (除非圖元從轉譯) 挑選出來。</span><span class="sxs-lookup"><span data-stu-id="c42ab-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="c42ab-146">計算著色器管線會使用一個著色器：</span><span class="sxs-lookup"><span data-stu-id="c42ab-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="c42ab-147">計算著色器-在任何種類的資料上運作。</span><span class="sxs-lookup"><span data-stu-id="c42ab-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="c42ab-148">輸出與執行緒數目無關。</span><span class="sxs-lookup"><span data-stu-id="c42ab-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="c42ab-149">著色器是區域函式，並遵循 C 樣式函數規則。</span><span class="sxs-lookup"><span data-stu-id="c42ab-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="c42ab-150">當編譯效果時，會編譯每個著色器，並在內部儲存每個著色器函式的指標。</span><span class="sxs-lookup"><span data-stu-id="c42ab-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="c42ab-151">編譯成功時，會傳回 ID3D11Effect 介面。</span><span class="sxs-lookup"><span data-stu-id="c42ab-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="c42ab-152">此時，編譯的效果會採用中繼格式。</span><span class="sxs-lookup"><span data-stu-id="c42ab-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="c42ab-153">若要瞭解已編譯著色器的詳細資訊，您將需要使用著色器反映。</span><span class="sxs-lookup"><span data-stu-id="c42ab-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="c42ab-154">這基本上就像是要求執行時間對著色器進行反編譯，然後將資訊傳回給您，以瞭解著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="c42ab-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="c42ab-155">效果著色器的語法在 [ (Direct3D 11) 的效果函數語法 ](d3d11-effect-function-syntax.md)中更加詳盡。</span><span class="sxs-lookup"><span data-stu-id="c42ab-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="c42ab-156">群組、技術和通過</span><span class="sxs-lookup"><span data-stu-id="c42ab-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="c42ab-157">群組是技術的集合。</span><span class="sxs-lookup"><span data-stu-id="c42ab-157">A group is a collection of techniques.</span></span> <span data-ttu-id="c42ab-158">技術是轉譯行程的集合， (至少必須有一個 pass) 。</span><span class="sxs-lookup"><span data-stu-id="c42ab-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="c42ab-159">每個效果傳遞 (在轉譯迴圈中的單一傳遞範圍中類似) 定義著色器狀態和轉譯幾何所需的任何其他管線狀態。</span><span class="sxs-lookup"><span data-stu-id="c42ab-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="c42ab-160">群組是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="c42ab-160">Groups are optional.</span></span> <span data-ttu-id="c42ab-161">有一個未命名的群組，其中包含所有的全域技術。</span><span class="sxs-lookup"><span data-stu-id="c42ab-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="c42ab-162">所有其他群組都必須命名為。</span><span class="sxs-lookup"><span data-stu-id="c42ab-162">All other groups must be named.</span></span>

<span data-ttu-id="c42ab-163">以下是其中一個技巧 (的範例，其中包含 BasicHLSL10 的一個 pass) 。</span><span class="sxs-lookup"><span data-stu-id="c42ab-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="c42ab-164">效果著色器的語法更完整地說明 [ (Direct3D 11) 的有效技巧語法 ](d3d11-effect-technique-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="c42ab-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c42ab-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="c42ab-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c42ab-166"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="c42ab-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
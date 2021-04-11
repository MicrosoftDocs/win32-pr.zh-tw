---
description: 使用 Direct3D 10 時，特定管線階段的效果狀態會依照下列結構來組織：
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: '將效果中的狀態組織 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110381"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="82c30-103">將效果中的狀態組織 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="82c30-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="82c30-104">使用 Direct3D 10 時，特定管線階段的效果狀態會依照下列結構來組織：</span><span class="sxs-lookup"><span data-stu-id="82c30-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="82c30-105">管線狀態</span><span class="sxs-lookup"><span data-stu-id="82c30-105">Pipeline State</span></span>  | <span data-ttu-id="82c30-106">結構</span><span class="sxs-lookup"><span data-stu-id="82c30-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c30-107">輸入組合器</span><span class="sxs-lookup"><span data-stu-id="82c30-107">Input Assembler</span></span> | [<span data-ttu-id="82c30-108">**D3D10 \_ 輸入 \_ 元素 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="82c30-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="82c30-109">光柵</span><span class="sxs-lookup"><span data-stu-id="82c30-109">Rasterization</span></span>   | [<span data-ttu-id="82c30-110">**D3D10 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="82c30-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="82c30-111">輸出合併</span><span class="sxs-lookup"><span data-stu-id="82c30-111">Output Merger</span></span>   | <span data-ttu-id="82c30-112">[**D3D10 \_BLEND \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)和 [ **D3D10 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="82c30-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="82c30-113">針對著色器階段，其中的狀態變更數目需要更多應用程式控制，狀態已分割成常數緩衝區狀態、取樣器狀態和著色器資源狀態。</span><span class="sxs-lookup"><span data-stu-id="82c30-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="82c30-114">這可讓精心設計的應用程式只更新變更狀態，藉由減少必須傳遞至 GPU 的資料量來改善效能。</span><span class="sxs-lookup"><span data-stu-id="82c30-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="82c30-115">那麼，您要如何在效果中組織管線狀態呢？</span><span class="sxs-lookup"><span data-stu-id="82c30-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="82c30-116">答案是，順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="82c30-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="82c30-117">全域變數不需要位於頂端。</span><span class="sxs-lookup"><span data-stu-id="82c30-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="82c30-118">不過，SDK 中的所有範例都遵循相同的順序，因為最好的做法是以相同的方式來組織資料。</span><span class="sxs-lookup"><span data-stu-id="82c30-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="82c30-119">這是 DirectX SDK 範例中資料排序的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="82c30-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="82c30-120">全域變數</span><span class="sxs-lookup"><span data-stu-id="82c30-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="82c30-121">著色器</span><span class="sxs-lookup"><span data-stu-id="82c30-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="82c30-122">技術與通過</span><span class="sxs-lookup"><span data-stu-id="82c30-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="82c30-123">全域變數</span><span class="sxs-lookup"><span data-stu-id="82c30-123">Global Variables</span></span>

<span data-ttu-id="82c30-124">就像標準 C 實務一樣，全域變數是在檔案頂端先宣告。</span><span class="sxs-lookup"><span data-stu-id="82c30-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="82c30-125">最常見的情況是，這些變數會由應用程式初始化，然後用於效果中。</span><span class="sxs-lookup"><span data-stu-id="82c30-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="82c30-126">有時候它們會初始化且永遠不會變更，而在其他情況下，則會更新每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="82c30-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="82c30-127">如同 C 函式範圍規則，在效果函式範圍外宣告的效果變數在整個效果中都是可見的;只有在該函式內才能看到任何在效果函式內宣告的變數。</span><span class="sxs-lookup"><span data-stu-id="82c30-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="82c30-128">以下是在 BasicHLSL10 中宣告的變數範例。</span><span class="sxs-lookup"><span data-stu-id="82c30-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="82c30-129">效果變數的語法在 [ (Direct3D 10) 的效果變數語法 ](d3d10-effect-variable-syntax.md)中更加詳盡。</span><span class="sxs-lookup"><span data-stu-id="82c30-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="82c30-130">效果紋理取樣器的語法在 [取樣器類型 (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-sampler.md)中更詳盡。</span><span class="sxs-lookup"><span data-stu-id="82c30-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="82c30-131">著色器</span><span class="sxs-lookup"><span data-stu-id="82c30-131">Shaders</span></span>

<span data-ttu-id="82c30-132">著色器是小型的可執行程式。</span><span class="sxs-lookup"><span data-stu-id="82c30-132">Shaders are small executable programs.</span></span> <span data-ttu-id="82c30-133">您可以將著色器視為封裝著色器狀態，因為 HLSL 程式碼會執行著色器功能。</span><span class="sxs-lookup"><span data-stu-id="82c30-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="82c30-134">管線會使用三種不同的著色器。</span><span class="sxs-lookup"><span data-stu-id="82c30-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="82c30-135">頂點著色器-在頂點資料上操作。</span><span class="sxs-lookup"><span data-stu-id="82c30-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="82c30-136">中的一個頂點會產生一個頂點。</span><span class="sxs-lookup"><span data-stu-id="82c30-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="82c30-137">幾何著色器-操作基本資料。</span><span class="sxs-lookup"><span data-stu-id="82c30-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="82c30-138">中的一個基本專案可能會產生0、1或許多基本專案。</span><span class="sxs-lookup"><span data-stu-id="82c30-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="82c30-139">圖元著色器-在圖元資料上操作。</span><span class="sxs-lookup"><span data-stu-id="82c30-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="82c30-140">中的一個圖元會產生1圖元輸出 (除非圖元從轉譯) 挑選出來。</span><span class="sxs-lookup"><span data-stu-id="82c30-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="82c30-141">著色器是區域函式，並遵循 C 樣式函數規則。</span><span class="sxs-lookup"><span data-stu-id="82c30-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="82c30-142">當編譯效果時，會編譯每個著色器，並在內部儲存每個著色器函式的指標。</span><span class="sxs-lookup"><span data-stu-id="82c30-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="82c30-143">編譯成功時，會傳回 ID3D10Effect 介面。</span><span class="sxs-lookup"><span data-stu-id="82c30-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="82c30-144">此時，編譯的效果會採用中繼格式。</span><span class="sxs-lookup"><span data-stu-id="82c30-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="82c30-145">若要瞭解已編譯著色器的詳細資訊，您將需要使用著色器反映。</span><span class="sxs-lookup"><span data-stu-id="82c30-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="82c30-146">這基本上就像是要求執行時間對著色器進行反編譯，然後將資訊傳回給您，以瞭解著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="82c30-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="82c30-147">效果著色器的語法在 [ (Direct3D 10) 的效果 ](d3d10-effect-function-syntax.md)函式語法中是更完整的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="82c30-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="82c30-148">技術與通過</span><span class="sxs-lookup"><span data-stu-id="82c30-148">Techniques and Passes</span></span>

<span data-ttu-id="82c30-149">技術是轉譯行程的集合， (至少必須有一個 pass) 。</span><span class="sxs-lookup"><span data-stu-id="82c30-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="82c30-150">每個效果傳遞 (在轉譯迴圈中的單一傳遞範圍中類似) 定義著色器狀態和轉譯幾何所需的任何其他管線狀態。</span><span class="sxs-lookup"><span data-stu-id="82c30-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="82c30-151">以下是其中一個技巧 (的範例，其中包含 BasicHLSL10 的一個 pass) 。</span><span class="sxs-lookup"><span data-stu-id="82c30-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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
```



<span data-ttu-id="82c30-152">效果著色器的語法更完整地說明 [ (Direct3D 10) 的有效技巧語法 ](d3d10-effect-technique-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="82c30-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c30-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="82c30-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c30-154"> (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="82c30-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
